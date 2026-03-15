# Deployment

**Version:** 1.1.0

Git Page Docs runs as a Next.js app with two major targets: local server and GitHub Pages.

## Local deployment

Use:

1. 
pm run build`
2. 
pm start`

This runs Node + Next.js runtime with the local `gitpagedocs/` folder.

## GitHub Pages deployment

In GitHub Actions builds:

- `GITHUB_ACTIONS=true`
- static export behavior is enabled by configuration
- repository search home is always enabled

## Publish flow

Package publish:

- bump version in `package.json`
- run 
pm publish --access public`
- ensure npm auth is valid (
pm whoami`)

If publishing prebuilt artifacts on Windows is skipped, use CI for `build:prebuilt`.
