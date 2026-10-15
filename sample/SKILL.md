---
name: sample
description: >-
  Lead with one concrete instance instead of abstract description; ground it in
  project evidence when the question touches implementation. MANUAL ONLY —
  never self-activate. Triggers: `/sample` or an explicit request for a sample.
  Use when: /sample, sample, 举例, 给个样例, 样例, 给个例子.
argument-hint: "<Object or Question>"
---

# sample

Show the thing itself before explaining it. Done when the reader sees one
concrete instance and can tell which parts rest on evidence and which are
illustrative.

## Scope

One object or question; this reply only.

1. Default: the next reply. "Keep it on" (or equivalent) → until the user turns it off.
2. Missing object → ask once what to sample and stop.
3. Another dialogue skill also active → this skill owns the instance; `/plain` owns wording; `/gist` owns density.

## Grounding

Decide per question whether the instance needs project evidence.

1. Judge whether the question touches project implementation: code, schema, interface, data shape, or file layout.
2. Lean toward grounding; when in doubt, ground.
3. Calling `/sample` is the user's explicit request to apply `/ground`; follow [ground/SKILL.md](../ground/SKILL.md) for Evidence and Result.
4. Grounded: take values from evidence. A value evidence cannot supply is marked unknown.
5. Not grounded (pure concept, no project object): the instance is illustrative; mark every invented value.
6. Grounding keeps `/ground` boundaries: conversation-only and read-only.

## Instance

What the reply carries.

1. Lead with one concrete instance — real data, a call, a file tree, or a before/after — before any rule.
2. Mark provenance per value or per block: evidence (with location) or illustrative.
3. After the instance, state only what the instance cannot show; one short table or list.
4. Stop when the reader can recover the shape.

## Vs siblings

| Skill | Owns |
|-------|------|
| `sample` | One concrete instance first; leans toward grounding |
| `ground` | Inspectable implementation evidence for one question |
| `explain` | Domain-novice understanding of one object |
| `plain` | Wording for a first-time inheritor |

If `/ground` is also invoked: its rules govern evidence; `sample` owns the instance-first shape.

## Activation

Manual only.

1. `/sample`, 举例, 给个样例, 样例, 给个例子, or an explicit request for a concrete instance.
2. No self-activation.

## Done

The reader sees a concrete instance, can tell evidence from illustration, and no unrelated layer was opened.

## Out of scope

1. Does not replace `/ground`, `/explain`, or `/plain`.
2. Does not change any non-conversation output (docs, code, artifacts).
3. Does not persist the instance unless the user asks.
