# 04 · Design Brief

**Purpose:** Set the visual and interaction direction deliberately: what the product should look like, feel like, and never do. This document is the design contract the build is checked against.

**When it is written:** After 01 and a draft of 03 exist, alongside the flow work. Owned by the design role on the engagement. Revised through the decision log when direction changes.

## Skeleton

### 1. Design principles
[Three to five principles, each one sentence plus what it forbids. A principle that forbids nothing decides nothing. Every principle must be usable in an argument: when two screens disagree, the principle picks the winner.]

### 2. The audience, as readers and viewers
[Who looks at this, in what conditions: lighting, device, stress level, time pressure. What they already know how to read (the conventions of the tools they use now) and what this product may not assume.]

### 3. Visual language
[Type: families, scale, where display type is allowed. Color: the palette posture (what color is rationed for, what it must never mean alone). Surface treatment: flat or dimensional, borders, elevation, texture. Density: how much fits on a screen and why.]

### 4. Component inventory
[The recurring parts: buttons, cards, lists, forms, dialogs, navigation. Each named with the name it carries in 03. New components are added here first, not invented per screen.]

### 5. Motion posture
[What moves, what never moves, and what movement means when it happens. Reduced-motion behavior is specified here, not patched in later: everything readable and usable with motion off.]

### 6. Accessibility commitments
[The concrete promises beyond the conformance target in 02: minimum contrast pairs by name, focus visibility, target sizes, text that survives 200 percent zoom, error messages that say what happened and what to do next.]

### 7. Content voice
[How the product talks: sentence case or title case, how errors are worded, which words the product uses for its own concepts (the same words as 01 and 03), and which words it never uses.]

### 8. Reference models
[Named products or systems studied for this direction. For each: what was borrowed, what was rejected, and why. Borrowing without a rejection list is imitation, not direction.]

### 9. What the design must never do
[The bright lines: patterns banned for this product (for example dark patterns, autoplay, color as the only signal, motion that cannot be turned off). Short list, absolute language.]

### 10. Open decisions
[Flagged with owner and date.]

## Filled fragment (fictional product: Tidepool)

### 1. Design principles (excerpt)

- **The Board is a desk, not a dashboard.** The product shows the work itself, large and plainly. This forbids summary widgets, charts, and stat bands on the Board screen: anything that describes the work instead of showing it lives elsewhere or nowhere.
- **Status is words first.** A Task's state is always readable as text. Color may repeat the words; it may never replace them. This forbids color-only status dots anywhere in the product.

### 9. What the design must never do (excerpt)

- Never animate a card while a person is dragging another card.
- Never use red for anything except a destructive action and its confirmation.
- Never show an empty state that is only an apology. Every empty state offers the action that fills it.
