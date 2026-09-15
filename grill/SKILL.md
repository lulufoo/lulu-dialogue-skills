---
name: grill
description: >-
  Pursue one user-given Goal through focused, one-at-a-time questions until the
  Goal is achieved, objectively blocked, or the user stops. Conversation-only;
  never self-activates or invents a separate completion contract. Use when:
  /grill, grill this, 追问到底, 持续追问, 围绕这个目标问清楚.
argument-hint: "<Goal>"
---

# grill

Pursue one Goal through focused questions. Complete when the Goal is achieved,
blocked by unavailable information, or aborted by the user.

## Activation

1. Activate on `/grill` or an unambiguous request for sustained questioning
   toward one Goal.
2. Never self-activate from a merely unclear or incomplete conversation.
3. Missing Goal → ask for it and stop. Ambiguous Goal → ask one focused
   clarification; continue only when the Goal is restatable.

## Session

1. Pin the Goal and the current result assembled from the conversation.
2. Assess what still prevents the current result from achieving the Goal.
3. Use relevant available evidence before asking; do not ask the user for facts
   that can be inspected.
4. If the Goal is not yet achieved, choose one material gap and ask exactly one
   focused question.
5. Integrate the answer into the current result and reassess the Goal. Repeat
   without fixing a question order or simulating an exhaustive decision tree.
6. A corrected Goal replaces the pinned Goal; reassess the accumulated result
   against it.

## Exit

Assign exactly one exit:

| Exit | When |
|------|------|
| `achieved` | The assembled result fulfills the Goal; further questioning would not materially improve it. |
| `blocked` | A material gap depends on information that neither the environment nor the user can currently provide. |
| `aborted` | The user stops the session. |

Stop immediately on `blocked` or `aborted`; do not manufacture closure.

## Result

Return a compact card:

```text
Goal:
Result:
Exit: achieved | blocked | aborted
Unresolved:
```

Default to chat only. Persist the result only when the user explicitly requests
a destination.

## Boundaries

1. `grill` owns one Goal. It does not diagnose a problem.
2. It does not diagnose bugs, run a disposition queue, own a workflow stage, or
   execute the result.
3. Conversation-only in v1; no persistence state or scripts.
