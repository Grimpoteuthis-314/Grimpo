---
layout: post
author: grim
categories: tech
permalink: introduction-c.html
---
Este lenguaje de alto nivel fue desarrollado inicialmente en Bell Labs de AT&T por Dennish Ritchie entre 1969 y 1973, la justificación de este lenguaje se encuentra íntimamente ligada con el sistema operativo UNIX (escrito en ensamblador), ya que C pasaría a reescribir este sistema operativo.

## Conceptos Básicos

--- --- **Creación de un programa** --- ---

Es necesario definir superficialmente los siguientes conceptos:
Un compilador es un programa que se encarga de traducir el código fuente de un lenguaje a otro, para lograr su objetivo es necesario un trabajo en conjunto con otros programas.
Se describe el siguiente caso, el compilador recibe el **código fuente** de un lenguaje de alto nivel y lo traduce a otro de bajo nivel (código ensamblador o máquina), el resultado es llamado **objeto**.

--- **Proceso de Compilación C**

- El archivo que contiene el código fuente escrito en C deberá poseer la extensión **\*.c**.

- Preprocesador (Preprocessor): realizan tareas como la inclusión de ficheros, sustituciones de macros y eliminación de comentarios, produciendo la entrada para el compilador; el preprocesador genera un archivo con extensión **\*.i**.

- Compilador: Este genera un archivo en lenguaje ensamblador con extensión **\*.s**.

- Ensamblador (Assembler/Assembly): Genera el objeto que será utilizado por el linker con extensión **\*.o**.

- Enlazador (Linker): Recibe el objeto (**.o**) generado y construye el objeto final enlazando las cabeceras (**.h**) y librerías (**.a**) esenciales para la ejecución del programa. El ejecutable tendrá la extensión **\*.out**.

--- **Estructura de programa en C**


**Fuentes**

- Fundamentos del sistema operativo UNIX, Jose M. Diaz - Rocio Muñoz, (2008).
- [C Lenguaje de programación](https://es.wikipedia.org/wiki/C_(lenguaje_de_programaci%C3%B3n)), Wikipedia.
- [Preprocessor](https://en.wikipedia.org/wiki/Preprocessor), Wikipedia.
