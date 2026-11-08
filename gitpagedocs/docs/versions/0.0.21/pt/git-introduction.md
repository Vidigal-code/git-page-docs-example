# Git para documentação GitPageDocs

O Git mantém Markdown, configuração e recursos de um site GitPageDocs versionados juntos. Uma versão em `VersionControl.versions` é um rótulo para o leitor; um commit registra um estado concreto do repositório. Eles atendem necessidades diferentes e não precisam usar o mesmo identificador.

## Faça uma mudança focada

```sh
git status --short
git switch -c docs/gitpagedocs-navigation
```

Edite os documentos nos idiomas habilitados. Se o nome de arquivo ou a identidade da página mudar, ajuste a configuração da versão e os destinos traduzidos dos menus na mesma mudança. Preserve caminhos históricos usados por links existentes.

## Confira o resultado completo

```sh
git diff --check
git diff -- gitpagedocs/config.json gitpagedocs/docs/versions/0.0.21
```

Valide sintaxe JSON, arquivos referenciados, traduções e o visualizador antes do commit. Um diff sem erros não comprova que o destino de menu funciona. Revise arquivos novos não rastreados também; eles não aparecem no `git diff` comum antes de serem adicionados ao stage.

## Salve e publique com intenção

Adicione apenas arquivos revisados ao stage, confira `git diff --cached` e descreva no commit o comportamento da documentação. O push atualiza o repositório remoto; um workflow de hospedagem independente ainda pode precisar executar antes da atualização do site. O visualizador oficial de repositórios lê o conteúdo do repositório; uma exportação usa os arquivos do seu build.

Não execute novamente o gerador sobre documentação personalizada apenas para publicar. Gere um candidato em outra pasta e compare, como explicado em [Migração](migration.md). Mantenha credenciais e arquivos locais da máquina fora do stage.

## Recupere uma mudança incorreta

Em uma mudança já compartilhada, revise um `git revert COMMIT` específico em vez de reescrever o histórico compartilhado. Confira a configuração resultante e a página publicada. Preserve conteúdo útil quando o defeito estiver apenas no caminho do menu ou na referência da versão; a recuperação deve corresponder à falha.

Use [Issues e Projects](github-issues-projects.md) para registrar um problema reproduzível e [Contribuição](contributing.md) quando a correção pertencer ao runtime do GitPageDocs.

> Versão: 0.0.21
