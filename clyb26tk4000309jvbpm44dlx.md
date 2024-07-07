---
title: "Descubre el Número Más Grande: Un Algoritmo Sencillo y Eficaz"
seoTitle: "Descubre el Número Más Grande: Un Algoritmo Sencillo y Eficaz"
seoDescription: "Descubre cómo diseñar un algoritmo sencillo y eficaz para encontrar el número más grande entre tres valores dados. Aprende paso a paso con ejemplo práctico."
datePublished: Sun Jul 07 2024 04:34:10 GMT+0000 (Coordinated Universal Time)
cuid: clyb26tk4000309jvbpm44dlx
slug: descubre-el-numero-mas-grande-un-algoritmo-sencillo-y-eficaz
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/Wpnoqo2plFA/upload/aafcfa7ed20d5342269a24fc31e090d9.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

## Problema

Diseña un algoritmo que imprima el número más grande de tres números dados.

```plaintext
Ejemplo 1
Entrada: 1, 2, 3
Salida: 9
```

```plaintext
Ejemplo 2
Entrada: 10, 15, 8
Salida: 15
```

*Consejo: Antes de escribir código debes entender cómo se resuelve el problema. Piensa en cómo lo harías sin usar código. Realiza el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

Nos piden determinar cuál es el número más grande de tres números dados.

Pero, ¿qué pasa hay números iguales?

* Si los tres números son iguales, imprimir cualquiera.
    
* Si dos números son iguales, imprimir cualquiera que cumpla la condición de ser mayor que el tercer número.
    

## 2\. Diseño del algoritmo

### 1\. Idea de solución

La idea es simple, comparar los tres números entre sí para decidir el mayor.

### 2\. Diseño

Usamos variable `mayor` para guardar temporalmente el número más grande cada vez que hacemos una comparación. Al final, `mayor` tendrá el resultado.

```plaintext
A, B, C = 1, 2, 3
mayor = infinito negativo

si A >= mayor entonces
    mayor ← A
fin si
si B >= mayor entonces
    mayor ← B
fin si
si C >= mayor entonces
    mayor ← C
fin si

print(mayor)
```

### 3\. Comprobación en seco

| entrada | resultado |
| --- | --- |
| 1, 2, 3 | 3 |
| 10, 15, 8 | 15 |
| 4, 4, 4 | 4 |
| 4, 4, 5 | 5 |
| \-20, -5, -10 | \-5 |

## 3\. Codificación

```python
A, B, C = 1, 2, 3
mayor = -float('inf')

if A >= mayor:
    mayor = A
if B >= mayor:
    mayor = B
if C >= mayor:
    mayor = C

print(mayor)
```

Inicializamos `mayor` como infinito negativo. Esto representa el valor menor que puede tener un número en Python. Cualquier número diferente a infinito negativo es superior a este. Así podemos actualizar el valor de mayor en cada comparación.

Comparamos cada número contra la variable `mayor`. Actualizamos el valor de esta.

Al final, imprimimos `mayor`.

## 4\. Complejidad

Tiempo: O(1) constante

Por que no hay una colección que recorrer.

Espacio: O(1) constante

Por que no hay una estructura de datos adicional.

## Conclusión

En conclusión, hemos diseñado un algoritmo sencillo y eficaz para determinar el número más grande entre tres números dados. A través de un análisis detallado y un diseño claro, hemos demostrado cómo comparar los números y actualizar una variable para encontrar el mayor. La implementación en código es directa y eficiente, con una complejidad constante tanto en tiempo como en espacio. Este enfoque no solo resuelve el problema de manera efectiva, sino que también es fácil de entender y aplicar en diversas situaciones.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.