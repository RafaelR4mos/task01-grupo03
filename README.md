# Comandos GIT

🔵 Desenvolvido por: Alunos do **programa Vem Ser 11ª edição** . [Saiba mais!](README-info.md)

> Aprenda sobre alguns dos comandos git que podem passar despercebidos por desenvolvedores, mas que ao mesmo tempo podem ser um fator determinante entre essoas que sabem git ou não.

**Lista de comandos**:

-   [Rebase](#Rebase)
    -   Definição
    -   Sintaxe
    -   Exemplos de uso
-   [Cherry Pick](#Cherry-Pick)
    -   Definição
    -   Sintaxe
    -   Exemplos de uso
-   [Revert](#Revert)
    -   Definição
    -   Sintaxe
    -   Exemplos de uso
-   [Squash](#Squash)
    -   Definição
    -   Sintaxe
    -   Exemplos de uso

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

O comando `git cherry-pick ` possibilita selecionar commits de sua escolha, vindos de uma branch diferente sendo simplesmente baseado na ação de selecionar um commit de uma branch e aplicar a outra. Através do nome "Pegar Cereja", do inglês "Cherry Pick", é possível fazer uma analogia em que: **Apenas** a cereja (commit) é retirada de um bolo (branch) e transferida para outro.

Antes do Cherry Pick:

```
   a - b - c - d   Main
         \
           e - f - g Feature

```

Após execução do comando, aplicando o _pick_ em 'f':

```
    a - b - c - d - f   Main
         \
           e - f - g Feature
```

### **Sintaxe**

```
git cherry-pick <commitSha> // Onde, "commitSha" é a referência do commit
```

> NOTE: A referência do commit pode ser obtida através do comando `git log` que retorna algo como:

```
commit 146ab86f964d266e7e8edebfb152fda269ccd7cd
Author: Joe <joedoe@example.com>
Date:   Wed Jan 25 20:11:15 2023 -0300
```

obs: A informação necessária é o **identificador** ao lado de _commit_

> NOTE: lembre-se de estar na branch em que deseja transferir o commit selecionado através do cherry pick. Para trocar de branch `git checkout <nome-da-branch> `

Já na branch desejada e com o identificador do commit a ser selecionado digite, por exemplo:

```
git cherry-pick 146ab86f964d266e7e8edebfb152fda269ccd7cd
```

### **Aplicação**

Por mais que o Cherry Pick possa "burlar" as regras do git flow ele pode ser uma ótima ferramenta para realizar ajustes rápidos extraindo somente alguns trechos de código para outras branch em um processo relativamente simples e sem precisar executar merges e etc. Entretanto não é recomendado utilizar este comando em ambientes de trabalho com git flow definidos.

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
Caso o código de uma certa branch já esteja com muitos commits o squash pode ser usado para simplificá-los e transformar todos em um só commit na main.

---

by 🔵 [Alunos Vem Ser 11ª edição](README-info.md)
