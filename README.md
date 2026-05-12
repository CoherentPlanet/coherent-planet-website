# coherent-planet-website

Website for the Coherent Planet project.

## Human-facing pages and AI-readable mirrors

Coherent Planet keeps public pages and AI-readable mirrors side by side by convention.

For essay content, use this filename pattern:

- `essay-slug-summary.html` — short public summary page.
- `essay-slug.html` — full public essay page.
- `essay-slug-ai.md` — AI-readable Markdown mirror.

AI-readable mirrors should parallel the public-site path under `/ai/`. For example:

```text
/field-notes/essays/example-summary.html
/field-notes/essays/example.html
/ai/field-notes/essays/example-ai.md
```

During migrations, do not delete older paths immediately. Keep old pages as redirects or migration notes until external links have had time to settle.

Current essay examples:

- `/field-notes/essays/not-nothing-summary.html`
- `/field-notes/essays/not-nothing.html`
- `/ai/field-notes/essays/not-nothing-ai.md`
- `/field-notes/essays/care-is-a-form-of-intelligence-summary.html`
- `/field-notes/essays/care-is-a-form-of-intelligence.html`
- `/ai/field-notes/essays/care-is-a-form-of-intelligence-ai.md`
