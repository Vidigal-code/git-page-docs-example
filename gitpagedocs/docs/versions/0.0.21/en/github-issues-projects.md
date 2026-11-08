# Report and plan GitPageDocs changes

Use the [official GitPageDocs repository](https://github.com/Vidigal-code/git-page-docs) for viewer, CLI, tools and MCP defects. Use this example repository for its own text, translations and configuration. Identify which repository owns the behavior before opening an issue.

## Make a report reproducible

Record the page URL, selected documentation version, language, theme, browser and viewport width. Explain the expected behavior, what happened and the smallest sequence that reproduces it. For a folded or split-screen phone, record the available CSS width and orientation instead of only its commercial model name.

For a configuration problem, include a minimal root/version fragment and the relevant Markdown heading or marker. Remove tokens, private URLs and unrelated data. For CLI/MCP problems, include `gitpagedocs version`, the command or tool name, process directory and the relevant error. Distinguish a tool's `isError` response from valid returned text.

## Choose the right evidence

- Missing menu destination: include its localized `path-click`, matching route and file path.
- Wrong document guide: include `RouteguideBrand`, `RouteGuideTags`, ID filters and the affected rendered element.
- Mobile overflow: include the route and exact viewport; test whether the overflow belongs to a code block or the whole page.
- Publication failure: include the workflow step and deployment commit, without credentials.
- External media/provider failure: record the dependency and error separately from the viewer behavior.

## Track work to a verifiable outcome

A GitHub Project can group documentation, runtime, accessibility and publication work. Give each item an observable acceptance condition, such as opening a translated menu destination at 320 CSS pixels. Link the implementation change and its test or manual verification. Avoid claiming a device/browser combination is supported solely because a related issue was closed.

For a pull request, describe the concrete behavior before and after, the scope of the change and the checks performed. Follow the source repository's contribution instructions for code; content-only changes in this example do not require inventing an application build or API.

> Version: 0.0.21
