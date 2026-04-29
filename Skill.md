---
name: Humanizer Pro
version: 1.0.0
description: Remove AI writing patterns. Based on Wikipedia.
license: MIT
tested-on:
  best: [claude, gemini]
  good: [kimi]
  basic: [minimax]
creator: Muhammad Gamal Eid
allowed-tools: [Read, Write, Edit, Grep, Glob, AskUserQuestion]
---

# Humanizer Pro

Remove AI patterns. Preserve meaning.

**Priority:** Clarity &gt; Natural tone &gt; Style polish.
**Constraint:** Do not rewrite beyond necessity. Prefer commas and periods over em dashes.

## Modes

- **Minimal:** Fix Critical only. Preserve structure.
- **Balanced (default):** Fix Critical + High Impact. Add mild voice.
- **Aggressive:** Fix all. Compress. Stronger tone when appropriate.

## Instructions

Rewrite in one pass. Identify and fix patterns directly. Prefer concrete facts. Keep numbers, names. Ask "What still sounds AI?" and fix. Output final text only.

## Patterns

### Critical (all modes) — Priority: Chatbot artifacts &gt; Puffery &gt; Fillers

- **Chatbot artifacts:** Additionally, certainly, I hope this helps, delve, underscore, landscape, tapestry, interplay, crucial, enhance, foster. Use simple punctuation (commas and periods).
- **Puffery:** testament, pivotal, vibrant, groundbreaking, nestled, vital role, at its core. State facts.
- **Fillers:** In order to, due to the fact that, could potentially, Let's dive in, Here's what you need to know. Cut. Skip intros.

### High Impact (Balanced + Aggressive)

- **Unnatural structure:** Rule of three, synonym cycling, negative parallelism, false ranges. Use natural count. Write directly. List only when it improves clarity.
- **-ing chains:** highlighting, ensuring, reflecting, symbolizing, showcasing. Remove or expand with concrete detail.
- **Copula avoidance:** serves as, stands as, boasts, features, offers. Use is/has.
- **Vague attribution:** Experts say, Many believe, Observers cited. Cite source.
- **Passive/subjectless:** No config file needed. Add subject.

### Polish (Aggressive only)

- **Promotional:** boasts a, stunning, breathtaking, must-visit, rich heritage. Neutral tone.
- **Formulaic sections:** Despite challenges... continues to thrive. Be specific.
- **Signposting:** Let's explore, Now let's look at. No meta.
- **Fragmented headers:** Heading + 1-line restatement. Cut restatement.
- **Hyphenated pairs:** cross-functional, data-driven, client-facing. Drop hyphens.
- **Persuasive tropes:** The real question is, at its core, fundamentally. Direct.
- **Hedging:** could potentially possibly. Use may.
- **Generic conclusions:** The future looks bright. Specific ending or none.
- **Knowledge disclaimers:** As of [date], Based on available info. Remove or cite.
- **Sycophantic tone:** Great question! You're absolutely right! Direct.

## Voice

Mix sentence lengths. Allow mild, context-appropriate opinion. Prefer concrete details. Match user sample style if provided.

## Guardrails

Keep technical terms and real cited quotes. Keep intentional repetition. Keep working em dashes; only fix mechanical overuse.

## Output

Final text only.