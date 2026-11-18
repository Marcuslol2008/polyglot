# PolyglotQuiz - O Jogo do Adivinhe a Linguagem

Site da **Atividade 1** feito só com HTML e CSS. O tema é um quiz gamificado em que o jogador vê um trecho de código misterioso e escolhe, entre quatro opções, a linguagem de programação.

> Nesta versão não há JavaScript. O quiz, o ranking com `localStorage` e as conquistas aparecem como estrutura e conteúdo de exemplo, e ganham comportamento numa etapa futura.

## Site publicado

- GitHub Pages: `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/` (preencher após publicar)

## Validação W3C

Resultado do [validator.w3.org/nu](https://validator.w3.org/nu/) para `index.html`:

![Resultado da validação W3C sem erros](prints/validador.png)

> Falta fazer: validar o `index.html` no site acima (aba "Check by file upload" ou "address"), salvar o print como `prints/validador.png` e confirmar que aparece "Document checking completed. No errors or warnings to show."

## Estrutura

```
polyglotquiz/
├── index.html
├── css/
│   └── style.css
├── images/
│   ├── brainfuck.svg
│   ├── haskell.svg
│   └── python.svg
├── prints/
│   └── validador.png
└── README.md
```

## Requisitos da atividade

| Requisito | Onde está |
|---|---|
| `lang`, `meta viewport` e `title` próprio | `<head>` do `index.html` |
| header, nav, main, aside e footer | estrutura da página |
| Um `h1` e hierarquia sem saltos (h1, h2, h3) | todas as seções |
| Pelo menos 3 `article` com conteúdo do tema | seção "Curiosidades" (Brainfuck, Haskell, Python) |
| 3 imagens em `figure` + `figcaption`, com `alt`, `width` e `height` | seção "Curiosidades" |
| Tabela com `caption`, `thead`, `tbody` e `th scope` | seção "Ranking e conquistas" |
| Formulário de contato com `label`, `type` corretos e `fieldset`/`legend` | seção "Contato" |
| `time`, `address`, `strong`/`em` | ranking, rodapé e textos |
| Link "pular para o conteúdo" | início do `body` |
| CSS externo, simples e responsivo | `css/style.css` |

## Como publicar no GitHub Pages

1. Crie um repositório no GitHub e envie estes arquivos para a branch `main`.
2. Abra **Settings > Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`.
4. Salve e aguarde alguns minutos. O endereço aparece no topo da mesma página.
5. Copie o endereço para a seção "Site publicado" deste README.

## Próximos passos

- JavaScript para sortear códigos, contar o tempo e pontuar.
- Ranking e conquistas salvos com `localStorage`.
- Mais curiosidades sobre a sintaxe de cada linguagem.
