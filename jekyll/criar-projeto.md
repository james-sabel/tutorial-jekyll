---
layout: default
title: Criar um novo projeto - Tutorial de Jekyll
---
# Criar um novo projeto
---
## Crie um projeto inicial

1. Crie um diretório vazio no seu disco rígido. Esse diretório será o local onde ficará armazenado o seu projeto. Para este tutorial, eu vou criar o seguinte local: **c:\projeto-tutorial**.

2. Acesse o terminal do **prompt de comando** do Windows e, no terminal, navegue até o diretório que você criou no passo anterior.

3. Execute o comando <code>jekyll new</code> seguido do nome do seu projeto. Neste tutorial o nome do projeto será **projeto-tutorial**. Então o comando ficará assim:
    ````
    jekyll new projeto-tutorial 
    ````
    O Jekyll vai criar uma nova pasta, na qual serão instalados os arquivos necessários para o projeto inicial. Ao terminar a instalação do projeto, o prompt vai mostrar um aviso confirmando a criação da pasta.

<span class="nota azul">No final dessa página eu explico como funciona a estrutura de pastas e arquivos que o Jekyll cria nessa etapa.</span>
<br>
### <i class="fas fa-lightbulb"></i> Tema padrão do Jekyll e personalização

Os projetos criados com o Jekyll suportam o uso de **temas**. Os temas são templates que determinam a aparência de todo o projeto. Por padrão, a instalação de um novo projeto do Jekyll usa um tema básico chamado **Minima**.

Esse tutorial não vai explicar como usar temas personalizados. Mas, para personalizar o seu projeto, você pode pesquisar por temas do Jekyll na internet.

Se você conhece **CSS**, essa também é uma alternativa para customizar a aparência do seu site. O Jekyll tem total suporte a essa linguagem.

---

## Visualize o projeto criado

1. No **prompt de comando**, certifique-se de que você está posicionado no diretório onde seu projeto foi instalado. No exemplo deste tutorial, o local é este: **c:\projeto-tutorial\projeto-tutorial**.

2. Execute o seguinte comando para fazer um **build** do seu projeto:
    ````
    bundle exec jekyll serve
    ````

3. Quando aparecer a mensagem indicando que o **build** foi finalizado, abra um navegador de sua preferência e acesse o seguinte endereço: **http://localhost:4000/**

Com isso você já poderá visualizar a versão inicial do seu site gerado.  
<br>
### <i class="fas fa-lightbulb"></i> Entenda como funciona o build do Jekyll

O Jekyll é um gerador de sites estáticos. Uma característica deste tipo de ferramenta é que você precisa compilar os arquivos do seu projeto para gerar os arquivos do site e visualizá-los no navegador. Esse processo é chamado de **build**.

Sempre que você alterar um arquivo, é preciso fazer um **build** do projeto antes de visualizar a alteração. Felizmente, o Jekyll facilita esse processo.

#### Comandos básicos de build

`bundle exec jekyll serve` ou `bundle exec jekyll s` — faz um build inicial do projeto e inicia o servidor local.

`bundle exec jekyll serve --skip-initial-build` — apenas inicia o servidor local, sem fazer um build inicial do projeto.

`bundle exec jekyll serve --port 4001` — faz um build inicial do projeto e inicia o servidor local em uma porta de sua escolha (substituindo o *4001*). Isso é especialmente útil quando você quer executar mais de um site ao mesmo tempo, rodando cada servidor em uma porta diferente.

<span class="nota azul">Sempre que você faz um build do seu projeto, todos os arquivos com extensão **.md** (Markdown) são convertidos para **.html** no output do seu site. Os arquivos originais do seu projeto permanecem com o formato **.md**.</span>
<br>
### <i class="fas fa-lightbulb"></i> Entenda a estrutura de arquivos e pastas do projeto

O Jekyll trabalha com uma estrutura de arquivos padronizada, com pastas e arquivos com nomes e funções dinstintos.

Sempre que você criar um projeto novo, o Jekyll vai gerar os arquivos básicos necessários para começar a trabalhar com o seu site.

**Principais componentes da estrutura de arquivos:**

<span class="nota rosa">Algumas pastas e arquivos citados na tabela abaixo só vão aparecer depois que você fizer o build do seu projeto pela primeira vez.</span>

|Arquivo ou pasta|Descrição
|---|---|
|**_config.yml**|Arquivo de configurações do Jekyll. Permite que você altere algumas propriedades e defina um padrão para algumas opções do projeto.<br><br>Inicialmente, deixe as configurações como foram criadas na instalação. Ao longo do tutorial você vai ver como fazer algumas das alterações necessárias.|
|**_posts**|Este tutorial é focado em criar arquivos de documentação, mas um dos propósitos do Jekyll é facilitar a construção de blogs em forma de site estático. Se você estivesse criando um blog, as páginas dos seus posts ficariam na pasta **_posts**.|
|**_site**|Toda vez que é feito um build do projeto, os arquivos gerados ficam nesta pasta. O conteúdo dessa pasta compõe o seu site gerado, com os arquivos finais prontos para serem publicados.|
|**404.html**|Página com o conteúdo que será mostrado no navegador sempre que o usuário tentar acessar uma URL inexistente do seu site (o famoso erro **404 - Not found**). O arquivo já vem com uma mensagem de erro simples, mas você pode personalizar a página normalmente.|
|**about.markdown** e **index.markdown**|São duas páginas com conteúdo de exemplo, que o Jekyll cria automaticamente. O **index** sempre será a página inicial do seu site. É a primeira página que será exibida quando um usuário acessar o seu site no domínio raiz.|
|**Gemfile** e **Gemfile.lock**|O **Gemfile** contém informações sobre os Gems que você tem instalados no seu ambiente do Ruby, como as versões que você está usando, por exemplo.<br><br>Já o arquivo de mesmo nome com a exensão **.lock** serve para bloquear alterações de novas instalações, a fim de evitar quebras de compatibilidade no seu projeto. Este bloqueio garante que você mude um Gem para uma versão mais recente somente fazendo um processo normal de atualização.|

**Front Matter (cabeçalho do Markdown):**

Cada arquivo Markdown do Jekyll possui um cabeçalho, que é chamado de **Front Matter**.

Se você estiver escrevendo em Markdown, o Front Matter é a primeira coisa que você precisa inserir no seu arquivo. Ele serve para determinar características da sua página, usando **atributos** e seus respectivos **valores**.

O Front Matter tem o seguinte formato:

````
---
atributos: valores
---
````

Os **atributos** determinam características importantes da sua página. O Jekyll tem diversos atributos e você pode definir quantos quiser. Neste tutorial eu vou abordar dois dos mais importantes:

* `title`: **título da página**. É o equivalente ao tag `<title>` de um HTML e é também o que vai aparecer no topo da janela do navegador.

* `layout`: **template da página**. Define qual é a estrutura que a página vai utilizar. Ao longo desse tutorial você vai ver como configurar o layout do jeito que quiser.

Você vai aprender a usar esses atributos nas próximas etapas do tutorial.

---

<a class="proximo-passo" href="editar-projeto.html">Ir para o próximo passo: Editar o projeto inicial</a>