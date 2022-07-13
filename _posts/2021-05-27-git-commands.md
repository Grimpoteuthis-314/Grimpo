---
layout: post
author: grim
categories: tech
permalink: git-commands.html
---

Lista de comandos Git

---

#### [Default values]

`remote = origin`

---

#### [Config]

`git config --global user.name ""` : Configurar nombre del autor

`git config --global user.email ""` : Configurar correo del autor

`git config --global credential.helper cache` : Guardar creedenciales en cache (15 min)

`git clone [path | url]` : Clonar repositorio local o remoto

`git init` : inicializar repositorio local

---

#### [Basics]

`git add *` : Anadir al staging area

`git commit -m ""` : Guardar cambios en el repositorio local

`git commit -am ""` : Add y Commit

`git commit --amend` : Editar descripcion del commit realizado

`git remote add [remote] [url]` : Agregar repositorio remoto

`git remote -v` : lista de los repositorios remotos

`git push` : Enviar cambios al repositorio remoto

`git push [remote] [branch]` : Enviar cambios a la rama x del repositorio remoto

`git fetch` : Descarga el contenido del repositorio remoto pero no actualiza el repositorio local

`git merge` : Permite fusionar cambios

`git pull` : Fetch y Merge para los cambios del repositorio remoto

`git status` : Mostrar informacion

`git status -s` : Estado del archivo o directorio

`git log` : Historial de commits

`git log --oneline` : Resultados en una sola linea

`git reset --hard [id-commit]`: Regresar algun cambio (Se perderan los cambios realizados en commits posteriores al ingresado)

---

#### [Branches]

`git checkout -b` : Crear nueva rama y seleccionar dicha rama

`git checkout [branch]` : Cambiar de rama

`git branch` : Listar todas las ramas del repositorio

`git branch -d [branch]` : Eliminar rama

`git branch -r` : Listar remote/branch

`git branch -vv` : Listar ramas con informacion extras

`git push [remote] [branch]` : Enviar rama al repositorio remoto

`git push --all [remote]` : Enviar todas las ramas al repositorio remoto

`git push [remote] --delete [branch]` : Eliminar rama del repositorio remoto

---

#### [Extras]

`git tag [tag]` : Asignar tag a commit

`git push --tags [remote]` : Enviar todos los tags al repositorio remoto

---

Última modificación: *27 May 2021*
