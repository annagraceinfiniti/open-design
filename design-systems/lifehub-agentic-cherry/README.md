# Life Hub / Agentic Cherry Design System

This design system is the Open Design preset for generating screens that match the Agentic Cherry UI and Life Hub product style.

Use this preset when the source request comes from the Agentic Cherry Feature Wizard, UI Builder Wizard, AC-WF workflow, or any Life Hub / Infiniti product surface.

## Design system id

```txt
lifehub-agentic-cherry
```

## Primary rule

Open Design must not invent a new visual style for Life Hub or Agentic Cherry screens.

Generated screens should reuse the existing app language:

- bright white cards on soft tinted backgrounds
- dark indigo text and high-contrast headings
- blurple primary actions
- neon mint AI / success / assistive actions
- rounded cards and pills
- soft shadows
- one clear primary action per screen
- concise helper copy
- role-specific dashboard, flow, review, and report patterns

## Where this is used

The Agentic Cherry UI Builder should pass this preset when it asks Open Design to generate or revise screens:

```json
{
  "designSystem": "lifehub-agentic-cherry",
  "designMode": "match-existing-app",
  "source": "agentic-cherry-ui-builder",
  "handoffTarget": "AC-WF parallel agents"
}
```

## Files

| File | Purpose |
|---|---|
| `tokens.json` | Brand and UI tokens for colors, typography, radius, shadows, spacing, and states |
| `components.md` | Component rules for buttons, cards, inputs, role cards, flow screens, dashboards, and Open Design controls |
| `layout-patterns.md` | Screen and page patterns to use for generated previews |
| `prompt-rules.md` | Prompt constraints that keep Open Design output app-matching and agent-ready |
| `examples/feature-wizard-open-design-prompt.md` | Example prompt from the UI Builder Wizard into Open Design |

## Non-negotiables

1. Keep the original simple user-flow builder style when representing flow data: `User -> Screen 1 -> Screen 2 -> + Add screen`.
2. Do not ask the user for low-level design details on the flow page. Infer details later from the simple flow text.
3. Treat the approved Open Design preview as visual direction, not production code to paste directly.
4. Include loading, empty, populated, error, permission-blocked, and success states in the design brief.
5. Generate outputs that development agents can turn into `DESIGN-SPEC.md`, `USER-FLOWS.md`, `DATA-CONTRACT.md`, `RBAC-CHECKLIST.md`, `ACCEPTANCE-CRITERIA.md`, and `TASKS.md`.
