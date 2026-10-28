# The Six-Document Engagement Package

This is the standard document set Lēdor Labs manages on client product work: six documents, in the same order, with the same names, produced with the engagement's designers and builders in their roles. Every app and web engagement gets the same set. The set is the engagement: it is what gets planned, built, checked, and handed over.

A fixed set exists for one plain reason. When every project invents its own paperwork, the paperwork becomes the project. A standard set means the client always knows where a fact lives, the team always knows which document governs a decision, and a reader picking up any engagement cold can find the requirements, the flows, and the current plan in the same places every time.

## The six documents

| # | Document | The question it answers | What it proves |
|---|----------|------------------------|----------------|
| 01 | Product Requirements | What is being built, for whom, and how will anyone know it worked? | The problem was understood before anything was designed. |
| 02 | Technical Requirements | What constraints must the build hold, no matter how it gets built? | The hard limits were named early, while they were still cheap. |
| 03 | App Flow | What can a person actually do, in what order, in every state? | Every route and state was thought through before it was coded. |
| 04 | Design Brief | What should this look like, feel like, and never do? | The visual and interaction direction was set deliberately, not inherited from a template. |
| 05 | Backend Schema | What data exists, how is it shaped, and what must always stay true about it? | The data model was designed, not accumulated. On a client-side project, 05 holds the data model instead of a server schema. |
| 06 | Implementation Plan | In what order does the work happen, who owns it, and how is each phase checked? | The plan exists before the build does, and it names its own risks. |

Each template in this folder carries a purpose line, the point in the engagement when it is written, a section skeleton with bracketed guidance, and a short filled fragment. All fragments use one fictional product, a small-team task board called Tidepool, so the shape is visible without any real client material.

## Depth scales with the engagement

The set is always six documents. Its depth is not fixed.

- **Clarity Sprint (condensed set).** Each document is short and pointed: enough to state the problem, the constraints, and the first plan. The sprint's job is a decision, and the set is sized to the decision.
- **Fractional lead and rescue engagements (full set).** Every document is written to working depth: full requirement lists with acceptance tests, complete route and state inventories, a schema that can be built from, and an implementation plan with milestones, exit criteria, and a verification plan per phase. A rescue engagement usually starts from someone else's documents or none; the full set is how the current state gets established before anything is changed.

## The consistency law

Feature names, route names, section names, and entity names are identical across all six documents. A thing called a Workspace in 01 is a Workspace in 03, 05, and 06. Screens carry the names given in the route inventory in 03; no other document renames a screen. IDs are global across the set, two digits, prefixed by family: PR for requirements, F for flows, OD for open decisions, D for rulings in the decision log, R for risks. Before the set is delivered, the names are checked across all six documents mechanically, not from memory. A set that fails the name check is not finished, however good each document reads on its own.

## Open decisions stay open

A decision nobody has made yet is flagged as open in the document where it lives, with an owner and a date by which it is needed. Open decisions are never silently filled in by whoever happened to be writing that section. A flagged open decision is a healthy document. A guessed one is a defect that will be discovered later, at a worse time.

## Rulings get reconciled back

Clients rule on open decisions as the engagement runs. Every ruling is recorded in the decision log (appendix), and then reconciled back into whichever of the six documents it changes. The set is the current truth at all times, not a snapshot of what was true at kickoff. If a document and a ruling disagree, the document is wrong until it is updated.

## The appendix instruments

Four working instruments travel with the set:

- **Risk register** (appendix/risk-register.md): every named risk, its owner, its mitigation, and the trigger that says it has arrived.
- **Decision log** (appendix/decision-log.md): every ruling, the options that were considered, and the documents each ruling changed.
- **RACI** (appendix/raci.md): who is responsible, accountable, consulted, and informed for each recurring engagement decision.
- **Status report** (appendix/status-report.md): the weekly shape: what moved, what is next, what needs a decision and by when.

## How an engagement uses the set

The documents are written in order, 01 through 06, because each one spends the decisions the previous one made, and they are revised against each other as the set firms up: drafting is iterative, not a single pass in numeric order. 01 settles what and why. 02 settles the constraints. 03 and 04 are drafted together once 01 and 02 exist. 05 settles the data. 06 turns all of it into a sequence with owners and dates. After kickoff the set is maintained, not archived: the implementation plan is revised at every milestone, and any ruling lands in the decision log and back into the set the same week it is made.

## Who runs this

This package is the standard engagement set of Lēdor Labs. Rodel Oiga is its Principal. Contact and more on how Lēdor Labs works: rodeloiga.com.
