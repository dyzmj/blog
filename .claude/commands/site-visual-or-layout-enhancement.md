---
name: site-visual-or-layout-enhancement
description: Workflow command scaffold for site-visual-or-layout-enhancement in blog.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /site-visual-or-layout-enhancement

Use this workflow when working on **site-visual-or-layout-enhancement** in `blog`.

## Goal

Implements visual, layout, or UX improvements across the blog, often involving CSS, HTML partials, and sometimes config.

## Common Files

- `assets/css/extended/custom.css`
- `layouts/partials/*.html`
- `layouts/_default/*.html`
- `config.yml`
- `static/js/*.js`
- `assets/css/extended/*.css`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit assets/css/extended/custom.css (and/or other CSS files)
- Update or add layouts/partials/*.html or layouts/_default/*.html for structure/UX changes
- Optionally, update config.yml or related config files
- Optionally, add new static/js or static/css files for new features

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.