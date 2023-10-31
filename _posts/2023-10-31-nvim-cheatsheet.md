---
layout: post
author: grim
categories: tech
permalink: nvim-cheatsheet.html
---

Lista de comandos usuales para nvim

---

#### [basics]

`e` : avanzar a la siguiente palabra

`u` : deshacer

`o` : insertar nueva linea

`r` : reemplazar un caracter

`cc` : eliminar una linea

`s` : elimina un caracter

`ctrl + r` : rehacer

`yy` : copiar una linea

`dd` : cortar una linea

`p` : pegar

---

#### [Visual-Mode]

`v` : modo visual

`shift + v` : modo visual línea

`ctrl + v` : modo visual bloque

`y` : copiar

`d` : cortar

`u` : cambiar a minúsculas

`U` : cambiar a mayúsculas

---

#### [Buffers]

`:e filename` -> editar un archivo o crearlo (Esto crea un nuevo buffer)

`:ls` -> Listar los buffers

`:bn` -> buffer siguiente

`:bp` -> buffer anterior

`:split` -> dividir en dos ventanas el área actual dentro del mismo buffer (Horizontal).

`:vsplit` -> dividir en dos ventanas el área actual dentro del mismo buffer (Vertical).

`Ctrl + w w` (ventana siguiente)

`:b number` -> muestra el buffer que corresponde al número.

`:bd` -> Borrar el buffer actual de forma segura.

`:bd!` -> Borrar el buffer actual descartando todos los cambios.

`:tabe example.txt` -> editar el archivo en una nueva pestaña.

`g t` -> pestaña siguiente

`g T` -> pestaña anterior

---

#### [Leaders & Plugins]

`leader = ','`

`CoCSearch = 's'`

`Files = 'f'`

`NERDTreeToggle = 'd'`

---


*[init.vim](https://github.com/juxxon23/nvim-configuration)*, Configuracion actual.


---

Última modificación: *31 October 2023*
