# To git or not to git

## Git Source Control
Se usa para:
- Colaboración
- Versiones
<br><br/>


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

## github.com

## collaboration with git

## openSource

## troubleshooting git

## git clients