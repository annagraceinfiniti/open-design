# Example: Agentic Cherry Feature Wizard → Open Design

This is the shape of prompt Agentic Cherry should send to Open Design after the user completes:

```txt
Idea → Users → Flow → Open Design Studio
```

## Request

```json
{
  "designSystem": "lifehub-agentic-cherry",
  "designMode": "match-existing-app",
  "featureName": "Learner Progress Review Hub",
  "idea": "Create a role-based feature where learners can see their task progress and next step, Learner Support can review or grade submitted work, and Organization Admins can configure settings and view progress from one dashboard.",
  "users": [
    "Learner",
    "Learner Support",
    "Organization Admin",
    "Fini",
    "Infiniti"
  ],
  "flowScreens": [
    {
      "userType": "Learner",
      "screenIndex": 1,
      "action": "Learner lands on the feature, sees the task or next step, and understands what to do."
    },
    {
      "userType": "Learner",
      "screenIndex": 2,
      "action": "Learner completes the action, gets help from Fini if needed, submits, and sees confirmation."
    },
    {
      "userType": "Learner Support",
      "screenIndex": 1,
      "action": "Learner Support opens a queue of submitted learner work that needs review, grading, or feedback."
    },
    {
      "userType": "Organization Admin",
      "screenIndex": 1,
      "action": "Org Admin opens a dashboard to monitor progress, settings, exceptions, and reporting."
    }
  ],
  "designSystemOptions": {
    "style": "Match existing app exactly",
    "scope": "All screens",
    "iterationPreset": "Create first design",
    "customInstruction": "Keep the learner screens simple and make the admin screens more like a review dashboard."
  },
  "requiredStates": [
    "loading",
    "empty",
    "populated",
    "error",
    "permission-blocked",
    "success"
  ],
  "handoffTarget": "AC-WF parallel agents"
}
```

## Expected Open Design behavior

Open Design should:

1. Use the Life Hub / Agentic Cherry design system.
2. Generate screens that match the existing app.
3. Preserve the user-flow sequence and role separation.
4. Infer components, layout, data, states, and permissions from the plain-English screen text.
5. Return a preview plus a structured design brief that agents can convert into implementation tasks.

## Expected design brief sections

```txt
Feature summary
Roles and permissions
Screen-by-screen design spec
UI states
Likely components
Likely data needs
Open questions
Agent handoff notes
```
