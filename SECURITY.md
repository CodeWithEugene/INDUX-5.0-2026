# Security Policy

Suraksha Loop processes **workers' voice reports, workplace hazard data and operational permits**. Security and privacy failures here can harm the very people the product protects. This policy explains how to report vulnerabilities, how we handle data, and what we do if something goes wrong.

---

## 1. Supported versions
| Version | Supported |
|---|---|
| `main` (hackathon prototype, INDUX 5.0-2026) | ✅ best effort |
| Tagged demos (`demo-v1`, `demo-final`) | ⚠️ frozen; fixes land on `main` |

This is a **prototype**. Do not use it with real personal data without a security review, a data-protection impact assessment and the plant's authorisation.

---

## 2. Reporting a vulnerability
- **Do not open a public GitHub issue** for security problems.
- Use **GitHub's private vulnerability reporting** on this repository (Security → Report a vulnerability), or contact the repository owner privately.
- Include:
  - the affected component (worker PWA, console, API route, pipeline, provider adapter, sovereign stack);
  - steps to reproduce or a proof of concept;
  - the impact (data exposure, unauthorised action such as releasing a permit hold, prompt-injection effect);
  - any suggested fix.
- **What to expect:**
  - acknowledgement within **72 hours**;
  - an initial assessment within **7 days**;
  - coordinated disclosure after a fix.
  - We credit reporters who want credit.
- **Please do not:** access or modify data that isn't yours, degrade availability (no load or DoS testing), or use social engineering against team members or event staff.

---

## 3. Threat model (summary)
| Asset | Threats | Key controls |
|---|---|---|
| Worker identity & voice | Re-identification, retaliation, leakage | Anonymous mode (hashed device tokens); raw audio deleted after confirmation; PII redaction; no biometrics; faces blurred on-device |
| Incident & permit integrity | Forged reports, malicious hold/release, tampering | Device-token auth + rate limits; RBAC; confirmation dialogs; release requires a reason; append-only audit log |
| AI pipeline | **Prompt injection** in reports or SOPs; hallucinated fixes; model outage | Inputs treated as data; Jev `instruction_injection` and passage-injection checks; quarantine; citation verification; deterministic policy; tiered fallbacks |
| Secrets / API keys | Leakage to the client or git | Server-only env vars; `import "server-only"`; no keys in `NEXT_PUBLIC_*`; secret scanning; rotation after the event |
| Media storage | Unauthorised access | Private buckets; short-lived signed URLs; EXIF/GPS stripped |
| Availability during the demo | Network/API failure | Local sovereign stack; cached golden path; backup video |

---

## 4. Secure development practices
- **Secrets:**
  - never commit `.env*` files except `.env.example`;
  - store keys in a password manager;
  - set spend caps on AI providers;
  - **rotate every key after the hackathon** (keys will have been exposed on screens and shared laptops).
- **Dependencies:** lockfile committed; `pnpm audit` before freeze; no dependency upgrades in the last 12 hours of the event.
- **Headers:** CSP, `X-Content-Type-Options`, `X-Frame-Options: DENY`, `Referrer-Policy`, `Permissions-Policy` (camera/microphone self only). See [docs/build.md §18](docs/build.md).
- **Input validation:** Zod on every route; audio and image type/size limits; server-side re-encoding of images.
- **Database:** row-level security by plant and role; the service-role key is used only in server routes.
- **Logging:** no transcripts or personal data at `info` level; request IDs for tracing; audit logs retained ≥ 1 year.
- **AI safety:** actions come only from the deterministic policy engine, never directly from model output. Generated content is labelled "AI draft" until a human approves it.

---

## 5. Privacy and data protection (India DPDP Act 2023 / DPDP Rules 2025)
| Principle | Implementation |
|---|---|
| Notice & consent | Multilingual notice with audio; purpose-specific opt-in (no pre-ticked boxes); easy withdrawal; consent log |
| Data minimisation | Pseudonymous worker IDs; anonymous reporting; raw audio deleted after confirmation (default); no face images stored for PPE checks |
| Purpose limitation | Reports are used for hazard control, training and aggregate analytics, **never for disciplining individual workers** |
| Storage limitation | Configurable retention; automatic purge jobs; "Delete my data" for workers |
| Security safeguards | Encryption in transit and at rest (managed Postgres/Storage), RBAC/RLS, audit logs |
| Residency / transfers | India-region hosting (Mumbai). US-hosted AI sub-processors (Anthropic, TypeSafe) are disclosed. **Sovereign mode** keeps all processing on-prem |
| Rights | Access to own reports; correction via re-record/edit; erasure; grievance contact |

---

## 6. Incident response (data breach runbook)
1. **Contain** (within 1 hour): revoke exposed keys and tokens, disable affected routes, rotate the Supabase service key, snapshot logs.
2. **Assess** (within 24 hours): what data, whose, how many, and since when. Preserve evidence.
3. **Notify:**
   - affected individuals **without delay**, in their language, with the likely consequences and the steps taken;
   - the plant operator (the data fiduciary);
   - the **Data Protection Board of India within 72 hours** with a detailed report, as the DPDP Rules 2025 require (verify current requirements at the time).
4. **Remediate:** fix the root cause, add tests and monitoring, and document it in a post-incident review.
5. **Learn:** update this policy and the threat model.

---

## 7. Responsible disclosure scope
**In scope:** this repository's code and its deployed demo instances.
**Out of scope:** third-party services (Anthropic, TypeSafe, Sarvam, Bhashini, Supabase, Vercel, Upstash, Meta); report issues there to the respective vendor. Also out of scope: the INDUX event infrastructure and Vikrant University systems.
