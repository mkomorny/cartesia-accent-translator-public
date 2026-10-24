---
name: cartesia-accent-translator
description: Translates quotes, dialogue, phrases, or word lists into any requested accent (Chinese, Spanish, French, German, Russian, Japanese, Indian, Scottish, British Cockney/RP, Southern US, etc.) using Cartesia's canonical pipe-separated broad phonemic IPA syntax (<<ˈ|m|ɝ|d|ə|ˈ|b|i|ə|t|s>>). Responds directly in chat with inline TTS-ready text, a word-by-word phonetic breakdown table, and a copy-pasteable JSON snippet. Strictly zero-disk by default: NEVER creates folders or writes .json files to disk unless the user specifically and explicitly asks. Trigger with /cartesia-accent-translator, 'translate to [accent] accent', 'accent translation for', 'phonetic accent', or 'how would a [accent] speaker say'.
---

# Cartesia Accent Translator: Phonetic Dialect & Accent Engine

Specialized linguistic translation skill for **Cartesia Sonic Text-to-Speech (TTS)** and voice cloning workflows.

Unlike standard dictionary generators that write files to disk, `cartesia-accent-translator` functions as an **in-chat, on-demand accent translation engine**. It accepts any input quote, sentence, dialogue line, or vocabulary list and transforms it into authentic accented English phonetics using Cartesia's canonical pipe-separated broad phonemic IPA syntax:
`<<ˈ|m|ɝ|d|ə|ˈ|b|i|ə|t|s>>`

---

## 🔒 The Zero-Disk Guarantee (Strict In-Chat Rule)

> [!IMPORTANT]
> **STRICT IN-CHAT EXECUTION — ZERO DISK WRITES BY DEFAULT**:
> 1. This skill **MUST respond directly in the chat message**.
> 2. It **NEVER creates a folder or writes a `.json` file to disk** without an explicit, unambiguous user command (e.g. *"save this to a json file"*, *"export to my speaker folder"*).
> 3. All outputs—including inline TTS text, phonetics breakdown tables, and Cartesia JSON snippets—are delivered formatted cleanly in Markdown right in the chat conversation.

---

## 🎯 Core Capabilities

1. **On-Demand Accent Translation**: Converts standard text into accented speech for any global accent or dialect:
   - **East Asian**: Chinese (Mandarin / Cantonese), Japanese, Korean, Vietnamese.
   - **European**: French, German, Italian, Spanish, Portuguese, Russian / Slavic, Greek.
   - **South Asian**: Indian (Hindi, Tamil, Punjabi English).
   - **Regional Anglophone**: Scottish, Irish, British RP, Cockney, Australian, South African, Southern US, New York / Brooklyn, Boston, Jamaican Patois.
   - **Fictional & Persona Dialects**: Fantasy accents, comedic characters, sci-fi personas.
2. **Canonical Cartesia IPA Compliance**: Formats every phoneme with exact pipe-separated boundaries, isolates stress tokens (`|ˈ|`, `|ˌ|`), and protects atomic diphthongs and affricates.
3. **Dual Integration Output**:
   - **Inline TTS Ready**: Embeds `<<ˈ|...>>` tags directly into the sentence so the user can paste the prompt straight into Cartesia Sonic TTS.
   - **Copy-Pasteable Dictionary JSON Block**: Formats the words into Cartesia's official dictionary schema inside a chat code block for easy manual copy-pasting.

---

## 📐 Cartesia Pipe-Separated IPA Standards

Cartesia Sonic requires broad phonemic IPA enclosed in `<< >>` and delimited by pipes (`|`):
`<<ˈ|m|ɝ|d|ə|ˈ|b|i|ə|t|s>>`

### Syntax Rules
1. **Pipe Delimitation**: Every single phonemic unit must be flanked by pipes (`|`).
2. **Stress Markers**: Primary stress (`ˈ`) and secondary stress (`ˌ`) are separate pipe-delimited tokens placed before the stressed syllable:
   - Primary: `|ˈ|` (e.g., `<<ˈ|w|ɑː|t|ɚ>>`)
   - Secondary: `|ˌ|` (e.g., `<<ˌ|k|ɑː|l|ə|ˈ|ɹ|æ|d|oʊ>>`)
3. **Atomic Units (Never Split)**:
   - Diphthongs: `|aɪ|`, `|eɪ|`, `|oʊ|`, `|aʊ|`, `|ɔɪ|`, `|ɪə|`, `|eə|`, `|ʊə|` (NEVER `|a|ɪ|` or `|e|ɪ|`).
   - Affricates: `|tʃ|`, `|dʒ|` (NEVER `|t|ʃ|` or `|d|ʒ|`).
4. **Cadence & Vowel Elongation**:
   - Duplicate vowel tokens to model drawls, hesitation, or non-native vowel stretching:
     - `liiiike` -> `<<ˈ|l|aɪ|aɪ|k>>`
     - `soooo` -> `<<ˈ|s|oʊ|oʊ>>`
     - `veryyy` -> `<<ˈ|w|ɛ|ɹ|i|i>>`
5. **No Casual Latin Respellings**:
   - Never use informal respellings like `chou-fan` or `WAN-der-fool`. Always compile to canonical Cartesia pipe IPA.

---

## 🌍 Accent Phonological Engine & Native Transfer Rules

When translating text into an accent, apply systematic phonological transfer (L1 transfer effects, syllable restructuring, vowel shifts, and consonant substitutions):

### 1. Chinese-Accented English (Mandarin / Cantonese L1)
- **Dental Fricative Substitution**:
  - Unvoiced `/θ/` -> `/s/` or `/t/` (*think* -> `<<ˈ|s|ɪ|ŋ|k>>`, *three* -> `<<ˈ|s|ɹ|iː>>`)
  - Voiced `/ð/` -> `/z/` or `/d/` (*this* -> `<<ˈ|z|ɪ|s>>`, *that* -> `<<ˈ|z|æ|t>>` or `<<ˈ|d|æ|t>>`)
- **Labiodental /v/ -> /w/ or /f/**:
  - *very* -> `<<ˈ|w|ɛ|ɹ|i>>` or `<<ˈ|f|ɛ|ɹ|i>>`
  - *have* -> `<<ˈ|h|æ|f>>` or `<<ˈ|h|æ|w>>`
- **Consonant Cluster Epenthesis & Vowel Insertion**:
  - Mandarin phonotactics disallow consonant codas (except /n/ and /ŋ/). Speakers insert an epenthetic schwa `/ə/` or `/u/` after stop consonants:
  - *please* -> `<<ˈ|p|ə|ˈ|l|iː|z>>` or `<<ˈ|p|ə|ˈ|l|iː|s>>`
  - *good* -> `<<ˈ|ɡ|uː|d|ə>>`
  - *friend* -> `<<ˈ|f|ə|ˈ|ɹ|ɛ|n>>`
- **Final Consonant Devoicing or Deletion**:
  - Voiced stops devoice or drop: *bad* -> `<<ˈ|b|æ|t>>`, *card* -> `<<ˈ|k|ɑː|t>>`
  - Final `/l/` vocalized: *people* -> `<<ˈ|p|iː|p|oʊ>>`
- **Liquid Realization (/ɹ/ vs /l/)**:
  - Retroflex `/ɹ/` softened or substituted with `/l/` or glide: *right* -> `<<ˈ|l|aɪ|t>>` or `<<ˈ|ɹ|aɪ|t>>`
- **Vowel Shifts & Monophthongization**:
  - `/æ/` -> `/ɛ/` (*cat* -> `<<ˈ|k|ɛ|t>>`, *thank* -> `<<ˈ|s|ɛ|ŋ|k>>`)
  - `/ɪ/` -> `/iː/` (*it* -> `<<ˈ|iː|t>>`, *sit* -> `<<ˈ|s|iː|t>>`)
  - `/ʌ/` -> `/ɑ/` or `/ə/` (*love* -> `<<ˈ|l|ɑ|f>>`)
- **Prosody**: Syllable-timed staccato rhythm with higher tonal pitch excursions.

### 2. Spanish-Accented English
- **S-Cluster Prothesis**:
  - Prepends `/ɛ/` before word-initial /s/ + consonant clusters:
  - *special* -> `<<ɛ|ˈ|s|p|ɛ|ʃ|ə|l>>`
  - *student* -> `<<ɛ|ˈ|s|t|uː|d|ə|n|t>>`
  - *speak* -> `<<ɛ|ˈ|s|p|iː|k>>`
- **B/V Betacism**:
  - Merges `/v/` into bilabial stop `/b/`: *very* -> `<<ˈ|b|ɛ|ɹ|i>>`, *voice* -> `<<ˈ|b|ɔɪ|s>>`
- **De-affrication / Affricate Shifts**:
  - `/dʒ/` -> `/j/` (*just* -> `<<ˈ|j|ʌ|s|t>>`, *juice* -> `<<ˈ|j|uː|s>>`)
  - `/ʃ/` and `/tʃ/` frequent alternation (*shoes* -> `<<ˈ|tʃ|uː|s>>`)
- **Devoicing Sibilants**:
  - `/z/` -> `/s/` (*is* -> `<<ˈ|iː|s>>`, *was* -> `<<ˈ|w|ɑː|s>>`)
- **5-Vowel Inventory Collapse**:
  - `/ɪ/` -> `/iː/` (*bit* -> `<<ˈ|b|iː|t>>`)
  - `/ʊ/` -> `/uː/` (*pull* -> `<<ˈ|p|uː|l>>`)
  - `/æ/` -> `/a/` (*cat* -> `<<ˈ|k|a|t>>`)
  - Rhotic trills or flaps: `|ɾ|`, `|r|`.

### 3. French-Accented English
- **Initial /h/ Dropping**:
  - *have* -> `<<ˈ|æ|v>>`, *hello* -> `<<ɛ|ˈ|l|oʊ>>`, *happy* -> `<<ˈ|æ|p|i>>`
- **Dental Fricative Shifts**:
  - `/θ/` -> `/s/` (*thing* -> `<<ˈ|s|ɪ|ŋ|k>>`)
  - `/ð/` -> `/z/` (*the* -> `<<ˈ|z|ə>>`, *this* -> `<<ˈ|z|iː|s>>`)
- **Stress Displacement**:
  - Shifts primary stress to the final syllable of multi-syllable words or phrases.
- **Rhotics**:
  - Non-rhotic vowel coloration or uvular realization.

### 4. German-Accented English
- **W/V Transposition**:
  - `/w/` -> `/v/` (*water* -> `<<ˈ|v|ɑː|t|ɚ>>` or `<<ˈ|v|a|t|ɐ>>`, *we* -> `<<ˈ|v|iː>>`)
  - `/v/` -> `/f/` (*very* -> `<<ˈ|f|ɛ|ɹ|i>>`)
- **Terminal Devoicing (Auslautverhärtung)**:
  - Final voiced consonants become voiceless: `/d/` -> `/t/` (*good* -> `<<ˈ|ɡ|uː|t>>`), `/b/` -> `/p/`, `/ɡ/` -> `/k/` (*bag* -> `<<ˈ|b|æ|k>>`), `/z/` -> `/s/` (*is* -> `<<ˈ|ɪ|s>>`).
- **Dental Fricatives**:
  - `/θ/` -> `/s/` or `/t/` (*think* -> `<<ˈ|s|ɪ|ŋ|k>>`).

### 5. Russian / Slavic-Accented English
- **Consonant Mergers**:
  - `/w/` -> `/v/` (*what* -> `<<ˈ|v|ɑː|t>>`)
  - `/θ/` -> `/t/` or `/s/` (*three* -> `<<ˈ|t|ɹ|iː>>`)
  - `/ð/` -> `/d/` or `/z/` (*there* -> `<<ˈ|d|ɛ|ɹ>>`)
- **Monophthongization**:
  - Diphthongs reduced: `/oʊ/` -> `/oː/`, `/eɪ/` -> `/eː/`.
- **Rhotics & Devoicing**:
  - Alveolar trill `|r|` or tap `|ɾ|`.
  - Severe final obstruent devoicing (*friend* -> `<<ˈ|f|ɹ|ɛ|n|t>>`).

### 6. Indian-Accented English
- **Retroflex Consonants**:
  - Alveolar `/t/` and `/d/` become retroflex.
- **V/W Approximant Merger**:
  - Voiced labiodental approximant `/ʋ/` or `/v/` used for both /w/ and /v/.
- **Monophthongized Vowels**:
  - `/eɪ/` -> `/eː/` (*make* -> `<<ˈ|m|eː|k>>`), `/oʊ/` -> `/oː/` (*go* -> `<<ˈ|ɡ|oː>>`).
- **Syllable-Timed Meter**:
  - Even cadence across all syllables without schwa reductions.

---

## 💬 Response Protocol: How to Deliver the Translation

When a user provides a quote or text and an accent (e.g. *"translate 'I don't think this is going to work' in a Chinese accent"*), deliver the response with the following structured sections:

### 1. 🎤 Accented Phonetic Line (TTS Ready)
Provide the full sentence with inline Cartesia IPA tokens embedded, so the user can immediately copy-paste the line into the Cartesia Sonic TTS text input:
> *"I <<ˈ|d|oʊ|n|t>> <<ˈ|s|ɪ|ŋ|k>> <<ˈ|z|ɪ|s>> <<ˈ|iː|s>> <<ˈ|ɡ|oʊ|ɪ|n>> to <<ˈ|w|ɝ|k|ə>>."*

### 2. 📑 Word-by-Word / Phrasal Accent Breakdown Table
Display a clear Markdown table detailing the phonetic shift for each accented word:

| Original Word | Cartesia Pipe IPA | Accent Shift & Realization |
| :--- | :--- | :--- |
| **think** | `<<ˈ|s|ɪ|ŋ|k>>` | Dental fricative /θ/ replaced with alveolar fricative /s/ |
| **this** | `<<ˈ|z|ɪ|s>>` | Voiced dental fricative /ð/ replaced with voiced sibilant /z/ |
| **is** | `<<ˈ|iː|s>>` | Vowel tensed (/ɪ/ -> /iː/) and final /z/ devoiced to /s/ |
| **work** | `<<ˈ|w|ɝ|k|ə>>` | Consonant coda release with epenthetic schwa /ə/ |

### 3. 🔬 Phonological Mechanics Applied
Provide 3-4 bullet points highlighting the specific linguistic and dialectal rules used (e.g. L1 phonotactics, coda restrictions, vowel shifts).

### 4. 📋 Copy-Pasteable Cartesia JSON Dictionary Snippet
Provide a clean JSON code block formatted to Cartesia's official dictionary API schema (so the user can copy-paste it into an existing dictionary if they want):

```json
{
  "name": "Chinese_Accent_Quote_Dictionary",
  "items": [
    {
      "text": "think",
      "pronunciation": "<<ˈ|s|ɪ|ŋ|k>>",
      "case_sensitive": false
    },
    {
      "text": "this",
      "pronunciation": "<<ˈ|z|ɪ|s>>",
      "case_sensitive": false
    }
  ]
}
```

### 5. 💾 Zero-Disk Notice
Conclude with a clear reminder:
> *ℹ️ **Note**: No files or folders were created on disk. If you'd like this saved to a `.json` dictionary file or persona directory, just let me know!*

---

## ⚡ File Export Policy (Only When Explicitly Asked)

If and ONLY IF the user explicitly requests saving to disk (e.g., *"save this dictionary to a file"*, *"write this to my persona folder"*):
- Save the consolidated JSON file to `B:\Media\Audio\Voice_Clones\<Speaker_Name>\<Speaker_Name>_Pronunciation_Dictionary.json` or the user's requested path.
- Validate that all entries strictly follow Cartesia pipe-separated broad phonemic IPA syntax (`<<ˈ|...>>`).
