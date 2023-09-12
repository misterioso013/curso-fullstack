# Commits
Preparamos um conteúdo para você aprender a trabalhar com commits de forma eficiente e organizada.

## O que é um commit?
Um commit é uma forma de salvar o estado atual do seu projeto, ou seja, é uma forma de salvar o que você fez até o momento. Com isso, você pode voltar para um estado anterior do seu projeto, caso seja necessário.

## Como fazer um commit?
Para fazer um commit, você precisa adicionar os arquivos que você deseja salvar e depois executar o comando `git commit -m "Mensagem do commit"`. Veja o exemplo abaixo:

```bash
git add .
git commit -m "Adicionando o arquivo index.html"
```

Acima, adicionamos todos os arquivos que foram modificados e depois fizemos o commit com a mensagem "Adicionando o arquivo index.html".

## Como fazer um commit com um arquivo específico?
Para fazer um commit com um arquivo específico, você precisa adicionar o arquivo que você deseja salvar e depois executar o comando `git commit -m "Mensagem do commit"`. Veja o exemplo abaixo:

```bash
git add index.html
git commit -m "Adicionando o arquivo index.html"
```
Veja como é simples fazer um commit com um arquivo específico ou com todos os arquivos modificados. Agora, vamos falar sobre boas práticas de commit que é muito importante para manter o seu projeto organizado.

## Boas práticas de commit
É muito importante manter o seu projeto organizado, pois, caso você precise voltar para um estado anterior do seu projeto, você vai conseguir encontrar o que você precisa com facilidade. E além disso, se você trabalha em equipe as mensagens de commit precisam ser claras para que todos entendam o que foi feito.

### Convencional Commits
O Convencional Commits é uma convenção para mensagens de commit. Essa convenção define um padrão para as mensagens de commit, ou seja, todas as mensagens de commit devem seguir esse padrão. Veja abaixo um exemplo de mensagem de commit seguindo o Convencional Commits:

```bash
git commit -m "feat: adicionando o arquivo index.html"
```
Acima, temos uma mensagem de commit seguindo o Convencional Commits. A mensagem de commit começa com o tipo do commit, que no caso é `feat` que significa que foi adicionado uma nova funcionalidade. Depois, temos a descrição do commit que é `adicionando o arquivo index.html`.

### Tipos de commit
Abaixo, temos uma lista com os tipos de commit que você pode usar:

- `feat`: Adicionando uma nova funcionalidade
- `fix`: Corrigindo um bug
- `docs`: Alterando a documentação
- `style`: Alterando o estilo do código
- `refactor`: Refatorando o código
- `test`: Alterando testes
- `chore`: Alterando configurações e tarefas de build
- `perf`: Alterando código para melhorar a performance
- `ci`: Alterando configurações do CI

### Descrição do commit
A descrição do commit deve ser clara e objetiva, ou seja, deve ser fácil de entender o que foi feito. Veja abaixo alguns exemplos de descrição de commit:

- `adicionando o arquivo index.html`
- `corrigindo o bug na página de login`
- `alterando o estilo do botão`

### Mensagem de commit
A mensagem de commit deve seguir o padrão abaixo:

```bash
<tipo>: <descrição>
```
Veja abaixo alguns exemplos de mensagem de commit:

```bash
feat: adicionando o arquivo main.css
fix: corrigindo o bug na página de login
style: alterando o estilo do botão
```
Agora que você já sabe como fazer um commit e como seguir o Convencional Commits, vamos falar sobre como fazer um commit com uma mensagem de commit que não segue o Convencional Commits e o porquê você não deve fazer isso.

## Commit sem seguir o Convencional Commits
Você pode fazer um commit sem seguir o Convencional Commits, mas não é recomendado fazer isso. Pois, se você fizer isso, você não vai conseguir usar o `git log` para ver os commits de forma organizada. Veja abaixo um exemplo de mensagem de commit que não segue o Convencional Commits:

```bash
git commit -m "adicionando novo arquivo"
```
Acima, temos uma mensagem de commit que não segue o Convencional Commits. A mensagem de commit não começa com o tipo do commit, ou seja, não sabemos qual foi o tipo do commit. E além disso, a mensagem de commit não tem uma descrição clara, ou seja, não sabemos o que foi feito.

## Conclusão
Esse foi um conteúdo curto para onde falamos sobre commits e boas práticas de commit. Você pode ver mais sobre commits na documentação do Git: [https://git-scm.com/docs/git-commit](https://git-scm.com/docs/git-commit) e sobre o Convencional Commits: [https://www.conventionalcommits.org/pt-br/v1.0.0/](https://www.conventionalcommits.org/pt-br/v1.0.0/).

[Agora você já pode voltar para a página anterior de onde parou e continuar o seu aprendizado sobre Git e GitHub](./introducao-ao-git-github.md#criando-um-repositório-no-github).