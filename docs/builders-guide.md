# Arkiv × Puna Tech Builder Challenge — Builder's Guide

---

## What you're building

A **web3-native application** where all data lives on Arkiv. Users own their data — not the platform.

Pick the approved theme:

| Theme | The pitch | The hook |
|-------|-----------|---------|
| **AI apps on [ARKIV]** | Build AI applications that use Arkiv as their data layer | you're replacing centralised data layers for AI agents |

**Go with whatever excites you.**

---

## How Arkiv works (60-second mental model)

### 1. Entities = payload + typed attributes + `expiresIn`

Every Arkiv entity has:

- **Payload** — the actual data (JSON, text, or bytes). Stored as-is.
- **Attributes** — typed key-value pairs. **This is your index.** Filtering, sorting, and lookups happen against attributes, not the payload.
- **`expiresIn`** — a **duration in seconds** set at creation.

### 2. Attributes have types — pick the right one

- **String attributes** support equality and glob matching (`~`). Use for tags, statuses, names, identifiers.
- **Numeric attributes** support range queries (`gt`, `lt`, `gte`, `lte`). Use for any value you'll filter or sort by range — timestamps, scores, counts.

If you store `priority` as the string `"5"`, you lose range queries. Always store numerics as numbers.

### 3. Relationships are shared attribute keys

There is no built-in foreign-key field. To link entities, use a shared attribute key with the parent's entity key as the value (e.g., `{ key: "agentKey", value: agentEntityKey }`). Querying children of a parent is then a single `where(eq(...))`.

### 4. Two metadata fields matter: `$owner` and `$creator`

- **`$owner`** — the wallet that currently controls the entity. Mutable. Only the owner can update or delete.
- **`$creator`** — the wallet that originally created the entity. **Immutable** — cannot be spoofed.

---

## Best practice: PROJECT_ATTRIBUTE

**Arkiv is a shared, public database.** Every entity from every project lives in the same store. Without a project namespace, your queries return everyone else's data.

Every Arkiv project must:

1. Define a unique `PROJECT_ATTRIBUTE` constant (e.g., `lib/arkiv.ts`).
2. Stamp it on **every** create and update call.
3. Filter on it in **every** query.

```typescript
// lib/arkiv.ts
export const PROJECT_ATTRIBUTE = {
  key: "project",
  value: "myteam-arkiv-puna-tech-builder-challenge-7x9k",  // globally unique to your project
} as const;
```

This is graded.

---

## Minimum requirements (all themes)

- [ ] Define and use a unique `PROJECT_ATTRIBUTE` on every entity and every query
- [ ] At least 2 entity types
- [ ] Wallet-based ownership (creators own their data)
- [ ] Queryable attributes used for filtering or search
- [ ] Rational expiration dates on entities (see [A note on expiration](#a-note-on-expiration) below)
- [ ] Public read access (no wallet needed to browse)
- [ ] Open source GitHub repo
- [ ] Working demo link
- [ ] README with setup instructions

---

## Theme: AI apps on [ARKIV]

*Build AI applications that use Arkiv as their data layer*

TBC — to be filled in with partner before publishing

### Things worth thinking through

TBC — to be filled in with partner before publishing

### Directions to push it further

TBC — to be filled in with partner before publishing

---

## A note on expiration

All Arkiv entities have an expiration date — this is core to how Arkiv works, not an optional feature. On testnet, expiration has no cost implications. On mainnet, shorter-lived entities are cheaper. Choose expiration dates thoughtfully: different entity types should have different durations reflecting real product logic. That intentionality is what scores well on Arkiv integration depth.

---

## Getting started

1. **Pick your theme**
2. **Read the Arkiv docs** — [docs.arkiv.network](https://docs.arkiv.network)
3. **Install the Arkiv agent skill** — [docs/agent-skill.md](agent-skill.md) — front-loads SDK knowledge into your AI coding assistant
4. **Set up your `PROJECT_ATTRIBUTE`** before writing any entity code
5. **Connect to Arkiv Testnet:**

   | Setting | Value |
   |---------|-------|
   | Network ID | `60138453102` |
   | RPC (HTTP) | `https://braga.hoodi.arkiv.network/rpc` |
   | RPC (WebSocket) | `wss://braga.hoodi.arkiv.network/rpc/ws` |
   | Bridge contract | `0xB52b417A79c9dE21ffe221dF9a3821B7EaC60813` |
   | Faucet | TBC — check Discord for updates |

6. **Install the SDK:**

   ```bash
   npm install @arkiv-network/sdk@0.6.8
   ```

7. **Get create + read + query working for one entity type first** — then add relationships, then more types
8. **Join the Discord support channel** — **dedicated support channel (coming soon)** on the [Arkiv Discord](https://discord.gg/arkiv)

---

## Submission requirements

| What | Details |
|------|---------|
| **Theme** | State which theme your submission addresses |
| **GitHub repo** | Public, open source, README with setup instructions |
| **Demo link** | Working deployment connected to Arkiv Testnet |
| **Demo video** | Optional at submission, required for prize claim (2–3 min walkthrough) |
| **Team info** | Names, GitHub handles, wallet address for prize |

**Submit here:** [Submission form — link coming soon]()

---

## Questions?

Join our [Discord](https://discord.gg/arkiv) → **dedicated support channel (coming soon)**. The Arkiv team is on call daily during the build window.

Don't struggle alone. If you're stuck on an Arkiv integration issue, ask.
