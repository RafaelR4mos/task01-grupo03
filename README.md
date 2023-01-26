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

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

**Comando: Sintaxe completa**

```md
git rebase [-i | --interactive] [<options>] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
git rebase [-i | --interactive] [<options>] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
git rebase (--continue | --skip | --abort | --quit | --edit-todo | --show-current-patch)
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's.

**Exemplo de uso:**
Você está há algum tempo sem trabalhar em uma branch e está se tornou desatualizada em relação a branch main, conforme a seguinte ilustação:
```
          A---B---C topic
         /
    D---E---F---G master
```
Podendo assim utilizar o git rebase para realocar sua branch e seus commits em relação a main e os commits mais atuais:
```
git rebase master
git rebase master topic
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

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
