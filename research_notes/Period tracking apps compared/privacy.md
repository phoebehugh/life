# Privacy and data security of period tracking apps (as of October 2026)

Note on method: several primary sites (mozillafoundation.org, ucl.ac.uk, therecord.media, courthousenews.com, mlex.com) were blocked by the research environment's network proxy, so some findings rest on search-result snippets and secondary write-ups rather than full-page reads. Where that matters, it is flagged below. Some search snippets also gave 2026 court dates that I could not open at source; treat them as "reported" until checked.

## 1. FTC Flo settlement (2021) and Frasco v. Flo Health (2025–26)

### Takeaway
The FTC found in 2021 that Flo shared users' health data with Facebook, Google and others despite promising not to, but fined it nothing. The private class action (Frasco v. Flo Health) went further. Flo ($8M), Google ($48M) and Flurry ($3.5M) settled for $59.5M in total. Meta refused to settle, and in August 2025 a jury found it liable under California's wiretapping law (CIPA). As of late September 2026, a proposed judgment of about $1.1B against Meta was still being contested. All of this concerns data shared between 2016 and 2019, not Flo's current practices.

### Cited Findings
- **FTC 2021:** The FTC finalised its order on 22 June 2021. It alleged that, despite promising privacy, Flo shared sensitive health data from millions of users with marketing and analytics firms including Facebook and Google — [FTC press release (archived PDF)](https://data.aclum.org/wp-content/uploads/2025/01/FTC_www_ftc_gov_news-events_news_press-releases_2021_06_ftc-finalizes-order-flo-health-fertility-tracking-app-shared-sensitive-health-data-facebook-google.pdf)
- The order requires Flo to get users' affirmative consent before sharing health data, commission an independent review of its privacy practices, tell affected users, and instruct the third parties to destroy the data. It also bars Flo from misrepresenting its data practices — [FTC press release (archived PDF)](https://data.aclum.org/wp-content/uploads/2025/01/FTC_www_ftc_gov_news-events_news_press-releases_2021_06_ftc-finalizes-order-flo-health-fertility-tracking-app-shared-sensitive-health-data-facebook-google.pdf)
- There was no monetary penalty, only injunctive relief — [offlist.me enforcement summary](https://www.offlist.me/enforcement/flo-health-2021). Two Democratic commissioners issued a joint statement arguing the FTC should also have charged a Health Breach Notification Rule violation — [FTC Chopra/Slaughter statement](https://www.ftc.gov/system/files/documents/public_statements/1586018/20210112_final_joint_rcrks_statement_on_flo.pdf)
- **Frasco v. Flo Health (N.D. Cal., 3:21-cv-00757):** The defendants were Flo, Meta, Google and Flurry. The claims covered data shared between 1 Nov 2016 and 28 Feb 2019 through in-app SDKs and were brought under CIPA, California's medical confidentiality law (CMIA) and related laws — [HIPAA Journal](https://www.hipaajournal.com/flo-health-google-flurry-59-5m-settlement-privacy-lawsuit/); [Labaton case page](https://www.labaton.com/Cases/Frasco-v-Flo-Health-Inc)
- **Settlements:** Flurry settled for $3.5M (March 2025), Google for $48M (just before trial), and Flo for $8M (31 July 2025, mid-trial). Flo also agreed to show a privacy-commitment notice on its website for a year. The total is $59.5M. Preliminary approval was reported in June 2026, with a final approval hearing reported for 29 Oct 2026 — [HIPAA Journal](https://www.hipaajournal.com/flo-health-google-flurry-59-5m-settlement-privacy-lawsuit/) (dates taken from a search snippet)
- **Meta verdict:** A unanimous jury found Meta liable under CIPA (verdict dated 1 Aug 2025 in some reports and 4 Aug in others) for intentionally eavesdropping on or recording users' communications with the Flo app without consent — [National Law Review](https://natlawreview.com/article/jury-finds-meta-liable-collecting-private-reproductive-health-data); [Digital Policy Alert](https://digitalpolicyalert.org/event/32655-jury-issued-final-verdict-regarding-metas-role-in-frasco-et-al-v-flo-health-et-al-finding-meta-guilty). It was described as the first major CIPA jury verdict and one of the first times Big Tech was held liable at trial for misusing health data — [Lawdragon](https://www.lawdragon.com/news-features/2025-08-25-big-tech-on-trial-jury-finds-meta-liable-for-misusing-women-health-data)
- Judge James Donato rejected Meta's post-trial motions, finding the evidence "amply supported the conclusion that Meta was directly acquiring the content of the user's communications with the Flo App in real time" — [Law360](https://www.law360.com/articles/2388518/meta-loses-bid-to-overturn-verdict-in-flo-privacy-class-action); [Business & Human Rights Centre](https://www.business-humanrights.org/en/latest-news/usa-judge-rejects-metas-bid-to-overturn-jury-verdict-on-breach-of-flo-period-tracking-app-users-privacy/)
- **Damages:** CIPA allows $5,000 per violation. Courthouse News reported that the judge signalled Meta "may owe $8 billion" — [Courthouse News (headline)](https://www.courthousenews.com/judge-signals-meta-may-owe-8-billion-in-menstrual-app-privacy-suit/)
- Plaintiffs reportedly asked (14 Sept 2026) for a partial final judgment of about $1.1B covering roughly 222,000 California residents. Meta opposed this on 28 Sept 2026, calling it a "Frankenstein's monster" that violates due process, and a hearing was reported for 29 Oct 2026 — [Law360](https://www.law360.com/articles/2531657/meta-fights-monster-proposed-1-1b-cipa-judgment); [MLex](https://www.mlex.com/mlex/articles/2531469/meta-opposes-final-us-approval-of-1-1-billion-flo-health-privacy-judgment). An appeal by Meta is widely expected — [Bloomberg Law](https://news.bloomberglaw.com/litigation/metas-health-privacy-trial-loss-spotlights-power-of-wiretapping)

### Inferences
- The wrongdoing dates from 2016–2019 and is a past incident. Flo's later moves, such as Anonymous Mode (2022) and its ISO 27001 certification, are a response to it. Still, the case shows that SDK-based leakage to ad platforms is the main real-world risk with commercial trackers.
- The case is a US class action, so UK users are not class members and get no compensation.

### Gaps
- I could not confirm whether the 29 Oct 2026 hearing has happened or what was decided (it is after today's date of 4 Oct 2026).
- I found no evidence of FTC enforcement against Flo after the 2021 order.

## 2. Post-Dobbs concerns: anonymous modes, encryption claims, local vs cloud storage

### Takeaway
After Roe was overturned in 2022, apps reacted in three main ways:
- **Flo** added an anonymous mode, routed through Cloudflare using Oblivious HTTP (OHTTP), so Flo cannot link health data to an identity.
- **Stardust** claimed end-to-end encryption it did not actually have. It has since dropped the claim and still shares data with third-party analytics.
- **Clue and Natural Cycles** pointed to their EU base and GDPR.

The strongest models are local-only apps with no account (Euki, drip) and Apple Health, which has true end-to-end encrypted iCloud sync.

### Cited Findings
- **Flo Anonymous Mode:** Users can track without their name, email or IP address being linked to their health data. Flo says "No one, not even Flo, can identify you" — [Flo](https://flo.health/anonymous-mode)
- It uses Cloudflare's OHTTP relay (the IETF RFC 9458 standard), which swaps the user's IP address for Cloudflare's so that Flo cannot see where data comes from, with post-quantum encryption in transit — [Cloudflare case study](https://www.cloudflare.com/case-studies/flo-health); [Flo blog](https://flo.health/blog/5-ways-flo-s-anonymous-mode-protects-your-reproductive-health-data)
- It won the 2022 IAPP Privacy Innovation Award — [IAPP](https://iapp.org/news/a/period-tracker-app-creates-anonymous-mode/). It has to be switched on; the standard Flo account is not anonymous by default — [MobiHealthNews](https://www.mobihealthnews.com/news/period-tracking-app-flo-adds-anonymous-mode-after-roe-decision)
- **Stardust:** On 24 June 2022 it posted a viral TikTok saying that if subpoenaed it "will not be able to hand over any of your period tracking data". TechCrunch found it actually used standard SSL and server-side encryption, not end-to-end encryption, and was sending phone numbers to a third-party analytics firm. Stardust then removed the E2E claim from its privacy policy — [Truth in Advertising](https://truthinadvertising.org/blog/period-tracker-capitalizes-on-post-roe-fears/); [Silicon Republic](https://www.siliconrepublic.com/?p=982223)
- Privacy International found Stardust sharing data, including first and last names, with third-party analytics providers. A search snippet also reported that its policy named Meta and Google ad-measurement tools as of May 2026, but I could not check that at source — [Truth in Advertising](https://truthinadvertising.org/blog/period-tracker-capitalizes-on-post-roe-fears/)
- Mozilla saw Stardust start third-party tracking immediately after launch, transmitting birth date, birth-control method, reproductive goals and symptoms through external services — [Captain Compliance summary of Mozilla](https://captaincompliance.com/?p=12974)
- **Natural Cycles** (Sweden) says it applies GDPR to all users and built an anonymous experience so that "no one — not even us at Natural Cycles — can identify the user" — [Tom's Guide](https://tomsguide.com/news/period-tracking-apps-respond-to-roe-v-wade-ruling); [Yahoo/news](https://news.yahoo.com/period-tracking-apps-scramble-anonymize-101223458.html)
- **Clue** (Berlin) cites GDPR, says it uses de-identified data for research, and said it would "not respond to any disclosure request or attempted subpoena of their users' health data by U.S. authorities" — [Tom's Guide](https://tomsguide.com/news/period-tracking-apps-respond-to-roe-v-wade-ruling)
- **Apple Health Cycle Tracking:** With two-factor authentication on, Health data synced to iCloud is end-to-end encrypted and Apple does not hold the key. Cycle predictions are calculated on the device — [Apple Health Privacy Overview (May 2023)](https://apple.com.cn/health/pdf/Health_Privacy_Overview_May_2023.pdf); [Apple Support](https://support.apple.com/120356)
- **drip** keeps all data on the phone and offers export only, with no cloud — [Cult of Mac / search summary](https://www.cultofmac.com/how-to/how-to-keep-iphone-menstrual-cycle-tracking-data-private)
- **Euki** stores data locally, needs no account and collects no personal information — [Captain Compliance summary of Mozilla](https://captaincompliance.com/?p=12974)
- Privacy experts flag data brokers as a separate route: police could buy data rather than serve a subpoena — [Yahoo/news](https://news.yahoo.com/period-tracking-apps-scramble-anonymize-101223458.html)

### Inferences
- How the apps store data:

  | App | Storage |
  |---|---|
  | Euki | Local only, no account |
  | drip | Local only, no account |
  | Apple Health | On device, with E2E-encrypted iCloud sync |
  | Flo, Clue, Natural Cycles, Ovia, Glow, Premom, Stardust, Period Calendar | Cloud accounts (based on their business models and the reporting above; not verified app by app for 2026) |

- An anonymous mode protects your identity on the company's servers. It does not protect data left on a seized phone. Under UK police guidance (section 4), device seizure is the more relevant risk.

### Gaps
- I found no independent technical audit of Flo Anonymous Mode, beyond Flo citing its ISO audit.
- I could not confirm how Clue currently stores data (cloud sync is assumed) or whether Natural Cycles' anonymous mode is still offered in 2026.
- I found no sourced current data on Ovia, Glow or Period Calendar storage.

## 3. Mozilla, Consumer Reports and academic rankings

### Takeaway
- **Mozilla (2022):** 18 of 25 reproductive-health apps and devices got a "Privacy Not Included" warning.
- **Mozilla's newer "Nothing Personal" test of six apps** (apparently updated for 2026) ranked them Euki 10/10, Clue 8, Flo 7, Period Calendar 6, Planned Parenthood's Spot On 5 and Stardust 2.
- **KCL/UCL study (CHI 2024, 20 apps):** found widespread contradictions between apps' privacy policies and their app-store labels, and poor protection against law-enforcement access.
- **Consumer Reports (2020):** tested apps including drip and Euki.

### Cited Findings
- **Mozilla 2022:** 18 of 25 reproductive-health apps and devices got the warning, and most had unclear rules on sharing data with law enforcement — [Mozilla Foundation](https://www.mozillafoundation.org/blog/in-post-roe-v-wade-era-mozilla-labels-18-of-25-popular-period-and-pregnancy-tracking-tech-with-privacy-not-included-warning/) (page blocked; confirmed via search snippet and [Business Insider NL](https://www.businessinsider.nl/mozilla-slaps-18-period-and-pregnancy-tracking-apps-and-devices-with-a-privacy-not-included-warning-label/))
- **Mozilla "Nothing Personal"** (tested by Shoshana Wodinsky, using hands-on testing plus network-traffic analysis):

  | Rank | App | Score | Mozilla's description |
  |---|---|---|---|
  | 1 | Euki | 10/10 | Open source, non-profit, only "Best Of" |
  | 2 | Clue | 8/10 | Germany-based, clinical focus |
  | 3 | Flo | 7/10 | "Data-hungry", with an AI symptom chatbot |
  | 4 | Period Calendar | 6/10 | The only ad-financed app tested |
  | 5 | Spot On | 5/10 | From Planned Parenthood |
  | 6 | Stardust | 2/10 | Astrology-themed |

  Mozilla also noted "privacy-washing" among the apps — [Mozilla (German page, titled 2026)](https://www.mozillafoundation.org/de/nothing-personal/period-ovulation-trackers/); [Captain Compliance](https://captaincompliance.com/?p=12974)
- Mozilla also has a Privacy Not Included entry for Natural Cycles — [Mozilla PNI: Natural Cycles](https://foundation.mozilla.org/de/privacynotincluded/natural-cycles-birth-control/) (details not retrievable)
- **KCL/UCL study** (Malki et al., CHI 2024, presented 14 May 2024): analysed the privacy policies and Google Play data-safety labels of 20 popular female-health apps in the UK and US — [UCL news](https://www.ucl.ac.uk/news/2024/may/female-health-apps-misuse-highly-sensitive-data); [KCL news](https://www.kcl.ac.uk/news/female-health-apps-misuse-highly-sensitive-data-study-finds). Its findings:
  - 35% of the apps claimed no third-party sharing in their data-safety section but described sharing in their privacy policy.
  - Only one app explicitly addressed the sensitivity of menstrual data with regard to law enforcement.
  - Several pregnancy apps required users to say whether they had had a miscarriage or abortion.
  - Some apps had no data-deletion function, or made deletion difficult.

  Source: [UCL](https://www.ucl.ac.uk/news/2024/may/female-health-apps-misuse-highly-sensitive-data); [TechXplore](https://techxplore.com/news/2024-05-female-health-apps-misuse-highly.html)
- **Consumer Reports 2020:** its Digital Lab evaluated drip, Euki, Lady Cycle, Periodical and others. A 2020 write-up says the apps tested stored data in the cloud and gave no guarantee against third-party sharing — [Consumer Reports](https://www.consumerreports.org/health/health-privacy/period-tracker-apps-privacy-a2278134145/) (paywalled); [TechXplore 2020](https://techxplore.com/news/2020-01-menstrual-tracker-app-health.amp). This conflicts with the local-storage descriptions of drip and Euki above. The CR evaluation was probably of older versions, or the snippet is mixing up apps, so treat it with caution.
- **Premom (FTC 2023):** Easy Healthcare paid $200,000 and was permanently banned from sharing health data with third parties for advertising. This followed SDK-based sharing and a breach of the Health Breach Notification Rule — [WilmerHale](https://www.wilmerhale.com/en/insights/blogs/wilmerhale-privacy-and-cybersecurity-law/20230525-ftc-brings-second-enforcement-action-against-healthcare-company-for-violating-the-health-breach-notification-rule); [Arnold & Porter](https://www.arnoldporter.com/en/perspectives/blogs/enforcement-edge/2023/06/ftc-settles-with-premom-app-developer)
- **Glow (California AG 2020):** a $250,000 penalty over privacy and security flaws in 2013–2016. The settlement included a first-ever requirement to consider how privacy lapses affect women in particular. Glow admitted no liability — [California OAG via HHS-OIG](https://oig.hhs.gov/fraud/enforcement/attorney-general-becerra-announces-landmark-settlement-against-glow-inc-fertility-app-risked-exposing-millions-of-womens-personal-and-medical-information); [WilmerHale](https://www.wilmerhale.com/en/insights/blogs/wilmerhale-privacy-and-cybersecurity-law/20200929-california-settles-with-glow-app-over-alleged-privacy-and-security-violations)

### Inferences
- Across the sources, the consistent ranking runs as follows:
  1. Euki and drip (local, no account)
  2. Apple Health (E2E encrypted)
  3. Clue and Natural Cycles (EU/GDPR, cloud)
  4. Flo (better since 2022, but with an enforcement history and heavy data collection)
  5. Period Calendar (ad-funded)
  6. Glow, Premom and Stardust, which have the poorest track records

### Gaps
- **The "UCL/Plymouth 2024 study" in the brief:** I found the 2024 study was KCL and UCL, not Plymouth. I found no Plymouth-led period-app study to verify.
- **Ovia:** I found no sourced 2023–2026 assessment. (Earlier reporting on its employer-sponsored data sharing exists but wasn't retrieved.)
- I could not retrieve full Mozilla per-app write-ups or the date of the Mozilla 2026 update.
- I could not find a current Consumer Reports rating.

## 4. UK/EU angle: GDPR, the ICO review, and UK legal risk

### Takeaway
UK GDPR treats menstrual and health data as special category data. The ICO reviewed period and fertility apps from September 2023 to February 2024 and found "no serious compliance issues or evidence of harm", but asked developers to be clearer about transparency, consent and lawful basis. UK legal risk changed materially in 2026:
- **From May 2025:** police guidance expressly allowed officers to examine women's phones and period apps after a pregnancy loss.
- **From 29 April 2026:** the Crime and Policing Act 2026 took women ending their own pregnancies out of the criminal law in England and Wales, with immediate effect.

So the main reason UK users had to fear prosecution using app data has largely gone. The risk was always much lower than in US ban states.

### Cited Findings
- In September 2023 the ICO launched its review of period and fertility apps. Its poll found:
  - A third of women have used such apps.
  - Women ranked transparency (59%) and security (57%) above cost (55%) when choosing an app.
  - Over half of users believed they saw more baby or fertility adverts after signing up, and 17% found these adverts distressing.

  Source: [ICO](https://ico.org.uk/about-the-ico/media-centre/news-and-blogs/2023/09/ico-to-review-period-and-fertility-tracking-apps)
- The ICO contacted the providers of the most popular apps among UK users and named its concerns: confusing privacy policies, excessive data collection, and upsetting targeted ads — [ICO](https://ico.org.uk/about-the-ico/media-centre/news-and-blogs/2023/09/ico-to-review-period-and-fertility-tracking-apps)
- It reported back in February 2024: no serious compliance issues or evidence of harm, but room for improvement, plus four tips for developers (be transparent, get valid consent, use the correct lawful basis, be accountable) — [LexisNexis](https://www.lexisnexis.co.uk/legal/news/ico-advises-app-developers-on-protecting-users-privacy-following-review); [LBC](https://lbc.co.uk/tech/5691202d57854b2a9f6ad8593753fb04)
- In May 2025, National Police Chiefs' Council guidance told officers investigating pregnancy loss they could examine devices, including period-app data, to establish "a woman's knowledge and intention in relation to the pregnancy". MSI called this "regressive policing" — [Humanists UK](https://humanists.uk/2025/06/04/police-access-to-period-apps-highlights-need-to-decriminalise-abortion/); [ABC News](https://www.abc.net.au/news/2025-05-30/npcc-guidelines-on-stillbirths-abortions-draws-controversy/105332518)
- The Crime and Policing Act 2026 got Royal Assent on 29 April 2026, with the change effective immediately. It stops women being investigated or prosecuted for ending their own pregnancies in England and Wales. MPs passed the amendment 379–137 in June 2025 and the Lords upheld it in March 2026. It does not change time limits, and others, such as providers acting outside the law, can still be prosecuted — [Humanists UK](https://humanists.uk/2026/04/29/success-decriminalisation-of-abortion-and-historic-pardons-for-women-become-law/); [RCOG](https://www.rcog.org.uk/news/women-s-health-organisations-celebrate-as-new-law-removes-women-from-the-criminal-law-related-to-abortion/); [Wikipedia](https://en.wikipedia.org/wiki/Crime_and_Policing_Act_2026)
- Clue (Germany) and Natural Cycles (Sweden) apply GDPR to all users — [Tom's Guide](https://tomsguide.com/news/period-tracking-apps-respond-to-roe-v-wade-ruling)

### Inferences
- For a UK user in England in 2026:
  - **Legal risk from her own cycle data** is now low.
  - **Commercial risk** remains the main concern: ad targeting, SDK leakage, data brokers and breaches.
  - **Scotland and Northern Ireland:** the 2026 Act covers England and Wales only, and their position was not researched here.
- UK GDPR gives enforceable rights (access, erasure, objecting to processing) against any app serving UK users, US-based ones included. In practice, enforcement against US firms such as Flo (London/US) or Ovia is weaker than against EU-established firms like Clue.
- The ICO's review produced guidance, not fines. Regulators are watching but have not taken enforcement action against period apps in the UK.

### Gaps
- The ICO published no app-by-app findings, and the apps it contacted were not named.
- I did not research whether any UK police force has actually used period-app data in a prosecution.

## 5. Practical privacy tips

### Takeaway
To minimise risk:
- Prefer local-only or end-to-end encrypted options: drip, Euki or Apple Health. Clue is the strongest EU cloud option.
- If you use Flo, switch on Anonymous Mode.
- Avoid ad-funded or poorly rated apps (Stardust, Period Calendar).
- Limit what you log (abortion or miscarriage history, sex).
- Use your UK GDPR rights to delete data.

### Cited Findings
- Local storage and no account are what earned Euki Mozilla's only perfect score — [Captain Compliance/Mozilla](https://captaincompliance.com/?p=12974)
- To get end-to-end encryption on Apple Health, enable two-factor authentication on your Apple ID. Health data is encrypted on the device when the phone is locked — [Apple Health Privacy Overview](https://apple.com.cn/health/pdf/Health_Privacy_Overview_May_2023.pdf)
- Flo Anonymous Mode must be switched on to separate identity from health data — [Flo](https://flo.health/anonymous-mode)
- The KCL/UCL study warns that some apps ask about miscarriage or abortion history and make deletion hard, so check that deletion exists before entering sensitive data — [UCL](https://www.ucl.ac.uk/news/2024/may/female-health-apps-misuse-highly-sensitive-data)
- App-store privacy labels can contradict the privacy policy (35% of apps in the KCL/UCL study), so don't rely on the label alone — [UCL](https://www.ucl.ac.uk/news/2024/may/female-health-apps-misuse-highly-sensitive-data)
- The ICO has encouraged users to raise concerns with it — [ICO](https://ico.org.uk/about-the-ico/media-centre/news-and-blogs/2023/09/ico-to-review-period-and-fertility-tracking-apps)

### Inferences
- Further steps (general good practice, not drawn from a single source):
  - Turn off ad personalisation and ad-tracking IDs (iOS "Ask App Not to Track"; Android "Delete advertising ID").
  - Don't sign in with Facebook or Google.
  - Turn off optional research and data-sharing toggles.
  - Lock the app with a PIN or biometrics where offered.
  - When leaving an app, delete the account in-app rather than just uninstalling.
- Device seizure is the residual UK risk scenario, and only for people outside the 2026 decriminalisation (e.g. Scotland/NI, not researched). Local-only storage protects you from company-side disclosure but not from a seized, unlocked phone. A strong passcode matters more than which app you use.

### Gaps
- I found no source testing whether in-app deletion in Flo, Clue or others actually purges backups.
- Settings menus change between versions; I did not verify current menu names.
