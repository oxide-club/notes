# Notas do Oxide Club

Um acervo de notas sobre computação: modelos, algoritmos, protocolos, sistemas e as ideias que ajudam a entendê-los. Também cabem temas como linguagens, compiladores, bancos de dados, redes, sistemas distribuídos, segurança, arquitetura de computadores e fundamentos teóricos. O conteúdo deste repositório alimenta a [seção de notas do site do Oxide Club](https://oxideclub.dev/notas).

Cabem aqui explicações curtas, ensaios, guias de leitura, análises de artigos, demonstrações, relatos de experimentos e comparações de abordagens. A estrutura deve servir ao assunto; não há um formato editorial único.

As notas devem ser úteis por si mesmas; não precisam estar vinculadas a um desafio. São documentos colaborativos e revisáveis, abertos a correções e a novas evidências, e não referências inquestionáveis.

O acervo integra o [ecossistema de repositórios do Oxide Club](https://github.com/oxide-club). Discussões e contribuições para estas notas acontecem no [repositório notes](https://github.com/oxide-club/notes).

Este repositório começa sem artigos. O arquivo em `templates/` é um modelo de escrita e não faz parte do acervo publicado.

## Organização

Cada nota ocupa um diretório na raiz, com nome em `kebab-case`:

```text
{kebab-slug}/
  index.md
  assets/
templates/
  note.md
```

O nome do diretório define o identificador da nota. Não use um campo `slug` no frontmatter. Crie `assets/` apenas quando houver anexos.

Os arquivos de documentação da raiz e o diretório `templates/` ficam fora da coleção de notas.

## Metadados

Cada `index.md` começa com frontmatter YAML:

| Campo         | Tipo            | Regra                                                                         |
| ------------- | --------------- | ----------------------------------------------------------------------------- |
| `title`       | texto           | Obrigatório; título descritivo.                                               |
| `summary`     | texto           | Obrigatório; resumo do que a nota aborda.                                     |
| `publishedAt` | data            | Obrigatório para publicação; pode ser omitido em rascunhos. Use `YYYY-MM-DD`. |
| `updatedAt`   | data            | Opcional; data de uma atualização relevante, em `YYYY-MM-DD`.                 |
| `topics`      | lista de textos | Opcional; assuntos da nota.                                                   |
| `draft`       | booleano        | Opcional; o padrão é `false`. Use `true` durante a elaboração.                |
| `authors`     | lista de textos | Opcional; nomes ou pseudônimos para atribuição.                               |
| `featured`    | booleano        | Opcional; o padrão é `false`.                                                 |

Comece copiando [templates/note.md](templates/note.md) para `{kebab-slug}/index.md`. Substitua os textos de orientação, mantenha `draft: true` enquanto escreve e inclua `publishedAt` antes de publicar.

## Markdown e anexos

Use Markdown, sem HTML bruto, MDX ou scripts executáveis. Blocos de código servem à leitura; não são executados pelo site.

Anexos locais devem ficar em `assets/` e usar uma destas extensões: `png`, `jpg`, `jpeg`, `webp`, `gif`, `avif`, `pdf`, `txt`, `csv` ou `json`. Não inclua SVG, HTML, JavaScript ou links simbólicos.

Referencie um anexo com `./assets/arquivo.ext`. Para outra nota, use `../outro-slug/index.md`. Âncoras são permitidas, como `#referencias` ou `../outro-slug/index.md#referencias`. Dê texto alternativo às imagens e descreva a finalidade dos anexos.

## Prévia e publicação

No repositório do **site**, com suas dependências instaladas, execute:

```sh
NOTES_SOURCE=/caminho/absoluto/para/notes npm run dev
```

`NOTES_SOURCE` seleciona uma cópia local das notas para desenvolvimento. Esse override não é permitido em produção.

Depois da revisão e do merge das notas, a publicação é manual: execute o workflow **Deploy production** no GitHub do repositório do site. Um merge neste repositório não dispara automaticamente o deploy do site.

Consulte [CONTRIBUTING.md](CONTRIBUTING.md) para o fluxo de contribuição e a revisão editorial.

## Licença

A prosa e a documentação originais são disponibilizadas sob [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), na medida dos direitos que os contribuidores podem licenciar. Preserve a atribuição e os avisos de materiais de terceiros. Consulte [LICENSE](LICENSE) para o escopo e a referência ao texto legal.

Código substancial que possa ser usado como software independente precisa de uma licença de software explícita e separada; não presuma que este aviso a fornece.
