# FallSeed Clinic

> **A Progressive Web App (PWA) seed for UK Clinic firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-clinic/

## What this is

`fallseed-clinic` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Clinic wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Healthcare clinic · GP / private practice (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallclinic`](https://sjgant80-hub.github.io/fallclinic/) | Patient register · consultations · prescriptions · investigations · safeguarding flags · DNAR · CQC 5KQ tracker · 12-pt compliance |
| onboard | [`fallcliniconboard`](https://sjgant80-hub.github.io/fallcliniconboard/) | Patient onboarding · consent · capacity check · safeguarding screen · GP records request · privacy notice · vulnerable flag |
| paper | [`fallclinicpaper`](https://sjgant80-hub.github.io/fallclinicpaper/) | Consent forms · capacity assessments · DNAR · safeguarding referrals · discharge letters · privacy notices · duty-of-candour letters |
| practice | [`fallclinicpractice`](https://sjgant80-hub.github.io/fallclinicpractice/) | Clinical governance · audit cycle · significant-event log · controlled-drugs register · CQC fundamental-standards tracker · CPD log |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-clinic-v2`) on your device
- **BroadcastChannel mesh** — `fall-clinic` for cross-tool sync; `fall-signal` for global hello
- **Mansoor P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1153**, spine-clean mod 127. Mesh channel **`fall-clinic`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
