# Authorized routes

GitPageDocs consumer example containing configuration, icon, translations and versioned Markdown. It is not the CLI/viewer source. It has no backend, database, application authentication or application package.json. Current content uses contract 0.0.17; 0.0.8 remains in the catalog as history.

## Data contracts

Markdown/JSON in a public repository are public. Viewer auth.accessKeys/docsAccess do not make public files private; actual confidentiality requires source access controls. Do not store tokens in config, examples or URLs. Keep text alternatives, heading hierarchy and clear menu labels for accessibility.

## Workflow and failure cases

Reader opens the official viewer and selects Vidigal-code/git-page-docs-example → viewer reads root config → selects version/language → loads catalog → resolves Markdown → renders menus, outline and navigation. rendering points to the official viewer; ProjectLink/source-viewer point to this example.

Edit gitpagedocs only. This repository has no documentation deployment workflow. Updating it does not publish to GitHub Pages or run --push/deploy. Check the CLI with the pinned version command in the internal README. For 404 check VersionControl, route paths, language and files. Wrong identity: ProjectLink/source-viewer; wrong theme: official URLs. The root README describes the historical 0.0.8 baseline and remains outside this folder-only change.

## Related files

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navigation

- [Project guide](?menu=en&lang=en&id=13)
- [Source reference](?menu=en&lang=en&id=14)
