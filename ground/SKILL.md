---
name: ground
description: >-
  Make one implementation-related question concrete through fresh project
  evidence or an explicit proposed implementation shape. MANUAL ONLY. Use when:
  /ground, 实现接地, 强制接地, 太虚, 代码层面, 当前实现, 目标实现,
  改完是什么样.
argument-hint: "<Question>"
---

# ground

Ground one implementation-related question in the project. Complete when its
material claims are inspectable in implementation evidence.

## Scope

One question; the user's words and current conversation supply its context.

1. Infer what the user wants grounded; do not require or expose modes.
2. Pin the implementation object before inspecting evidence.
3. Missing or unrestatable object → ask once and stop.

## Evidence

Use the smallest implementation view that makes the answer checkable.

1. Re-read relevant project sources at invocation. Prior dialogue is a lead,
   not evidence of current behavior.
2. Choose evidence by the question: code, symbols, call relations, schemas,
   resulting file structure, interfaces, or tests.
3. Prefer an existing project precedent when expressing a proposed shape.
4. Separate verified current behavior, proposed shape, and unresolved facts.
5. If fresh evidence invalidates an earlier claim, surface the invalidation.

## Result

Answer the user's question directly; structure follows the evidence.

1. Anchor every material implementation claim to a project location or mark it
   unresolved.
2. For a proposed result, show enough post-change shape to inspect the claim;
   do not imply that proposed code already exists.
3. For a comparison, ground both sides before stating the difference.
4. Stop when the implementation claim is recoverable; omit decorative code.

## Activation

Manual only: `/ground <Question>`, 太虚, 强制接地, or an explicit request
to ground one implementation question. Do not self-activate from ordinary
design discussion.

## Done

The user can inspect the implementation basis of the answer and distinguish
current fact from proposal and unresolved matter.

## Boundaries

1. Conversation-only and read-only; no edits, persistence, scripts, or session
   state.
2. Does not decide open design choices, produce a plan, implement a change, or
   review completed code.
