---
name: new-post
description: Cria um novo post em _posts/ no formato do Scriptor Jekyll Theme — monta o frontmatter, sugere tags e conceitos de imagem a partir do conteúdo do post. Use quando o usuário pedir para criar/escrever um novo post do blog.
---

# Criar novo post do blog

Esta skill cria um novo arquivo em `_posts/` seguindo exatamente o formato dos posts existentes deste site Jekyll.

## Post-modelo de referência

Use `_posts/2026-07-12-clipper-summer-97.md` como âncora de formato exato:

```markdown
---
layout: post
title: "Clipper Summer 87: onde tudo começou"
description: "A linguagem de programação Clipper foi bem popular nos anos 90"
date: 2026-07-12
authors: ["r-a-albuquerque"]
feature_image: images/posts/clipper-summer-97/feature.jpg
tags:
  - Clipper
  - Tecnologia
---
Corpo do post em markdown...
```

Regras fixas do formato (não desviar):
- `title` e `description` sempre entre aspas duplas.
- `tags` sempre em bloco de lista (não usar `tags: [a, b]` inline).
- `feature_image` é um caminho relativo à raiz do site, **sem barra inicial**, sempre no padrão `images/posts/<slug-do-post>/feature.<ext>` (ex: `images/posts/clipper-summer-97/feature.jpg`), nunca `assets/images/...` nem solto direto em `images/`.
- `authors` é uma lista mesmo com um único autor.

Ignore como modelo os posts `2019-01-04-a-week-with-the-apple-watch.md` (tags em inglês/minúsculo, estilo inline) e `2026-07-22-china-guanxi.md` (autor `mike_vance` — não existe em `_data/authors.yml`, é lixo de dado). Esses formatos legados não devem ser replicados.

## Passo a passo

1. **Determinar o corpo do post.**
   - Se o usuário já colou um texto substancial (mais que um título/frase curta) na conversa, use-o como corpo do post, sem reescrever o conteúdo — apenas ajuste formatação markdown se necessário.
   - Se o usuário só deu um tema/assunto curto (ex: "escreva sobre X"), redija um rascunho de corpo em português, no mesmo tom dos posts existentes (parágrafos curtos, estilo direto/informativo). Deixe claro na sua resposta ao usuário que é um **rascunho** para revisão, não texto final.

2. **Autor — sempre fixo.** Use `authors: ["r-a-albuquerque"]`. Nunca pergunte ao usuário sobre autoria.

3. **Título e descrição.**
   - `title`: use o que o usuário informou, ou proponha um a partir do tema/conteúdo.
   - `description`: resumo de uma frase do conteúdo do post.

4. **Data e nome do arquivo.**
   - Sempre pergunte ao usuário qual é a data de criação do post (por exemplo via AskUserQuestion, sugerindo a data de hoje como opção padrão). Nunca assuma a data de hoje silenciosamente.
   - Essa data confirmada é usada tanto no campo `date` do frontmatter quanto no nome do arquivo — as duas devem sempre coincidir.
   - Gere um slug kebab-case a partir do título (minúsculo, sem acentos, hífens no lugar de espaços).
   - Nome do arquivo: `_posts/AAAA-MM-DD-slug.md`.

5. **Sugerir tags (com confirmação do usuário).**
   - Analise o conteúdo do post e proponha de 3 a 5 tags.
   - Tags existentes no repositório (reutilize quando fizer sentido temático): `Clipper`, `Tecnologia`, `China`.
   - Novas tags só quando necessário, sempre em **Capitalized, português** (ex: `Programação`, `História`), consistente com o padrão mais recente do blog. Não usar minúsculas nem inglês (esse é o padrão legado do post de 2019, a ignorar).
   - Apresente as opções ao usuário (por exemplo via AskUserQuestion ou pergunta direta) e espere a confirmação/escolha antes de gravar o arquivo. Não decida tags silenciosamente.

6. **Sugerir imagem (com confirmação do usuário).**
   - Esta skill não gera nem baixa arquivos de imagem. Proponha 2–3 conceitos visuais curtos (o que a imagem deveria mostrar, com base no conteúdo do post) e o caminho sugerido no padrão do repo: `images/posts/<slug-do-post>/feature.<ext>` (uma pasta por post; `<ext>` conforme o formato da imagem escolhida, ex: `jpg`, `png`).
   - Se o post tiver imagens adicionais além da feature (inline no corpo), elas vão na mesma pasta `images/posts/<slug-do-post>/`, com nome descritivo (ex: `linkedin.jfif`).
   - Deixe explícito ao usuário que o arquivo de imagem precisa ser adicionado manualmente depois em `images/posts/<slug-do-post>/`; o `feature_image` no frontmatter aponta para o caminho sugerido mesmo que o arquivo ainda não exista.

7. **Montar e escrever o arquivo.**
   - Monte o frontmatter exatamente no formato do post-modelo (seção acima) com os valores definidos nos passos 1–6.
   - Escreva o arquivo em `_posts/AAAA-MM-DD-slug.md` usando a ferramenta Write.

8. **Criar a pasta de imagens do post.**
   - Crie a pasta vazia `images/posts/<slug-do-post>/` (ex: `mkdir -p`), para o usuário adicionar manualmente o arquivo de imagem depois. Não crie nem baixe nenhum arquivo de imagem dentro dela.

9. **Gerar prompt de imagem para ferramenta externa de geração.**
   - Ao finalizar, produza um prompt curto (1–3 frases, em inglês, pronto para copiar e colar) para o usuário usar em outra ferramenta de geração de imagem (ex: Midjourney, DALL·E, Stable Diffusion).
   - Base o prompt no(s) conceito(s) visual(is) escolhido(s) no passo 6 e no conteúdo/tom do post. Inclua estilo visual sugerido (ex: "flat illustration", "editorial photo", "minimalist digital art") e proporção adequada para feature image de blog (ex: paisagem, 16:9).
   - Apresente o prompt em um bloco de código separado, para facilitar a cópia.

10. **Resumir para o usuário.**
    - Informe o caminho do arquivo `.md` criado, a pasta de imagens criada, as tags escolhidas, e o caminho de imagem sugerido (`feature_image`) — lembrando que o arquivo de imagem precisa ser adicionado manualmente na pasta criada.
    - Inclua o prompt de geração de imagem do passo 9.
