# Git Page Docs Example

This repository is an example of a documentation project generated with `gitpagedocs`.
It demonstrates versioned content, multi-language pages, and centralized configuration through `gitpagedocs/config.json`.

## What is included

- Versioned documentation under `gitpagedocs/docs/versions/`
- Three languages: English (`en`), Portuguese (`pt`), and Spanish (`es`)
- A main project configuration file: `gitpagedocs/config.json`
- Per-version configuration files, for example:
  - `gitpagedocs/docs/versions/1.0.0/config.json`
  - `gitpagedocs/docs/versions/1.1.0/config.json`
  - `gitpagedocs/docs/versions/1.1.1/config.json`

## Project structure

```text
gitpagedocs/
  config.json
  docs/
    versions/
      1.0.0/
        config.json
        en/*.md
        pt/*.md
        es/*.md
      1.1.0/
        config.json
        en/*.md
        pt/*.md
        es/*.md
      1.1.1/
        config.json
        en/*.md
        pt/*.md
        es/*.md
```

## Getting started

1. Install dependencies:

```bash
npm install
```

2. Regenerate or initialize docs structure (optional):

```bash
npx gitpagedocs
```

## Editing documentation

- Edit markdown pages inside `gitpagedocs/docs/versions/<version>/<language>/`
- Update global behavior in `gitpagedocs/config.json`
- Update version-specific settings in each version `config.json`

## View docs

Use the official Git Page Docs website and point it to this repository:

- https://vidigal-code.github.io/git-page-docs/

Then fill in the GitHub owner and repository name to load the docs.

## Dependency

This project uses:

- `gitpagedocs` (defined in `package.json`)
