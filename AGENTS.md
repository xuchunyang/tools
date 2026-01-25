# Repository Guidelines

## Project Structure & Module Organization
This repository is a small collection of single-file HTML tools. Everything lives at the repo root.

- `index.html` lists and links to all tools.
- `*.html` files are the tools themselves (each is standalone with embedded HTML/CSS/JS).
- `CNAME` configures the GitHub Pages custom domain.
- `README.md` describes the project philosophy and usage.

When adding a new tool, place a new `*.html` file at the root and add a link in `index.html`.

## Build, Test, and Development Commands
There is no build step or backend. Open files directly or serve them locally:

```bash
open index.html
python3 -m http.server 8000
```

The `http.server` option is helpful when a tool loads assets via fetch or needs a consistent origin.

## Coding Style & Naming Conventions
- Use 4-space indentation in HTML.
- Keep each tool self-contained: inline CSS/JS or CDN scripts (for example Tailwind in `index.html`).
- Name new tools with concise kebab-case files, e.g. `markdown-preview.html`.
- Prefer clear, semantic HTML and minimal dependencies since this is a static, offline-friendly set.

## Testing Guidelines
There is no automated test suite. Validate changes by opening the tool in a browser and manually exercising core flows. If a tool modifies content (e.g., HTML formatting), test with at least one real-world input sample.

## Commit & Pull Request Guidelines
Recent history uses short, imperative messages with occasional conventional prefixes:
- `Add <tool-name>.html`
- `feat: add <tool>`
- `docs: <change>`

For pull requests, include:
- A brief description of the tool or change.
- The updated `index.html` entry.
- Screenshots or a short GIF when UI changes are visible.

## Agent-Specific Instructions
Follow the AGENTS requirements: keep updates concise, avoid unnecessary refactors, and preserve the single-file tool philosophy.
