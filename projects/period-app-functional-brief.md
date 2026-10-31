# Period app: functionality brief

Version 0.1 · 31 October 2026 · Phoebe Hugh
Companion to `projects/period-app-design-brief.md` (look, feel and copy). Science sources: `reports/Cycle science and ovulation prediction.md`.

## 1. What it is

An iPhone period tracker whose main job is one-tap daily flow logging. From that log it predicts the next period and fertile window as honest ranges, gently flags patterns worth mentioning to a GP, and keeps all data private on the phone.

**Platform:** iOS 18+ (SwiftUI), iPhone first. Home Screen widget, Lock Screen / Control Centre control, Apple Health sync. Android later.

**Success measures**
- Logging a day takes one tap and under 2 seconds (app or widget).
- At least 70% of active users log on most bleeding days after 3 months.
- Next-period range contains the actual start at least 80% of the time for users with 3+ cycles.

## 2. Users and goals

On first launch the user picks a goal (changeable in Settings):

| Goal | What changes |
| --- | --- |
| Just tracking | Fertile window hidden by default |
| Trying to conceive | Fertile window shown; ovulation test and sex logging switched on; "take a test" prompt when late |
| Noticing changes (40s+) | Later: perimenopause view. For v1, same as Just tracking |

## 3. Data model

One record per calendar day (local date, no time zone drift).

| Field | Values | Notes |
| --- | --- | --- |
| flow | none · spotting · light · medium · heavy | UI labels: Nothing today · Mist · Drizzle · Shower · Downpour |
| ovulationTest | none · negative · positive | Optional extra |
| sex | true/false | Optional extra |
| cramps | true/false | Optional extra |
| clotsOrFlooding | true/false | Optional extra; feeds heavy-bleeding notes |
| source | app · widget · healthImport | For de-duplication |

Derived, never entered:
- **Period** = a run of days with flow light or heavier. Spotting alone never starts a period. A single gap day inside a run doesn't break it.
- **Period start** = first day of a period with at least 2 non-bleeding days before it.
- **Cycle** = from one period start to the day before the next. Cycle length in days.

Settings: goal, fertile window on/off, extras on/off, reminders, notification wording (discreet/detailed), Face ID lock, iCloud backup on/off, Apple Health sync on/off, optional age band (for GP thresholds), optional "trying since" month.

## 4. Features (version 1)

### 4.1 Logging
- Home screen asks "How's today?" with four flow tiles plus "Nothing today". One tap saves, shows a calm confirmation with Change/undo.
- Logging a past day: tap it in the calendar; the same tiles appear. Drag across days to fill a whole period with one level (then adjust single days).
- Undo toast after every change (5 seconds).
- Optional extras (if switched on) appear as small toggles under the confirmation card, never before it.
- No streaks, no "missed day" prompts. Unlogged days are simply unknown, treated as no flow outside a predicted period.

### 4.2 Widget and Lock Screen
- Interactive Home Screen widget (small and medium): four flow buttons that log without opening the app; optional cycle day.
- Lock Screen / Control Centre control that opens straight to the logging tiles.
- Privacy: by default the widget shows no cycle or fertility info; the user can choose to show cycle day.

### 4.3 Home screen
- Date, cycle day (large), cycle ring (period arc, fertile arc, today marker).
- "Next period" as a date range; "Likely fertile" as a date range (if enabled).
- Logging tiles or the logged card.
- Nothing else: no articles, tips, charts or upsells.

### 4.4 Calendar
- Month view: one month per screen, swipe between. Logged days as filled colour by flow; predicted period days as outline; fertile window as a soft band; today highlighted; tiny key.
- Year view: 12 small month grids of coloured squares, read-only; tap a month to open it.

### 4.5 Predictions (see section 5)
- Next period start as a range; likely ovulation day as a range; fertile window.
- Every prediction display says "estimate" somewhere nearby; the fertile window always carries "not contraception".

### 4.6 Gentle notes
Shown as cards on Home under the logging area, dismissible, never pop-ups.
- **Period due soon:** from 2 days before the predicted range starts.
- **Late:** 3+ days past the end of the predicted range with no flow logged: "Your period's a few days later than usual." If goal is Trying to conceive, or sex was logged in the fertile window: "Might be worth taking a test."
- **GP pattern notes:** see section 6.
- **Trying for a while:** if goal is TTC and "trying since" is 12+ months ago (or age band 36+ at any time): "It might be worth talking to your GP about fertility support."

### 4.7 GP summary
One tap from Settings or a GP note: a PDF covering the last 6 cycles (start dates, cycle lengths, period lengths, flow per day, extras logged, any active notes). Plain, clinical-friendly, shareable via the share sheet.

### 4.8 Onboarding (max 2 screens)
1. Import from Apple Health (one button), or enter last period start date (and optionally a typical cycle length).
2. Choose goal. Done. No account, no email.

### 4.9 Privacy and data
- All data stored locally (SwiftData). No account, no analytics, no third-party SDKs, no ads.
- Optional Face ID / passcode lock on open.
- Optional iCloud backup via the user's private CloudKit database.
- Apple Health: read flow history on import; write flow (with cycle-start metadata on period starts) and spotting going forward, if allowed.
- Export: CSV of all days; delete-all-data button with confirmation.

### 4.10 Notifications
- Default wording is discreet: "Quick check-in". Detailed wording ("Your period may start in the next few days") is opt-in.
- Types: period due soon (once), late (once), optional gentle daily check-in only on predicted or active period days.
- Never more than one notification a day.

## 5. Prediction engine

All rules work from period starts derived from the daily log.

**Next period**
1. Take the last 6 completed cycles. Exclude any cycle longer than 1.8x the median of the others (likely a missed log); ask the user once, gently, if it was a missed log.
2. Predicted length L = median of included cycles. With fewer than 3 cycles, blend with a population prior of 29 days: L = (n x median + (3 - n) x 29) / 3. With no cycles, use the user's typical length if given, else 29.
3. Range half-width W = max(2, ceil(standard deviation)), capped at 7. With fewer than 3 cycles, W = 3.
4. Next period range = last start + L - W to last start + L + W.

**Ovulation and fertile window**
1. Estimated ovulation = predicted next start - 13 days (range: -15 to -11, widened by W).
2. Fertile window = 5 days before the ovulation range start through 1 day after the ovulation estimate.
3. Positive ovulation test this cycle: ovulation = test day + 1; fertile window = test day - 2 to test day + 2. Overrides the estimate for this cycle only.
4. Optional (v1.1): Apple Watch wrist temperature from Health. A sustained rise (3 nights at least 0.2 C above the previous 6) confirms ovulation happened about 1 day before the rise and tightens the next-period prediction (next start = ovulation + 13, W = 2).

**Rules**
- Never show a single date for anything predicted.
- Irregular cycles simply widen W; never call them errors.
- Unit-test the engine against fixed fixtures (regular, irregular, missed log, first cycle, positive LH test).

## 6. GP pattern notes

Only shown after a pattern appears in at least 2 of the last 3 cycles (except the 90-day rule). Wording is calm: "Might be worth mentioning to your GP."

| Pattern | Rule |
| --- | --- |
| Short or long cycles | Cycle under 24 or over 38 days |
| Irregular | Longest minus shortest of last 6 cycles over 7 days (age 26-41) or over 9 days (other ages or age unknown) |
| Long periods | Period over 8 days |
| No period | 90+ days since last period start (and not pregnant) |
| Heavy bleeding | Clots or flooding logged, or 3+ heavy days, in a period |
| Bleeding between periods | Spotting or flow on 2+ days outside a period |

Thresholds are from FIGO 2018, NHS and NICE (checked October 2026); recheck before launch.

## 7. Pregnancy

- If a period is late and the user marks "I'm pregnant" (from the late note or Settings), predictions and notes pause. A calm "Paused" state shows on Home. No baby content, no countdowns.
- "End pregnancy mode" is one tap, with no questions asked and gentle copy. Tracking resumes from the next logged period.

## 8. Out of scope for v1

Perimenopause view, partner sharing, Apple Watch app, label themes, Android, symptom grids, content or articles, community, accounts, contraception claims.

## 9. Acceptance checklist

- [ ] Log today from Home in one tap; from the widget without opening the app.
- [ ] Edit any past day in two taps; drag to fill a period; undo works.
- [ ] Apple Health import produces the same period starts as Health shows.
- [ ] Predictions always show ranges; engine passes all fixture tests.
- [ ] Positive ovulation test moves the fertile window for that cycle only.
- [ ] GP notes fire only on repeated patterns; never on a single cycle (except 90 days).
- [ ] No network calls except optional iCloud; verified with a network monitor.
- [ ] VoiceOver reads every tile and calendar day; Dynamic Type to the largest size doesn't break layouts; Reduce Motion respected; dark mode.
- [ ] Discreet notifications by default.
