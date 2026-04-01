---
name: add-or-update-blog-post
description: Workflow command scaffold for add-or-update-blog-post in blog.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-blog-post

Use this workflow when working on **add-or-update-blog-post** in `blog`.

## Goal

Adds new blog posts or updates existing ones, often in multiple languages (EN/ZH), sometimes with associated images and index files.

## Common Files

- `content/en/posts/*.md`
- `content/zh/posts/*.md`
- `content/en/ai-technology/posts/*.md`
- `content/zh/ai-technology/posts/*.md`
- `content/en/growth/posts/*.md`
- `content/zh/growth/posts/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or update markdown file(s) in content/en/posts/ or content/zh/posts/ or content/en/ai-technology/posts/ or content/zh/ai-technology/posts/ or content/en/growth/posts/ or content/zh/growth/posts/
- If needed, add or update _index.md in the relevant section
- Optionally, add associated images to static/images/posts/
- Optionally, update layouts/partials/index_profile.html or other partials for homepage display

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.