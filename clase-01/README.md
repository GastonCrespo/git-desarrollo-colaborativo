# Clase 01 - Git Desarrollo Colaborativo

## Crear un respositorio de GIT

```sh
git init
```

## Configurar por primera vez y única a GIT

```sh
git config --global user.name "Gaston config --global user.email "cualquiercorreo@gmail.com"

```

## Listar configuraciones git para verificar si tengo o no esto configurado

```sh
git config --list
```

## Cambiar de acá en adelante como se va a llamar la rama principal por defecto

```sh
git config --global init.defaultBranch main
```

# Para pasar del working directory al staging area (index)

```sh
git add <nombre-archivo>
git add README.md
```

## Como ver el estado del archivo y en que área está

```sh
git status
```

## Para pasar del stanging area al local repo

```sh
git commit -m "mensaje descriptivo" # -m <---- mensaje
```

## Como ver la lista de commits

```sh
git log # versión larga
git log --oneline # versión corta
```

## Como ver diferencias entre el workding directory y el local repo

```sh
git diff
```

## Ver el contenido del commit y quien hizo ese commit

```sh
git show <hash>
git show 8f2a
```