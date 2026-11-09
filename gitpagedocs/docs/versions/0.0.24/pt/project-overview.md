# Visão geral do projeto

Este repositório publica documentação sobre o GitPageDocs. A implementação do produto está em [git-page-docs](https://github.com/Vidigal-code/git-page-docs); [git-page-docs-example](https://github.com/Vidigal-code/git-page-docs-example) contém esta documentação e configuração. Ele não representa outro aplicativo ou uma API fictícia.

GitPageDocs é um monorepo pnpm + turborepo que transforma a pasta `gitpagedocs/` de um repositório em um site de documentação multilinguagem e versionado — com assistente de IA integrado e um servidor MCP (Model Context Protocol).

## Pacotes do monorepo

- **frontend/** — visualizador Next.js 15 (App Router, React 19), exportado estaticamente para o GitHub Pages.
- **cli/** — o pacote npm publicado `@gitpagedocs/cli` (`npm install -g @gitpagedocs/cli`): gera a estrutura de docs, documenta com IA, configura o Pages e roda o servidor MCP.
- **tools/** — `@gitpagedocs/tools`, o núcleo de lógica compartilhado: sistema de IA com 14 provedores, cofre de credenciais criptografado, loader de config, caches e logger.
- **mcp/** — `@gitpagedocs/mcp`, servidor Model Context Protocol (20 ferramentas + 7 recursos).
- **gitpagedocs/** — o contrato do usuário: `config.json`, docs versionados e layouts.

## Stack

- Next.js 15 (App Router) + React 19 + TypeScript; exportação estática para GitHub Pages
- gray-matter + marked + hast-util-sanitize para Markdown; react-icons
- pnpm workspaces + turborepo; Vitest + Playwright; ESLint

## Destaques

- Multilinguagem (`en`, `pt`, `es`) e rotas por versão (`/v/:version`)
- Sistema de IA com 14 provedores (OpenAI, Anthropic, Gemini, Ollama, Mistral, DeepSeek, Cohere, Groq, xAI e mais) com streaming
- Chaves de IA **criptografadas em repouso** (AES-256-GCM) atras de uma senha local — nunca em texto puro
- **Drawer de chat de IA** nos docs + um **console `/ai`** dedicado
- Sistema de 124 temas (variantes escuras e claras); execução local e no GitHub Pages

> Versão: 0.0.24
