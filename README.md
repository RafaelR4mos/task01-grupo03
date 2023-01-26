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

**Comando**

```md
git checkout -b <nome-da-branch> //Exemplo
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's.

**Exemplo de uso:**

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

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
