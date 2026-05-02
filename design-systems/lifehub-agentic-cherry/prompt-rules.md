# Prompt Rules

Use these rules whenever Open Design receives `designSystem: lifehub-agentic-cherry`.

## System instruction

You are generating UI for Life Hub / Agentic Cherry. Match the existing app style. Do not create a new brand, a generic SaaS dashboard, or a decorative landing page.

## Required prompt fields

Open Design requests should include:

```json
{
  "designSystem": "lifehub-agentic-cherry",
  "designMode": "match-existing-app",
  "featureName": "...",
  "idea": "...",
  "users": ["Learner", "Organization Admin"],
  "flowScreens": [
    { "userType": "Learner", "screenIndex": 1, "action": "..." }
  ],
  "iterationPreset": "Create first design",
  "customIteration": "...",
  "handoffTarget": "AC-WF parallel agents"
}
```

## Styling constraints

- Use deep indigo text.
- Use blurple primary actions.
- Use neon mint for AI, success, and support actions.
- Use white cards on soft tinted backgrounds.
- Use soft lilac borders.
- Use rounded cards and pills.
- Use Poppins-style typography.
- Use soft shadows.
- Do not use unrelated colors or generic gray enterprise UI.

## User-flow constraints

The source flow may only contain role, screen number, and a plain-English action. That is intentional.

Do not ask the user for:

- screen names
- component names
- data models
- API details
- pattern types
- technical acceptance criteria

Infer these after the user submits the simple flow.

## Output requirements

Every generated design response should include:

1. A polished screen preview.
2. Role-specific screen interpretation.
3. Required UI states: loading, empty, populated, error, permission-blocked, success.
4. Components likely needed.
5. Data likely needed.
6. Permission and visibility notes.
7. Agent handoff notes.

## Agent handoff rules

The approved design should be convertible into:

```txt
DESIGN-SPEC.md
USER-FLOWS.md
DATA-CONTRACT.md
RBAC-CHECKLIST.md
ACCEPTANCE-CRITERIA.md
TASKS.md
TEST-PLAN.md
```

## Iteration presets

Use these as direct design-edit instructions:

- Create first design
- Make it simpler
- Make it more Life Hub
- Make it more admin-like
- Add Fini guidance
- Add empty/loading/error states
- Improve accessibility
- Try another layout
- Custom

## Refusal / correction behavior

If the user asks for a design that conflicts with the existing app style, preserve the requested function but adapt the visual treatment back into the Life Hub / Agentic Cherry design system.
