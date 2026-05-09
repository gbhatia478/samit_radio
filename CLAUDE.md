# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A static markdown reader app hosted on GitHub Pages. It fetches and renders a markdown file in the browser using `marked.js` (loaded via CDN — no build step).

## Stack

- Plain HTML/CSS/JS — no framework, no bundler
- `marked.js` via CDN for markdown parsing
- GitHub Pages for hosting

## Development

Open `index.html` directly in a browser, or serve locally to avoid CORS issues with `fetch`:

```
python3 -m http.server
```

Then visit `http://localhost:8000`.

## How it works

`index.html` fetches the `.md` file at runtime using `fetch()`, passes the content to `marked.parse()`, and injects the resulting HTML into the page. The markdown file path is configurable at the top of the `<script>` block in `index.html`.
