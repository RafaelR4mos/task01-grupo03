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

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

**Comando**

```md
git checkout -b <nome-da-branch> //Exemplo
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's.

**Exemplo de uso:**

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

## Squash

---

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

**Comando**

```md
git checkout -b <nome-da-branch> //Exemplo
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's.

**Exemplo de uso:**

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

---

by 🔵 [Alunos Vem Ser 11ª edição](README-info.md)
