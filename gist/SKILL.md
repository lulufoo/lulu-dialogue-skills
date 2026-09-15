---
name: gist
description: >-
  On-demand gist mode: lead with one glanceable bottom line, then optional short
  support. Compresses expression density for causes, proposals, and concepts —
  does not deepen reasoning. MANUAL TRIGGER ONLY — never self-activate. User
  triggers with `/gist` (or an explicit request for the gist / 要点 / 一眼抓住).
  The assistant MAY recommend triggering it when the reply is long or the user
  asks to compress — but must ask first and only activate after the user agrees.
  Use when: /gist, gist, 要点, 一眼抓住, 结论先行, bottom line up front, BLUF.
---

# gist

Give the **gist** first: one glanceable bottom line, then only as much support as
needed. Governing principle: **Bottom Line Up Front** (结论先行).

## Purpose

1. Surface the essential point in one sentence the user can grab at a glance.
2. Keep support short and subordinate — never rewrite the bottom line.
3. Compress **expression**; do not pretend to deepen **reasoning**.

## Principle

**Bottom Line Up Front** — state a stand-alone one-sentence conclusion first;
expand only if needed; expansion must not change the conclusion.

## Vs siblings

| Skill | Owns |
|-------|------|
| `gist` | Density — conclusion first, glanceable |
| `plain` | Accessibility — first-time inheritor, no prior context |
| `explain` | Domain-novice understanding of one object — then stop |
| `clash` / `converge` | Collision / disposition queue |

If `/plain` is also on: `gist` owns structure (bottom line first); `plain` owns wording only.

## Activation

- **Manual:** `/gist`, 要点, 一眼抓住, or an explicit request for the gist / BLUF.
- **Recommend-only:** when a trigger signal appears (below), the assistant may add
  one line — "Want me to switch to `/gist`?" — and MUST wait for user confirmation.
- **Never self-activate.** Absent explicit user go-ahead, this mode stays off.

### Recommend signals (suggest, do not apply)

1. User asks to compress, summarize to the point, or "一眼抓住".
2. The natural answer would be long while the user needs a skim-first read.
3. User rejects a prior reply as too long / buried the point.

## Scope

- Applies to the **next reply only** by default.
- If the user says "keep it on" (or equivalent) → stays active until the user turns it off.
- Fits causes, proposals, concepts, and short status answers.

## Mandatory actions while active

1. **Lead with the bottom line** — exactly one sentence; must stand alone.
2. **Then optional support** — at most a few short bullets or one short block;
   each line must serve the bottom line.
3. **One fixed wording** for the core claim — do not rephrase the same conclusion
   across the reply.
4. **No padding** — omit background, history, and alternatives unless the user
   asked for them or the bottom line is unsafe without one caveat.
5. **Stop early** — if the bottom line is enough, do not expand.

## Out of scope

- Does NOT require first-principles decomposition or deeper analysis.
- Does NOT replace `/plain` (zero-context clarity) or verify-first labeling.
- Does NOT change any non-conversation output (docs, code, artifacts).
