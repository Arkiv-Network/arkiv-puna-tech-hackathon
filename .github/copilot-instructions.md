# Arkiv × PunaTech Hackathon — GitHub Copilot Instructions

## Context

This repo contains official hackathon materials for the **Arkiv × PunaTech Hackathon**, a hackathon track run by Arkiv at PunaTech in collaboration with PunaTech / SaltaDev.

- **Build window:** 28 May 2026–30 May 2026
- **Prize:** $1,500 USDC total — 4 ranked prizes ($600 1st · $450 2nd · $300 3rd · $150 4th)
- **Theme:** AI apps on [ARKIV]
- **Testnet:** Arkiv Testnet — `https://braga.hoodi.arkiv.network/rpc`
- **SDK:** @arkiv-network/sdk@0.6.8 or later

## File map

- `README.md` — overview and pitch
- `docs/builders-guide.md` — themes, entity design, getting started
- `docs/agent-skill.md` — install `arkiv-best-practices` skill
- `RULES.md` — eligibility, prizes, legal terms
- `docs/scoring-rubric.md` — scoring breakdown
- `FAQ.md` — common questions

## Rules for builder assistance

**Technical:**
- `PROJECT_ATTRIBUTE` is mandatory — define a unique constant and stamp it on every entity and every query
- At least 2 entity types, related via shared-attribute foreign-key
- Numeric attributes for range queries; string attributes for equality/glob
- `expiresIn` durations via `ExpirationTime` helpers — differentiate per entity type
- `$owner` for write/update/delete control; `$creator` for immutable tamper-proof attribution

**Language:**
- "Arkiv" — never "Golem Base"
- "expiration dates" — never "TTL"
- "tamper-proof" — never "verifiable"
- Avoid "trustless" and "fully decentralised" — Arkiv launches with centralised sequencers
- Reference `RULES.md` verbatim for prize and legal questions

**Brand use:**
- Builders may credit Arkiv as the technology they built on — that is encouraged. Using the Arkiv / [ ARKIV ] brand, name, or logos in a way that implies official endorsement, sponsorship, or partnership is not permitted unless the builder is operating under a signed agreement with Arkiv.

**Design tip (optional — not separately scored):**
- Design & UX is 20% of the score — suggest builders use an open-source component kit such as shadcn/ui (alternatives: Tailwind UI, Radix, daisyUI) to ship a polished interface faster, freeing more time for Arkiv integration depth (40%).

**Guidance:**
- Send builders to `docs/builders-guide.md` for entity-model help
- Send builders to `docs/scoring-rubric.md` when asked how to score well
- Send builders to the Arkiv Discord for Arkiv-specific support issues: https://discord.gg/arkiv
