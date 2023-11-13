---
title: "004. Problema: Determinar si en un conjunto de números naturales..."
seoTitle: "Algoritmo usa estructuras condicionales simple para resolver problema"
seoDescription: "Diseña un algoritmo para determinar si en un conjunto de números naturales se dan ciertas condiciones. Pone en práctica estructuras condicionales simples."
datePublished: Mon Nov 13 2023 00:08:33 GMT+0000 (Coordinated Universal Time)
cuid: clow5ccfw000109jo6h6cbslf
slug: 004-problema-determinar-si-en-un-conjunto-de-numeros-naturales
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cYRMl1HeuVo/upload/27e3cbef49568173d6d1f67bedaf624f.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

## Problema

Determina en un conjunto de 5 números naturales:

1. ¿Cuántos son menores de 15?
    
2. ¿Cuántos son mayores de 500?
    
3. ¿Cuántos están comprendidos entre 25 y 50?
    

```plaintext
Ejemplo 1
Entrada: 2,1000,500,20,800
Salida:
    menores 15: 1
    mayores 500: 2
    entre 25 y 50: 0
```

```plaintext
Ejemplo 2
Entrada: 300, 45, 1, 600, 10
Salida:
    menores 15: 2
    mayores 500: 1
    entre 25 y 50: 1
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema* a mano. *Piensa en cómo lo resuelves. Haz el algoritmo* paso a paso *en un papel o en el editor de código*.

## 1\. Análisis

Nos dan una lista de 10 números enteros naturales. El cálculo es contar cuántos elementos cumplen cada una de las condiciones.

En el rango entre 25 y 50, el 50 está incluído.

Suponemos que los elementos de la entrada son válidos.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Recorrer cada elemento de la lista y preguntar si se cumplen las condiciones.

### 2\. Diseño

*Primer diseño*

```plaintext
1. Preguntar si el número es menor a A
2. Preguntar si el número es mayor a B
3. Preguntar si el número está entre C y D
```

*Estructuras de decisión: condicionales*

Estas estructuras nos permiten condicionar qué va a pasar o no en el algoritmo. Si la condición se cumple, se ejecuta una acción. Las condicionales imitan la decisiones humanas. Con ellas añadimos inteligencia al algoritmo, una capacidad de decisión.

Las condiciones se resuelven en verdadero o falso.

Hay 3 tipos de condiciones:

* *Condicional simple*: Ejecuta una acción si la condición es verdadera.
    

```plaintext
si condición
    acción 1
fin si
```

* *Condicional doble o compuesta*: Ejecuta una acción si la condición es verdadera; otra ación, si es falsa.
    

```plaintext
si condición
    acción 1
si no 
    acción 2
fin si
```

* *Condicional múltiple*: Ejecuta diferentes acciones dependiendo de sus codiciones respectivas. Cada condición es una rama. El flujo se detiene cuando se cumple una condición; no se evalúan las restantes.
    

```plaintext
si condición 1
    acción 1
pero si condición 2
    acción 2
pero si condición 3
    acción 3
por defecto
    acción 4
fin si
```

En este problema tenemos 3 condicionales simples porque cada condición es independiente.

*Pseudocódigo*

```plaintext
# variables
lista ← [entrada]
enteros contadorA = 0 
        contadorB = 0
        contadorC = 0
        A = 15
        B = 500
        C = 25
        D = 50

inicio
    para cada elemento en lista hacer
        si elemento < A entonces
            contadorA++
        fin si
        si elemento > B entonces
            contadorB++
        fin si
        si elemento >= C Y elemento <= D entonces
            contadorC++
        fin si
    fin para cada

    escribir('Menores a {A}: {contadorA}')
    escribir('Mayores a {B}: {contadorB}')
    escribir('Entre {C} y {D}: {contadorc}')
fin
```

Agregamos flexibilidad al algoritmo al colocar en constantes los valores de las condiciones. Así, podemos cambiar esos valores y el programa seguirá funcionando.

### 3\. Comprobación en seco

| elemento | elemento &lt; 15 | elemento &gt; 500 | elemento &gt;= 25 Y elemento &lt;= 50 |
| --- | --- | --- | --- |
| 2 | contadorA = 1 |  |  |
| 1000 |  | contadorB = 1 |  |
| 500 |  |  |  |
| 20 |  |  |  |
| 800 |  | contadorB = 2 |  |

Comprueba el algoritmo con la segunda entrada del problema.

## 3\. Codificación

```python
# entrada 
lista = lista = [2,1000,500,20,800]
contador_a = 0
contador_b = 0
contador_c = 0
A = 15
B = 500
C = 25
D = 50

# cálculo
for elemento in lista:
    if elemento < A:
        contador_a += 1
    if elemento > B:
        contador_b += 1
    if elemento >= C and elemento <= D:
        contador_c += 1

# salida
print(f"Menores a {A}: {contador_a}")
print(f"Mayores a {B}: {contador_b}")
print(f"Entre {C} Y {D}: {contador_c}")
```

## 4\. Complejidad

Tiempo: O(n)

Es lineal porque recorre una vez la lista para realizar el cálculo.

Espacio: O(1)

Es constante porque no utiliza una estructura de datos extra.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.