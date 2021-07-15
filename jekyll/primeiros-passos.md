---
layout: default
title: Tutorial de Jekyll - Primeiros passos
---
# Primeiros passos
---
## Baixe e instale o RubyInstaller

1. [Clique aqui](https://rubyinstaller.org/downloads/){:target="_blank"} para acessar a página de download do **RubyInstaller** para Windows.
   
2. Faça o download do arquivo de instalação. Escolha a versão recomendada na própria página de download, apenas certifique-se que seja uma versão **com o DevKit** (*RubyInstaller with DevKit*).
   
3. Depois de terminar o download, execute o instalador. Siga os passos sem alterar nenhuma das opções de instalação padrão.
    <span class="nota rosa">Na última etapa da instalação, você vai ver a opção **Run ‘ridk install’ to setup MSYS2 and development toolchain**. Mantenha esta opção **selecionada**.</span>

4. Clique em **Finish**. Uma tela de terminal será aberta automaticamente, pedindo para escolher uma das opções do **ridk install**. Simplesmente tecle <span class="tecla">Enter</span> para fazer a instalação padrão.

5. Quando o **ridk install** finalizar, feche a janela do terminal.

Se tudo foi feito corretamente, agora você tem o **Ruby** instalado na sua máquina.

---

## Instale o Jekyll e o Bundler

1. Acesse o terminal do **prompt de comando** do Windows.
   
2. Na janela do terminal, execute o comando abaixo para começar a instalação do **Jekyll** e do **Bundler**:\
`gem install jekyll bundler`

3. Aguarde até o final da instalação dos pacotes. Depois de terminar, faça um teste para ver se o **Jekyll** foi instalado corretamente.<br>Para fazer isso, ainda na janela do terminal, execute o comando abaixo:\
`jekyll -v`

Se o terminal retornar a versão do Jekyll (exemplo: `jekyll 4.2.0`) é porque deu tudo certo.

**Pronto!** Agora você tem tudo que você precisa para começar a usar o Jekyll.

---

<a class="proximo-passo" href="criar-projeto.html">Ir para o próximo passo: Criar um novo projeto</a>