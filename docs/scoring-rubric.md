# Arkiv × Puna Tech Builder Challenge — Scoring Rubric

---

## Scoring scale

Each sub-criteria is scored **1–5**:

| Score | Meaning |
|-------|---------|
| 1 | Missing or broken |
| 2 | Minimal effort, barely functional |
| 3 | Works, meets expectations |
| 4 | Good — thoughtful implementation, above average |
| 5 | Excellent — impressive, creative, or production-quality |

---

## Criteria 1: Arkiv integration depth (40%)

This is the core of the challenge. We're evaluating how meaningfully Arkiv is used as the data layer — not just whether it's present.

| Sub-criteria | 1 (Weak) | 3 (Solid) | 5 (Excellent) |
|-------------|----------|-----------|----------------|
| **Entity schema design** | Single blob entity, no structure. Missing or generic `PROJECT_ATTRIBUTE`. | Separate entity types stamped with a unique `PROJECT_ATTRIBUTE`, with typed attributes and clear separation of concerns | Well-designed schema with right-typed attributes, payload structured for the use case, project-namespaced cleanly |
| **Query usage** | Only reads by entity key | Filters by `PROJECT_ATTRIBUTE` plus 1–2 theme attributes | Uses multiple query filters, range queries on numeric attributes, paginates large result sets |
| **Ownership model** | No wallet association | Uses `$owner` correctly (only the owner can update/delete) | End-user `$owner` for write/update/delete control, plus `$creator` used intentionally for tamper-proof attribution where it matters |
| **Entity relationships** | No relationships | Parent → child links via shared-attribute foreign keys | Foreign-key attributes used consistently, relationships maintained on create/delete, used for navigation and data integrity |
| **Expiration dates** | No expiration set, or same expiration on everything | `expiresIn` durations present and reasonable for the domain | Thoughtful, differentiated `expiresIn` per entity type reflecting real product logic |
| **Advanced features** | None | Entity lifecycle transitions based on business logic | Multiple: batch creates via `mutateEntities`, creative use of Arkiv features |

**Section score** = average of 6 sub-criteria, weighted at 40%

---

## Criteria 2: Functionality (30%)

Does it work? Can a real user complete the core flows for the chosen theme?

| Sub-criteria | 1 (Weak) | 3 (Solid) | 5 (Excellent) |
|-------------|----------|-----------|----------------|
| **Core flows work** | Can't complete basic create or browse flow | Create + browse + view details all work end-to-end | All flows work reliably: create, browse, filter, view, interact, edit, manage |
| **Filtering & search** | No filtering | 1–2 filters work | Multiple filters, keyword search, filters combinable, results update correctly |
| **Wallet integration** | Wallet connects but nothing happens | Wallet-gated features work | Smooth wallet flow: connect, chain check, error states, disconnect. Blockchain complexity abstracted away. |
| **Error handling** | Crashes or silent failures | Basic error messages shown to user | Graceful error states: network issues, failed transactions, validation errors |
| **Data integrity** | Data inconsistencies, broken references | Data is consistent within the app | Entity status transitions are reliable, no orphaned data |

**Section score** = average of 5 sub-criteria, weighted at 30%

---

## Criteria 3: Design & UX (20%)

Would someone actually use this? Does it feel like a product, not a demo?

| Sub-criteria | 1 (Weak) | 3 (Solid) | 5 (Excellent) |
|-------------|----------|-----------|----------------|
| **Visual design** | Default/unstyled, no design effort | Clean, consistent styling. Looks intentional. | Distinctive visual identity, good typography, cohesive colour palette, feels professional |
| **User experience** | Confusing navigation, unclear what to do next | Clear information hierarchy, obvious CTAs, reasonable flow | Intuitive from first visit, good empty states, loading states, progressive disclosure |
| **Responsive** | Broken on mobile | Usable on mobile, basic responsive layout | Looks and works well across screen sizes |
| **Blockchain abstraction** | User needs to understand Arkiv/blockchain to use the app | Blockchain details present but not blocking | User doesn't need to know about Arkiv or blockchain to browse and use core flows |

**Section score** = average of 4 sub-criteria, weighted at 20%

---

## Criteria 4: Code quality & documentation (10%)

Can someone else understand and run your project?

| Sub-criteria | 1 (Weak) | 3 (Solid) | 5 (Excellent) |
|-------------|----------|-----------|----------------|
| **README** | Missing or "TODO" | Setup instructions that work, basic description | Clear README with architecture overview, setup steps, and explanation of Arkiv integration approach |
| **Code organisation** | Single file or spaghetti | Reasonable file structure, components separated | Clean architecture, separation of concerns, readable naming |
| **Code quality** | Unreadable, no error handling | Consistent style, basic error handling | Clean, consistent, well-structured. Types where appropriate. No obvious security issues. |

**Section score** = average of 3 sub-criteria, weighted at 10%

---

## Final score calculation

```
Final Score = (Arkiv Integration × 0.40) + (Functionality × 0.30) + (Design & UX × 0.20) + (Code Quality × 0.10)
```

Each section score is the average of its sub-criteria (all on 1–5 scale), so the final score is also on a 1–5 scale.

---

## Judge scorecard template

```
Submission: [Team name]
Theme(s): [Themes addressed]
Judge: [Name]
Date: [Date]

ARKIV INTEGRATION (40%)
  Entity schema design:     _/5
  Query usage:              _/5
  Ownership model:          _/5
  Entity relationships:     _/5
  Expiration dates:         _/5
  Advanced features:        _/5
  Section avg:              _/5

FUNCTIONALITY (30%)
  Core flows work:          _/5
  Filtering & search:       _/5
  Wallet integration:       _/5
  Error handling:           _/5
  Data integrity:           _/5
  Section avg:              _/5

DESIGN & UX (20%)
  Visual design:            _/5
  User experience:          _/5
  Responsive:               _/5
  Blockchain abstraction:   _/5
  Section avg:              _/5

CODE QUALITY (10%)
  README:                   _/5
  Code organisation:        _/5
  Code quality:             _/5
  Section avg:              _/5

WEIGHTED FINAL:             _/5

Notes:
[Free-form observations, standout features, concerns]
```

---

## Tiebreaker

If two submissions have the same final score (within 0.1):
1. Arkiv Integration score is the tiebreaker (highest wins)
2. If still tied, the judge panel discusses and reaches consensus
