---
name: converge
description: >-
  Walk a disposition queue one question at a time (confirm / fork / resolve /
  dispose / unclassified). Each turn shows type, i/n, options, and lean; no
  advance until answered; ends with a decision table and exit gate. MANUAL
  ONLY. Use when: /converge, 逐题收敛, 收敛, 逐个问题, one question at a time,
  option walk, disposition queue.
---

# converge

Walk a **disposition queue** one at a time: options + stated lean; lock then
next; finish with a table and exit gate.

## Purpose

1. Turn surfaced disposition items into a completed choice table.
2. One live question per turn; show lean without choosing for the user.
3. Prefer **coarse-first**; discovery stays upstream (`/clash` or prior talk).

## Activation

- **Manual only** (`/converge`, `逐题收敛`, or explicit one-by-one option walk).
- **Never self-activate.**
- Runs until queue done, user aborts, or user says stop.

## Queue

| type | Meaning |
|------|---------|
| `confirm` | Binding confirmation |
| `fork` | Fork / option choice |
| `resolve` | Contradiction resolution |
| `dispose` | Gap disposition (fill / defer / out-of-scope) |
| `unclassified` | Holding bay — not a stable fifth type |

- Each item also has `grain`: `coarse` | `fine` (orthogonal to type).
- Default order: **coarse → fine**; type does not set primary order.
- `unclassified`: AI may propose; must state why not one of the four; **user
  must confirm** before enqueue; no bare / unsourced `unclassified`.
- Not disposition and no consequence → do not enqueue.
- Types are labels, not a coarse→fine ladder.

## Inputs

Resolve the queue, in order:

1. Explicit list the user pastes or numbers (types optional; label then confirm).
2. Already-stated open questions **or** already-surfaced gaps/contradictions /
   binding premises in this conversation — rewrite into typed items, quote the
   full queue, **confirm with user**, then Q1.
3. If neither — ask once for the list; **do not invent** items or exposures.

## Hard rules

1. **One main question per turn** — no unrelated bundles.
2. **Options required** — A/B/C… (or yes/no/rewrite; fill/defer/oos); one-line
   meaning each.
3. **Preference required** — exactly one `I lean: <option>` + short why.
4. **No advance without an answer** — hedge → clarify this item; do not skip.
5. **Sub-question OK** — required follow-up is the live question; then return.
6. **Record then proceed** — one-line lock ack, then next (same shape).
7. **No silent file writes** — table in chat; persist only if user asks.

## Turn shape (live question)

1. One-line recap of last lock (omit on Q1).
2. `type: <…>` and position `i/n` (sub-question: `i/n · sub`).
3. Plain question (what must be true after we choose).
4. Option table.
5. `I lean: <X>` + one short reason.
6. Single ask: which option? (or precise sub-question)

If `/plain` is also on: `converge` owns the queue; `plain` owns wording only.

## Done

When the queue is empty (or user stops early):

1. Table: `#` · `type` · `grain` · question (short) · choice · notes.
2. List skipped / still-open explicitly.
3. If any `unclassified` → one line: whether to adjust the four-type set.
4. **Exit gate**: locked / proceed-with-open / hard-block.
5. Stop — do not start implementation unless the user asks.

Observable completion: the chat table covers every queued item as chosen,
skipped, or still-open, plus exit gate.

## Out of scope

- Does not replace domain or delivery skills.
- Does not discover or invent exposures; no auto-scan of past `/clash` into a
  queue; no clash→queue pipeline.
- Does not decide for the user or pressure the lean.
- Does not redefine `/plain` or `/clash`.
- No `scripts/` in v1 — conversation-only orchestration.
