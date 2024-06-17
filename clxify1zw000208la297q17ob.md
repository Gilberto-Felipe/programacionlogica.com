---
title: "Saber si un año es bisiesto o no"
seoTitle: "Descubre si un Año es Bisiesto con Python"
seoDescription: "Descubre cómo determinar si un año es bisiesto con un algoritmo en Python. Aprende las reglas del calendario gregoriano. Analiza, diseña y codifica."
datePublished: Mon Jun 17 2024 03:53:57 GMT+0000 (Coordinated Universal Time)
cuid: clxify1zw000208la297q17ob
slug: saber-si-un-ano-es-bisiesto-o-no
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/GjAKNK4ocRc/upload/8f850611d658437c3b4d275bcda501b6.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

En este artículo, exploraremos, diseñaremos y codificaremos un algoritmo en Python para determinar si un año es bisiesto o no.

## Problema

Saber si un año dado es bisiesto o no.

```plaintext
Ejemplo 1
Entrada: 1000
Salida: false
```

```plaintext
Ejemplo 2
Entrada: 2000
Salida: true
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

El problema nos da un año y debemos definir si es una año bisiesto o no. La salida es true o false.

Un año es el tiempo que tarda la tierra en dar una vuelta al sol. Un año bisiesto es un año que tiene 366 días y no 365.

¿Cómo determinar si un año es bisiesto o no? Para entender mejor este tema, investiguemos qué nos dice Copilot de Microsoft Bing. Copilot nos dice que según el calendario gregoriano un año es bisiesto si cumple estas tres reglas:

1. Ser divisible por 4
    
2. No ser divisible por 100
    
3. Pero si es divisible por 100, debe ser divisible por 400.
    

## 2\. Diseño del algoritmo

### 1\. Idea de solución

La fórmula compacta que nos da Copilot es:

```plaintext
bisiesto = (año mod 4 = 0) Y (año mod 100 ≠ 0 O año mod 400 = 0)
```

Si el año es divisible entre 4 y no divisible entre 100, entonces es bisiesto. Pero ¿qué pasa con los años que son divisibles entre 100? Todavía pueden ser bisiestos si son divisibles entre 400.

`año mod 4 = 0`

si año es divisible entre 4

`(año mod 100 ≠ 0 O año mod 400 = 0)`

El operador lógico `O` maneja dos condiciones.

* Si no es divisible entre 100
    
* Si es divisible entre 400
    

Basta con que una sea verdadera para que la expresión sea verdadera.

El operador lógico `Y` une las dos partes de la fórmula. Ambas tienen que ser verdaderas para que la expresión sea verdadera.

### 2\. Diseño

Un primer acercamiento, siguiendo las reglas de los años bisiesto, sería:

```plaintext
bisiesto = false
si año es divisible por 4 entonces
    si año no es divisible por 100 entonces 
        bisiesto = true
    sino // si el año es divisible por 100
        si año es divisble por 400 entonces 
            bisiesto = true
fin si
imprimir(bisiesto)
```

Este pseudocódigo es entendible por sí solo, pero es verboso. La fórmula compacta nos dice lo mismo.

### 3\. Comprobación en seco

| year | result |
| --- | --- |
| 1000 | true Y (false O false) = true Y false = false |
| 2000 | true Y (false O true) = true Y true = true |
| 1600 | true Y (false O true) = true Y true = true |
| 1900 | true Y (false O false) = true Y false = false |
| 2024 | true Y (true O false) = true Y true = true |
| 2005 | false... |

## 3\. Codificación

Codificamos aquí solo la fórmula compacta. Pasa a código el pseudocódigo que presentamos arriba y pruébalo.

```python
year = int(input("Ingresa el año: "))
bisiesto = (year % 4 == 0) and (year % 100 != 0 or year % 400 == 0)
print(bisiesto)
```

## 4\. Complejidad

Tiempo: O(1) constante

Porque no recorremos una colección.

Espacio: O(1) constante

Porque no usamos estructura de datos extra.

## Conclusión

En conclusión, determinar si un año es bisiesto es una tarea sencilla cuando se conocen las reglas del calendario gregoriano. Presentamos dos algoritmos, uno más descriptivo en pseudocódigo; el otro, más compacto tipo fórmula. Además, explicamos cómo funciona una condición compuesta con los operadores lógicos `and` y `or`.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.