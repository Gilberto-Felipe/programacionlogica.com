---
title: "005. Problema: Determinar si un número es decimal"
seoTitle: "Algoritmo que determina si un número es par o impar usando Truncate"
seoDescription: "Diseña un algoritmo para determinar si un número es decimal usando la función Truncate. Además, explica cómo refactorizar para evitar el bloque else."
datePublished: Tue Nov 14 2023 02:43:56 GMT+0000 (Coordinated Universal Time)
cuid: cloxqc0kp000208l61ifmdmm0
slug: 005-problema-determinar-si-un-numero-es-decimal
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/4ApmfdVo32Q/upload/2786dbf3bb4881fa7ac6a674919c0c0b.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

## Problema

Determina si un número es decimal. Pide al usuario un número. Devuelve verdadero si es decimal; de lo contrario, devuelve falso.

```plaintext
Ejemplo 1
Entrada: 3.1416
Salida: true
```

```plaintext
Ejemplo 2
Entrada: 80
Salida: false
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema a mano. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego, compara con el artículo.*

## 1\. Análisis

Debemos pedir un número al usuario, luego calcular si es decimal o no y devolver verdadero o falso según el caso.

Suponemos que la entrada de dato es correcta.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Se me ocurren dos ideas de solución.

1. Comparar el número contra el número truncado a la parte entera. Si son iguales, es entero; de lo contrario, decimal.
    
2. Usar el operador módulo con 1. Si el resultado es diferente de 0, entonces es decimal.
    

Elegí la primera porque trabajamos con el operador módulo en el problema anterior.

### 2\. Diseño

*Primer diseño*

```plaintext
1. Leer el número
2. Calcular si es decimal
3. Escribir el resultado
```

*Refinamiento*

```plaintext
1. Pedir el número
2. Leer el número
3. Truncar el número
4. Comparar el número contra el número truncado
5. Escribir el resultado
```

*¿Cómo truncar un número?*

Truncar un número es reducir el número de dígitos decimales.

La mayoría de lenguajes de programación tienen incorporada esta tarea. Suele llamarse `Truncar()`.

Las tareas que vienen implementadas por el lenguaje se llaman *funciones internas*. Nos facilitan la vida porque no tenemos que desarrollarlas.

*Pseudocódigo*

```plaintext
# variables
real: numero
cadena: entrada

inicio
    escribir("Ingresa un número (decimal o entero): ")
    leer(entrada)
    // convertir número a decimal
    si numero <> Truncar(numero)
        escribir(true)
    si no
        escribir(false)
    fin si
fin
```

Observa que en lugar de escribir una condición compuesta

```plaintext
si numero <> Truncar(numero)
    escribir(true)
si no
    escribir(false)
fin si
```

podemos mejorar nuestro código usando este patrón para ahorrarnos el `si no [else]`

```plaintext
esDecimal ← false
si numero <> Truncar(numero)
    esDecimal ← true
fin si

escribir(esDecimal)
```

Pasos

1. Declaramos una variable con el estado/acción que tendría el bloque `si no`: `esDecimal ← false`.
    
2. Eliminamos el bloque `si no`.
    
3. Dentro del bloque `si`, actualizamos el valor de `esDecimal` al estado que le corresponde: `esDecimal ← true`.
    

El código es más compacto y legible. Además, separamos la salida del cálculo; la función `escribir()` quedó fuera del bloque `si`.

*Refactorizar*

Lo que acabamos de hacer se llama *refactorizar*. Refactorizar es reesctructurar el código sin cambiar su comportamiento. Esto sirve para mejorar la calidad, legibilidad y mantenibilidad del código.

Siempre que puedas, refactoriza tu código. Es una excelente práctica para mejorar. Casi siempre podemos encontrar elementos defectuosos, repetidos o innecesarios.

Al final, no te olvides de comprobar que el programa funciona. Recuerda que el mejor algoritmo o programa es el que funciona; no el que se ve más bonito.

> Refactorizar es reesctructurar el código sin cambiar su comportamiento.

### 3\. Comprobación en seco

| numero | Truncar(numero) | esDecimal |
| --- | --- | --- |
| 3.14 | 3 | verdadero |
| 5 | 5 | falso |

## 3\. Codificación

En ocasiones hay que modificar el algoritmo para traducirlo al lenguaje de programación.

*Convertir entrada a tipo numérico*

En este caso, tenemos que hacer un paso extra, convertir la entrada del usuario a un tipo numérico. ¿Por qué? Porque, por defecto, las entradas de usuario son de tipo cadena, aunque sean números.

*Tipos de datos numéricos*

Hay lenguajes que tienen diferentes tipos de datos numéricos dependiendo de si son decimales o enteros, y de la longitud de datos que pueden guardar.

```python
entrada = input("Ingresa un número -decimal o entero-: ")
numero = float(entrada)

esDecimal = False
if numero != int(numero):
    esDecimal = True

print(esDecimal)
```

Comentarios:

* La funcion `input()` sirve para leer una entrada de usuario. Puede recibir como argumento un mensaje para el usuario que se imprime en consola.
    
* La función `float()` convierte una cadena o número entero a número decimal.
    
* Convertimos la entrada a `float` para no perder datos. Si convertimos la entrada a entero, y el usuario ingresó un número decimal, perderíamos datos.
    
* La funcion `int()` convierte una cadena a entero. Sirve también para truncar la parte decimal de un número.
    
* En lugar de `int()`, también se puede usar la función `math.trunc()`.
    

## 4\. Complejidad

Tiempo: O(1) constante

No hay una colección de datos, es una entrada sola.

Espacio: O(1) constante

No hay una estructura de datos extra que ocupe espacio en memoria.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.