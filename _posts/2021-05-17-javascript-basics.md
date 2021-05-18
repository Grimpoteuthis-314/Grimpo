---
layout: post
author: grim
categories: tech
permalink: javascript-basics.html
---

JavaScript fue creado en 1995 por Brendan Eich cuando era ingeniero en Netscape, se lanzó por primera vez en Netscape 2 a principios de 1996, ese mismo año resultó la primera edición estándar de ECMAScript; en 1999 se actualizó a la edición 3, la edición 5 de ECMAScript fue publicada en 2009 y la edición 6 fue publicada en junio de 2015.

El lenguaje JavaScript no posee el concepto de entrada o salida, está diseñado para ser ejecutado como lenguaje de scripting en un entorno hospedado y depende de los mecanismos que este disponga para comunicarse con el exterior, el entorno más común es el navegador pero no es el único que existe.

JavaScript es un lenguaje dinámico multiparadigma con tipos y operadores, objetos estándar integrados y métodos. Admite la programación orientada a objetos con prototipos de objetos, también admite programación funcional, las funciones se pueden almacenar en variables y ser pasadas como un objeto.

## Tipos de datos

1. **Números**
    Valores IEEE 754 de formato de 64 bits de doble precisión, por lo que no existen números enteros a excepción de `BigInt`. Un entero aparente resultaría ser un float aunque en la práctica, los valores enteros se tratarán como enteros de 32 bits.

    - Se admiten operadores estándar de aritmética, además existe un objeto incorporado llamado `Math` que proporciona funciones matemáticas avanzadas y constantes.

    - La función `parseInt(string, base)` permite convertir una cadena a número entero especificando su base, además se puede convertir a hexadecimal de la siguiente forma `parseInt('0x10')` y a octal anteponiendo el `0` en lugar del `0x` pero esto solo funciona en navegadores antiguos (2013 o menor).

    - En el caso de la función `parseFloat()`, este siempre usa base *10*.

    - Se puede convertir valores a números utilizando el operador unario `+`, ejemplo:
    `+ '42';` esto sería equivalente a `42`, `+ '0x10';` igual a 16.

    - Si la cadena no es numérica devuelve un valor especial `NaN` ("Not a Number").

    - Si `NaN` es utilizado como operando en una operación matemática el resultado será `NaN`.

    - Existe la función `isNaN()` para probar si un valor es `NaN`.

    - JavaScript también cuenta con los valores especiales `Infinity` e `-Infinity` y pueden ser probados con la función `isFinite()`, ejemplo: `1 / 0;` equivale a `Infinity`, `-1 / 0;` equivale a `-Infinity`; `isFinite(1/0);` equivale a `false`.

    - Las funciones `parseInt()` y `parseFloat()` analizan una cadena y devuelve hasta que alcancen un carácter no válido para el formato de número; el operador `'+'` al encontrar un carácter no válido devuelve `NaN`.

2. **Cadenas de texto**
3. **Booleanos**
4. **Objetos**
    - **Funciones**
    - **Array**
    - **Date**
    - **RegExp**
5. **null**
6. **undefined**
7. **Simbolos**

---
## **Fuentes**

- *[Reintroducción a JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/A_re-introduction_to_JavaScript)*, MDN Web Docs.

---

Última modificación: *17 May 2021*
