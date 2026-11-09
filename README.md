# GitPageDocs documentation

Detailed documentation and working configuration examples for **GitPageDocs**: the repository documentation viewer, its CLI, shared tools and MCP server. This repository contains Markdown, JSON and local HTML documentation assets. The product implementation is maintained in [Vidigal-code/git-page-docs](https://github.com/Vidigal-code/git-page-docs).

[Open the documentation](https://vidigal-code.github.io/git-page-docs/Vidigal-code/git-page-docs-example/) · [Product source](https://github.com/Vidigal-code/git-page-docs) · [CLI reference](https://github.com/Vidigal-code/git-page-docs/blob/main/cli/README.md) · [MCP reference](https://github.com/Vidigal-code/git-page-docs/blob/main/mcp/README.md)

## Read in your language

| Language | Start | Configuration | Document guide | Narrow and foldable screens |
| --- | --- | --- | --- | --- |
| English | [Getting started](gitpagedocs/docs/versions/0.0.24/en/getting-started.md) | [Reference](gitpagedocs/docs/versions/0.0.24/en/configuration.md) | [RouteGuideTags](gitpagedocs/docs/versions/0.0.24/en/route-guide.md) | [Responsive reading](gitpagedocs/docs/versions/0.0.24/en/responsive-layout.md) |
| Português | [Primeiros passos](gitpagedocs/docs/versions/0.0.24/pt/getting-started.md) | [Referência](gitpagedocs/docs/versions/0.0.24/pt/configuration.md) | [RouteGuideTags](gitpagedocs/docs/versions/0.0.24/pt/route-guide.md) | [Leitura responsiva](gitpagedocs/docs/versions/0.0.24/pt/responsive-layout.md) |
| Español | [Primeros pasos](gitpagedocs/docs/versions/0.0.24/es/getting-started.md) | [Referencia](gitpagedocs/docs/versions/0.0.24/es/configuration.md) | [RouteGuideTags](gitpagedocs/docs/versions/0.0.24/es/route-guide.md) | [Lectura adaptable](gitpagedocs/docs/versions/0.0.24/es/responsive-layout.md) |

The active documentation version is **0.0.24**. The selector also preserves **0.0.21**, **0.0.17** and **0.0.8** as historical snapshots, including their original file paths. The new version is focused entirely on GitPageDocs; historical snapshots retain the examples originally published with them.

## Documentation map

The active version has 37 Markdown documents per language, a translated HTML configuration map, 36 Markdown routes and two composed examples. The index is also available as the fallback document.

- **Start:** installation, the documentation contract, product overview and feature reference.
- **Configure your site:** root/version configuration, complete JSON recipes, themes, icons, menus, breadcrumbs, the document guide and narrow-screen behavior.
- **Read and explore:** focus mode, narration/accessibility, PDF and HTML containers, ordered content blocks, independent pagination and explicit Markdown markers.
- **Automate and integrate:** CLI commands, MCP tools/resources and the boundaries of route authorization.
- **Publish and maintain:** deployment, migration, troubleshooting and frequently asked questions.
- **Develop GitPageDocs:** package architecture, source-of-truth files, contribution and validation.
- **Git and GitHub:** reviewing documentation changes, reporting reproducible defects and planning work against observable outcomes.

The 0.0.24 edition covers fixed theme families with independent light/dark modes, the GitHub-style source viewer with folders and breadcrumbs, lightweight background effects, and the desktop document guide that follows its content height and marks the active entry.

The combined example uses the actual installation and configuration documents plus the HTML configuration map. The paginated example uses a three-document learning path. The active catalog includes no unrelated video, music or game content.

## Repository structure

```text
README.md
gitpagedocs/
  README.md
  config.json
  icon.svg
  langs/
    en.json
    pt.json
    es.json
  docs/versions/
    0.0.24/
      config.json
      en/
      pt/
      es/
    0.0.21/
    0.0.17/
    0.0.8/
```

`gitpagedocs/config.json` controls the site and registered versions. Each version configuration connects route IDs, translated paths, menus and composed pages. The bundles under `langs/` translate interface controls; the documents under each language directory translate the actual content.

## Configure the document guide

Version 0.0.24 uses an explicit selection on every Markdown route:

```json
{
  "RouteguideBrand": true,
  "RouteGuideTags": ["h1", "h2", "h3"],
  "RouteGuideSpeciFicbrand": [],
  "RouteguideBrandPosition": "left"
}
```

`RouteguideBrand` enables automatic document-outline entries; explicit Markdown markers remain available when it is false. `RouteGuideTags` chooses safe rendered HTML element types for automatic indexing. Omitting the list preserves legacy h1–h6 indexing; an empty list disables automatic entries while preserving explicit Markdown markers. `RouteGuideSpeciFicbrand` filters eligible entries by ID. `RouteGuide` is a separate setting for breadcrumbs. See the translated guide for full examples.

## Maintain this documentation

1. Edit the active version's Markdown in `en`, `pt` and `es`, preserving technical meaning and valid UTF-8.
2. Update routes and translated menu destinations together when adding or moving a document.
3. Keep older version folders and registered paths unless an intentional migration provides replacements.
4. Validate JSON, file references, links, markers, menus and the rendered result in the GitPageDocs viewer.
5. Inspect `git diff --check`, the complete diff and new files before committing.

This repository has no local application manifest or build pipeline. Runtime tests and builds belong to the [GitPageDocs source repository](https://github.com/Vidigal-code/git-page-docs). The CLI is useful for generating a new candidate, but it is not a merge tool for customized documentation: compare generated output before applying it here.

For narrow screens and foldable devices, the documentation provides a repeatable matrix at 280, 320, 344, 390 and 768 CSS pixels. This is a verification procedure, not a blanket certification of every Galaxy Z Fold model, browser, orientation or zoom level.

## Publication and references

The official viewer can load this public repository after its documentation changes are pushed. A dedicated exported site has a separate build/deployment lifecycle; see the deployment guide before choosing that model. This repository does not contain a separate backend, database or product API.

Site identity and version metadata point to this documentation repository. The Source code container deliberately points to the official GitPageDocs implementation so that the architecture references can be followed in the product's code.

The viewer integration targets GitPageDocs **0.0.25** while this documentation edition retains its **0.0.24** identifier and paths. On screens wider than 1024 CSS pixels, the side guide uses the available viewport height before scrolling, taking precedence over TocScrollMaxHeightDesktop. Centered guides above the content and layouts at 1024 pixels and below retain their previous sizing rules.
