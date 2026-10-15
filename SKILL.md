---
name: lulu-dialogue-skills
description: >-
  Dialogue-mode skill pack: on-demand conversation tools that do not own
  delivery. Routes to plain / gist / explain / ground / sample / verify / walk /
  grill / clash / converge / cut. Use when:
  lulu-dialogue-skills, dialogue skills, 对话技能, /plain, /gist, /explain,
  /ground, /sample, /verify, /walk, /grill, /clash, /converge, /cut,
  白话, 实现接地, 强制接地, 太虚, 要点, 一眼抓住, 解释一下, 解释清楚,
  逐题收敛, 碰撞, 砍一刀, 逐题讲解, 带着我按图听, 追问到底, 举例, 给个样例,
  验证一下, 求证.
argument-hint: "[plain | gist | explain | ground | sample | verify | walk | grill | clash | converge | cut]"
---

# lulu-dialogue-skills

On-demand **dialogue** skills — conversation tools that help explain one object,
ground one implementation question in inspectable evidence, show a concrete
instance, settle an inferred claim, walk one object as a confirmed node list,
clarify, compress, stress-test, converge a disposition queue, cut problem
boundaries, or pursue one Goal.

## Scope

- Route to a sub-SKILL and follow that file.
- Do **not** invent delivery stages or document sources of truth here.
- Each sub-SKILL's Activation states its own start rule. `converge`, `walk`,
  `grill`, and `verify` start only on the user's request or agreement; the
  assistant may ask for agreement. The other seven also start when their own
  condition holds.
- At most one sub-SKILL starts on the assistant's own initiative per reply (a
  proposal counts); a proposal the user declined is not repeated.
- This orchestrator routes only when the user names a key or an unambiguous
  intent; self-start conditions live in each sub-SKILL.

## Sub-SKILL Routing

When the user provides a key, slash command, or clear intent, route to the
corresponding sub-SKILL — then follow that `SKILL.md` only.

| Key | Sub-SKILL | Action |
|-----|-----------|--------|
| `plain` / `/plain` / 白话 / 说人话 | Plain language | Read [plain/SKILL.md](./plain/SKILL.md) |
| `gist` / `/gist` / 要点 / 一眼抓住 | Bottom line up front | Read [gist/SKILL.md](./gist/SKILL.md) |
| `explain` / `/explain` / 解释一下 / 解释清楚 | Domain-novice understanding of one object | Read [explain/SKILL.md](./explain/SKILL.md) |
| `ground` / `/ground` / 实现接地 / 强制接地 / 太虚 | Fresh implementation evidence | Read [ground/SKILL.md](./ground/SKILL.md) |
| `sample` / `/sample` / 举例 / 给个样例 | One concrete instance first; leans toward grounding | Read [sample/SKILL.md](./sample/SKILL.md) |
| `verify` / `/verify` / 验证一下 / 求证 | Settle one inferred claim by authoritative source or hands-on check | Read [verify/SKILL.md](./verify/SKILL.md) |
| `walk` / `/walk` / 逐题讲解 / 带着我按图听 | Confirmed node list; one node per turn | Read [walk/SKILL.md](./walk/SKILL.md) |
| `grill` / `/grill` / 追问到底 / 持续追问 | Pursue one Goal through focused questions | Read [grill/SKILL.md](./grill/SKILL.md) |
| `clash` / `/clash` / 碰撞 | Equal-footing collision | Read [clash/SKILL.md](./clash/SKILL.md) |
| `converge` / `/converge` / 逐题收敛 / 收敛 | Disposition queue (confirm/fork/resolve/dispose) | Read [converge/SKILL.md](./converge/SKILL.md) |
| `cut` / `/cut` / 砍一刀 | Boundary surgery | Read [cut/SKILL.md](./cut/SKILL.md) |

If the key is missing or ambiguous: route to `explain` only when its Activation
allows self-activate; otherwise list the eleven keys in one short line and ask
which to run — do not guess.

## Done

Observable completion is defined by the active sub-SKILL (not this file).

## Out of scope

- Conversation orchestration only.
- Does not own delivery stages or persist results unless the user asks.
