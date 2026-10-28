# 06 · Implementation Plan

**Purpose:** Turn the other five documents into a sequence: phases, owners, milestones with exit criteria, and the order the work actually happens, including how each phase is verified before the next one starts.

**When it is written:** Last of the six, once 01 through 05 exist in draft. Revised at every milestone and whenever a ruling changes scope, sequence, or staffing.

## Skeleton

### 1. Phases and milestones
[Each phase: what it produces, its milestone, and its exit criteria stated as observable facts (not percentages). A phase ends when its criteria are met, not when its calendar box runs out. Dependencies between phases are stated, including the ones on the client: reviews, content, accounts, approvals.]

### 2. Work breakdown by governing document
[For each build chunk, the document that governs it: Board interactions answer to 03 and 04; the permission model answers to 05 and 02. When build work and a document disagree, the document wins until a ruling changes it.]

### 3. Staffing
[Who is on the engagement, in what role, at what allocation. Links to the RACI (appendix). Single-person dependencies are named here and carried into the risk register.]

### 4. Risk summary
[The top risks from the risk register (appendix), by ID, with the mitigation already in motion. The full register lives in the appendix; this section is the three to five that could change the plan.]

### 5. Decision points and dates
[Every open decision from 01 through 05, gathered into one dated list: the decision, its owner, the date it is needed, and the phase it blocks. This is the list the status report nags about.]

### 6. Verification plan
[Per phase: what gets checked, by whom, against which document. Includes the pre-launch pass over the whole set: names consistent across all six documents, every acceptance test in 01 exercised, every flow in 03 walked end to end, every invariant in 05 tested. A phase with no verification plan is a hope.]

### 7. Launch and rollback
[How the release ships, in what order, to whom first. What rollback means for this product, who can call it, and how long it takes. Data migrations name their point of no return explicitly.]

### 8. Open decisions
[Any plan-level decisions still open, flagged with owner and date. The plan may proceed around a flagged decision only if the blocked phase is named.]

## Filled fragment (fictional product: Tidepool)

### 1. Phases and milestones (excerpt)

**Phase 2 · Boards that hold real work.**
Produces: Boards with Tasks, owners, states, and due dates, per flows F-01 to F-04 in 03 and the schema in 05.
Exit criteria: a Workspace with 500 seeded Tasks opens within the performance budget in 02 section 2; every invariant in 05 section 4 has a passing test; two people outside the build team complete F-02 (invite a teammate) without help.
Depends on: Phase 1 (accounts and Workspaces). Blocks: Phase 3 (invitations and permissions polish).
Note on the phase boundary: the invite flow ships in basic form in Phase 2, and the F-02 exit test above is its proof. Phase 3 polishes invitations and permissions; it does not introduce them.

### 5. Decision points and dates (excerpt)

No open decisions in this excerpt. Closed since the last plan revision: **OD-01**, guest access in the first release, ruled out by D-03 (2026-09-14). Phase 3 scope reduced accordingly, and the permission model in 05 proceeds without a guest variant.
