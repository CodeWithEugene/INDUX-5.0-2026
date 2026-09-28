# Problem: discovery, evidence, and the one we will solve

> **Owner:** Team Suraksha Loop · **Research date:** 28 Sep 2026 · **Status:** decision made; the evidence register stays live.
>
> This document records **every problem we considered**, **why each one matters**, **what evidence we have**, and **which problem we will actually solve and why**. Evidence tags:
> - **[V]** verified at the cited URL
> - **[S]** secondary or reported (for example, a number from a news article or search snippet)
> - **[U]** unverified, or our own inference
>
> **Check every statistic marked [S] or [U] against the primary source before it goes on a slide.** The master evidence register is in [research.md §4](research.md).

---

## 0. The decision (one screen)

**We will build _Suraksha Loop_: a voice-first, multilingual occupational-safety early-warning loop for Indian MSME shop floors.**

A worker reports a hazard or near-miss **by voice, in their own language**. Suraksha Loop then:
1. turns the report into a **structured, triaged incident** with calibrated AI judgments;
2. places an **automatic hold on the affected machine's permit-to-work** when the danger is serious;
3. retrieves the relevant **SOP clause** and drafts a **corrective action and SOP fix** for supervisor approval;
4. sends a **45-second toolbox talk back to the next shift in each worker's language**;
5. **tells the reporter what happened** because they spoke up.

The near-miss reports feed a live **early-warning risk index** per zone and shift, together with **heat-stress** (WBGT) and **fatigue** (hours worked) signals.

| | |
|---|---|
| **Theme** | Environment, Health & Safety (EHS) |
| **Official anchor** | **PS-17** "AI Heat-Stress, Fatigue & Occupational Safety Early-Warning System", absorbing **PS-2** (SOP/expert knowledge assistant) and **PS-15** (multilingual assistance) |
| **One-line problem** | Workers on Indian factory floors see hazards first, but their warnings are lost. They speak languages the paperwork doesn't, reporting is a form they can't easily fill, and nothing ever comes back to them. So near-misses go unreported until they become amputations and deaths. |
| **One-line insight** | The cheapest, earliest safety sensor in a factory is the worker's voice. It only works if the system **listens in their language** and **closes the loop**. |
| **Why us, why now** | Indic speech and translation reached usable quality in 2025–26 (Hindi WER is about 5–8% on the best systems). Calibrated decision models (Jev) make trustworthy automation cheap. The OSH Code came into force on 21 Nov 2025. |

---

## 1. How we discovered problems (method)

### 1.1 Inputs
1. **The event itself**: 14 themes, 23 official 2026 problem statements, 103 industry problem statements from 2025, the six README evaluation criteria, and the 2025 jury composition (see [info.md](info.md)).
2. **Desk research** on government and authoritative sources: DGFASLI, NCRB ADSI, MoRTH, I4C/MHA, CPCB, MSME Ministry, PIB, ILO, Lancet Countdown, Census, Bhashini, the Supreme Court, and GTRI. Reputable journalism (IndiaSpend, Newslaundry, Down To Earth, The Wire, ThePrint, Mongabay) and NGO reports (Safe in India Foundation's *CRUSHED* series, IndustriALL) fill in where official data is thin.
3. **The India AI stack**: Sarvam, Bhashini, AI4Bharat, Claude, Gemini, TypeSafe Jev, Web Speech, WhatsApp Cloud API. This tells us what is feasible in 24 hours.
4. **Hackathon pattern research**: SIH, Google Solution Challenge, Imagine Cup and Devpost judging, plus the clichés juries are tired of (see [research.md §6](research.md)).

### 1.2 Filters every candidate had to pass
- **Real, quantified pain in India**, ideally visible in Madhya Pradesh or Gwalior-Chambal.
- **AI is essential**, not decorative. Without AI the solution either could not exist or would be far worse.
- **24-hour feasibility** as a working web prototype. Hardware must be optional or simulated.
- **Theme fit** with a manufacturing-heavy jury, a computer-vision academic judge, and a sovereign-AI sponsor.
- **Originality versus the crowd**: the 23 briefs and the usual college-hackathon clichés.
- **Ethics**: no worker surveillance, DPDP-aware handling, and no harm if the model is wrong.

### 1.3 Scoring weights (derived from the official six criteria plus our lenses)

| Criterion | Weight | Maps to the README criterion |
|---|---|---|
| Innovation / originality | 25% | innovation & originality |
| Real-world impact & strength of evidence | 20% | real world impact |
| 24-hour feasibility (working prototype, achievable technical depth) | 15% | feasibility, technical depth |
| Demo "wow" | 15% | prototype & demo quality |
| Theme fit / jury appeal (Industry 5.0, manufacturing jury) | 10% | (jury reality) |
| Differentiation from typical entries and crowded briefs | 10% | originality |
| Data / API availability | 5% | feasibility |

---

## 2. What the event tells us about the problem space

1. **Industry DNA.** The event name refers to Industry 5.0, which is human-centric, sustainable and resilient. The host's MD is National President of the **Quality Circle Forum of India**, where frontline workers solving problems is the core idea. The 2025 jury came from **Mondelez, JK Tyre, Godrej, Crompton Greaves and SRF**, almost all with plants in **Malanpur or Banmore**, a few kilometres from the venue **[V]**.
2. **Sponsors kept asking for safety and people.** Industry-submitted 2025 problem statements include **PS-30** Behaviour-Based Safety ("resistance to change and cultural barriers, inconsistent and poor quality of observations"), **PS-33** AI safety training for drivers and *casual workmen* ("mass scale learning application"), **PS-46** Unskilled manpower (contractors hire untrained labour, which leads to defects and breakdowns), **PS-23** tacit rules lost when leadership changes, **PS-24** contract-labour history including safety violations, **PS-83** worker safety in high dust, and **PS-93** PPE compliance by CV **[V]** (2025 Google Sheet; dump in [research.md](research.md)).
3. **The 2026 briefs will be crowded.** PS-2 (SOP assistant), PS-15 (multilingual), PS-16 (farmer bot) and PS-17 (heat/fatigue wearables) invite look-alike builds. The way to win is to **sit on a brief so the fit is obvious, then reframe it sharply**.
4. **The six criteria punish thin wrappers.** Technical depth and prototype quality are scored explicitly **[V]** (README).
5. **Judge and sponsor lenses.** The listed judge works on image processing and deep learning. The sponsor sells sovereign, on-prem, open-model AI **[V]**.

---

## 3. Candidate problems (15 + 1 cliché baseline)

Each candidate uses the same template: problem → persona → evidence → current solutions and gaps → why AI now → data/APIs → 24-hour feasibility → demo → risks.

---

### C1. Near-misses that never get heard: a voice-first, multilingual safety loop for MSME shop floors ⭐ *selected*
**Theme:** EHS (secondary: Multilingual AI). **Maps to:** 2026 PS-17, PS-2, PS-15; 2025 PS-30, PS-33, PS-46, PS-23, PS-93.

**Problem.** Deaths and amputations in Indian factories concentrate in small, subcontracted units staffed by inter-state migrant contract workers. They rarely get safety training they understand. The hazards they notice (a sensor taped over, a leaking valve, a missing guard) almost never get reported or acted on. SOPs, permits and forms are in English. Near-miss reporting, the *leading indicator* of serious accidents, barely exists, because it depends on literacy, forms, time and trust.

**Personas.**
- **Ramesh, 24**, from Gaya, Bihar. Speaks Magahi/Bhojpuri and Hindi, runs a power press at a Tier-2 auto-component supplier in Malanpur, and learned the machine on the job.
- **Sunita, 34**, the single-person safety officer, also doing HR and compliance, at a 150-worker MSME.
- **Mr. Agarwal, 52**, the plant head who answers to the OEM customer, the inspector and the insurer.

**Evidence.**
- **~3 deaths and 11 injuries per day** in registered factories (2017–2020, DGFASLI data via RTI). **3,331 deaths in 2018–2020, but only 14 people imprisoned** under the Factories Act **[S]**, https://www.indiaspend.com/special-reports/3-workers-die-every-day-in-indian-factories-govt-data-show-850083
- Reported non-fatal injuries fell from **25,500 (2014) to 2,949 (2023)**, while the fatal injury rate only moved from **6.32 to 5.46 per lakh workers** **[S]** (DGFASLI via Factly, https://factly.in/fewer-workplace-injuries-but-fatal-risks-persist-in-indian-factories/). Injury counts falling while fatality rates stay flat is the classic signature of **under-reporting** **[U]**.
- **Under-reporting, quantified:** in **2023 DGFASLI recorded 40 non-fatal injuries in Haryana, while one NGO (Safe in India) alone assisted 1,041 injured workers there, about 26× more** **[S]**, https://www.newslaundry.com/2026/06/15/safety-rules-are-routinely-flouted-in-indias-factories
- NCRB ADSI data: factory accidents are falling, but **deaths per 100 accidents rose from 66 (2010) to 89 (2024)**. There were **660 factory-accident deaths in 2024**, and **Madhya Pradesh ranked 4th with 70** (after Gujarat 121, Rajasthan 95, Maharashtra 87) **[S]**, https://insights.dataful.in/articles/factory-accidents-are-falling-but-deaths-remain-high
- **Safe in India Foundation, *CRUSHED 2025*:** 8,500+ injured workers assisted since 2016, and **79% lost fingers or limbs** **[S]**, https://m.thewire.in/article/labour/unsafe-machines-no-training-a-new-report-reveals-neglect-of-worker-safety-in-auto-sector
  - In 2025: **2,514 injured workers assisted**.
  - **93% of 2025 injuries involved power presses lacking safety sensors.**
  - **2 in 5 injured workers knew about the malfunction, and 84% had reported issues to supervisors that were ignored.**
  - **37% learned machine operation on the job with no formal training.**
  - **85% (Haryana) and 63% (Maharashtra) were migrants from Bihar, UP and Madhya Pradesh.**
  - **72% worked 60+ hours a week.**
  - **82% said auditors never spoke to workers.** **[S]** (Newslaundry, above)
- IndustriALL counted **240 accidents, 400+ deaths and 850+ serious injuries** in manufacturing, mining and energy in 2024 (to 10 Dec). Chemicals and pharma alone accounted for 110 accidents and 220+ deaths, and "the majority of the workers killed and injured are precarious workers" **[S]**, https://www.industriall-union.org/over-400-workers-killed-in-india-in-due-to-workplace-safety-lapses
- **Recent disasters:**
  - **Sigachi Industries**, Telangana, 30 Jun 2025: spray-dryer explosion, **46 dead** **[S]**, https://www.deccanherald.com/amp/story/india%2Ftelangana%2Fsigachi-pharma-plant-explosion-death-toll-rises-to-46-3636604
  - **Vedanta Singhitarai**, Chhattisgarh, 14 Apr 2026: **24 dead** **[S]**, https://countercurrents.org/2026/05/industrial-deaths-in-india-routine-tragedy-rare-accountability/
  - Firecracker units in 2026: Kakinada, 28 Feb, **21 dead** **[S]** (https://www.newsonair.gov.in/andhra-pradesh-21-killed-in-firecracker-manufacturing-unit-explosion-in-samarlakota); Tamil Nadu, 19 Apr, **21 dead** **[S]** (https://english.news.cn/asiapacific/20260420/8e45f42dc3224d44933c14c96b3bce61/c.html); Kaushambi UP, 1 Sep, **11 dead including 8 children** **[S]** (https://india.shafaqna.com/EN/india-firecracker-factory-explosion-kills-11-including-eight-children/).
  - Madhya Pradesh: **Harda, Feb 2024: 11 dead, 174 injured**, and workers said there was no fire extinguisher **[S]** (https://www.deccanherald.com/india/madhya-pradesh/no-fire-extinguisher-safety-gear-workers-recount-firecracker-factory-fire-in-madhya-pradeshs-harda-that-killed-11-2884007). **Dewas, May 2026: 2 dead, 15 injured** **[S]** (https://www.tribuneindia.com/news/madhya-pradesh/2-killed-15-injured-as-blast-triggers-blaze-at-firecracker-factory-in-mps-dewas/).
- **Enforcement gap:** **one inspector per 506 registered factories** (British Safety Council study; the year is **[U]**) **[S]**, https://www.business-humanrights.org/en/latest-news/india-nearly-6500-workers-have-died-in-industrial-accidents-in-the-past-five-years-reveals-government-data/. British Safety Council (2017) estimated **48,000 occupational-accident deaths a year** in India **[S]**, https://www.business-humanrights.org/en/latest-news/india-british-safety-council-report-says-48000-die-yearly-due-to-occupational-accidents/
- **Global:** ILO estimates **2.93 million work-related deaths (2019)**, about 63% in Asia-Pacific **[S]**, https://www.ilo.org/resource/news/nearly-3-million-people-die-work-related-accidents-and-diseases
- **Language gap:**
  - Only **10.6% of Indians speak English** (Census 2011) **[S]**, https://en.wikipedia.org/wiki/Multilingualism_in_India
  - **Bhojpuri (5+ crore speakers) is folded under "Hindi"** in the Census **[S]**, https://www.shankariasparliament.com/article/language-data-of-2011-census
  - **45.36 crore internal migrants (37%)** in Census 2011 **[S]**, https://www.drishtiias.com/daily-updates/daily-news-analysis/india-s-internal-migration
  - Research finds that training and signage only in the host language act as "a means of discrimination" for migrant workers **[S]**, https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6862054/
- **Regulatory tailwind:** all four Labour Codes, including the **Occupational Safety, Health and Working Conditions Code, 2020** (consolidating 13 laws including the Factories Act and the Inter-State Migrant Workmen Act), **came into force on 21 Nov 2025** **[S]**, https://www.legal500.com/intelligence/india/employment-and-hr/central-government-notifies-commencement-of-all-four-labour-codes-%E2%80%93-effective-21-november-2025
- **Why near-misses matter:** the Bird/Heinrich accident triangle is about **1 serious : 10 minor : 30 property damage : 600 near-misses**. The ratio is contested, but it is standard EHS vocabulary that every industry juror knows **[S]**, https://en.wikipedia.org/wiki/Accident_triangle

**Current solutions and gaps.** Enterprise EHS suites (VelocityEHS, Benchmark Gensuite, SafetyConnect, Safetymint, NeoEHS) are designed for English-literate supervisors, priced per seat, and built around forms. Detect Technologies T-Pulse targets CCTV analytics for large asset-heavy plants. **None close the loop** from a worker's own voice in their mother tongue → structured hazard → machine hold → SOP update → toolbox talk back in the worker's language → feedback to the reporter, for a **50–500-worker MSME** **[U]** (based on product pages; not an exhaustive market scan).

**Why AI now.** Indic ASR, MT and TTS became production-grade and cheap in 2025–26. Sarvam Saaras v3 covers 22 Indian languages plus English with a code-mix mode. The "Voice of India" benchmark reports **Hindi WER of 5.0% (Sarvam), 6.0% (Gemini 3 Pro) and 8.2% (IndicConformer)** **[V]**, https://arxiv.org/html/2604.19151v1. LLMs can structure rambling code-mixed speech into incident schemas. **Calibrated decision models (Jev)** can triage in about 100 ms for about $0.00005 per report **[V]** (docs.typesafe.ai). Vision models can check PPE and guards on-device.

**Data and APIs.** Sarvam / Bhashini / AI4Bharat for speech and translation; Claude Opus 5 for extraction; TypeSafe Jev for judgments; open PPE datasets and YOLO weights for CV; OSHA/HSE public SOP templates; open-meteo for heat; synthetic incident history modelled on *CRUSHED* distributions.

**24-hour feasibility: High.** It is mostly API composition, a dashboard and one small CV model. **Demo: very high.** A teammate speaks Bhojpuri-accented Hindi, "press number 3 ka sensor tape se band kiya hua hai", and within seconds a HIGH-severity "guard bypass" incident appears, Press 3's permit goes on hold, the LOTO SOP clause is cited, and a toolbox talk plays in Hindi, Odia and Bengali.

**Risks.**
- Bhojpuri/Magahi ASR quality (they are *not* among the 22 scheduled languages; Maithili is). Mitigation: Hindi ASR plus LLM normalisation, and **test before the event**.
- Hallucinated SOP advice. Mitigation: RAG with citations, a citation check, and supervisor approval.
- The "just another chatbot" perception. Mitigation: lead with the loop, the permit hold and leading indicators.
- Worker retaliation fears. Mitigation: an anonymous mode and a no-blame charter.

---

### C2. "Ustad": capturing retiring technicians' tacit knowledge in their own voice
**Theme:** AI & GenAI / Smart Manufacturing. **Maps to:** 2026 PS-2; 2025 PS-23, PS-11, PS-46.
- **Problem:** in MSMEs, the know-how for fixing a machine sits in one senior fitter's head. Manuals are English OEM PDFs, and juniors are high-churn contract workers.
- **Evidence:** PMMI 2025 says **74%** of CPG/OEM respondents call knowledge transfer extremely or very significant **[S]** (https://www.oemmagazine.org/pmmi-news/business-intelligence/article/22959283/navigating-the-loss-of-tribal-knowledge). US figures: 25% of the manufacturing workforce is over 55, and 97% of manufacturers worry about brain drain **[S]** (https://www.automate.org/robotics/industry-insights/the-great-knowledge-transfer-safeguarding-manufacturing-expertise-as-veteran-workers-retire). **India-specific numbers were not found [U].** The strongest India evidence is sponsor demand (2025 PS-23, PS-11, PS-46).
- **Gap:** knowledge captured from *speech* in Hindi and turned into validated fault → cause → check → fix trees.
- **Feasibility:** high. **Demo:** high. **Risk:** it overlaps heavily with the crowded PS-2, and India evidence is weak. **Verdict:** fold into C1 as "senior voice notes → SOP improvements".

### C3. "Listen to the Machine": phone-microphone acoustic predictive maintenance
**Theme:** IIoT / Predictive Intelligence. **Maps to:** PS-3; 2025 PS-4, PS-29, PS-40.
- **Evidence:**
  - **7.83 crore enterprises registered on Udyam and Udyam Assist (28 Feb 2026)**; MSMEs contribute **31.1% of GDP, 48.58% of exports and 35.4% of manufacturing output** **[S]** (https://www.ibef.org/news/over-7-83-crore-enterprises-registered-on-udyam-platforms-indicating-strong-msme-formalisation-growth).
  - About **99% of MSMEs are micro units**; MSMEs employ **32.8 crore** **[S]** (Mongabay 2026).
  - "70% of MSMEs not digitally adopted" **[U]**.
  - A real 2025 sponsor PS reported "Ribbon Machine Down time 14%" **[V]**.
- **Data:** MIMII and DCASE machine-sound datasets, AI4I 2020, NASA C-MAPSS, CWRU bearings.
- **Feasibility:** medium-high. **Demo:** high (play a faulty-pump sound and watch the anomaly score spike). **Risk:** lab-to-floor domain gap, and PS-3 is crowded. **Verdict:** a good future module ("machine sound as an incident attachment").

### C4. "CBAM Passport": EU carbon-border compliance for MSME steel and aluminium exporters
**Theme:** Sustainability.
- **Evidence:**
  - The CBAM definitive phase started **1 Jan 2026**. EU default values are **30–80% higher** than actual emissions **[S]** (https://vajiramandravi.com/current-affairs/eus-cbam-begins-impact-on-indias-steel-and-aluminium-exports/).
  - GTRI says exporters may need to **cut prices 15–22%** **[S]** (https://www.business-standard.com/industry/news/cbam-may-force-steel-aluminium-firms-cut-prices-gtri-125123101012_1.html).
  - India's steel and aluminium exports to the EU **fell 24.4% in FY25** **[S]** (https://www.alcircle.com/news/indian-steel-and-aluminium-exports-to-eu-plunge-24-4-per-cent-ahead-of-cbam-rollout-gtri-reports-115600).
  - **3,000–4,000 direct and 25,000–30,000 indirect exporters**; MRV costs about **₹25 lakh a year per firm** **[S]** (https://india.mongabay.com/2026/06/european-union-border-tax-tests-indias-small-iron-and-steel-businesses/).
- **Gap:** turning the bills and invoices an MSME already has into a CBAM communication template and a reduction plan.
- **Feasibility:** medium-high. **Demo:** medium-high. **Risk:** methodology correctness, low visual drama, and Gwalior is not a steel-export cluster. **Verdict:** a strong #3 and our fallback if the organisers push "Sustainability".

### C5. MSME compliance copilot for the Labour Codes transition
- **Evidence:**
  - A single-state manufacturing MSME faces **1,450+ obligations** and spends about **₹15.55 lakh a year** on compliance. **216+ clauses carry imprisonment**, and 44% of obligations are labour-related **[S]** (TeamLease RegTech, https://www.teamleaseregtech.com/msme-compliance-report/).
  - The consolidation into 4 Codes took effect on 21 Nov 2025 **[S]**.
- **Feasibility:** high. **Demo:** medium. **Risk:** legal liability and a crowded "RAG over law" pattern. **Verdict:** a C1 module (OSH obligations only).

### C6. "Kavach Call": a real-time guardian against digital-arrest and investment scams
**Theme:** Cybersecurity.
- **Evidence:**
  - I4C/NCRP: **₹19,812.96 crore lost across 21,77,524 complaints in 2025**; **77% of losses came from investment scams and 8% from digital arrest** **[S]** (https://the420.in/india-cyber-fraud-losses-i4c-data-statewise-investment-scams/).
  - **₹22,812 crore lost in 2024**, against ₹2,290 crore in 2022, with only about **2% refunded** **[S]** (CyberPeace, citing Rajya Sabha answers).
  - **Gwalior:** a 70-year-old CA lost **₹21+ crore** to a fake USDT scheme (Dec 2025–Jul 2026) **[S]** (https://theprint.in/india/gwalior-ca-loses-rs-21-crore-in-cyber-fraud-after-being-promised-high-returns-on-investments/2984792/).
  - McAfee (2023): **69% of Indians** were not confident they could spot a cloned voice **[S]**.
- **Feasibility:** medium (intercepting real calls is out of scope). **Demo:** very high. **Risk:** the "fraud detector" cliché, privacy, weak fit with a manufacturing jury, and falling digital-arrest numbers. **Verdict:** rejected for this jury.

### C7. OSINT disinformation and deepfake triage in Hindi
- **Evidence:** PIB Fact Check repeatedly debunked deepfakes of the Defence Minister and the Army Chief around **Operation Sindoor** (May 2025) and into 2026 **[S]**.
- **Feasibility:** low-medium. **Risk:** poor generalisation of deepfake detectors, PS-9 crowding, and political sensitivity. **Verdict:** rejected.

### C8. "Chambal Sentinel": Supreme Court–mandated sand-mining intelligence for Morena
**Theme:** Space Tech (secondary: Defence/Security).
- **Evidence:**
  - The **Supreme Court took suo motu cognizance on 13 Mar 2026**. On **17 Apr 2026** (2026 SCC OnLine SC 631) it ordered CCTV on mining routes, **GPS on all mining vehicles in Morena and Dholpur**, and **control rooms to analyse live feeds** **[S]** (https://www.scconline.com/blog/post/2026/04/18/monitoring-illegal-sand-mining-chambal-sanctuary-sc-directions/).
  - Forest guard **Jitendra Singh Shekhawat was run over by a tractor-trolley on 8 Jan 2026** **[S]** (https://www.verdictum.in/court-updates/supreme-court/stays-rajasthan-denotification-chambal-sanctuary-land-amid-rampant-illegal-sand-mining-1611216).
  - Research has already used object recognition on Sentinel/Resourcesat imagery to map mining landforms **[S]** (https://www.nature.com/articles/d44151-026-00112-x).
- **Build:** Sentinel-2 change detection, GPS-trajectory anomalies, CV on CCTV, and a Hindi evidence pack.
- **Feasibility:** medium, because of geospatial data wrangling. **Demo:** very high, and it is local (30–50 km from the venue). **Risk:** weaker fit with a manufacturing jury, local political sensitivity, and the 10 m pixel limit. **Verdict:** the strongest #2. Pick it only if the team has GIS skills and the jury turns out academic or defence-oriented.

### C9. "Parali Pulse": stubble-fire forecasting in Gwalior-Chambal
- **Evidence:**
  - **MP recorded the most crop-residue fires in India for the second straight year: 14,165 of 28,529 in 2025.** **7 of the 10 worst districts are in MP, including Sheopur (#1), Datia and Gwalior** **[S]** (https://www.downtoearth.org.in/air/madhya-pradesh-leads-in-farm-stubble-burning-for-second-year-uttar-pradesh-and-punjab-follow).
  - Punjab fell from 36,663 fires (2023) to 5,092 (2025) **[S]**.
- **Data:** NASA FIRMS, Sentinel-2 NDVI, open-meteo, CPCB AQI.
- **Feasibility:** medium-high. **Demo:** high. **Risk:** crowding with farmer bots (PS-16), and behaviour change is hard to prove. **Verdict:** rejected for jury fit.

### C10. Heat-stress guardian for shop-floor workers (WBGT work-rest scheduling)
**Theme:** EHS (PS-17 literal).
- **Evidence:**
  - The Lancet Countdown estimates India lost **247 billion potential labour hours to heat in 2024 (≈$194 bn)** **[S]** (https://www.policycircle.org/environment/extreme-heat-productivity-loss/).
  - ILO projects **5.8% of working hours lost by 2030, equivalent to 34 million jobs** **[S]**.
  - NCDC confirmed **14** heatstroke deaths for 1 Mar–24 Jun 2025, while HeatWatch counted **733** for Mar–Jun 2024, which points to under-counting **[S]**.
  - MP heatwave alerts covered **Gwalior and Morena** (Apr 2026) **[S]**.
- **Feasibility:** very high. **Demo:** medium. **Risk:** it is the most crowded PS-17 build (wearable dashboards). **Verdict:** fold into C1 as the heat-stress channel of the early-warning index.

### C11. Voice-first access to government schemes
- **Evidence:** real exclusion exists (Dvara Research). But **myScheme (2,500+ schemes), Jugalbandi and Kisan e-Mitra (92 lakh+ queries)** already exist **[S]**.
- **Verdict:** low originality, rejected.

### C12. Ambient scribe for ASHA health workers
- **Evidence:** **10 lakh+ ASHAs** do double data entry **[S]**. **MP's infant mortality rate is 40 per 1,000 vs 26 nationally** (SRS 2021) **[S]**.
- **Verdict:** real impact, but weak EHS or manufacturing fit and clinical-safety scrutiny. Rejected.

### C13. MP highway black-spot prediction
- **Evidence:** **4,80,583 accidents and 1,72,890 deaths in 2023** (MoRTH) **[S]**. **MP ranked 2nd in accidents (55,327) in 2023** **[S]**.
- **Verdict:** point-level data is closed (iRAD is restricted), and it is a trope. Rejected.

### C14. "Dukaan Drishti": kirana shelf photo → ONDC catalogue
- **Evidence:** ONDC had **7.6 lakh+ sellers (Mar 2025)**, and catalogue digitisation is the main barrier **[S]**.
- **Verdict:** far from the jury and a risk on VLM SKU accuracy. Rejected.

### C15. Low-cost counter-drone detection
- **Evidence:** BSF seized **272 drones on the Punjab border in 2025** **[S]**.
- **Verdict:** a noisy on-site demo, dual-use sensitivity, and a crowded YOLO trope. Rejected.

### R0. Crop-disease detection from leaf photos (the cliché baseline)
It is included only to calibrate the floor of the scoring scale. It is the single most common Indian student hackathon project. Local mustard crops (Morena's ODOP) don't change that.

---

## 4. Scoring matrix

Scores run from 1 to 10, and the weighted total is Σ(score × weight).

| # | Candidate | Innov (25) | Impact (20) | Feas (15) | Wow (15) | Fit (10) | Diff (10) | Data (5) | **Weighted** |
|---|---|---|---|---|---|---|---|---|---|
| **C1** | **Suraksha Loop: multilingual near-miss safety loop** | 8 | 9 | 8 | 9 | 10 | 8 | 7 | **8.50** |
| C8 | Chambal Sentinel: sand-mining surveillance | 9 | 8 | 6 | 9 | 7 | 10 | 7 | 8.15 |
| C2 | Ustad: tacit-knowledge capture | 8 | 7 | 8 | 8 | 9 | 8 | 6 | 7.80 |
| C4 | CBAM Passport | 8 | 8 | 7 | 7 | 8 | 9 | 7 | 7.75 |
| C6 | Kavach Call: anti-scam guardian | 7 | 9 | 7 | 9 | 7 | 5 | 6 | 7.45 |
| C9 | Parali Pulse: stubble fires | 7 | 8 | 7 | 8 | 7 | 7 | 9 | 7.45 |
| C3 | Listen to the Machine: acoustic PdM | 7 | 7 | 7 | 8 | 9 | 6 | 8 | 7.30 |
| C10 | Heat-stress guardian | 6 | 8 | 9 | 6 | 8 | 6 | 9 | 7.20 |
| C5 | Labour-Code compliance copilot | 6 | 8 | 8 | 6 | 7 | 6 | 6 | 6.80 |
| C12 | ASHA ambient scribe | 6 | 8 | 7 | 7 | 5 | 5 | 5 | 6.45 |
| C14 | Kirana → ONDC | 6 | 6 | 7 | 7 | 6 | 6 | 5 | 6.25 |
| C7 | Deepfake/OSINT triage | 6 | 7 | 5 | 7 | 6 | 4 | 6 | 6.00 |
| C15 | Counter-drone | 5 | 7 | 6 | 7 | 6 | 4 | 7 | 5.95 |
| C13 | MP black-spot prediction | 4 | 8 | 7 | 6 | 5 | 3 | 6 | 5.65 |
| C11 | Voice-first schemes | 3 | 8 | 8 | 6 | 5 | 2 | 8 | 5.55 |
| R0 | Crop-disease detection | 2 | 7 | 9 | 5 | 3 | 1 | 9 | 4.85 |

**Worked example:** C1 = 8(.25) + 9(.20) + 8(.15) + 9(.15) + 10(.10) + 8(.10) + 7(.05) = 2.00 + 1.80 + 1.20 + 1.35 + 1.00 + 0.80 + 0.35 = **8.50**.

**Sensitivity analysis [U].**
- If Innovation were weighted 40% (Devpost's single criterion) and the others scaled down proportionally, C8 would narrowly overtake C1 (≈8.4 vs ≈8.3).
- Under the official six-criterion reading, with a manufacturing-heavy jury, C1 wins clearly.
- If the on-site jury turns out academic or defence-heavy, C8 becomes competitive. The sponsor's sovereign-AI positioning favours both equally.
- **We accept this risk because C1's score is robust across five of the seven lenses.**

---

## 5. Why C1, and not the others

### 5.1 Why C1 wins
1. **The jury literally asked for it.** The 2025 industry sponsors submitted Behaviour-Based Safety, AI safety training for casual workmen, unskilled contract labour, tacit rules, contract-labour history and PPE compliance. The 2026 list has PS-17, PS-2 and PS-15. C1 hits all of them with **one coherent product**.
2. **The evidence is visceral, recent and local:**
   - about 3 factory deaths a day;
   - 26× under-reporting;
   - 93% of 2025 injuries on sensor-less power presses;
   - **84% of injured workers had reported the problem and were ignored**;
   - most injured workers are migrants from Bihar, UP **and MP**;
   - **MP ranked 4th in factory deaths in 2024**;
   - Harda 2024, Sigachi 2025, the 2026 firecracker blasts;
   - the OSH Code in force since 21 Nov 2025.
3. **It is novel inside a crowded brief.** Others will build "SOP chatbot" (PS-2) or "wearable heat dashboard" (PS-17). We build the **closed loop**, which is the human-centric principle of Industry 5.0 and the frontline-problem-solving culture of QCFI.
4. **It shows technical depth across the whole AI stack:** speech, language, calibrated decisions, retrieval, generation, vision and analytics, all evaluated.
5. **It is feasible in 24 hours** with free or cheap Indic AI APIs plus open-source fallbacks.
6. **It pleases every stakeholder honestly:**
   - industry gets fewer incidents, compliance evidence and ₹ ROI;
   - the CV judge gets an on-device PPE/guard detector with metrics and privacy;
   - the sovereign-AI sponsor gets an on-prem open-model mode;
   - QCFI-minded hosts see workers as problem-solvers.
7. **It absorbs C2, C5 and C10 as modules.** Scalability and roadmap are clear, and the core stays focused.

### 5.2 Why not C8 (the closest rival)
- Weaker fit with a manufacturing jury, and politically sensitive locally (mining mafias).
- Geospatial data risk in 24 hours (cloud-free tiles, 10 m resolution).
- **Keep it as our backup** if the organisers or the jury profile shift.

### 5.3 Why not C4
- Methodology correctness risk under a 24-hour build.
- Low visual drama, and Gwalior is not a steel-export cluster.
- **Keep it as a talking point** in the roadmap ("the same document-intelligence engine could produce CBAM packs").

### 5.4 How the runners-up live inside Suraksha Loop

| Module | Absorbed from | Status in the 24-hour build |
|---|---|---|
| Heat-stress channel (WBGT per zone per shift) | C10 | **In scope** (makes the PS-17 fit literal) |
| Fatigue channel (roster hours → risk) | C10 / PS-17 | **In scope** (simple, data-driven) |
| Senior-technician voice notes → SOP improvements | C2 | Stretch |
| OSH Code obligations checklist | C5 | Stretch (roadmap slide) |
| Machine-sound attachment on incidents | C3 | Roadmap |

---

## 6. The chosen problem in depth

### 6.1 Problem statement (final, abstract-ready)
> In Indian MSME factories, the people who see hazards first are the shop-floor workers, many of them migrant contract workers who speak Hindi, Bhojpuri, Odia or Bengali rather than English. Their warnings rarely reach anyone who can act. Reporting means English paper forms or apps. Supervisors are overloaded. And when workers *do* speak up, nothing comes back: in 2025, 84% of injured workers assisted by one NGO had already reported the machine problem and been ignored. The result is a system blind to its own leading indicators. Near-misses go unrecorded (official injury figures undercount by ~26× in one state), and hazards become amputations and deaths: about 3 deaths a day in registered factories, 660 factory-accident deaths in 2024, and MP 4th nationally with 70.

### 6.2 Root-cause analysis

**5-Why (why did Ramesh lose two fingers?)**
1. Why? The power press cycled while his hand was in the die area.
2. Why? The light-curtain sensor had been taped over to speed up production.
3. Why wasn't it fixed? He mentioned it to the line supervisor twice, verbally, in Bhojpuri-Hindi, and it was never logged.
4. Why wasn't it logged? The only reporting channel is an English near-miss form in the safety office. The supervisor was measured on output, not safety, and no one asked him.
5. Why does the system tolerate this? There is no cheap, trusted, language-inclusive channel that turns frontline observations into **tracked actions with accountability**, and no feedback loop that makes reporting feel worthwhile.

**Fishbone (Ishikawa) summary**

| Category | Causes |
|---|---|
| **People** | Migrant contract workers; low formal training (37% learned on the job); long hours (72% at 60+ h/week); fear of blame or job loss; supervisors measured on output |
| **Method** | English-only forms and SOPs; no near-miss culture; permit-to-work on paper; audits that skip workers (82% never spoken to) |
| **Machine** | Power presses without sensors (93% of injuries); guards bypassed for speed; no interlock feedback |
| **Material / information** | SOPs not in workers' languages; tacit knowledge not captured; no reliable data |
| **Measurement** | Lagging indicators only (injuries); under-reporting (~26×); no leading-indicator dashboard |
| **Environment** | Heat (tin sheds, furnaces, 45 °C+ summers in Gwalior-Chambal); noise; night shifts; subcontracted units with no safety officer |

### 6.3 Stakeholder map

| Stakeholder | Role | Pain today | What they need from us | Influence |
|---|---|---|---|---|
| Shop-floor worker (migrant, contract) | Primary user (reporter, trainee) | Unheard; unsafe machines; training they can't understand | Speak once, in their language, be heard, see action, stay anonymous if needed | Low today → **high with us** |
| Line supervisor / shift in-charge | Primary user (first responder) | Output pressure; verbal reports lost; no time for forms | A prioritised, pre-structured queue; one-tap acknowledge; auto-drafted actions | Medium |
| Safety officer (often part-time, also HR) | Primary user (EHS owner) | Paperwork; no data; compliance anxiety | Structured incidents, CAPA tracking, audit-ready records, leading indicators | Medium |
| Plant head / owner | **Buyer** | Inspector, OEM audits, insurance, downtime, reputation | Fewer incidents, compliance evidence, ROI, low cost, no IT burden | **High** |
| Maintenance head | Secondary user | Learns about bypassed guards too late | Machine-linked hazards; holds; fix confirmation | Medium |
| OEM customer (e.g., auto OEM's supplier-quality team) | Influencer / mandator | Supplier-safety risk in the chain | Supplier safety scorecards | High |
| Contractor / labour agency | Secondary | Blamed; untrained labour | Worker-level training records (consented) | Low |
| Factory inspector (DISH/state) | External | 1 inspector per ~506 factories | Credible records | Medium |
| QCFI chapters / industry associations | Channel | Promoting quality circles | Tools that make frontline problem-solving measurable | Medium |
| Insurers (ESIC and private) | Future partner | Claims | Risk data (aggregate, consented) | Medium |

### 6.4 Personas (detailed)

**Ramesh Kumar, 24: power-press operator (primary user).**
- **Background:** from Gaya, Bihar; 3 years in Malanpur through a labour contractor; lives in shared rooms near the industrial area.
- **Languages:** Magahi at home, Hindi at work; reads basic Hindi slowly, no English.
- **Device:** Redmi/Realme Android (~₹8,000), WhatsApp daily, YouTube in Hindi, patchy 4G inside the shed.
- **Shifts:** 12-hour shifts, often 6–7 days a week.
- **Goals:** keep the job, send money home, not get hurt.
- **Fears:** being blamed; the contractor dropping him; "complaining" labels.
- **Quote (illustrative):** *"Bola tha supervisor ko… kuch nahi hua."* ("I told the supervisor… nothing happened.")
- **Success for Ramesh:** he reports in 20 seconds without typing, hears back in Hindi that "Press 3 is locked until the sensor is fixed", and nobody knows it was him.

**Sunita Verma, 34: safety officer cum HR (primary user).**
- **Background:** B.Sc. plus a 1-year diploma in industrial safety; a 150-worker auto-component MSME, one person covering EHS, HR and compliance.
- **Tools:** Excel, WhatsApp groups, paper registers.
- **Goals:** zero reportable injuries, audit-ready files for the OEM customer and inspector, less paperwork.
- **Pain:** hazards reach Sunita only after incidents, and there is no way to train 150 workers in 5 languages.
- **Success for Sunita:** a morning dashboard with the 3 real risks, drafted CAPAs to approve, training delivered and verified automatically, and an audit export in one click.

**Mr. R. K. Agarwal, 52: plant head / owner (buyer).**
- **Background:** runs 2 units supplying an auto OEM, and cares about OEE, delivery and cost.
- **Worries:** an accident means shutdown, police, compensation, lost customer and reputation. The OSH Code transition adds anxiety.
- **Buying criteria:** price per month under a supervisor's salary, zero IT setup, works on existing phones, data stays with him, and evidence he can show the OEM and inspector.

### 6.5 Current workflow (as-is) and failure points

```
Hazard noticed by worker
   │  ✗ No channel in worker's language; fear of blame
   ▼
Verbal mention to supervisor (maybe)
   │  ✗ Not recorded; output pressure; forgotten
   ▼
(Rarely) English near-miss form filled by safety officer from memory
   │  ✗ Details lost; no severity logic; no machine link
   ▼
Excel / paper register
   │  ✗ No prioritisation; no CAPA tracking; no trend analysis
   ▼
Monthly safety meeting (maybe)
   │  ✗ Toolbox talks in English/Hindi only; no comprehension check
   ▼
Worker never hears back → stops reporting → hazard persists → INJURY
```

### 6.6 Jobs-to-be-done
- **Worker:** "When I see something dangerous, I want to tell someone who will actually fix it, in my own words and language, without getting into trouble, so that I and my friends don't get hurt."
- **Supervisor:** "When a hazard is reported, I want to know instantly how serious it is and what to do, so I can act before my shift ends without extra paperwork."
- **Safety officer:** "When I prepare for an audit, I want complete, structured records of hazards, actions and training, so I can prove compliance and focus on prevention."
- **Plant head:** "When I think about safety risk, I want early warning and evidence, so that I avoid shutdowns, liability and losing customers."

### 6.7 Quantifying the cost (for the ROI slide; assumptions marked)
- **Human cost:** amputations (79% of cases in the *CRUSHED* cohort) end livelihoods. This is the headline, not rupees.
- **Employer cost per serious injury [U, to be refined with the Employee's Compensation Act formula and ESIC rules]:**
  - statutory compensation (a function of wage × age factor × % disability);
  - production stoppage and investigation;
  - legal exposure under the OSH Code;
  - OEM supplier-audit penalties;
  - replacement training.
  - **Our planning assumption: ₹5–15 lakh all-in per serious injury in an MSME [U].**
- **Suraksha Loop cost:** about **₹4 per report** in AI costs (see [solution.md §14](solution.md)), plus an indicative subscription (hypothesis: ₹3,999–₹9,999 per plant per month).
- **Break-even logic:** preventing **one** serious injury per plant every few years pays for the system many times over. The interview answer is "one prevented amputation pays for about 10 years of the tool" **[U]**, and it must be validated with real inputs.

### 6.8 Why now
1. **Technology:** Indic ASR/MT/TTS quality (2025–26); cheap calibrated decision models (Jev, launched Sep 2026, $0.042 per M input tokens); on-device CV in the browser (WebGPU/WASM).
2. **Regulation:** OSH Code in force since 21 Nov 2025. DPDP Rules 2025 set up privacy-by-design expectations (Consent Manager provisions from about 13 Nov 2026; full obligations May 2027).
3. **Market:** OEMs and exporters are pushing supplier ESG and safety audits (CBAM and ESG pressure reach MSME supply chains).
4. **Culture:** the Industry 5.0 / human-centric narrative, and QCFI quality circles, are mainstream in the host ecosystem.

### 6.9 Success metrics (what "solved" looks like)

| Level | Metric | Baseline (assumed) | Pilot target (3 months) |
|---|---|---|---|
| Leading | Near-miss reports per 100 workers per month | ~0–2 (paper) **[U]** | **≥ 15** |
| Leading | % of reports acknowledged by a supervisor within 1 shift | unknown / low | **≥ 90%** |
| Leading | Median time from hazard reported to control applied (hold or fix) | days to never | **< 4 h** for high severity |
| Leading | % of reporters who receive closure feedback | ~0% | **100%** |
| Learning | Toolbox-talk comprehension (quiz pass rate, per language) | unmeasured | **≥ 80%** |
| Lagging | Recordable injuries (LTIFR) | plant-specific | trend down (12-month horizon) |
| Trust | % anonymous vs named reports (named rising = trust) | — | named share rises over time |
| Quality | Triage agreement with the safety officer (severity ±1) | — | **≥ 85%** |

### 6.10 Assumptions to validate before the 8–9 Oct interview (validation plan)

| # | Assumption | How we validate (by 7 Oct) | Evidence we want on a slide |
|---|---|---|---|
| A1 | Workers will report by voice if it's anonymous and in their language | 5–10 short phone or in-person conversations with factory or construction workers (Hindi); ITI students with factory internships | Quotes + "x of y would use it" |
| A2 | Supervisors and safety officers lack time and structure | 2–3 calls with EHS/safety officers (LinkedIn, QCFI chapter members, alumni in Malanpur/Banmore/Pithampur/Manesar) | Their current process + pain in their words |
| A3 | Plant heads would pay ₹4–10k/month | 1–2 conversations with MSME owners or plant heads | Willingness-to-pay range |
| A4 | Hindi, Bhojpuri-accented and Odia ASR is good enough | Record 30–60 test utterances; measure WER on Sarvam, Bhashini and IndicConformer | WER table |
| A5 | Jev triage agrees with human severity | Label 40 synthetic reports; compare against Jev and LLM | Agreement % and calibration plot |
| A6 | Toolbox talks in the worker's language improve comprehension | Quick A/B with 5–10 people: an English/standard-Hindi talk vs a simple mother-tongue talk plus quiz | Quiz scores |

> **Ethics note:** validation conversations are voluntary and anonymous, and nobody is recorded without consent. We collect no personal data beyond first names used with permission.

### 6.11 Risks inherent to the problem (not the tech)
- **Retaliation or blame culture:** workers fear reporting. We use an **anonymous mode**, a no-blame charter, and aggregate-only analytics for individuals.
- **Management may ignore reports anyway:** the system creates **accountability trails** (acknowledgement SLAs, escalation to the plant head, audit logs).
- **"Safety theatre":** we focus on **controls applied** (holds, fixes), not report counts.
- **Surveillance misuse:** there is **no individual scoring of workers**, and we state it in the product charter (see [solution.md §12](solution.md)).

---

## 7. Final problem framing for the submission

- **Title:** *Suraksha Loop: every worker's voice is a safety sensor*
- **Theme:** Environment, Health & Safety (EHS) · **Aligned PS:** PS-17 (with PS-2, PS-15)
- **Problem (2 sentences):** Hazards on Indian MSME shop floors are seen first by migrant workers whose warnings, spoken in Hindi, Bhojpuri, Odia or Bengali, never become tracked action. The result is massive under-reporting of near-misses and preventable amputations and deaths (about 3 a day in registered factories; MP 4th nationally in 2024).
- **Who:** workers, supervisors and safety officers in 50–500-worker manufacturing MSMEs, starting with auto-component, forging, rubber and chemical units in the Malanpur–Banmore–Gwalior belt.
- **Measure of success:** near-miss reports per 100 workers ↑, time-to-control ↓, closure feedback 100%, toolbox-talk comprehension ≥ 80%.
