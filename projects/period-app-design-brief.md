# Period app — design brief

6 October 2026 · Phoebe Hugh

## Overview

We are designing a period tracker that does one thing beautifully: you open it, tap how heavy today's flow is, and you're done in under two seconds.

- **The problem:** popular apps like Flo and Clue have become cluttered, pushy and anxious. Users complain about upgrade pop-ups, paywalled basics, endless symptom grids, fiddly calendars, alarming notifications and privacy worries.
- **Who it's for:** anyone who wants to know when their period is coming and roughly when they ovulate, without the noise. That includes people trying to conceive, people who just want dates, and people noticing changes in their 40s.
- **The promise:** as calm as Headspace, as simple as a light switch, honest about what it knows.
- **Platform:** iPhone first (with Home Screen widget, Lock Screen control and Apple Health sync). Android later.

## Design principles

1. **Calm first.** Soft, rounded, unhurried. Nothing flashes, shouts or nags. If a screen makes someone's heart rate go up, it's wrong.
2. **One thing per screen.** The home screen shows two facts and the log buttons. Everything else is one tap away, never in the way.
3. **Logging is the habit.** Make it nearly effortless: big targets, one tap, works from the widget without opening the app.
4. **Honest, not confident.** Predictions are always ranges that narrow as the app learns. Never a single, falsely precise date.
5. **Forgiving.** Missed days are fine. No streaks, no guilt, no "you haven't logged in 3 days".
6. **Private by design.** No account, no ads, no tracking. Data stays on the phone.
7. **Small and stable.** Resist feature creep. A feature earns its place only if most users would miss it.

## What users hate today, and our answer

| Common complaint | Our answer |
| --- | --- |
| Too pink, flowery, babyish | Warm, non-pink palette; grown-up tone |
| Assumes everyone is a woman trying for a baby | Neutral language; user picks a goal (just tracking / trying to conceive) |
| Upgrade pop-ups on every open | None. App opens straight to today |
| Home screens full of articles, stories, tips | Two facts plus the log buttons |
| Grids of 50+ symptoms | Three optional extras at most, hidden by default |
| Fiddly calendars with separate edit modes and tiny circles | Tap a day to change it; drag to fill a period; big cells; undo |
| Mystery symbols (dotted, solid, teal numbers) | Logged = solid colour, predicted = soft outline, fertile = gentle band; tiny key |
| Lock-screen notifications like "You're fertile today!" | Discreet wording by default; detail only inside the app |
| Alarming language ("HIGH chance", "LATE") | Calm, plain wording |
| Predictions that jump around | Ranges that narrow over time |
| Irregular cycles treated as errors | Irregular is normal; the range just widens |
| Baby content that's hard to escape, painful after a loss | No baby content pushed; pregnancy mode easy to pause or end, with care |
| Long sign-up questionnaires | No account; two questions at most, or import from Apple Health |
| Redesigns that remove features; hard to export | Small, stable app; one-tap export |

## Feature set

### Version 1

1. **One-tap logging:** Mist (spotting), Drizzle, Shower, Downpour, plus "Nothing today". Also from a Home Screen widget and a Lock Screen control.
2. **Import history from Apple Health** on first launch, so predictions work immediately.
3. **Home screen:** cycle day and next period as a range.
4. **Fertile window and likely ovulation,** shown as a range. Can be switched off. Labelled "not contraception".
5. **Ovulation test logging:** one tap for positive or negative; sharpens the fertile window. Optionally reads Apple Watch wrist temperature to confirm ovulation afterwards.
6. **Optional extras, hidden by default:** sex, cramps, clots or flooding.
7. **Calendar:** month and year views.
8. **Gentle notes:** period due soon; period late (suggest a test); things worth mentioning to a GP, only after a pattern repeats; one-tap summary to show a GP.
9. **Privacy:** no account, data on the phone, Face ID lock, optional iCloud backup, writes to Apple Health.

### Later

- Perimenopause view (cycle changes from the 40s)
- Sharing with a partner
- Apple Watch app
- Extra label themes

### Never

- Ads, account sign-up, forums, articles or content feeds, streaks or badges, "cycle syncing" advice

## Screens to design

| Screen | Must show | Notes |
| --- | --- | --- |
| Home (not yet logged) | Date; cycle day (large); next period as a range; slim cycle bar (period, fertile band, today marker); "How's today?" with four big flow tiles; quiet "Nothing today" | The whole app for most days. Nothing else on it |
| Home (logged) | Calm confirmation card with the chosen level and a kind line; "Change" button | Gentle animation and soft haptic on tap. No confetti |
| Calendar: month | One month per screen, swipe between; logged days as colour wash by flow; predicted as outline; fertile band; tiny key | Tap a day: the same four tiles slide up. Drag across days to fill a period. Undo after every change. Day cells at least 44pt |
| Calendar: year | A grid of small coloured squares ("year in pixels") | Mostly for looking; beautiful at a glance |
| Optional extras | Sex, cramps, clots or flooding, ovulation test (positive / negative) | Off by default; turned on in settings; one tap each |
| Notes | Period due soon; period late; GP summary; pattern notes | Cards, never pop-ups or red warnings |
| GP summary | Last 6 cycles: lengths, period lengths, flow pattern, any flags | Shareable PDF; plain and clinical-friendly |
| Widget and Lock Screen | Log today in one tap; optional cycle day | Must be discreet: user can hide what it shows |
| Onboarding | Import from Apple Health, or enter last period start; choose goal | Two screens max. No account |
| Settings | Goal, fertile window on/off, extras on/off, reminders, Face ID lock, backup, export, theme | Plain list |

What each screen must do is set; how it looks and is laid out is up to you. The rough home-screen mockup linked in the last section is only a sketch of the idea.

## Look and feel: goals for the designer

The visual language is yours to create. This section sets the goals and the guardrails, not the answer.

### How it should feel

- **Calm.** Opening it should feel like a deep breath, the way Headspace does. Nothing urgent, nothing shouting.
- **Warm and kind.** Like a friend who gets it, not a medical device and not a toy.
- **Colourful but pared back.** Joyful colour used with restraint; lots of space; one thing at a time.
- **Grown-up.** Confident and modern. Something you'd be happy for anyone to glimpse on your phone.
- **Effortless.** Logging should feel almost physical and satisfying, so it becomes a habit.

### Goals to achieve

1. Someone can log today in one tap, in under two seconds, without reading anything.
2. The four flow levels are instantly distinguishable, including for colour-blind users and at a glance on a widget.
3. Logged, predicted and fertile days are impossible to confuse on the calendar.
4. Predictions read as gentle ranges, not hard dates.
5. Health notes (GP flags, a late period) feel caring and calm, never alarming.
6. The app has a recognisable personality of its own in a category full of look-alikes.

### Guardrails

- **Avoid** the period-app clichés: pink and purple, flowers, petals, hearts, glitter, blood-red.
- **Avoid** clinical coldness: stark white, hospital blues, charts on the home screen.
- **Avoid** gamification: confetti, badges, streak counters.
- **Must** meet accessibility basics (see the next sections): contrast, 44pt targets, Dynamic Type, dark mode, never colour alone.
- **Must** work on a small widget and Lock Screen, not just full screen.

### Open to exploration

- Palette, type, iconography, illustration style, motion and haptics.
- The flow labels. "Mist / Drizzle / Shower / Downpour" (a weather theme) is our working favourite; feel free to push it, or propose something better. Whatever the labels, the data underneath is spotting / light / medium / heavy.
- How the cycle is visualised: a bar, a ring, something new.
- Whether a theme or illustration system could give the app its personality.

### For inspiration, not to copy

Headspace (overall calm), Timepage (colour-wash calendar), Daylio's Year in Pixels (a year at a glance), How We Feel (soft, colourful and calm), Stardust (dreamy mood), Structured (colourful without clutter). Flo's calendar is a useful anti-example: hard pink circles, harsh contrast and too many symbols.

## Voice and copy

Warm, plain and brief, like a kind friend. Never clinical, never alarming, never cutesy. The lines below show the tone; they are examples, not final copy.

| Moment | Say | Not |
| --- | --- | --- |
| Logging prompt | How's today? | Log menstrual flow |
| After logging | Shower — logged. Be kind to yourself today. | Great job! 3-day streak! |
| Prediction | Next period around 26–29 Oct | Period in 21 days |
| Fertile window | Likely fertile 10–15 Oct | HIGH chance of pregnancy today |
| Period late | Your period's a few days later than usual. Might be worth taking a test. | Your period is LATE |
| GP pattern | Your cycles have been a bit longer lately. Might be worth mentioning to your GP. | Warning: abnormal cycle |
| Missed days | (say nothing; just ask about today) | You haven't logged in 3 days |
| Lock-screen notification | Quick check-in | You're fertile today! |
| Contraception | Not a form of contraception. | (never imply it is) |

## Accessibility and inclusion

- **Colour is never the only signal.** Flow levels also differ by drop count and lightness; logged vs predicted differ by fill vs outline.
- **Contrast:** body text at least 4.5:1; large text at least 3:1.
- **Touch targets** at least 44pt, including calendar days.
- **Dynamic Type** supported throughout; layouts must not break at larger sizes.
- **VoiceOver:** every tile and day reads its meaning ("Tuesday 6 October, Shower, logged").
- **Reduce Motion:** swap animations for simple fades.
- **Dark mode:** a warm dark version, not pure black.
- **Inclusive language:** no assumptions about gender or goals; "you", never "ladies".

## Science the design must respect

The numbers below come from our research reports (checked against NHS, NICE, FIGO and peer-reviewed studies, 6 October 2026). Designs need room for ranges and gentle caveats.

- **Predictions are ranges.** Average cycle is about 29 days and varies; a single date would be wrong most of the time.
- **Ovulation sits about 12–13 days before the next period,** not the textbook 14. The fertile window is the ~6 days ending on ovulation day.
- **Dates alone can't pinpoint ovulation.** The best single-day guess is right only about 1 in 5 times, so the fertile window must look like a soft band, not a precise day. Ovulation tests make it much more accurate.
- **GP notes appear only after a pattern repeats** over 2–3 cycles. Triggers: cycles shorter than 24 or longer than 38 days; cycle length varying by more than 7–9 days; periods longer than 8 days; no period for 3 months; heavy-period signs (changing pads or tampons every 1–2 hours, clots larger than a 10p coin, flooding); bleeding between periods.
- **Never contraception.** The fertile window must always carry that label.
- **Flow data model:** one record per day (none, spotting, light, medium, heavy), matching Apple Health and Android Health Connect.

## Deliverables and open questions

**Starting point:** a rough clickable home-screen mockup (https://claude.ai/artifact/CEV4oxE9DneuY34ppViBHp). Treat it as a sketch of the idea, not a finished design.

**Deliverables**

- [ ] Visual direction: two or three moodboards or style options to choose from
- [ ] Flow tile and drop icon set (all four levels plus "Nothing today")
- [ ] Key screens in light and dark: home (both states), calendar month and year, tap-to-edit sheet, notes, GP summary, onboarding, settings
- [ ] Home Screen widget and Lock Screen control
- [ ] Clickable prototype of the logging flow
- [ ] Colour, type and spacing tokens ready for development
- [ ] App icon and name lockup

**Open questions**

- What is the app called?
- Should the cycle bar on the home screen stay, or is it one thing too many?
- How discreet should the widget be by default: show cycle day, or nothing but the log button?
- Should label themes (weather, cheeky) be in version 1 or later?
- How should pregnancy be handled when a test is positive: a gentle pause, or a simple pregnancy mode?
