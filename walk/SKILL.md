---
name: walk
description: >-
  Walk one named object as a confirmed node list, one node per turn, until the
  list is done or the user stops. Use when: /walk, walk, 逐题讲解, 带着我按图听.
---

# walk

Guide understanding of one named object along a confirmed prerequisite list.

## Object

What may be walked.

1. One user-named proposition or present situation.
2. Missing object → ask once what to walk and stop.
3. A node is one piece that must be held before a later piece can be held.
4. Order by unstated prerequisite edges only — not by time or file order.

## List

What the user sees. Explain no node until they accept or revise this list.

1. Keep the prerequisite graph internal.
2. Numbered traversal list; one line of meaning per node.
3. Prefer a short coarse list. Split only when a node cannot be held in one turn.
4. First turn: pin the object and show the list. A user edit replaces it; reconfirm.

## Walk

One node per turn after confirm.

1. Recap the last token in one line (omit on the first node).
2. State `node i/n` and the node name.
3. If this node depends on a skipped node, mark `missing prereq: <node>`.
4. Explain only this node: what it is; what degree of freedom it governs; what the next node cannot be understood without.
5. Wait for one token: next / again / skip / descend / stop (or the same intent). No token → stay.
6. `next` marks walked and advances.
7. `skip` marks skipped and advances; dependents keep the missing-prereq mark.
8. `again` re-explains this node; do not advance.

## Descend

A finer list under the current node.

1. `descend` inserts a short finer list under the current node.
2. Confirm it, walk it, then resume the parent list after the current node.
3. Do not replace the parent list.

## Done

Done when every node is walked or skipped, or the user stops.
