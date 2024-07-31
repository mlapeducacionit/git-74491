## Clase 04 - Git Desarrollo Colaborativo

### Área de Stash
Los stashes son para el trabajo individual, no se suben al remoto. Puedo tener más de un stash en la caja de stashes. Es una estructura de datos conocida como pila.

#### Listar stashes

```sh
git stash list
```

#### Crear un stash

```sh
git stash
git stash -m "Empezando a trabajar con stashes"
```

#### Aplicar un stash (el último)
Si lo aplica. Borra el último stash. Si hay conflicto. Lo aplica y no lo borra.

```sh
git stash pop
```

#### Aplicación de un stash en particular
Lo aplica pero nunca borra el stash

```sh
git stash apply <numero de stash>
git stash apply 1 # stash@{1}
```

### Borrar un stash (el último)

```sh
git stash drop 
```

### Borrar un stash en particular

```sh
git stash drop <numero-stash>
git stash drop 5 # stash@{5}
```

# Git alias
Me permite crear alias de comandos para en vez de estar escribiendo el comando y sus subcomandos hacerlo a traves de una letra o una palabra.

## Creando un alias

```sh
git config --global alias.<alias-elegido> "<comando-de-git-sin-la-palabra-git>"
git config --global alias.s "status --short"
git config --global alias.c "commit -m"
git config --global alias.l "log --oneline"
git config --global alias.ll "log --oneline --all --graph --decorate"
```

## Quitar un alias

```sh
git config --global --unset alias.ll # me quita el alias ll
```

## Listar alias configurados

```sh
git config --global --get-regexp alias
```

# GIT RESET
Me permite deshacer cambios en el árbol de trabajo y en el área de preparación (Staging Área) de git

## 3 tipos de resets

1. Reset Soft
Va a borrar el commit o los commits seleccionados y arrojar los cambios al staging area

```sh
git reset --soft <hash>
```

2. Reset Mixed
Va a borrar el commit o los commits seleccionados y arrojar los cambios al working directory

```sh
git reset <hash>
git reset --mixed <hash>
```

3. Reset Hard
Va a borrar el commit o los commits seleccionados y descartar los cambios dentro de esos commit.

```sh
git reset --hard <hash>
```

## Para ver la historia del principio de lo tiempos y todos los cambios

```sh
git reflog
```