# Git Page Docs Example

This repository is an example of a documentation project generated with `gitpagedocs` **0.0.7**.
It demonstrates versioned content, multi-language pages, and centralized configuration through `gitpagedocs/config.json`.

## What is included

- Versioned documentation under `gitpagedocs/docs/versions/`
- Three languages: English (`en`), Portuguese (`pt`), and Spanish (`es`)
- A main project configuration file: `gitpagedocs/config.json`
- A per-version configuration file: `gitpagedocs/docs/versions/0.0.7/config.json`
- Interface translations under `gitpagedocs/langs/`

## Project structure

```text
gitpagedocs/
  config.json
  icon.svg
  langs/
    en.json
    pt.json
    es.json
  docs/
    versions/
      0.0.7/
        config.json
        en/*.md
        pt/*.md
        es/*.md
```

## Getting started

Regenerate or initialize the docs structure with the CLI (published as `@gitpagedocs/cli`, bin `gitpagedocs`):

```bash
npx @gitpagedocs/cli
```

Or install it globally:

```bash
npm install -g @gitpagedocs/cli
gitpagedocs
```

## Editing documentation

- Edit markdown pages inside `gitpagedocs/docs/versions/<version>/<language>/`
- Update global behavior in `gitpagedocs/config.json`
- Update version-specific settings in each version `config.json`
- Update interface texts in `gitpagedocs/langs/<language>.json`

## View docs

Use the official Git Page Docs website and point it to this repository:

- https://vidigal-code.github.io/git-page-docs/

Then fill in the GitHub owner and repository name to load the docs.

## Source

- CLI and runtime: https://github.com/Vidigal-code/git-page-docs
