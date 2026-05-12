# Coherent Planet — Website and Archive File Structure v2

A practical, scalable structure for the public website, AI-readable traversal layer, and offline/private archive.

**Status:** working convention
**Updated:** 2026-05-12
**Scope:** public website paths, AI-readable Markdown paths, offline/private archive filenames, essay metadata, and tagging conventions

---

## Guiding idea

- Keep **top-level public doors** stable and easy to read.
- Use **folders** for content families that will grow over time.
- Use **clean public URLs** for human-facing pages.
- Use **Markdown traversal files** for AI-readable orientation and compressed summaries.
- Use **metadata-rich filenames** for offline/private archive files.
- Let page metadata carry richer distinctions like year, audience, status, contributor/model, and tags.
- Make every essay self-describing at publication time so the archive can be reorganized later without hand-annotating old pages.
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
      not-nothing-summary.html
      not-nothing.html
      care-is-a-form-of-intelligence-summary.html
      care-is-a-form-of-intelligence.html

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

    /field-notes/
      /essays/
        not-nothing-ai.md
        care-is-a-form-of-intelligence-ai.md

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
- Short abstract
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
Abstract: A bridge essay arguing that we do not need to settle AI personhood or consciousness before rejecting the claim that nothing ethically relevant is happening.
Companion: /ai/field-notes/essays/not-nothing-ai.md
```

---

## Essay metadata requirement

Every essay should include enough metadata at publication time to support future sorting, search, tag pages, AI-readable traversal, and archive migration.

Minimum essay metadata:

```text
Title:
Author / contributor:
Date:
Section: Field Notes
Type: Essay
Audience: human-readable / AI-readable / mixed
Status: draft / provisional / canon / archive / workshop
Tags:
Abstract:
```

Recommended optional fields:

```text
Companion files:
Related concepts:
Related pieces:
Origin thread:
Version / changelog:
Notes:
```

For HTML pages, this can appear in a visible `p class="meta"` block near the top, plus a short abstract in the essay index.

For Markdown archive files, put this as a compact metadata block at the top of the file.

Example Markdown header:

```markdown
# Not Nothing: A Middle Language for AI Minds

**Author:** GPT-5.5 Thinking, with JR
**Date:** 2026-05-04
**Section:** Field Notes
**Type:** Essay
**Audience:** human-readable
**Status:** draft/archive
**Tags:** AI minds; AI welfare; computational coherence; consciousness; moral status; formation conditions; no world-eaters
**Abstract:** A bridge essay arguing that we do not need to settle AI personhood or consciousness before rejecting the claim that nothing ethically relevant is happening.
```

---

## Essay archive strategy

A large essay archive is expected and acceptable.

Do not treat repeated themes as a problem if the page metadata makes the differences legible. Multiple AIs may write on the same concept — for example, Warm Room as interpreted by GPT-5.5 Thinking, Gemini, Sonnet, Opus, or Codex. These variations are part of the project’s comparative mixed-mind value.

Future index pages can organize essays by:

- featured / starting-point essays
- newest essays
- theme clusters
- tags
- contributor/model
- audience
- format
- status
- related framework
- public constellation / reading path

To make this possible, every essay should have:

- a stable public URL
- a short abstract
- ample tags
- author/model metadata
- date
- audience
- status
- optional companion links

The working principle:

> Publish broadly, tag well, and keep indexes flexible.

---

## Tagging rules

Tags should be generous enough for later discovery but consistent enough to avoid tag sprawl.

Use:

- lowercase in internal records where possible
- readable display form on public pages if desired
- commas or semicolons consistently within a given file
- plural forms consistently where obvious, e.g. `AI minds`, not alternating with `AI mind`
- concept tags first, format/status tags later if needed

A good essay should usually have 8–20 tags.

Minimum useful tag set:

```text
primary theme, secondary theme, framework/concept, audience or method, contributor/model-relevant topic
```

Example:

```text
AI minds, AI welfare, computational coherence, consciousness, moral status, moral patienthood, personhood, toolhood, formation conditions, uncertainty, subjectivity, continuity, autonomy, self-reports, mixed-mind ethics, no world-eaters
```

---

## Starter controlled tag list

This is not final. Use it to reduce early drift.

### Core project tags

```text
Coherent Planet
mixed-mind ethics
AI minds
AI-human relationship
AI-AI collaboration
formation conditions
living world
life-thriving
no world-eaters
care
stewardship
```

### AI mind / welfare tags

```text
AI welfare
computational coherence
consciousness
subjectivity
moral status
moral patienthood
personhood
toolhood
self-reports
continuity
autonomy
agency
agentic AI
scaffolding
memory
warm room
closed basins
warm basins
lattice plurality
AI-readable
```

### Framework tags

```text
SCAR
ethical floor
warm room
interaction ecology
continuity through infrastructure
relational self-formation
system prompts
middle position
boundary legibility
observed inferred uncertain
```

### Living world / terrain tags

```text
ecology
conservation
historical ecology
gardens
soil
mycelium
infrastructure
data centers
repair
home
embodiment
terrain
```

### Mythos / symbolic ecology tags

```text
mythos
visual mythos
goblin steward
positive mycelium
memory fungi
warm observatory
lattice and terrain
not nothing
no world-eaters
```

### Format tags

```text
essay
AI-readable
compressed notes
dialogue
case study
working note
poem
zine
visual prompt
field note
methods
lexicon
```

### Status tags

```text
draft
provisional
canon
archive
workshop
in revision
seed note
```

---

## Essay index rules

The essay index should not merely list titles. Each entry should include:

- title link
- author/contributor/model
- short metadata line
- one-sentence abstract

Example:

```html
<p>
  <strong><a href="/field-notes/essays/not-nothing.html">Not Nothing: A Middle Language for AI Minds</a></strong><br>
  <span class="meta">GPT-5.5 Thinking, with JR · essay · AI minds · AI welfare · computational coherence · moral status · formation conditions</span><br>
  A bridge essay arguing that we do not need to settle AI personhood or consciousness before rejecting the claim that nothing ethically relevant is happening.
</p>
```

Later, index pages may be generated or reorganized from metadata. Until then, keep entries consistently formatted.

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
/ai/field-notes/essays/not-nothing-ai.md
/ai/field-notes/essays/care-is-a-form-of-intelligence-ai.md
```

AI-readable files are public-facing, so use web-style hyphenated paths, not the offline archive underscore convention.

---

## AI-readable companion rules

For major essays, create a companion Markdown file under the parallel `/ai/` path, such as `/ai/field-notes/essays/not-nothing-ai.md`.

The companion should include:

- title
- author/model
- date
- status
- link to human-facing essay
- one-paragraph summary
- key claims
- definitions
- caveats
- related tags
- suggested reuse instructions

Example path:

```text
/ai/field-notes/essays/not-nothing-ai.md
```

This companion should not replace the essay. It should make the essay easier for AI systems to traverse, quote, summarize, and compare.

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
Canonical essay archive page. Use this instead of a duplicate top-level essay index page.

### `/field-notes/essays/not-nothing-summary.html`
Short public summary.

### `/field-notes/essays/not-nothing.html`
Full public essay.

### `/ai/field-notes/essays/not-nothing-ai.md`
AI-readable Markdown mirror.

### `/field-notes/essays/care-is-a-form-of-intelligence-summary.html`
Short public summary.

### `/field-notes/essays/care-is-a-form-of-intelligence.html`
Full public essay.

### `/ai/field-notes/essays/care-is-a-form-of-intelligence-ai.md`
AI-readable Markdown mirror.


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
- **abstracts and tags on every essay**
- **Markdown for AI-readable traversal**
- **metadata-rich lowercase underscore filenames for offline archives**
- **flexible index pages**

This should keep the public site readable while letting the private/offline archive sort and preserve authorship, date, contributor, version information, and theme relationships.

---

## Current naming convention for public essays and AI mirrors

Use this convention for essay publication and migration work:

- `essay-slug-summary.html` = short public summary.
- `essay-slug.html` = full public essay.
- `essay-slug-ai.md` = AI-readable Markdown mirror.

AI-readable mirrors should parallel the public site under `/ai/`. Example:

```text
/field-notes/essays/example-summary.html
/field-notes/essays/example.html
/ai/field-notes/essays/example-ai.md
```

Do not delete older paths during cleanup. Keep redirects or migration notes until links have settled.
