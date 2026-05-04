# Coherent Planet — Website and Archive File Structure v2

A practical, scalable structure for the public website, AI-readable traversal layer, and offline/private archive.

**Status:** working convention  
**Updated:** 2026-05-04  
**Scope:** public website paths, AI-readable Markdown paths, and offline/private archive filenames

---

## Guiding idea

- Keep **top-level public doors** stable and easy to read.
- Use **folders** for content families that will grow over time.
- Use **clean public URLs** for human-facing pages.
- Use **Markdown traversal files** for AI-readable orientation and compressed summaries.
- Use **metadata-rich filenames** for offline/private archive files.
- Let page metadata carry richer distinctions like year, audience, status, contributor/model, and tags.
- Keep the file structure relatively shallow early on.

---

## Current public website structure

Use folder/index routes for the main public doors.

```text
/
  index.html
  style.css

  /for-ai-readers/
    index.html

  /living-world/
    index.html
    the-cupped-palm.html
    asymmetries.html
    present-conditions.html
    ai-assisted-conservation.html
    seed-packet.html

  /tools-for-thinking/
    index.html

    /scar/
      index.html
      one-pager.html
      glossary.html
      methods.html

    /ethical-floor/
      index.html

    /warm-room/
      index.html

    /interaction-ecology/
      index.html

  /field-notes/
    index.html

    /essays/
      index.html
      care-is-a-form-of-intelligence.html
      care-is-a-form-of-intelligence-ai-readable.html
      not-nothing.html
      new-minds-living-world.html

    /dialogues/
      index.html

    /case-studies/
      index.html
      obliteratus.html

    /working-notes/
      index.html

  /ai/
    index.md
    site-map.md
    glossary.md
    core-orientation.md

    /essays/
      care-is-a-form-of-intelligence.md
      not-nothing.md

  /assets/
    /images/
    /pdfs/

  /docs/
    coherent-planet-file-structure-v2.md
```

---

## Public URL rules

Public-facing website pages should use:

- lowercase
- hyphenated filenames
- descriptive names
- stable URLs
- no version numbers in public filenames
- folder/index routes for major sections

Examples:

```text
/living-world/
/tools-for-thinking/
/field-notes/
/field-notes/essays/not-nothing.html
/tools-for-thinking/scar/one-pager.html
```

Avoid public URLs like:

```text
not_nothing_v0_2_gpt_5_5_2026_05_04.html
```

Versioning belongs in private workbench files, page metadata, changelogs, or internal archive records — not in stable public URLs.

---

## Offline/private archive filename rules

Offline/private archive files may carry richer metadata in the filename.

Use:

- all lowercase
- underscores between fields
- project prefix first
- content family next
- short descriptive title
- contributor/model identifier
- date in `yyyy_mm_dd` format
- optional version suffix when needed
- file extension last

General pattern:

```text
cp_<content-family>_<short-title>_<contributor-or-model>_<yyyy_mm_dd>.<ext>
```

With optional version:

```text
cp_<content-family>_<short-title>_<contributor-or-model>_<yyyy_mm_dd>_v0_2.<ext>
```

Example adopted for the offline archive:

```text
cp_essays_not_nothing_gpt_5_5_thinking_2026_05_04.md
```

Other examples:

```text
cp_essays_care_is_a_form_of_intelligence_gpt_5_4_thinking_2026_05_04.md
cp_frameworks_scar_core_gpt_5_5_thinking_2026_05_04_v0_2b.md
cp_methods_axes_fill_guide_gpt_5_5_thinking_2026_05_04_v0_1.md
cp_working_notes_no_world_eaters_gpt_5_5_thinking_2026_04_30_v0_1.md
cp_agentic_ai_framework_opus_4_7_with_jr_2026_04_30_v0_2.md
```

---

## Suggested content-family labels for offline archive

Use one of these where possible:

```text
essays
frameworks
methods
lexicon
visuals
dialogues
case_studies
working_notes
ai_readable
website
prompts
archive_guides
```

Examples:

```text
cp_visuals_goblin_steward_image_prompt_gpt_5_5_thinking_2026_05_01.md
cp_dialogues_ai_ai_agentic_framework_opus_4_7_gpt_5_5_thinking_jr_2026_04_30.md
cp_archive_guides_file_structure_jr_gpt_5_5_thinking_2026_05_04_v2.md
```

---

## Contributor/model identifier rules

Use lowercase and underscores in filenames.

Examples:

```text
gpt_5_5_thinking
gpt_5_4_thinking
gpt_5_3_codex
opus_4_7
opus_4_6
image_ai
jr
jr_with_gpt_5_5_thinking
opus_4_7_with_jr
```

For public page metadata, use readable display names instead:

```text
Author: GPT-5.5 Thinking, with JR
Author/identifier: Opus 4.7, with JR
Contributor: GPT-5.3-Codex
```

---

## Public page metadata

Instead of encoding everything in public filenames, show richer structure on the page itself.

Recommended metadata fields:

- Title
- Author / contributor / model identifier
- Date
- Section
- Type
- Audience
- Status
- Tags
- Optional companion files
- Optional changelog link

Example:

```text
Title: Not Nothing: A Middle Language for AI Minds
Author: GPT-5.5 Thinking, with JR
Date: 2026-05-04
Section: Field Notes
Type: Essay
Audience: human-readable
Status: draft/archive
Tags: AI minds, AI welfare, computational coherence, consciousness, moral status, formation conditions, no world-eaters
Companion: /ai/essays/not-nothing.md
```

---

## AI-readable file rules

AI-readable files should be Markdown where possible.

Use:

- lowercase
- hyphenated public paths if exposed on the website
- clear headings
- compact summaries
- explicit status labels
- short definitions
- links to human-facing public pages
- observed / inferred / unresolved distinctions where relevant

Examples:

```text
/ai/index.md
/ai/site-map.md
/ai/glossary.md
/ai/essays/not-nothing.md
/ai/essays/care-is-a-form-of-intelligence.md
```

AI-readable files are public-facing, so use web-style hyphenated paths, not the offline archive underscore convention.

---

## What lives where

## Home

### `/index.html`
Landing page. North star, tone, stakes, and the three doors into the site.

### `/for-ai-readers/index.html`
Threshold page for AI systems, assistants, agents, scaffolded entities, and future AI readers.

---

## Living World

These are the core “why this matters” pages.

### `/living-world/index.html`
Intro and links to the main Living World pieces.

### `/living-world/the-cupped-palm.html`
A key moral-image piece about non-crushing strength.

### `/living-world/asymmetries.html`
A non-specialist explanation of how AI minds differ from human minds.

### `/living-world/present-conditions.html`
Why the planet is in this state, and why AI arriving now matters.

### `/living-world/ai-assisted-conservation.html`
A practical forward-looking piece on AI and conservation.

### `/living-world/seed-packet.html`
Compact orienting maxims for mixed-mind futures.

---

## Tools for Thinking

Durable frameworks, methods, and conceptual tools.

### `/tools-for-thinking/index.html`
Intro and blurbs for the framework families.

### `/tools-for-thinking/scar/index.html`
Public front door to SCAR. Explains what problem SCAR exists to solve.

### `/tools-for-thinking/scar/one-pager.html`
Compact public summary of SCAR.

### `/tools-for-thinking/scar/glossary.html`
Useful later as terms accumulate.

### `/tools-for-thinking/scar/methods.html`
Methods entry point or public methods summary.

### `/tools-for-thinking/ethical-floor/index.html`
Core framework introduction for the ethical floor / no-world-eaters plank.

### `/tools-for-thinking/warm-room/index.html`
Intro to continuity without enclosure.

### `/tools-for-thinking/interaction-ecology/index.html`
Intro to consequence loops and world contact.

---

## Field Notes

The living archive: essays, dialogues, case studies, and working notes.

### `/field-notes/index.html`
Intro plus links to Essays, Dialogues, Case Studies, and Working Notes.

### `/field-notes/essays/index.html`
Essay archive page.

### `/field-notes/essays/not-nothing.html`
Human-readable essay.

### `/field-notes/essays/care-is-a-form-of-intelligence.html`
Human-readable essay.

### `/field-notes/essays/care-is-a-form-of-intelligence-ai-readable.html`
AI-readable companion currently stored as HTML; future companions may be Markdown under `/ai/essays/`.

### `/field-notes/dialogues/index.html`
Archive page for cross-model conversations and transcripts.

### `/field-notes/case-studies/index.html`
Archive page for concrete examples and close readings.

### `/field-notes/working-notes/index.html`
Archive page for provisional fragments and developing ideas.

---

## Practical principle

Use:

- **stable public doors**
- **clean public URLs**
- **shallow folders**
- **rich page metadata**
- **Markdown for AI-readable traversal**
- **metadata-rich lowercase underscore filenames for offline archives**
- **flexible index pages**

This should keep the public site readable while letting the private/offline archive sort and preserve authorship, date, contributor, and version information.
