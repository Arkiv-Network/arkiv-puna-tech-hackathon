# AGENTS.md — Arkiv × PunaTech Hackathon

Apply the root `AGENTS.md` first. This file adds hackathon-specific context and constraints.

## Purpose

This repo contains the official rules, guides, and resources for the Arkiv × PunaTech Hackathon: a hackathon track run by Arkiv at PunaTech, organised with PunaTech / SaltaDev, 28 May 2026–30 May 2026. The top 4 ranked submissions receive prizes totalling $1,500 USDC.

## Use these files

| Question | File |
|----------|------|
| What is the challenge? | `README.md` |
| What should builders create? | `docs/builders-guide.md` |
| Official Arkiv agent skill (install for SDK + best-practice context) | `docs/agent-skill.md` |
| Rules, eligibility, prizes, legal terms | `RULES.md` |
| How submissions are scored | `docs/scoring-rubric.md` |
| Common questions | `FAQ.md` |

## Key facts

- Prize: $1,500 USDC total — 4 ranked prizes ($600 1st · $450 2nd · $300 3rd · $150 4th).
- Theme: AI apps on [ARKIV]. Pick it or hybridise.
- Scoring: Arkiv integration depth 40%, functionality 30%, design and UX 20%, code quality and docs 10%.
- All entities expire. Use "expiration dates", never "TTL".
- Testnet only.
- AI tools are allowed.
- Demo video: Required — 2–3 min walkthrough, public URL (YouTube or Google Drive).
- Open source is required.
- Build window: 28 May 2026–30 May 2026.

## Current testnet

Use Arkiv Testnet for all building.

| Item | Value |
|------|-------|
| Network ID | `60138453102` |
| HTTP RPC | `https://braga.hoodi.arkiv.network/rpc` |
| WebSocket RPC | `wss://braga.hoodi.arkiv.network/rpc/ws` |
| Standard Bridge | `0xB52b417A79c9dE21ffe221dF9a3821B7EaC60813` |
| Faucet | https://braga.hoodi.arkiv.network/faucet/ |
| TS/JS SDK | `@arkiv-network/sdk@0.6.8` or later |

## Minimum technical requirements

Every submission must:
- Use the official `@arkiv-network/sdk`.
- Define a unique `PROJECT_ATTRIBUTE` and stamp it on every entity and every query.
- Store core data as Arkiv entities, not a traditional database.
- At least 2 entity types, related via shared-attribute foreign-key.
- Numeric values stored as numeric attributes (range queries); strings as string attributes.
- Right-sized `expiresIn` durations using `ExpirationTime` helpers — different per entity type.
- Use `$owner` (mutable, controls writes) and `$creator` (immutable, tamper-proof attribution) correctly.
- Open source on GitHub with a working demo and README.

## Operating boundaries

### Always do

- Point builders to published docs before inventing explanations.
- Use `docs/builders-guide.md` for theme guidance and per-theme entity models.
- Use `docs/scoring-rubric.md` when asked how to score well.
- Use `RULES.md` for eligibility, prizes, deadlines, or legal terms.
- Preserve the challenge framing, published rubric, and official requirements.
- Respect Arkiv's language conventions: "tamper-proof" (not "verifiable"), "expiration dates" (not "TTL"), "Arkiv" (never "Golem Base").
- Stamp `PROJECT_ATTRIBUTE` on every entity create and every query. Without it, queries leak data from other projects in the shared DB.

### Ask before

- Changing official challenge rules, prize details, deadlines, or scoring language.
- Inventing new technical requirements not present in the published materials.

### Never do

- Paraphrase legal terms from `RULES.md` when exact wording matters.
- Use "TTL" instead of "expiration dates".
- Present Arkiv as optional. It is the required data layer.
- Use deprecated terms like "Golem Base" or describe Arkiv as "trustless" or "fully decentralised" — Arkiv launches with centralised sequencers.
- Recommend a deprecated testnet. Always verify the current network name and RPC from CLAUDE.md or the docs before advising builders.
- Suggest or generate branding, project names, or marketing copy that implies Arkiv officially endorses or partners with the builder's project — crediting Arkiv as the technology used is fine; implying official endorsement is not.

## Builder guidance

- Help builders think in entities (payload + typed attributes + `expiresIn`), shared-attribute foreign keys for relationships, and `$owner` / `$creator` for ownership and attribution.
- Numeric attributes for range queries; string attributes for equality + glob.
- `PROJECT_ATTRIBUTE` on every entity create and every query.
- Batch creates via `walletClient.mutateEntities({ creates: [...] })`. Paginate reads via `result.hasNextPage()` / `result.next()`.
- Direct Arkiv-specific issues to the Arkiv Discord: https://discord.gg/arkiv.
- Design tip (optional, not separately scored): Design & UX is 20% of the score — suggest builders use an open-source component kit such as shadcn/ui (alternatives: Tailwind UI, Radix, daisyUI) to ship faster and invest more time in Arkiv integration depth (40%).
