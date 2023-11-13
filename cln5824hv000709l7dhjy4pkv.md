---
title: "001. Problema: Obtener el promedio de una lista de calificaciones"
seoTitle: "Problema obtener promedio"
seoDescription: "El artículo muestra una posible solución al problema de obtener el promedio de una lista de calificaciones. Explica paso a paso cómo resolverlo."
datePublished: Fri Sep 29 2023 23:15:06 GMT+0000 (Coordinated Universal Time)
cuid: cln5824hv000709l7dhjy4pkv
slug: 001-problema-obtener-el-promedio-de-una-lista-de-calificaciones
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/_zsL306fDck/upload/2c861f7a9667b3a9a36c9ad160544343.jpeg
tags: programacion, ejercicios

---

## Problema

Dada una lista de calificaciones, calcula el promedio de un salón de clases. Las calificaciones son números enteros.

```plaintext
Ejemplo 1
Entrada: [10,9,9,8,5]
Salida: 8.2
```

```plaintext
Ejemplo 2
Entrada: [8,7,9,10,6]
Salida: 8
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">✏</div>
<div data-node-type="callout-text">Resuleve el problema solo. Escribe a mano o en tu editor de código tu solución. Compara tu solución con el artículo.</div>
</div>

## 1\. Análisis

* Entrada es una lista de números enteros; la salida es un número decimal.
    
* Piden calcular el promedio. El promedio es la suma de los datos divididos por el número de estos.
    
* Asumimos que las calificaciones miden del 0 al 10, que la lista no puede estar vacía, y que todos los datos son correctos.
    

## 2\. Diseño

### 1\. Idea de solución

* Usar la función interna Suma(). Pero eso hace todo el trabajo. Por lo tanto, queda fuera.
    
* Usar un ciclo para obtener el promedio. Elegimos esta.
    

### 2\. Diseño del algoritmo

La técnica para resolver problemas de programación consiste en dividir el problema en problemas más simples.

Luego, refinamos el diseño para lograr pasos concretos hasta completar todos los pasos necesarios para resolver el problema.

*El primer diseño*

```plaintext
1. Sumar las calificaciones
2. Obtener el promedio
```

*Primer refinamiento*

```plaintext
1. Sumar las calificaciones
    1. Sumar una calificación con la siguiente
    2. Guardar el resultado de la suma
2. Repetir la suma hasta sumar todas las calificaciones
3. Dividir el resultado de la suma por la cantidad de calificaciones
4. Escribir el promedio
```

*Segundo refinamiento*

Inicializamos la variable `suma` en 0 para guardar el resultado de las sumas. 0 es un valor neutro. Al sumar 0 + un número, obtenemos el número.

Sumamos la calificación actual a `suma`. Esto porque visitamos una calificación de la lista de calificaciones a cada paso del ciclo. Al final, `suma` contendrá la suma de todas las calificaciones.

```plaintext
1. Sumar las calificaciones 
    1. Asignar 0 a suma
    2. Sumar la calificación actual a suma
    3. Guardar el resultado de la suma
2. Repetir la suma hasta sumar todas las calificaciones
3. Dividir el resultado de la suma por la cantidad de calificaciones 
4. Escribir el promedio
```

*Tercer refinamiento*

Organicemos las variables que usaremos:

* En la variable `tamaño` guardamos el número de elementos de la lista de calificaciones.
    
* Asignamos 0 a `suma`.
    
* Asignamos 0 a `i` que es la variable de control del ciclo.
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Obtenemos el número de elementos de una lista o array con la función interna <code>Longitud</code>.</div>
</div>

Usaremos un ciclo `mientras`. El ciclo se va a repetir mientras `i < tamaño`.

En cada paso del ciclo se ejecuta:

* `suma ← suma + calificaciones[i]`
    
* `i++`
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Es muy importante no olvidar aumentar la variable de control <code>i</code>. De lo contrario, el ciclo caerá en un ciclo infinito. Esto porque <code>i</code> siempre va a ser 0. Por lo tanto, la condición de parada del ciclo <code>i &lt; tamaño</code> siempre evaluará <code>true</code>.</div>
</div>

Ejecutemos en seco dos pasos del ciclo para ver qué estamos haciendo.

| i | suma |
| --- | --- |
| 0 | 0 + 10 = 10 |
| 1 | 10 + 9 = 19 ... |

*Diseño final en pseudocódigo*

```plaintext
Algoritmo Promedio:

# Variables
array[n] enteros: calificaciones
real: suma ← 0
entero: i ← 0
        tamaño ← Longitud(calificaciones)

inicio
    mientras i < tamaño hacer
        suma ← suma + calificaciones[i]
        i++
    fin mientras
    escribir(suma / tamaño)
fin
```

### 3\. Comprobación en seco

Ejecutamos en seco el algoritmo para comprobarlo paso a paso.

Ejemplo 1

| i | suma |
| --- | --- |
| 0 | 10 |
| 1 | 19 |
| 2 | 28 |
| 3 | 36 |
| 4 | 41 |

Promedio = 8.2

Al parecer, nuestro algoritmo es correcto. Hicimos un buen trabajo.

Ahora es tu turno. Ejecuta en seco el algoritmo con los datos del ejemplo 2.

## 3\. Codificación

Una vez que tenemos el algoritmo, podemos traducirlo a cualquier lenguaje de programación. He aquí el algoritmo codificado en Python.

```python
# Programa Promedio
# variables
calificaciones = [10,9,9,8,5]
tamanio = len(calificaciones)
suma = 0

# Obtener la suma de las calificaciones
i = 0
while i < tamanio:
    suma = suma + calificaciones[i]
    i+=1 

# Salida
print(suma/tamanio)
```

Comprueba el programa ejecutándolo. Si encuentras errores, es necesario depurar el programa. Depurar es estudiar el código para encontrar el error y solucionarlo.

## 4\. Complejidad

Tiempo: O(n) (lineal) porque el algoritmo debe recorrer cada elemento de la lista.

Espacio: O(1) (constante) porque el algoritmo no utiliza una estructura de datos adicional.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.