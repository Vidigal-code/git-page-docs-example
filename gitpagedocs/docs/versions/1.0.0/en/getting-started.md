# Getting Started

**Version:** 1.0.0

This guide configures the project from zero to running docs.

## Prerequisites

- Node.js 20+
- npm 10+ (or pnpm if preferred)

## Local setup

1. Install dependencies:
   - 
pm install`
2. Generate/update docs assets:
   - 
pm run gitpagedocs`
3. Start development:
   - 
pm run dev`
4. Build + run production locally:
   - 
pm run build`
   - 
pm start`

## CLI behavior


px gitpagedocs` (or 
pm run gitpagedocs`) generates docs assets in the official `gitpagedocs/` folder.

- Generates only markdown/json artifacts
- Does not generate `index.html`
- Does not generate `index.js`
- Does not run install commands

## Repository search mode

Local repository search is controlled by environment variable:

- `GITPAGEDOCS_REPOSITORY_SEARCH=true`
- `GITPAGEDOCS_REPOSITORY_SEARCH=false`

On GitHub Pages builds (`GITHUB_ACTIONS=true`), repository search is always enabled.
