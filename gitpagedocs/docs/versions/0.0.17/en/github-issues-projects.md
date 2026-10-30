# GitHub issues and projects

GitPageDocs consumer example containing configuration, icon, translations and versioned Markdown. It is not the CLI/viewer source. It has no backend, database, application authentication or application package.json. Current content uses contract 0.0.17; 0.0.8 remains in the catalog as history.

## Workflow and failure cases

1. Reader opens the official viewer and selects Vidigal-code/git-page-docs-example → viewer reads root config → selects version/language → loads catalog → resolves Markdown → renders menus, outline and navigation. rendering points to the official viewer; ProjectLink/source-viewer point to this example.

2. Editor changes Markdown in three languages → registers a route with a unique ID/existing path → updates menus without breaking IDs → validates JSON/links → reviews the diff. For a new version create folder/config and register a real VersionControl entry while preserving history. CLI version and consumer application version are independent concepts.

3. Version 0.0.17 supports named branch/release/commit arrays of {name,url}. Link only existing resources. This example links a real branch/commit without inventing a release. Do not run the generic scaffold over reviewed content without comparing changes; its product demonstration pages do not automatically describe this repository.

## Related files

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navigation

- [Project guide](?menu=en&lang=en&id=13)
- [Source reference](?menu=en&lang=en&id=14)
