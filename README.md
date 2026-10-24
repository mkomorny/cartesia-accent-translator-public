# Cartesia Accent Translator

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Phonetic Dialect & Accent Engine — Translates dialogue and quotes into authentic accented English phonetics using Cartesia's canonical broad phonemic pipe IPA syntax (<<ˈ|m|ɝ|d|ə|ˈ|b|i|ə|t|s>>) with strict zero-disk in-chat guarantees.

---

## Overview

`cartesia-accent-translator` provides standardized capabilities across conversational AI platforms:
- In-chat, zero-disk on-demand phonetic accent translation engine.
- Global dialect catalog (East Asian, European, South Asian, Regional Anglophone, Fictional).
- Strict Cartesia pipe-separated broad phonemic IPA syntax formatting (<<ˈ|...>>).
- Isolated primary/secondary stress tokens and atomic diphthong/affricate protection.
- Triple-tier response output: Inline TTS ready text, word breakdown table, and JSON dictionary block.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\cartesia-accent-translator`
- **Claude**: `C:\Users\<you>\.claude\skills\cartesia-accent-translator` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\cartesia-accent-translator` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\cartesia-accent-translator` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
