---
name: make-knowledge-cards
description: "Turn pasted articles or local Markdown/TXT files into concise, source-faithful knowledge cards. Use when a user wants to study or review an article; not for web pages, PDFs, Anki exports, or graphical interfaces."
---

# Make Knowledge Cards

Convert one user-provided article into a small set of standalone study cards. The goal is useful recall, not a comprehensive summary.

## Input and scope

- Accept pasted article text, or a local `.md`, `.markdown`, or `.txt` file the user identifies. Read the local file before making cards.
- Do not fetch web content or handle PDFs. Do not create Anki packages, applications, or graphical interfaces; explain the boundary and offer Markdown cards instead when relevant.
- Treat headings, callouts, examples, and lists as source material, but do not infer facts that the source does not support.

## Distill the article

1. Identify the article's central claims, concepts, methods, distinctions, and constraints. Prefer ideas that are necessary to understand or apply the material.
2. Merge restatements and overlapping claims. Exclude decorative details, tangents, and weakly supported asides.
3. Make each card about exactly one knowledge point. Split cards that combine independent ideas; combine cards that merely repeat the same idea.
4. Aim for 5–8 cards only when the source has that many distinct, important ideas. Return fewer when it does not. Do not pad with generic advice, invented context, or trivial rewrites.
5. Preserve qualifications, uncertainty, and limits in the source. If a claim is unclear or information is insufficient, say so briefly or omit it rather than completing it from outside knowledge.

## Card format

Write in the user's language unless they request another one. Use Markdown with one numbered section per card:

```markdown
## 1. [Short, specific title]

**Core knowledge:** [One precise claim or concept from the source.]

**Explanation:** [A plain-language explanation that stays within the source.]

**Example / self-check:** [A source-grounded example, or one short question that tests recall or application.]
```

Use a self-check question when the article gives no reliable example. Keep it answerable from the card and source; do not imply missing facts. After the cards, optionally add a one-sentence note only when the source was too short, repetitive, or incomplete to support the usual range.
