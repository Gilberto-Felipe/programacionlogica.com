---
title: "Escribir la suma de los diez primeros números pares"
seoTitle: "Suma de los primeros 10 números pares"
seoDescription: "Descubre cómo calcular la suma de los primeros 10 números pares con diseñando un algoritmo. Aprende paso a paso y mejora tus habilidades de programación."
datePublished: Sun May 26 2024 08:01:16 GMT+0000 (Coordinated Universal Time)
cuid: clwn93dag00020al34xpud0xz
slug: escribir-la-suma-de-los-diez-primeros-numeros-pares
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cHhbULJbPwM/upload/9fc79fcd45d95cb8dbf6a91861883697.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

En este artículo, exploramos cómo calcular la suma de los primeros 10 números pares usando un algoritmo simple. Este ejercicio ayuda a comprender conceptos básicos de programación.

## Problema

Calcula la suma de los diez primeros números pares. Genera estos números, pero solo imprime el resultado de la suma.

```plaintext
Ejemplo 
Entrada: 2,4,6,8,10,12,14,16,18,20
Salida: 110
```

*Consejo: Antes de escribir código debes saber cómo resolver el problema. Piensa en cómo lo resolverías sin código. Haz el algoritmo paso a paso en papel o en el editor de código. Luego, compara tu solución con la del artículo.*

## 1\. Análisis

Nos piden calcular la suma de los diez primeros números pares. Tenemos que saber cuáles son los números pares. Los números pares son aquellos números que son divisibles o múltiplos de 2. Por ejemplo, 8.

Los diez primeros números pares van del 2 al 20. Nos piden generarlos para hacer la suma.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Se me ocurren dos ideas de solución:

A. Recorrer cada número del 1 al 20 incluido y evaluar si es divisible entre 2. Si lo es, es par. Luego, hago una sumatoria con todos los pares.

B. Recorrer los números de dos en dos hasta llegar al 20 incluido. Eso asegura que son pares. Luego, hago la sumatoria.

Elijo la opción B, parece más sencilla.

### 2\. Diseño

```plaintext
1. Inicializar una variable sumatoria en 0.
2. Usar un ciclo for que recorra los números desde 2 hasta 20, con un salto de 2 en 2.
3. En cada iteración, sumar el valor actual a sumatoria.
4. Imprimir el resultado final de sumatoria.
```

### 3\. Comprobación en seco

| i | sumatoria |
| --- | --- |
| 2 | 0 + 2 |
| 4 | 2 + 4 |
| ... | ... |
| 20 | 110 |

## 3\. Codificación

Ahora vamos a implementar nuestro algoritmo en Python.

```python
# Suma 10 primeros números pares
sumatoria = 0
for i in range(2, 21, 2):
    sumatoria += i
print(sumatoria)
```

En el ciclo recorremos los primeros 10 números pares. Comenzamos en 2 y saltamos de dos en 2 hasta llegar al 20 incluido.

`Range` genera una secuencia de números y tiene 3 parámetros:

* `Inicio`: en 2.
    
* `Parada`: en 21, para que incluya el último número par, el 20. Este parámetro no es inclusivo. Si lo dejamos en 20, llegaría hasta el 19.
    
* `Paso`: de 2 en 2.
    

En cada paso del ciclo hacemos la sumatoria del acumulado con el valor actual de i. Voilá.

## 4\. Complejidad

Tiempo: O(n) lineal

Es lineal porque necesitamos recorrer la colección de números pares.

Espacio: O(1) constante

Es constante porque no generamos ninguna estructura de datos extra.

## Conclusion

En este artículo analizamos, diseñamos y codificamos en Python un algoritmo para calcular la suma de los diez primeros números pares. De dos ideas de solución escogimos una: recorrer los números de dos en dos hasta llegar al 20. Se te ocurre otra solución. Inténtala y comenta.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.