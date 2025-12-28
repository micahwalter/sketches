# CLAUDE Memory File

This file contains workflow preferences and guidelines for working on this repository.

## Branching Strategy

**ALWAYS create a feature or bug fix branch before making changes to the codebase.**

- For new features: `git checkout -b feature/descriptive-name`
- For bug fixes: `git checkout -b bugfix/descriptive-name`
- Never commit directly to the `main` branch

## Documentation Requirements

**When adding new projects/sketches, ALWAYS update:**

1. **README.md** - Add the new project to the documentation
2. **index.html** (or index page) - Ensure the new project appears in the UI listing
3. **Add analytics tracking** - Include Fathom analytics code in the `<head>` section (see Analytics Template below)
4. **Add standard footer** - Include the navigation footer in every project HTML file (see Footer Template below)

## Analytics Template

**CRITICAL: Every HTML page MUST include the Fathom analytics tracking code in the `<head>` section.**

Insert this code in the `<head>` section after the `<title>` tag and before any `<style>` or other `<script>` tags:

```html
    <!-- Fathom - beautiful, simple website analytics -->
    <script src="https://cdn.usefathom.com/script.js" data-site="BQSMBQKX" defer></script>
    <!-- / Fathom -->
```

## Footer Template

**CRITICAL: Every project HTML file MUST include the standard navigation footer before the closing `</body>` tag.**

**IMPORTANT: Ensure the HTML file has `<meta charset="UTF-8">` in the `<head>` section to properly display the footer's arrow characters.**

The footer provides navigation to:
- Home page (index.html)
- GitHub source for the current project (dynamically generated)
- micahwalter.com

Insert this code before `</body>` in every new project:

```html
    <!-- Footer Navigation -->
    <div id="sketch-footer" style="
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        background: rgba(0, 0, 0, 0.7);
        backdrop-filter: blur(10px);
        padding: 12px 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 24px;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        font-size: 14px;
        z-index: 1000;
    ">
        <a href="index.html" style="color: #fff; text-decoration: none; opacity: 0.9; transition: opacity 0.2s;" onmouseover="this.style.opacity='1'" onmouseout="this.style.opacity='0.9'">← Home</a>
        <a id="github-source-link" href="#" style="color: #fff; text-decoration: none; opacity: 0.9; transition: opacity 0.2s;" onmouseover="this.style.opacity='1'" onmouseout="this.style.opacity='0.9'">View Source</a>
        <a href="https://micahwalter.com" target="_blank" rel="noopener" style="color: #fff; text-decoration: none; opacity: 0.9; transition: opacity 0.2s;" onmouseover="this.style.opacity='1'" onmouseout="this.style.opacity='0.9'">micahwalter.com →</a>
    </div>
    <script>
        // Set GitHub source link dynamically
        (function() {
            const filename = window.location.pathname.split('/').pop();
            const githubLink = document.getElementById('github-source-link');
            githubLink.href = `https://github.com/micahwalter/sketches/blob/main/${filename}`;
        })();
    </script>
</body>
</html>
```

## General Workflow

1. Create appropriate branch before starting work
2. Implement the feature or fix
3. Update documentation (README and index page if adding new projects)
4. Test changes locally
5. Commit with clear, descriptive messages
6. Create pull request for review

## Repository Context

This is a creative coding sketches repository. Each new sketch/project should be properly documented and made discoverable through both the README and the web interface.
