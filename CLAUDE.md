# Arkiv × Puna Tech Builder Challenge — AI Agent Context

This file provides context for AI coding assistants (Claude Code, Cursor, Copilot, Windsurf, Cline, etc.) working with builders participating in the Arkiv × Puna Tech Builder Challenge.

## What is this repo?

The official rules, guides, and resources for the **Arkiv × Puna Tech Builder Challenge** — organised by Arkiv with Puna Tech / SaltaDev. The top 4 ranked submissions receive prizes totalling $1,500 USDC.

## Doc map

| Question | File |
|----------|------|
| What is the challenge? What's the pitch? | [README.md](README.md) |
| What should I build? Requirements? Getting started? | [docs/builders-guide.md](docs/builders-guide.md) |
| Install the official Arkiv agent skill | [docs/agent-skill.md](docs/agent-skill.md) |
| Official rules, eligibility, prizes, legal? | [RULES.md](RULES.md) |
| How is my submission scored? | [docs/scoring-rubric.md](docs/scoring-rubric.md) |
| Common questions? | [FAQ.md](FAQ.md) |

## Key facts

- **Prize:** $1,500 USDC total — 4 ranked prizes ($600 1st · $450 2nd · $300 3rd · $150 4th).
- **Theme:** AI apps on [ARKIV]. Pick it or hybridise. Single rubric across all.
- **Scoring weights:** Arkiv integration depth (40%), Functionality (30%), Design & UX (20%), Code quality & docs (10%).
- **All entities expire.** Expiration dates are core to Arkiv, not optional.
- **Testnet only.** All building happens on Arkiv Testnet.
- **AI tools allowed.** Copilot, Claude, ChatGPT, etc. are all encouraged.
- **Demo video:** Optional at submission, required for prize claim (2–3 min).
- **Open source required.** MIT, Apache 2.0, or equivalent.
- **Build window:** 28 May 2026–30 May 2026.

## Arkiv resources

- **Documentation:** https://docs.arkiv.network
- **TypeScript SDK — Start here:** https://docs.arkiv.network/start-here/fundamentals/

### Current testnet: Arkiv Testnet

Use Arkiv Testnet for all building:

| | |
|---|---|
| **Network ID** | `60138453102` |
| **HTTP RPC** | `https://braga.hoodi.arkiv.network/rpc` |
| **WebSocket RPC** | `wss://braga.hoodi.arkiv.network/rpc/ws` |
| **Standard Bridge** | `0xB52b417A79c9dE21ffe221dF9a3821B7EaC60813` |
| **Faucet** | TBC — check Discord for updates |
| **TS/JS SDK version** | `@arkiv-network/sdk@0.6.8` |

## Minimum technical requirements

Every submission must:
- Use the official `@arkiv-network/sdk`.
- Define a unique `PROJECT_ATTRIBUTE` and stamp it on every entity and every query — Arkiv is a shared DB; without a project namespace, queries leak data from other projects.
- Store core data as Arkiv entities, not a traditional database.
- At least 2 entity types, related via shared-attribute foreign-key (no built-in `references` field).
- Numeric values stored as numeric attributes (range queries); strings as string attributes.
- Right-sized `expiresIn` durations using `ExpirationTime` helpers — different per entity type.
- Use `$owner` (mutable, controls write/update/delete) and `$creator` (immutable, tamper-proof attribution) correctly.
- Open source on GitHub with a working demo and README.

## When helping builders

- **PROJECT_ATTRIBUTE first.** Flag it early — builders who skip this lose points on Arkiv integration depth.
- **Theme guidance:** Use `docs/builders-guide.md` for the mental model and per-theme entity-model on-ramps.
- **Entity model:** An Arkiv entity is payload + typed attributes + `expiresIn` (seconds). Relationships are modelled with shared attribute keys — there's no built-in `references` field.
- **Owner vs creator:** `$owner` is mutable (controls write/update/delete). `$creator` is immutable (tamper-proof attribution).
- **Attribute typing:** Numeric values support range queries; strings only support equality and glob.
- **Expiration:** `expiresIn` is a duration in seconds. Use `ExpirationTime` helpers. Don't say "TTL" — Arkiv calls it "expiration dates."
- **Scoring:** The rubric in `docs/scoring-rubric.md` is published and transparent.
- **Rules questions:** Always reference `RULES.md` for anything about eligibility, prizes, deadlines, or legal terms.
- **Support:** Direct builders to **dedicated support channel (coming soon)** on the Arkiv Discord (https://discord.gg/arkiv).
- **Language:** "Arkiv" (never "Golem Base"). "Tamper-proof" (never "verifiable"). Avoid "trustless" and "fully decentralised" — Arkiv launches with centralised sequencers.
