# Primeiros passos

Exemplo de consumo do GitPageDocs, formado por configuração, ícone, traduções e Markdown versionado. Não é o código-fonte do CLI nem do viewer. Não possui backend, banco, autenticação de aplicação ou package.json de aplicação. O conteúdo atual usa o contrato 0.0.17; 0.0.8 permanece no catálogo como histórico.

## Configuração e implantação

Edite somente gitpagedocs. Não existe workflow de deploy de documentação neste repositório. A atualização não publica no GitHub Pages nem executa --push/deploy. Para conferir CLI, use o comando de versão fixado no README interno. Para 404 confira VersionControl, paths de rotas, idioma e existência dos arquivos. Para identidade errada confira ProjectLink e source-viewer; para tema confira URLs oficiais. O README da raiz descreve a base histórica 0.0.8 e permanece fora do escopo desta alteração restrita.

## Comandos de execução

```sh
npx --yes --package @gitpagedocs/cli@0.0.17 gitpagedocs version
```

Nomes extraídos apenas dos arquivos de exemplo e das referências a variáveis no código. Configure os valores localmente; credenciais privadas não fazem parte desta referência. Variáveis NEXT_PUBLIC_ e VITE_ são públicas no navegador.

## Arquivos relacionados

- [README.md](https://github.com/Vidigal-code/git-page-docs-example/blob/b5b8ad11d28dbbcd904b105d625c72efd2805cd5/README.md)

## Navegação

- [Project guide](?menu=pt&lang=pt&id=13)
- [Source reference](?menu=pt&lang=pt&id=14)
