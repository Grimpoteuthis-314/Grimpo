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

- Se crea un programa básico con el siguiente nombre: `basic.c`

![C basic program](assets/images/20210418/Cbasis1.png)

- Se compila el codigo fuente, en este caso se específica el nombre del ejecutable: `bas`

![gcc compilation](assets/images/20210418/Cbasis2.png)

- Se ejecuta el archivo generado.

![execution](assets/images/20210418/Cbasis3.png)

---

--- **Datos**

Las **constantes** se refieren a valores fijos e inalterables por el programa, se pueden
categorizar de la siguiente forma:

1. **Constantes Enteras:** Números con valores enteros, estos permiten su escritura en
tres sistemas numéricos:
    - **Decimales:** Combinación de dígitos existentes en el conjunto de **0** a **9**, si consta
    de dos o más dígitos, el primero debe ser distinto de **cero**.
    - **Octal:**  Combinación de dígitos del conjunto **0** a **7**, el primer dígito debe ser el **0**.
    - **Hexadecimal:** Combinación de dígitos del conjunto de **0** a **9** y de **a** a **f** (mayuscula o minuscula), debe comenzar con **0x** o **0X**.

2. **Constantes con punto flotante:** Números decimales con punto decimal y/o con exponente.

3. **Constantes de carácter:** Equivale a un solo carácter entre comillas simples, cada carácter es equivalente a un número entero descrito en el código ASCII.

4. **Constantes de cadenas de caracteres:** N número de caracteres consecutivos entre
comillas dobles.

Las constantes se pueden declarar con el modificador `const` o utilizando la directiva
de compilación `#define`.

![const](assets/images/20210418/const.png)

Al final de cada constante de cadena de caracteres el compilador inserta un caracter nulo, este puede ser representado con la secuencia de escape (`\0`), a partir
de esto podemos identificar que el carácter `'H'` es diferente de la cadena de caracteres `"H"`, ya que esta última posee el carácter nulo al final (`"H\0"`).

---

**Variables**

Estas se declaran de la siguiente forma: `tipo_dato nombre_variable;`

Se inicializan asignando un valor que corresponda al tipo de dato: `tipo_dato nombre_variable = valor;`.

**Tipos de datos**

Los tipos fundamentales que el lenguaje *C* ofrece se encuentran clasificados de la siguiente forma:
1. **Tipos enteros:** Estos son utilizados para representar subconjuntos de números naturales y enteros.
    - **`char`:** Número entero de 8 bits, rango [-128, 127]. También es utilizado para representar caracteres de acuerdo al código ASCII.
    - **`int`:** Número entero de 16 o 32 bits (depende del procesador).

    ![Integer Data Types](assets/images/20210418/TiposDatosEnteros.png)

    ![Integer Data Types Execution](assets/images/20210418/TiposDatosEnterosEx.png)

2. **Tipos reales:** Permiten representar subconjuntos de números racionales.
    - **`float`:** Número con punto flotante, el tamaño es de 32 bits o 4 bytes.
    - **`double`:** Número con punto flotante, el tamaño es de 64 bits o 8 bytes.

    ![real Data Types](assets/images/20210418/TiposDatosReales.png)

    ![real Data Types Execution](assets/images/20210418/TiposDatosRealesEx.png)

3. **Tipo `void`:** Es empleado para declarar la ausencia de valores en el retorno de una función o para declarar punteros genéricos.

    ![void](assets/images/20210418/void.png)

---

**Modificadores**
Los modificadores permiten cambiar el tamaño de los tipos de datos numéricos.
- **`unsigned`:** Representa números naturales (Mayor o igual a cero).
- **`signed`:** Representa tanto números positivos como negativos, comportamiento por defecto.
- **`long`:** Permite ampliar el tamaño en bits.
- **`short`:** Indica un tamaño de bits menor.

![Bytes Sizes Data Types](assets/images/20210418/bytesSize.png)

![Bytes Sizes Data Types Execution](assets/images/20210418/bytesSizeEx.png)

---
## **Fuentes**

- Fundamentos del sistema operativo UNIX, Jose M. Diaz - Rocio Muñoz, (2008).
- *[C Lenguaje de programación](https://es.wikipedia.org/wiki/C_(lenguaje_de_programaci%C3%B3n))*, Wikipedia.
- *[Preprocessor](https://en.wikipedia.org/wiki/Preprocessor)*, Wikipedia.
- *[Lenguaje C](https://informatica.uv.es/estguia/ATD/apuntes/laboratorio/Lenguaje-C.pdf)*, Enrique Vicente Bonet Esteban.

---

Última modificación: *08 May 2021*
