# Clase 02 - Git desarrollo colaborativo

## Repasando dinamica de trabajo base de git

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