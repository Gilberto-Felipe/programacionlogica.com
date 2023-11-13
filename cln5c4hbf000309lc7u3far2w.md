---
title: "002. Problema: Calcular los primeros multiplos de un número"
seoTitle: "Calcular los primeros múltiplos de un número"
seoDescription: "El artículo resuelve paso a paso el problema Calcular los primeros múltiplos de un número. Guía por los pasos de analizar, diseñar el algoritmo y codificar."
datePublished: Sat Sep 30 2023 01:08:55 GMT+0000 (Coordinated Universal Time)
cuid: cln5c4hbf000309lc7u3far2w
slug: 002-problema-calcular-los-primeros-multiplos-de-un-numero
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cHhbULJbPwM/upload/fe9216fbfc3e2be2ba63fe0eea3a1b29.jpeg
tags: programacion, ejercicios

---

## Problema

Calcula los `x` primeros múltiplos de un número dado llamado `base`. `x` y `base` deben ser ingresados por teclado. Imprime el resultado.

```plaintext
Ejemplo 1
Entrada: x = 4, base = 4
Salida: 4, 8, 12, 16
```

```plaintext
Ejemplo 2
Entrada: x = 3, base = 5
Salida: 5, 10, 15
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">✏</div>
<div data-node-type="callout-text">Resuleve el problema solo. Escribe a mano o en tu editor de código tu solución. Compara tu solución con el artículo.</div>
</div>

## 1\. Análisis

* Los múltiplos son números que son se obtienen al mutiplicar un número por otro. En palabras simples, nos piden calcular la tabla de multiplicar de un número base, del 1 hasta el número x.
    
* Entrada son números enteros. Salida son números enteros.
    
* Asumimos que el cálculo incluye el número x, y que todas las entradas son válidas.
    

## 2\. Diseño del algoritmo

### 1\. Idea de solución

* Usar un ciclo para resolver el problema porque la solución es repetir una multiplicación.
    
* El problema no pide una estructura de datos.
    

### 2\. Diseño

*Primer diseño*

```plaintext
1. Pedir al usuario x y base
2. Multiplicar 1 x base
2. Multiplicar 2 x base...
x. Multiplicar x x base
```

*Refinamiento 1*

```plaintext
1. Pedir x
2. Pedir base
3. Multiplicar base * i
4. Escribir resultado
5. Repetir hasta que i sea igual o menor a x
```

*Refinamiento 2*

```plaintext
1. Pedir x
leer x
Convertir x a entero
Guardar valor entero en x
2. Pedir base
leer base
Convertir base a entero
Guardar valor entero en base
4. Escribir base * i
5. Repetir hasta que i sea igual o menor a x
```

Los datos que ingresa el usuario, aunque sean números, son de tipo cadena. Debemos convertirlos a enteros para manejarlos como tal. Esto lo hacemos con una función interna del lenguaje de programación a la que llamamos, arbitrariamente, ConvertirEntero().

Inicializamos `i` en 1, porque el problema comienza en 1.

*Pseudocódigo*

```plaintext
Algoritmo Obtner múltiplos
# variables
enteros: x, base, i ← 1

inicio
    escribir("Escribe el número de multiplos: ")
    x ← ConvertirEntero(leer(x))
    escribir("Escribe la base: ")
    base ← ConvertirEntero(leer(base))

    mientras i <= x hacer
        escribir(base * i)
        i++
    fin mientras
fin
```

### 3\. Comprobación en seco

Ejemplo 1

| i | salida |
| --- | --- |
| 1 | 4 \* 1 = 4 |
| 2 | 4 \* 2 = 8 |
| 3 | 4 \* 3 = 12 |
| 4 | 4 \* 4 = 16 |

El programa se comporta de la forma deseada.

## 3\. Codificación

He aquí la codificación en Python.

```python
# Programa Calcular los primeros x múltiplos

print("Escribe el número de múltiplos:", end=" ")
x = input()
x = int(x)

print("Escribe el número:", end=" ")
base = input()
base = int(base)

i = 1
while i <= x:
    print(base * i)
    i+=1
```

## 4\. Complejidad

Tiempo: O(n) -lineal- porque depende el número de múltiplos `x`.

Espacio: O(1) -constante- porque no se necesita una estructura de datos adicional.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.