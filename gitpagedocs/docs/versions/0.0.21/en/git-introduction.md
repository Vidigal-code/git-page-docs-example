# Git for GitPageDocs documentation

Git keeps the Markdown, configuration and assets of a GitPageDocs site versioned together. A documentation version in `VersionControl.versions` is a reader-facing label; a Git commit records a concrete repository state. They solve different needs and do not have to use the same identifier.

## Make a focused documentation change

```sh
git status --short
git switch -c docs/gitpagedocs-navigation
```

Edit the relevant Markdown files in each enabled language. If a filename or page identity changes, update the version configuration and localized menu destinations in the same change. Keep historical paths when existing links still depend on them.

## Inspect the complete result

```sh
git diff --check
git diff -- gitpagedocs/config.json gitpagedocs/docs/versions/0.0.21
```

Check JSON syntax, referenced files, translations and the actual viewer before committing. A clean diff does not prove that a menu destination renders. Review new untracked files too; they do not appear in ordinary `git diff` until staged.

## Save and publish deliberately

Stage only the reviewed files, inspect `git diff --cached`, then create a commit describing the documentation behavior. A push updates the remote repository; an independent hosting workflow may still need to run before its site changes. The official repository viewer reads repository content, while an exported site uses the files from its build.

Avoid rerunning the generator on hand-edited documentation just to publish. Generate a candidate in a separate output folder and compare it, as described in [Migration](migration.md). Keep credentials and local machine files outside the staged changes.

## Recover a mistaken change

For an already shared change, review a targeted `git revert COMMIT` instead of rewriting shared history. Confirm the resulting configuration and published page. Preserve useful content changes when the problem is only a menu path or version pointer; recovery should match the actual fault.

Use [Issues and Projects](github-issues-projects.md) to record a reproducible problem and [Contributing](contributing.md) when the fix belongs to the GitPageDocs runtime.

> Version: 0.0.21
