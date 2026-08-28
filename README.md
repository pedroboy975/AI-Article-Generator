# AI Article Generator — blog

Site Jekyll publicado via GitHub Pages em
<https://pedroboy975.github.io/AI-Article-Generator>.

O conteúdo não é escrito à mão: um workflow n8n (`AI Journalist Agent`) pesquisa,
escreve, verifica e commita os artigos aqui pela API do GitHub.

## Estrutura

| Caminho | O que é |
|---|---|
| `_config.yml` | Configuração do site. Tema `minima`, nativo do Pages. |
| `index.md` | Página inicial — lista os posts. |
| `about.md` | O que é o blog, quem escreve e como a verificação funciona. |
| `_posts/` | **Artigos aprovados** na verificação. Publicam no site. |
| `_drafts/` | **Artigos reprovados.** O Jekyll ignora esta pasta no build. |

## A regra que sustenta o resto

Artigo que não passa na verificação anti-alucinação **nunca** vai para `_posts/`.
Vai para `_drafts/`, fora do site, e só um humano promove — movendo o arquivo.

Isso não é preferência de estilo. Enquanto a saída era um email privado, um texto com
afirmações não verificadas era um aviso. Publicado num blog com um nome em cima, vira
uma declaração pública. A separação `_posts/` vs `_drafts/` é a condição para o blog
existir de forma honesta.

## Rodar localmente (opcional)

```sh
gem install bundler jekyll
bundle exec jekyll serve --drafts   # --drafts mostra os reprovados, para revisão
```
