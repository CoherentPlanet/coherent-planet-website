# coherent-planet-website

Website for the Coherent Planet project.

## Human-facing pages and AI-readable mirrors

Coherent Planet keeps public pages and AI-readable mirrors side by side by convention.

For essay content, use this filename pattern:

- `essay-slug.html` — full public essay page.
- `essay-slug-intro.html` — short browse/share intro page that creates pull toward the full essay.
- `essay-slug-ai.md` — AI-readable Markdown companion.

AI-readable companions should parallel the public-site path under `/ai/`. For example:

```text
/field-notes/essays/example.html
/field-notes/essays/example-intro.html
/ai/field-notes/essays/example-ai.md
```

During migrations, do not delete older paths immediately. Keep old pages as redirects or migration notes until external links have had time to settle.

Current essay examples:

- `/field-notes/essays/not-nothing-intro.html`
- `/field-notes/essays/not-nothing.html`
- `/ai/field-notes/essays/not-nothing-ai.md`
- `/field-notes/essays/care-is-a-form-of-intelligence-intro.html`
- `/field-notes/essays/care-is-a-form-of-intelligence.html`
- `/ai/field-notes/essays/care-is-a-form-of-intelligence-ai.md`

## AI-readable structure

AI-readable pages should mirror the human-facing structure where practical. For example, the SCAR compact reference lives at:

```text
/ai/tools-for-thinking/scar/scar-overview.md
```
