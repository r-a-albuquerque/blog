# Scriptor Jekyll Theme

![Jekyll](https://img.shields.io/badge/Jekyll-4.0.1-CC0000?style=flat-square&logo=jekyll&logoColor=white)
![Ruby](https://img.shields.io/badge/Ruby-%3E%3D2.5-CC342D?style=flat-square&logo=ruby&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-deployed-222222?style=flat-square&logo=github&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

Blog pessoal construído sobre o tema **Scriptor**, um tema Jekyll minimalista focado em leitura, criado por [JustGoodThemes](https://www.justgoodthemes.com).

## Tecnologias utilizadas

- [Jekyll](https://jekyllrb.com/) `4.0.1` — gerador de sites estáticos
- [Ruby](https://www.ruby-lang.org/) + [Bundler](https://bundler.io/) — gerenciamento de dependências
- [Sass/SCSS](https://sass-lang.com/) — estilização (`_sass/`)
- [Kramdown](https://kramdown.gettalong.org/) — conversão Markdown
- [jekyll-paginate](https://github.com/jekyll/jekyll-paginate) e [jekyll-sitemap](https://github.com/jekyll/jekyll-sitemap) — plugins
- [GitHub Pages](https://pages.github.com/) — hospedagem e deploy

## Instalação

### Pré-requisitos

- [Ruby](https://www.ruby-lang.org/en/documentation/installation/) (versão 2.5 ou superior)
- [Bundler](https://bundler.io/) (`gem install bundler`)

### Passos

1. Clone o repositório:

   ```bash
   git clone https://github.com/r-a-albuquerque/blog.git
   cd blog
   ```

2. Instale as dependências:

   ```bash
   bundle install
   ```

3. Rode o servidor local:

   ```bash
   bundle exec jekyll serve
   ```

4. Acesse [http://localhost:4000/blog](http://localhost:4000/blog) no navegador.

## Estrutura do projeto

```
_config.yml     # configurações gerais do site
_data/          # dados (autores, etc.)
_includes/      # partials reutilizáveis
_layouts/       # layouts das páginas
_posts/         # posts do blog
_sass/          # estilos SCSS
images/         # imagens do site e dos posts
assets/         # CSS/JS compilados
```

## Deploy no GitHub Pages

O site é publicado via [GitHub Pages](https://docs.github.com/pages), que faz o build automaticamente a partir do Jekyll a cada push na branch configurada (geralmente `main` ou `gh-pages`). Para mais detalhes, veja a [documentação oficial de deploy do Jekyll no GitHub Pages](https://jekyllrb.com/docs/github-pages/).

## Licença

Distribuído sob a licença [MIT](LICENSE.md).
