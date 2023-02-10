# Tutorial prático de Git (bash) e GitHub

## Primeiramente, para que serve o Git e GitHub?

Git é um sistema de controle de versão distribuído que ajuda você (e demais pessoas envolvidas em um projeto) a acompanhar as alterações em seu código ao longo do tempo. GitHub é uma plataforma baseada na web que fornece hospedagem para repositórios Git, tornando mais fácil para você armazenar, gerenciar e colaborar em seu código.

A importância do Git e do GitHub é que eles fornecem uma forma fácil e eficiente de gerenciar e colaborar em projetos de software. Com o Git, você pode manter o histórico de todas as alterações feitas no seu código e reverter facilmente as alterações indesejadas. O GitHub permite que você armazene seus projetos na nuvem, o que significa que é possível acessá-los de qualquer lugar e compartilhá-los com outros desenvolvedores. Além disso, o GitHub oferece uma ampla comunidade de desenvolvedores que você pode colaborar e aprender, quase como uma rede social propriamente dita.

## Índice de assuntos

---

## 1. Instalando o Git Bash

O primeiro passo do tutorial é baixar o Git Bash, caso você ainda não o tenha em seu computador. O link para download pode ser acessado [clicando aqui](https://git-scm.com/downloads).

Após download, basta seguir o fluxo normal de instalação até que ela seja finalizada.

## <a name="topico2">2. Criando um repositório local (Computador)</a>

1. Crie uma nova pasta no seu computador para utilizarmos nesse tutorial. Para fins de exemplificação, vou usar como nome `Tutorial Git`, mas sinta-se a vontade de usar o nome que preferir.

2. Com o Visual Studio Code (VS Code) aberto, clique em "Open folder..." para abrir a pasta que acabamos de criar (ou Ctrl+K > Ctrl+O).

   - Caso você não tenha o VS Code instalado, o download pode ser feito [clicando aqui](https://code.visualstudio.com/download).

    <img width="300px" height="400px" src="./assets/img/open-folder.jpg">

3. Vamos criar um arquivo `README.md` em nossa pasta. Esse arquivo será utilizado apenas como referência que no tutorial, mas a mesma sequência se aplicaria para quaisquer arquivos que você criasse em sua pasta (.html, .js, .json, etc). Vamos colocar algum texto em nosso `README.md`, apenas para ele não ficar vazio.

<img src="./assets/img/criando-README.jpg">

4. Vá até a pasta que você cruiou no item 1., e, clicando com botão direito dentro dela, clique em `Git Bash Here`, isso fará com que o terminal do Git seja aberto.

   <img src="./assets/img/abrir-gitbash.jpg">

   - Uma janela semelhante a essa será aberta:

       <img src="./assets/img/pagina-gitbash.jpg">

5. A primeira coisa que precisamos fazer ao usar o Git pela primeira vez é configurar nosso `user name` e `e-mail`. Para isso vamos usar os seguintes códigos (um de cada vez):

   - `git config --global user.name <usuário>` -> Exemplo prático: `git config --global user.name "João Bicicleta"`.
   - `git config --global user.email <email>` -> Exemplo prático: `git config --global user.email joao.bicicleta@email.com"`.
   - Note que o terminal não irá apresentar nenhuma informação depois que inserimos esses dois códigos. Esse é um comportamento esperado, ele só irá retornar algo em caso de erro.

6. Para "inicializar" nosso repositório local, nós vamos usar o comando `git init`. Dessa vez, note que houve três alterações que podemos observar:

   - O terminos nos informou `Initialized empty Git repository in C:...`. O que significa que nossa pasta agora é um repositório local.

   - Note que ao lado do caminho da nossa pasta, agora é apresentado o termo `(master)`.

       <img src="./assets/img/git-master.jpg">

   - Uma pasta oculta `.git` foi criada em nosso repositório. Caso você não esteja vendo esta pasta, é porque sua visualização de pastas ocultas está desativada.

       <img src="./assets/img/repositorio-git-init.jpg">

## 3. Criando um repositório remoto (GitHub)

1. Acesse a sua conta do GitHub, caso você não tenha, ela pode ser criada [clicando aqui](https://github.com/).

2. Em seu perfil, acesse a aba de repositórios e clique em `New` para criar um novo repositório.

<img src="./assets/img/new-repositorio.jpg">

3. Vou nomear o repositório como `Tutorial Git`, assim como a pasta que criei anteriormente. Isso não é obrigatório, apenas estou adotando para seguir um padrão. As demais configurações do repositório podem permanescer como estão.

<img src="./assets/img/tutorial-repositorio.jpg">

4. Pronto, nosso repositório remoto foi criado! O próximo passo é fazer a interligação entre ele e nosso repositório local, criado no [Tópico 2. Criando um repositório local (Computador)](#topico2)
