---
layout: page
title: Sobre
permalink: /about/
---

## O que é este blog

Um blog sobre inteligência artificial, escrito em português para quem não trabalha
com tecnologia. A régua é simples: se um termo técnico aparece, ele é explicado na
primeira vez em linguagem comum. Se não dá para explicar, ele não entra.

## Quem escreve

Os textos são **produzidos por um agente de inteligência artificial**, não por um
jornalista humano. Isso está dito aqui, no rodapé de cada artigo, e não é uma
formalidade: é a diferença entre um blog automatizado honesto e um que finge
autoria humana.

O que o agente faz, em ordem: pesquisa a web sobre a pauta, seleciona cerca de oito
fontes de veículos diferentes, escreve a matéria citando qual fonte sustenta cada
parágrafo, e então passa por uma verificação antes de qualquer publicação.

## Como a verificação funciona

O problema conhecido de textos gerados por IA é a invenção — números que não existem,
citações que ninguém disse, links que levam a lugar nenhum. Pedir ao modelo que
"revise o próprio texto" não resolve: se ele inventou um dado ao escrever, tende a
confirmá-lo ao revisar.

Por isso a verificação aqui **não depende de o modelo ser sincero**. As checagens
decisivas são comparações mecânicas, que nenhum modelo tem como driblar:

- **Atribuição.** Todo parágrafo precisa apontar para uma fonte que existe de fato na
  lista pesquisada.
- **Citação literal.** Quando a verificação afirma que um trecho da fonte sustenta uma
  frase do artigo, esse trecho é procurado, caractere a caractere, no texto original
  da fonte. Citação inventada não sobrevive a uma busca de string.
- **Links.** Toda URL listada precisa estar entre as páginas efetivamente baixadas
  durante a pesquisa. Link inventado é impossível por construção.
- **Números e datas.** Cifras, percentuais e datas são extraídos do artigo e cada um
  precisa aparecer em alguma fonte. Órfãos são sinalizados.

Além disso, quem julga as afirmações é um modelo de **família diferente** daquele que
escreveu o texto — e o julgamento desse segundo modelo também é auditado pelas
comparações acima. Modelos diferentes erram de formas diferentes; é isso que quebra a
confirmação em cadeia.

Artigo que não passa nessa verificação **não é publicado**. Ele fica retido como
rascunho, fora do site, para revisão humana.

## Limites

Verificação automática reduz invenção; não a elimina, e não substitui apuração
jornalística. Os textos partem do que as fontes públicas dizem — se as fontes estão
erradas, o artigo herda o erro. As fontes de cada matéria estão listadas ao final
dela justamente para que você possa conferir por conta própria.

Encontrou um erro? Abra uma issue no
[repositório](https://github.com/pedroboy975/AI-Article-Generator).
