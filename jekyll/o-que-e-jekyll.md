---
layout: default
title: Jekyll - o que é e quais tecnologias utiliza
---
# Sobre o Jekyll

O **Jekyll é um gerador de sites estáticos**. Depois de instalar o Jekyll pela primeira vez, ele já traz um modelo para começar a criar e gerar um site em forma de blog. Mas o Jekyll pode ser usado para gerar qualquer formato de site e página.

O site e as páginas são geradas a partir de arquivos-fonte em diversos formatos. Mas um dos recursos mais úteis do Jekyll é unir diferentes linguagens usadas na criação de documentação de software, entre elas o **Markdown**.

## Ruby e Gems

O Jekyll foi desenvolvido usando a linguagem de programação **Ruby**.

Por ter sido construído nessa linguagem, o Jekyll precisa que o ambiente do Ruby esteja instalado na máquina onde ele será executado.

O Ruby permite usar pacotes, que são chamados de **Gems**. O Jekyll é um dos Gems que podem ser instalados no Ruby. Portanto, existe essa dependência.

## Bundler e Build

**Bundler** também é um **Gem** suportado pelo Ruby.

O Bundler é usado pelo Jekyll para compilar os arquivos que você vai criar, seja em Markdown, HTML, CSS ou qualquer outro formato que você escolher para construir o conteúdo.

Esse processo de compilação é chamado de **build**, que é responsável por juntar todos os seus arquivos e **gerar um output**.

O **output** é a saída final do seu site estático, que é gerado a partir dos arquivos-fonte e pronto para ser visualizado.

## Command based

O Jekyll é uma ferramenta **command based**. Isso significa que ele roda a base de comandos executados em um terminal, como o **prompt de comando do Windows** ou o **Bash**.

Ao longo do tutorial você vai conhecer os comandos necessários para executar as operações básicas do Jekyll, que são necessárias para manipular e gerar o seu projeto. Para exeutar esses comandos, você precisa estar confortável em lidar com ambientes command based.

# Formatos da documentação

A seguir eu explico um pouco sobre os formatos e linguagens com as quais o Jekyll está preparado para lidar, mas não limitado a estes.

## Markdown (.MD)

O **Markdown** é uma das linguagens mais comuns para criar e gerar documentação, por ser quase universal e integrar bem com ambientes como o [GitHub](https://github.com/). Então, não é por acaso que o Jekyll tem total suporte para este formato de conteúdo.

Os arquivos escritos em Markdown são salvos com a extensão **.md**. Esta linguagem tem sintaxe própria, que determina como o texto será interpretado e apresentado no output.

Por exemplo: se eu quiser escrever um título de uma página usando Markdown, eu vou simplesmente escrever: `# Isso é um título`. O sustenido (#) antes da frase faz com que esta linha seja interpretada como um título.

Se você está acostumado com HTML e criação de conteúdo para a web, fica simples ao saber que isso será interpretado como um `<h1>`. O mesmo acontece para diversos outros elementos em HTML, permitindo criar outros níveis de heading, links, inserir imagens, estilizar o texto e muito mais.

Uma breve pesquisa por "markdown cheatsheet" no Google deve trazer vários resultados de como escrever usando a notação em Markdown. Uma boa referência é a própria [página de Markdown do GitHub](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Tipos alternativos de Markdown

É importante saber que hoje em dia existem versões distintas de Markdown.

Existe a versão chamada "plain" ou "vanilla", que é a versão mais pura do Markdown e é interpretada por praticamente todas as ferramentas que trabalham com esta notação. É a versão raiz e mais segura com a qual você pode trabalhar.

Mas existem também versões alternativas, que são interpretadas apenas por plataformas e ferramentas específicas. Estas versões foram criadas para ampliar o leque de possibilidades oferecidas pelo Markdown puro, aumentando o número de customizações possíveis ou simplificando a sintaxe.

Se você nunca mexeu com Markdown antes, eu recomendo fortemente começar entendendo a versão pura primeiro. Depois, avalie as ferramentas que você usará no dia a dia para determinar quais variações valem a pena você conhecer e praticar.

## Liquid

Outra linguagem usada pelo Jekyll é o **Liquid**.

Se você não é developer ou não conhece lógica de programação, o Liquid pode ser uma notação um pouco mais complexa de se entender.

O Liquid não é obrigatório para usar o Jekyll, mas eu recomendo conhecer e praticar com ele. Isso vai permitir que você crie recursos para ganhar tempo e melhorar a estrutura do seu projeto de documentação.

Neste guia vamos usar somente alguns dos recursos disponíveis do Liquid, como o {% raw %}`{{ content }}` e o `{% include %}`{% endraw %}. Mas não se preocupe com isso agora — você aprenderá a usá-los ao longo do tutorial.

Se você quiser se aprofundar nos outros recursos do Liquid, você pode consultar o [site da documentação oficial](https://shopify.github.io/liquid/).

# Editando a documentação

Para facilitar a criação da documentação usando Markdown e Liquid, é importante usar um bom software que permita editar **texto e código** (*text+code*).

Você até pode usar um processador de texto qualquer e salvá-lo no formato **.md**, por exemplo. Desde que o texto esteja com a sintaxe e formato corretos, vai funcionar. Mas a criação de um site usando o Jekyll permite misturar diversas linguagens.

Usando um editor text+code, você vai criar conteúdo muito mais facilmente, pois ele facilita o controle dos seus arquivos e das linguagens que você vai usar.

O meu favorito é o [**Visual Studio Code (VSCode)**](https://code.visualstudio.com/), por ser bem completo. Mas tem também o [**Sublime Text**](https://www.sublimetext.com/), que eu recomendo se você nunca mexeu com esse tipo de software antes.

O Sublime Text é mais limpo e intuitivo e também é o software que eu vou usar como exemplo ao longo deste tutorial. Mas eu gosto mais do VSCode, por ter mais funcionalidades e plugins disponíveis.

Ambos são gratuitos e facilitam muito a vida para trabalhar com diversos formatos ao mesmo tempo. Eles também têm bastante suporte das comunidades e permitem instalar extensões que trazem ainda mais recursos.

---

<a class="proximo-passo" href="primeiros-passos.html">Ir para o próximo passo: Primeiros passos</a>