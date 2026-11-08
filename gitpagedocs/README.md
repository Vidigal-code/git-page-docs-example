# GitPageDocs content contract

This folder is the documentation input for the GitPageDocs viewer. Its active version, **0.0.21**, documents GitPageDocs itself in English, Portuguese and Spanish. It is maintained as curated content; do not replace it blindly with a generic scaffold.

## Files and ownership

| Location | Responsibility |
| --- | --- |
| `config.json` | Site identity, languages, theme source, reading controls and version catalog |
| `langs/en.json`, `langs/pt.json`, `langs/es.json` | Interface labels from the GitPageDocs language bundles |
| `docs/versions/0.0.21/config.json` | Public routes, translated menu destinations, page composition and container pagination |
| `docs/versions/0.0.21/{en,pt,es}/*.md` | Product documentation; matching filenames across languages |
| `docs/versions/0.0.21/{en,pt,es}/configuration-map.html` | Local visual explanation of the GitPageDocs configuration layers |
| `icon.svg` | Preserved site icon |
| `docs/versions/0.0.17`, `docs/versions/0.0.8` | Preserved historical documentation and route contracts |

A documentation version is independent of a Git branch or commit. The root catalog orders the available versions; adding a directory alone does not add a selectable version. Keep `VersionControl.versions[].path` and `PathConfig` aligned with the real configuration file.

## Current navigation

The Markdown tree groups setup, reading, automation, operation and contribution. Parent documents are useful introductions and can coexist with submenus. All active routes are public. The active version does not configure external authentication providers or put unrelated media into product pages.

Markdown menu destinations use real localized `.md` paths. The local HTML map uses its localized `.html` path. Source-viewer and composed pages use `page:<id>` aliases. Pages 39 and 50 are composed examples, and route 51 owns a three-item Markdown pagination sequence. Every reference resolves to a route/file in the same version.

Each Markdown route explicitly configures `RouteGuideTags: ["h1", "h2", "h3"]`. The document guide, breadcrumbs (`RouteGuide`) and the main menu are separate controls. Use the product's [English](docs/versions/0.0.21/en/route-guide.md), [Portuguese](docs/versions/0.0.21/pt/route-guide.md) or [Spanish](docs/versions/0.0.21/es/route-guide.md) reference before narrowing tags or IDs.

## Update a page

Edit the Markdown in each language. Keep filenames stable when only wording changes. Preserve code examples and JSON field spelling while translating the explanations. Use headings that express the document hierarchy; ordinary `h4`–`h6` content remains visible even when the route guide indexes only the first three levels.

To add a document, add its route with a unique ID and existing file path for every enabled language, then add the translated menu entry. To add a composed block or pagination item, reference a route of the correct content type. Do not assume a menu title creates a route or that a language toggle creates translated content.

## Check the result

- Parse every changed JSON file and confirm its referenced version, route and file paths.
- Compare the document filenames and page/menu structure across all three languages.
- Render the Markdown through the GitPageDocs pipeline; verify headings, anchor IDs, code examples and links.
- Open main and nested menu entries, composed pages and pagination in the viewer.
- Repeat important reading paths at the widths in the responsive guide, including resizing with a menu or guide open.
- Confirm historical version files remain unchanged unless their maintenance was explicitly part of the change.

Markdown and JSON use their parser/renderer validation. There is no TypeScript application or local test runner in this repository. HTML examples should be validated as HTML and exercised inside the viewer; runtime behavior is tested in the main GitPageDocs repository.

## Reuse canonical product material

The official content sources are `cli/content/` in the [GitPageDocs source repository](https://github.com/Vidigal-code/git-page-docs/tree/main/cli/content), with route defaults and metadata under `cli/builders/` and `cli/data/`. Update factual references from those sources, then preserve this site's focused examples, repository identity, translations and historical paths.

The official theme catalog is pinned to `v0.0.21`. A new pin should correspond to the GitPageDocs release used by the viewer. Do not confuse that product tag with a release of this documentation repository. The Source code container points to the product implementation; site/version repository links identify this documentation repository.
