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