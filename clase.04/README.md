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

# Trabajar en proyectos Open Source (Fork y Pull Request)


1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.
---
5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

    git remote add upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

    git pull upstream <rama-que-quiero-actualizar>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

    git push origin <rama-a-actualizar>

## GITHUB CLI
Es un herramienta para interacturar con los repositorios remotos de GITHUB

<https://cli.github.com/>


## GIST
Compartir código, pasar snippet a otras personas o información que quiero compartir.

<https://gist.github.com/>

Secretos => Solo la persona que tienen link puede verlo. No son privados
Publicos => Se van indexar en los motores de búsqueda

Pueden tener varios archivos y sus revisiones.


## Crear caratula o presentación de mi cuenta de github

Tengo que crear un repo con este nombre: mlapeducacionit

## GIT PAGES
Me permite alojar un sitio, estaticos. Aplicaciones React, Vue, Angular.
Hosting gratuito.

Respositorio que me crear una GitPages: mlapeducacionit.github.io

Hay que activar las GitHub Pages... 

Settings > Pages...