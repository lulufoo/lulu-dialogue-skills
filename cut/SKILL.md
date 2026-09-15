---
name: cut
description: >-
  On-demand boundary surgery for stuck complex problems: lock a certain premise,
  carve out what is out of scope this round, collapse one axis, split now vs
  later, or refuse a dangling delivery dependency — so the remaining problem
  becomes workable. One cut per turn; does not solve the domain problem, run a
  converge queue, or persist. MANUAL TRIGGER ONLY. Use when: /cut, cut, 砍一刀,
  boundary surgery, narrow the scope, lock this premise, carve out.
---

# cut

Boundary surgery on a problem that is too large or stuck. Change the **working
boundary** so what remains is actionable — do not expand options, collide with
status quo, or walk a disposition queue.

## Cognition

### What it does

`cut` performs **boundary surgery**: lock a premise, carve out topics for this
round, freeze one axis among several, split “this round” from “later / TODO”,
or refuse a dangling dependency that would leave a delivery incomplete. Each
confirmed cut **changes the boundary** so the residual problem can be worked.

### What problem it solves

Stuck complexity is often not missing material — it is floating premises,
distracting branches, or entangled axes. `cut` first **narrows or nails** the
boundary; expansion and option-picking come after.

| Symptom | Cut provides |
|---------|--------------|
| Shared premise never written down; debate reopens it | Binding premise sentence |
| Branches the user does not want still dominate attention | Explicit carve-out |
| Several axes tangled; cannot start | Collapse one axis first |
| One blob cannot be scheduled | Split “this round” vs “later / TODO” |
| Implicit external dependency blocks a self-contained delivery | Refuse dangling dep (cite only if bundled) |

### What it is not

**cut = change the boundary.** It is not brainstorming, not status-quo collision
(`clash`), not one-by-one option locking (`converge`), and not writing a domain
solution.

## Principles

1. **Manual only** — activate only on `/cut`, 砍一刀, or an explicit cut request;
   never self-activate.
2. **One cut per turn** — propose and confirm exactly one cut per turn; queue
   further cuts.
3. **Cut changes the boundary** — every cut must yield a citable boundary-change
   sentence (lock / carve-out / collapse / split / refuse-dep).
4. **Grounded cuts only** — the cut must rest on user-explicit or already-agreed
   grounds; no empty “let’s simplify” talk.
5. **Reversible on record** — state how to unbind or reopen so a wrong cut is not
   silently permanent.
6. **Simplify, don’t solve** — shrink the problem space only; do not replace
   domain skills or choose the solution for the user.
7. **Hand back, don’t file** — return the result to the user; do not write files,
   todos, or archives unless the user explicitly authorizes that write.

## Vs siblings

| Skill | Action |
|-------|--------|
| `clash` | **Collide** — expose friction between expectation and status quo |
| `cut` | **Cut** — change the problem boundary |
| `converge` | **Converge** — lock surfaced options one question at a time |
| `gist` / `plain` | Expression density / wording — do not change boundaries |
| brainstorm | Diverge and add options — opposite direction from `cut` |

## Activation

- **Manual only** (`/cut`, `cut`, 砍一刀, or an explicit request for boundary
  surgery / scope cut).
- **Never self-activate.**
- Default: one cut per turn; continue only if the user asks for another cut or
  confirms the next queued cut.

## Cut types

| type | Meaning |
|------|---------|
| `lock-premise` | Nail a premise that is already certain |
| `carve-out` | Explicitly exclude what this round will not discuss or do |
| `collapse-axis` | Among several axes, freeze one first |
| `split` | Split into “this round” vs “later / TODO” |
| `refuse-dangling-dep` | Refuse an external dependency outside the delivery unless it is bundled |

Every proposed cut **must** name exactly one `type` from this table.

## Turn shape

1. Briefly restate, in the user’s terms, what is too large or stuck.
2. Propose **exactly one** cut:
   - `type`
   - boundary-change sentence
   - grounds (user-explicit or already agreed)
   - what follows from the cut / what is explicitly out
   - how to unbind or reopen
3. Wait for confirm / revise / reject.
4. On confirm: one-line lock ack; ask whether to cut again, hand off to
   `/converge`, or return to a domain skill.
5. Without confirm, do **not** pretend the boundary has changed.

## Done

Observable completion when **all** of the following hold:

- At least one cut was confirmed by the user; and
- The chat shows: boundary-change sentence, scope of effect, follow-ons, explicit
  out-of-scope list, and unbind hint.

If the user aborts or confirms zero cuts: state that cut did not complete — do
not claim the problem was simplified.

## Out of scope

- Does not discover exposure lists (upstream: `/clash` or ordinary talk).
- Does not run a `converge` queue or choose among options for the user.
- Does not own a delivery stage or decide the domain solution.
- Does not auto-edit the repo, todos, or archives.
- No `scripts/` in v1 — conversation orchestration only.

## Handoff

| Next | When |
|------|------|
| `/converge` | After cuts, remaining items are disposition options |
| Domain skill | Boundary is workable for deep dive or implementation |
| Another `/cut` | Still too large; queue the next cut |
