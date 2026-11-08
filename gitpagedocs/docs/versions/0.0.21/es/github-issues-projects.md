# Informa y planifica cambios en GitPageDocs

Usa el [repositorio oficial GitPageDocs](https://github.com/Vidigal-code/git-page-docs) para fallos del visor, CLI, tools y MCP. Usa este repositorio de ejemplo para sus textos, traducciones y configuración. Identifica qué repositorio es responsable del comportamiento antes de abrir una issue.

## Haz reproducible el informe

Registra URL de la página, versión de documentación, idioma, tema, navegador y ancho de ventana. Explica el resultado esperado, lo observado y la secuencia mínima para reproducirlo. En un teléfono plegado o con pantalla dividida, registra el ancho CSS disponible y la orientación además del modelo comercial.

Para problemas de configuración, incluye un fragmento mínimo de los archivos raíz/versión y el título o marcador Markdown afectado. Elimina tokens, URLs privadas y datos no relacionados. Para CLI/MCP, indica `gitpagedocs version`, comando o herramienta, directorio del proceso y error relevante. Distingue una respuesta `isError` de un texto devuelto correctamente.

## Elige evidencias útiles

- Destino de menú ausente: incluye `path-click` traducido, ruta y archivo correspondiente.
- Guía incorrecta: incluye `RouteguideBrand`, `RouteGuideTags`, filtros por ID y elemento renderizado afectado.
- Desbordamiento móvil: registra la ruta y el ancho exacto; comprueba si afecta a un bloque de código o a toda la página.
- Fallo de publicación: indica el paso del workflow y el commit de despliegue, sin credenciales.
- Fallo de medios o proveedor externo: registra la dependencia y el error por separado del comportamiento del visor.

## Sigue el trabajo hasta un resultado verificable

Un GitHub Project puede agrupar documentación, runtime, accesibilidad y publicación. Define una condición observable para cada elemento, como abrir un destino traducido en 320 píxeles CSS. Vincula la implementación con su prueba o comprobación manual. Cerrar una issue no demuestra por sí solo compatibilidad con un dispositivo o navegador.

En una pull request, describe el comportamiento anterior y nuevo, el alcance y las comprobaciones realizadas. Sigue las instrucciones del repositorio oficial para código; los cambios de contenido de este ejemplo no necesitan inventar una compilación de aplicación o una API.

> Versión: 0.0.21
