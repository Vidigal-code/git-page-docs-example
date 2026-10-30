# Introducción a Git

Ejemplo consumidor de GitPageDocs con configuración, icono, traducciones y Markdown versionado. No es código fuente del CLI/visor. No tiene backend, banco, autenticación de aplicación ni package.json de aplicación. Contenido actual usa contrato 0.0.17; 0.0.8 permanece como histórico.

## Flujo y casos de fallo

1. Lector abre visor oficial y selecciona Vidigal-code/git-page-docs-example → lee config raíz → elige versión/idioma → carga catálogo → resuelve Markdown → presenta menús/índice/navegación. rendering apunta al visor oficial; ProjectLink/source-viewer a este ejemplo.

2. Editor modifica Markdown en tres idiomas → registra route con ID único/path existente → actualiza menús sin romper IDs → valida JSON/enlaces → revisa diff. Para nueva versión cree carpeta/config y entrada real en VersionControl preservando historia. Versión CLI y versión de aplicación consumidora son conceptos independientes.

3. 0.0.17 admite arrays branch/release/commit de {name,url}. Enlace solo recursos existentes. Este ejemplo usa branch/commit reales sin inventar release. No ejecute scaffold genérico sobre contenido revisado sin comparar; sus demostraciones no describen automáticamente este repositorio.

## Archivos relacionados

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navegación

- [Project guide](?menu=es&lang=es&id=13)
- [Source reference](?menu=es&lang=es&id=14)
