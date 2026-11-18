## Atividade 1: o que foi feito

# 1. `lang`, `meta viewport`, `title` e landmarks
- `lang="pt-BR"` no `<html>`, `meta viewport` para o layout responsivo e `title` próprio: "PolyglotQuiz - O Jogo do Adivinhe a Linguagem".
- `header` com o nome do site, a tagline e o `nav` com âncoras para as seções.
- `main` com todo o conteúdo principal (Como funciona, Desafio, Ranking, Curiosidades e Contato).
- `aside` com a caixa "Você sabia?" (curiosidade e dica de jogo), que complementa o conteúdo sem fazer parte dele.
- `footer` com o contato e a data de atualização.
- Dentro do `main`, cada parte é uma `section` com `h2`, e os conteúdos independentes de Curiosidades são `article`.

# 2. Hierarquia de títulos e 3 `article`
- Um único `h1` (o nome do site), seguido de `h2` para cada seção e `h3` para os títulos dos artigos e das conquistas, sem saltos de nível.
- 3 `article` na seção Curiosidades, todos sobre o tema: **Brainfuck** (8 comandos, sintaxe que parece ruído), **Haskell** (funções puras e casamento de padrões) e **Python** (a indentação é a sintaxe).

# 3. Imagens em `figure` + `figcaption`
- 3 imagens SVG próprias, uma por artigo: `brainfuck.svg`, `haskell.svg` e `python.svg`.
- Cada uma está em uma `figure` com `figcaption` e tem `alt` descritivo do conteúdo, além de `width` e `height` definidos, o que evita deslocamento de layout.

# 4. Tabela acessível
- Ranking de exemplo na seção "Ranking e conquistas", com `caption`, `thead`, `tbody` e `th` com `scope`.
- `scope="col"` nos cabeçalhos de coluna e `scope="row"` na posição de cada jogador.
- A tabela fica em um contêiner com rolagem horizontal, para não quebrar em telas pequenas.

# 5. Formulário de contato
- Seção "Contato", com `label` ligado por `for`/`id` a todos os campos.
- Tipos corretos: `text` (nome), `email`, `url` (perfil do GitHub), `select`, `textarea` e `checkbox`.
- Dois `fieldset` com `legend`: "Seus dados" e "Sua sugestão".
- `required` nos campos obrigatórios e `autocomplete` em nome e e-mail.
- O formulário do desafio (opções de linguagem em `radio`) segue o mesmo padrão, com `fieldset` e `legend`.

# 6. `time`, `address`, `strong`/`em` e link "pular para o conteúdo"
- `time` com `datetime` nas datas do ranking, no ano de criação do Brainfuck e na atualização do rodapé.
- `address` no rodapé, com o e-mail de contato.
- `strong` para termos-chave (ex.: "8 comandos", "Adivinhe a Linguagem") e `em` para ênfase (ex.: "mais pontos", "fácil de ler").
- Link **"Pular para o conteúdo"** logo no início do `<body>`. Ele fica escondido e aparece ao receber foco pelo teclado, levando direto ao `<main>`.

# 7. Zero erros no validador W3C
- HTML escrito sem tags fora de ordem, sem `id` repetido e com todo campo associado a um `label`.
- Validado em validator.w3.org/nu. Print do resultado:

[Validação W3C sem erros](prints/validador.png)

# 8. CSS externo, responsivo e GitHub Pages
- `css/style.css` é um arquivo externo e simples, com variáveis CSS (`:root`) para as cores e tema escuro de terminal.
- **Mobile-first:** uma coluna no celular. Com mais de 40rem, as conquistas e os campos do formulário passam a duas colunas. Com mais de 60rem, o `aside` vira uma barra lateral fixa.
- Imagens com `max-width: 100%` e `height: auto`.
- Acessibilidade: `:focus-visible` bem visível, `prefers-reduced-motion` respeitado e contraste alto entre texto e fundo.
- Site publicado no GitHub Pages (branch `main`, pasta raiz): [https://marcuslol2008.github.io/polyglot/](https://marcuslol2008.github.io/polyglot/)