# 03 · App Flow

**Purpose:** Describe every route and state a person can reach, and the paths between them, before any of it is coded. This document is where missing screens and dead ends get found on paper.

**When it is written:** After 01 and a draft of 02, alongside 04. Owned by the UX role on the engagement. Every route named here uses the exact name it has in 01 and will have in 05 and 06.

## Skeleton

### 1. Route inventory
[One row per route or screen.]

| Route | Purpose | Entry points | Exit points |
|-------|---------|--------------|-------------|
| [name] | [one line] | [where a person arrives from] | [where they can go next] |

### 2. Primary flows
[Numbered F-01, F-02, and so on, one per job from 01 section 3. Each flow is a step list written from the person's side: what they see, what they do, what the product does back. Count the steps. A core flow over seven steps gets challenged in review.]

### 3. State inventory
[For each route in section 1, its states: first-run empty, populated, loading, error, offline or degraded, permission denied, and archived or closed where those exist. A route with no error state designed is an error state that will be improvised later by an engineer at a bad moment.]

### 4. Navigation rules
[What is always reachable (home, settings, help, sign-out). What the back action does on each route. What survives a refresh or a killed app: the person should return to where they were, with their work intact.]

### 5. Deep links and notifications
[Which routes can be arrived at from outside (email, a notification, a shared link), what sign-in state each assumes, and where an unauthenticated arrival lands after signing in: on the thing they came for, not the home screen.]

### 6. Open decisions
[Flagged with owner and date. Flow questions are decisions too: if nobody has ruled on what happens when an invite expires, it goes here, not into a developer's guess.]

## Filled fragment (fictional product: Tidepool)

### 2. Primary flows (excerpt)

**F-02 · Invite a teammate**
1. The Workspace owner opens Members from the Workspace menu. The current Member list shows, with roles.
2. The owner enters an email address and picks a role: Member or Lead.
3. Tidepool sends the invitation and shows the address in the list as Invited, with the date.
4. The invited person follows the email link. If they have no account, they create one and land on the Board, not a marketing page.
5. If the invitation is not accepted in 14 days, it expires. The Workspace owner sees Expired in the list and can resend in one action.

### 3. State inventory (excerpt)

| Route | Empty | Loading | Error | Permission denied |
|-------|-------|---------|-------|-------------------|
| Board | "No Tasks yet" with the create action offered | Column skeletons, Board frame visible | Saved copy shown with a retry banner; no data lost | Route hidden; direct link lands on the request-access screen |
