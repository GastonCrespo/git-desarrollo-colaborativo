# Clase 02 Git Desarrollo Colaborativo

# Repaso

# 1. VERIFICAMOS EL ESTADO ACTUAL
# Tiramos un status para ver cómo está nuestro proyecto. 
# Git detecta que creamos una carpeta nueva (clase-02/) pero nos avisa en rojo 
# que está "untracked" (sin rastrear). Es decir, Git todavía no le está prestando atención.
git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        clase-02/

nothing added to commit but untracked files present (use "git add" to track)


# 2. PREPARAMOS EL ARCHIVO (STAGING)
# Usamos "add" para decirle a Git: "empezá a seguir este archivo específico y preparalo 
# porque lo voy a querer guardar". Lo pasamos a lo que se llama "Staging Area".
git add clase-02/README.md 


# 3. CHEQUEAMOS QUE SE HAYA AGREGADO BIEN
# Volvemos a tirar status. Ahora Git nos muestra en verde ("Changes to be committed") 
# que el archivo nuevo ya está listo y en la sala de espera para ser guardado (comiteado).
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   clase-02/README.md


# 4. GUARDAMOS LOS CAMBIOS LOCALMENTE (COMMIT)
# Hacemos el commit, que es como sacarle una "foto" al proyecto en este estado. 
# Le agregamos la bandera -m para dejar un mensaje claro ("iniciando clase 02") 
# que nos sirva para el historial.
git commit -m "iniciando clase 02"
[main f8705fa] iniciando clase 02
 1 file changed, 1 insertion(+)
 create mode 100644 clase-02/README.md


 # 5. VERIFICAMOS EL ESTADO FINAL
 # Tiramos un último status. Git nos dice que nuestra máquina está limpia ("working tree clean"),
 # pero nos avisa que estamos 1 commit por delante de la nube ('origin/main'). 
 # Básicamente nos está diciendo: "Ya guardaste todo acá, ahora solo te falta hacer un 'git push' 
 # para subirlo al repositorio remoto".
 git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean


# ¿Qué pasa si modifico un archivo DESPUÉS de hacer un commit?
# Si todavía no hice "git push", tengo dos opciones para guardar estos nuevos cambios:

# ---------------------------------------------------------
# OPCIÓN 1: Hacer un nuevo commit (El camino tradicional)
# ---------------------------------------------------------

# 1. VOLVEMOS A PREPARAR EL ARCHIVO (STAGING)
# Git detecta que el archivo fue modificado. Usamos "add" para prepararlo de nuevo.
git add clase-02/README.md

# 2. CHEQUEAMOS EL ESTADO
# Git nos muestra en verde que el archivo fue modificado (modified) y está listo para guardarse.
git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   clase-02/README.md

# 3. HACEMOS EL NUEVO COMMIT
# Creamos una nueva "foto" con un mensaje que describa esta última modificación.
git commit -m "Agrego comentarios explicativos al repaso"
[main abc1234] Agrego comentarios explicativos al repaso
 1 file changed, 15 insertions(+), 2 deletions(-)


# ---------------------------------------------------------
# OPCIÓN 2: Modificar el commit anterior (El "truquito" Pro)
# ---------------------------------------------------------
# Ideal para no llenar el historial de commits chiquitos por olvidos. 
# IMPORTANTE: Solo se recomienda si todavía NO hicimos "git push".

# 1. PREPARAMOS EL ARCHIVO MODIFICADO (Igual que siempre)
git add clase-02/README.md

# 2. CHEQUEAMOS EL ESTADO
git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   clase-02/README.md

# 3. SOBREESCRIBIMOS EL ÚLTIMO COMMIT CON --amend
# Fusionamos estos nuevos cambios adentro del commit anterior. 
# Podemos cambiarle el mensaje para que abarque todo lo que hicimos.
git commit --amend -m "Iniciando clase 02 y sumando apuntes de repaso"
[main def5678] Iniciando clase 02 y sumando apuntes de repaso
 Date: Wed Apr 29 11:32:00 2026 -0300
 1 file changed, 20 insertions(+)
 create mode 100644 clase-02/README.md


 ## .gitignore 
Me permite indicar los archivos o carpetas que quiero modificar que no formen parte del repositorio. por ejemplo archivos de log durante desarollo, archivos temporales, variables de entorno  etc.

## .gitkeep
Ayuda versionar carpetas que quiero que sean partes del repositorio pero estan vacías.
**se crea el archivo .gitkeep dentro de la carpeta que quiero que versione**