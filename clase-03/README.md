# CLase 03 - Git desarollo colaborativo

## Borrando una rama

```sh
git branch -d <nombre de la rama> # Si la rama ya esta en alguna otra rama fusionada
git branch -D # Fuerzo el borrado a pesar de que el contenido de esta rama no este en otro lado
```

## Clonado de un repositorio
Si quiero que la carpeta .git exista en mi local, necesito clonar el repositorio.

```sh
git clone https:// etc .git
```
# arreglar un mensaje de commit o agregar en un commit un archivo que me olvide
``` sh
git commit -amend -m "Mensaje ( se borra la DIR del commit y se reemplaza por una nueva)"
```


