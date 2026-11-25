# SEO do PolyglotQuiz (Atividade 2)

Site: https://marcuslol2008.github.io/polyglot/

## Páginas

| Página | URL canônica | O que tem |
|---|---|---|
| Início | `https://marcuslol2008.github.io/polyglot/` | Quiz, ranking, curiosidades e contato |
| Linguagens | `https://marcuslol2008.github.io/polyglot/linguagens.html` | Guia com o mesmo código em Python, Haskell, JavaScript e Brainfuck |
| Sobre | `https://marcuslol2008.github.io/polyglot/sobre.html` | Pontuação, conquistas e próximas etapas |

Os nomes dos arquivos são curtos, em minúsculas e descritivos, sem parâmetros na URL.

## 1. title, description e canonical por página

| Página | title (caracteres) | description (caracteres) |
|---|---|---|
| Início | PolyglotQuiz: adivinhe a linguagem de programação do código (59) | 138 |
| Linguagens | Como reconhecer linguagens de programação \| PolyglotQuiz (56) | 139 |
| Sobre | Sobre o jogo, pontuação e conquistas \| PolyglotQuiz (51) | 142 |

- Cada título e cada descrição é único e descreve o assunto da própria página.
- `<link rel="canonical">` com URL absoluta, igual ao `og:url` e ao endereço do `sitemap.xml`.

## 2. Open Graph e favicon

- `og:type`, `og:site_name`, `og:title`, `og:description`, `og:image`, `og:url` e `og:locale` em todas as páginas, mais `twitter:card`.
- `og:image` é `images/og-cover.png`, com 1200×630 px e URL absoluta. Usei PNG porque WhatsApp e redes sociais não mostram SVG na prévia.
- Favicon em `favicon.svg`, na raiz, ligado por `<link rel="icon" type="image/svg+xml">`. Sem ele o navegador pede `/favicon.ico` e recebe 404.

## 3. JSON-LD

| Página | Tipos schema.org |
|---|---|
| Início | `WebSite` |
| Linguagens | `CollectionPage` com `ItemList` de `ComputerLanguage` e `BreadcrumbList` |
| Sobre | `AboutPage` com `BreadcrumbList` |

O JSON está dentro do `<head>` de cada página, em `<script type="application/ld+json">`. Conferi que o JSON é sintaticamente válido.

Validação no [validator.schema.org](https://validator.schema.org/) e no Teste de pesquisa aprimorada do Google: **COLOQUE AQUI O PRINT**

## 4. robots.txt e sitemap.xml

- `robots.txt` na raiz do repositório, com `User-agent: *`, `Disallow: /polyglot/prints/` (a pasta só tem o print do validador) e a linha `Sitemap:` com URL absoluta.
- `sitemap.xml` na raiz, com as 3 páginas, URLs absolutas iguais aos canonicals e `lastmod` real.
- Observação: como o site é um GitHub Pages de projeto (`usuario.github.io/polyglot/`), o buscador só lê o `robots.txt` da raiz do domínio. O arquivo fica no repositório pelo requisito da atividade, e o sitemap pode ser enviado pelo Google Search Console.

## 5. Imagens, URLs e links internos

- As 3 imagens da página inicial têm `alt` descritivo, `width` e `height` (evita deslocamento de layout) e `loading="lazy"`, porque ficam abaixo da dobra.
- Cada página tem um único `h1` e os títulos seguem a ordem h1, h2, h3.
- Links com texto descritivo, como "Veja como reconhecer Haskell no guia de linguagens", e nenhum "clique aqui".
- Menu igual em todas as páginas, com `aria-current="page"` na página atual, trilha de navegação (breadcrumb) nas páginas internas e links cruzados entre o conteúdo (por exemplo, curiosidades levam ao guia de linguagens, e o guia leva ao desafio).
- Conferi os 49 links internos: todos apontam para arquivos e âncoras que existem.

## 6. Lighthouse antes e depois

- **Antes:** versão da Atividade 1 (sem canonical, Open Graph, favicon e JSON-LD).
- **Depois:** versão atual.

| Categoria | Antes | Depois |
|---|---|---|
| Desempenho | 99 | 100 |
| Acessibilidade | 100 | 100 |
| Boas práticas | 96 | 100 |
| SEO | 100 | 100 |

Prints dos relatórios:

- Antes: `prints/lighthouse-antes.png`
- Depois: `prints/lighthouse-depois.png`

O que mudou:

1. Favicon: tira o erro 404 do console, que reprovava Boas práticas.
2. Canonical e meta description únicos por página: itens da auditoria de SEO.
3. Links com texto descritivo e imagens com `alt`, `width` e `height`.
