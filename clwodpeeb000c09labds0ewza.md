---
title: "Detectar si un número es decimal o entero"
seoTitle: "Detectar si un número es decimal o entero"
seoDescription: "Descubre cómo identificar si un número es decimal o entero utilizando Python. Ejercita la lógica de programación. "
datePublished: Mon May 27 2024 02:58:09 GMT+0000 (Coordinated Universal Time)
cuid: clwodpeeb000c09labds0ewza
slug: detectar-si-un-numero-es-decimal-o-entero
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/gdL-UZfnD3I/upload/c37db16b2e8b322455c0aefcf49aadcf.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

En este artículo, exploraremos, diseñaremos y codificaremos en Python un algoritmo para determinar si un número posee una parte decimal o si es un número entero.

## Problema

Detecta si un número dado es decimal o entero.

```plaintext
Ejemplo 1
Entrada: 4
Salida: entero
```

```plaintext
Ejemplo 2
Entrada: 3.1416
Salida: decimal
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

Nos piden detectar si un número dado es decimal o entero.

Los números enteros incluyen los números naturales, sus opuestos negativos, y el cero. Es decir, números positivos, negativos y el cero. Por ejemplo, 1, -1, 0.

Los números decimales constan de una parte entera y de una fracción decimal. La parte entera y decimal se separa por una convención que puede ser un punto o una coma dependiendo del país. Entonces, un número decimal sería 1.5.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Se me ocurren tres ideas de solución.

A. Preguntar si el número contiene un punto o una coma, puesto que estos son los separadores de la parte entera de la parte decimal.

B. Truncar el número a la parte entera y preguntar si el número es igual al número truncado. Si es igual, es entero. Si es diferente, es decimal.

C. Usar el operador módulo para saber si el número tiene residuo. Si tiene residuo es decimal, de lo contrario, es entero.

Elegimos la opción B.

### 2\. Diseño

```plaintext
1. Comparar el número contra el número truncado
    1.1 Si es igual entonces es entero,
    1.2 De lo contrario, es decimal
2. Guardar resultado
3. Imprimir resultado
```

### 3\. Comprobación en seco

| Entrada | Comparación | Resultado |
| --- | --- | --- |
| 4 | 4 = 4 | entero |
| 3.1416 | 3.1416 = 3 | decimal |

## 3\. Codificación

Casi todos los lenguajes poseen ya una función para truncar un número. Solo tenemos que utilizarla. En el caso de Python hay varias opciones. Un par de ellas son:

* usar `int()`. Esto convierte el número a entero.
    
* usar `math.trunc()` de la librería `math`
    

```python
numero = 3.1416
if numero == int(numero):
    resultado = "entero"
else:
    resultado = "decimal"
print(resultado)
```

## 4\. Complejidad

Tiempo: O(1) constante

Es constante porque no hay una colección que recorrer.

Espacio: O(1) constante

Es constante porque no hay una estructura de datos adicional.

## Conclusión

En resumen, en este artículo analizamos y diseñamos un algoritmo para determinar si un número es entero o decimal. Tuvimos tres ideas de solución y seleccionamos una para desarrollar: comparar el número dado contra el número truncado. Aprendimos que para truncar un número en Python podemos usar el método `int()`. ¿Conoces otras formas de resolver este problema? ¡Coméntalas!

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.