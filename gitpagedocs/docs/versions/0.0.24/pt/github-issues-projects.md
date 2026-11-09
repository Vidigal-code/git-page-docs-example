# Relate e planeje mudanças no GitPageDocs

Use o [repositório oficial GitPageDocs](https://github.com/Vidigal-code/git-page-docs) para defeitos do visualizador, CLI, tools e MCP. Use este repositório de exemplo para seus textos, traduções e configuração. Identifique qual repositório é responsável pelo comportamento antes de abrir uma issue.

## Torne o relato reproduzível

Registre URL da página, versão da documentação, idioma, tema, navegador e largura da janela. Explique o resultado esperado, o observado e a menor sequência que reproduz o problema. Em um celular dobrado ou com tela dividida, registre a largura CSS disponível e a orientação, além do modelo comercial.

Para problemas de configuração, inclua um fragmento mínimo dos arquivos raiz/versão e o título ou marcador Markdown afetado. Remova tokens, URLs privadas e dados sem relação. Para CLI/MCP, informe `gitpagedocs version`, comando ou tool, diretório do processo e erro relevante. Diferencie uma resposta `isError` de um retorno de texto válido.

## Escolha evidências úteis

- Destino de menu ausente: informe `path-click` traduzido, rota e caminho do arquivo correspondente.
- Guia incorreto: inclua `RouteguideBrand`, `RouteGuideTags`, filtros de ID e elemento renderizado afetado.
- Transbordamento móvel: informe rota e largura exata; confira se ocorre dentro de um bloco de código ou na página inteira.
- Falha de publicação: informe etapa do workflow e commit do deploy, sem credenciais.
- Falha de mídia ou provedor externo: registre a dependência e o erro separadamente do comportamento do visualizador.

## Acompanhe até um resultado verificável

Um GitHub Project pode agrupar documentação, runtime, acessibilidade e publicação. Defina uma condição observável para cada item, como abrir um destino traduzido em 320 pixels CSS. Relacione a implementação ao teste ou à verificação manual. Fechar uma issue não comprova por si só compatibilidade com um aparelho ou navegador.

No pull request, descreva o comportamento antes/depois, o escopo e as verificações realizadas. Siga as instruções do repositório oficial para código; mudanças somente de conteúdo neste exemplo não exigem inventar build de aplicativo ou API.

> Versão: 0.0.24
