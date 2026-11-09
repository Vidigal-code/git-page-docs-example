# Git para documentación GitPageDocs

Git mantiene versionados juntos el Markdown, la configuración y los recursos de un sitio GitPageDocs. Una versión en `VersionControl.versions` es una etiqueta para el lector; un commit registra un estado concreto del repositorio. Cumplen funciones distintas y no necesitan el mismo identificador.

## Haz un cambio concreto

```sh
git status --short
git switch -c docs/gitpagedocs-navigation
```

Edita los documentos de los idiomas habilitados. Si cambia un nombre de archivo o la identidad de una página, actualiza la configuración de versión y los destinos traducidos de los menús en el mismo cambio. Conserva las rutas históricas usadas por enlaces existentes.

## Comprueba el resultado completo

```sh
git diff --check
git diff -- gitpagedocs/config.json gitpagedocs/docs/versions/0.0.24
```

Valida la sintaxis JSON, los archivos referenciados, las traducciones y el visor antes del commit. Un diff sin errores no demuestra que funcione el destino del menú. Revisa también los archivos nuevos sin seguimiento; no aparecen en el `git diff` normal antes de añadirlos al área de preparación.

## Guarda y publica deliberadamente

Prepara solo los archivos revisados, comprueba `git diff --cached` y describe en el commit el comportamiento de la documentación. Un push actualiza el repositorio remoto; un workflow independiente puede necesitar ejecutarse antes de que cambie el sitio. El visor oficial de repositorios lee su contenido, mientras que una exportación usa los archivos de su compilación.

No vuelvas a ejecutar el generador sobre documentación personalizada solo para publicarla. Genera un candidato en otra carpeta y compáralo, como explica [Migración](migration.md). Mantén las credenciales y los archivos locales de la máquina fuera de los cambios preparados.

## Recupera un cambio incorrecto

Para un cambio compartido, revisa un `git revert COMMIT` específico en lugar de reescribir el historial común. Comprueba la configuración resultante y la página publicada. Conserva el contenido útil si el fallo está solo en la ruta del menú o la referencia de versión; la recuperación debe corresponder al problema.

Usa [Issues y Projects](github-issues-projects.md) para registrar un problema reproducible y [Contribución](contributing.md) cuando la corrección pertenezca al runtime de GitPageDocs.

> Versión: 0.0.24
