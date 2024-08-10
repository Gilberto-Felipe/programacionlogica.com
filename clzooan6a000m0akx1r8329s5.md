---
title: "Cómo Diseñar un Algoritmo para un Reloj Digital: Suma un Segundo y Mantén el Formato HH MM SS"
seoTitle: "Cómo Diseñar un Algoritmo para un Reloj Digital: Suma un Segundo"
seoDescription: "Aprende a diseñar un algoritmo para programar un reloj digital. Suma un segundo y mantén el formato HH MM SS. Luego, crea un programa en Python."
datePublished: Sat Aug 10 2024 21:53:43 GMT+0000 (Coordinated Universal Time)
cuid: clzooan6a000m0akx1r8329s5
slug: como-disenar-un-algoritmo-para-un-reloj-digital-suma-un-segundo-y-manten-el-formato-hh-mm-ss
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/ifVZHBYVx1A/upload/3b9017d36732127a4dabe56c1405eede.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

¿Alguna vez has pensado en cómo programar un reloj digital en formato HH MM SS? En este artículo, diseñaremos un algoritmo para el caso básico de agregar un segundo a una hora dada. Analizaremos los casos que debes considerar para diseñar el algoritmo y lo codificaremos en Python.

## Problema

Diseña un algoritmo que calcule la hora dentro de un segundo. El reloj cuenta con horas, minutos y segundos (HH MM SS). Es un reloj digital y sigue el siguiente formato. Hora en formato 24 horas, 24 horas = 00; 60 minutos = 00; 60 segundos = 00. Así que las 00 00 00 equivale a las 12 pm en punto.

```plaintext
Ejemplo 1
Entrada: 09 05 30
Salida:  09 05 31
```

```plaintext
Ejemplo 2
Entrada: 10 59 59
Salida:  11 00 00
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

Piden calcular la hora del reloj agregando un segundo. Debo seguir el formato sugerido. Además, hay que tomar en cuenta los casos límite en los que puede caer el algoritmo para poder solucionar correctamente esta tarea.

* Horas: después de las 23 sigue 00.
    
* Minutos: después de los 59 sigue 00.
    
* Segundos: después de los 59 sigue 00.
    
* Considerar el acarreo de una unidad de segundos a minutos, cuando los segundos dados coincidan con 59.
    
* Considerar el acarreo de una unidad de minutos a horas, cuando los minutos dados coincidan con 59 y reciba el acarreo de una unidad procedente de los segundos.
    

El acarreo es importante, porque recordemos que 60 segundos añaden un minuto; 60 minutos añaden 1 hora.

Ejemplo de caso normal:

01 10 11 - el siguiente segundo actualiza la hora a: 01 10 12.

Ejemplo de caso con acarreo:

03 59 59 - el siguiente segundo actualiza la hora a: 04 00 00.

## 2\. Diseño del algoritmo

### 1\. Idea de solución

La idea de solución es sencilla: sumar un segundo a la hora dada y considerar los casos especiales para que se muestre la hora en el formato indicado. Los casos especiales los manejamos con estructuras de condición.

### 2\. Diseño

```plaintext
# variables:
horas, minutos, segundos, hh, mm, ss

iniciar
    sumar 1 a segundos
    si segundos = 60 entonces
        segundos ← 00
        sumar 1 a minutos
        si minutos = 60 entonces
            minutos ← 00
            sumar 1 a horas
            si horas = 24 entonces
                horas ← 00
            fin si
        fin si
    fin si

    imprimir(horas.formatedas, minutos.formateados, segundos.formateados)
fin
```

En las ramas condicionales hemos cubierto todas los escenarios. Al imprimir hemos inidicado que las horas, minutos y segundos van formateados. No lo hemos desarrollado. Eso lo haremos en el código.

### 3\. Comprobación en seco

| entrada | salida |
| --- | --- |
| 09 05 30 | 09 05 31 |
| 10 59 59 | 11 00 00 |

## 3\. Codificación

Una vez que tenemos diseñado y probado el algortimos es hora de traducirlo a código. Manos al teclado!

```python
# entrada
horas = 11
minutos = 59
segundos = 00

# algoritmo
segundos += 1
if segundos == 60:
    segundos = 0
    minutos += 1
    if minutos == 60:
        minutos = 0
        horas += 1
        if horas == 24:
            horas = 0

print(f"{str(horas).zfill(2)} {str(minutos).zfill(2)} {str(segundos).zfill(2)}")
```

El método `str(numero)` convierte a tipo cadena un número.

El método `zfill` es un método interno de Python que sirve para para rellenar una cadena numérica con ceros a la izquierda hasta que alcance un ancho especificado por el argumento que recibe. Esto asegura que la representación en cadena del número tenga una longitud mínima. Por ejemplo, si la cadena es "0", entonces "00"; si "1", entonces "01"; si "20", entonces "20", ya no necesita relleno.

Fíjate que unimos el método `zfill` a `str(numero)`. Primero `str(numero)` convierte cadena el número. Luego, `zfill` formatea esta cadena. Por último, guardamos el resultado en la variable correspondiente.

Ejecuta el programa, o haz la comprobación en seco.

## 4\. Complejidad

Tiempo: O(1) constante

Porque no recorremos una colección.

Espacio: O(1) constante

Porque no usamos estructura de datos extra.

## Conclusión

En resumen, en este artículo diseñamos y codificamos el algoritmo base de un reloj digital y cumplimos con el formato que se nos pidió. Pon atención en que, para resolverlo, listamos los casos límite o escenarios que podría tener. Con estructuras condicionales manejamos estos escenarios. Conocer estos escenarios es muy importante para tu programa o software para que tengan el comportamiento esperado. Al codificar, usamos el método `zfill` dePython que rellena una cadena de números con ceros a la izquierda.

Reto: Diseña el algoritmo y el programa en Python de un reloj para que funcione las 24 horas.

## Bibliografía

Joyanes Aguilar, L. (2008). *Fundamentos de programación.* Madrid: McGraw-Hill.