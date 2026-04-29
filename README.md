# Humanizer Pro

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Tokens](https://img.shields.io/badge/tokens-~750-blue)](#comparison)
[![One Pass](https://img.shields.io/badge/pass-1-green)](#key-features)
[![Output](https://img.shields.io/badge/output-final--only-black)](#key-features)
[![Tested on](https://img.shields.io/badge/tested%20on-Claude%20%7C%20Gemini%20%7C%20Kimi%20%7C%20MiniMax-purple)](#compatibility)
[![OpenCode](https://img.shields.io/badge/OpenCode-supported-informational)](#integrations)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-supported-informational)](#integrations)

> One-pass humanizer. No drafts. No noise. ~6–7x fewer tokens (750 vs 5,000+).

## What it does

Paste AI text. Get clean, human-sounding output in one shot. No intermediate drafts, no verbose explanations, no cleanup.

Built for people who edit a lot of generated text and need consistent results without burning context windows.

## Why this exists

Most humanizer prompts are too long, too slow, or too inconsistent:

- **Bloated** — 3,000–6,000+ tokens that eat your context window  
- **Multi-step** — Draft, audit, final. Three passes where one should do  
- **Inconsistent** — Same input, different output across models  
- **Noisy** — Preambles, summaries, change logs you didn't ask for  

Humanizer Pro fixes all of that.

## Quick use

Paste your text. Get the final version instantly. No steps, no cleanup.

## Key features

- **One pass + silent self-check** — catches lingering tells without extra output  
- **~750 tokens** — fits anywhere, leaves room for your actual work  
- **Final output only** — no summaries, no greetings, no change logs  
- **Controlled editing** — won't alter technical terms or intentional repetition unnecessarily  
- **Consistent behavior** — tested across Claude, Gemini, Kimi, and MiniMax  

## Example

### Before

> The new software update serves as a testament to the company's commitment to innovation. Moreover, it provides a seamless, intuitive, and powerful user experience—ensuring that users can accomplish their goals efficiently. It's not just an update, it's a revolution in how we think about productivity. Industry experts believe this will have a lasting impact on the entire sector, highlighting the company's pivotal role in the evolving technological landscape.

### After

> The software update adds batch processing, keyboard shortcuts, and offline mode. Beta testers say tasks finish faster.

## Comparison

Estimates based on typical prompt sizes.

| | Humanizer Pro | blader/humanizer | Typical Prompts |
|---|---|---|---|
| **Tokens** | ~750 | ~5,000+ | 1,000–3,000+ |
| **Token reduction** | ~7x smaller | — | — |
| **Passes** | 1 + silent check | 2 (draft + final) | Varies |
| **Output** | Final only | Draft + audit + final | Verbose |
| **Consistency** | High | Medium | Low |
| **Cross-model stability** | Stable | Claude-focused | Inconsistent |
| **Over-editing risk** | Controlled | Uncontrolled | Uncontrolled |

## Why it's different

- **Minimal by design** — every word justifies its place  
- **Deterministic** — same input produces similar output across models  
- **Focused** — 22 prioritized patterns instead of an exhaustive, noisy list  

## Integrations

Works as a reusable skill in local environments or via system instructions.

### Claude Code

```bash
mkdir -p ~/.claude/skills/humanizer-pro
cp SKILL.md ~/.claude/skills/humanizer-pro/
```

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/muhammadgamaleid/humanizer-pro.git ~/.claude/skills/humanizer-pro
```

Usage:

```
/humanizer-pro
[paste your text here]
```

---

### OpenCode

```bash
mkdir -p ~/.config/opencode/skills/humanizer-pro
cp SKILL.md ~/.config/opencode/skills/humanizer-pro/
```

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/muhammadgamaleid/humanizer-pro.git ~/.config/opencode/skills/humanizer-pro
```

Usage:

```
/humanizer-pro
[paste your text here]
```

---

### Any LLM

1. Copy `SKILL.md`  
2. Paste into system prompt  
3. Send your text  

Example:

```
Humanize this:
[paste your text]
```

## Compatibility

| Model   | Performance |
|---------|------------|
| Claude  | Best       |
| Gemini  | Best       |
| Kimi    | Good       |
| MiniMax | Basic      |

## Tool Support

Works well inside:

- **Claude Code** — native skill support  
- **OpenCode** — compatible skill system  

These tools provide a local skill environment for execution.

## Legal

Not affiliated with or endorsed by any of the above platforms.

## Philosophy

80% of results come from fixing 20% of patterns.

If this saves you tokens and time, consider starring the repo.

## Author

Muhammad Gamal Eid

## License

MIT