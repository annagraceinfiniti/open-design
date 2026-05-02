# Component Rules

Use these component rules when Open Design generates Life Hub / Agentic Cherry screens.

## Global component rules

- Use a bright card-based interface.
- Use deep indigo for headings and body text.
- Use blurple for primary actions.
- Use neon mint for AI assistance, success, and guided helper actions.
- Use pill buttons for navigation and actions.
- Use rounded cards with soft shadows.
- Avoid dense enterprise UI. The product should feel capable, clear, and optimistic.
- Do not use random gradients, dark-mode dashboards, generic gray SaaS panels, or unrelated brand colors.

## Buttons

### Primary button

Use for the main next action on a screen.

Visual style:

```txt
background: blurple
color: white
shape: pill
weight: 800 or 900
shadow: soft blurple shadow
```

Examples:

- Next
- Generate first design
- Approve design
- Send to agents
- Start task
- Submit work

### AI / assistive button

Use for AI-generated help, suggestions, or improvement actions.

Visual style:

```txt
background: soft mint
color: deep green / mint text
shape: pill
weight: 900
```

Examples:

- Generate an idea
- Improve my idea
- AI suggest users
- Generate flows from my inputs
- Add Fini guidance

### Secondary button

Use for lower-risk actions.

Visual style:

```txt
background: transparent
border: soft lilac border
color: muted text or blurple
shape: pill
```

Examples:

- Back
- Save draft
- Reset prompt
- Remove

## Cards and panels

### Main wizard card

```txt
background: white
border: soft lilac
radius: 28px
shadow: soft indigo shadow
padding: 40px
footer: soft tinted background
```

### Design Studio panel

```txt
background: soft tinted white
border: soft lilac
radius: 20px
padding: 18px
```

Use panels for:

- Open Design controls
- design preview
- handoff summary
- role information

## Inputs

```txt
background: white
border: soft lilac
radius: 10 to 12px
padding: 12 to 16px
font: Poppins or system equivalent
```

Textareas should be generous and writable. Do not make users fill many small technical fields when one plain-English textarea works better.

## Role cards

Role cards should show:

- role name
- one-line helper text
- selected state

Selected state:

```txt
border: blurple
background: soft lilac
```

Role helper examples:

- Learner: The learner sees or completes the feature directly.
- Learner Support: Reviews, grades, comments, or supports learners.
- Organization Admin: Configures settings, assigns work, manages learners, or views reports.
- Fini: Adds guidance, nudges, or AI coaching.
- Infiniti: Generates content, reports, analytics, or recommendations.

## Locked flow-page pattern

This pattern must be retained when Open Design represents Feature Wizard flow input.

```txt
What is the user flow?

[Generate flows from my inputs]

User: Learner
Screen 1 [large textarea]
Screen 2 [large textarea]
+ Add screen

User: Organization Admin
Screen 1 [large textarea]
Screen 2 [large textarea]
+ Add screen
```

Do not replace this with detailed fields such as:

- screen name
- pattern
- what does this role do
- what should the screen show
- what happens next

Those details should be inferred later by Open Design and development agents.

## Open Design Studio controls

The Design Studio page should include:

- design system selector
- regenerate scope
- iteration preset
- custom instruction
- editable Open Design prompt
- design preview
- generate/revise button
- approve design button
- handoff summary

## Preview frame

Use a large app-preview frame with a white background, rounded corners, and soft border.

The preview should feel like a screen generated inside the existing app, not a separate website mockup.
