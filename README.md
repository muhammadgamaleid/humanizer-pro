# Humanizer Pro

[![Version](https://img.shields.io/badge/version-1.1.0-blue)](https://github.com/muhammadgamaleid/humanizer-pro)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Tokens](https://img.shields.io/badge/tokens-~800--900-blue)](#comparison)
[![Tested on](https://img.shields.io/badge/tested%20on-Claude%20%7C%20Gemini%20%7C%20Kimi%20%7C%20MiniMax-purple)](#compatibility)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-supported-informational)](#integrations)

> One-pass humanizer for AI-generated text. No drafts. No noise. Consistent results.

---

## What it does

Paste AI-generated text and get a cleaner, more natural version in one step.
No drafts, no explanations, no extra output—just the final result.

Designed for people who work with AI text daily and want something reliable without wasting context window space.

Optimized for English, with limited support for other languages.

---

## Why this exists

Most “humanizer” prompts break down in real use:

* **Too long** — 3,000–6,000+ tokens that consume context
* **Too many steps** — draft → audit → final
* **Unstable** — same input, different output across models
* **Too noisy** — explanations and meta output you didn’t ask for

This solves those issues with a focused, pattern-based approach.

---

## Key features

* **One pass + self-check** — fixes what matters without extra output
* **~800–900 tokens** — compact without losing clarity
* **Final output only** — no summaries, no greetings, no logs
* **Controlled editing** — preserves meaning, technical terms, and intent
* **Cross-model consistency** — works reliably across major LLMs

---

## Example

### Before

> The new software update serves as a testament to the company's commitment to innovation. Moreover, it provides a seamless, intuitive, and powerful user experience—ensuring that users can accomplish their goals efficiently.

### After

> The software update adds batch processing, keyboard shortcuts, and offline mode. Users report faster task completion.

---

## Comparison

Estimates based on publicly available prompt sizes and common usage patterns.

|                           | Humanizer Pro  | blader/humanizer      | Typical Prompts |
| ------------------------- | -------------- | --------------------- | --------------- |
| **Tokens**                | ~800–900       | ~5,000+               | 1,500–3,000+    |
| **Token reduction**       | ~6–7x smaller  | —                     | —               |
| **Passes**                | 1 + self-check | 2 (draft + final)     | Varies          |
| **Output**                | Final only     | Draft + audit + final | Verbose         |
| **Consistency**           | High           | Medium                | Low             |
| **Cross-model stability** | Stable         | Claude-focused        | Inconsistent    |

---

## Integrations

Works as a reusable skill or system-level instruction.

### Claude Code

```bash
mkdir -p ~/.claude/skills/humanizer-pro
cp SKILL.md ~/.claude/skills/humanizer-pro/
```

```bash
git clone https://github.com/muhammadgamaleid/humanizer-pro.git ~/.claude/skills/humanizer-pro
```

Usage:

```
/humanizer-pro
[paste your text]
```

---

### OpenCode

```bash
mkdir -p ~/.config/opencode/skills/humanizer-pro
cp SKILL.md ~/.config/opencode/skills/humanizer-pro/
```

```bash
git clone https://github.com/muhammadgamaleid/humanizer-pro.git ~/.config/opencode/skills/humanizer-pro
```

Usage:

```
/humanizer-pro
[paste your text]
```

---

### Any LLM

1. Copy `SKILL.md`
2. Paste into system prompt or custom instructions
3. Send your text normally

---

## Compatibility

| Model   | Performance |
| ------- | ----------- |
| Claude  | Best        |
| Gemini  | Best        |
| Kimi    | Good        |
| MiniMax | Basic       |

---

## Legal

Not affiliated with or endorsed by any of the above platforms.

---

## Philosophy

80% of results come from fixing 20% of patterns.

---

## Author

Muhammad Gamal Eid

---
## License

MIT
