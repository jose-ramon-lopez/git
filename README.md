# To git or not to git

## Git Source Control
Se usa para:
- Colaboración
- Versiones
<br><br/>

git no shace seguimiendo de directorios

Sistema distribuido que controla los cambios.
- Me bajo todo el source control en mi rama
- sincronizo la rama con la principal
<br><br/>

GitHub es un reppositorio de git

## Installing git
<pre>
git config --global user.name "jlopez98"
git config --global user.email "joseramon.lopez@dxc.com"
</pre>

## Configuring git
<pre>
git config --list --show-origin
file:C:/CloudOpsSoftware/Git/etc/gitconfig      diff.astextplain.textconv=astextplain
file:C:/CloudOpsSoftware/Git/etc/gitconfig      filter.lfs.clean=git-lfs clean -- %f
file:C:/CloudOpsSoftware/Git/etc/gitconfig      filter.lfs.smudge=git-lfs smudge -- %f
file:C:/CloudOpsSoftware/Git/etc/gitconfig      filter.lfs.process=git-lfs filter-process
file:C:/CloudOpsSoftware/Git/etc/gitconfig      filter.lfs.required=true
file:C:/CloudOpsSoftware/Git/etc/gitconfig      http.sslbackend=schannel
file:C:/CloudOpsSoftware/Git/etc/gitconfig      core.autocrlf=true
file:C:/CloudOpsSoftware/Git/etc/gitconfig      core.fscache=true
file:C:/CloudOpsSoftware/Git/etc/gitconfig      core.symlinks=false
file:C:/CloudOpsSoftware/Git/etc/gitconfig      pull.rebase=false
file:C:/CloudOpsSoftware/Git/etc/gitconfig      credential.helper=manager
file:C:/CloudOpsSoftware/Git/etc/gitconfig      credential.https://dev.azure.com.usehttppath=true
file:C:/CloudOpsSoftware/Git/etc/gitconfig      init.defaultbranch=master
file:C:/Users/jlopez98/.gitconfig       user.name=jlopez98
file:C:/Users/jlopez98/.gitconfig       user.email=joseramon.lopez@dxc.com
file:.git/config        core.repositoryformatversion=0
file:.git/config        core.filemode=false
file:.git/config        core.bare=false
file:.git/config        core.logallrefupdates=true
file:.git/config        core.symlinks=false
file:.git/config        core.ignorecase=true
file:.git/config        remote.origin.url=https://github.com/jose-ramon-lopez/git.git
file:.git/config        remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
file:.git/config        branch.main.remote=origin
file:.git/config        branch.main.merge=refs/heads/main
file:.git/config        branch.main.vscode-merge-base=origin/main
PS C:\Users\jlopez98\OneDrive - DXC Production\Desktop\JR\git> 
PS C:\Users\jlopez98\OneDrive - DXC Production\Desktop\JR\git>
</pre>

## updating git
git update-git-for-windows


## git commands
<pre>
Version de git
git --version
git version 2.48.1.windows.1
</pre>

## Basic git
- Repository: Donde el source control guardia los ficheros, ficheros de control, etc.
- Init: Inicializa el source control.
- Clone: Copio el repositorio a local
- .gitignore: ignora ciertos ficheros del source control
- Stage: Da a conocer al source control los cambios que yo quiero agrupar
- Commit: Añado a stage un título y es un set de cambios y lo mando al source control. Se ven en el history
- Amend: Cambia el commit, por si falta un fichero, hay un typo...
- Remote: Es el repositorio principal
- Local: Es el repositorio de mi PC
- Push: Llevo mi commit al repositorio remote
- Pull: Traigo a mi repositorio local los cambios pendientes
- Fetch: Trae los cambios del repositorio remoto al local pero no cambia los ficheros locales.  Se usa para ver los cambios antes de cambiar el repositorio local
- Sync: hace un pull y un push
    1. Pull
    2. Push 
- Stash: Llevo los cambios a un espacio temporal y vuelvo a los ficheros anteriores
- Branch: Es una bifurcación de la rama principal del repositorio 
- Fork: Bajarse/copiar un repositorio.
- Merge y merge conflict: Es unir 2 branches.
- Fast Forward: Es un commit "falso" cuando un rama evoluciona y la main no. Entonces hay un comit fast forward para unirlas
- Head: Es el último commit de una branch por defecto, pero puedo mover mover el head a un commit anterior.     
- Rebase: Rehace el historial. Es como un merge pero en vez de la rama main y otra rama convierte el historial a solo la main añadiendo a esta los cambios de la otra rama. Se usa antes de un merge para limpiar el historial de tu rama.
- Tags: Identifica un commit
- Pull request: Petición para actualizar mi rama a partir de la suya

## basic process
### crear un repopsitorio
En un directorio
git init
ayuda: Usando 'master' como el nombre de la rama inicial. Este nombre de rama predeterminado
ayuda: está sujeto a cambios. Para configurar el nombre de la rama inicial para usar en todos
ayuda: de sus nuevos repositorios, reprimiendo esta advertencia, llama a:
ayuda: 
ayuda:  git config --global init.defaultBranch <nombre>
ayuda: 
ayuda: Los nombres comúnmente elegidos en lugar de 'master' son 'main', 'trunk' y
ayuda: 'development'. Se puede cambiar el nombre de la rama recién creada mediante este comando:
ayuda: 
ayuda:  git branch -m <nombre>
Inicializado repositorio Git vacío en /home/jose/gitRepo/.git/

y se crea el directorio .git



git init dirName crea un dir yrepo

git init
ayuda: Usando 'master' como el nombre de la rama inicial. Este nombre de rama predeterminado
ayuda: está sujeto a cambios. Para configurar el nombre de la rama inicial para usar en todos
ayuda: de sus nuevos repositorios, reprimiendo esta advertencia, llama a:
ayuda: 
ayuda:  git config --global init.defaultBranch <nombre>
ayuda: 
ayuda: Los nombres comúnmente elegidos en lugar de 'master' son 'main', 'trunk' y
ayuda: 'development'. Se puede cambiar el nombre de la rama recién creada mediante este comando:
ayuda: 
ayuda:  git branch -m <nombre>
Inicializado repositorio Git vacío en /home/jose/gitRepo/.git/

### -gitignore
Ignora archivos para commits

### commit archivo
git status
En la rama master

No hay commits todavía

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        .gitignore
        MyCode.txt

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)

git add .gitignore 

git status
En la rama master

No hay commits todavía

Cambios a ser confirmados:
  (usa "git rm --cached <archivo>..." para sacar del área de stage)
        nuevos archivos: .gitignore

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        MyCode.txt


git commit -m "Initial commit"
[master (commit-raíz) 79ea7ab] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

 
git status
En la rama master
Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        MyCode.txt

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)


Hago un commit para todos los ficheros
jose@jose:~/gitRepo$ git add .
jose@jose:~/gitRepo$ git status
En la rama master
Cambios a ser confirmados:
  (usa "git restore --staged <archivo>..." para sacar del área de stage)
        nuevos archivos: MyCode.txt


git commit -m "Add existing file"
[master f117e1f] Add existing file
 1 file changed, 1 insertion(+)
 create mode 100644 MyCode.txt

 git status
En la rama master
nada para hacer commit, el árbol de trabajo está limpio


git log
commit f117e1fb1e56abcf14313ceaf684172e39a970aa (HEAD -> master)
Author: jose <ejosera@gmail.com>
Date:   Sat Jul 19 22:25:42 2025 +0200

    Add existing file

commit 79ea7ab7cc3de714adcf1ba1f4c279985985e679
Author: jose <ejosera@gmail.com>
Date:   Sat Jul 19 22:18:23 2025 +0200

    Initial commit


### crear una rama
No se suele trabajar en main sino en una rama

git branch bug-FixFileNam

jose@jose:~/gitRepo$ git branch
  bug-FixFileNam
* master

Me cambio a la rama nueva
git checkout bug-FixFileNam 
Cambiado a rama 'bug-FixFileNam'
jose@jose:~/gitRepo$ git branch
* bug-FixFileNam
  master
jose@jose:~/gitRepo$ git status
En la rama bug-FixFileNam
nada para hacer commit, el árbol de trabajo está limpio

borro la ramma
git checkout master 
Cambiado a rama 'master'
jose@jose:~/gitRepo$ git branch -delete bug-FixFileNam   //-d si está syn con main -D si no está sync con main
error: ¿quisiste decir `--delete` (con dos guiones)?
jose@jose:~/gitRepo$ git branch --delete bug-FixFileNam 
Eliminada la rama bug-FixFileNam (era f117e1f).

Ahora creo una rama y voy a ella en un paso
git checkout -b feat-ChangeToMarkdown
Cambiado a nueva rama 'feat-ChangeToMarkdown'
jose@jose:~/gitRepo$ git status
En la rama feat-ChangeToMarkdown
nada para hacer commit, el árbol de trabajo está limpio

### añadir commit a master
Lo primero es hacer un merge desde la master
ose@jose:~/gitRepo$ git status
En la rama feat-ChangeToMarkdown
nada para hacer commit, el árbol de trabajo está limpio

jose@jose:~/gitRepo$ git merge master
Merge made by the 'ort' strategy.
 OtherCode.txt | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 OtherCode.txt

jose@jose:~/gitRepo$ git log
commit 1ab34213be3f66a1005dde0e621dbc834a2aa715 (HEAD -> feat-ChangeToMarkdown)
Merge: d4858c7 10905ac
Author: jose <ejosera@gmail.com>
Date:   Sun Jul 20 22:21:08 2025 +0200

    Merge branch 'master' into feat-ChangeToMarkdown // mensaje de merge

commit 10905ac6b78e4017e5cbad6df7dc95b8d277c684 (master)
Author: jose <ejosera@gmail.com>
Date:   Sun Jul 20 22:18:23 2025 +0200

    Add other code    // mensaje de commit de master
...................................................

y ahora actualizo la main desde la rama main

it checkout master 
Cambiado a rama 'master'
jose@jose:~/gitRepo$ git stats
git: 'stats' no es un comando de git. Mira 'git --help'.

El comando más similar es
        status
jose@jose:~/gitRepo$ git merge feat-ChangeToMarkdown 
Actualizando 10905ac..1ab3421
Fast-forward
 MyCode.md  | 8 ++++++++
 MyCode.txt | 1 -
 2 files changed, 8 insertions(+), 1 deletion(-)
 create mode 100644 MyCode.md
 delete mode 100644 MyCode.txt


git branch -d feat-ChangeToMarkdown 
Eliminada la rama feat-ChangeToMarkdown (era 1ab3421).


## github.com

## collaboration with git
### clono a repositorio
git clone https://github.com/jose-ramon-lopez/gitdemo.git

git status
En la rama main
Tu rama está actualizada con 'origin/main'.

nada para hacer commit, el árbol de trabajo está limpio

### creo código
touch 1.txt 2.txt



Tu rama está actualizada con 'origin/main'.

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        1.txt
        2.txt

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)

 git status
En la rama main
Tu rama está actualizada con 'origin/main'.

Cambios a ser confirmados:
  (usa "git restore --staged <archivo>..." para sacar del área de stage)
        nuevos archivos: 1.txt
        nuevos archivos: 2.txt


git commit -m "+1.txt y 2.txt"
[main 281df71] +1.txt y 2.txt
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1.txt
 create mode 100644 2.txt

 git status
En la rama main
Tu rama está adelantada a 'origin/main' por 1 commit.
  (usa "git push" para publicar tus commits locales)

nada para hacer commit, el árbol de trabajo está limpio
jose@jose:~/Documentos/Workspace/gitdemo$ 

// siempre un pull primero
git pull //la forma genérica es git pull local remote 
it pull
Ya está actualizado.


git push 
Enumerando objetos: 4, listo.
Contando objetos: 100% (4/4), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 304 bytes | 304.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
To https://github.com/jose-ramon-lopez/gitdemo.git
   918b703..281df71  main -> main
  

git status
En la rama main
Tu rama está actualizada con 'origin/main'.

nada para hacer commit, el árbol de trabajo está limpio

## Identify a Needed Change
Ejemplo de cambios en pequeña org

### crea un issue en github
### creo una rama
git status
En la rama main
Tu rama está actualizada con 'origin/main'.

nada para hacer commit, el árbol de trabajo está limpio
jose@jose:~/Documentos/Workspace/gitdemo$ git pull
Ya está actualizado.
jose@jose:~/Documentos/Workspace/gitdemo$ ls
1.txt  2.txt  README.md
jose@jose:~/Documentos/Workspace/gitdemo$ git checkout -b bug-1-update-readme
Cambiado a nueva rama 'bug-1-update-readme'

### fix code
git status
En la rama bug-1-update-readme
Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md

sin cambios agregados al commit (usa "git add" y/o "git commit -a")
jose@jose:~/Documentos/Workspace/gitdemo$ git add .
jose@jose:~/Documentos/Workspace/gitdemo$ git status 
En la rama bug-1-update-readme
Cambios a ser confirmados:
  (usa "git restore --staged <archivo>..." para sacar del área de stage)
        modificados:     README.md

// si pongo #1 githu hace un link al issue 1
jose@jose:~/Documentos/Workspace/gitdemo$ git commit -m "format readme file"
[bug-1-update-readme 0a97d1d] format readme file
 1 file changed, 2 insertions(+), 1 deletion(-)
jose@jose:~/Documentos/Workspace/gitdemo$ git status
En la rama bug-1-update-readme
nada para hacer commit, el árbol de trabajo está limpio

### merge main to branch to sync them
jose@jose:~/Documentos/Workspace/gitdemo$ git checkout main
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
jose@jose:~/Documentos/Workspace/gitdemo$ git pull
Ya está actualizado.
jose@jose:~/Documentos/Workspace/gitdemo$ git branch 
  bug-1-update-readme
* main
jose@jose:~/Documentos/Workspace/gitdemo$ git checkout bug-1-update-readme 
Cambiado a rama 'bug-1-update-readme'
jose@jose:~/Documentos/Workspace/gitdemo$ git merge main
Ya está actualizado.

### marge branch tomain
git merge bug-1-update-readme 
Actualizando 281df71..0a97d1d
Fast-forward
 README.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

 ### mando los cambios a git hub
git pull
gYa está actualizado.
jose@jose:~/Documentos/Workspace/gitdemo$ git push
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 264 bytes | 264.00 KiB/s, listo.
Total 3 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jose-ramon-lopez/gitdemo.git
   281df71..0a97d1d  main -> main

### borro la rama
git branch -d bug-1-update-readme 
Eliminada la rama bug-1-update-readme (era 0a97d1d).

### cierro el issue

## Working with Pull request
Hago un fork en github

clono mi fork a mi pc
it clone https://github.com/ejosera/gitdemo.git
Clonando en 'gitdemo'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 10 (delta 1), reused 6 (delta 1), pack-reused 0 (from 0)
Recibiendo objetos: 100% (10/10), 4.44 KiB | 1.11 MiB/s, listo.
Resolviendo deltas: 100% (1/1), listo.
jose@jose:~/Documentos/Workspace/gitdemoforked$ 

it status
En la rama main
Tu rama está actualizada con 'origin/main'.

nada para hacer commit, el árbol de trabajo está limpio

fix the issue
creo un branch

it status
En la rama main
Tu rama está actualizada con 'origin/main'.

nada para hacer commit, el árbol de trabajo está limpio

### pongo los cambios en mi repo forked
git add .
git commit -m "new readme2.txt"

### subo mi rama a mi rama en github
it push 
fatal: The current branch feat-2-update-readme has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feat-2-update-readme

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

// el mismo comando anterior es
// git push -u origin feat-2-update-readme

git add .
git commit -m "sdf"

git push --set-upstream origin feat-2-update-readme
Enumerando objetos: 4, listo.
Contando objetos: 100% (4/4), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 407 bytes | 407.00 KiB/s, listo.
Total 3 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'feat-2-update-readme' on GitHub by visiting:
remote:      https://github.com/ejosera/gitdemo/pull/new/feat-2-update-readme
remote: 
To https://github.com/ejosera/gitdemo.git
 * [new branch]      feat-2-update-readme -> feat-2-update-readme
rama 'feat-2-update-readme' configurada para rastrear 'origin/feat-2-update-readme'.

it status
En la rama feat-2-update-readme
Tu rama está actualizada con 'origin/feat-2-update-readme'.

nada para hacer commit, el árbol de trabajo está limpio


it status
En la rama feat-2-update-readme
Tu rama está actualizada con 'origin/feat-2-update-readme'.

nada para hacer commit, el árbol de trabajo está limpio

### Handle merge conficts
Hago cambios a la vez en 2 ramas

git branch
* main

cambio un fichero en main con 
git add .
git commit -m "sd"

git checkout -b conflict
Cambiado a nueva rama 'conflict'
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git branch
* conflict
  main

hago un cambio en esta rama 
git add .
git commit -m "sd"

llevo mis cambios a main y veo un conflicto
git merge main
Auto-fusionando README.md
CONFLICTO (contenido): Conflicto de fusión en README.md
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.

veo en el fichero "extra información"
<<<<<<< HEAD
# git conflict Repo
=======
# git demo main Repo
>>>>>>> main

Borro lo que no quiereoy dejo 
# git conflict Repo
borro incluso el carriage return

git status
En la rama conflict
Tienes rutas no fusionadas.
  (arregla los conflictos y ejecuta "git commit"
  (usa "git merge --abort" para abortar la fusion)

Rutas no fusionadas:
  (usa "git add <archivo>..." para marcar una resolución)
        modificados por ambos:  README.md

sin cambios agregados al commit (usa "git add" y/o "git commit -a")

git add .
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git status
En la rama conflict
Todos los conflictos resueltos pero sigues fusionando.
  (usa "git commit" para concluir la fusión)

Cambios a ser confirmados:
        modificados:     README.md


soluciono el conflicto con el commit

git commit -m "asf"
[conflict 634fc39] asf
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git status
En la rama conflict
nada para hacer commit, el árbol de trabajo está limpio

it checkout main
Cambiado a rama 'main'
Tu rama está adelantada a 'origin/main' por 1 commit.
  (usa "git push" para publicar tus commits locales)

git merge conflict 
Actualizando d2510c7..634fc39
Fast-forward
 README.md | 3 +--
 1 file changed, 1 insertion(+), 2 deletions(-)
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git status
En la rama main
Tu rama está adelantada a 'origin/main' por 3 commits.
  (usa "git push" para publicar tus commits locales)

nada para hacer commit, el árbol de trabajo está limpio
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git pull
Ya está actualizado.
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git push

### update el ultimo commit
vim README.md 
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git add .
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git commit -m "bad commit"
[main 273c791] bad commit
 1 file changed, 1 insertion(+), 1 deletion(-)

 git log
commit 273c791655012daad2719c035d9468241b46f166 (HEAD -> main)
Author: jose <ejosera@gmail.com>
Date:   Sat Jul 26 17:31:11 2025 +0200

    bad commit


solucione el problema
git add .
jose@jose:~/Documentos/Workspace/gitdemoforked/gitdemo$ git commit --amend -m "fixed"  // siempre antes del push
En la rama main
Tu rama está adelantada a 'origin/main' por 4 commits.
  (usa "git push" para publicar tus commits locales)

Sin cambios
Has solicitado enmendar tu commit más reciente, pero hacerlo lo
vaciaría. Puedes repetir el comando con --allow-empty, o puedes eliminar
el commit completamente con "git reset HEAD^".


### update a commit message
git commit --amend -m "udate"
En la rama main
Tu rama está adelantada a 'origin/main' por 4 commits.
  (usa "git push" para publicar tus commits locales)

Sin cambios
Has solicitado enmendar tu commit más reciente, pero hacerlo lo
vaciaría. Puedes repetir el comando con --allow-empty, o puedes eliminar
el commit completamente con "git reset HEAD^".

## otros comando
it reset --hard origin/main
HEAD está ahora en 0a97d1d format readme file
// levo atras el head hasta la última vez que sync con origen
HEAD está ahora en 273c791 bad commit

Recuperar cambios en unfichero
it checkout README.md
Actualizada 1 ruta desde el índice  

## openSource


## troubleshooting git

## git clients