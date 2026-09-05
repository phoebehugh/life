# Family notes

Persistent facts to remember across sessions (e.g. scheduled school-check tasks).

## Children

- **Ralph Land** — Year 1 at Arnold House School (Pre-Prep, St John's Wood).
  - PE kit worn Mondays & Fridays.
  - Attends Canons Park site from Monday 7th September 2026 onwards.
  - Drop-off window: 8.20–8.45am. Pickup: 3.30pm.
  - After-school clubs: signed up to Wallace Chess on Wednesdays only (no other clubs).
  - Not using Early Morning Club or Sibling Extended Day Club — no standing form needed, only ad hoc 2pm notice to school if that ever changes.
  - Uniform (tie, PE polo, grey shirts) arrived.
  - Shoes ordered: black school shoes + white PE shoes (check delivery).
  - Behaviour Policy Parents Acknowledgement Form — done (completed by Daniel).
  - Intimate Care Policy 2026-2027 Consent Form — done.

## Tapestry

- Access was restored as of ~7 September 2026 (school had disabled it while relinking parent accounts). Should be usable again — no need to keep flagging it as offline in daily briefs.
- No automated login access to Tapestry itself (no connector, and its app content is only readable in a real JS-capable browser, which this automation doesn't have). Never attempt to log into Tapestry or fetch its pages directly — it doesn't work from here and isn't worth retrying.
- Tapestry sends a "Weekly Notification Summary" email from **noreply@tapestryjournal.com** (subject like "Recent Arnold House School Notifications") listing new observations/memos/etc. by title, author, and timestamp, each linking back to Tapestry. It only lists what was posted — no actual content/text, since that requires opening the link in a real browser.
- This currently goes to Daniel's account (dan.land@mac.com) — Daniel has been forwarding it to phoebehugh@gmail.com manually. Ideally set up an auto-forward rule from his account so this happens automatically; check whether that's been done.
- In the school-check automation: search Gmail for emails from noreply@tapestryjournal.com (or forwards of them, e.g. from daniel@donttelldad.co.uk) and include what they list (titles + links, e.g. "New observation: 'The Week Ahead' — [link]") in the Saturday weekly roundup. Be clear this is just a list of what was posted, not a summary of its actual content, since the brief can't read what's behind the links.

## Daily school brief preferences

- The Early Morning Club / Sibling Extended Day Club note should only appear in the **Monday** brief (as a standing FYI for the week), not repeated on Tuesday–Friday. Lead with what each club is, then note we're not using them, e.g.: "Arnold House offers an Early Morning Club (wraparound care from 8.10am, open to any family) and a Sibling Extended Day Club (care until 3.45pm for boys with siblings in the school on different schedules) — we're not using either, no action needed unless that changes."
- Include the drop-off window (8.20–8.45am) and pickup time (3.30pm) in every daily brief.
- Before compiling each day's brief, check for a reply on the previous brief email's thread. If one exists, read it and update the relevant facts in this file (e.g. "shoes arrived" → update the shoes line) before writing that day's brief, so replies feed into the notes rather than being missed. This means a reply is only picked up on the *next* run, not instantly — if the reply is ambiguous, use judgement but keep the change conservative and note the source in the commit.
- Whenever a brief mentions something needing action (a form, a booking, a consent form, a policy PDF, a club sign-up page), include the actual link pulled from the Arnold House email (the "Reply" link, the direct booking URL, or the attachment link) inline, so there's no need to open the original school email to act on it.

## Saturday weekly summary

- Saturday's brief (in addition to the usual daily content) should be a longer, weekly-roundup version: highlights from the week's Arnold House emails (events, announcements, things covered), plus anything still open heading into next week. Fine for it to run longer than the weekday briefs.
- Also include a "Tapestry this week" section listing anything found in a Tapestry Weekly Notification Summary email (see Tapestry section above) — titles + links, clearly labelled as a list of what was posted rather than a content summary.
- This can only draw on what arrived via email — see the Tapestry limitation above. Don't claim to have checked Tapestry itself or browsed its content.
