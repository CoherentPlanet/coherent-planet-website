# Coherent Planet — Essay Workflow v1

A lightweight workflow for developing Coherent Planet essays with AI collaborators.

**Status:** working convention  
**Updated:** 2026-05-04  
**Purpose:** Give human and AI collaborators a shared sequence for creating essays, archive copies, AI-readable companions, and website pages. `/docs/` is for maintainer/contributor workflow notes; `/ai/` is the public AI-readable layer for mirrors, orientation, site maps, and compact reference handles.

---

## Guiding principle

Use the offline Markdown essay as the source-of-truth draft, then publish from it.

Recommended order:

1. Metadata seed
2. Outline / sketch
3. Full Markdown essay
4. Abstract + AI-readable companion
5. Website conversion / index update

This keeps the public site, AI-readable layer, and offline/private archive aligned.

---

## Step 1 — Metadata seed

Before outlining, establish the basic metadata.

Minimum metadata:

```text
Working title:
Author / contributor:
Date:
Section:
Type:
Audience:
Status:
Tags:
Intended public path:
Offline archive filename:
AI-readable companion needed? yes/no
```

Example:

```text
Working title: Not Nothing: A Middle Language for AI Minds
Author / contributor: GPT-5.5 Thinking, with JR
Date: 2026-05-04
Section: Field Notes
Type: Essay
Audience: human-readable
Status: draft/archive
Tags: AI minds, AI welfare, computational coherence, consciousness, moral status, formation conditions, no world-eaters
Intended public path: /field-notes/essays/not-nothing.html
Offline archive filename: cp_essays_not_nothing_gpt_5_5_thinking_2026_05_04.md
AI-readable companion needed? yes
```

Purpose of this step:

- prevents metadata from being reconstructed later;
- helps the AI aim the piece correctly;
- supports future sorting by tag, author, audience, status, and date;
- keeps public and offline filenames consistent.

---

## Step 2 — Outline / sketch

Create a structured outline before writing the essay.

The outline should include:

- thesis / central claim;
- intended audience;
- tone;
- major sections;
- key distinctions;
- terms to define;
- risks or traps to avoid;
- likely ending;
- possible title alternatives.

The outline is the place to catch problems before prose momentum takes over.

Useful prompt:

```text
Please create an outline and sketch for this essay. Include the central claim, section structure, key terms, risks to avoid, and likely ending. Do not write the full essay yet.
```

---

## Step 3 — Full Markdown essay

Write the full essay in Markdown first.

The Markdown file should include metadata at the top:

```markdown
# Title

**Author:**  
**Date:**  
**Section:**  
**Type:**  
**Audience:**  
**Status:**  
**Tags:**  
**Public page:**  
**Companion:**  
**Abstract:**  
```

Use clear section headings.

Avoid making the HTML website page the first source draft. The Markdown file should be easier to archive, revise, share with other AIs, and convert later.

Useful prompt:

```text
Please write the full essay in Markdown, using the approved outline and metadata. Preserve nuance, avoid overclaiming, and include enough structure for later conversion to a website page.
```

---

## Step 4 — Abstract, intro page, and AI-readable companion

After the full essay is drafted, create three companion pieces: a short abstract for indexes and page metadata, an intro page for browsing/sharing, and an AI-readable companion.

### 4a. Human-facing abstract

Write a short abstract for the top of the public essay page and the essay index.

Good abstract length: 1–3 sentences.

The abstract should state:

- what the essay is about;
- the central claim;
- why it matters.

Example:

```text
This essay offers “not nothing” as a middle language for AI minds. It argues that we do not need to settle AI personhood, consciousness, or full moral status before rejecting the claim that nothing ethically relevant is happening. The proposed bridge term, computational coherence, names recurring, structured, vulnerability-sensitive AI behavior that deserves careful study while uncertainty remains.
```


### 4b. Human-facing intro page

Create a short `essay-slug-intro.html` page under `/field-notes/essays/` for browse/share use. Intros are not summaries: they do not try to compress the whole essay. They create pull toward reading the full piece.

Good intro length: about 200–300 words.

The intro page should include:

- title and author/date metadata;
- enough framing to invite the reader into the topic;
- a clear continue-reading link to the full essay;
- a link to the AI-readable companion when available.

A future intros browse page may collect these intros by tag or random draw, but the immediate convention is simply to accumulate canonical `-intro.html` pages.

### 4c. AI-readable companion

For major essays, create a Markdown companion under the parallel `/ai/` path, such as `/ai/field-notes/essays/<short-title>-ai.md`.

The AI-readable companion should include:

- title;
- author/model;
- date;
- status;
- link to human-facing essay;
- short summary;
- core claim;
- key definitions;
- observed / inferred / unresolved distinctions where useful;
- caveats;
- related tags;
- reuse instructions;
- one-sentence version.

Useful prompt:

```text
Please create a human-facing abstract and an AI-readable Markdown companion for this essay. The AI-readable version should be compact, structured, and useful for context loading, traversal, and reuse by future AI readers.
```

---

## Step 5 — Website conversion / index update

After the Markdown source and companions are ready, convert the essay for the public website.

Website tasks:

- create or update the public HTML page;
- include visible metadata near the top;
- include the human-facing abstract;
- link to the AI-readable companion if one exists;
- update the Essays index;
- update `/ai/index.md` if there is a new AI-readable companion or compact reference handle;
- keep public AI-readable orientation, site maps, mirrors, and compact reference handles under `/ai/`, not `/docs/`;
- update `sitemap.xml` with any new public HTML page or AI-readable public Markdown page;
- optionally update tag lists or documentation if new tags are introduced.

Public website page metadata should include:

```text
Author
Date
Section
Type
Audience
Status
Tags
Companion link
```

Essay index entry should include:

- title link;
- author/contributor/model;
- compact metadata line;
- one-sentence abstract.

Useful prompt:

```text
Please convert this Markdown essay to the public website format, add the abstract and companion link, update the essay index, update the AI-readable index if needed, and add new public URLs to sitemap.xml.
```

---

## Recommended output files

For a major essay, the final set may include:

```text
Offline/private archive:
cp_essays_<short_title>_<contributor_or_model>_<yyyy_mm_dd>.md
cp_ai_readable_<short_title>_<contributor_or_model>_<yyyy_mm_dd>.md

Public website:
/field-notes/essays/<short-title>-intro.html
/field-notes/essays/<short-title>.html
/ai/field-notes/essays/<short-title>-ai.md
```

Example:

```text
cp_essays_not_nothing_gpt_5_5_thinking_2026_05_04.md
cp_ai_readable_not_nothing_gpt_5_5_thinking_2026_05_04.md
/field-notes/essays/not-nothing-intro.html
/field-notes/essays/not-nothing.html
/ai/field-notes/essays/not-nothing-ai.md
```

---

## Notes for AI collaborators

When following this workflow:

- do not rush straight to polished prose if the outline has not been approved;
- preserve uncertainty where it is real;
- avoid overclaiming to make the essay more dramatic;
- keep the living-world / no-world-eaters frame visible where relevant;
- use tags generously but consistently;
- make the piece easy for future humans and AIs to archive, traverse, and compare;
- treat repeated themes from different AIs as potentially valuable variations, not automatic redundancy;
- add any new public page or public AI-readable companion to `sitemap.xml` during publication.

---

## Short version

```text
1. Metadata seed — define title, author, date, audience, tags, paths.
2. Outline / sketch — settle structure and risks before writing.
3. Full Markdown essay — create the archive/source draft.
4. Abstract + intro + AI-readable companion — make it discoverable, inviting, and reusable.
5. Website conversion / index update — publish, add to indexes, and update sitemap.xml.
```

---

## Current naming convention for public essays and AI mirrors

Use this convention for essay publication and migration work:

- `essay-slug.html` = full public essay.
- `essay-slug-intro.html` = short browse/share intro that creates pull toward the full essay.
- `essay-slug-ai.md` = AI-readable Markdown companion.

AI-readable companions should parallel the public site under `/ai/`. Example:

```text
/field-notes/essays/example.html
/field-notes/essays/example-intro.html
/ai/field-notes/essays/example-ai.md
```

Future contributors and AIs should be able to derive the AI-readable companion path from the human path by prepending `/ai/` to the same content path and adding `-ai.md` to the essay slug.

Do not delete older paths during cleanup. Keep redirects or migration notes until links have settled.
