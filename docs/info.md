# INDUX 5.0-2026: everything about the challenge

> **Document owner:** Team Suraksha Loop · **Last researched:** 28 Sep 2026 · **Status:** living document, update after every organiser communication
>
> This file covers **everything we know about the hackathon**: what it is, who runs it, dates, rules, judging, people, sponsor, venue, history, contradictions, and what we must do next. Evidence tags used throughout:
> - **[V]** verified: we read it ourselves at the cited source on 28 Sep 2026
> - **[S]** secondary: a credible third-party source we could not confirm on a primary page
> - **[U]** unverified or inferred: our own reasoning, or a conflict between sources
>
> Companion docs: [research.md](research.md) (full research log and evidence register) · [problem.md](problem.md) (problem discovery and selection) · [solution.md](solution.md) (end-to-end solution) · [build.md](build.md) (build spec).

---

## 0. TL;DR: read this first

| # | Fact | Why it matters | Source |
|---|---|---|---|
| 1 | **Registration closes 1 Oct 2026.** | Three days from the research date. Miss it and we are out. | Devpost rules, VU page banner, brochure **[V]** |
| 2 | **Abstract + PPT + (optional) 3-min video are due "Till 2 October 2026"** per the official brochure. **Devpost** says submissions close **15 Oct 2026, 3:30 pm IST**. | The brochure date is almost certainly the real one, because the interviews on 8–9 Oct have to come after submissions. **Plan for 2 Oct.** | Brochure p.2 **[V]**; Devpost `/details/dates` **[V]** |
| 3 | Registration and PPT submission run through **Google Forms on the university site**, in addition to Devpost. | We must do **both**: the VU forms and Devpost. | https://vikrantuniversity.ac.in/indux_5.0_2026/ **[V]** |
| 4 | **Online interview with an industry + academic jury: 8–9 Oct 2026.** | We need a crisp 3-minute pitch, a clickable proof of concept or mock, and answers to about 20 likely questions (see [solution.md §19](solution.md)). | All sources **[V]** |
| 5 | **Selection + ₹2,500/team registration fee: 10–20 Oct 2026.** | Devpost says "zero participation fee". That is true for registration only; the fee is due after shortlisting. | Brochure p.2 **[V]** |
| 6 | **On-site 24-hour build: 2–3 Nov 2026 at Vikrant University, Gwalior (MP).** Physical presence for the full 24 h is mandatory. | Travel, stay and hardware planning. | All sources **[V]** |
| 7 | **Six evaluation criteria**, not one: *innovation & originality, real-world impact, technical depth of the AI/ML implementation, feasibility & scalability, prototype & demo quality, clarity of presentation.* | Devpost shows only "Innovation". The official GitHub README gives the full list. | README **[V]** |
| 8 | **"5.0" means Industry 5.0**, not the fifth edition. The only prior edition was **InduX 5.0 Hackathon 2025** (28–29 Oct 2025), themed on Industry 5.0 and smart manufacturing. | It has an **industry-heavy DNA**. The 2025 jury came from Mondelez, JK Tyre, Godrej, Crompton Greaves and SRF. | VU blog, QCFI **[V]** |
| 9 | **Presented by Arina AI + Vikrant University + GoKloud.** GoKloud (Pune) builds **Arina AI**, a "sovereign", on-prem, open-source-LLM platform. The GoKloud CEO sits on the advisory committee. | We will show a **sovereign / on-prem mode** with open models. | Brochure p.1 **[V]** |
| 10 | The listed Devpost **judge Bulbul Agrawal** is VU's **AI Cell Faculty Coordinator**, with research in **image processing, computer vision, deep learning** (they/them). | Our build includes a genuine CV component with honest metrics. | VU AI Cell page, Google Scholar **[V]** |
| 11 | There is an **official list of 23 problem statements** for 2026. | We anchor on **PS-17** (Occupational Safety Early-Warning) and draw in PS-2 and PS-15. | https://vikrantuniversity.ac.in/indux_5.0_2026/problem-statements/ **[V]** |
| 12 | Team size: **brochure says 3–4 members** (+1 optional faculty mentor); Devpost says 2–4. | **Form a team of 3–4** to be safe. | Brochure p.2, Devpost **[V]** |

### Immediate action checklist (owner → deadline)

- [ ] **Register the team on the VU Google Form** (https://forms.gle/ibHbVYqGicaL1Jhq7) → **before 1 Oct 2026, 23:59 IST at the latest; aim for 29 Sep**
- [ ] **Join the Devpost hackathon** (https://indux-5-0-2026.devpost.com/ → "Join hackathon") and create the project draft → 29 Sep
- [ ] **Email the organisers** with the questions in §17 (the draft email is in §17.2) → 29 Sep
- [ ] **Call the coordinator** if there is no email reply within 24 h: Prof. Aishwarya Singh, +91 79874 59533 (the official contact printed on the brochure) → 30 Sep
- [ ] Finalise the **abstract, PPT and 3-min video** (content ready in [solution.md §19](solution.md)) → **submit on the VU PPT form (https://forms.gle/TkkYDqTUdjRjtTHG7) and on Devpost by 2 Oct 2026**
- [ ] Book **3–5 validation conversations** with shop-floor workers, supervisors or EHS officers → before 7 Oct (quotes go into the interview deck)
- [ ] Build an **interview proof of concept** or clickable mock (see [build.md §2](build.md) for the rules on pre-built code) → 7 Oct
- [ ] Rehearse the interview Q&A twice → 7 Oct
- [ ] If selected: **pay ₹2,500**, confirm the slot, book travel to Gwalior → 10–20 Oct
- [ ] Accounts, keys, datasets, model weights, hardware kit (see [build.md §2](build.md)) → by 30 Oct

---

## 1. Official sources index

| Resource | URL | What it contains | Status |
|---|---|---|---|
| Devpost overview | https://indux-5-0-2026.devpost.com/ | About, themes, prizes, requirements, judge, criteria, sponsor | **[V]** |
| Devpost rules | https://indux-5-0-2026.devpost.com/rules | Eligibility, 5-stage timeline | **[V]** (short, no legal boilerplate) |
| Devpost schedule | https://indux-5-0-2026.devpost.com/details/dates | Submissions 22 Sep 16:00 IST → 15 Oct 15:30 IST; winners 3 Nov 16:30 IST | **[V]** |
| Devpost updates | https://indux-5-0-2026.devpost.com/updates | "Stay tuned…" (no updates as of 28 Sep) | **[V]** |
| Devpost discussions | https://indux-5-0-2026.devpost.com/forum_topics | "No topics have been created yet." | **[V]** |
| Devpost project gallery | https://indux-5-0-2026.devpost.com/project-gallery | Not published yet | **[V]** |
| Devpost participants | https://indux-5-0-2026.devpost.com/participants | Needs login; **45 participants** on 28 Sep | **[V]** |
| Devpost resources | https://indux-5-0-2026.devpost.com/resources | Empty | **[V]** |
| Devpost submission manager | https://devpost.com/submit-to/31477-indux-5-0-2026/manage/submissions | Where the Devpost submission is made (challenge id **31477**) | **[V]** |
| **VU official INDUX 2026 page** | https://vikrantuniversity.ac.in/indux_5.0_2026/ | Banner "Last Date of Registration is 1 October 2026", forms, brochure, advisory committee, contacts | **[V]** |
| **VU problem statements (23)** | https://vikrantuniversity.ac.in/indux_5.0_2026/problem-statements/ | Official 2026 problem briefs (full text in [research.md, Appendix A](research.md)) | **[V]** |
| **Official brochure (PDF, 2 pages)** | https://vikrantuniversity.ac.in/static/images/hackthon/Brochure_2.pdf | Dates (incl. **2 Oct** submission), fee **₹2,500**, team 3–4, prototype grants | **[V]** |
| **Official GitHub repo** | https://github.com/VikrantUniversity-gwalior/Indux-5.0-2026 | README with **full evaluation criteria and rules** (created 22 Sep 2026) | **[V]** |
| Team registration form | https://forms.gle/ibHbVYqGicaL1Jhq7 | Google sign-in required | **[V]** link |
| PPT submission form | https://forms.gle/TkkYDqTUdjRjtTHG7 | Google sign-in required | **[V]** link |
| Industry problem-statement submission form | https://forms.gle/2o4uQvjHqkfDjzRx6 | For companies (still open, so more PSs may appear) | **[V]** link |
| Junior Hackathon (school students) | https://vikrantuniversity.ac.in/indux_5.0_2026/jrhackathon/ | Same day, 2 Nov, Classes IX–XII | **[V]** |
| VU Facebook announcement | https://www.facebook.com/VUGWALIOR/posts/-indux-50-2026-ai-for-real-world-impact-vikrant-university-gwalior-is-all-set-fo/1505506528278201/ | Login wall | not readable |
| INDUX socials | https://www.linkedin.com/company/indux5-0/ · https://www.instagram.com/indux5.0/ · https://www.youtube.com/@induX-5.0 · https://x.com/induxhack | Mostly 2025 material | **[V]** handles |
| 2025 edition site | https://induxhack.com/ | 2025 schedule, FAQ, problem statements (Google Sheet), PPT template | **[V]** |
| Organiser email | indux5.0_hackathon@vikrantuniversity.ac.in | Official 2026 contact | **[V]** |

---

## 2. Event identity

| Field | Value |
|---|---|
| Official name | **INDUX 5.0-2026: AI FOR REAL-WORLD IMPACT** (brochure: "INDUX 5.0 HACKATHON 2026 – AI FOR REAL-WORLD IMPACT – An International-Level Hackathon") |
| Presenters | **Arina AI · Vikrant University, Gwalior · GoKloud** ("…PRESENTS") **[V]** brochure p.1 |
| Host | Vikrant University, Gwalior, Madhya Pradesh, India |
| Venue | Vikrant University campus, **Gwalior–Chitora Road, Banarpura, MP 474006** (Plus code 68V7+4VH). Map: https://maps.google.com/?q=68V7%2B4VH%2C%20Gwalior-Chitora%20Rd%2C%20Banarpura%2C%20Madhya%20Pradesh%20474006%2C%20India **[V]** |
| Format | Online funnel (registration → submission → interview → selection), then a **24-hour on-site hackathon** |
| Positioning | "International level 24-hour AI hackathon … bringing together student innovators, academia, and industry to build working AI solutions for problems that actually matter in manufacturing, healthcare and safety, security, sustainability, commerce, language, and space." **[V]** Devpost/README |
| Key promise | "**This isn't a slide-deck competition.** Teams clear a three-stage selection funnel, then get 24 hours on campus to turn a validated idea into a demonstrable prototype in front of an industry academia jury." **[V]** |
| Expected participation | "1000+ innovators" (claimed). Devpost showed **45** participants on 28 Sep. The 2025 edition had ~165 registered teams and 20–27 finalists **[V/S]** |
| Vision (brochure) | "To foster AI-driven innovation, strengthen industry-academia collaboration, and empower young innovators to develop intelligent solutions that address real-world challenges and create meaningful impact." **[V]** |
| Closing line (brochure) | "From idea to innovation — participate in INDUX 5.0–2026 and build solutions that create real-world impact." **[V]** |
| Devpost tags | Cybersecurity, Design, Robotic Process Automation (these look arbitrary) **[V]** |
| Devpost managed-by | "vikrant university, gwalior" · Public · ₹225,000 in cash **[V]** |

---

## 3. What "INDUX 5.0" means, and the 2025 edition

### 3.1 The name
- **"5.0" = Industry 5.0.** No INDUX 1.0–4.0 exists anywhere. Every search for them returned only 5.0 material, and Devpost's API returns exactly one INDUX hackathon **[V]** (see [research.md §2](research.md)).
- The 2025 tagline was **"Innovate for Industry, Build for Bharat"**, billed as "India's first National-level Hackathon dedicated to Industry 5.0 and Smart Manufacturing" **[V]** (https://qcfi.in/event/induxhack/ ; https://qcfi.in/indux-5-0-indias-first-national-level-hackathon-on-industry-5-0-and-smart-manufacturing-on-10th-12th-october-2025/).
- **Industry 5.0** (EU framing) = *human-centric, sustainable, resilient* industry, where technology augments workers instead of replacing them **[S]**. Our pitch vocabulary should reflect this.
- **2026 is the second edition.** The branding broadened from "Industry 5.0 & Smart Manufacturing" to "AI for Real-World Impact" with 14 themes, and the partners changed from QCFI + SenseLive to **Arina AI + GoKloud**.

### 3.2 The 2025 edition in detail (the best predictor of 2026)

| Aspect | 2025 fact | Source |
|---|---|---|
| Dates | Planned 10–12 Oct, then 11–12 Oct; **held 28–29 Oct 2025** (the schedule slipped twice) | QCFI slug, induxhack.com bundle, VU blog **[V]** |
| Co-organisers | Vikrant University ("Academic Host"), **QCFI – Quality Circle Forum of India** ("Industry Eco-system"), **SenseLive Technologies** ("Technical Partner", a Nagpur IIoT startup) | induxhack.com **[V]** |
| Advisory committee | Avinash Mishra (National President QCFI & MD, VU), D. K. Shrivastava (ED, QCFI), Rituraj Mehta (Group Safety Head, **Adani Group**), Dr. Richa Verma (Registrar, VU), Abhijeet Bhoyar (CEO, SenseLive) | induxhack.com **[V]** |
| Themes | Industrial Digitalization, Industry IoT, Robotics, AI & ML, Industry Automation, **EHS**, Digital Twin, Image Processing, Sustainability | QCFI, induxhack.com **[V]** |
| Problem statements | **103** real industry statements in a public Google Sheet, from Jindal Stainless, **SRF Malanpur**, APAR, a soap maker, a glass/lighting maker (probably Surya Roshni **[U]**), a pharma vial plant, a zinc smelter, a cement plant, dairy robotics and others | induxhack.com Google Sheet **[V]**, full dump in [research.md](research.md) |
| Safety-related PSs (relevant to us) | **PS-30** Behaviour-Based Safety; **PS-33** AI safety training for drivers & casual workmen; **PS-46** Unskilled manpower; **PS-23** Digital rule repository (tacit rules); **PS-24** Contract labour history; **PS-83** Worker safety in high dust; **PS-93** PPE compliance by CV; **PS-4** (Jindal) PdM + energy + **EHS** platform | Google Sheet **[V]** |
| Format | Stage 1: abstract + PPT + 3-min video → Stage 2: **15-minute jury interview** ("clarity, feasibility, and readiness"), 2 rounds → Stage 3: 24 h on-site "Demo Day & Prototype" | induxhack.com **[V]** |
| Fee | **₹2,500 per team** (the same as 2026) | 2025 FAQ **[V]** |
| Prizes | ₹1,00,000 / ₹75,000 / ₹50,000 + "Prototype Development Grants (₹25,000–₹50,000)", internships, incubation. Every Stage 3 finalist got a ₹5,000 **Chancellor's Prize**. Totals disagree between sources (₹3L vs "₹5L+" vs 6 prize-winning teams) | FAQ, VU blog, LinkedIn **[V]** |
| IP policy | "The student team retains IP rights of their idea; if adopted by industry, a mutual agreement will be signed post-hackathon." **But** some company PS sheets said IP stays with the company (e.g. Jindal Stainless). Undisclosed use of "commercial pre-built solutions" meant disqualification. | FAQ, Google Sheet **[V]** |
| Participation | "Over 400 students from 40+ institutions", "The jury rated the 52 projects" (VU blog). "165 student teams", "27 finalist teams", "250+ colleges" (LinkedIn). "Top 20 teams" (RBU newsletter). Institutions included IIT Mandi, ABV-IIITM, MITS Gwalior, Ramdeobaba Univ. Nagpur, RN Patel Inst. (Bardoli), P P Savani Univ., ISPM BSIOTR Pune, Sanjeevani Univ. | VU blog, LinkedIn, RBU **[V]** |
| **Jury** | **Mondelez International, JK Tyre & Industries, Godrej Group, Crompton Greaves, SRF Limited, Simplifying Skills, ABV-IIITM Gwalior**. Criteria: "innovation value, technical feasibility, **market relevance**, and originality, along with presentation quality" | VU blog **[V]** |
| Guests | Chief guest **Dr. Rajesh Chhabra** (possibly Mondelez India, Malanpur **[U]**); valedictory **Dr. Ashok K. Mittal**, retired professor, IIT Kanpur | VU blog **[V]** |
| **Winners** | **1st (₹1L):** InnoCrew, Ampere Squad · **2nd (₹75k):** Codesoft, The NextGen Automators · **3rd (₹50k):** EcoData Coders, ChaturGo | VU blog **[V]** |
| Winner institutions | Gold: RNGPIT Bardoli + **Vikrant University**; Silver: SPU College Falna + ABV-IIITM; Bronze: Ramdeobaba Univ. Nagpur + **Vikrant University** | LinkedIn (Avinash Mishra) **[V]** |
| One known winning project | **"ChaturGo DairyBot"** (RBU Nagpur, B.Tech 2nd-year Robotics & AI): a robot for automated cow milking, feeding and dairy-farm cleaning. Won ₹50,000 as 2nd runner-up "after an extremely challenging two stage elimination" | RBU newsletter PDF **[V]** |
| Pattern | **Two prize-winners per tier** (possibly hardware and software tracks **[U]**). **Host university teams took 2 of 6 podium spots**, so expect strong local competition. | Inference **[U]** |

### 3.3 The 2025 on-site schedule (expect a similar 2026 shape)

| Day 1 | | Day 2 | |
|---|---|---|---|
| 09:00 | Registration | 07:00 | Breakfast |
| 10:00 | Opening ceremony | 08:00 | Hacking Session 4 + **mentor reviews** |
| 11:00 | Problem-statement briefing | 14:00 | **Submission deadline**, demo prep |
| 13:00 | Hacking Session 1 | 15:00 | **Presentations + jury Q&A** |
| 19:00 | Dinner | 18:00 | Jury deliberation |
| 20:00 | Session 2 | 19:00 | Closing & awards |
| 00:00 | Fun break | | |
| 01:00 | Session 3 | | |

Source: induxhack.com bundle **[V]**. Implication: the real coding window is roughly **13:00 Day 1 → 14:00 Day 2 (~25 h)**, with **mentor reviews on the morning of Day 2**. Devpost says winners are announced **3 Nov 16:30 IST**.

---

## 4. 2026 timeline, with every source compared

| Stage | What | Devpost rules | Devpost schedule | VU page | Brochure | README | **Our working date** |
|---|---|---|---|---|---|---|---|
| 1 | Online registration (free) | 14 Sep – 1 Oct | — | 14 Sep – 1 Oct (banner: "Last Date of Registration is 1 October 2026") | 14 Sep – 1 Oct | 14 Sep – 1 Oct | **Register by 29 Sep** |
| 2 | Abstract + PPT + optional 3-min video | "Till October 2026" | **Submissions 22 Sep 16:00 IST → 15 Oct 15:30 IST** | "Till October 2026" (hidden HTML `data-event-date="2026-10-01"`) | **"Till 2 October 2026"** | "Till October 2026" | **Submit by 2 Oct, on the VU form AND Devpost** |
| 3 | Online interview & screening (industry + academic jury) | 8–9 Oct | — | 8–9 Oct | 8–9 Oct | 8–9 Oct | **8–9 Oct** |
| 4 | Selection + registration fee payment | 10–20 Oct | — | 10–20 Oct | 10–20 Oct (**₹2,500/team**) | 10–20 Oct | Pay promptly once selected |
| 5 | On-site 24-hour hackathon | 2–3 Nov | Winners announced **3 Nov 16:30 IST** | 2–3 Nov (countdown to 2026-11-02T00:00+05:30) | 2–3 Nov | 2–3 Nov | **Arrive 1 Nov** |

**Reading:** Devpost's "15 Oct" makes no sense as a Stage 2 deadline, because it falls after the 8–9 Oct interviews. It is probably a default Devpost window, and it is where the Devpost submission record lives. The overview line "October 15 at 6:00am EDT to deadline" equals 15:30 IST on the same day, a display artefact. **Act on the earliest date (2 Oct), but also submit on Devpost.** The organisers reserve the right to change the schedule, and the 2025 schedule slipped twice, so re-check the VU page and Devpost updates daily.

---

## 5. Eligibility and team

| Rule | Devpost overview | Devpost rules | Brochure | 2025 precedent | **Our reading** |
|---|---|---|---|---|---|
| Who | "Above legal age of majority in country of residence"; "**College students only**"; all countries except standard exceptions | "Open to **students and young innovators** from institutions in **India and abroad**" | "B.Tech/B.E./BCA/M.Tech/MCA, Diploma, and other technical programs (all disciplines)"; "Interdisciplinary teams encouraged" | Same, plus Ph.D. scholars | Enrolled students of any technical programme; international students allowed but must attend in person |
| Team size | "**Team required: 2 to 4 members**" | "Team based participation" | "**Team size: 3 to 4 members** (with 1 faculty mentor-optional but encouraged)" | "up to 3–4 members", one mentor, one team per student | **Form 3–4 members; add a faculty mentor if possible** |
| Presence | — | "Selected teams must be **physically present** at Vikrant University, Gwalior on 2 - 3 November 2026" | Venue: VU Gwalior | Physical mode | Whole team on campus for the full 24 h (README: "Teams must be present on campus for the entire 24 hour round") |
| Pre-requisite | — | "Participants must complete online registration **before 1 October 2026** and clear the submission and interview stages to qualify for the on-site round" | — | — | Hard gate |

**If any teammate is outside India [U]:** the rules explicitly allow institutions abroad, but attendance is physical. Check visa requirements early (Indian e-Visa categories and processing times), ask the organisers for an **official invitation letter**, and budget for travel. Gwalior Airport (GWL) is about 15 km from campus and Gwalior Junction railway station about 8 km (2025 FAQ **[V]**). Delhi (IGI) → Gwalior is about 3–4 h by fast train (Gatimaan/Vande Bharat/Shatabdi **[U]**).

---

## 6. Prizes, rewards and fees

| Item | Detail | Source |
|---|---|---|
| Total prize pool | **₹2,25,000 in cash** | Devpost, brochure **[V]** |
| Winner | **₹1,00,000** | **[V]** |
| 1st Runner-up | **₹75,000** | **[V]** |
| 2nd Runner-up | **₹50,000** | **[V]** |
| **Prototype Development Grants** | "**up to ₹50,000**" | Brochure p.1 **[V]** |
| Other | "Internship Opportunities & Startup Incubation"; "Certificates & Media Exposure for all Participants"; "mentorship from industry and academic experts, pan India visibility … opportunities to take the idea forward with partner organisations"; "Startup Pathways – Connect with incubators & industry scout[s]" | Brochure, Devpost **[V]** |
| Registration fee | **₹0** to register; **₹2,500 per team**, "Payable after shortlisting by the Online Interview Committee" | Brochure p.2 **[V]** (Devpost: "Zero participation fee to register") |
| Devpost achievements | Devpost badges for submitting | Devpost **[V]** |
| Travel / accommodation | **Not mentioned anywhere** for 2025 or 2026 | Ask the organisers **[U]** |
| Food / Wi-Fi | 2025 provided Wi-Fi, food, swag (T-shirt, stickers, ID kit) and certificates | 2025 FAQ **[V]** |

---

## 7. The 14 themes ("Pick One")

Exactly as listed on Devpost, VU and the brochure **[V]**. The README rule says: "Each team selects **one** theme from the 14 focus areas".

| # | Theme | Official 2026 PSs that map to it |
|---|---|---|
| 1 | AI & Generative AI | PS-1 Agentic BPA, **PS-2 Multimodal GenAI Assistant for Industrial SOPs, Manuals & Expert Knowledge** |
| 2 | Smart Manufacturing | PS-3 Predictive Maintenance & Failure Diagnosis |
| 3 | Industrial IoT (IIoT) | PS-4 Edge-AI Multi-Sensor Quality Inspection, PS-5 IIoT Energy & Machine Utilization |
| 4 | Robotics & Intelligent Automation | PS-6 Vision-Guided Pick-and-Place, PS-7 Indoor Delivery Robot, PS-23 Indoor Mobile Robot (SLAM) |
| 5 | Cybersecurity & Digital Trust | PS-8 OT Cyber Threat Detection, PS-9 Deepfake/Voice-Clone Detection |
| 6 | Digital Twin & Simulation | PS-10 Production-Line Digital Twin, PS-11 Infrastructure Emergency Digital Twin |
| 7 | Computer Vision & Image Processing | PS-12 Surface & Product Defect Inspection |
| 8 | Retail & Intelligent Commerce | PS-13 Checkout-Free Retail, PS-14 Demand Forecasting & Pricing for Local Retailers |
| 9 | Multilingual AI & Language Technologies | **PS-15 Multilingual AI Information, Assistance & Service Automation**, PS-16 Regional-Language Farmer Advisory Voice Assistant |
| 10 | **Environment, Health & Safety (EHS)** | **PS-17 AI Heat-Stress, Fatigue & Occupational Safety Early-Warning System** |
| 11 | Sustainability & Green Technologies | PS-18 Water Quality Monitoring & Pollution Prediction |
| 12 | Data Analytics & Predictive Intelligence | PS-19 Geospatial Risk Mapping & Early Warning for Natural Disasters |
| 13 | Space Technology & Exploration | PS-20 Satellite Image Change Detection |
| 14 | Defence, Security & Strategic Technologies | (no dedicated PS) |
| — | *(not among the 14)* | PS-21 Remote Healthcare Monitoring ("Healthcare AI & Digital Health"), PS-22 Intelligent Drone ("Drone Technology") |

**Our theme: Environment, Health & Safety (EHS). Anchor PS: PS-17**, with PS-2 (SOP knowledge) and PS-15 (multilingual) absorbed as sub-capabilities. Full rationale in [problem.md](problem.md).

---

## 8. The 23 official 2026 problem statements (summary)

Full verbatim text is in [research.md Appendix A](research.md). **[V]** from https://vikrantuniversity.ac.in/indux_5.0_2026/problem-statements/

| PS | Title | Stated tech stack | Hardware? |
|---|---|---|---|
| 1 | Agentic AI for Autonomous Business Process Automation | Software + AI/ML + Cloud + Data Analytics | No |
| 2 | Multimodal GenAI Assistant for Industrial SOPs, Manuals & Expert Knowledge | Software + AI/ML + **RAG** + Cloud + Data Analytics | No |
| 3 | AI-Powered Predictive Maintenance & Failure Diagnosis for Industrial Assets | Software + Hardware + AI/ML + IoT + Cloud + DA | Yes |
| 4 | Edge-AI Multi-Sensor Quality Inspection for Real-Time Manufacturing | + Edge + CV | Yes |
| 5 | AI-Driven Smart IIoT Energy & Machine Utilization Optimization Platform | + IoT | Yes |
| 6 | AI Vision-Guided Robotic Pick-and-Place & Sorting System | + CV + Robotics | Yes |
| 7 | AI-Powered Autonomous Indoor Delivery Robot with Intelligent Navigation | + Robotics + Edge | Yes |
| 8 | AI-Based OT Cyber Threat Detection & Autonomous Incident Response | + Cybersecurity + Edge + Cloud | Optional edge |
| 9 | AI Deepfake, Voice Clone & Synthetic Media Detection Platform | + CV + NLP | No |
| 10 | AI-Enabled Digital Twin for Production-Line Simulation & What-If Analysis | + Digital Twin + Simulation | No |
| 11 | AI-Enabled Digital Twin for Smart Infrastructure Emergency Simulation | + GIS + Simulation | No |
| 12 | AI & Computer-Vision Based Surface & Product Defect Inspection | + DL + CV + Edge | Camera |
| 13 | AI-Powered Checkout-Free Retail Billing & Product Recognition | + CV + Retail | Yes |
| 14 | AI Demand Forecasting & Dynamic Pricing Advisor for Local Retailers | + DA + Retail | No |
| 15 | Multilingual AI Information, Assistance & Service Automation Platform | + **NLP + Multilingual AI** + Mobile | No |
| 16 | Regional-Language AI Farmer Advisory & Voice Assistant | + NLP + Multilingual + IoT + Mobile | Optional IoT |
| 17 | **AI Heat-Stress, Fatigue & Occupational Safety Early-Warning System** | Software + Hardware + AI/ML + IoT + **Wearable** + DA | Wearables (can be simulated) |
| 18 | AI-Based Water Quality Monitoring & Pollution Prediction | + IoT + Cloud | Yes |
| 19 | AI Geospatial Risk Mapping & Early Warning for Natural Disasters | + GIS + Geospatial | No |
| 20 | AI Satellite Image Change Detection for Climate & Land Monitoring | + CV + Satellite + Geospatial | No |
| 21 | AI-Powered Remote Healthcare Monitoring & Early Risk Detection Platform | + IoT + Wearables (simulated OK) | Optional |
| 22 | AI-Powered Intelligent Drone for Agri Monitoring, Disaster Response & Surveillance | Drone + CV + Segmentation + GIS | Simulated OK |
| 23 | Autonomous Indoor Mobile Robot for Mapping, Navigation & Obstacle Detection | Robotics + SLAM (simulation OK) | Simulation OK |

**PS-17 verbatim brief [V]:** "The Occupational Safety Early-Warning System protects workers who operate in hot, demanding, or hazardous environments. Wearable devices and IoT sensors track environmental conditions such as temperature and humidity along with worker activity and physiological signals, and AI models estimate individual heat-stress and fatigue risk levels. Timely preventive alerts are sent to the worker and the safety supervisor so that rest, hydration, or task rotation can be arranged before any incident occurs. A dashboard provides site-wide visibility of workforce safety status, high-risk zones, and alert history for compliance reporting. Overall, the system reduces heat-related incidents and downtime, strengthens workplace safety culture, and can be scaled across different industrial and outdoor work settings."

**Observations [U]:**
1. Unlike 2025, **no 2026 PS names a company**. They read like organiser-written briefs, and the "Submit Problem Statements" call to industry is still open, so industry PSs may be added later.
2. Many briefs mention **Cloud Computing and Data Analytics**, which matches GoKloud (cloud/DevOps) and Arina Grid (documents and data).
3. The Devpost/rules text "Submit your problem statement, proposed AI solution…" suggests teams **may frame their own problem within a theme**. We will map explicitly to PS-17 anyway, to be safe.
4. Crowding: PS-2, PS-15, PS-16 and PS-17 will attract many look-alike entries (SOP chatbots, generic multilingual bots, farmer bots, wearable heat dashboards). Differentiation strategy is in [problem.md §5](problem.md).

---

## 9. What we must submit (Stage 2)

| Artefact | Official wording | Our plan | Where |
|---|---|---|---|
| **Abstract** | "Abstract – problem statement, proposed AI solution, intended impact" **[V]** | ~250 words, 5-paragraph structure (final text in [solution.md §19.1](solution.md)) | VU PPT form (probably has an abstract field **[U]**) + Devpost "About the project" |
| **Presentation (PPT)** | "Presentation (PPT) – approach, tech stack, feasibility, novelty" **[V]** | 12 slides + appendix (content in [solution.md §19.2](solution.md)); export PDF + PPTX | VU PPT form + Devpost upload |
| **3-minute video pitch** | "3-Minute Video Pitch — team introduction and solution walkthrough (**optional**)" **[V]** | **Do it anyway**: it is our best differentiation signal and Devpost judges weight video heavily. Script in [solution.md §19.3](solution.md) | YouTube unlisted link on the VU form + Devpost |
| PPT template | 2025 had an official template: https://induxhack.com/Presentation-Format(1).pptx (~92 KB, last modified 11 Oct 2025) **[V]** (HEAD only; not downloaded) | Download it and check whether the 2026 form references a template; if not, use our own 16:9 deck | — |

**Devpost submission fields to prepare [U]** (standard Devpost form): project name, elevator pitch (≤200 chars), "About the project" (markdown: inspiration, what it does, how we built it, challenges, accomplishments, what we learned, what's next), "Built with" tags, "Try it out" links, image gallery (≥3 screenshots, 3:2), video URL (YouTube/Vimeo), team member invitations, and any custom questions (e.g., theme selection). Everything is prepared in [solution.md §19](solution.md).

---

## 10. Judging and evaluation

### 10.1 What each source says

| Source | Criteria |
|---|---|
| Devpost | **Innovation** (single criterion, no description) **[V]** |
| **Official README** | "Submissions and prototypes are assessed by an industry academia jury on **innovation and originality, real world impact, technical depth of the AI/ML implementation, feasibility and scalability, prototype and demo quality, and clarity of presentation**." **[V]** |
| 2025 jury (precedent) | "innovation value, technical feasibility, **market relevance**, and originality, along with presentation quality" **[V]** |
| 2025 interview | "15-minute jury interview to test **clarity, feasibility, and readiness**" **[V]** |
| 2025 individual PS rubrics | e.g. PS-1 "Innovation 25%", PS-16 "Innovation & Creativity – 25%" **[V]** |

### 10.2 Our working rubric (weights are our estimate) **[U]**

| Criterion | Weight | What a 9/10 looks like for us |
|---|---|---|
| Innovation & originality | 25 | A **closed loop** from a worker's own voice, in their language, to a machine permit hold, SOP fix and toolbox talk back in their language. **Calibrated AI judgments** (Jev) decide what gets automated versus sent to a human. Not "a chatbot for SOPs". |
| Real-world impact | 20 | Named persona, sourced numbers (≈3 factory deaths/day; 26× under-reporting; 93% of 2025 injuries on unguarded power presses; 84% reported and were ignored), validation quotes, KPIs and ₹ ROI |
| Technical depth of AI/ML | 20 | A multi-stage pipeline: Indic ASR → LLM structured extraction → **Jev verification and triage** → hybrid RAG with reranking and citation checks → Indic TTS → **on-device CV (PPE/guard check)**, with an **evaluation harness** (WER, field F1, severity MAE, mAP, latency, ₹/report) |
| Feasibility & scalability | 15 | Works on a ₹8–10k Android phone, offline-first PWA, cost ≈ ₹4 per report, sovereign on-prem mode, DPDP-aware data flow, pilot plan |
| Prototype & demo quality | 10 | 90-second golden path live, offline demo, tier badges, recorded backup |
| Clarity of presentation | 10 | One-sentence problem, one-sentence solution, one architecture picture, every builder answers questions on their own component |

### 10.3 Who will judge (our expectation) **[U]**
- **Online interview panel:** "industry + academia" (brochure). Likely VU faculty (the AI Cell, including Bulbul Agrawal), GoKloud/Arina people, and local industry.
- **On-site jury:** based on 2025, plant, EHS, quality and operations leaders from **Malanpur/Banmore** manufacturers (Mondelez, JK Tyre, Godrej, Crompton, SRF, Surya Roshni, Jamna Auto…), plus academics (ABV-IIITM, MITS, IIT Kanpur alumni).
- **What they will reward:** things that look deployable on their shop floor next Monday; shop-floor vocabulary (near-miss, LOTO, permit-to-work, PPE, Kaizen, 5S, PDCA, OEE, MTTR, CAPA); honesty about limits; working demos.

---

## 11. Rules (complete list of what is written anywhere)

From the README **[V]**:
1. "Each team selects one theme from the 14 focus areas"
2. "**All code and assets built during the 24 hour on-site round must be original work by the team; open source libraries and APIs are permitted with attribution**"
3. "Teams must be present on campus for the entire 24 hour round"
4. "The jury's decision is final and binding"
5. "Organisers reserve the right to modify the schedule or format; registered teams will be informed of any changes."

From Devpost rules **[V]**: registration before 1 Oct; clear the submission and interview stages; physical presence 2–3 Nov.

From 2025 (precedent, may carry over) **[V]**: disqualification for false information, missed deadlines or mandatory sessions, Code of Conduct violations, plagiarism; external tools, datasets and APIs allowed if open-source or properly licensed; **undisclosed use of commercial pre-built solutions = disqualification**; students keep IP unless a PS says otherwise.

**Interpretation for us [U]:**
- **Pre-built code:** the rule covers work "built during the 24 hour on-site round" but is silent on pre-event preparation. The safe path: prepare **designs, specs (this repo's docs), datasets, accounts, prompts, evaluation sets and model downloads** before the event. Treat any pre-event code as a **throwaway interview PoC** unless the organisers confirm in writing that a disclosed pre-built scaffold is acceptable. See [build.md §2](build.md).
- **Attribution:** keep an `ATTRIBUTION.md` listing every library, model, dataset and API with its licence (planned in [build.md](build.md)).
- **Commercial APIs** (Claude, Sarvam, TypeSafe Jev) are "APIs", so they are permitted with attribution. Declare them.

---

## 12. People

### 12.1 Advisory committee 2026 (brochure) **[V]**
| Name | Role |
|---|---|
| Prof. (Dr.) Atul Kumar | Vice-Chancellor, Vikrant University |
| **Mr. Manav Prasad** | **CEO and Co-Founder, GoKloud** |
| Dr. Richa Verma | Registrar, Vikrant University |
| Dr. Anand Kumar Singh | Dean Academics, Vikrant University (a VU AI Cell report names "Dr. Anand Singh Bisen, Dean Academics"; possibly different people **[U]**) |

### 12.2 Official contacts (as printed for the hackathon) **[V]**
| Name | Role | Phone |
|---|---|---|
| **Prof. Aishwarya Singh** | Co-ordinator, INDUX 5.0 2026 | +91 79874 59533 |
| Prof. Narrotam Dutt Upadhyay | Asst. Prof. (committed the official GitHub README) | +91 99070 59984 |
| Prof. Madhwan Upadhyay | Asst. Prof.; AI Cell Faculty Coordinator | +91 96300 36698 |
| Prof. Anand Kumar Singh | Dean (VU page) | +91 77730 04155 |
| Email | indux5.0_hackathon@vikrantuniversity.ac.in | — |

### 12.3 The listed judge: Bulbul Agrawal (they/them)
- **Role:** Faculty Coordinator, **AI Cell**, Computer Science & Engineering, School of Engineering & Technology, VU **[V]** (https://vikrantuniversity.ac.in/ai-cell/). Program coordinator for the **Arina Prism Sense pilot** (24 Jun 2026) with GoKloud **[V]**.
- **Research (Google Scholar, JV5kovoAAAAJ) [V]:** image processing, deep learning, AI, neural networks. Papers on CNN age and gender estimation (2019), PCA/ICA facial feature analysis (2019), **comparison of training algorithms for facial expression recognition** (2025), ML for student mental well-being (2023), a review of image enhancement techniques, and a **2026 design registration: "AI-Based Image Encryption and Decryption Device"**. Scholar affiliation still lists **MITS Gwalior** (they probably moved **[U]**).
- **How we tailor for them [U]:**
  - A **real CV component**: an on-device PPE/guard-state detector with honest mAP/precision/recall, a confusion matrix, and a comparison of two backbones or training settings.
  - **Image privacy**: faces blurred on-device, no biometrics stored, encryption at rest. This connects to their encryption work.
  - **Responsible-AI language**: the AI Cell mission stresses "ethical, responsible and sustainable use of AI".
  - A **reproducible method**: eval set, metrics, and the confidence/threshold policy.

### 12.4 Vikrant University: context
- **Status:** state private university under MP Private University (Establishment and Operation) Act, 2022 (Act No. 25 of 2022). Formerly VITM, part of the Vikrant Group of Institutions (claims 18–20 years). 50+ acre campus on Chitora Road. UGC 2(f) listed **[V]** (https://vikrantuniversity.ac.in/ ; https://en.wikipedia.org/wiki/Vikrant_University).
- **Leadership:** Chancellor Rakesh Singh Rathore; VC Prof. (Dr.) Atul Kumar; Registrar Dr. Richa Verma; MD Avinash Mishra (also National President, QCFI) **[V/U]**.
- **12 schools**, including Engineering & Technology, Computer Application, Management, Pharmacy, Agriculture **[V]**.
- **AI Cell (formed 27 Feb 2026) [V]:** chair Dr. Anand Pandey; mentor Dr. Sandeep K Tiwari; faculty coordinators **Prof. Bulbul Agrawal** and Prof. Madhwan Upadhyay; student president Vinay Pratap Singh. Activities: prompt-engineering workshop, **Gwalior AI Summit 2026 at ABV-IIITM** (27–28 Mar), Google Gemini training, NeuroSpark AI quiz, "Web Development using AI" masterclass, **Arina Prism Sense faculty onboarding (MoU with GoKloud)**.
- **Quality culture:** VU hosted the **33rd QCFI Gwalior Chapter Convention (2025)**, and its MD is QCFI National President. **Quality Circles, Kaizen and frontline problem-solving** are part of the host's identity **[V]**.

---

## 13. Sponsor: GoKloud / Arina AI

| Field | Detail | Source |
|---|---|---|
| Company | **GoKloud Software Solutions Pvt Ltd**, Pune (Creaticity Mall, Yerawada) and Goa offices; "Conceptualized in 2020"; ~36 staff; bootstrapped **[S]** | https://gokloud.io/ **[V]**, Inc42 **[S]** |
| Services | IT consulting, product engineering, cloud-native builds, **DevSecOps**, cloud migration, multi-cloud, MVP development | **[V]** |
| Product | **Arina AI** (https://arina.ai/): "Sovereign" enterprise AI on **open-source LLMs/VLMs**, **on-prem / air-gapped**, NVIDIA H100/A100 orchestration, fixed licence with no per-token billing, "over 70% cost efficiency compared to standard SaaS API-based services" | **[V]** |
| Arina product lines | **Prism Sense** (education: professor/student co-pilots, multilingual avatar lectures, local-language support "within one week"); **Care Sense** (healthcare: ambient scribe, Doc2FHIR); **Arina Grid** ("Sovereign Enterprise AI for Documents, Data, & Decisions": document OCR/layout, conversational data intelligence, NL→SQL) | **[V]** |
| Relationship to VU | **MoU** "for establishing an AI-Driven Academic Ecosystem at Vikrant University"; Prism Sense pilot, 24 Jun 2026 | VU AI Cell report 16 **[V]** |
| People | **Manav Prasad**, CEO & Co-Founder (advisory committee); Devesh Chanchlani (Arina AI, resource person at the VU pilot) | **[V]** |

**How we align (without claiming any partnership) [U]:**
1. **Sovereign mode:** every AI stage has an open-source, self-hostable fallback (IndicConformer ASR, IndicTrans2 MT, Indic Parler-TTS, an open LLM via Ollama). The pitch line: *"The factory's voice data never has to leave the factory."*
2. **Cloud-native polish:** Docker Compose, CI, IaC-ready, secrets hygiene, a portable deploy diagram (GoKloud's core business).
3. **Document intelligence:** SOP ingestion, grounded answers with citations and hallucination controls (Arina Grid messaging).
4. **Multilingual:** local-language delivery (Prism Sense messaging).
5. The phrase "**could run on Arina Grid**" as a deployment option. **Never claim** an integration we have not built.

---

## 14. Venue, logistics and local context

### 14.1 Getting there and being there
- **Campus:** Gwalior–Chitora Road (MP State Highway), Banarpura, Gwalior 474006 **[V]**. City office: Plot 2850, Airport Road, Gwalior 474005 **[V]**.
- **Airport:** Gwalior (GWL), ~15 km. **Rail:** Gwalior Junction, ~8 km. Free parking **[V]** (2025 FAQ).
- **Weather, early November:** mild days (~25–30 °C), cool nights (~12–15 °C) **[U]**. Bring a sweater for AC halls at night.
- **Busy campus:** the **Junior Hackathon** (6-hour, Classes IX–XII) runs on **2 Nov** too **[V]**.
- **Connectivity [U]:** expect overloaded venue Wi-Fi. Carry **two phones on different carriers** (Jio + Airtel/Vi) with large data packs for hotspots, and test signal in the hall at T−1 h.
- **Power [U]:** bring 2 extension boards (Indian plug types C/D/M), power banks and all chargers.

### 14.2 Why Gwalior's industrial context matters for our pitch
- **Malanpur industrial area (Bhind, ~10–30 km):** Mondelez (Cadbury), Godrej Consumer, Jamna Auto, C.T. Cotton Yarn **[V]**; also Crompton Greaves, **SRF (Tyre Cord Fabric)**, Surya Roshni, Malanpur Steel **[S]**.
- **Banmore industrial area (Morena):** **JK Tyre**, the Gwalior dairy cooperative, pipes, steel, foam; MSMEs in edible oil, **stone crafting**, transformer components **[S]**.
- **Gwalior district:** 8 industrial areas (Birla Nagar, Maharajpura…), **Railway Spring Karkhana (Sithouli)**, a transformers cluster, and **~200 sandstone-processing units** (silicosis risk) **[V/S]** (DC-MSME district profile).
- **Madhya Pradesh ranked 4th in India in factory-accident deaths in 2024 (70 deaths)** (NCRB ADSI via Dataful **[S]**). **Harda firecracker factory blast, Feb 2024: 11 dead, 174 injured**, with workers saying there was no fire extinguisher **[S]**. **Dewas firecracker blast, May 2026: 2 dead, 15 injured** **[S]**.
- **Heat:** MP issued heatwave alerts for 22 districts **including Gwalior and Morena** (25 Apr 2026) **[S]**. Gwalior-Chambal summers exceed 45 °C.
- **MP policy hooks (for the scalability slide):** MP Industrial Promotion Policy 2025, MP MSME Promotion Scheme 2025, MP Startup Policy 2025 **[V titles]**.

---

## 15. Competitive landscape at INDUX (what we are up against) **[U]**

1. **Host university teams**, who won 2 of 6 podium spots in 2025 and know the jury.
2. **Repeat hackathon teams** from Nagpur (RBU), Gujarat (RNGPIT, P P Savani), Rajasthan (SPU Falna), Gwalior (ABV-IIITM, MITS) and Pune.
3. Hardware-heavy robotics teams (a 2025 winner was a dairy robot). Judges like physical demos.
4. **Crowded briefs:** SOP RAG chatbots (PS-2), generic multilingual bots (PS-15), farmer bots (PS-16), wearable heat dashboards (PS-17), YOLO defect detection (PS-12), deepfake detectors (PS-9).

**Our edge:** we sit on PS-17 but deliver a **human-centric closed loop** that no crowded brief will produce, with visible **technical depth** (calibrated triage, evaluation harness, on-device CV), **sovereign deployability**, and a **local, visceral story** (MP 4th in factory deaths; migrant workers from Bihar, UP and MP).

---

## 16. Inconsistencies and red flags register

| # | Issue | Details | Our response |
|---|---|---|---|
| 1 | Submission deadline | Brochure "Till 2 Oct" vs Devpost "15 Oct 15:30 IST" vs "Till October 2026" | Submit by **2 Oct** everywhere |
| 2 | Registration | Must be done "before 1 October 2026" although Devpost submissions stay open | Register on the VU form by 29 Sep |
| 3 | Fee | "Zero participation fee" (Devpost/VU) vs **₹2,500/team** after shortlisting (brochure) | Budget ₹2,500 |
| 4 | Team size | 2–4 (Devpost) vs 3–4 (brochure) | 3–4 |
| 5 | Eligibility | "College students only" vs "students and young innovators" | Keep everyone enrolled; carry student IDs |
| 6 | Scale | "International", "1000+ innovators" vs 45 on Devpost; 2025 ≈ 165 teams / 20–27 finalists | Expect ~20–30 finalist teams |
| 7 | Industry PSs | "Real problem statements contributed by industry partners" vs no attribution in the 2026 list | Bring our own validated framing, mapped to PS-17 |
| 8 | Themes vs PSs | PS-21 (Healthcare) and PS-22 (Drones) are outside the 14 themes; no Defence PS | Not our concern (EHS) |
| 9 | Judging | Devpost: one criterion, one judge; README: six criteria, industry + academia jury | Optimise for all six |
| 10 | On-site dates | Consistent everywhere: **2–3 Nov 2026** | ✔ |
| 11 | Schedule slippage | 2025 moved twice | Re-check sources daily |
| 12 | 2025 prize totals | ₹3L vs ₹5L+ vs 6 winners | Irrelevant; note only |
| 13 | Dean's name | Anand Kumar Singh vs Anand Singh Bisen | Use titles in emails |
| 14 | Sponsor naming | GoKloud / Gokloud / "GoCloud" (typo) | Use **GoKloud** |
| 15 | Logistics | No info on accommodation or travel | Ask (§17) |

---

## 17. Open questions for the organisers

### 17.1 Questions
1. Is the **Stage 2 deadline 2 Oct 2026** (brochure) or **15 Oct 2026** (Devpost)? Which submission channel is authoritative: the VU PPT Google Form, Devpost, or both?
2. Must we pick one of the **23 listed problem statements**, or may we submit our own problem framed within a theme? (We map to **PS-17** with elements of PS-2 and PS-15.)
3. Is a **pre-event proof of concept** allowed for the online interview? And may we bring **pre-prepared datasets, trained model weights and design assets** to the on-site round, provided all on-site code is written during the 24 hours and everything is disclosed?
4. **Team size:** is a team of 3 or 4 (brochure) required, or are 2-member teams allowed (Devpost)?
5. **Interview format:** duration, platform (Meet/Zoom/Teams), whether a live demo is expected, and how we will be scheduled.
6. **Registration fee:** confirm ₹2,500 per team and the payment method; is it refundable?
7. **On-site logistics:** accommodation (provided or recommended hostels/hotels), meals, reporting time on 2 Nov, Wi-Fi/wired internet, power sockets per team, GPU/compute availability, projector/HDMI for demos.
8. **Hardware:** may we bring our own laptops, phones, a small edge device (e.g., Raspberry Pi/Jetson), and a USB camera?
9. **IP policy for 2026:** do teams retain IP as in 2025?
10. **Judging:** are there weights for the six README criteria, and will there be mentor/jury checkpoints during the 24 h?
11. For international or out-of-state team members: can the university issue an **official invitation letter**?

### 17.2 Draft email (send from the team lead's college email)

> **To:** indux5.0_hackathon@vikrantuniversity.ac.in
> **Subject:** INDUX 5.0-2026 – Team [Team Name] – clarifications on Stage 2 deadline and rules
>
> Respected INDUX 5.0 Organising Committee,
>
> We are Team [Team Name] from [College], registering for INDUX 5.0-2026 under the **Environment, Health & Safety (EHS)** theme (aligned to Problem Statement 17). We are excited to participate and would be grateful for clarity on a few points so that we comply fully with the rules:
>
> 1. The brochure lists the Stage 2 (Abstract, PPT & Video) deadline as **2 October 2026**, while Devpost shows **15 October 2026**. Could you confirm the final deadline and whether we should submit on the university PPT form, on Devpost, or both?
> 2. May teams frame their own problem statement within a theme, or must it be one of the 23 listed statements?
> 3. For the online interview, may we demonstrate a small proof of concept? And for the on-site round, may we bring pre-prepared datasets, pre-trained model weights and design mock-ups (with all on-site code written during the 24 hours and all resources disclosed with attribution)?
> 4. Is the team size 3–4 members as per the brochure?
> 5. Could you share details on the interview format, the registration-fee payment process, and on-site logistics (accommodation, reporting time, internet and power availability)?
>
> Thank you for organising this initiative. We look forward to your guidance.
>
> Warm regards,
> [Name], Team Lead, Team [Team Name]
> [College, Programme, Year] · [Phone] · [Email]

---

## 18. Devpost platform notes

- **Challenge ID 31477**; slug `indux-5-0-2026` **[V]**.
- Devpost shows "**Deadline: Oct 15, 2026 @ 3:30pm IST**" and a calendar export (Apple/Google/Outlook) **[V]**.
- Winners announced **3 Nov 2026, 16:30 IST** **[V]**.
- Devpost's Discord link (https://discord.com/invite/HP4BhW3hnp) is Devpost's **global** server, not a hackathon-specific one **[V]**.
- "Looking for a teammate" lives in the participants tab (login required) **[V]**.
- reCAPTCHA protects the site; the participants list needs login **[V]**.

---

## 19. Strategic implications (summary)

1. **Speed first:** register now, submit by 2 Oct, and confirm with the organisers in writing.
2. **Theme: EHS, anchor PS-17**, reframed as a *human-centric occupational-safety early-warning loop*, where **near-miss voice reports are the earliest warning signal**, fused with heat-stress and fatigue signals.
3. **Speak industry.** Near-miss, LOTO, permit-to-work, CAPA, 5-Why, Bird's triangle, ISO 45001, OSH Code 2020. Show ₹ ROI and a buyer.
4. **Show technical depth** (six criteria): a multi-model pipeline, calibrated triage with Jev, an evaluation harness, and on-device CV.
5. **Please every stakeholder honestly.** The industry jury gets shop-floor impact; the CV judge gets real CV with metrics and privacy; the sovereign-AI sponsor gets open-model on-prem mode; the QCFI/Kaizen host culture gets frontline workers as problem-solvers.
6. **Demo reliability over feature count:** one golden path, offline fallback, recorded backup.

---

## 20. Sources (primary first)

- Devpost: https://indux-5-0-2026.devpost.com/ · /rules · /details/dates · /updates · /forum_topics · /project-gallery · /participants · /resources
- Official README: https://github.com/VikrantUniversity-gwalior/Indux-5.0-2026 (raw: https://raw.githubusercontent.com/VikrantUniversity-gwalior/Indux-5.0-2026/main/README.md)
- VU INDUX page: https://vikrantuniversity.ac.in/indux_5.0_2026/ · problem statements: https://vikrantuniversity.ac.in/indux_5.0_2026/problem-statements/ · brochure: https://vikrantuniversity.ac.in/static/images/hackthon/Brochure_2.pdf · junior hackathon: https://vikrantuniversity.ac.in/indux_5.0_2026/jrhackathon/
- VU AI Cell: https://vikrantuniversity.ac.in/ai-cell/ · report: https://vikrantuniversity.ac.in/static/images/aicell/Reports/16.pdf
- 2025 recap: https://vikrantuniversity.ac.in/blog/indux-50-national-hackathon-at-vikrant-university/ · https://induxhack.com/ · https://qcfi.in/event/induxhack/ · https://qcfi.in/indux-5-0-indias-first-national-level-hackathon-on-industry-5-0-and-smart-manufacturing-on-10th-12th-october-2025/ · LinkedIn recap: https://www.linkedin.com/posts/avinash-mishra-8496a669_national-indux-50-hackathon-2025-vikrant-activity-7389652296776880128-OQvA · RBU newsletter: https://rbunagpur.in/wp-content/uploads/2026/07/Oct-Dec-2025-_Newspaper-Format-Setting-10x15-Currection-File.pdf
- Judge: https://scholar.google.com/citations?user=JV5kovoAAAAJ&hl=en
- Sponsor: https://gokloud.io/ · https://arina.ai/ · https://inc42.com/company/gokloud-software-solutions/
- Local context: https://dcmsme.gov.in/dips/gwalior.pdf · https://en.wikipedia.org/wiki/Malanpur · https://insights.dataful.in/articles/factory-accidents-are-falling-but-deaths-remain-high
