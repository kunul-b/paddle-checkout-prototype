# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Server

Serve the static files locally with:

```bash
python3 -m http.server 3000 --directory Test
```

Then open `http://localhost:3000` in a browser.

## Project Overview

This is a static HTML/CSS/JS prototype repository for Paddle payment UI components. There is no build system, package manager, or test suite — all files are self-contained HTML pages in the `Test/` directory.

## Architecture

All prototypes live in `Test/` as standalone HTML files. Each file is self-contained with inline `<style>` and `<script>` blocks.

**Current files:**


**Design patterns used across files:**
- Multiple named variants (V1, V2, V3) side-by-side to compare UI solutions for the same problem
- State toggled via CSS class addition/removal (`.open`, `.active`, `.future`) with JS
- Consistent card component structure (`.card` with shadow, border-radius, padding)
- Smooth transitions via CSS (`transition: opacity 0.15s`, etc.)

## Figma Integration

The `.claude/settings.local.json` grants WebFetch access to `www.figma.com`. When given a Figma URL, use the Figma MCP tools to retrieve design context before implementing or modifying UI components.
