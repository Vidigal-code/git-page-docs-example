# HTML containers for GitPageDocs

Use an HTML route when a GitPageDocs explanation benefits from a standalone visual document. This documentation includes a configuration map: it connects the root configuration, version routes, translated files and viewer. The map has no external scripts, account requirement or unrelated media.

## Add a local route

Merge the following into the version configuration. Keep existing routes and give new destinations unique IDs.

```json
{"routes-html":[{"id":29,"title":{"en":"GitPageDocs configuration map","pt":"Mapa de configuração GitPageDocs","es":"Mapa de configuración GitPageDocs"},"path":{"en":"gitpagedocs/docs/versions/0.0.21/en/configuration-map.html","pt":"gitpagedocs/docs/versions/0.0.21/pt/configuration-map.html","es":"gitpagedocs/docs/versions/0.0.21/es/configuration-map.html"},"fullscreenEnabled":true,"blockLink":true,"container":520}]}
```

Create each UTF-8 HTML file before linking it. In `menus-header-html`, use the matching localized file path as `path-click`; a menu label does not create the source file. The current configuration map is available under its HTML menu entry and inside the combined/paginated examples.

## Size and layout

A positive `container` number sets a pixel height; `"full"` uses the full container behavior. `fullscreenEnabled` enables the viewer's fullscreen action. Include a viewport meta tag, readable text, flexible widths and keyboard-accessible links inside the HTML document. Keep styles with the document or use explicit trusted URLs: local HTML is loaded through iframe `srcDoc`, so resource paths do not automatically resolve relative to the original file.

## External pages

An external route uses `url: {"en":"https://example.com/gitpagedocs-demo"}` instead of `path`; supply the other enabled languages too. The external server may prevent embedding through its own policies. Verify the published destination and provide an appropriate way to open it outside the iframe. `blockLink: true` sets a new-tab default for local HTML links; it does not block script-driven navigation.

## Trust and maintenance

Review local HTML and every external dependency. The current iframe allows scripts and same-origin content, so it is not a security boundary for arbitrary untrusted HTML. Do not place credentials in a document or URL. Public static files remain public even when a menu or route is hidden.

Test the HTML container at the narrow widths described in [Narrow and foldable screens](responsive-layout.md), with keyboard navigation, theme changes and fullscreen exit. Update the HTML file and the matching route/menu together whenever a path changes.

> Version: 0.0.21
