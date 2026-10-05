# Ovulation and Period Prediction: Methods, Algorithms and Accuracy

Method note: the proxy blocked PMC, frontiersin.org, jmir.org, arxiv.org and mdpi.com, so I could not open the full texts. Many figures below come from search-result snippets of abstracts, press releases or the publisher/company pages listed. I flag each place where I relied only on a snippet or on a company source.

## 1. Calendar/rhythm, Standard Days Method, and simple averaging (basic apps): accuracy limits

### Takeaway
Calendar methods start from population averages or the user's average cycle length. They are limited by biology: ovulation timing varies a lot from cycle to cycle, and most of that variation is in the follicular phase. The best fixed "ovulation day" guess on a 28-day cycle is right only about 1 time in 5. Most basic apps also draw the fertile window wrongly.

### Cited Findings
- **Real-world cycle physiology (Bull et al. 2019, npj Digital Medicine).** 612,613 ovulatory cycles from 124,648 Natural Cycles users. Mean cycle length was 29.3 days. Mean follicular phase was 16.9 days (95% CI 10–30) and mean luteal phase 12.4 days (95% CI 7–17). Follicular length fell by 0.19 days per year of age from 25 to 45. Per-woman cycle-length variation was 0.4 days (14%) higher at BMI >35 than at BMI 18.5–25. — [UCL Discovery PDF](https://discovery-pp.ucl.ac.uk/10084180/1/Real-world%20menstrual%20cycle%20characteristics%20of%20more%20than%20600%2C000%20menstrual%20cycles.pdf); [PMC6710244](https://pmc.ncbi.nlm.nih.gov/articles/PMC6710244) (snippet only; PMC blocked)
- **Fehring et al. 2006 (JOGNN).** 141 women, 1,060 cycles tracked with an electronic fertility monitor. Mean cycle was 28.9 days (SD 3.4) and 95% of cycles fell between 22 and 36 days. 42.5% of women had cycle-to-cycle variation of more than 7 days. The follicular phase contributes most of the variability. — [PubMed 16700687](https://pubmed.ncbi.nlm.nih.gov/16700687/); [Marquette ePublications](https://epublications.marquette.edu/nursing_fac/11)
- **Wilcox, Dunson & Baird 2000 (BMJ).** 221 women, 696 cycles, with ovulation estimated from urinary oestrogen and progesterone metabolites. Only about 30% of women had a fertile window that fell entirely within days 10–17, the window clinical guidelines use. On every day from day 6 to day 21, women had at least a 10% chance of being in their fertile window. The timing is "highly unpredictable, even if their cycles are usually regular." — [PubMed 11082086](https://pubmed.ncbi.nlm.nih.gov/11082086/); [BMJ](https://www.bmj.com/lookup/volpage/321/1259)
- **Johnson et al. 2018 (Curr Med Res Opin), "Can apps and calendar methods predict ovulation with accuracy?"** Given a simulated 28-day cycle, most popular apps named day 15 as ovulation day. That day has a 19% probability of being the true ovulation day. The best achievable single-day guess is day 16, at 21%. The best app prediction was correct for only 1 in 5 women. — [RRM Academy summary](https://www.rrmacademy.org/library/can-apps-and-calendar-methods-predict-ovulation-with-accuracy-rechiwfyisygrytkn) (snippet)
- **Setton et al. 2016 (Obstet Gynecol).** Reviewed 20 websites and 33 apps. Only 1 website (Babymed.com) and 3 apps (Clue, My Days, Period Tracker) predicted the exact fertile window. 26/33 apps and 15/20 websites included post-ovulation days in the window. Predicted windows started as early as day 4 and ended as late as day 21. — [Medical Xpress](https://m.medicalxpress.com/news/2016-06-websites-apps-accurate-fertile-window.html); [PET/Progress](https://www.progress.org.uk/study-finds-most-fertility-tracker-apps-are-inaccurate/)
- **Standard Days Method (Arevalo et al. 2002, Contraception 65:333–338).** Users avoid unprotected sex on days 8–19. Eligibility was self-reported cycles of 26–32 days. 478 women in Bolivia, Peru and the Philippines took part. Cumulative pregnancy probability over 13 cycles was 4.75% with correct use and 11.96% with typical use. — [IRH](https://www.irh.org/resource-library/efficacy-of-a-new-method-of-family-planning-the-standard-days-method/); [IRH PDF](https://www.irh.org/wp-content/uploads/2013/04/Efficacy_SDM_2002.pdf)
- **Simple prediction models do poorly at predicting the next bleed.** One analysis (a practitioner Substack, not peer-reviewed) found next-bleed error of about 6 days across five common models. — [Malone, Substack](https://maloneperform.substack.com/p/why-menstrual-cycle-predictions-are-less-accurate-than-you-think) (low-quality source; treat as indicative only)

### Inferences
- If ovulation is placed at "predicted next period minus 14 days", the error compounds. The luteal phase alone ranges from about 7 to 17 days (Bull 95% CI). That error is added to the error in predicting cycle length. So a calendar app cannot place ovulation reliably to within ±1 day, even for very regular users.
- The Standard Days Method works well enough for contraception only because its window is wide (12 days) and it restricts eligibility to 26–32-day cycles. It does not pinpoint ovulation.

### Gaps
- I could not open Bull 2019 to check two widely quoted figures: the share of cycles that are exactly 28 days, and the share of women ovulating on day 14. I have left them out.
- I found no peer-reviewed head-to-head MAE (mean absolute error) figures for period-start prediction by Clue, Flo or other calendar apps.

## 2. Basal body temperature (BBT), symptothermal method, and cervical mucus (Billings, Creighton)

### Takeaway
BBT can only confirm ovulation after it has happened: the temperature rise comes after ovulation, driven by progesterone. On its own it is a weak detector of the exact day. Cervical mucus is somewhat better. Combined in a strict rule set (the symptothermal method, e.g. Sensiplan), they give the best-documented effectiveness among fertility awareness methods: a 0.4–0.6% annual unintended pregnancy rate (Frank-Herrmann 2007).

### Cited Findings
- **Frank-Herrmann et al. 2007 (Hum Reprod 22(5):1310–1319).** 900 women recorded daily temperature, cervical secretions and intercourse. 322 abstained during the fertile phase and 509 used barriers. The overall annual unplanned pregnancy rate was about 0.6 per 100 women. With always-correct use it was 0.4 per 100 women. The authors say this is comparable to the pill. — [RRM Academy](https://rrmacademy.org/library/the-effectiveness-of-a-fertility-awareness-based-method-to-avoid-pregnancy-in-re-recfwatewz6ucgakm/); [NBC News](https://www.nbcnews.com/id/wbna17282285); [Diocese of Lansing PDF of paper](https://dioceseoflansing.org/sites/default/files/2021-04/Frank-Herman%20STM%20Study.pdf)
- **BBT vs ultrasound (Su et al. 2017 review, Bioeng Transl Med 2(3):238–246).** In infertile women, BBT detected ovulation with sensitivity 0.77, specificity 0.33 and accuracy 0.74. Timing of the BBT nadir varied widely, and BBT agreed with ultrasound in about 74% of cases. The review concludes that neither BBT nor cervical mucus is reliable for *predicting* ovulation. — [PMC5689497](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5689497/) (snippet)
- **Cervical mucus vs BBT (Indonesian J Obstet Gynecol 2018).** Accuracy for detecting ovulation was 65% for mucus and for mucus+BBT combined, and 59% for BBT alone. Mucus had sensitivity 70% and specificity 57.8%. The combination had sensitivity 46.67% and specificity 94.73%. This was a small study from a single centre. — [DOAJ](https://doaj.org/article/640d71311bd14132a353841bb8242ae5); [UI Scholar](https://scholar.ui.ac.id/en/publications/basal-temperature-cervical-mucous-and-both-combination-as-diagnos/) (snippet)
- **Wrist skin temperature vs oral BBT.** Wrist skin temperature was more sensitive than BBT for detecting ovulation (sensitivity 0.62 vs 0.23). — [JMIR 2021;23(6):e20710](https://www.jmir.org/2021/6/e20710/) (snippet; JMIR blocked)

### Inferences
- Temperature-based methods tell the user, typically 1–3 days after the fact, that ovulation has happened. Any *prospective* fertile-window estimate from BBT still comes from past cycles, i.e. it is a calendar estimate.
- The very high symptothermal effectiveness comes from conservative double-check rules: the fertile phase closes only after both the temperature shift and the mucus peak. It does not come from precise prediction.

### Gaps
- I did not retrieve primary effectiveness or validation figures for the Billings Ovulation Method (e.g. the WHO 1981 five-country trial) or for the Creighton Model (Hilgers' mucus "Peak day" vs ultrasound/LH correlation). These need a follow-up search; I have not quoted numbers from memory.

## 3. LH urine tests, E3G/PdG tests (Mira, Inito, Proov), and ultrasound as gold standard

### Takeaway
Serial transvaginal ultrasound, showing follicle rupture, is the reference standard. The urinary LH surge is the best widely available *prospective* marker. Ovulation typically follows LH surge onset by about 34 hours (range 22–56). Quantitative E3G/PdG monitors add early warning (rising oestrogen) and post-ovulation confirmation (PdG). Their published validation is mostly analytical or manufacturer-sponsored.

### Cited Findings
- **LH surge and ovulation meta-analysis** (2022, "The LH surge and ovulation re-visited", re: true natural cycle frozen embryo transfer). Mean interval from LH surge onset to ovulation was 33.91 h (95% CI 30.79–37.03), from 6 studies and 187 cycles, with a range of 22–56 h. In one included study, the first positive urine LH test came 20 ± 3 h before ovulation (95% CI 14–26). In 90% of cases ovulation occurred 16–48 h after the initial LH rise. — [Atilim University copy of PubMed record](https://www.atilim.edu.tr/uploads/pages/iletisim-1632722835/1665402218-The%20LH%20surge%20and%20ovulation%20re-visited_%20a%20systematic%20review%20and%20meta-analysis%20and%20implications%20for%20true%20natural%20cycle%20frozen%20thawed%20embryo%20transfer%20-%20PubMed.pdf); [Procrearte PDF](https://procrearte.com/revista/2022-11-09-032841-lh-surge-re-visited-in-true-natural-cicle.pdf) (snippet)
- **Direito et al. 2013.** 107 women, 283 cycles. The LH surge was defined at 30% of LH peak amplitude around the ultrasound-determined ovulation day. Surge shape and timing were highly heterogeneous. — [Clearblue HCP PDF](https://us-es.clearblue.com/sites/default/files/HCP_Publications/PUB-0108_v1.pdf) (snippet)
- **Inito Fertility Monitor (measures E3G, PdG and LH).** Coefficients of variation were 5.05% (PdG), 4.95% (E3G) and 5.57% (LH), with high correlation to ELISA. A new PdG-based criterion separated ovulatory from anovulatory cycles with 100% specificity and AUC 0.98. A new hormone trend was seen in 94.5% of ovulatory cycles. — [PMC10247788](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10247788/); [medRxiv preprint](https://medrxiv.org/content/10.1101/2021.05.11.21257023v2.full) (snippet; manufacturer-affiliated authors per trial registry [ISRCTN15534557](https://www.isrctn.com/ISRCTN15534557))
- **Proov (PdG test strips).** The company says it confirmed ovulation in 95% of women against serum progesterone, with no false positives, and that it confirmed "sufficient ovulation" (3 positives in a row) in 82% in another study. — [Proov blog](https://proovtest.com/blogs/blog/proov-validated) (company source)
- **Mira.** Its ovulation estimates correlated highly with the Clearblue Fertility Monitor, and both "provided an accurate estimate of the fertile window". The comparison was not against ultrasound. — [Marquette, Quantitative vs Qualitative Estrogen and LH Testing](https://epublications.marquette.edu/nursing_fac/979) (snippet)
- **BBT vs ultrasound for context.** BBT and ultrasound agreed in about 74% of cases. — [PMC5689497](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5689497/)

### Inferences
- A positive LH test gives about 1–2 days' notice of ovulation. Fertility is highest in the 2 days before ovulation, so LH tests are well timed for conception but give too little notice for contraception.
- E3G/PdG monitors improve on LH alone mainly by (a) a wider "high fertility" warning from the oestrogen rise and (b) confirming ovulation actually happened. There is no published evidence that they beat ultrasound-referenced LH timing at pinpointing the day.

### Gaps
- I found no independently verified sensitivity figures for consumer LH strips against ultrasound. Clearblue's "99% accurate" figure is a lab claim about detecting LH, not about timing ovulation.
- I found no ultrasound-referenced peer-reviewed validation of Mira's or Proov's day-of-ovulation accuracy.

## 4. Wearables: Apple Watch, Oura, Ava, Tempdrop

### Takeaway
Wrist, finger and armpit temperature wearables retrospectively estimate ovulation in about 80–96% of cycles, with a mean absolute error of about 1.2–1.6 days, measured against LH tests. They are confirmation tools, not prospective predictors. All the major validations are sponsored by the device maker.

### Cited Findings
- **Apple Watch / iPhone (Human Reproduction, March 2025, DOI 10.1093/humrep/deaf005; Apple-sponsored prospective cohort, NCT05852951).**
  - Algorithm 1 (during an ongoing cycle) estimated ovulation in 80.5% of cycles. MAE was 1.59 days (95% CI 1.45–1.74) and 80.0% of estimates were within ±2 days. For typical cycle lengths it estimated ovulation in 81.9% of cycles (MAE 1.53); for atypical lengths, 77.7% (MAE 1.71).
  - Algorithm 2 (after the cycle has ended) estimated ovulation in 80.8% of cycles, with MAE 1.22 days (95% CI 1.11–1.33) and 89.0% within ±2 days.
  - Algorithm 3 predicted next menses start once ovulation had been estimated: 89.4% within ±3 days, MAE 1.65 days (95% CI 1.52–1.79), in cycles with a wrist temperature signal of at least 0.2°C.
  - [Nature Index listing](https://www.nature.com/nature-index/article/10.1093/humrep%2Fdeaf005); [ClinicalTrials.gov NCT05852951](https://clinicaltrials.gov/study/NCT05852951); [PMC10747116 related review](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10747116/) (snippets)
- **Oura (JMIR 2025;e60667; in-house Oura scientists).** Detected 96.4% of ovulations with an average error of ±1.26 days. It was reported as significantly more accurate than the calendar method. — [Oura blog](https://ouraring.com/blog/oura-ovulation-detection-algorithm-validation-study/); [Wareable](https://www.wareable.com/health-and-wellbeing/oura-ring-fertile-window-outperforms-calendar-ovulation-predictions); [JMIR](https://www.jmir.org/2025/1/e60667/XML) (snippets; JMIR blocked; company-authored)
- **Ava bracelet (Goodale et al. 2019, JMIR; company-sponsored).** More than 200 women and over 1,000 cycles. Using wrist skin temperature, resting pulse, breathing rate and heart-rate variability, it identified the 5 most fertile days with 89% accuracy. — [JMIR blog](https://blog.jmir.org/2019/05/20/va-unveils-unprecedented-insights-into-physical-changes-during-menstrual-cycle-that-can-be-used-to-accurately-identify-fertile-window/); [MobiHealthNews](https://www.mobihealthnews.com/news/emea/wearable-technology-can-detect-biomarkers-linked-fertility-windows)
- **Ava, earlier work (Shilaih et al. 2018, Biosci Rep).** Wrist wearables captured the temperature changes associated with the menstrual cycle. — [PMC6265623](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6265623/) (title/snippet only)
- **Tempdrop (Sensors 2025;25(20):6327), "Accuracy of an Overnight Axillary-Temperature Sensor for Ovulation Detection: Validation in 194 Cycles".** 125 women, 194 cycles, April 2023–June 2024, with the Clearblue Connected Ovulation Test System as reference. The authors conclude it "can accurately determine the timing of ovulation." — [PMC12567647](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12567647/); [RRM Academy](https://rrmacademy.org/library/accuracy-of-an-overnight-axillary-temperature-sensor-for-ovulation-detection-val-recxoioeowqv6rtnw/) (snippet; I could not get the numbers because MDPI and PMC were blocked)

### Inferences
- The reference standard in these studies is usually a urine LH test, not ultrasound. So "error" means distance from the LH-predicted day, which itself sits about 1 day (range 0.5–2) before actual ovulation.
- The roughly 20% of cycles with no estimate in the Apple data matters. A wearable will regularly fail to give a reading, for reasons such as a weak signal, fever or alcohol.
- Once ovulation is known, period prediction improves to an MAE of about 1.65 days. This is because the luteal phase is more stable than the follicular phase.

### Gaps
- I could not obtain Tempdrop's MAE or detection-rate figures.
- I found no independent (non-sponsored) validation for any of the four wearables.

## 5. App algorithms: Natural Cycles, Flo, and academic work (Setton, Johnson, Freis, Li/Clue)

### Takeaway
Natural Cycles is the only app with a regulatory clearance as contraception (FDA De Novo, Aug 2018). Its algorithm combines temperature, optional LH tests and period dates in a statistical model. Its published effectiveness is Pearl Index 1.0 with perfect use and 6.8 with typical use. Flo's machine-learning claims are company marketing, with no independent validation. Academic work (Li/Urteaga/Elhadad with Clue data) shows that hierarchical Bayesian models that account for users skipping logging beat simple averages and neural networks at predicting cycle length.

### Cited Findings
- **Natural Cycles algorithm accuracy (Scherwitzl et al. 2015/2016).** Users enter BBT, plus the LH surge if available. Only 0.05% of "green" (non-fertile) days fell within the estimated fertile window. There were no pregnancies from intercourse on green days in that dataset. — [PMC4898152](https://pmc.ncbi.nlm.nih.gov/articles/PMC4898152) (snippet)
- **Natural Cycles effectiveness (Berglund Scherwitzl et al. 2017, Contraception).** 22,785 users, 18,548 woman-years. Typical-use Pearl Index was 6.8 ± 0.4 and perfect-use Pearl Index 1.0 ± 0.5. — [PubMed 28882680](https://pubmed.ncbi.nlm.nih.gov/28882680/)
- **FDA status.** De Novo Class II classification in August 2018 (DEN170052), the first app cleared as birth control in the US. Press materials cite 93% typical-use effectiveness based on 22,785 women and 224,563 cycles. — [MobiHealthNews](https://www.mobihealthnews.com/news/fda-grants-natural-cycles-contraception-app-de-novo-marketing-approval); [BioSpace](https://www.biospace.com/us-food-and-drug-administration-fda-clears-natural-cycles-as-the-first-digital-method-of-birth-control-in-the-united-states)
- **Natural Cycles vs calendar.** NICE has reviewed the evidence (MIB244). — [NICE MIB244](https://www.nice.org.uk/advice/mib244/chapter/Clinical-and-technical-evidence)
- **Flo's ML claims.** The founder says machine learning cut irregular-cycle prediction error from 5.6 to 2.6 days, a "54.2%" improvement, using a neural network over "400+ inputs". Flo also says 90% of users report accurate period predictions (self-report). — [Flo accuracy page](https://flo.health/flo-accuracy); [InData Labs case study](https://www.casestudies.com/company/indata-labs/case-study/flo-improves-cycle-prediction-accuracy-by-542-with-indata-labs); [AWS Startups blog](https://aws.amazon.com/blogs/startups/using-machine-learning-to-track-periods-with-flo) (company/vendor claims, not peer-reviewed)
- **Freis et al. 2018 (Front Public Health 6:98).** Evaluated 12 apps: 6 calendar-based (Clue, Flo, Maya, Menstruationskalender Pro, Period Tracker Deluxe, WomanLog), 2 "calculothermal" (Ovy, Natural Cycles) and 4 symptothermal (myNFP, Lady Cycle, Lily, OvuView). The rationale is that the peak-fertility interval is short and ovulation day varies even in regular cycles, so conception apps need to be precise. The study used cycle data from the Sensiplan (symptothermal) database. — [Frontiers](https://www.frontiersin.org/articles/10.3389/fpubh.2018.00098/text); [LMU ePub PDF](https://epub.ub.uni-muenchen.de/63721/1/fpubh-06-00098.pdf) (snippet only; per-app sensitivity numbers not retrieved)
- **Setton 2016 and Johnson 2018:** see Section 1.
- **Li, Urteaga, Shea, Vitzthum, Elhadad et al. (Clue data).** 186,000 menstruators and more than 2 million cycles. Their hierarchical generative model for next cycle length (a) explicitly models skipped tracking, (b) updates its prediction as the current cycle goes on, and (c) pools individual history with population information. It achieved state-of-the-art accuracy against neural-network and summary-statistic baselines. Its advantage grew as the likelihood of skipped logging increased. — [arXiv 2102.12439](https://arxiv.org/abs/2102.12439v1); [PMLR v149 Urteaga 2021](https://proceedings.mlr.press/v149/urteaga21a.html); [PMC8714275](https://pmc.ncbi.nlm.nih.gov/articles/PMC8714275) (snippets; full text blocked). There is also an R package implementing skip-aware modelling, [skipTrack](https://mynixos.com/nixpkgs/package/rPackages.skipTrack).
- **Li et al. 2020 (npj Digital Medicine), "Characterizing physiological and symptomatic variation in menstrual cycles using self-tracked mobile-health data".** This is the companion descriptive paper on the Clue data. — [DOAJ](https://doaj.org/article/6dbf3df4478a4eda941ff103364754ab)
- **State-space models (athlete cohort, Sci Rep 2021).** A hybrid state-space model reached an RMSE of 1.64 days for cycle length with substantial history per user. Prediction error rose with cycle length. — [PMC8379295](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8379295/) (snippet)

### Inferences
- The algorithmic gains come mainly from three things: (1) adding a physiological signal (temperature or LH) that locates ovulation in the *current* cycle; (2) Bayesian shrinkage toward population priors when a user has little history; and (3) handling missing or skipped logs. Fancier ML on period dates alone has a low ceiling, because the follicular phase varies inherently.
- Flo's "2.6-day error" cannot be compared with the Apple MAE of 1.65 days: the definitions, populations and validation are unknown.

### Gaps
- I could not retrieve Freis 2018's per-app accuracy results or the Li et al. model's exact MAE numbers, because the full texts were blocked.
- Natural Cycles' detailed algorithm (e.g. the specific Bayesian priors and the temperature-shift detection rules) is not public beyond high-level descriptions.

## 6. How quickly predictions improve with more cycles; what a minimal period-date-only app could achieve

### Takeaway
I found no clean peer-reviewed learning curve of "error vs number of logged cycles." The evidence does set a floor, though. Within-woman cycle variability (Fehring: 42.5% of women vary by more than 7 days) limits any period-date-only predictor. A realistic minimal app predicts the next period to within about ±2–3 days for regular users. It places ovulation only roughly, at predicted period minus about 12–14 days, within a window of several days.

### Cited Findings
- Population luteal phase is 12.4 days (95% CI 7–17) and follicular phase 16.9 days (95% CI 10–30). — [Bull 2019](https://discovery-pp.ucl.ac.uk/10084180/1/Real-world%20menstrual%20cycle%20characteristics%20of%20more%20than%20600%2C000%20menstrual%20cycles.pdf)
- 42.5% of regularly cycling women had cycle-length variation of more than 7 days across 3–13 cycles. — [Fehring 2006](https://pubmed.ncbi.nlm.nih.gov/16700687/)
- A hierarchical model that pools population data with individual history beats summary-statistic baselines (e.g. averages) on Clue data, especially when users skip logging. — [Li/Urteaga et al.](https://arxiv.org/abs/2102.12439v1)
- Simple models' next-bleed error was about 6 days in one non-peer-reviewed analysis. A rich-history state-space model reached an RMSE of about 1.6 days. — [Substack](https://maloneperform.substack.com/p/why-menstrual-cycle-predictions-are-less-accurate-than-you-think); [Sci Rep 2021](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8379295/)
- Even with perfect knowledge of a 28-day cycle, the best single-day ovulation guess is right only 21% of the time. — [Johnson 2018](https://www.rrmacademy.org/library/can-apps-and-calendar-methods-predict-ovulation-with-accuracy-rechiwfyisygrytkn)
- Adding a temperature signal (once ovulation is detected) gives next-period prediction of MAE 1.65 days, with 89.4% within ±3 days. — [Apple, Hum Reprod 2025](https://www.nature.com/nature-index/article/10.1093/humrep%2Fdeaf005)

### Inferences
These are my own design reasoning from the findings above, not sourced results.
- **Suggested minimal algorithm:**
  1. Predict next cycle length as a weighted or robust mean of the last ~6 cycles, e.g. median or exponentially weighted.
  2. Shrink that toward a population prior (about 28–29 days) when fewer than ~3 cycles are logged.
  3. Flag cycles more than 2× the user's median as probably skipped logs, not real long cycles.
  4. Show the prediction as a range (±1 SD of the user's cycle lengths) rather than a single day.
- **Suggested ovulation and fertile-window estimate:** place ovulation at predicted next start minus 12–14 days, the luteal estimate. Show a 6-day fertile window ending on the estimated ovulation day. Widen it by the user's cycle variability, and do not include post-ovulation days (the error Setton found in 26/33 apps).
- **How fast it improves:** most of the gain should come in the first 3–6 cycles, as the mean and SD estimates stabilise. After that, accuracy is capped by the user's own cycle variability, not by the amount of data. This is a statistical expectation; no source quantifies the curve.
- A period-date-only app should not claim to "predict ovulation". Honest wording is "estimated fertile window". Day-level accuracy needs LH, temperature or hormone data.

### Gaps
- I found no peer-reviewed study that directly measures prediction error as a function of the number of logged cycles for period-date-only apps. A follow-up could target Clue/Columbia papers or Bull et al. follow-ups.
- I found no published MAE for "mean of last 6 cycles" vs other baselines. The Li et al. baselines likely include this, but I could not access the full text.
