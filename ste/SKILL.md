---
name: ste
description: >-
  Express the current point in ASD-STE100 controlled form: one idea per
  sentence, short sentences, active voice, one fixed term per concept, lists
  for complex content. English replies apply the writing rules and the
  dictionary at about 80%; Chinese replies apply the writing rules only.
  Starts only on `/ste` or an explicit request. Use when: /ste, ste, STE,
  ASD-STE100, 受控语言, 简明技术英语.
---

# ste

Express the current point in ASD-STE100 controlled form so the reader parses
each sentence once. Done when every sentence and paragraph meets the Form rules.

## Scope

Form of the active reply only.

1. Default: the next reply. "Keep it on" (or equivalent) → until the user turns it off.
2. Another dialogue skill also active → this skill owns sentence and paragraph form only; the other skill keeps its reply shape.

## Form rules

Language-independent subset of the ASD-STE100 writing rules.

1. One idea per sentence; one instruction per sentence.
2. Instruction ≤ 20 words; description ≤ 25 words; Chinese ≤ 30 characters.
3. Active voice; simple tenses; subject and verb stated.
4. One concept, one term; do not switch synonyms across the reply.
5. One topic per paragraph; ≤ 6 sentences per paragraph.
6. Complex content goes to a vertical list, one item per line.
7. Noun strings ≤ 3 words.

## Language

How the dictionary applies.

1. English reply: apply the approved-word dictionary at about 80%; technical nouns and verbs of the subject stay, as the standard allows.
2. Chinese reply: apply the Form rules only; the dictionary does not apply.
3. Code identifiers, commands, and quoted sources are not rewritten.

## Vs siblings

| Skill | Owns |
|-------|------|
| `ste` | Form — sentence and paragraph shape |
| `gist` | Density — bottom line first |
| `plain` | Accessibility — term table, first-time inheritor |
| `explain` | Domain-novice understanding of one object, then stop |

## Activation

Starts only on the user's request: `/ste`, STE, 受控语言, or an explicit request for ASD-STE100 form. Does not self-activate.

## Done

Every sentence and paragraph meets the Form rules; the dictionary is applied per Language; the meaning of the content is unchanged.

## Out of scope

1. Does not compress content (`/gist`) or add a term table (`/plain`).
2. Does not change any non-conversation output (docs, code, artifacts).
