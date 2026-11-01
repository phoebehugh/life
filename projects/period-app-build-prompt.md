# Build prompt: period app v1

Copy everything below the line into Claude Code (or another coding agent) in a new, empty iOS project repo. Attach or paste `period-app-functional-brief.md` and `period-app-design-brief.md` alongside it.

---

You are building version 1 of a calm, private, one-tap period tracker for iPhone. Read the two attached briefs first: the **functional brief** is the source of truth for behaviour; the **design brief** covers look, feel, copy and accessibility. If they conflict, ask me before choosing.

**The product in one line:** open the app (or tap the widget), tap today's flow (Mist / Drizzle / Shower / Downpour, or "Nothing today"), done. From that log the app predicts the next period and fertile window as honest ranges, shows gentle "worth mentioning to your GP" notes when a pattern repeats, and keeps everything on the phone.

**Tech constraints**
- Swift + SwiftUI, iOS 18 minimum. SwiftData for storage. WidgetKit with App Intents for the interactive widget and a Lock Screen / Control Centre control.
- HealthKit: read menstrual flow history on import; write flow (with the menstrual-cycle-start metadata on period starts) and spotting. Check the current HealthKit API names for iOS 18 (some menstrual-flow types were renamed) rather than relying on memory.
- Optional iCloud backup via the user's private CloudKit database. No other network access, no analytics, no third-party SDKs, no account.
- No dependencies unless you ask me first.

**Architecture**
- `CycleEngine`: a pure Swift module with no UI or storage imports. It derives periods and cycles from daily records and produces predictions and GP notes exactly as sections 3, 5 and 6 of the functional brief specify. Every number it shows to the user is a range.
- Data layer (SwiftData models + HealthKit sync + export).
- UI layer (SwiftUI screens, widget, notifications).

**Build in this order, and stop for my review after each phase**
1. `CycleEngine` + unit tests. Fixtures: regular 28-day cycles, irregular 24-38, a missed-log cycle, first cycle only, a positive ovulation test, each GP note rule, spotting-only days. All tests pass.
2. Data model, onboarding (Apple Health import or last-period date, then goal), and the Home screen with one-tap logging, logged card and undo.
3. Calendar month and year views, tap-to-edit sheet, drag-to-fill.
4. Interactive widget, Lock Screen / Control Centre control, notifications (discreet wording by default, never more than one a day).
5. GP summary PDF, CSV export, delete-all-data, Face ID lock, iCloud backup, pregnancy pause.
6. Accessibility pass (VoiceOver labels, Dynamic Type, Reduce Motion, dark mode, 44pt targets) and the acceptance checklist in section 9 of the functional brief.

**Design guidance**
Follow the design brief's goals: calm like Headspace, colourful but pared back, rounded, lots of space, one thing per screen, pink is fine but grown-up, not candy or girly, no streaks or badges, no pop-ups. Put all colours, type and spacing in one theme file of design tokens so a designer can restyle the app later without touching screens. Use placeholder tokens from the "Dawn" direction (warm cream background, terracotta flow scale, sage fertile colour, soft serif for large numbers) until the final design arrives.

**Copy**
Warm, plain, brief. Use the examples in the design brief's Voice and copy table. Never alarming words ("LATE", "HIGH chance"), never imply contraception, never mention streaks or missed days.

**Working style**
- Small, reviewable commits with clear messages.
- When the briefs are silent, choose the simplest option that keeps the app calm and private, and note the decision in `DECISIONS.md`.
- At the end of each phase, give me a short summary, how to run it, and anything you'd like me to decide.
