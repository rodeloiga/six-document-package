# 05 · Backend Schema

**Purpose:** Define the data: what entities exist, how they relate, and what must always stay true about them. The schema is designed here, on paper, so it does not get accumulated by accident during the build.

**When it is written:** After 01 and 03 are stable in draft, and revised against 02 as the set firms up. The set is drafted iteratively, not in strict numeric order: 02's budgets are an input here (section 5 sizes its indexes to the volumes in 02), and 02's section 5 in turn depends on this document's entity inventory. Entity names are the names used in 01 and 03, exactly. Revised through the decision log; a schema change that ships without this document changing is a process failure, not a shortcut.

**Client-side substitution:** For projects with no server of their own, this slot holds a data model document instead: the local storage shape, the sync rules if any, what happens on conflict, and what is lost when a device is lost. The document number and its place in the set do not change.

## Skeleton

### 1. Entity inventory
[One row per entity.]

| Entity | What it represents | Owned by (which role creates and retires it) |
|--------|--------------------|------------------------------------------------|
| [name] | [one line] | [role] |

### 2. Relationships
[Stated in words before any diagram: a Workspace has many Projects; a Project has many Tasks; a Task belongs to exactly one Project and moves between Projects only by an explicit transfer action, never silently. Cardinality and optionality for every pair.]

### 3. Field definitions
[Per entity: each field, its type, whether it is required, its default, and where its values come from. Fields that duplicate another field's fact are flagged: one fact lives in one place.]

### 4. Invariants and validation
[The rules that must hold at all times, stated so they can be tested: a Task always has exactly one owner who is a member of its Workspace; a deleted Project's Tasks are archived, never orphaned. Each invariant names where it is enforced: database, service, or interface, and why there.]

### 5. Indexes and query patterns
[The five to ten queries the product actually runs, taken from the flows in 03, and the index each one needs at the three-year volume from 02. Queries not on this list do not get indexes speculatively.]

### 6. Migration policy
[How schema changes ship: additive first, destructive changes staged across releases, and the rollback story for each class of change.]

### 7. Retention and deletion
[Per entity: how long it lives, what archives it, what deletes it, and how deletion is verified. This section must agree with the retention requirements in 02; if they disagree, one of them is wrong and the set fails review.]

### 8. Open decisions
[Flagged with owner and date.]

## Filled fragment (fictional product: Tidepool)

### 1. Entity inventory (excerpt)

| Entity | What it represents | Owned by |
|--------|--------------------|----------|
| Workspace | One team's shared space; the permission boundary for everything inside it | Workspace owner |
| Project | A named body of work inside a Workspace, with its own Board | Any Lead in the Workspace |
| Task | One unit of work: title, owner, state, due date, history | Its current owner |

### 4. Invariants and validation (excerpt)

- A Task always has exactly one owner, and that owner is a current member of the Task's Workspace. Removing a member reassigns their open Tasks to the Workspace owner in the same transaction; a Task is never left ownerless.
- A Task's history is append-only. Edits add entries; nothing rewrites or deletes an existing entry. Enforced at the service layer, because the database cannot distinguish a correction from a rewrite.
