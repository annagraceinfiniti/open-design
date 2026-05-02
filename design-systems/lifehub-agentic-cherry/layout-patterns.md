# Layout Patterns

These are the approved layout patterns for Life Hub / Agentic Cherry Open Design output.

## 1. Feature Wizard shell

Use this for idea collection, role selection, user-flow entry, Open Design Studio, and final agent handoff.

Structure:

```txt
Step pills
Main white rounded card
  Header
  One main question
  Input or selection surface
  Optional AI button
Footer
  Save draft
  Back
  Next
```

Rules:

- One major task per page.
- Keep the card spacious.
- Do not crowd the user with developer terminology.
- Use helper copy when the user needs to understand hidden users or downstream roles.

## 2. Role selection grid

Use this for selecting who sees, uses, approves, supports, configures, or receives output from a feature.

Structure:

```txt
Title
Subtitle explaining hidden/supporting roles
AI suggest users button
Role card grid
```

Each card includes:

- role name
- short helper text
- selected state

## 3. Locked simple screen-flow builder

Use this exact interaction model when representing user flows.

Structure:

```txt
What is the user flow?
Subtitle
Generate flows from my inputs button

User section
  Eyebrow: USER
  Role name
  Screen count
  Screen 1 number block + textarea
  Screen 2 number block + textarea
  + Add screen
```

Rules:

- Keep one large textarea per screen.
- Do not require screen pattern or data-contract details here.
- Add up to 20 screens per user.
- Role sections should stack vertically.
- Each screen textarea should accept plain English.
- Open Design infers details later.

## 4. Open Design Studio

Use this after the simple flow builder.

Structure:

```txt
Left panel: controls
  Design system
  Regenerate scope
  Selected role, if scoped
  Iteration preset
  Custom instruction
  Editable prompt
  Generate / Revise
  Approve design

Right panel: preview
  Preview iframe or generated artifact
  Handoff summary
```

Rules:

- The design system selector defaults to `Match existing app exactly`.
- Iteration must be explicit.
- Prompt is editable.
- Approval must be required before send-to-agents.

## 5. Admin dashboard

Use when Organization Admin is the primary role.

Structure:

```txt
Header with context
Status cards
Filter/search row
Table or review queue
Right drawer or detail panel
Empty/error/success states
```

Visual feel:

- structured
- clear
- actionable
- not gray or corporate-generic

## 6. Learner screen

Use when Learner is the primary role.

Structure:

```txt
Friendly header
Progress or goal context
Task/instruction card
Primary action
Fini helper area, if relevant
Reward/badge/earnings context, if relevant
```

Visual feel:

- accessible
- simple language
- positive
- high contrast
- large tap targets

## 7. Learner Support review screen

Use when Learner Support reviews, grades, comments, or provides feedback.

Structure:

```txt
Review queue
Learner/submission detail
Rubric or decision panel
Comment box
Approve / Request changes / Save feedback
```

## 8. Funder / sponsor report screen

Use when Funder or Corporate Sponsor views impact.

Structure:

```txt
Outcome summary
KPI cards
Chart or evidence panel
Narrative summary
Cohort/filter controls
Export/share action
```

Use this pattern only for approved impact/reporting views, not learner-facing screens.
