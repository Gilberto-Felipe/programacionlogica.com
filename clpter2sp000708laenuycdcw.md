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

Usar un condicional compuesto para resolver el problema. En la primera rama, evaluamos el caso feliz, donde a diferente de 0. En la segunda rama, evaluamos los casos donde la solución es imposible o indeterminada.

### 2\. Diseño

Observamos que no nos piden resolver paso a paso la ecuación. Luego, el despeje de `x` lo podemos hacer manualmente.

*Primer diseño*

*Pseudocódigo*

### 3\. Comprobación en seco

| a | b | resultado |
| --- | --- | --- |
| 0 | 3 | imposible: -3/0 |
| 0 | 0 | indeterminada: 0/0 |
| 2 | 4 | \-2 |

## 3\. Codificación

```python
def resolver_ecuacion(a, b):
    if a != 0:
        return -b / a
    elif a == 0 and b != 0:
        return "imposible"
    elif a == 0 and b == 0:
        return "indeterminada"

# Ejemplos de uso
print(resolver_ecuacion(0, 3))  # imposible
print(resolver_ecuacion(0, 0))  # indeterminada
print(resolver_ecuacion(2, 4))  # -2
```

## 4\. Complejidad

Tiempo: O(1) constante

No hay una colección de datos, es una entrada sola.

Espacio: O(1) constante

No hay una estructura de datos extra que ocupe espacio en memoria.

## Conclusión

Hemos analizado y resuelto una ecuación de primer grado considerando diferentes escenarios. La implementación en código refleja los casos posibles: solución única, solución imposible o solución indeterminada.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.