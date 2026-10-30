# Rotas autorizadas

Exemplo de consumo do GitPageDocs, formado por configuração, ícone, traduções e Markdown versionado. Não é o código-fonte do CLI nem do viewer. Não possui backend, banco, autenticação de aplicação ou package.json de aplicação. O conteúdo atual usa o contrato 0.0.17; 0.0.8 permanece no catálogo como histórico.

## Contratos de dados

Markdown/JSON em repositório público são públicos. auth.accessKeys ou docsAccess no viewer não transformam arquivos públicos em documentos privados; proteção real exige controlar o acesso à origem. Não armazene tokens em config, exemplos ou URLs. Preserve alternativas textuais, hierarquia de títulos e nomes claros nos menus para acessibilidade.

## Fluxo e casos de falha

Leitor abre o viewer oficial e seleciona Vidigal-code/git-page-docs-example → viewer lê a configuração raiz → escolhe versão/idioma → carrega catálogo → resolve Markdown → apresenta menus, índice e navegação. A URL rendering aponta para o viewer oficial; ProjectLink/source-viewer apontam para este exemplo.

Edite somente gitpagedocs. Não existe workflow de deploy de documentação neste repositório. A atualização não publica no GitHub Pages nem executa --push/deploy. Para conferir CLI, use o comando de versão fixado no README interno. Para 404 confira VersionControl, paths de rotas, idioma e existência dos arquivos. Para identidade errada confira ProjectLink e source-viewer; para tema confira URLs oficiais. O README da raiz descreve a base histórica 0.0.8 e permanece fora do escopo desta alteração restrita.

## Arquivos relacionados

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navegação

- [Project guide](?menu=pt&lang=pt&id=13)
- [Source reference](?menu=pt&lang=pt&id=14)
