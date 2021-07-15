---
layout: default
title: Editar um projeto - Tutorial de Jekyll
---
# Editar um projeto

---

## Edite a página inicial

<ol>
    <li>
        Usando a ferramenta de edição de texto e código da sua escolha, abra o arquivo <b>index.markdown</b>. Este é um dos arquivos que foram gerados automaticamente pelo Jekyll quando você criou o seu projeto inicial.<br /><br />
    </li>
    <li>
        Dentro do arquivo <b>index.markdown</b>, você encontrará um Front Matter inicial, que é criado por padrão em novos projetos do Jekyll. Apague todo o conteúdo do arquivo e substitua pelo seguinte:
        <br /><br />
        <code>
        ---<br />
        layout: <span style="color: #FFCCE1;">geral</span><br />
        title: <span style="color: #FFCCE1;">Página inicial</span><br />
        ---<br />
        # Olá, mundo!<br />
        Esta é a minha primeira página.
        </code>
        <br /><br />
        Assim você criou sua primeira página e definiu que ela irá usar um layout chamado <b>geral</b>. Este layout ainda não existe, então vamos criá-lo agora.
        <br /><br />
    </li>
    <li>
        Crie uma pasta chamada <b>_layouts</b> dentro da pasta raiz do seu projeto. Por padrão, este é o nome da pasta onde o Jekyll busca os layouts do projeto.
        <br /><br />
    </li>
    <li>
        Crie um arquivo chamado <b>geral.html</b> dentro da pasta <b>_layouts</b> e abra o arquivo usando o seu editor.
        <br /><br />
    </li>
    <li>
        Os layouts são escritos em formato <b>.html</b>, então eles não precisam de um Front Matter. Comece a edição do seu layout <b>geral.html</b> como se ele fosse uma página comum da web e faça as seguintes modificações:
        <br /><br />
        <ul>
            <li>
                Adicione o parâmetro <code>{% raw %}{{ page.title }}{% endraw %}</code> dentro do tag de título da página - este parâmetro é substituído automaticamente pelo título da página que o usuário estiver acessando.
            </li>
            <li>
                Adicione o parâmetro <code>{% raw %}{{ content }}{% endraw %}</code> entre os tags <b>&lt;body&gt; &lt;/body&gt;</b> - este parâmetro sempre é substituído automaticamente pelo conteúdo (corpo) da página que o usuário estiver acessando.
                <br /><br />Agora a estrutura do seu layout deverá estar assim:<br />
                <code>
                &lt;!doctype html&gt;
                <br />&lt;html&gt;
                <br />&lt;head&gt;
                <br />&lt;meta charset="utf-8"&gt;
                <br />&lt;title&gt;<span style="color: #FFCCE1;">{% raw %}{{ page.title }}{% endraw %}</span>&lt;/title&gt;
                <br />&lt;/head&gt;
                <br />&lt;body&gt;
                <br />&nbsp;&nbsp;<span style="color: #FFCCE1;">{% raw %}{{ content }}{% endraw %}</span>
                <br />&lt;/body&gt;
                <br />&lt;/html&gt;
                </code>
                <br /><br />
            </li>
        </ul>
    </li>
    <li>
        Se você não fez o build desse projeto, faça agora. Com o servidor local do Jekyll rodando, acesse o seguinte endereço no seu navegador: <a href="http://localhost:4000" target="_blank">http://localhost:4000</a>
        <br /><br />
    </li>
</ol>
Ao acessar o endereço, você verá a página inicial que você criou com o texto **Olá, mundo!**

---

## Crie uma nova página e faça links

<ol>
    <li>
        Crie um arquivo chamado <b>pagina2.md</b> dentro da pasta raiz do seu projeto e abra-o no seu editor. Coloque o seguinte texto dentro deste arquivo:<br /><br />
        <code>
        ---<br />
        layout: <span style="color: #FFCCE1;">geral</span><br />
        title: <span style="color: #FFCCE1;">Página 2</span><br />
        ---<br />
        # Oi, de novo!<br />
        Esta é a segunda página do meu site.
        </code><br /><br />
        Perceba que, assim como a página inicial que criamos, esta aqui também usa o layout <b>geral</b>. Mas, se você quisesse, poderia criar um layout diferente e defini-lo aqui.<br /><br />
    </li>
    <li>
        Abra o arquivo <b>index.markdown</b> novamente. Agora vamos criar um link dele para a nova página que acabamos de criar.<br />
        Para isso, acrescente mais uma linha no final do arquivo, como demonstrado a seguir:
        <br /><br />
        <code>
        ---<br />
        layout: geral<br />
        title: Página inicial<br />
        ---<br />
        # Olá, mundo!<br />
        Esta é a minha primeira página.<br />
        <span style="color: #FFCCE1;">Mas eu também tenho mais uma página. [<span style="color: #ffffff;">Clique aqui</span>](<span style="color: #ffffff;">pagina2.md</span>) para ver!</span><br />
        </code>
        <br /><br />
        Dessa forma, você linkou o texto <b>Clique aqui</b> com a página do arquivo <b>pagina2.md</b>.
        <br /><br />
    </li>
        <li>
        Com o servidor local do Jekyll rodando, acesse o seguinte endereço no seu navegador: <a href="http://localhost:4000" target="_blank">http://localhost:4000</a>
        <br /><br />
    </li>
        <li>
        Clique no link que você acabou de criar e veja que assim você navegou da página inicial para a segunda página do seu projeto. É desse jeito que você cria links quando estiver escrevendo em Markdown!
        <br /><br />
    </li>
</ol>

---

<a class="proximo-passo" href="publicar-projeto.html">Ir para o próximo passo: Colocar o projeto no ar</a>