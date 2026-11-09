# Containers HTML para GitPageDocs

Use uma rota HTML quando uma explicação do GitPageDocs se beneficiar de um documento visual independente. Esta documentação inclui um mapa de configuração: ele conecta configuração raiz, rotas da versão, arquivos traduzidos e visualizador. O mapa não depende de scripts externos, conta ou mídia sem relação com o produto.

## Adicione uma rota local

Mescle o trecho na configuração da versão. Preserve as rotas existentes e use IDs exclusivos para novos destinos.

```json
{"routes-html":[{"id":29,"title":{"en":"GitPageDocs configuration map","pt":"Mapa de configuração GitPageDocs","es":"Mapa de configuración GitPageDocs"},"path":{"en":"gitpagedocs/docs/versions/0.0.24/en/configuration-map.html","pt":"gitpagedocs/docs/versions/0.0.24/pt/configuration-map.html","es":"gitpagedocs/docs/versions/0.0.24/es/configuration-map.html"},"fullscreenEnabled":true,"blockLink":true,"container":520}]}
```

Crie cada arquivo HTML UTF-8 antes de ligá-lo ao menu. Em `menus-header-html`, use o caminho do arquivo no idioma correspondente como `path-click`; um rótulo não cria o arquivo. O mapa atual está no menu HTML e nos exemplos combinados e paginados.

## Dimensões e layout

Um número positivo em `container` define altura em pixels; `"full"` usa o comportamento de container completo. `fullscreenEnabled` habilita a ação de tela cheia do visualizador. Inclua meta tag de viewport, texto legível, larguras flexíveis e links acessíveis por teclado dentro do documento. Mantenha os estilos no arquivo ou use URLs explícitas e confiáveis: o HTML local entra por `srcDoc` do iframe, portanto os recursos não são resolvidos automaticamente em relação ao arquivo original.

## Páginas externas

Uma rota externa usa `url: {"pt":"https://example.com/gitpagedocs-demo"}` no lugar de `path`; informe também os outros idiomas habilitados. O servidor externo pode impedir a incorporação pelas próprias políticas. Confira o destino publicado e ofereça uma forma adequada de abri-lo fora do iframe. `blockLink: true` define nova aba como padrão dos links locais; não bloqueia navegação feita por scripts.

## Confiança e manutenção

Revise o HTML local e cada dependência externa. O iframe atual permite scripts e conteúdo de mesma origem, portanto não é uma barreira de segurança para HTML arbitrário não confiável. Não inclua credenciais no documento ou na URL. Arquivos estáticos públicos continuam públicos mesmo com menu ou rota ocultos.

Teste o container nas larguras descritas em [Telas estreitas e dobráveis](responsive-layout.md), com teclado, troca de tema e saída de tela cheia. Quando um caminho mudar, atualize o arquivo HTML, a rota e o menu em conjunto.

> Versão: 0.0.24
