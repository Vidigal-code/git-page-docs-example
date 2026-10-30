# Primeros pasos

Ejemplo consumidor de GitPageDocs con configuración, icono, traducciones y Markdown versionado. No es código fuente del CLI/visor. No tiene backend, banco, autenticación de aplicación ni package.json de aplicación. Contenido actual usa contrato 0.0.17; 0.0.8 permanece como histórico.

## Configuración y despliegue

Edite solo gitpagedocs. No existe workflow de despliegue documental aquí. Actualizar no publica en GitHub Pages ni ejecuta --push/deploy. Compruebe CLI con comando fijado en README interno. Ante 404 revise VersionControl, paths, idioma y archivos. Identidad incorrecta: ProjectLink/source-viewer; tema: URLs oficiales. README raíz describe base histórica 0.0.8 y queda fuera de este cambio limitado.

## Comandos de ejecución

```sh
npx --yes --package @gitpagedocs/cli@0.0.17 gitpagedocs version
```

Los nombres proceden solo de archivos de ejemplo y referencias del código. Configure los valores localmente; se excluyen credenciales privadas. NEXT_PUBLIC_ y VITE_ son variables públicas en el navegador.

## Archivos relacionados

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navegación

- [Project guide](?menu=es&lang=es&id=13)
- [Source reference](?menu=es&lang=es&id=14)
