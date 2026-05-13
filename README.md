# Academic Writer — Claude Skill

A skill for Claude that edits research paper sections to sound like they were
written by a competent researcher who is a **non-native English speaker** — fluent,
technically precise, and academically appropriate, but not artificially polished
or AI-generated.

Built for researchers writing for **IEEE, Elsevier, MDPI, and Springer** journals.

---

## What This Skill Does

Most AI writing tools push text toward casual, personal, or "more native" English.
That is the wrong direction for a research paper.

This skill targets the specific intersection of two problems:

1. **AI slop** — inflation, hollow transitions, -ing appendages, vague quantifiers,
   hedging clusters, synonym cycling
2. **Non-native English patterns** — article errors (a/the/zero), preposition
   mistakes, sentence embedding, tense inconsistency by section

The output sounds like a researcher from Korea, Bangladesh, India, or South/East
Asia who knows their field deeply and writes careful but non-native English — which
is exactly how papers from those research groups read in top journals.

---

## What It Covers

| Area | Details |
|------|---------|
| AI slop removal | 9 pattern types with before/after examples |
| Non-native English fixes | Articles, prepositions, tense, agreement, sentence length |
| Academic register | We vs. passive, confidence level per section, citation format, figure references, numbers/units |
| Section-specific guidance | Abstract, Intro, Related Work, Methods, Results, Discussion, Conclusion |

---

## Installation

### Option 1 — Download ZIP (Easiest)

1. Click the green **Code** button on this GitHub page
2. Select **Download ZIP**
3. Unzip the file — you will get a folder called `academic-writer-skill-main`
4. Rename the folder to `academic-writer`
5. Upload the folder to Claude's skill directory:
   - **Claude.ai (web/app):** Go to **Settings → Skills → Upload Skill Folder**,
     select the `academic-writer` folder
   - **Claude Code:** Move the folder to `~/.claude/skills/academic-writer/`
   - **OpenCode:** Move the folder to `~/.config/opencode/skills/academic-writer/`
     (or `~/.claude/skills/academic-writer/` — OpenCode scans both)

### Option 2 — Git Clone (For Developers)

**Claude Code:**
```bash
mkdir -p ~/.claude/skills
git clone https://github.com/YOUR_USERNAME/academic-writer-skill.git ~/.claude/skills/academic-writer
```

**OpenCode:**
```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/YOUR_USERNAME/academic-writer-skill.git ~/.config/opencode/skills/academic-writer
```

---

## Usage

Once installed, paste any draft section and ask Claude to edit it using this skill.

### Example prompts

```
Edit this Methods section using the academic-writer skill:

[paste your draft here]
```

```
I am writing a paper for Elsevier. Edit this Results section:

[paste your draft here]
```

```
Fix this abstract. I am a non-native English speaker and I want it to sound
natural but still academic:

[paste your draft here]
```

### What Claude will return

1. **Edited version** — full section rewritten
2. **Change log** — brief list of what was changed and why
3. **Remaining concerns** — anything that needs your input (facts to verify,
   missing citations, unclear logic)

---

## Example

**Before (raw draft, AI-assisted):**

> In this paper, we propose a novel and groundbreaking approach for voice
> activity detection that leverages codec-aware training strategy to
> significantly improve the performance of VAD models under the conditions
> of G.711 A-law codec distortion. The proposed method, which uses software
> simulation of A-law encoding that has been validated against real RTP packets
> captured using Wireshark, demonstrates that training on codec-simulated data
> can potentially help to achieve better generalization to telephony
> environments. It is worth noting that the results are competitive with
> existing state-of-the-art methods, highlighting the effectiveness of the
> proposed training methodology and showcasing the importance of codec-aware
> data augmentation in practical VoIP systems.

**After (edited by Claude using this skill):**

> We propose a codec-aware training strategy for voice activity detection (VAD)
> that improves robustness under G.711 A-law codec distortion. The strategy
> uses software-simulated A-law encoding, validated against real G.711 PCMA
> RTP packets via byte-level comparison. Models trained on codec-simulated data
> achieved an average F1 improvement of 7.2% over clean-trained baselines on
> telephony test conditions, and performed comparably to models trained on
> actual encoded audio.

**Change log produced by Claude:**
- Removed "novel and groundbreaking" — replaced with specific claim
- Removed "significantly" — replaced with actual improvement figure
- Removed "it is worth noting that" — started next sentence directly
- Split 3-comma embedded sentence into two sentences
- Removed -ing appendages ("highlighting", "showcasing")
- Replaced "can potentially help to achieve" with direct claim
- Corrected tense to past (Results section norm)

---

## Who This Is For

- Researchers and graduate students (MS/PhD) whose first language is not English
- Anyone submitting to IEEE, Elsevier, MDPI, or Springer journals
- Anyone who used an AI assistant to draft sections and wants to clean them up
  before submission

---

## What This Is Not

This is not a plagiarism tool, a paraphraser, or a grammar checker. It is a
style and register editor. The technical content — your claims, your numbers,
your citations — must be accurate. The skill only fixes how the content is expressed.

---

## Built With

Developed with Claude (Anthropic). Skill format compatible with Claude Code and OpenCode.

---

## License

MIT — free to use, share, and modify. See [LICENSE](LICENSE).

---

## Author

**Cinmoy** — Embedded S/W and AI Engineer

Contributions and feedback welcome via GitHub Issues.
