# Appendix · Risk Register

**Purpose:** Every named risk on the engagement, in one place, with an owner and a trigger. A risk nobody owns is a surprise being scheduled.

**When it is written:** Opened with 06, reviewed at every status report. A risk leaves the register when it happens (it becomes an issue, tracked in the status report) or when its window closes.

## Format

| ID | Risk (if / then) | Likelihood | Impact | Owner | Mitigation in motion | Trigger | Status |
|----|------------------|-----------|--------|-------|----------------------|---------|--------|
| R-01 | [If X happens, then Y follows for the engagement] | Low / Med / High | Low / Med / High | [name or role] | [what is already being done about it] | [the observable sign it has arrived] | Open / Watching / Closed |

Rules of the register:

- A risk statement names a cause and a consequence. "The schedule slips" is not a risk; "if the client's reviewer is unavailable in week 4, then the accessibility pass has no sign-off and launch moves" is.
- Likelihood and impact are words, not numbers, unless the engagement has real base rates to score from. False precision is worse than honest words.
- Every open risk has exactly one owner, and the owner is a person, never a team.
- The trigger is observable by someone other than the owner. If only the owner can tell the risk has arrived, the register is decoration.

## Filled rows (fictional product: Tidepool)

| ID | Risk (if / then) | Likelihood | Impact | Owner | Mitigation in motion | Trigger | Status |
|----|------------------|-----------|--------|-------|----------------------|---------|--------|
| R-01 | If guest access (OD-01) is ruled in after Phase 2, then the permission model in 05 is reworked and Phase 3 grows by a week | Med | Med | Engagement lead | Permission model drafted with the guest case isolated behind one rule, so the rework stays local | OD-01 ruling date passes, or the sponsor raises guests in a review | Closed (2026-09-14: OD-01 was ruled out by D-03, so the rework risk did not materialize) |
| R-02 | If the seeded 500-task board misses the load budget in 02, then Phase 2 exit criteria fail and the data shape is revisited late | Low | High | Build lead | Budget test written in week 1 of Phase 2 against generated data, not in the final week | Budget test fails on generated data | Watching |
