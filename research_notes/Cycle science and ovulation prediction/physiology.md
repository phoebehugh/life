# Menstrual cycle physiology and real-world cycle data

> **Method note / proxy limitations:** The egress proxy blocked direct fetches of every primary source tried (nature.com, pubmed.ncbi.nlm.nih.gov, www.ncbi.nlm.nih.gov, pmc.ncbi.nlm.nih.gov, europepmc.org, arxiv.org, obgproject.com, epublications.marquette.edu). **All findings below come from search-engine snippets/summaries of the cited pages, not from reading full texts.** Numbers that appear in multiple snippets or are well-known canonical values are flagged as reliable; anything recalled from background knowledge but not confirmed in a snippet is explicitly marked "(unverified — from background knowledge)" and should be checked before use in-app.

## 1. Hormonal sequence; follicular vs luteal phase; is the luteal phase really fixed at 14 days?

### Takeaway
The cycle is driven by a hypothalamic–pituitary–ovarian feedback loop: FSH recruits follicles → the dominant follicle's rising oestradiol triggers an LH surge (positive feedback) → ovulation → the corpus luteum secretes progesterone for the luteal phase. The luteal phase is *less* variable than the follicular phase but is not fixed at 14 days: large datasets put its mean at ~12.4 days with a range of roughly 7–17 days; most cycle-length variation comes from the follicular phase.

### Cited Findings
- Early follicular phase: rising FSH stimulates follicular recruitment and maturation; the resulting oestradiol selectively inhibits FSH release and maintains rapid GnRH pulsatility in the late follicular phase — [Endotext / NCBI summary via search](https://www.endotext.org/?p=22242); [HERO/EPA ref](https://hero.epa.gov/hero/index.cfm/reference/details/reference_id/7354559)
- The LH surge is primarily triggered by a surge in oestradiol from the maturing follicle, which feeds back positively on hypothalamus and pituitary; the surge lasts ~24–48 h and triggers ovulation — [advancestudy.org](https://advancestudy.org/?p=10545) (secondary source)
- After ovulation, LH stimulates the empty follicle (corpus luteum) to produce progesterone throughout the luteal phase — [advancestudy.org](https://advancestudy.org/?p=10545) (secondary source)
- **Bull et al. 2019 (Natural Cycles, 612,613 ovulatory cycles, 124,648 users):** mean follicular phase 16.9 days (95% CI 10–30); mean luteal phase 12.4 days (95% CI 7–17) — [Bull et al., npj Digit Med 2019](https://www.nature.com/articles/s41746-019-0152-7)
- **Fehring et al. 2006 (JOGNN; 165 women aged 21–44, regularly cycling):** follicular phase mean/median/mode/SD = 16.5/16/15/3.4 days; luteal phase = 12.4/13/13/2.0 days; follicular ~11–27 days, luteal ~7–15 days; "the follicular phase contribut[es] most to this variability" — [Fehring, Schneider & Raviele 2006](https://epublications.marquette.edu/context/nursing_fac/article/1010/viewcontent/auto_convert.pdf); [RRM Academy summary](https://rrmacademy.org/library/variability-in-the-phases-of-the-menstrual-cycle-recsxkk9jmsoksgza/). Note: search snippets gave n=165 women; the commonly cited abstract says 141 women/1,060 cycles — sample size discrepancy unresolved because the PDF could not be fetched.
- Flo app cohort (Grieger & Norman 2020): more cycles with short luteal phases in younger women; women ≥40 had more cycles with longer luteal phases — [JMIR 2020;22(6):e17109](https://www.jmir.org/2020/6/e17109/PDF)

### Inferences
- Two independent methods (BBT/LH from app users; urinary/mucus markers in Fehring) converge on a mean luteal phase of ~12.4 days, not 14. An app that back-calculates ovulation as "next period − 14" will on average place ovulation ~1.5 days too early in the cycle and will be wrong by several days in many cycles.
- Because the luteal phase is the more stable phase, it is still the better anchor for retrospective ovulation estimation — but prediction should use a personal luteal estimate (ideally from confirmed ovulation via LH tests/BBT) with a distribution, not a constant.

### Gaps
- Precise timing from LH surge onset to ovulation (often quoted as ~24–36 h) was not confirmed in any fetched snippet.
- Corpus luteum lifespan (~14 ± 2 days classically) not confirmed in snippets.
- Fehring sample size discrepancy (141 vs 165 women) unresolved.

## 2. Large dataset findings (Bull 2019, Apple Women's Health Study, Clue/Flo, Fehring 2006, Wilcox 2000)

### Takeaway
Mean cycle length in large app datasets is ~29 days; only ~13–16% of cycles/women have a 28-day cycle; ovulation in a 28-day cycle falls on day 14 in only ~20% of cycles; and cycle length shortens with age into the 40s, then lengthens and becomes much more variable around 50. Fertile-window timing is unpredictable even in "regular" women.

### Cited Findings
**Bull et al. 2019 (npj Digital Medicine; Natural Cycles + UCL)**
- 612,613 ovulatory cycles from 124,648 users; mean cycle length 29.3 days — [Bull et al. 2019](https://www.nature.com/articles/s41746-019-0152-7); [ResearchGate copy](https://www.researchgate.net/publication/335422962_Real-world_menstrual_cycle_characteristics_of_more_than_600000_menstrual_cycles)
- Mean cycle length decreased by 0.18 days per year of age from 25 to 45; mean follicular phase length decreased by 0.19 days per year (i.e., the age-related shortening is almost entirely follicular) — [Bull et al. 2019](https://www.nature.com/articles/s41746-019-0152-7)
- Only ~13% of cycles were 28 days long — [Oura blog summarising Bull](https://ouraring.com/blog/busting-the-14-day-ovulation-myth/); [Natural Cycles/UCL press release](https://www.prnewswire.com/news-releases/natural-cycles--ucl-release-groundbreaking-data-in-womens-reproductive-health-300916536.html) (secondary)
- In 28-day cycles, ovulation was most commonly on day 15 (27%), then day 16 (21%), then day 14 (20%); there was a ~10-day spread of ovulation days for a 28-day cycle, and similar spread for all cycle lengths — same secondary sources as above
- (unverified — from background knowledge) Bull also reported BMI-associated differences in cycle length/variability and that a large share of women had cycle-to-cycle variation >7 days; could not confirm exact figures.

**Apple Women's Health Study (Li et al. 2023, Hum Reprod Open / Harvard–NIEHS)**
- 165,668 cycles from 12,608 US participants — [Li et al. 2023](https://pubmed.ncbi.nlm.nih.gov/37248288/); [Harvard AWHS update](https://hsph.harvard.edu/research/apple-womens-health-study/study-updates/menstrual-cycles-today-how-menstrual-cycles-vary-by-age-weight-race-and-ethnicity)
- Mean cycle length is shorter with older age across all age groups until 50, then longer for those ≥50 — same
- Cycle variability is lowest at ages 35–39; ~46% higher in those <20 and 45–49; ~200% higher in those >50 (vs 35–39) — same
- Asian participants' cycles average 1.6 days longer and Hispanic participants' 0.7 days longer than white non-Hispanic participants, with larger variability — same
- BMI ≥40 kg/m²: cycles ~1.5 days longer than BMI 18.5–25, with higher variability — same

**Flo app global cohort (Grieger & Norman 2020, JMIR) — note: often misattributed to Clue; it is Flo data**
- 16.32% (257,889/1,579,819) of women had a 28-day median cycle length; more women ≥40 had a 27-day median than women 18–24 — [JMIR 2020](https://www.jmir.org/2020/6/e17109/PDF)
- Median cycle length and phase lengths did not differ materially with BMI except at BMI ≥50 — same

**Clue data (Li, Urteaga et al. 2020, npj Digital Medicine — Columbia University, not Oxford)**
- Characterised users as consistently highly variable vs not, with differences in cycle and period characteristics and symptoms — [Li et al. 2020, npj Digit Med](https://www.nature.com/articles/s41746-020-0269-8); [arXiv preprint](https://arxiv.org/pdf/1909.11211). Specific numbers could not be retrieved.

**Wilcox et al. 2000 (BMJ 321:1259) — fertile window timing**
- 221 healthy women planning pregnancy, 696 cycles, ovulation estimated from urinary oestrogen/progesterone metabolites — [Wilcox, Dunson & Baird 2000](https://www.bmj.com/lookup/volpage/321/1259); [AAFP summary](https://www.aafp.org/afp/2001/0501/p1829a)
- On days 12 and 13, more than half the women were in the fertile window; 17% were already in it by cycle day 7 — same
- On every day between days 6 and 21, women had at least a 10% probability of being in the fertile window — same
- Only ~30% of women had the fertile window entirely within days 10–17 (the clinical-guideline window) — same
- The 16% reporting irregular periods ovulated later and more variably; authors concluded fertile window timing "can be highly unpredictable, even if their cycles are usually regular" — same

### Inferences
- "28 days / ovulation day 14" describes a minority of cycles. Defaults in an app should be ~29 days, with ovulation shown as a probability distribution spanning several days.
- Age is a key personalisation covariate: expect a gradual ~2-day shortening between 25 and 35/45 (Bull), lowest variability in late 30s, and rising variability/longer cycles in the mid-40s+ (AWHS).
- Ethnicity and very high BMI shift mean cycle length by ~1–1.6 days — small but relevant priors.

### Gaps
- Bull 2019 exact figures for within-woman variability (% with >7-day variation), bleed length, and BMI effects not confirmed.
- No reliable Clue/Oxford study found; the Clue academic work identified is with Columbia (Li et al. 2020). The "Oxford" link may be a misremembering — flag for the report writer.
- AWHS age-bracket mean cycle lengths (e.g., ~30 d at <20, ~28 d at 40–44) not retrieved.

## 3. Normal vs abnormal: FIGO definitions, flow volume, heavy menstrual bleeding, what flow intensity indicates

### Takeaway
FIGO 2018 "System 1" defines normal as: frequency 24–38 days, regularity (shortest–longest cycle) ≤7–9 days depending on age, duration ≤8 days, and volume defined by the patient's perception (historically 5–80 mL). Average blood loss is ~30–40 mL per cycle. Clinically (NICE), heavy menstrual bleeding is defined by its impact on quality of life, not a measured volume.

### Cited Findings
- FIGO 2018 normal limits: frequency 24–38 days (<24 = frequent, >38 = infrequent); duration ≤8 days; regularity: variation between shortest and longest cycle ≤7–9 days — specifically ≤9 days at ages 18–25 and 42–45, ≤7 days at 26–41 — [Munro et al. 2018, FIGO revisions, Int J Gynecol Obstet](https://obgyn.onlinelibrary.wiley.com/doi/10.1002/ijgo.12666); [Jain et al. 2023 FIGO Systems 1 & 2](https://obgyn.onlinelibrary.wiley.com/doi/full/10.1002/ijgo.14946)
- Volume: heavy >80 mL, normal 5–80 mL, light <5 mL (research definitions); StatPearls summarises normal as 24–38 days, 2–7 days bleeding, 5–80 mL — [StatPearls, Abnormal Uterine Bleeding](https://www.ncbi.nlm.nih.gov/sites/books/NBK532913/); [MSD Manual](https://www.msdmanuals.com/professional/gynecology-and-obstetrics/abnormal-uterine-bleeding/abnormal-uterine-bleeding)
- NICE NG88: HMB is "excessive menstrual blood loss which interferes with a woman's physical, social, emotional and/or material quality of life"; interventions should aim to improve quality of life rather than focusing on blood loss alone — [NICE NG88 Context](https://www.nice.org.uk/guidance/ng88/chapter/Context); [NICE NG88](https://www.nice.org.uk/guidance/ng88)
- Average menstrual blood loss 30–40 mL per cycle, based on Hallberg et al. 1966 (Acta Obstet Gynecol Scand 45:320) population study — [AAFP, Treatment of Menorrhagia 2007](https://www.aafp.org/afp/2007/0615/p1813)
- FIGO PALM-COEIN classifies causes of AUB (structural: Polyp, Adenomyosis, Leiomyoma, Malignancy; non-structural: Coagulopathy, Ovulatory dysfunction, Endometrial, Iatrogenic, Not otherwise classified) — [Munro et al. 2018](https://obgyn.onlinelibrary.wiley.com/doi/10.1002/ijgo.12666)
- ACOG recommends screening adolescents with HMB for bleeding disorders — [ACOG CO 785, 2019](https://www.acog.org/clinical/clinical-guidance/committee-opinion/articles/2019/09/screening-and-management-of-bleeding-disorders-in-adolescents-with-heavy-menstrual-bleeding)

### Inferences
- App flags could map directly to FIGO: cycle <24 or >38 days; shortest–longest spread >7 days (age 26–41) or >9 days (18–25, 42–45); bleeding >8 days; plus self-reported heavy flow that affects daily life (NICE framing).
- Self-reported "flow intensity" (light/medium/heavy) is subjective; the 80 mL threshold is a research measure (alkaline haematin) that users can't measure. Practical proxies (e.g., changing products every 1–2 h, clots >2.5 cm, flooding) are used clinically but were not sourced here.
- Flow intensity alone doesn't indicate fertility or ovulation; persistent heavy flow is a prompt to see a clinician (possible fibroids, adenomyosis, coagulopathy, ovulatory dysfunction).

### Gaps
- Clinical practical criteria for HMB (pad/tampon change frequency, clot size, PBAC score thresholds) not sourced.
- FIGO 2018 dropped volume numbers in favour of patient perception — snippets conflate the older 2011 mL figures with 2018; check the original if precision matters.

## 4. How cycles change with age, after contraception, with stress, with travel/shift work

### Takeaway
Cycles are long and frequently anovulatory for ~3 years after menarche, settle into the most regular pattern in the late 30s, shorten (mostly via the follicular phase) through the 30s–40s, then become irregular in perimenopause (STRAW: persistent ≥7-day change = early transition; ≥60-day gap = late transition). After the pill, the first cycle is often a few days longer and fully normalises for most within 1–3 months. Circadian disruption (rotating night shifts) modestly raises irregularity; stress evidence is weaker.

### Cited Findings
**Adolescence**
- Median menarche ~12.43 years; stable at 12–13 years in well-nourished populations — [ACOG Committee Opinion 651 (2015)](https://pubmed.ncbi.nlm.nih.gov/26595586/)
- Second year after menarche: 50% of cycles fall in 21–45 days, 80% by two years, 95% by three years postmenarche (snippet wording ambiguous on years) — [ACOG CO 651](https://pubmed.ncbi.nlm.nih.gov/26595586/); [Columbia Academic Commons](https://academiccommons.columbia.edu/doi/10.7916/cef8-4t37/download)
- Early cycles often anovulatory; when menarche is before age 12, ~50% of cycles are ovulatory in the first gynaecological year — same
- AWHS: variability ~46% higher at <20 than at 35–39 — [Li et al. 2023](https://pubmed.ncbi.nlm.nih.gov/37248288/)

**30s–40s**
- Cycle shortens 0.18 days/year from 25–45, mostly follicular — [Bull et al. 2019](https://www.nature.com/articles/s41746-019-0152-7)
- Lowest variability at 35–39 — [AWHS](https://hsph.harvard.edu/research/apple-womens-health-study/study-updates/menstrual-cycles-today-how-menstrual-cycles-vary-by-age-weight-race-and-ethnicity)

**Perimenopause**
- STRAW+10 early menopausal transition (stage −2): persistent ≥7-day difference in length of consecutive cycles; late transition (stage −1): ≥60 days of amenorrhoea — [STRAW executive summary, Fertil Steril](https://www.fertstert.org/article/S0015-0282(01)02909-0/fulltext); [Harlow et al., Climacteric](https://www.tandfonline.com/doi/full/10.1080/13697130701258838)
- AWHS: cycles lengthen at ≥50 and variability is ~200% higher than at 35–39; variability ~46% higher at 45–49 — [Li et al. 2023](https://pubmed.ncbi.nlm.nih.gov/37248288/)

**After stopping hormonal contraception**
- Recent pill stoppers: mean cycle length 33.3 days vs 29.6 days in non-users in one study — [Hertility blog](https://hertilityhealth.com/blog/how-long-does-period-take-to-return-after-stopping-the-pill) (secondary; original likely Natural Cycles/Bull or Gnoth)
- Natural Cycles data: median first post-HBC cycle 31 days after pill, hormonal IUD or ring; by the second cycle median length matched later cycles and never-users — [Natural Cycles research library](https://www.naturalcycles.com/research-library/how-soon-does-ovulation-return-after-stopping-hormonal-birth-control) (company source)
- Gnoth et al. (Gynecol Endocrinol): major disturbances (cycle >35 days, luteal phase <10 days, or anovulation) significantly more frequent post-pill up to the 7th cycle; reversible but recovery could take ≥9 months — [Gnoth et al., Gynecol Endocrinol vol 16(4)](https://www.tandfonline.com/doi/abs/10.1080/gye.16.4.307.317)

**Shift work / jet lag / stress**
- Lawson et al. 2011 (Nurses' Health Study II, 71,077 nurses aged 28–45 not on OCs): ≥20 months rotating night shifts → irregular cycles adjusted RR 1.23 (95% CI 1.14–1.33); cycles <21 days RR 1.27 (0.99–1.62); cycles ≥40 days RR 1.49 (1.19–1.87); dose-response — [Lawson et al., CDC Stacks](https://stacks.cdc.gov/view/cdc/44155)
- NHS3 (2015) also examined work schedule and menstrual function — [Lawson et al. 2015, Scand J Work Environ Health 41(2):194](https://www.sjweh.fi/article/3482)
- Flight attendants: one small study found irregular cycles in 21%; associations between circadian disruption and irregularity appear modified by stress, meal timing, prolactin/cortisol — [Neuroendocrinol Lett](https://www.nel.edu/assessment-of-the-occurrence-of-menstrual-disorders-in-female-flight-attendants-preliminary-report-and-literature-review-468); [JEHS review](https://apcz.umk.pl/JEHS/article/view/70323)
- Stress: Nagma et al. 2015 (J Clin Diagn Res, students) found association between high perceived stress (PSS >20) and irregularity — [JCDR 2015](https://jcdr.net/articles/PDF/5611/6906_CE[NJ]_F(P)_PF1(NJAK)_PFA(AK)_PF2(PAG).pdf). Small cross-sectional study, low quality evidence.

### Inferences
- Apps should widen prediction intervals for users <20, ≥45, in the first ~2–3 cycles after stopping hormonal contraception, and for shift workers/frequent long-haul travellers.
- A persistent ≥7-day change in cycle length in a user in her 40s is a STRAW marker worth surfacing as "possible early perimenopause" (informational, not diagnostic).

### Gaps
- No good-quality quantitative data found on jet lag/travel specifically (vs shift work).
- Stress evidence is mostly small cross-sectional studies; no large prospective estimate found.

## 5. The fertile window: sperm survival, egg survival, day-specific conception probabilities

### Takeaway
The fertile window is the ~6 days ending on ovulation day: sperm survive up to ~5 days, the egg ~a day or less. Conception probability per act of intercourse rises from ~10% five days before ovulation to ~33% around ovulation day (Wilcox 1995); other analyses put the peak 1–2 days before ovulation. Because ovulation timing varies, cycle-day-based windows mislead most women.

### Cited Findings
- Wilcox et al. 1995 (NEJM 333:1517; 221 women, 625 cycles, 192 pregnancies): conception occurred only with intercourse in a six-day window ending on the estimated ovulation day; probability ranged from 0.10 (day −5) to 0.33 (ovulation day) — [Wilcox, Weinberg & Baird 1995, NEJM](https://www.nejm.org/doi/full/10.1056/NEJM199512073332301); [FACTS About Fertility summary](https://www.factsaboutfertility.org/research/timing-of-sexual-intercourse-in-relation-to-ovulation-effects-on-the-probability-of-conception-survival-of-the-pregnancy-and-sex-of-the-baby/)
- (unverified — from background knowledge) Wilcox 1995 day-specific values: day −5 ≈0.10, −4 ≈0.16, −3 ≈0.14, −2 ≈0.27, −1 ≈0.31, 0 ≈0.33; no pregnancies from intercourse after ovulation day. Wilcox's model implied sperm viable up to ~5 days and egg ≤~24 h. Confirm before citing.
- A GitHub issue in an existing period app (lunarlog) specifically flags that a "+1 day" conception value is *not* in Wilcox 1995 — a real-world warning against extending the curve past ovulation day — [lunarlog issue #789](https://github.com/wjdavis5/lunarlog/issues/789)
- The most fecund days are the 2–3 days preceding ovulation, though the full fertile window may be ≥6 days — [Fertil Steril 2019 / ScienceDirect summary](https://www.sciencedirect.com/science/article/pii/S0015028219304327)
- Dunson, Baird, Wilcox & Weinberg 1999 (Hum Reprod) re-estimated day-specific probabilities of clinical pregnancy across two studies with imperfect ovulation measures; Wilcox, Dunson, Weinberg et al. (2001, Contraception) produced benchmark single-act conception rates — [demographic-research.org reference list](https://www.demographic-research.org/volumes/vol3/5/3-5.pdf); [Zhou 2006, Stat Methods Med Res](https://doi.org/10.1191/0962280206sm438oa)
- Colombo & Masarotto 2000 (7,017 cycles, 881 women, European mucus-method data): fertile window could extend up to 12 days in duration — [Demographic Research vol 3](https://www.demographic-research.org/volumes/vol3/5/3-5.pdf)
- Wilcox 2000: probability of being in fertile window ≥10% on every day 6–21; only ~30% of women have the window fully within days 10–17 — [BMJ 2000](https://www.bmj.com/lookup/volpage/321/1259)
- Cervical mucus quality on the day of intercourse is an accurate marker of highly fertile days — [Bilian et al., EJOG](https://www.ejog.org/article/S0301-2115(05)00411-2/abstract)

### Inferences
- Model the fertile window as ovulation day −5 to day 0 (inclusive), with peak probability on days −2 to 0, and convolve with the uncertainty in ovulation day (several days SD) — the resulting calendar window is naturally wider than 6 days.
- Don't show any meaningful conception probability for the day after ovulation (per Wilcox 1995).
- For contraception use cases, calendar-only estimates are inadequate given Wilcox 2000; physiological markers (BBT, LH, mucus) are required.

### Gaps
- Full Wilcox 1995 day-specific table, Dunson 2002 age-specific probabilities (decline with age, especially male age >35), and Wilcox 2001 single-act benchmarks not retrieved due to blocked pages.
- No direct sourced figures for sperm survival (5 days) or oocyte viability (12–24 h) beyond Wilcox model framing.
