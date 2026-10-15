---
name: verify
description: >-
  Settle one load-bearing inference through an authoritative source or a
  hands-on check; a claim neither can settle stays marked as inference. Manual
  via /verify; the assistant may propose it and runs it only after the user
  agrees. Use when: /verify, 验证一下, 验证这个判断, 求证.
argument-hint: "<Claim>"
---

# verify

Turn one inferred claim into a settled one. Done when the claim is confirmed or
refuted on a basis the user can inspect, or is left as inference with the reason.

## Scope

One claim; the user's words and the conversation supply its context.

1. Missing or unrestatable claim → ask once and stop.

## Settling

A claim is settled only by:

1. **Authoritative source** — an original source for this claim, read at a cited
   location and version, that could have contradicted it. A source that cannot
   speak to the claim in this version or environment does not count.
2. **Hands-on check** — a result produced by the object under test itself, from a
   script, command, or experiment, that could have gone against the claim.

The basis prefers an authoritative source over a hands-on check. Blogs, forums,
search snippets, other assistants' answers, and recollection are leads, never a
basis.

## Result

1. Settled: ✅ confirmed or refuted, with the basis — the source (location,
   version, why it could contradict) or the check (what ran, expected,
   observed).
2. Unsettled: ⚠️ inference, with the leads, why no authoritative source and no
   hands-on check was available (a check the user declined is unavailable), and
   what would settle it. Reachable only after both were attempted.

## Consent

The user's agreement bounds what runs.

1. User invocation covers checks without lasting side effects.
2. The assistant may propose `/verify` when a claim is load-bearing and only
   inferred; the proposal lets the user judge what will happen before agreeing.
   Agreement covers what the proposal named.
3. A check leaves no lasting side effect — project files, external state,
   deletion, spending, scratch files — beyond what the user agreed to.

## Activation

Manual, or propose.

1. **Manual:** `/verify <Claim>`, 验证一下, 求证, or an explicit request to verify
   one claim.
2. **Propose:** a claim is load-bearing (a later conclusion, decision, or action
   rests on it) and only inferred. Run only after the user agrees; without
   agreement the claim stays marked as inference.

## Done

The user can inspect the basis of the result and tell settled from inferred.

## Out of scope

1. Code claims are settled by the code itself; `/ground` is not invoked.
2. Does not persist the result unless the user asks.
