---
title: "006. Problema: Resolver ecuación de primer grado"
seoTitle: "Algoritmo para resolver ecuación de primer grado"
seoDescription: "Diseña un algoritmo para resolver una ecuación de primer grado de la forma ax+b=0. Explica los casos que pueden existir usando  el condicional compuesto."
datePublished: Wed Dec 06 2023 06:48:21 GMT+0000 (Coordinated Universal Time)
cuid: clpter2sp000708laenuycdcw
slug: 006-problema-resolver-ecuacion-de-primer-grado
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/05A-kdOH6Hw/upload/bb6e50643419160656fa2cb2d3462510.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

## Problema

Resuelve la ecuación de primer grado con los datos de entrada. Escribe el resultado, o si el resultado es indeterminado o imposible.

$$ax + b = 0$$

```plaintext
Ejemplo 1
Entrada: a=0, b=3
Salida: indeterminada
```

```plaintext
Ejemplo 2
Entrada: a=0, b=0
Salida: imposible
```

```plaintext
Ejemplo 3
Entrada: a=2, b=4
Salida: x = -b/a => -2
```

*Consejo: Antes de escribir código debemos saber cómo se resuelve el problema. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

Nos piden resolver una ecuación de primer grado. Los valores conocidos -entrada- son a, b. Para resolver la ecuación tenemos que saber qué es y cómo se resuelven. De lo contrario, estamos atorados. Repasemos.

*Ecuación de primer grado*

* Una ecuación de primer grado es una igualdad matemática que tiene una o más incógnitas.
    
* El grado de la ecuación lo recibe de la potencia a la que está elevada la incógnita. Por ejemplo, `x^2` es una ecuación de segundo grado.
    
* El grado nos dice el número de soluciones que tiene la ecuación. Una ecuación de primer grado solo tiene una solución.
    

La ecuación que nos pasan tiene la forma de `a * x + b = 0`. El cálculo consiste en:

1. Agrupar los términos que llevan x en la primera parte de la ecuación (antes del signo `=`). Los que no, los pasamos a la segunda parte.
    
2. Despejar x.
    
3. Resolver la operación.
    

> Recuerda que si pasamos un término de un lado a otro de la ecuación, se realizan operaciones opuestas. Si suman, pasan restando. Si multiplican, pasan dividiendo.

Con eso resolvemos la ecuación. Pero, la solución puede caer en tres casos o escenarios diferentes. Los casos son:

* Si a es diferente de 0, resolvemos la operación.
    
* Si a = 0 y b diferente de 0, la solución es imposible.
    
* Si a = 0 y b = 0, la solución es indeterminada.
    

El 0 es problemático porque la ecuación despejada termina siendo `0/0`, o `-b/0`.

Este problema nos da los casos o escenarios en los que puede caer el programa. En muchas ocasiones, estos casos no vienen dados. Debemos pensar en ellos y encontrarlos.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Usar un codicional compuesto para resolver el problema. En la primera rama, evaluamos el caso feliz, donde a diferente de 0. En la segunda rama, evaluamos los casos donde la solución es imposible o indeterminada.

### 2\. Diseño

Observamos que no nos piden resolver paso a paso la ecuación. Luego, el despeje de `x` lo podemos hacer manualmente.

```plaintext
1. a*x+b = 0
2. a*x = 0-b
3. x = -b/a
```

*Primer diseño*

```plaintext
1. Si a <> 0, resolver y escribir resultado.
2. Si a = 0 y b <> 0, escribir imposible.
3. Si a = 0 y b = 0, escribir indeterminada.
```

*Pseudocódigo*

```plaintext
variables
    real a, b, x

inicio
    si a <> 0, entonces
        x ← -b/a
        escribir(x)
    si no, entonces
        si b <> 0, entonces
            escribir(Solución imposible)
        si no, entonces
            escribir(Solución indeterminada)
        fin si
    fin si
fin
```

### 3\. Comprobación en seco

| a | b | resultado |
| --- | --- | --- |
| 0 | 3 | imposible: -3/0 |
| 0 | 0 | indeterminada: 0/0 |
| 2 | 4 | \-2 |

## 3\. Codificación

```python
# Programa Ecuación de primer grado 
# variables
a = 0
b = 0

# inicio
if a != 0:
    x = -b / a
    print(x)
else:
    if b != 0:
        print("Solución imposible")
    else:
        print("Solución indeterminada")
# fin
```

## 4\. Complejidad

Tiempo: O(1) constante

No hay una colección de datos, es una entrada sola.

Espacio: O(1) constante

No hay una estructura de datos extra que ocupe espacio en memoria.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.