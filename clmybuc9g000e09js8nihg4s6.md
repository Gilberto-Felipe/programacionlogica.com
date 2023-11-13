---
title: "¿Cómo resolver problemas de programación?"
seoTitle: "¿Cómo resolver problemas de programación? Un marco de trabajo."
seoDescription: "El artículo presenta un marco de trabajo para afrontar problemas de programación tipo LeetCode. Los pasos son: 1. Análisis, 2. Diseño, 3. Codificación."
datePublished: Mon Sep 25 2023 03:26:38 GMT+0000 (Coordinated Universal Time)
cuid: clmybuc9g000e09js8nihg4s6
slug: como-resolver-problemas-de-programacion
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/ieic5Tq8YMk/upload/a26cdef122a5c57237711dbdef17c8ab.jpeg
tags: programacion, diseno-de-algoritmos

---

## Resumen

En breve, este es el marco de trabajo:

1. Asegúrate de entender bien el problema.
    
2. Diseña el algoritmo
    
    1. Piensa en una idea que pueda resolverlo. Incluye una estructura de datos y una técnica que ayuden a la solución.
        
    2. Diseña el algoritmo. Desarrolla esa idea. Es un proceso de dividir el problema en problemas más simples. Luego, refina los pasos hasta tener pasos que se traduzcan en operacionese concretas. Los pasos deben estar completos.
        
    3. Ejecuta en seco el algortimo.
        
3. Codifica: Traduce a código el algoritmo, ejecútalo y comprueba el programa.
    

## Introducción

¿Cuántas veces vemos un problema de leetcode o de algún libro de fundamentos de programación y no sabemos cómo afrontarlo?

Cuando estudiaba en la universidad, acudí con un par de compañeros a algunas sesiones de *coding dojo* en una empresa de software de mi ciudad llamada Michelada.io. En estas sesiones se proponía un problema, había un tiempo de 30 minutos para resolverlo, al final se compartían las respuestas.

Uno de esos problemas fue convertir un número arábigo a número romano. Recuerdo que me quedé en blanco. No tenía ni idea de cómo comenzar. Mis amigos tuvieron éxito; otros no terminaron, pero tenían idea de cómo continuar.

Me sentí desanimado por este hecho. ¿Qué pasó? ¿Eso significaba que la programación no era para mí, o que debía renunciar a mi proyecto de ser ingeniero de software? Pues no.

No poder resolver un problema no significa que seamos tontos, o que no seamos aptos para programar. Significa que todavía no tenemos demasiada exposición a estos problemas, que necesitamos practicar para mejorar esta habilidad.

*Acotar el problema*

Estamos limitando los problemas a problemas de tipo LeetCode.

Generalmente, estos problemas se resuelven eligiendo las estructuras de datos apropiadas, diseñando un algoritmo y codificando la solución en tu lenguaje de programación favorito.

Es una realidad que los problemas de software reales son diferentes a estos ejercicios tipo LeetCode. Sin embargo, desde mi punto de vista, estos ejercicios ayudan a:

* Repasar estructuras de datos.
    
* Diseñar algoritmos.
    
* Apropiarnos de la sintaxis.
    
* Probar en seco un programa.
    
* Practicar para entrevistas técnicas.
    
* Aumentar la confianza en nuestras habilidades.
    

## Marco de trabajo

Este es el marco de trabajo:

1. Analizar el problema.
    
2. Diseñar el algoritmo.
    
3. Codificar.
    

Desarrollemos más estos tres pasos.

### 1 Analizar el problema

Aristóteles decía que un “error pequeño al inicio se convierte en un error mayor al final”. Si no entendemos el problema, sus partes y límites, no tiene sentido seguir adelante.

¿Qué analizamos aquí? Todo problema de programación se resume en tres partes:

* Entrada de datos.
    
* Procesamiento de esos datos.
    
* Salida de datos.
    

Debemos entender cuáles son los datos de entrada, cuál es el resultado esperado (porque con ese comprobaremos si nuestro cálculo es correcto) y qué procesamiento vamos a dar a los datos.

Adicionalmente, debemos pensar en los límites o restricciones que tenga el problema. Por ejemplo, ¿los datos son enteros o decimales? ¿Son positivos o negativos? ¿Existen casos límites que exijan una atención especial?

Por último, debemos confirmar nuestras suposiciones. Un enunciado del problema puede ser ambiguo, no explicitar todo lo que debería, o podemos entender una palabra con otro significado al del problema.

El análisis nos dice *qué* debemos hacer.

### 2 Diseñar el algoritmo

Programar es diseñar algoritmos para resolver un problema. Es la etapa creativa e intelectual y la más importante.

El algoritmo nos dice *cómo* se resuelve el problema.

Aterricemos unos pasos para diseñar el algoritmo:

1. Idea de solución.
    
2. Diseño y refinamiento de pasos.
    
3. Comprobación en seco.
    

*Idea de solución*

Después de entender el problema, debemos buscar un recurso, idea o técnica que ayude a resolverlo. Es una idea inicial, no está desarrollada.

La idea inlcuye una técnica de solución y, si es necesario, una estructura de datos.

Existen muchas formas de resolver un mismo problema, así que elige la idea que te parezca más fácil. Por ejemplo, para hallar el área de un triángulo hay varias fórmulas; pero la más común es (b x h) / 2.

¿De dónde sacamos esta idea? Puedes conocerla por aprendizaje o experiencia, deducirla por razonamiento, o pedir ayuda a chat GPT.

*Diseño y refinamiento de pasos*

Hasta ahora la idea es genérica y abstracta. Pero las computadoras entienden operaciones concretas. El problema no se resolverá si no hay instrucciones concretas y si no están completas.

1. Divide y vencerás: Divide el problema en problemas más simples.
    
2. Refina los pasos: Refina o itera sobre tu diseño hasta que tengas pasos concretos.
    

Escribe los pasos del algoritmo. Existen muchas formas de representar el algoritmo:

* Lenguaje natural.
    
* Pseudocódigo.
    
* Diagrama de flujo.
    
* Diagrama Nassi-Schneiderman.
    
* Fórmula matemática.
    

Elige una, la que más se te facilite. Yo prefiero el pseudocódigo.

*Ejecutar en seco*

Ejecutar en seco sirve para probar manualmente el flujo de tu algoritmo. Es decir, seguimos los valores de las variables en cada paso del algoritmo.

¿Cómo hacemos esto? Haz una tabla con los valores que toman las variables en cada paso del algoritmo. Compara el resultado final con la salida.

Esto es un ejemplo de un algoritmo que saca el promedio de las notas de estudiantes con las notas \[10,9,9,8,5\]. Salida = 8.2.

| i | suma | promedio |
| --- | --- | --- |
| 0 | 10 | 0 |
| 1 | 19 | 0 |
| 2 | 28 | 0 |
| 3 | 36 | 0 |
| 4 | 41 | 8.2 |

Al ejecutar el algoritmo en seco, comprobamos que el resultado es correcto.

### 3 Codificar

Codificar es el último paso de este marco de trabajo. Codificar es traducir a código el algoritmo diseñado.

1. Traduce el algoritmo. Revisa si tienes que ajustar el algoritmo a casos particulares del lenguaje de programación.
    
2. Ejecuta y comprueba el resultado. Si es el caso, depura el programa para corregir errores.
    
3. Analiza su complejidad de tiempo y espacio. Usamos la notación big O. Esto nos dice qué tan eficiente es un algoritmo.
    

## Conclusión

En este artículo expliqué un marco de trabajo para resolver problemas de programación tipo LeetCode.

Se resume en entender el problema, diseñar un algoritmo y codificarlo.

Programar es como redactar una novela. Codificar es como escribir (en el sentido de trazar letras o palabras) no te hace un escritor. Nuestro error es pensar que por saber sintaxis y conceptos de programación ya sabemos programar.

Sin embargo, programar es pensar en cómo resolver un problema usando herramientas computacionales. En otras palabras, es sobre todo diseñar algoritmos.

Un par consejos:

* Comienza practicando problemas fáciles, luego aumenta la dificultad.
    
* Comienza escribiendo a mano el diseño del algoritmo, o en el editor de código si no quieres hacerlo a mano. No lo dejes el diseño en aire, es decir, hacerlo sólo mentalmente. Escribir nos da claridad y nos facilita traducirlo a código.
    

En los siguientes artículos, resolveré problemas usando este marco de trabajo. Si te interesa, puedes suscribirte y seguirme. ¡Hasta la próxima!

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.

Stepwise refinement. (s/f-b). Cornell.edu. Recuperado el 18 de noviembre de 2022, de [Stepwise refinement\[1\]](https://www.cs.cornell.edu/courses/JavaAndDS/stepwise/stepwise.html)

Stepwise refinement. (s/f-a). Uct.ac.za. Recuperado el 18 de noviembre de 2022, de [Stepwise refinement\[2\]](https://www.cs.uct.ac.za/mit_notes/software/htmls/ch07s09.html)