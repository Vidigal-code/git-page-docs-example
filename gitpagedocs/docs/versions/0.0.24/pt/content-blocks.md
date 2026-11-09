# Blocos de conteúdo ordenados

Uma página pode conter vários documentos Markdown, players HTML, vídeos, faixas de áudio e PDFs em qualquer ordem. Adicione um array `pages` no nível principal do config da versão. Cada bloco referencia uma rota já definida em `routes-md`, `routes-html`, `routes-video`, `routes-audio` ou `routes-pdf`. A página possui uma única URL; os blocos não criam destinos de navegação separados.

## Exemplo completo GitPageDocs

A página 39 deste site combina Primeiros passos (rota 1), Configuração (rota 13) e o mapa de configuração local (rota HTML 29). O exemplo contém somente conteúdo do GitPageDocs. Mescle o objeto na configuração da versão preservando as rotas e os arquivos referenciados.

```json
{
  "pages": [
    {
      "id": 39,
      "blocks": [
        {
          "id": "start",
          "type": "md",
          "routeId": 1
        },
        {
          "id": "configuration",
          "type": "md",
          "routeId": 13
        },
        {
          "id": "configuration-map",
          "type": "html",
          "routeId": 29
        }
      ]
    }
  ]
}
```

Adicione um destino traduzido com `"path-click": "page:39"`. A entrada deste site fica em Guias → Leia e explore → Guia GitPageDocs combinado. O rótulo da página é independente do título de cada bloco.

## Ordem, repetição e opções individuais

- `pages[].id` é um identificador inteiro da página. Use um ID novo que não coincida com um ID de rota existente.
- `blocks[].id` é uma string não vazia, única dentro da página. Duas instâncias podem usar o mesmo `routeId`, mas precisam de IDs de bloco diferentes.
- `type` aceita exatamente `md`, `html`, `video`, `audio` ou `pdf`; `routeId` seleciona uma rota da lista desse tipo.
- A ordem do array é a ordem de exibição. Mova um objeto para reordená-lo, remova-o para ocultar aquela instância ou copie-o com um ID novo para repetir. `hierarchyPage` continua valendo para páginas legadas e não reordena esse array.

Cada referência usa a origem, tradução, visibilidade, dimensões, ações PDF, controles de mídia e autorização da sua rota. Para dar opções diferentes a duas ocorrências do mesmo arquivo, defina duas rotas com IDs distintos e o mesmo caminho de origem; depois referencie esses IDs. Não duplique parâmetros de rota dentro do bloco.

Um bloco Markdown renderiza apenas seu documento; um áudio inline legado da rota não se transforma em bloco extra. Referencie uma rota de áudio explicitamente quando ela fizer parte da sequência. Os blocos selecionam rotas fixas e não compartilham um índice de `browseAll`. A exclusividade de mídia e as restrições do navegador continuam valendo; repetir um player não inicia reprodução automaticamente.

Modo foco e narração leem os blocos Markdown autorizados e disponíveis no idioma selecionado, na ordem do array, incluindo repetições. Copiar/baixar no foco reúne as fontes originais com duas quebras de linha e usa `page-39.md` neste exemplo. Cada container Markdown visível mantém suas ações individuais de cópia/download e o nome original do arquivo. IDs de títulos renderizados recebem um prefixo por bloco para evitar âncoras duplicadas; a fonte baixada não muda. Páginas ou blocos negados são excluídos da renderização, cópia, foco e narração. Esse controle no cliente não protege arquivos públicos nem impede o carregador de documentos de ler suas fontes.

## Posicionar títulos e descrições

Toda rota de conteúdo aceita `layout.title` e `layout.description` independentemente. `placement` vale `outside` ou `inside` do container; `position` vale `before` ou `after` do conteúdo. Combine este fragmento de apresentação com uma rota existente, preservando os campos do conteúdo:

```json
{
  "id": 13,
  "layout": {
    "title": {
      "placement": "outside",
      "position": "before"
    },
    "description": {
      "placement": "inside",
      "position": "after"
    }
  }
}
```

No Markdown, título e descrição configurados sempre ficam fora do documento renderizado; a posição antes/depois é respeitada. Títulos escritos dentro do Markdown continuam pertencendo ao documento. HTML, vídeo, áudio e PDF aceitam as duas posições de container. Esses campos mudam a apresentação, não o arquivo de origem nem o conteúdo da mídia. `titleIsVisible`, `descriptionIsVisible`, alinhamento e estilos existentes continuam valendo. Omita `layout` para manter a apresentação atual. Valores compartilhados podem ficar em `routeDefaults`; um `layout` explícito da rota substitui esse objeto dos defaults.

## Compatibilidade e acesso

Configs sem `pages` mantêm o comportamento existente de containers únicos ou rotas mistas. O array `pages` da versão sobrescreve o array raiz; `[]` limpa a lista. Definições inválidas ou referências inexistentes são ignoradas sem impedir o carregamento das outras páginas. IDs duplicados de página ou bloco preservam a primeira entrada válida; um ID de página que coincide com uma rota é ignorado para preservar a rota existente. Corrija esses erros na configuração em vez de depender da omissão.

O campo `authorization` da página protege o destino composto, e cada rota referenciada mantém suas próprias exigências de acesso. Ocultar um bloco não protege arquivos públicos. Markdown e PDF não inventam uma tradução quando falta o arquivo do idioma selecionado; os outros tipos preservam o fallback existente da rota, incluindo inglês para vídeo/áudio e URLs HTML externas. Teste todos os blocos e idiomas, navegação direta, rotas protegidas, mídias repetidas, erros de download e limites do navegador antes de publicar. Muitos embeds ou PDFs ativos consomem memória e rede; inclua apenas o que o leitor precisa.

> Versão: 0.0.24
