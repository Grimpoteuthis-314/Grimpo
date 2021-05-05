---
layout: post
author: grim
categories: tech
permalink: introduction-c.html
---
Este lenguaje de alto nivel fue desarrollado inicialmente en Bell Labs de AT&T por Dennish Ritchie entre 1969 y 1973, la justificación de este lenguaje se encuentra íntimamente ligada con el sistema operativo UNIX (escrito en ensamblador), ya que C pasaría a reescribir este sistema operativo.

## Conceptos Básicos

---

--- --- **Creación de un programa**

Es necesario definir superficialmente los siguientes conceptos:
Un compilador es un programa que se encarga de traducir el código fuente de un lenguaje a otro, para lograr su objetivo es necesario un trabajo en conjunto con otros programas.
Se describe el siguiente caso, el compilador recibe el **código fuente** de un lenguaje de alto nivel y lo traduce a otro de bajo nivel (código ensamblador o máquina), el resultado es llamado **objeto**.

--- **Proceso de Compilación C**

  - El archivo que contiene el código fuente escrito en C deberá poseer la extensión **\*.c**.

  - Preprocesador (Preprocessor): realizan tareas como la inclusión de ficheros, sustituciones de macros y eliminación de comentarios, produciendo la entrada para el compilador; el preprocesador genera un archivo con extensión **\*.i**.

  - Compilador: Este genera un archivo en lenguaje ensamblador con extensión **\*.s**.

  - Ensamblador (Assembler/Assembly): Genera el objeto que será utilizado por el linker con extensión **\*.o**.

  - Enlazador (Linker): Recibe el objeto (**.o**) generado y construye el objeto final enlazando las cabeceras (**.h**) y librerías (**.a**) esenciales para la ejecución del programa. El ejecutable tendrá la extensión **\*.out**.


![Compilation Process](assets/images/20210418/compilation_process.png){:width="60%"}

---

--- **Estructura general de programa en C**

1. Directivas del preprocesador, ejemplo:
    - #include \<xx.h\>, indica las cabeceras donde se encuentran identificadores, macros, constantes, variables globales, prototipos de funciones, entre otros.
    - #define, declarar identificadores de constantes o macros.

2. Declaracion de variables globales.

3. Declaracion de prototipos de funciones.

4. Funcion main.

5. Funciones de prototipos definidos.

**Ejemplo:**

- Se crea un programa basico con el siguiente nombre: `basic.c`

![C basic program](assets/images/20210418/Cbasis1.png)

- Se compila el codigo fuente, en este caso se especifica el nombre del ejecutable: `bas`

![gcc compilation](assets/images/20210418/Cbasis2.png)

- Se ejecuta el archivo generado.

![execution](assets/images/20210418/Cbasis3.png)

---

--- **Datos**

Las **constantes** Se refiere a valores fijos inalterables por el programa, se pueden
categorizar de la siguiente forma:

1. **Constantes Enteras:** Numeros con valores enteros, estos permiten su escritura en
tres sistemas numericos:
    - **Decimales:** Combinacion de digitos existentes en el conjunto de **0** a **9**, si consta
    de dos o mas digitos, el primero debe ser distinto de **cero**.
    - **Octal:**  Combinacion de digitos del conjunto **0** a **7**, el primer digito debe ser el **0**.
    - **Hexadecimal:** Combinacion de digitos del conjunto de **0** a **9** y de **a** a **f** (mayuscula o minuscula), debe comenzar con **0x** o **0X**.

2. **Constantes con punto flotante:** Numeros decimales con punto decimal y/o con exponente.

3. **Constantes de caracter:** Equivale a un solo caracter entre comillas simples, cada caracter tiene es equivalente a un numero entero descrito en el codigo ASCII.

4. **Constantes de cadenas de caracteres:** N numero de caracteres consecutivos entre
comillas dobles.

Las constantes se pueden declarar con el modificador `const` o utilizando la directiva
de compilacion `#define`.

![const](assets/images/20210418/const.png)

Al final de cada constante de cadena de caracteres el compilador inserta un caracter nulo, este puede ser representado con la secuencia de escape (`\0`), a partir
de esto podemos identificar que el caracter `'H'` es diferente de la cadena de caracteres `"H"`, ya que esta ultima posee el caracter nulo al final (`"H\0"`).






---
## **Fuentes**

- Fundamentos del sistema operativo UNIX, Jose M. Diaz - Rocio Muñoz, (2008).
- *[C Lenguaje de programación](https://es.wikipedia.org/wiki/C_(lenguaje_de_programaci%C3%B3n))*, Wikipedia.
- *[Preprocessor](https://en.wikipedia.org/wiki/Preprocessor)*, Wikipedia.

---

Ultima modificacion: *04 May 2021*
