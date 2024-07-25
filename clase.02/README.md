# Clase 02 - Git desarrollo colaborativo

## Repasando dinamica de trabajo base de git

## Listar una cantidad especifica de commits en el log

```sh
git log --oneline -<cantidad-commits>
git log --oneline -5
git log --oneline -10
```

### Haciendo un commit. Pasos

1. Hacer un status para ver en que estado están los archivos que quiero sean parte del commit

```sh
git status
```

2. Agregar lo que quiero dentro del commit al área de confirmación (staging area)

```sh
git add <nombre-archivo>
git add clase.02/README.md
git add . # Agregar todo lo que sea parte de la funcionalidad en la que trabajo
```

3. Hago el commit. Todo lo que estuviera en el area de staging se guarda en el repositorio local.

```sh
git commit -m "Nuevo commit, mensaje descriptivo"
```

## Git diff comparo entre diferentes commits en el tiempo

```sh
git diff <hash> <hash>
git diff 6ceff27 3760d7e
```

## Para agregar algo que olvide o quiero incorparar en el último commit, uso el siguiente comando

```sh
git add .
git commit --amend
```
# Ramas (Branches)
Nos permiten trabajar en el proyecto de manera auxiliar.

## Listar ramas

```sh
git branch
```

## Crear un rama

```sh
git branch <nombre-rama>
git branch feature/navbar
git branch feature/footer
```

## Moverme entre ramas

```
git switch <nombre-rama>
git switch feature/navbar
```

## Crear y moverme

```sh
git switch -c <nombre-rama>
git switch -c feature/ramas
```