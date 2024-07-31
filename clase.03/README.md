# Clase 03 - Git Desarrollo Colaborativo

## Ramas (Branches)

![estructuras-ramas](_ref/basica.png)

![Alt text](_ref/avanzada.png)

## Creando un rama

```sh
git branch <nombre-rama>
```

## Crear rama y moverse a esa rama

```sh
git switch -c <nombre-rama>
git switch -c feature/footer
```

## Listar ramas dentro de un repositorio

```sh
git branch
```

## Cambiar de ramas

```sh
git switch <nombre-rama>
git switch feature/ramas
git switch - # Toogle entre las últimas 2 ramas
```

## Borrar una rama

```sh
git branch -d <nombre-rama>
git branch -d feature/footer # Si los cambios existen en otra rama de nuestro repositorio voy a poder borrar la rama sin problemas pero si no existen tengo que forzar el borrado de la rama.
git branch -D feature/footer # Fuerzo el borrado de la rama cuando los cambios (commits) que tengo dentro de la rama, no forman parte de alguna de las ramas.
```

## Para ver todas las ramas del proyecto

```sh
git log --oneline --decorate --graph --all
```

## Git Merge (Fusiones)

Nota: Tengo que estar ubicando en la rama en la cual me quiero traer los cambios. O sea si tengo la rama feature/branches y quiero traerme los cambios a main. Tengo que estar parado sobre la rama main y ejecutar el siguiente comando

```sh
git switch main
git merge <nombre-rama-que-quiero>
git merge feature/branches
```

IMPORTANTE: Si los integrantes del proyecto no estan todos para la fusión. Debo abortar el proceso.

## Tipos de fusiones

* Fast-forward: Este tipo de fusión, git lo hace automaticamente
* Tiple vía: Este tipo de fusión, git lo hace automaticamente
* Conflicto: Este tipo de funsión, git no lo puede resolver automaticamente. Lo tenemos que solucionar nosotros.

## Clientes de GIT con GUI (Interfaz Gráfica)

* GitHub Desktop <https://github.com/apps/desktop>
* GitKraken <https://www.gitkraken.com/>
* Alternatives <https://alternativeto.net/software/gitkraken/>
