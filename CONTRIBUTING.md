# Como contribuir

Contribuições podem explicar uma ideia, registrar uma investigação, comparar soluções ou corrigir uma nota existente. O acervo cobre computação de forma ampla, incluindo modelos, algoritmos, protocolos e sistemas. Escolha um recorte que possa ser tratado com clareza e sustentado por referências ou evidências.

Correções de imprecisões, links quebrados, diagramas, exemplos e explicações também são contribuições importantes. As notas permanecem abertas à revisão depois de publicadas.

## Converse sobre contribuições maiores

Antes de desenvolver um artigo novo substancial, recomendamos abrir uma [issue](https://github.com/oxide-club/notes/issues) com o assunto, a pergunta que pretende responder, o escopo, os conceitos envolvidos e as referências iniciais. Isso ajuda a ajustar o recorte e encontrar pessoas interessadas em colaborar.

Pequenas correções podem seguir diretamente para um pull request, sem aprovação prévia.

## Prepare a nota

1. Crie uma branch para a contribuição.
2. Para uma nota nova, crie um diretório na raiz com um nome descritivo em `kebab-case` e copie `templates/note.md` para seu `index.md`.
3. Substitua os textos de orientação do modelo. Mantenha `draft: true` enquanto a nota estiver em elaboração.
4. Preencha os metadados conforme o [README](README.md). O identificador vem do diretório; não adicione `slug`.
5. Coloque anexos permitidos em `assets/` dentro da nota e confira seus links e créditos.
6. Abra um pull request com o objetivo da contribuição, as fontes consultadas e o que foi verificado.

O modelo é um ponto de partida. Uma nota pode ser um ensaio, uma explicação breve, um guia, uma análise, uma demonstração ou um relato de experimento. Adapte ou remova suas seções; priorize a pergunta que o texto pretende responder.

## Escreva para permitir verificação

Apresente o contexto e os pré-requisitos necessários. Diferencie resultados demonstrados, observações, hipóteses e opiniões. Explique as limitações de exemplos e experimentos; registre versões, condições e comandos quando forem relevantes para reproduzir o resultado.

Use referências próximas às afirmações que elas sustentam. Prefira fontes primárias quando disponíveis e confira se os links apontam para o material correto. Citações, imagens, dados e trechos de código de terceiros precisam de origem e avisos de licença apropriados.

Não inclua segredos, credenciais ou dados pessoais que não devam ser públicos.

## Formato e anexos

Use Markdown sem HTML bruto, MDX ou scripts executáveis. Código em blocos cercados deve ser legível e identificado por linguagem quando possível.

Anexos permitidos: `png`, `jpg`, `jpeg`, `webp`, `gif`, `avif`, `pdf`, `txt`, `csv` e `json`. Não adicione SVG, HTML, JavaScript ou links simbólicos. Use `./assets/arquivo.ext` para anexos e `../outro-slug/index.md` para outra nota; âncoras também são aceitas.

Evite renomear diretórios de notas já publicadas sem coordenar a atualização dos links com os mantenedores.

## Assistência de IA

Ferramentas de IA podem auxiliar a escrita, a tradução, a pesquisa e a preparação de exemplos. Informe no pull request quais ferramentas foram usadas e em quais partes da contribuição. Se essa assistência for relevante para compreender a origem do material ou reproduzir um experimento, registre-a também na própria nota.

Uma pessoa deve revisar o texto, verificar as fontes, conferir afirmações técnicas e testar os exemplos quando aplicável. Não use referências inventadas nem trate a saída de uma ferramenta como evidência.

O uso de IA não garante originalidade, titularidade ou permissão para licenciar um conteúdo. Revise a procedência e os direitos do material antes de submetê-lo.

## Licenciamento e atribuição

Ao contribuir, disponibilize sua prosa e documentação originais sob a CC BY 4.0, somente na medida dos direitos que você detém ou está autorizado a licenciar. Não é necessário transferir sua titularidade ao projeto.

Preserve a atribuição e os avisos de terceiros. Identifique claramente qualquer material sujeito a outra licença e sua origem. A licença do repositório não substitui esses direitos.

Código substancial que possa funcionar como software independente deve ter uma licença de software explícita e separada, acordada com os responsáveis pelo código. Não presuma uma licença de software a partir da CC BY 4.0 aplicada à documentação. Para exemplos extensos, considere manter o software em um repositório próprio e referenciá-lo na nota.

Veja o escopo e o texto legal indicado em [LICENSE](LICENSE).

## Revisão e publicação

A revisão avalia o trabalho apresentado, não a senioridade de quem contribui. Em caso de discordância, explique o raciocínio e apresente fontes, exemplos ou resultados que permitam comparar as posições. Mantenha a discussão respeitosa e aberta a correções.

Antes de pedir revisão, confira:

- Título e resumo descrevem o conteúdo; datas e demais metadados estão corretos.
- Não restam textos de orientação do modelo.
- Afirmações técnicas, exemplos e referências foram verificados.
- Links, imagens, anexos e atribuições estão corretos.
- A prévia local no site foi conferida com `NOTES_SOURCE=/caminho/absoluto/para/notes npm run dev`.
- O pull request descreve o uso de IA, quando houver.

Para publicar, inclua `publishedAt` e altere `draft` para `false` após a revisão editorial. Como `draft` omitido equivale a `false`, mantenha o valor explícito nos rascunhos. Use `updatedAt` para registrar atualizações relevantes em uma nota publicada.

Após aprovação e merge, um mantenedor executa manualmente o workflow **Deploy production** no repositório do site. O merge das notas não publica automaticamente o site. `NOTES_SOURCE` é uma opção de desenvolvimento e não pode substituir a origem de produção.
