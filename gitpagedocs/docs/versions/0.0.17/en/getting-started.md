# Getting Started

GitPageDocs consumer example containing configuration, icon, translations and versioned Markdown. It is not the CLI/viewer source. It has no backend, database, application authentication or application package.json. Current content uses contract 0.0.17; 0.0.8 remains in the catalog as history.

## Configuration and deployment

Edit gitpagedocs only. This repository has no documentation deployment workflow. Updating it does not publish to GitHub Pages or run --push/deploy. Check the CLI with the pinned version command in the internal README. For 404 check VersionControl, route paths, language and files. Wrong identity: ProjectLink/source-viewer; wrong theme: official URLs. The root README describes the historical 0.0.8 baseline and remains outside this folder-only change.

## Execution commands

```sh
npx --yes --package @gitpagedocs/cli@0.0.17 gitpagedocs version
```

Names are extracted only from example files and environment references in source. Configure values locally; private credentials are excluded. NEXT_PUBLIC_ and VITE_ variables are public in the browser.

## Related files

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navigation

- [Project guide](?menu=en&lang=en&id=13)
- [Source reference](?menu=en&lang=en&id=14)
