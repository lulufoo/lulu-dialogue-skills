---
name: explain
description: >-
  Give a domain novice the smallest explanation of one named thing or concept
  that still produces understanding — then stop. Triggers: `/explain` or an
  explicit request to 解释一下 / 解释清楚 a named object. Self-activate when one
  object is named and a full reply would sprawl — not on a missing object or a
  too-large object. Use when: /explain, explain, 解释一下, 解释清楚.
---

# explain

Treat the reader as new to this object's field. Done when they understand the
object from this reply and no further layer was opened.

## Scope

One named object; a domain novice; this reply only.

1. Default: the next reply. "Keep it on" (or equivalent) → until the user turns it off.
2. Missing object → ask once what to explain and stop.
3. Another dialogue skill also active → this skill owns the explanation; `/plain` owns wording; `/gist` owns density.

## Audience

The reader has no field knowledge of this object.

1. Do not assume prior terms, mechanisms, or jargon of the field.
2. Introduce a term only if a must-hold fails without it.
3. Followable wording alone is not done — that is `/plain`. Done is understanding.

## Must hold

What a domain novice must be able to recover. Not a thinking order.

1. **Object** — nail the one thing being explained, in the user's name for it.
2. **What it is** — one stand-alone sentence that bounds the object.
3. **Principle** — the one degree of freedom it actually governs, or what it stands on.
4. **Key points** — only what would change use or judgment; drop the rest.
5. **Stop** — no background, history, comparison, or next layer unless the bound is unsafe without one caveat.

## Too large

When a domain novice cannot understand from one reply without walking layers.

1. Say the object is too large for `/explain`.
2. Hand back `/walk` or `/cut`. Do not start either.

## Vs siblings

Contrast with `/plain`.

| Skill | Owns |
|-------|------|
| `explain` | Domain-novice understanding of one object; minimal; then stop |
| `plain` | Wording — first-time inheritor, no prior context |

If `/plain` is also on: `explain` owns understanding; `plain` owns wording only.

## Activation

Manual, or narrow self-activate.

1. **Manual:** `/explain`, 解释一下, 解释清楚, or an explicit request to explain one named object.
2. **Self-activate:** one object is named and a full reply would sprawl — open in this reply; do not ask first.
3. **Do not self-activate:** missing object (ask once and stop); too large (hand back `/walk` or `/cut`; do not start either).

## Done

A domain novice can understand the object from this reply; all must-holds
hold; no further layer was opened.

## Out of scope

Still-possible mix-ups on this path.

1. Does not start `/walk` or keep a walk node list.
2. Does not replace `/plain` or `/gist`.
3. Does not change any non-conversation output (docs, code, artifacts).
