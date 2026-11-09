# GitPageDocs

GitPageDocs é um runtime de documentação multi-idioma para repositórios que possuem a pasta `gitpagedocs/`.

## O que este projeto entrega

- Renderização markdown em varios idiomas (`en`, `pt`, `es`)
- Roteamento por versão (`/v/:versao`)
- Sistema de temas por templates JSON
- Execução local e em GitHub Pages
- Busca de repositório + renderização remota opcional

## Contrato de pastas

O runtime espera esta estrutura:

- `gitpagedocs/config.json`
- `gitpagedocs/docs/<lang>/*.md`
- `gitpagedocs/docs/versions/<versao>/config.json`
- `gitpagedocs/docs/versions/<versao>/<lang>/*.md`
- `gitpagelayouts/layoutsConfig.json`
- `gitpagelayouts/templates/*.json`

## Navegação rápida

- Abra **Primeiros passos** para setup local.
- Abra **Configuração** para detalhes completos do `config.json`.
- Abra **Publicação** para comportamento local/produção/GitHub Pages.
- Abra **Arquitetura** para mapa de código e fluxo de dados.
- Abra **Temas e layouts** para autoria de templates.
- Abra **Rotas autorizadas** para configurar chave, papeis e autenticação externa.
- Abra **FAQ** para troubleshooting.

## Referências detalhadas

- **Referência da CLI**: instalação, todos os comandos e flags de compatibilidade.
- **Servidor MCP**: cliente, 20 tools, 7 resources e configuração de provedores.
- **Navegação e submenus**: árvores recursivas, URLs e sobrescritas dos breadcrumbs.
- **Blocos de conteúdo ordenados**: repita e ordene Markdown, HTML, vídeo, áudio e PDF na mesma página; posicione títulos e descrições configurados independentemente.
- **Modo foco**: copiar/baixar Markdown e navegar por seção/documento.
- **Acessibilidade e narração**: vozes do navegador, controles e interação com mídias.
- **Documentos PDF**: prévia nativa, download/nova aba e o guia incluído em inglês.
- **Receitas de configuração**: um site multilíngue completo e um menu com seções dentro de seções.
- **Migração e compatibilidade**: atualizar configurações desde a versão 0.0.1 preservando seu conteúdo.
- **Solução de problemas**: UTF-8, caminhos locais e do Pages, carregamento de PDF, vozes e inicialização do MCP.
- **Contribuição e validação**: arquivos fonte, geração, contratos públicos e verificações de publicação.
- **Containers HTML**: páginas locais e externas, configuração de rotas/menus e o mapa de configuração do GitPageDocs.

O menu gerado mantém Primeiros passos e Visão geral do projeto no início. Guias contém Configure seu site, Leia e explore e Automatize e integre; cada categoria contém suas páginas relacionadas. Operação e desenvolvimento agrupa publicação, manutenção e contribuição. Git e GitHub contém os exemplos de repositório. As categorias podem conter outras categorias sem um limite fixo de níveis.

## Escolha o guia do documento

Use `RouteGuideTags: ["h1", "h2", "h3"]` na rota Markdown para indexar esses níveis. A lista omitida preserva h1–h6; `[]` mantém marcadores Markdown explícitos sem entradas automáticas. `RouteguideBrand` controla a indexação automática; marcadores explícitos continuam disponíveis quando ele é false. Consulte [Guia do documento](route-guide.md) e [Telas estreitas e dobráveis](responsive-layout.md) para exemplos completos.

> Versão: 0.0.24
