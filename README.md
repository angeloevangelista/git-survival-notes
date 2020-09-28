<h1 align="center">

![Git Tuto](.github/images/logo.png)

</h1>

<h3 align="center">
  Git Tuto
</h3>
<p>

<p align="center">Esperamos que este tutorial possa te ajudar a dar seus primeiros passinhos com o git. 😉</p>

# Indice

- <a href="#instalação">Instalação</a>
- <a href="#configuração-inicial">Configuração inicial</a>
- <a href="#iniciando-um-repositório">Iniciando um repositório</a>

# Instalação

Para comerçarmos será necessário instalar o _[git](https://git-scm.com/)_ no seu sistema, você pode seguir os procedimentos na [página oficial](https://git-scm.com/) ou seguir para [este tutorial](./INSTALL_GIT.md) mais específico.

<br/>

# Configuração inicial

Agora que temos o Git instalado no nosso sistema, vamos às configurações iniciais. Por agora, vamos configurar o seu **_nome de usuário_** e o seu **_email_**. Essas informações são necessárias para que você seja capaz de realizar commits, que são os "Pontos na história", veremos como criá-los mais a frente. 😉

Para as configurações citadas, basta executar os seguintes comandos, substituindo os valores:

```bash
$ git config --global user.name "Seu Nome"

# Ex.: git config --global user.name "Angelo Evangelista"


$ git config --global user.email "seu_email@dominio.com"

# Ex.: git config --global user.email "angeloevan@gmail.com"

```

Pronto, a partir de agora podemos ir para o próximo passo.

<br/>

# Iniciando um repositório

Um repositório do git é basicamente uma "pasta" na qual você terá o controle de versionamento, isto significa que você terá uma sequência de mudanças e poderá "navegar" entre elas.

Imagine então que o seu código está numa linha do tempo, e que você terá um controle temporal sobre ela, logo, poderá restaurar para qualquer "momento na história" que desejar, mas é claro, você precisará definir estes "pontos".

<br/>

Para iniciar um repositório vazio, basta rodar o comando _`init`_:

![example-init](./.github/images/example-init.png)

A partir de agora qualquer alteração nesta pasta será "enxergada" pelo git, e podemos adicionar o que mudamos para um "grupo de mudanças", o que chamamos de _commit`_.

<br/>

Faremos um exemplo seguindo os seguintes passos:

1. Criaremos um arquivo `html` simples, com o nosso querido <a href="https://www.youtube.com/watch?v=Yw6u6YkTgQ4" target="_black">Hello, World</a>.

1. Verificaremos o que foi alterado no nosso projeto/pasta.

1. Após isso, adicionaremos o arquivo criado ao grupo de arquivos que serão usados para criar um ponto de modificação na linha do tempo.

1. Criaremos um ponto na linha do tempo.

1. Veremos os pontos na nossa linha do tempo.

**Let's Go! 🚀**

<br/>

**Passo 01:**

!["Hello, World" in html](./.github/images/example-html_01.png)

Podemos ver um html bem simples, mas muito simpático.

<br/>

**Passo 02:**

![Exibindo status de alterações](./.github/images/example-status_01.png)

Utilizando o comando _`status`_ nós podemos ver todas as alterações feitas na pasta, mudanças como _**adições**_, _**remoções**_, de arquivos, ou mesmo _**alterações**_ no conteúdo destes.

<br/>

**Passo 03:**

Para adicionar arquivos ao _commit_, nós precisamos usar o comando _`add`_. Sua sintaxe é a seguinte:

```bash

$ git add arquivo_expecifico.ext

$ git add arquivo_01.ext arquivo_02.ext ...

$ git add diretório

# Ex.: git add ./
#                 Diretório atual inteiro

```

Agora adicionaremos nosso `index.html`.

![Adicionando index.html](./.github/images/example-add_01.png)

Se executarmos o comando `status` novamente, veremos que um arquivo foi adicionado com sucesso.

<br/>

**Passo 04:**

A partir de agora, chamaremos nossos pontos na linha do tempo de _'commits'_.

Para criar um _commit_, nós usamos o comando `commit`, sim é isso mesmo 😅. Sua sintaxe é a seguinte:

```bash
$ git commit -m "Sua mensagem descritiva"

# Ex.: git commit -m "Validando dados do formulário"
```

Vejamos como fica nosso exemplo...

![Fazendo commit do index.html](./.github/images/example-commit_01.png)

**Atenção:** É de extrema importância que a descrição usada nos commits seja clara e objetiva, é ela que você vai usar para entender facilmente o que foi alterado naquele ponto da história, então nada de _"Alterando projeto..."_

<br/>

**Passo 05:**

Como todo bom viajante do tempo, nós precisamos de uma forma para saber do passado, faz sentido?

Para vermos os commits anteriores, usaremos o comando _`log`_, vejamos:

![Exibindo commits](./.github/images/example-log_01.png)

**Informações**

1. Autor do commit, quem realizou o commit.
1. Data em que o commit foi realizado.
1. Mensagem inserida no momento do commit

O _hash_ em amarelo no topo é o que usaremos futuramente para navegar entre os commits, mas calma, tudo a seu tempo...

**Atenção**
Para fechar esta listagem, basta pressionar a tecla `'q'`. Viu só? É bem mais fácil do que fechar o [Vim](https://www.vim.org/) (risos).
