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