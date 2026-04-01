```markdown
# blog Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns, coding conventions, and common workflows for the `blog` repository. The codebase is primarily JavaScript, structured for use with the Go framework (likely Hugo for static site generation). It supports multi-language content, AI-powered features, and customizable layouts. This guide will help you contribute effectively, maintain consistency, and automate frequent tasks using suggested commands.

## Coding Conventions

- **File Naming:**  
  Use camelCase for JavaScript and CSS files.  
  _Example:_  
  ```
  searchPalette.js
  customStyles.css
  ```

- **Import Style:**  
  Always use relative imports in JavaScript files.  
  _Example:_  
  ```js
  import { fetchPosts } from './apiUtils.js';
  ```

- **Export Style:**  
  Use named exports for modules.  
  _Example:_  
  ```js
  // In blogUtils.js
  export function formatDate(date) { ... }
  export function getPostSlug(title) { ... }
  ```

- **Commit Messages:**  
  - Prefix with `feat` for new features, `fix` for bug fixes.
  - Freeform message after the prefix.
  - Average length: ~51 characters.
  _Examples:_  
  ```
  feat: add AI-powered search palette
  fix: correct post date formatting in listing
  ```

## Workflows

### Add or Update Blog Post
**Trigger:** When you want to publish a new article or update an existing post.  
**Command:** `/new-post`

1. Create or update a markdown file in one of:
    - `content/en/posts/`
    - `content/zh/posts/`
    - `content/en/ai-technology/posts/`
    - `content/zh/ai-technology/posts/`
    - `content/en/growth/posts/`
    - `content/zh/growth/posts/`
2. If needed, add or update `_index.md` in the relevant section.
3. Optionally, add images to `static/images/posts/`.
4. Optionally, update `layouts/partials/index_profile.html` or other partials for homepage display.

_Example:_  
```bash
# Add a new English post
touch content/en/posts/my-new-post.md

# Add an image
cp my-image.png static/images/posts/my-new-post/
```

### Site Visual or Layout Enhancement
**Trigger:** When you want to improve the site's look, layout, or user experience.  
**Command:** `/improve-layout`

1. Edit `assets/css/extended/custom.css` (and/or other CSS files).
2. Update or add HTML partials in `layouts/partials/` or `layouts/_default/`.
3. Optionally, update `config.yml` for site-wide settings.
4. Optionally, add new JS or CSS files in `static/js/` or `assets/css/extended/`.

_Example:_  
```css
/* assets/css/extended/custom.css */
.hero-title {
  font-size: 2.5rem;
  color: #222;
}
```
```html
<!-- layouts/partials/header.html -->
<header>
  <h1 class="hero-title">{{ .Site.Title }}</h1>
</header>
```

### AI Chat or Search Feature Development
**Trigger:** When you want to add or enhance AI-powered chat or search functionality.  
**Command:** `/add-ai-feature`

1. Edit or create Netlify function files, e.g., `netlify/functions/blog-ai.js`.
2. Edit or create frontend logic in `assets/js/search-palette.js` or `static/js/`.
3. Update UI partials: `layouts/partials/index_profile.html` or `layouts/partials/search-palette.html`.
4. Optionally, update `netlify.toml` for deployment or configuration.

_Example:_  
```js
// netlify/functions/blog-ai.js
export async function handler(event, context) {
  // AI chat logic here
}
```
```js
// assets/js/search-palette.js
import { fetchSuggestions } from './aiUtils.js';
```

### Documentation Update (README)
**Trigger:** When you want to update documentation or reflect latest changes in the README.  
**Command:** `/update-readme`

1. Edit `README.md` to update documentation or feeds.
2. Commit with a message referencing docs or feed update.

_Example:_  
```bash
vim README.md
git add README.md
git commit -m "docs: update usage instructions"
```

## Testing Patterns

- **Test File Naming:**  
  Test files follow the `*.test.*` pattern (e.g., `utils.test.js`).
- **Testing Framework:**  
  Not explicitly detected; check existing test files for framework usage.
- **Test Example:**  
  ```js
  // utils.test.js
  import { formatDate } from './blogUtils.js';

  test('formats date correctly', () => {
    expect(formatDate('2024-06-01')).toBe('June 1, 2024');
  });
  ```

## Commands

| Command         | Purpose                                         |
|-----------------|-------------------------------------------------|
| /new-post       | Add or update a blog post                       |
| /improve-layout | Enhance site visuals, layout, or UX             |
| /add-ai-feature | Add or improve AI chat or search functionality  |
| /update-readme  | Update documentation (README.md)                |
```