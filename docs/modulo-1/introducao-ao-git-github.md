# Introdução ao Git e GitHub
Para esse treinamento, vamos utilizar o Git e o GitHub para versionar nosso código e compartilhar com os demais participantes.

## O que é Git?
Git é um sistema de controle de versão distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo.

Inicialmente desenvolvido por Linus Torvalds para o desenvolvimento do kernel Linux, o Git tem como foco a velocidade, integridade dos dados e suporte para desenvolvimento não-linear, distribuído, com milhares de "[branches](#branches)"(ramificações) ativas.

Imagine que você está desenvolvendo um sistema e precisa fazer uma alteração no código, mas não tem certeza se essa alteração vai funcionar. Você pode criar uma ramificação do seu código, fazer a alteração e testar. Se funcionar, você pode integrar essa alteração ao código principal, se não funcionar, você pode descartar essa alteração sem afetar o código principal.

Essa é uma das grandes vantagens do Git, a possibilidade de criar ramificações do código e trabalhar em paralelo, sem afetar o código principal.

## O que é GitHub?
GitHub é uma plataforma de hospedagem de código-fonte com controle de versão usando o Git. Ele permite que programadores, utilitários ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo.

No GitHub, além de hospedar o código-fonte, você pode criar [issues](#issues), [pull requests](#pull-requests), [releases](#releases), [branches](#branches), [tags](#tags), [forks](#forks), [gists](#gists), [wikis](#wikis) e muito mais.

Antes de prosseguir, é necessário criar uma conta no GitHub. Para isso, acesse o site oficial do [GitHub](https://github.com) e crie a sua conta.

## Instalando o Git
Para instalar o Git, acesse o site oficial do [Git](https://git-scm.com/downloads) e baixe a versão para o seu sistema operacional.

Para verificar se o Git foi instalado corretamente, abra o terminal e digite o comando abaixo:
```bash
git --version
```
Se o Git foi instalado corretamente, você verá algo parecido com isso:
```bash
git version 2.42.0
```

## Configurando o Git
Após instalar o Git, é necessário configurar o seu nome e e-mail, para que o Git possa identificar quem está fazendo as alterações no código.

Para configurar o seu nome, digite o comando abaixo no terminal:
```bash
git config --global user.name "Seu Nome"
```
Para configurar o seu e-mail, digite o comando abaixo no terminal:
```bash
git config --global user.email "exemplo@email.com"
```
Para verificar se o Git foi configurado corretamente, digite o comando abaixo no terminal:
```bash
git config --list
```
Se o Git foi configurado corretamente, você verá algo parecido com isso:
```bash
user.name=Seu Nome
user.email=exemplo@email.com
```

## Criando um repositório
Finalmente vamos criar o nosso primeiro repositório e começar a trabalhar com o Git(E não é o repositório do GitHub, é o repositório local).

Se você seguiu todos os passos anteriores, você já tem uma pasta chamada `curso-fullstack` no seu computador. Se você não tem essa pasta, crie uma pasta com esse nome.

Abra o terminal e navegue até a pasta `curso-fullstack`:
```bash
cd curso-fullstack
```

> Se você não sabe usar o terminal, talvez você tenha pulado uma etapa importante. [Clique aqui](./terminais.md) para aprender a usar o terminal.

Agora vamos inicializar o repositório:
```bash
git init
```
Se tudo ocorreu bem, você verá algo parecido com isso:
```bash
Initialized empty Git repository in /home/usuario/curso-fullstack/.git/
```

## Salvando as alterações
Você já deve ter duas pastas ou mais dentro da pasta `curso-fullstack`. Vamos adicionar essas pastas ao repositório:
```bash
git add .
```
Isso vai adicionar todas as pastas e arquivos ao repositório.

Se você quiser adicionar apenas uma pasta ou arquivo, você pode fazer assim:
```bash
git add nome-da-pasta
```
ou
```bash
git add nome-do-arquivo.extensao
```

Agora vamos salvar as alterações:
```bash
git commit -m "Mensagem de commit"
```
A mensagem de commit é muito importante, pois ela vai ajudar a identificar o que foi alterado no código.

Por isso criamos uma aula só para falar sobre [Commits](./commits.md).

## Criando um repositório no GitHub
Agora que já temos o nosso repositório local, vamos criar um repositório no GitHub.

Acesse o site do [GitHub](https://github.com) e faça login na sua conta.

Clique no botão `New` para criar um novo repositório.

Agora vamos preencher os campos:
- Repository name: `curso-fullstack`
- Description: `Curso Fullstack`
- Public
- Add a README file
- Add .gitignore: `None`
- Choose a license: `MIT License`

Clique no botão `Create repository`.

## Enviando o repositório local para o GitHub
Agora que já temos o repositório local e o repositório remoto, vamos enviar o repositório local para o GitHub.

Para isso, vamos adicionar o repositório remoto:
```bash
git remote add origin <url-do-repositorio>
```
Agora vamos enviar o repositório local para o GitHub:
```bash
git push -u origin main
```
Se tudo ocorreu bem, você verá algo parecido com isso:
```bash
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 219 bytes | 219.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:usuario/curso-fullstack.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```
## Branches
Branches são ramificações do código principal. Você pode criar uma ramificação do código principal, fazer alterações e testar. Se funcionar, você pode integrar essa alteração ao código principal, se não funcionar, você pode descartar essa alteração sem afetar o código principal.

Para criar uma ramificação, digite o comando abaixo no terminal:
```bash
git branch nome-da-branch
```
Para listar as branches, digite o comando abaixo no terminal:
```bash
git branch
```
Para mudar de branch, digite o comando abaixo no terminal:
```bash
git checkout nome-da-branch
```
Para criar uma branch e mudar para ela, digite o comando abaixo no terminal:
```bash
git checkout -b nome-da-branch
```
Para enviar uma branch para o GitHub, digite o comando abaixo no terminal:
```bash
git push origin nome-da-branch
```
Para enviar uma branch para o GitHub e criar uma branch com o mesmo nome no GitHub, digite o comando abaixo no terminal:
```bash
git push -u origin nome-da-branch
```
Para mesclar uma branch com a branch principal, digite o comando abaixo no terminal:
```bash
git merge nome-da-branch
```
Para deletar uma branch, digite o comando abaixo no terminal:
```bash
git branch -d nome-da-branch
```
Para deletar uma branch no GitHub, digite o comando abaixo no terminal:
```bash
git push origin --delete nome-da-branch
```
## Tags
Tags são usadas para marcar versões do código. Por exemplo, se você está desenvolvendo um sistema e chegou na versão 1.0.0, você pode criar uma tag para marcar essa versão.

Para criar uma tag, digite o comando abaixo no terminal:
```bash
git tag nome-da-tag
```
Para listar as tags, digite o comando abaixo no terminal:
```bash
git tag
```
Para enviar uma tag para o GitHub, digite o comando abaixo no terminal:
```bash
git push origin nome-da-tag
```
Para enviar todas as tags para o GitHub, digite o comando abaixo no terminal:
```bash
git push origin --tags
```
Para deletar uma tag, digite o comando abaixo no terminal:
```bash
git tag -d nome-da-tag
```
Para deletar uma tag no GitHub, digite o comando abaixo no terminal:
```bash
git push origin --delete nome-da-tag
```
## Releases
Releases são usadas para marcar versões do código que estão prontas para serem usadas. Por exemplo, se você está desenvolvendo um sistema e chegou na versão 1.0.0, você pode criar uma release para marcar essa versão.

Para criar uma release, acesse o repositório no GitHub, clique na aba `Releases`, clique no botão `Create a new release`, preencha os campos e clique no botão `Publish release`.

Em breve vamos criar uma aula só para falar sobre Releases.

## Forks
Forks são usados para criar uma cópia de um repositório. Por exemplo, se você quer contribuir com um projeto Open Source, você pode criar um fork do repositório, fazer as alterações e enviar um pull request.

Para criar um fork, acesse o repositório no GitHub, clique no botão `Fork` e selecione a sua conta.

Você não precisa obrigatoriamente contribuir com um projeto Open Source para criar um fork. Você pode criar um fork de um repositório e fazer as alterações que você quiser no código.

## Pull Requests
Pull Requests são usados para enviar alterações para um repositório. Por exemplo, se você criou um fork de um repositório, fez algumas alterações e quer enviar essas alterações para o repositório original, você pode criar um pull request.

Para criar um pull request, acesse o repositório no GitHub, clique na aba `Pull requests`, clique no botão `New pull request`, preencha os campos e clique no botão `Create pull request`.

Em breve vamos criar uma aula só para falar sobre Pull Requests.

## Issues
Issues são usadas para reportar bugs, solicitar novas funcionalidades, fazer perguntas, etc. Por exemplo, se você encontrou um bug em um sistema, você pode criar uma issue para reportar esse bug.

Um projeto pode ter várias issues abertas, mas é importante que as issues sejam claras e objetivas para que os desenvolvedores possam resolver o problema.

Através das issues, grandes projetos Open Source conseguem organizar o trabalho dos desenvolvedores e manter um histórico de bugs, novas funcionalidades, etc.

Para criar uma issue, acesse o repositório no GitHub, clique na aba `Issues`, clique no botão `New issue`, preencha os campos e clique no botão `Submit new issue`.

Por se tratar de um assunto muito importante, vamos criar uma aula só para falar sobre Issues.

## Gists
Agora vamos falar de algo que eu particularmente gosto muito, os Gists.

Gists são usados para compartilhar códigos, textos, etc. Por exemplo, se você quer compartilhar um código com alguém, você pode criar um Gist e enviar o link para a pessoa.

Para criar um Gist, acesse o site do [GitHub](https://gist.github.com), clique no botão `New gist`, preencha os campos e clique no botão `Create public gist`.

> Você pode criar um Gist público ou privado e pode adicionar quantos arquivos quiser.

## Wikis
Wikis são usadas para criar documentações. Por exemplo, se você quer criar uma documentação para o seu projeto, você pode criar uma Wiki.

Para criar uma Wiki, acesse o repositório no GitHub, clique na aba `Wiki`, clique no botão `Create the first page` e preencha os campos.

Já vamos adiantar que vamos criar uma Wiki para o nosso projeto final do curso.

## .gitignore
O arquivo `.gitignore` é usado para ignorar arquivos e pastas. Por exemplo, se você tem uma pasta com arquivos de configuração, você pode adicionar essa pasta ao `.gitignore` para que ela não seja enviada para o GitHub.

Preste muita atenção ao criar o arquivo `.gitignore`, pois se você adicionar uma pasta ou arquivo ao `.gitignore` depois de enviar o repositório para o GitHub, essa pasta ou arquivo continuará no GitHub.

Esse assunto é muito importante, por isso vamos criar uma aula só para falar sobre o segurança e o `.gitignore` está diretamente relacionado com a segurança do seu projeto.

## Conclusão
Nessa aula aprendemos o que é Git e GitHub, como instalar o Git, como configurar o Git, como criar um repositório, como salvar as alterações, como criar branches, como criar tags, como criar releases, como criar forks, como criar pull requests, como criar issues, como criar gists, como criar wikis e como usar o `.gitignore`.

Agora que você já sabe o básico do Git e GitHub, Vamos para a próxima aula.

< [Voltar para o índice](../../README.md) | [Próxima aula](./introducao-ao-javascript.md) >