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

#### Aplicar un stash (el últimos)

```sh
git stash pop
```

#### Aplicación de un stash en particular

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
