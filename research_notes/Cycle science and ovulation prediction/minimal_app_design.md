# Minimal one-tap period tracker: design patterns and evidence

Scope: research to inform a future simple iOS build (open app, tap light / medium / heavy, done). Research date 5 Oct 2026.

**Proxy and source notes:** ncbi.nlm.nih.gov, washington.edu and knowledge.insead.edu were blocked by the egress proxy. Findings from those sources (Epstein 2017 CHI menstrual-tracking paper, UW press release, INSEAD streaks article) come from **search-result snippets only**, not full text. Apple developer docs were fetched in full by adding `.md` to the URL. That trick is useful for the build itself. Android Health Connect docs were fetched but only summarised.

## Existing minimalist period trackers and one-tap loggers: what works, what doesn't

### Takeaway
The privacy-first, open-source trackers (drip, Euki, Menstrudel, Mensinator) set the standard to beat on privacy: local storage, no account, neutral styling. Most still pile on symptom, fertility and mood logging, though. The best model for the "one tap and done" feel comes from outside the period-app category: Streaks (one big tap-and-hold button per habit) and Daylio (a two-tap entry). Apple's Cycle Tracking already makes a flow log possible in about 3–4 taps on Watch, so a new app has to be faster than that.

### Cited Findings
- **drip** (Heart of Code e.V.) is non-commercial and open source, stores all data locally, has no servers, and uses gender-neutral UI with "neutral and rather encouraging language". It deliberately avoids the typical pink palette. It is feature-heavy, though: it uses the sympto-thermal method and tracks bleeding, fertility, sex, mood and pain, with graphs and password-protected import/export. — [dripapp.org](https://dripapp.org/); [Superrr Feminist Tech Fellow: drip](https://superrr.net/feministtech/fellow/drip/); [App Store: drip](https://apps.apple.com/app/id1584564949); [Bloomberg 2022](https://prod.cm.bloomberg.com/news/articles/2022-08-31/free-period-tracking-app-drip-offers-privacy-for-menstrual-data) (search snippet)
- **Euki** is a nonprofit, open-source app with local storage and no account. It got the only perfect 10/10 in Mozilla's privacy review of six trackers, ahead of Clue 8, Flo 7, Period Calendar 6, Spot On 5 and **Stardust 2**. Stardust was found sharing birthdates, birth-control method, pregnancy status, moods and symptoms with the analytics firm RudderStack. — [Digital Trends on Mozilla review](https://www.digitaltrends.com/phones/stardust-flo-and-other-popular-period-trackers-flunk-mozillas-latest-privacy-test/); [The Star (Kenya), Jul 2026](https://www.the-star.co.ke/news/world/2026-07-19-how-period-trackers-share-your-private-details) (snippets)
- **Menstrudel** is a Flutter app (on the iOS App Store and F-Droid) that is fully offline with no accounts or tracking. It is open source. It logs start dates, symptoms and flow intensity, and predicts the next cycle. — [GitHub J-shw/Menstrudel](https://github.com/J-shw/Menstrudel); [F-Droid RFP](https://gitlab.com/fdroid/rfp/-/issues/3271) (snippets)
- **Mensinator** offers a "clean and intuitive interface", no sign-up, MIT licence, and is Android/F-Droid only. — [AlternativeTo period trackers](https://www.alternativeto.net/feature/period-tracker/) (snippet)
- **Apple Cycle Tracking:** on Watch, logging a period means tap Log → Period → flow level → confirm. On iPhone it is Health → Browse → Cycle Tracking → select day → Period → choose option → Done. Predictions can use heart-rate and wrist-temperature data. — [Apple Support: Cycle Tracking on Apple Watch](https://support.apple.com/en-mn/guide/watch/apd26429adf0); [Apple Support: Log menstrual cycle in Health](https://support.apple.com/en-jo/guide/iphone/iph51a822b18/ios); [MacStories review](https://www.macstories.net/stories/apples-cycle-tracking-a-personal-review/) (snippets)
- **Streaks** (Crunchy Bagel, Quentin Zervaas) is an Apple Design Award winner. Each habit is shown as "a big button – just tap and hold to mark as done". It allows up to 24 tasks, syncs via iCloud, auto-completes from Health, and offers 78 colour themes and 600+ icons. — [App Store: Streaks](https://apps.apple.com/no/app/id963034692); [Apple "Apps We Love"](https://apps.apple.com/be/story/id1272004658) (snippets; I could not confirm the year of the ADA)
- **Daylio** makes an entry in "just two taps": a mood on a 5-point scale, then optional activities. One review credits that simplicity because it lets people log "even when they are at their worst and without being overwhelmed". — [Wikipedia: Daylio](https://en.wikipedia.org/wiki/Daylio); [mHealth journal review](https://mhealth.amegroups.org/article/view/11509/html)
- **User complaints about period apps generally** (Epstein et al., CHI 2017; 2,000 app reviews, a survey of 687 people and 12 interviews):
  - Apps are helpful but become ineffective when predictions are inaccurate.
  - Designs can exclude gender and sexual minorities.
  - Apps ignore life stages (young adulthood, pregnancy, menopause).
  - Press coverage summarised it as apps being "too pink".

  — [Epstein et al. 2017, PMC5432133](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5432133/) (blocked; snippet only); [PDF](https://homes.cs.washington.edu/~jfogarty/publications/chi2017-menstrualtracking.pdf); [ICT&health: "too pink"](https://www.icthealth.org/news/apps-tracking-menstrual-cycle-lack-functionality-and-are-too-pink)

### Inferences
- The gap in the market is an app that pairs Euki/drip-level privacy with Streaks/Daylio-level speed: a single screen with three large buttons. No app I found clearly fills this on iOS. Menstrudel is the closest, but it adds symptoms and predictions.
- Apple's own flow log takes about 4 taps after opening an app. A dedicated app needs zero navigation, with the buttons on the first screen and ideally a widget or control (see below), to beat it.
- Inaccurate predictions were the main frustration in Epstein 2017. If the app shows any prediction, it should show it humbly (a range, not a date) or leave it out at first.
- Tyd, Periodical and Bearable were not covered in the sources I found (see Gaps).

### Gaps
- No reliable sources found on **Tyd**, **Periodical**, **Bearable** or the **(Not Boring)** apps in this pass. They would need App Store pages or design write-ups.
- No Dribbble, Mobbin or Medium case studies were retrieved, for lack of tool-call budget.
- I couldn't read the full text of Epstein 2017 (NCBI and UW blocked), so its specific design recommendations and figures are missing.

## Habit-formation evidence: what applies to a ~5-days-a-month logging habit

### Takeaway
The evidence favours making the action trivially easy (Fogg's "Ability"), anchoring it to an existing routine, and forgiving lapses. Lally found one missed day doesn't derail habit formation. Self-tracking research treats lapsing and resuming as normal. Streaks motivate while intact but cause drop-off when broken, so streaks are a poor fit for an intermittent behaviour like period logging.

### Cited Findings
- **Lally et al. 2010 (UCL):** habits took on average **66 days** to form, with a range of **18–254 days**. Lally: "missing one opportunity did not significantly impact the habit formation process, but people who were very inconsistent in performing the behaviour did not succeed in making habits." — [University of Surrey: interview with Dr Pippa Lally](https://www.surrey.ac.uk/news/does-it-really-take-66-days-form-habit-we-asked-expert-dr-pippa-lally); [The Behavioral Scientist](https://www.thebehavioralscientist.com/articles/how-long-to-form-a-habit)
- **Fogg Behavior Model, B = MAP:** behaviour happens when Motivation, Ability and a Prompt coincide. Its key design insight is that raising Ability (making it easier) is more effective and sustainable than raising Motivation. The Tiny Habits recipe is "After I [anchor], I will [tiny behaviour]", followed by an immediate **celebration**. People "change best by feeling good, not by feeling bad". — [The Behavioral Scientist: B=MAP](https://www.thebehavioralscientist.com/?p=3058); [Coaching for Leaders PDF](https://coachingforleaders.com/wp-content/uploads/free/bj-fogg-tiny-habits.pdf) (secondary summaries)
- **Hook model (Eyal):** Trigger → Action → Variable Reward → Investment. Eyal's own ethics test asks "Would you use it?" and "Is it making people's lives better?" — [Medium explainer](https://medium.com/@omforux25/the-hook-model-explained-how-to-build-habit-forming-products-f261abb3fb03); [dsebastien concept note](https://concepts.dsebastien.net/concept/hook-model/) (secondary)
- **Lived informatics model (Epstein et al., UbiComp 2015):** based on surveys of 105, 99 and 83 trackers (activity, finance, location) and 22 interviews. It extends older models to cover deciding to track, selecting a tool, collection/integration/reflection, and explicitly **lapsing and resuming** tracking. — [Epstein 2015 PDF](https://my.eng.utah.edu/~cs5540/au16/readings/PersonalInformatics-Epstein2015.pdf); [Self-Research library entry](https://library.selfresearch.org/research/a-lived-informatics-model-of-personal-informatics/)
- A follow-up line of work covers designing for **life after abandonment** ("Beyond Abandonment to Next Steps", Epstein et al.). — [Self-Research library](https://library.selfresearch.org/research/beyond-abandonment-to-next-steps-understanding-and-designing-for-life-after-personal-informatics-tool-use/) (title/snippet only)
- **Streaks (Silverman & Barasch, Journal of Consumer Research, 2023; seven studies):**
  - Showing an *intact* streak in a log increases later engagement, compared with showing a *broken* one. The effect depends only on how the log represents the behaviour, not on actual past behaviour.
  - The effect is amplified when people blame the break on themselves, and weakened when they can "repair" the streak.
  - The authors advise against messages that highlight failure, since people "just drop off once their streaks are broken".

  — [UD Space: On or Off Track](https://udspace.udel.edu/handle/19716/34160); [CU Boulder research summary](https://www.colorado.edu/business/faculty-research/2023/04/19/or-track-how-broken-streaks-affect-consumer-decisions); [UDaily 2024](https://udel.edu/udaily/2024/march/power-of-streaks-motivation-jackie-silverman)
- A blog claims "a 2021 study in Computers in Human Behavior" linked rigid streaks to guilt, anxiety and abandonment. **Unverified:** the source is a secondary habit-app blog and the original paper was not found. Treat with caution. — [yumuuv blog](https://yumuuv.com/blog/psychology-of-streaks)

### Inferences
- **Streaks are a mismatch for period logging.** The behaviour only happens on bleeding days (roughly 3–7 days per cycle), so a daily streak would "break" every month by design. In Silverman & Barasch's terms, that is a highlighted broken streak, which suppresses engagement. Better alternatives:
  - count cycles logged rather than consecutive days
  - show a gentle "period complete" state
  - frame non-period days as "nothing to log" rather than "missed"
- **Apply Fogg directly:** make Ability as high as possible (one tap from a widget or lock screen) and anchor to an existing routine, e.g. a prompt the user chooses at morning/bathroom time. A tiny celebration (a haptic tick plus a satisfying colour fill) can stand in for the Tiny Habits celebration.
- The Hook model's **variable reward** is ethically dubious for a health log. Use predictable, calm feedback instead. A possible "investment" analogue is a slowly building, beautiful cycle history.
- Following Lally and lived informatics, treat missed days as normal. Allow retroactive logging ("yesterday was medium") and never show guilt messaging.
- **Gentle reminders:** this pass found no dedicated HCI paper on notification design for trackers. A sensible default from the cited evidence:
  - reminders off by default, or only switched on once a period has started
  - one quiet prompt a day only while a period is in progress
  - stop automatically after 1–2 days with no logs, assuming the period has ended

### Gaps
- I didn't find a peer-reviewed study specifically on **reminder/notification fatigue** in self-tracking apps.
- I didn't verify the alleged 2021 *Computers in Human Behavior* streak study.
- No data was found on abandonment rates specific to period-tracking apps.

## Flow logging standards: HealthKit and Health Connect (for sync)

### Takeaway
Both platforms model flow as roughly **unspecified / light / medium / heavy** (Apple also has **none**). That maps exactly onto a light / medium / heavy UI, so syncing is straightforward. Apple requires a "cycle start" boolean on each sample. On iOS 18+ Apple deprecated the old `HKCategoryValueMenstrualFlow` enum in favour of `HKCategoryValueVaginalBleeding`, which has the same cases.

### Cited Findings
- **`HKCategoryTypeIdentifier.menstrualFlow`** (iOS 9+, watchOS 2+):
  - Samples **must include `HKMetadataKeyMenstrualCycleStart`**.
  - You can log the whole period as one sample (cycle start = true, with start and end dates), or as **multiple samples, one per day**, with only the first sample set to true and the rest false.
  - Different samples can carry different flow values to record changes over the period.

  — [Apple Developer: menstrualFlow](https://developer.apple.com/documentation/healthkit/hkcategorytypeidentifier/menstrualflow)
- **`HKCategoryValueMenstrualFlow`** cases: `unspecified`, `none`, `light`, `medium`, `heavy`. Its availability is listed as **iOS 9.0–18.0** (watchOS 2–11), i.e. deprecated as of iOS 18. — [Apple Developer: HKCategoryValueMenstrualFlow](https://developer.apple.com/documentation/healthkit/hkcategoryvaluemenstrualflow)
- **`HKCategoryValueVaginalBleeding`** (iOS 18+, watchOS 11+) has the cases `unspecified`, `light`, `medium`, `heavy` and `none`. It is used for bleeding-related category types, including `bleedingDuringPregnancy` and `bleedingAfterMenopause`. — [Apple Developer: HKCategoryValueVaginalBleeding](https://developer.apple.com/documentation/healthkit/hkcategoryvaluevaginalbleeding)
- HealthKit also has `intermenstrualBleeding` (spotting between periods; the Health app labels it "spotting"), plus a `persistentIntermenstrualBleeding` identifier. — [Apple Developer: persistentIntermenstrualBleeding](https://developer.apple.com/documentation/healthkit/hkcategorytypeidentifier/persistentintermenstrualbleeding.md) (search result); [WWDC 2015 "What's new in HealthKit"](https://devstreaming-cdn.apple.com/videos/wwdc/2015/203bxvbtrom9t1t/203/203_whats_new_in_healthkit.pdf?dl=1)
- **Android Health Connect:**
  - `MenstruationFlowRecord` (instantaneous) has `FLOW_UNKNOWN`, `FLOW_LIGHT`, `FLOW_MEDIUM` and `FLOW_HEAVY`.
  - Related records: `MenstruationPeriodRecord` (an interval covering the period) and `IntermenstrualBleedingRecord` (spotting).
  - The platform API was added in API level 34.

  — [Android Developers: MenstruationFlowRecord](https://developer.android.com/reference/kotlin/androidx/health/connect/client/records/MenstruationFlowRecord); [MenstruationFlowType (API 34)](https://developer.android.google.cn/reference/kotlin/android/health/connect/datatypes/MenstruationFlowRecord.MenstruationFlowType)

### Inferences
- **Recommended local data model:** one record per calendar day, with these fields:
  - `date` (local day, not a timestamp)
  - `flow` ∈ {light, medium, heavy}, plus optionally `spotting` and `none`
  - `isCycleStart` (derived: the first flow day after a gap of N or more days)
  - `createdAt`, `updatedAt`

  This maps 1:1 to HealthKit daily samples and to Health Connect `MenstruationFlowRecord`. It can also produce a `MenstruationPeriodRecord` interval.
- Write to HealthKit as one sample per day with the cycle-start metadata. Use `HKCategoryValueVaginalBleeding` on iOS 18+ (and the old enum only if supporting iOS 17 or earlier). Then Apple's Cycle Tracking predictions work for free, and the app doesn't have to own predictions at all.
- A hidden "spotting" option (e.g. long-press) keeps the three-button UI clean while still syncing `intermenstrualBleeding`.
- Make HealthKit sync **opt-in**. It sends data into iCloud Health (which Apple encrypts end-to-end, though I didn't verify that here), so it is a privacy choice for the user.

### Gaps
- I didn't confirm whether Apple's docs give a formal reason for deprecating `HKCategoryValueMenstrualFlow`, or whether `menstrualFlow` now officially expects `HKCategoryValueVaginalBleeding` raw values. The raw values appear identical in case order, but this needs a check in Xcode.
- The full Health Connect field list (e.g. `time`, `zoneOffset`, metadata) wasn't returned verbatim.

## Visual design: colourful but minimal, accessibility, widgets and Watch

### Takeaway
Avoid "pink by default". Epstein 2017 and the press flag it, and drip markets its neutrality. Use a small, bold palette in which the three flow levels differ in **lightness and shape/fill**, not hue alone. iOS 17/18 interactive widgets and Control Center / Lock Screen controls (App Intents) make true one-tap logging possible without opening the app.

### Cited Findings
- Criticism that period apps are "too pink" and stereotyped appears in coverage of Epstein 2017. drip and similar apps position their gender-neutral, non-pink design as a feature. — [ICT&health](https://www.icthealth.org/news/apps-tracking-menstrual-cycle-lack-functionality-and-are-too-pink); [MetaFilter "The Unbearable Pinkness of Bleeding"](https://metafilter.com/166770/The-Unbearable-Pinkness-of-Bleeding); [ExpressVPN on drip](https://www.expressvpn.com/blog/period-tracking-apps/) (snippets)
- **Okabe-Ito colour-blind-safe palette:** #E69F00 orange, #56B4E9 sky blue, #009E73 bluish green, #F0E442 yellow, #0072B2 blue, #D55E00 vermillion, #CC79A7 reddish purple, #000000 black. It stays distinguishable across common types of colour-vision deficiency. — [ConceptViz: Okabe-Ito reference](https://conceptviz.app/blog/okabe-ito-palette-hex-codes-complete-reference); [NYU Siegal lab palette](https://siegal.bio.nyu.edu/color-palette/)
- Streaks shows that "colourful but minimal" can work: big single buttons, 78 colour themes and icon-led tasks. — [App Store: Streaks](https://apps.apple.com/no/app/id963034692)
- **Interactive widgets (iOS 17+):** widget buttons and toggles run an **App Intent** without launching the app. — [Blake Crosley: iOS 26 widget and control surface](https://blakecrosley.com/blog/ios-26-widget-and-control-surface)
- **Control widgets (iOS 18+):** these appear in Control Center, on the Lock Screen, on the Action button and in Shortcuts. They are buttons or toggles built with `ControlWidgetButton` / `ControlWidgetToggle` and `StaticControlConfiguration` / `AppIntentControlConfiguration`. — [Apple: Creating controls to perform actions across the system](https://developer.apple.com/tutorials/data/documentation/widgetkit/creating-controls-to-perform-actions-across-the-system.md); [WWDC24 10157 notes](https://wwdcnotes.com/documentation/wwdc24-10157-extend-your-apps-controls-across-the-system/)
- A single App Intent can drive the Home Screen widget, Lock Screen, Control Center, Action button, Siri and Shortcuts. — [Blake Crosley](https://blakecrosley.com/blog/ios-26-widget-and-control-surface); [tessl WidgetKit skill notes](https://tessl.io/registry/dpearson2699/swift-ios-skills/3.9.0/files/skills/widgetkit/SKILL.md) (secondary)
- Apple's own Watch flow logging takes about 4 taps inside the Cycle Tracking app. — [Apple Support](https://support.apple.com/en-mn/guide/watch/apd26429adf0)

### Inferences
- **Palette suggestion:** pick one warm, non-pink hue family, e.g. vermillion/terracotta (#D55E00) or plum, and encode flow as a **lightness ramp**: light = pale tint, medium = mid tone, heavy = full saturation. Reinforce it with **1 / 2 / 3 filled drops or dots**, so the level reads without colour (WCAG "don't rely on colour alone"). Use a neutral warm off-white background and one accent. Alternatively, give each day of the cycle history a different Okabe-Ito colour for playful variety.
- **The zero-friction surfaces, in priority order:**
  1. Medium-size Home Screen interactive widget with three buttons (light/medium/heavy) calling a `LogFlowIntent(level:)`.
  2. Lock Screen / Control Center control. Controls hold only one button each, so either offer three separate controls or one "log today" control that repeats the last level.
  3. Shortcuts/Siri ("Log medium flow").
  4. Watch app or complication with the same three buttons (WidgetKit complications on watchOS share the App Intent).
- **Confirmation:** use a haptic plus an in-widget state change ("Medium · logged ✓") instead of a modal. Allow undo or change by tapping again.
- Keep the in-app screen to three big buttons plus a quiet history strip, e.g. a row of coloured dots for the past cycles.

### Gaps
- No Dribbble, Mobbin or Medium case studies of non-pink period-app UIs were retrieved.
- I didn't verify whether watchOS control widgets support multi-button layouts.

## Privacy-by-design for a local-first app

### Takeaway
The proven pattern, shown by Euki's perfect Mozilla score and by drip, Menstrudel and Mensinator, is: no account, no server, no analytics SDKs, local storage, and open source for auditability. The cautionary case is Stardust, whose analytics SDK leaked reproductive data.

### Cited Findings
- Euki's 10/10 Mozilla score is attributed to local storage plus no account. Stardust scored 2/10 for sharing reproductive and health data with RudderStack (analytics). — [Digital Trends](https://www.digitaltrends.com/phones/stardust-flo-and-other-popular-period-trackers-flunk-mozillas-latest-privacy-test/); [The Star (Kenya), Jul 2026](https://www.the-star.co.ke/news/world/2026-07-19-how-period-trackers-share-your-private-details)
- drip has "no servers that store any of your data". It is open source so its privacy claims can be audited, and it offers password-protected local storage with import/export. — [dripapp.org](https://dripapp.org/); [ExpressVPN](https://www.expressvpn.com/blog/period-tracking-apps/)
- Menstrudel stores data "completely offline on your device", never sends it to a server or third party, and has no accounts and no tracking. — [GitHub Menstrudel](https://github.com/J-shw/Menstrudel)

### Inferences
- **Build checklist:**
  - no third-party SDKs (analytics, crash reporting, ads)
  - SwiftData/Core Data store with iOS Data Protection (`NSFileProtectionComplete`)
  - optional Face ID lock
  - CSV/JSON export, plus a clear "delete everything" option
  - HealthKit sync opt-in
  - an App Store privacy label of "Data Not Collected"
- Widgets need an **App Group** shared container to write logs. Keep that container protected too, and decide whether the lock-screen widget should show "logged" status, since it is visible without unlocking.
- iCloud/CloudKit sync, if offered, should be opt-in.

### Gaps
- I didn't retrieve legal analysis of post-Dobbs data-subpoena risk, or of how CloudKit/Health backups are treated.
- I didn't verify Apple's current statement on end-to-end encryption of Health data in iCloud.
