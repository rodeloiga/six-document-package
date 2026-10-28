# 02 · Technical Requirements

**Purpose:** Name the constraints the build must hold no matter how it gets built, while changing them is still cheap.

**When it is written:** After 01 is stable in draft, before build work starts. Owned by whoever leads the build. Revised through the decision log when a constraint changes. The set is drafted iteratively, not in strict numeric order: section 5's volumes depend on the entity inventory in 05, so 02 and 05 are revised against each other until both are stable.

## Skeleton

### 1. Platforms and environments
[Operating systems, browsers, and devices in scope, with the oldest or weakest one named as the design target. Staging and production environments, and what each is for.]

### 2. Performance budgets
[Numbers, not adjectives. Page or screen load budget on the target device and connection; response budget for the three most common actions; data budget for the first load. "Fast" is not a requirement.]

### 3. Security and privacy requirements
[Authentication model. Authorization model in one paragraph: who can do what to which data. Data classification: what is personal, what is sensitive, what is public. Retention: how long each class is kept, and how deletion works and is proven. Encryption in transit and at rest.]

### 4. Integrations
[Each external system: what it provides, what happens when it is down, who owns the account and the keys. An integration with no failure behavior is an unfinished requirement.]

### 5. Data volume and growth
[Expected records at launch, at one year, at three years, for the largest entity in 05. Which queries must stay fast at the three-year number.]

### 6. Accessibility, technical side
[The conformance target (for example WCAG 2.2 AA), the assistive technologies in the test set, and the rule that accessibility defects are defects, triaged like any other.]

### 7. Observability and operations
[What gets logged, what gets alerted on, who gets paged, backup cadence, and the restore test: a backup that has never been restored is a hope, not a backup.]

### 8. Technical non-goals
[Named explicitly: the platforms not supported, the scale not engineered for, the features of the platform deliberately unused.]

### 9. Open technical decisions
[Flagged with owner and date, same discipline as 01 section 8.]

## Filled fragment (fictional product: Tidepool)

### 2. Performance budgets (excerpt)

- Board screen, target device (mid-range Android phone, 4G): interactive in 2.5 seconds or less with 500 Tasks in the Workspace.
- Dragging a Task between columns: visible response in 100 milliseconds; the Board never waits on the server to move the card.

### 3. Security and privacy requirements (excerpt)

- Sessions expire after 12 hours idle; signing out on one device offers sign-out everywhere.
- Task content is personal data. It is never used for advertising, never sold, and export produces a complete CSV or JSON archive the Workspace owner can download at any time.
- Deleting a Workspace deletes its data within 30 days, including backups, and the deletion is logged with a timestamp the owner can request.
