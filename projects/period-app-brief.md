# Period app: design brief (working notes)

Running list of what Phoebe wants for the one-tap period tracker. Research behind it:
`reports/Cycle science and ovulation prediction.md`, `reports/Period tracking apps compared.md`.

## Core idea
- Unbelievably simple: open the app, tap today's flow, done. Should become a habit.
- Clean, pared-back design that's still colourful. Avoid the clichéd period-app pink.

## Flow labels
- Shortlisted: Drizzle / Shower / Downpour (weather theme), with 1/2/3 filling drop icons; "Mist" for spotting.
- Store as light / medium / heavy underneath so it syncs with Apple Health.
- Maybe offer selectable themes later (e.g. a cheeky "Fine / Annoying / Crime scene").

## Feel
- As calm as Headspace: soft, rounded, unhurried, warm and reassuring, never clinical or alarming.

## From the research
- No daily streaks (they break every month and make people quit). Forgive missed days.
- Show the next period as a range, not a single date.
- Gentle "worth mentioning to your GP" notes only after a pattern repeats.
- No account, no tracking, data stays on the phone.

## Proposed feature set (draft, 6 Oct 2026)

### Version 1: the core
1. One-tap logging: Mist / Drizzle / Shower / Downpour; Home Screen widget + Lock Screen control; tap any calendar day to fix it.
2. Import history from Apple Health on day one (so predictions work immediately).
3. Home screen: cycle day + next period as a range ("around 26–29 Oct").
4. Fertile window + likely ovulation as a range, using ~12–13 day luteal phase (not 14). Toggle on/off. Labelled "not contraception".
5. Ovulation test logging (one tap: positive / negative) to sharpen the window. Optional Apple Watch wrist temperature from Apple Health to confirm afterwards.
6. A few optional extra taps, hidden by default: sex, cramps, clots/flooding.
7. Calm calendar: month + year view, coloured dots.
8. Gentle notes: period due soon; period late → suggest a test; GP flags only after a pattern repeats; one-tap GP summary.
9. Private by design: no account, data on phone, Face ID lock, optional iCloud sync, writes to Apple Health.

### Later
- Perimenopause view (cycle-length changes from 40s), partner sharing, Apple Watch app, extra label themes.

### Never
- Ads, account sign-up, community/forums, content feeds, streaks/badges, "cycle syncing" advice.

## Calendar (avoid the usual fiddliness)
- Calendar is mainly for looking; logging happens on the home screen/widget.
- To fix a day: tap it → the same four big flow buttons slide up (plus "None"). No separate edit mode.
- Fill a whole period at once by dragging a finger across days.
- Big day cells; one month per screen, swipe between months.
- Logged days = solid colour wash by flow; predicted days = soft outline/tint; fertile window = gentle band. Tiny key, no mystery symbols.
- Undo toast after every change.
- Visual references: Timepage (colour-wash month), Daylio Year in Pixels (year view), How We Feel (soft palette), Stardust (mood).

## Common design complaints → how we avoid them
- Pink, flowery, babyish → warm non-pink palette, grown-up tone.
- Gendered / assumes everyone is a woman trying for a baby → neutral language; user picks their goal (just tracking / trying to conceive).
- Pop-ups & upsells on open → none. App opens straight to today.
- Cluttered home (articles, stories, tips) → two facts + log buttons only.
- Huge symptom grids → max ~3 optional extras.
- Embarrassing lock-screen notifications ("fertile today!") → discreet wording by default (e.g. "Quick check-in"), detail only inside app; widget can hide info.
- Anxious language ("high chance of pregnancy", "period LATE") → calm, plain wording.
- Overconfident single-date predictions that keep jumping → ranges that narrow as data grows.
- Long onboarding + forced sign-up → no account; 2 questions max, or import from Apple Health.
- Pregnancy/baby content that's hard to escape (painful after a loss) → no baby content pushed; pregnancy mode easy to pause/end with care.
- Irregular cycles treated as errors → irregular is normal; just widen the range.
- Redesigns that remove features / hard to export → keep it small and stable; one-tap export (CSV/PDF).
