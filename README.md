# Suraksha Loop (सुरक्षा लूप)

**Every worker's voice is a safety sensor.**

Suraksha Loop is a voice-first, multilingual occupational-safety early-warning loop for Indian MSME shop floors. A worker reports a hazard **by voice, in their own language, in about 20 seconds, even offline**. AI then:
- turns the report into a triaged incident;
- **holds the affected machine's permit-to-work** when the danger is serious;
- drafts an **SOP-grounded corrective action** with verified citations for supervisor approval;
- sends a **45-second toolbox talk to the next shift in every worker's language**, with a comprehension check;
- **tells the reporter what changed**.

Near-miss reports, heat stress (WBGT) and fatigue signals feed a zone-by-shift **early-warning risk index**.

> Built for **[INDUX 5.0-2026: AI for Real-World Impact](https://indux-5-0-2026.devpost.com/)**, a 24-hour AI hackathon at Vikrant University, Gwalior (on-site 2–3 Nov 2026).
> **Theme:** Environment, Health & Safety (EHS) · **Aligned problem statement:** PS-17 *AI Heat-Stress, Fatigue & Occupational Safety Early-Warning System* (with PS-2 and PS-15).

---

## Status

| Phase | State |
|---|---|
| Research, problem selection, solution design, build spec | ✅ Complete (see `docs/`) |
| Stage 1 – registration (by **1 Oct 2026**) | ⏳ To do |
| Stage 2 – abstract, PPT, 3-min video (brochure: **by 2 Oct 2026**) | ⏳ Content ready in [docs/solution.md §19](docs/solution.md) |
| Stage 3 – online interview (8–9 Oct 2026) | ⏳ Q&A bank ready |
| Stage 5 – 24-hour on-site build (2–3 Nov 2026) | ⏳ Build spec ready in [docs/build.md](docs/build.md) |

> **Rules note:** the INDUX rules require all code built during the 24-hour round to be the team's original work, with open-source libraries and APIs allowed with attribution. This repository therefore contains **documentation and specifications only** until the organisers confirm what pre-event work is permitted. See [docs/build.md §2](docs/build.md) and `PREWORK.md` (created at the event).

---

## Why this matters

- About **3 workers die every day** in India's registered factories, and **660 died in factory accidents in 2024**. **Madhya Pradesh ranked 4th** with 70 deaths.
- In 2025, **93%** of injuries documented by Safe in India's *CRUSHED* report happened on power presses without working safety sensors, and **84%** of those injured workers had already reported the problem and been ignored.
- Most victims are **migrant contract workers** speaking Hindi, Bhojpuri, Odia or Bengali. Safety forms and SOPs are in English, and only about 10.6% of Indians speak English.

Sources and evidence tags are in [docs/problem.md](docs/problem.md) and [docs/research.md §4](docs/research.md).

---

## How it works

```
HEAR ─▶ UNDERSTAND ─▶ JUDGE ─▶ ACT ─▶ FIX & TEACH ─▶ CLOSE ─▶ LEARN
voice    Indic ASR +    Jev      permit   SOP-cited CAPA   reporter   risk index
in own   LLM structured calibrated hold   + toolbox talk   hears      (near-miss +
language extraction     triage   + alerts in every language back      heat + fatigue)
```

**Design mantra:** *The LLM writes. Jev judges. Code decides. Humans approve. Workers hear back.*

| Stage | Primary | Fallbacks (incl. sovereign / on-prem) |
|---|---|---|
| Speech-to-text | Sarvam Saaras v3 | Bhashini · AI4Bharat IndicConformer (local) · browser Web Speech |
| Extraction & generation | Claude Opus 5 (`claude-opus-5`) | Claude Sonnet 5 · open LLM via Ollama (local) |
| Calibrated judgments | TypeSafe Jev (`jev-1.13.0`) | LLM-judge (flagged uncalibrated) · rules |
| Translation | Sarvam Translate | IndicTrans2 (local) · Claude |
| Text-to-speech | Sarvam Bulbul v3 | Indic Parler-TTS (local) · browser TTS |
| Vision (PPE check) | YOLOX-Nano → ONNX, **in the browser** (faces blurred on-device) | — |

**Stack:** Next.js 16 (App Router) · React 19 · TypeScript · **shadcn/ui on Base UI** (Nova style, neutral + orange theme, Geist + Noto Indic fonts) · Tailwind CSS v4 · Supabase (Postgres + pgvector, Storage, Realtime, Auth; Mumbai region) · Drizzle ORM · Upstash Redis · Serwist + Dexie (offline PWA) · onnxruntime-web · open-meteo · Docker Compose (sovereign mode).

---

## Documentation

| Doc | What it covers |
|---|---|
| [docs/info.md](docs/info.md) | **Everything about the challenge**: dates (and conflicts), stages, rules, judging criteria, prizes, people, sponsor, 2025 history and winners, venue, open questions, the draft email to the organisers, and the action checklist |
| [docs/research.md](docs/research.md) | Research method, source log, **evidence register**, technology research (India AI stack, Claude, Jev, shadcn/ui), winning patterns, full source dossiers |
| [docs/problem.md](docs/problem.md) | 15 candidate problems + cliché baseline, evidence, scoring matrix, **why we chose C1**, root-cause analysis, personas, success metrics, validation plan |
| [docs/solution.md](docs/solution.md) | The end-to-end solution: audience, value proposition, the loop, journeys, AI design (Jev question batteries, policy engine), risk index, privacy/DPDP, business model, **ready-to-paste abstract, deck, video script and interview Q&A** |
| [docs/build.md](docs/build.md) | The **build spec**: scope, rules compliance, architecture, stack, repo layout, **pure shadcn/ui design system**, every page, data model, APIs, AI pipeline code, CV, offline, security, testing, deployment, the 24-hour plan and the demo runbook |

---

## Planned repository layout

```
apps/web/               Next.js app (worker PWA + staff console + API routes)
services/ml-sidecar/    FastAPI: local ASR / MT / TTS for sovereign mode
infra/                  docker-compose.sovereign.yml, Supabase migrations, seed data
eval/                   evaluation datasets, runners, reports
docs/                   research and specifications (this phase)
```

## Getting started (after the on-site build)

```bash
pnpm install
cp apps/web/.env.example apps/web/.env.local   # fill keys (see docs/build.md §22)
pnpm --filter web db:migrate && pnpm --filter web seed
pnpm --filter web dev
```

Sovereign / on-prem mode (all AI local):

```bash
docker compose -f infra/docker-compose.sovereign.yml up --build
```

---

## Principles
1. **Human-centric:** AI assists; safety-critical actions are reversible, logged and human-confirmed.
2. **No blame, no surveillance:** anonymous reporting, no individual worker scoring, no face recognition.
3. **Language-inclusive:** voice in and voice out, in the worker's language.
4. **Grounded:** every generated fix cites its SOP clause, and the citation is checked.
5. **Measured:** we publish per-language accuracy, calibration, CV metrics, latency and cost.
6. **Sovereign-capable:** everything can run inside the factory.

## Contributing, conduct, security
- [CONTRIBUTING.md](CONTRIBUTING.md): workflow, conventions, the hackathon rules we follow
- [CODE-OF-CONDUCT.md](CODE-OF-CONDUCT.md)
- [SECURITY.md](SECURITY.md): reporting vulnerabilities, data handling, the DPDP breach runbook

## Licence
[MIT](LICENSE.md). Third-party components keep their own licences (see `ATTRIBUTION.md`, created with the code).

## Acknowledgements
Organisers of INDUX 5.0-2026 (Vikrant University, Arina AI, GoKloud); Safe in India Foundation for documenting worker injuries; AI4Bharat, Bhashini, Sarvam AI, Anthropic and TypeSafe for the models and APIs we build on; the shadcn/ui community.
