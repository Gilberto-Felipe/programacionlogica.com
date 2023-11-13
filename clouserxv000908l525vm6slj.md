---
title: "003. Problema: Cálculo con pares e impares"
seoTitle: "Algoritmo calcular pares, impares y promedio."
seoDescription: "Algoritmo calcular pares, impares y promedio. El artículo enseña cómo diseñar un algoritmo paso a paso. Explica patrones y operaciones implicadas."
datePublished: Sun Nov 12 2023 01:18:46 GMT+0000 (Coordinated Universal Time)
cuid: clouserxv000908l525vm6slj
slug: 003-problema-calculo-con-pares-e-impares
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/JhevWHCbVyw/upload/f4fa974e6f6aeff0e416c741a8a7222b.jpeg
tags: programacion, algortimos, nivel-basico

---

## Problema

Dados 10 números enteros:

1. Imprime la suma de los números pares.
    
2. Imprime cuántos números pares hay.
    
3. Imprime el promedio de los números impares.
    

```plaintext
Ejemplo 1
Entrada: 1,2,3,4,5,6,7,8,9,10
Salida: 
    suma pares: 30
    números pares: 5
    promedio impares: 5
```

```plaintext
Ejemplo 2
Entrada: 11,12,13,14,15,16,17,18,19,20
Salida:
    suma pares: 80
    números pares: 5
    promedio impares: 15
```

*Consejo*

Antes de escribir código debes saber cómo se resuelve el problema a mano. Piensa en cómo lo resuelves. Haz el plan o algoritmo en un papel o en el editor de código.

## 1\. Análisis

Nos dan una lista de 10 números. Debemos hacer los 3 cálculos solicitados: suma de los pares, número de pares y promedio de los impares.

Suponemos que son naturales y que todos los elementos de la entrada son válidos.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Recorrer la lista y hacer los cálculos correspondientes.

### 2\. Diseño

*Primer diseño*

```plaintext
1. Calcular suma de pares
2. Calcular número de pares
3. Calcular el promedio de los impares
```

*Refinamiento*

```plaintext
1. si par, entonces
2. guardar valor en un acumulador
3. aumentar el contador de pares
4. si impar, entonces
5. guardar valor en un acumulador
6. aumentar el contador de impares
7. repetir por cada elemento de la lista
8. calcular promedio
9. imprimir resultado: 
    suma pares, 
    cantidad pares, 
    promedio impares
```

En este problema, necesitamos saber calcular 3 cosas:

* ¿Cómo calcular el promedio?
    
* ¿Cómo calcular si un número es par?
    
* ¿Cómo guardar valores acumulativamente en una variable?
    

*Calcular el promedio*

El promedio es la suma de los elementos de un conjunto dividido entre el número de ellos.

```plaintext
(1+2+3+4+5+6+7+8+9+10) / 10
```

*Calcular si un número es par con el operador módulo*

El operardor módulo o resto es una operación que devuelve el resto de la división entre dos números. En otras palabras, es lo que sobra en la división cuando no es exacta. Por ejemplo, el resto de 5 / 2 es 1.

* División entera de 5 / 2 = 2
    
* Módulo o resto de 5 / 2 = 1
    

El operador módulo se suele usar para

* verificar si un número es divisible entre otro
    
* obtener el último dígito de un número decimal
    

Representamos el operador módulo con `mod` o el símbolo `%`.

¿Cómo sabemos si un número es par? Aquí hacemos dos operaciones.

* Primero, calculamos el módulo `1 % 2`.
    
* Luego, comparamos si el resultado es igual a 0.
    

Expresamos las dos operaciones de forma abreviada así: `1 % 2 == 0`.

```python
1 % 2     #  1
1 == 0    # falso
```

1 módulo 2 es 1. 1 no es igual a 0. Por lo tanto, 1 no es par.

```python
2 % 2     # 0
0 == 0    # verdadero
```

2 módulo 2 es 0. 0 es igual a 0. Por lo tanto, 2 es par.

*Variable acumuladora*

Una variable acumuladora sirve para almacenar y actualizar valores. La diferencia con una variable normal es que agrega un nuevo valor al que ya tiene.

Generalmente, usamos las variables acumuladoras dentro de ciclos. Cada iteración del ciclo acumula un nuevo valor.

*Patron de código de variable acumuladora*

> nombre ← valor inicial + valor actual

El valor inicial suele ser 0 porque es un valor neutro.

Aquí utilizamos un par de variables acumuladoras; una para guardar la suma de los elementos pares, otra la de los impares.

*Pseudocódigo*

```plaintext
# variables
lista [entrada]
entero 
    SumaPares ← 0, SumaImpares ← 0, 
    ContadorPares ← 0, ContadorImpares ← 0

inicio
    por cada elemento en lista
        si elemento == par entonces (elemnto % 2 == 0)
            SumaPares ← SumaPares + elemento
            ContadorPares++
        fin si
        si no 
            SumaImpares ← SumaImpares + elemento
            ContadorImpares++
        fin si no
    fin por cada
    escribir('suma pares:', SumaPares)
    escribir('número pares:', ContadorPares)
    escribir('promedio impares:',SumaImpares/ContadorImpares)
fin
```

### 3\. Comprobación en seco

| i | SumaPares | ContadorPares | SumaImpares | ContadorImpares |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 1 | 1 |
| 1 | 2 | 1 |  |  |
| 2 |  |  | 4 | 2 |
| ... |  |  |  |  |
| 9 | 30 | 5 | 25 | 5 |

Comprueba el algoritmo con la segunda entrada del problema.

## 3\. Codificación

```python
# entrada
lista = [1,2,3,4,5,6,7,8,9,10]

sumaPares = 0
sumaImpares = 0
contadorPares = 0
contadorImpares = 0
promedioImpares = 0

# cálculo
for elemento in lista:
    if elemento % 2 == 0:
      sumaPares = sumaPares + elemento
      contadorPares+=1
    else:
      sumaImpares = sumaImpares + elemento
      contadorImpares+=1

promedioImpares = sumaImpares/contadorImpares

# salida
print("Suma pares> ", sumaPares)
print("Cantidad pares> ", contadorPares)
print("Promedio impares> ", promedioImpares)
```

## 4\. Complejidad

Tiempo: O(n)

Es lineal porque recorre una vez la lista para realizar el cálculo.

Espacio: O(1) constante

Es constante porque no utiliza una estructura de datos extra.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.