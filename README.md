# Comandos GIT

🔵 Desenvolvido por: Alunos do **programa Vem Ser 11ª edição** . [Saiba mais!](README-info.md)

> Aprenda sobre alguns dos comandos git que podem passar despercebidos por desenvolvedores, mas que ao mesmo tempo podem ser um fator determinante entre essoas que sabem git ou não.

**Lista de comandos**:

- [Rebase](#Rebase)
  - Definição
  - Sintaxe
  - Exemplos de uso
- [Cherry Pick](#Cherry-Pick)
  - Definição
  - Sintaxe
  - Exemplos de uso
- [Revert](#Revert)
  - Definição
  - Sintaxe
  - Exemplos de uso
- [Squash](#Squash)
  - Definição
  - Sintaxe
  - Exemplos de uso

## Rebase

---

O comando **git rebase** permite que você transfira seus commits de um branch para outro diferente. Isso pode ser útil para sincronizar o seu trabalho com as alterações recentes ou para resolver conflitos antes de realizar o merge.

**Sintaxe**

```md
git rebase [-i | --interactive] [<options>] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
git rebase [-i | --interactive] [<options>] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
git rebase (--continue | --skip | --abort | --quit | --edit-todo | --show-current-patch)
```

**Exemplo de uso:**

Você está há algum tempo sem trabalhar em uma branch e está se tornou desatualizada em relação a branch main, conforme a seguinte ilustação:

```
          A---B---C topic
         /
    D---E---F---G main
```

Podendo assim utilizar o git rebase para realocar sua branch e seus commits em relação a main e os commits mais atuais:

```
git checkout topic
git rebase main
```

Assim, podemos visualizar a nova disposição desta branch conforme a seguinte ilustração:

```
                  A'--B'--C' topic
                 /
    D---E---F---G main
```

Existem outras aplicações para este comando ao explorar seus parâmetros como transferir uma ramificação de uma para outra branch com a opção rebase --onto, contando com a possibilidade de realizar correções em caso de conflitos ou desistir da operação. Pode verificar estes e outros exemplos em https://git-scm.com/docs/git-rebase .

## Cherry Pick

---

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

**Comando**

```md
git checkout -b <nome-da-branch> //Exemplo
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's.

**Exemplo de uso:**

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

## Revert

---

Git revert é um comando que reverte o que foi feito dentro de um ou mais commits.
Para isso funcionar a arvore de trabalho (_working tree_) deve estar limpa e sem modificações.
Após as alterações um novo commit será criado com as alterações revertidas.

**Comando**

```md
git revert <chave-do-commit-a-ser-alterado>
ou
git revert HEAD~<número-a-partir-de-1>
```

Se a chave do commit a ser alterado for c1f5c789.
A sintaxe do comando ficará assim:

    ```
    git revert c1f5c789
    ```

Já se for alterado usando o HEAD~, deve botar o número que deseja alterar, sendo o do último commit feito o número 1, o penúltimo 2 e assim em diante.
Caso eu queira mudar o penúltimo commit ficará assim:

    ```
    git revert HEAD~2
    ```

**Exemplo de uso:**

Se 10 linhas foram alteradas em um novo commit ao usar o comando revert, essas linhas são alteradas para o seu estado original antes dessas 10 linhas serem alteradas, criando assim um novo commit com essas alterações feitas.

## Squash

---

O comando squash é uma funcionalidade do comando git merge, utilizando o squash é possível juntar commits de uma branch qualquer a branch main em um só commit.

**Comando**

```md
git merge --squash <nome-da-branch>
```

Se eu quero alterar a branch <feat/to-do-list-TK002> a sintaxe do comando ficará assim:

    ```
    git merge --squash feat/to-do-list-TK002
    ```

**Exemplo de uso:**

Esse comando pode ser aplicado para diminuir o número de commits em um só.
Caso o código de uma certa brnach já esteja com muitos commits o squash pode ser usado para simplificá-los e transformar todos em um só commit na main.

---

by 🔵 [Alunos Vem Ser 11ª edição](README-info.md)
