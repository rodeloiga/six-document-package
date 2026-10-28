# 01 · Product Requirements

**Purpose:** State what is being built, for whom, and how anyone will know it worked. Every later document spends the decisions made here.

**When it is written:** First. Drafted after the intake interviews and before any design or technical work. Revised only through a ruling in the decision log.

## Skeleton

### 1. Problem statement
[Two to five sentences. The problem in the words of the people who have it. No solution language. If the problem cannot be stated without naming a feature, it is not understood yet.]

### 2. People served
- **Primary users:** [Who uses this weekly or daily, and what they are trying to get done.]
- **Secondary users:** [Who touches it occasionally: admins, managers, support.]
- **Affected non-users:** [People whose work changes even though they never log in. Name them; they are where adoption fails.]

### 3. Jobs to be done
[One line per job, in the form: when [situation], the user needs to [action] so that [outcome]. Five to nine jobs. If a job has no user from section 2, cut it.]

### 4. Scope
- **In scope:** [The bounded list. Each item maps to a job in section 3.]
- **Out of scope:** [Named explicitly. The out-of-scope list is a commitment, not an omission. Everything deliberately excluded goes here so nobody has to guess later.]

### 5. Requirements
[Numbered PR-01, PR-02, and so on. Each requirement is one testable statement plus its acceptance test: the observable thing that proves it is done. Requirements that cannot be tested get rewritten until they can.]

### 6. Success measures
[Two to four measures, each with a baseline (where it starts) and a target (where it should be, by when). Measures describe the user's world improving, not the software shipping.]

### 7. Constraints and assumptions
[Budget shape, deadlines with external causes, mandated tools or vendors, compliance context. Assumptions are labeled as assumptions, with what breaks if one is wrong.]

### 8. Open decisions
[Flagged, never filled in by the writer. Each: the decision, the owner, the date it is needed by, and which requirement it blocks.]

## Filled fragment (fictional product: Tidepool, a small-team task board)

### 5. Requirements (excerpt)

- **PR-03.** A Lead can see every overdue Task across all their Projects on one screen, without opening each Project.
  *Acceptance test:* Given a Workspace with three Projects and overdue Tasks in two of them, the Lead opens the overview and sees both overdue Tasks, each labeled with its Project, in under three taps from sign-in.
- **PR-04.** A Task can be reassigned to another member of the same Workspace in at most two actions.
  *Acceptance test:* From an open Task, the current owner picks a new owner from the Member list and saves; the Task shows the new owner and the change appears in the Task history.
- **PR-06.** ~~Guest access for clients outside the Workspace, read-only.~~ Removed from release 1 scope by ruling D-03 (2026-09-14); see OD-01.

### 8. Open decisions (excerpt)

- **OD-01.** Does the first release include guest access for clients outside the Workspace? Owner: sponsor. Needed by: end of week 2. Blocks: PR-06, and the permission model in 05. **Closed 2026-09-14 by D-03:** no guest access in the first release; invited people join as Members or not at all.
