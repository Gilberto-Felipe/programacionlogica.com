---
title: "Descubre el día de la semana de cualquier fecha del mes"
seoTitle: "Descubre cómo determinar el día de la semana de cualquier día del mes"
seoDescription: "Descubre cómo determinar el día de la semana de cualquier fecha del mes, asumiendo que el primer día es lunes. Aprende a resolver este problema paso a paso"
datePublished: Sun Jun 23 2024 04:41:44 GMT+0000 (Coordinated Universal Time)
cuid: clxr2alwa000009moea2z2ich
slug: descubre-el-dia-de-la-semana-de-cualquier-fecha-del-mes
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/bwOAixLG0uc/upload/0bb567d1d0e67718c147a9bc00cded94.jpeg
tags: programacion, diseno-de-algoritmos, nivel-basico

---

Imagina que quieres saber qué día de la semana es un día específico del mes, sabiendo que el primer día del mes es lunes. Este artículo te mostrará cómo resolver este problema y codificar la solución en Python..

## Problema

Dado un día del mes, determinar qué día de la semana es asumiendo que el primer día del mes es lunes.

```plaintext
Ejemplo 1
Entrada: 15
Salida: lunes
```

```plaintext
Ejemplo 2
Entrada: 28
Salida: domingo
```

```plaintext
Ejemplo 3
Entrada: 11
Salida: jueves
```

*Consejo: Antes de escribir código debes saber cómo se resuelve el problema. Piensa en cómo lo resuelves sin código. Haz el algoritmo paso a paso en un papel o en el editor de código. Luego compara tu solución con la del artículo.*

## 1\. Análisis

El problema nos pide saber qué día de la semana es a partir de un día del mes. El primer día del mes corresponde a lunes. En otras palabras, se nos pide hacer un mapeo del día del mes que nos dan al día de la semana correspondiente. Por ejemplo, si me dan el día 9 de mes la respuesta sería martes.

Vamos a explicarlo con pelotas y con 7 cajas para guardar las pelotas. Dentro de cada caja caben varias pelotas. Las reglas:

Sólo puedes poner una pelota en la caja a la vez. La siguiente pelota va en la siguiente caja. No puedes saltar de caja. Cuando terminas de recorrer las 7 cajas vuelves a poner la siguiente pelota en la primera caja.

Las pelotas representa el día dado. Supongamos que nos dan 9 pelotas, el día 9 del mes.

| Lun 🟢 | Mar 🔵 | Mié 🟡 | Jue 🟠 | Vie 🟣 | Sáb 🟤 | Dom🔴 |

| Lun 🟢 | Mar 🔵 | Mié | Jue | Vie | Sáb | Dom |

## 2\. Diseño del algoritmo

### 1\. Idea de solución

Como primer paso, tengo que encontrar una operación que me permita obtener del día del mes las 7 cajas o valores de forma constante.

Una primera idea, sería usar la división: 9 / 1 = 9; 9 / 2 = 4.5; y no avanzo con mi objetivo.

Otra idea es usar el resto o residuo de la división. ¿Por qué? Porque en este caso, la operación resto nos devuelve un número comprendido entre 0 y 7. Allí tenmos los 7 valores que necesitmamos. Por ejemplo, el residuo de 9 dividido 7 es 2.

Luego, el segundo paso es mapear estos 7 valores a los días de la semana.

Este es el mapeo:

| resto | día de la semana |
| --- | --- |
| 0 | domingo |
| 1 | lunes |
| 2 | martes |
| 3 | miércoles |
| 4 | jueves |
| 5 | viernes |
| 6 | sábado |

Si deciden cambiar el día de referencia, es decir, que el primer día de la semana sea jueves, entonces debemos ajustar el mapeo y listo. El valor 0 sería para miércoles, el jueves el 1, viernes 2, etc.

### 2\. Diseño

Para resolver este problema sigue estos pasos:

1. Obtener el residuo del día del mes entre 7.
    
2. Mapear el resultado al día de la semana.
    
3. Imprimir el día de la semana.
    

```plaintext
diaMes = x
residuo = diaMes Modulo 7
segun sea residuo:
'0' -> diaSemana = domingo
'1' -> diaSemana = lunes
'2' -> diaSemana = martes
... 
imprimir(diaSemana)
```

La operación residuo también se conoce como módulo.

En el algoritmo estoy usando `según sea` que representa la estructura `switch` que existe en muchos lenguajes de programación.

### 3\. Comprobación en seco

| Día mes | Operación | Día semana |
| --- | --- | --- |
| 15 | 15 mod 7 = 1 | lunes |
| 28 | 28 mod 7 = 0 | domingo |
| 11 | 11 mod 7 = 4 | jueves |

## 3\. Codificación

```python
dia_mes = 2

residuo = dia_mes % 7

if residuo == 1:
    dia_semana = "lunes"
elif residuo == 2:
    dia_semana = "martes"
elif residuo == 3:
    dia_semana = "miércoles"
elif residuo == 4:
    dia_semana = "jueves"
elif residuo == 5:
    dia_semana = "viernes"
elif residuo == 6:
    dia_semana = "sábado"
else:
    dia_semana = "domingo"

print(dia_semana)
```

El código mapea el valor del residuo de la división del día del mes por 7 e imprime como resultado el día de la semana.

Python no tiene la sentencia `switch`. Por eso usamos la estructura `if-elif-else`.

Existen otras formas de resolver el problema, por ejemplo, usando una lista con los días de la semana. Pero en esencia, el problema se resuelve de la misma forma. Usa el operador residuo de la división y el mapeo a los días de la semana usando esa lista.

```python
def dia_de_la_semana(dia_mes):
    dias_semana = ["domingo", "lunes", "martes", "miércoles", "jueves", "viernes", "sábado"]
    return dias_semana[dia_mes % 7]

# Ejemplo de uso
dia = 15
print(f"El día {dia} del mes es {dia_de_la_semana(dia)}")
```

## 4\. Complejidad

Tiempo: O(1) constante

Porque no se recorre ninguna colección.

Espacio: O(1) constante

Porque no se utilizó una estructura de datos extra.

## Conclusión

En conclusión, hemos abordado el problema de determinar el día de la semana a partir de un día específico del mes, asumiendo que el primer día del mes es lunes. A través del análisis y diseño del algoritmo, hemos identificado que el uso del operador residuo de la división es una solución eficiente para mapear los días del mes a los días de la semana. La implementación en código demuestra que este enfoque es tanto simple como efectivo, con una complejidad constante en términos de tiempo y espacio. Este método puede ser fácilmente adaptado a diferentes días de referencia, lo que lo hace versátil y útil en diversas aplicaciones.

## Bibliografía

Joyanes Aguilar, L. (2008). Fundamentos de programación. Madrid: McGraw-Hill.