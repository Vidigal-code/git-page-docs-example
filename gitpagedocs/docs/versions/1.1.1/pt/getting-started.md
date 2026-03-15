# Primeiros passos

**Version:** 1.1.1

Este guia leva o projeto do zero ate docs rodando.

## Pre-requisitos

- Node.js 20+
- npm 10+ (ou pnpm)

## Setup local

1. Instale dependencias:
   - 
pm install`
2. Gere/atualize os artefatos de docs:
   - 
pm run gitpagedocs`
3. Inicie o desenvolvimento:
   - 
pm run dev`
4. Build e execucao local de producao:
   - 
pm run build`
   - 
pm start`

## Comportamento da CLI


px gitpagedocs` (ou 
pm run gitpagedocs`) gera os artefatos na pasta oficial `gitpagedocs/`.

- Gera somente markdown/json
- Nao gera `index.html`
- Nao gera `index.js`
- Nao executa comandos de instalacao

## Modo de busca por repositorio

No ambiente local, o controle e por variavel:

- `GITPAGEDOCS_REPOSITORY_SEARCH=true`
- `GITPAGEDOCS_REPOSITORY_SEARCH=false`

Em build de GitHub Pages (`GITHUB_ACTIONS=true`), a busca de repositorio fica sempre ativa.
