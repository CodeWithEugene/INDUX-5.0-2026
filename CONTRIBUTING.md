# Contributing to Suraksha Loop

Thank you for helping build Suraksha Loop. This guide covers **how the team works**: during pre-event preparation, during the 24-hour INDUX 5.0-2026 on-site build, and afterwards.

---

## 1. Ground rules from the hackathon
The INDUX 5.0-2026 rules (official README) say:
> "All code and assets built during the 24 hour on-site round must be original work by the team; open source libraries and APIs are permitted with attribution."

So:
1. **No product code is committed before the event** unless the organisers confirm in writing that disclosed pre-built code is allowed. Before the event we commit **docs, specs, designs, datasets (or pointers to them), prompts and evaluation labels** only. See [docs/build.md §2](docs/build.md).
2. **Everything prepared before the event is listed in `PREWORK.md`** (what, when, by whom).
3. **Every third-party library, model, dataset and API goes into `ATTRIBUTION.md`** with its licence *in the same PR that introduces it*.
4. **Commit early and often during the event.** Commit timestamps are our evidence of on-site work.

---

## 2. Roles and ownership (team of 4)
| Role | Owns | Code areas |
|---|---|---|
| R1 Captain / Product & Pitch | Scope, demo script, deck, seed content, translations, QA | `infra/seed/`, `apps/web/messages/`, `docs/` |
| R2 Frontend | Worker PWA, console UI, shadcn/ui | `apps/web/src/app/(worker|console|public|auth)`, `src/components/` |
| R3 AI/ML | Providers, Jev batteries, policy, RAG, talks, CV, eval | `src/server/{providers,jev,policy,rag,talks}`, `src/cv/`, `eval/` |
| R4 Backend & DevOps | Schema, APIs, realtime, deploy, security | `src/server/{db,pipeline,notify,audit,auth}`, `src/app/api/`, `infra/`, `services/` |

Each owner reviews changes in their area. **R4 merges to `main`.**

---

## 3. Workflow
1. **Branch** from `main`: `feat/<area>-<short-name>`, `fix/<area>-<short-name>`, `docs/<topic>`.
2. **Commit** with Conventional Commits:
   - `feat(worker): hold-to-record with read-back`
   - `fix(policy): tighten thresholds for non-English input`
   - `docs(build): add sovereign compose`
   - `chore(deps): pin shadcn 4.21.0`
3. **Before opening a PR:** `pnpm typecheck && pnpm lint && pnpm test` (and `pnpm eval:triage` if you touched prompts, Jev batteries or policy).
4. **PR description:** what, why, screenshots for UI, the eval delta for AI changes, and ATTRIBUTION updates.
5. **Merge windows** during the event: every 2 hours on the hour. Feature freeze at **T+18h** (bug fixes only after that).
6. Tag `demo-v1` at freeze and `demo-final` at submission.

---

## 4. Code conventions
- **TypeScript strict**; no `any` in server code (use Zod-inferred types).
- **Server-only code** lives in `src/server/**` and starts with `import "server-only"`. API keys never reach the client (no `NEXT_PUBLIC_` keys except the Supabase anon key and the VAPID public key).
- **Validation:** every route handler and server action validates input with Zod (shared schemas in `src/lib/schemas.ts`).
- **AI calls** go only through the provider registry (`src/server/providers/registry.ts`) and `runTiers()`, so every call is traced, timed and has a fallback.
- **Policy lives in code:** `src/server/policy/decide.ts` is pure and 100% unit-tested. Prompts never decide actions.
- **Prompts are versioned files** (`src/server/prompts/*.v<N>.ts`). Changing one needs a new version and an eval run.
- **Jev questions:** keep them narrow; include `other`/`none` options; describe Score levels as situations; pin `jev-1.13.0`.
- **Audit:** every state-changing action on incidents, permits, CAPAs, SOPs, talks, settings or exports writes an `audit_log` row.
- **Privacy:** never log transcripts or personal data at `info` level; raw audio is deleted after confirmation; faces are blurred on-device.

### 4.1 UI conventions: pure shadcn/ui
- Use **only** shadcn/ui components (`npx shadcn@latest add …`), blocks and charts. No other UI kits.
- **Semantic tokens only** (`bg-primary`, `text-muted-foreground`, custom `bg-severity-critical`). Never raw palette classes like `bg-red-500`. A quick check:
  ```bash
  rg "bg-(red|orange|amber|green|emerald|blue|yellow)-[0-9]" apps/web/src
  ```
- Use `gap-*` (not `space-y-*`), `size-*` for squares, and `className` for layout only.
- **Base UI composition:** use the `render` prop, not `asChild`. Links use `buttonVariants()` on `<Link>`.
- Every `Dialog`/`Sheet`/`Drawer` has a Title (`sr-only` if hidden); every icon-only button has an accessible label.
- Worker UI: touch targets ≥ 56 px, every action has an icon, a label **and audio**, and no typing is required.
- Preview upstream changes with `pnpm dlx shadcn@latest add <component> --diff` and never blind-overwrite.

Full rules: [docs/build.md §6](docs/build.md).

### 4.2 Language and copy
- Worker-facing strings live in `messages/{hi,en,or,bn,…}.json` **and** have an audio twin.
- Tone: respectful, warm, short. **Never blame workers.** No jargon in worker copy.
- AI-generated text shown to staff carries an **"AI draft"** badge until a human approves it.

---

## 5. Testing expectations
| Change | Required |
|---|---|
| Policy, risk maths, citation check, sync | Unit tests (vitest) |
| Provider adapters | Contract test against recorded fixtures |
| Golden path, offline, a11y | Playwright specs pass |
| Prompts / Jev batteries / thresholds | `pnpm eval:*` on the **dev split**, with the delta in the PR. Never tune on the test split. |

---

## 6. Data and evaluation sets
- Evaluation audio is recorded **only with explicit consent**. Store the consent note in `eval/CONSENT.md` (names optional).
- Label with two annotators where possible, and record adjudication decisions.
- Mark synthetic items `"synthetic": true`.
- Never commit real worker personal data. The demo plant is fictional and labelled as such.

---

## 7. Reporting issues and ideas
Open a GitHub issue using this template:
- **What happened / what you expected**
- **Steps to reproduce** (for AI issues, include the input and the tier/provider badges shown)
- **Area** (worker, console, pipeline, Jev, policy, RAG, CV, offline, deploy)

For security issues, **do not open a public issue**; see [SECURITY.md](SECURITY.md).

---

## 8. Code of conduct
All contributors follow the [Code of Conduct](CODE-OF-CONDUCT.md).
