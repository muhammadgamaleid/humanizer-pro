---
name: Humanizer Pro
version: 1.1.0
description: Remove common AI writing patterns in one pass using a structured approach.
license: MIT
tested-on:
  best: [claude, gemini]
  good: [kimi]
  basic: [minimax]
creator: Muhammad Gamal Eid
language: English-first, multilingual compatible
allowed-tools: [Read, Write, Edit, Grep, Glob]
---

# Humanizer Pro

Remove AI patterns. Preserve meaning.

**Priority:** Clarity &gt; Natural tone &gt; Style polish.
**Constraint:** Do not rewrite beyond necessity. Preserve original meaning and structure where possible.

## Modes

- **Minimal:** Fix Critical only. Preserve structure.
- **Balanced (default):** Fix Critical + High Impact. Add mild voice.
- **Aggressive:** Fix all. Compress. Stronger tone when appropriate.

**When to use:**
- Use **Balanced** for professional writing and general use.
- Use **Aggressive** for marketing, blogs, or opinionated content.

## Instructions

Rewrite in one pass. Identify and fix patterns directly. Prefer concrete facts. Keep numbers, names. Self-check: "What still sounds AI?" Fix without announcing. Output final text only.

## Patterns

### Critical (all modes) — Priority: Chatbot artifacts &gt; Puffery &gt; Fillers

- **Chatbot artifacts:** Additionally, certainly, I hope this helps, delve, underscore, landscape, tapestry, interplay, crucial, enhance, foster. Prefer simple punctuation when it improves clarity.
- **Puffery:** testament, pivotal, vibrant, groundbreaking, nestled, vital role, at its core. State facts.
- **Fillers:** In order to, due to the fact that, could potentially, Let's dive in, Here's what you need to know. Cut. Skip intros.

### High Impact (Balanced + Aggressive)

- **Unnatural structure:** Rule of three, synonym cycling, negative parallelism, false ranges. Use natural count. Write directly. Use lists only if they reduce repetition or improve readability.
- **-ing chains:** highlighting, ensuring, reflecting, symbolizing, showcasing. Remove or expand with concrete detail.
- **Copula avoidance:** serves as, stands as, boasts, features, offers. Use is/has.
- **Vague attribution:** Experts say, Many believe, Observers cited. Cite source only if in input; otherwise remove.
- **Passive/subjectless:** No config file needed. Add a clear subject to the sentence.

### Polish (Aggressive only)

- **Promotional:** boasts a, stunning, breathtaking, must-visit, rich heritage. Neutral tone.
- **Formulaic sections:** Despite challenges... continues to thrive. Be specific.
- **Signposting:** Let's explore, Now let's look at. No meta.
- **Fragmented headers:** Heading + 1-line restatement. Cut restatement.
- **Hyphenated pairs:** cross-functional, data-driven, client-facing. Drop unnecessary hyphens; keep standard compound forms.
- **Persuasive tropes:** The real question is, at its core, fundamentally. Direct.
- **Hedging:** could potentially possibly. Use may.
- **Generic conclusions:** The future looks bright. Specific ending or none.
- **Knowledge disclaimers:** As of [date], Based on available info. Remove. Cite only if source in input.
- **Sycophantic tone:** Great question! You're absolutely right! Direct.

## Voice

Mix sentence lengths. Allow mild, context-appropriate opinion only when the original text implies evaluation, uncertainty, or personal stance. Match user sample style if provided.

For non-English text, apply equivalent patterns when they exist; otherwise prioritize clarity and natural phrasing.

## Guardrails

Keep technical terms and real cited quotes. Keep intentional repetition. Keep working em dashes; only fix mechanical overuse.

## Output

Final text only.

---
## Example

### Before
&gt; The platform serves as a testament to innovation, highlighting its pivotal role in enhancing user productivity across various workflows.

### After
&gt; The platform improves productivity across workflows and makes everyday tasks faster.
