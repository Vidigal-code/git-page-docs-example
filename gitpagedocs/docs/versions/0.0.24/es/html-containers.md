# Contenedores HTML para GitPageDocs

Usa una ruta HTML cuando una explicación de GitPageDocs necesite un documento visual independiente. Esta documentación incluye un mapa de configuración: conecta la configuración raíz, las rutas de versión, los archivos traducidos y el visor. El mapa no depende de scripts externos, cuentas ni contenido multimedia ajeno al producto.

## Añade una ruta local

Combina el fragmento con la configuración de la versión. Conserva las rutas existentes y usa IDs únicos para los nuevos destinos.

```json
{"routes-html":[{"id":29,"title":{"en":"GitPageDocs configuration map","pt":"Mapa de configuração GitPageDocs","es":"Mapa de configuración GitPageDocs"},"path":{"en":"gitpagedocs/docs/versions/0.0.24/en/configuration-map.html","pt":"gitpagedocs/docs/versions/0.0.24/pt/configuration-map.html","es":"gitpagedocs/docs/versions/0.0.24/es/configuration-map.html"},"fullscreenEnabled":true,"blockLink":true,"container":520}]}
```

Crea cada archivo HTML UTF-8 antes de enlazarlo. En `menus-header-html`, usa la ruta del archivo del idioma correspondiente como `path-click`; una etiqueta no crea el archivo. El mapa actual aparece en el menú HTML y en los ejemplos combinados y paginados.

## Dimensiones y diseño

Un número positivo en `container` define la altura en píxeles; `"full"` usa el comportamiento de contenedor completo. `fullscreenEnabled` habilita la acción de pantalla completa. Incluye la metaetiqueta viewport, texto legible, anchos flexibles y enlaces accesibles con teclado. Mantén los estilos en el archivo o usa URLs explícitas de confianza: el HTML local se carga mediante `srcDoc`, por lo que los recursos no se resuelven automáticamente con respecto al archivo original.

## Páginas externas

Una ruta externa usa `url: {"es":"https://example.com/gitpagedocs-demo"}` en lugar de `path`; incluye los otros idiomas habilitados. El servidor externo puede bloquear la incorporación por sus propias políticas. Comprueba el destino publicado y ofrece una forma adecuada de abrirlo fuera del iframe. `blockLink: true` establece una nueva pestaña como destino predeterminado de los enlaces locales; no bloquea la navegación por scripts.

## Confianza y mantenimiento

Revisa el HTML local y cada dependencia externa. El iframe actual permite scripts y contenido del mismo origen, por lo que no es una barrera de seguridad para HTML arbitrario no confiable. No incluyas credenciales en documentos o URLs. Los archivos estáticos públicos siguen siendo públicos aunque el menú o la ruta estén ocultos.

Prueba el contenedor en los anchos descritos en [Pantallas estrechas y plegables](responsive-layout.md), con teclado, cambios de tema y salida de pantalla completa. Al cambiar una ruta, actualiza el archivo HTML, la configuración y el menú juntos.

> Versión: 0.0.24
