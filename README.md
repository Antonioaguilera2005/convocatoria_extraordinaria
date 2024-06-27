https://github.com/Antonioaguilera2005/convocatoria_extraordinaria.git
# convocatoria_extraordinaria
## Torres de Hanói

### Hipótesis

El problema de las Torres de Hanói puede resolverse de manera eficiente utilizando un enfoque recursivo, moviendo los discos entre las varillas según las reglas establecidas.

### Precondición

- Se tiene un número `n` de discos.
- Los discos están apilados en la varilla `source` en orden descendente de tamaño.
- Existen tres varillas: `source`, `target` y `auxiliary`.

### Postcondición

- Todos los discos se han movido de la varilla `source` a la varilla `target`, manteniendo el orden descendente de tamaño.

### Entrada

- `n`: Número de discos.
- `source`: Nombre de la varilla de origen.
- `target`: Nombre de la varilla de destino.
- `auxiliary`: Nombre de la varilla auxiliar.

### Salida

- Instrucciones para mover los discos de la varilla `source` a la varilla `target`.

### Efecto

- Los discos se mueven de la varilla `source` a la varilla `target` siguiendo las reglas del juego.

### Pseudocódigo

función hanoi(n, source, target, auxiliary)
    si n es 1
        imprimir "Mover disco 1 de " + source + " a " + target
    de lo contrario
        hanoi(n-1, source, auxiliary, target)
        imprimir "Mover disco " + n + " de " + source + " a " + target
        hanoi(n-1, auxiliary, target, source)

## Bubble Sort

### ¿Qué es el método Bubble Sort?

El método Bubble Sort, también conocido como Ordenamiento Burbuja, es un sencillo algoritmo de ordenación que funciona comparando repetidamente los elementos adyacentes de una lista y permutándolos si están en el orden incorrecto. Este proceso se repite hasta que la lista esté completamente ordenada.

### ¿Cómo funciona Bubble Sort?

El algoritmo Bubble Sort recorre la lista varias veces. En cada pasada, compara cada par de elementos adyacentes y los intercambia si están en el orden incorrecto. Este proceso hace que los elementos más grandes "burbujen" hacia el final de la lista, de ahí el nombre "Bubble Sort".

#### Pasos del algoritmo:

1. Comenzar en el primer elemento de la lista.
2. Comparar el elemento actual con el siguiente elemento.
3. Si el elemento actual es mayor que el siguiente elemento, intercambiarlos.
4. Mover al siguiente par de elementos adyacentes y repetir el proceso hasta llegar al final de la lista.
5. Repetir los pasos del 1 al 4 hasta que no se necesiten más intercambios.

El algoritmo tiene una complejidad temporal de \(O(n^2)\) en el peor y promedio de los casos, donde \(n\) es el número de elementos en la lista.

### ¿Cuándo utilizar Bubble Sort?

Bubble Sort es conveniente para listas pequeñas o listas que ya están parcialmente ordenadas, ya que su implementación es sencilla y fácil de entender. Sin embargo, no es eficiente para listas grandes debido a su complejidad temporal.

### Ejemplo Conceptual de Bubble Sort

Vamos a aplicar Bubble Sort para ordenar la lista de números [29, 10, 14, 37, 13]:

#### Lista inicial: [29, 10, 14, 37, 13]

**Primera pasada:**
1. Comparar 29 y 10. Intercambiar, ya que 29 > 10.
   Lista: [10, 29, 14, 37, 13]
2. Comparar 29 y 14. Intercambiar, ya que 29 > 14.
   Lista: [10, 14, 29, 37, 13]
3. Comparar 29 y 37. No intercambiar, ya que 29 < 37.
   Lista: [10, 14, 29, 37, 13]
4. Comparar 37 y 13. Intercambiar, ya que 37 > 13.
   Lista: [10, 14, 29, 13, 37]

**Segunda pasada:**
1. Comparar 10 y 14. No intercambiar, ya que 10 < 14.
   Lista: [10, 14, 29, 13, 37]
2. Comparar 14 y 29. No intercambiar, ya que 14 < 29.
   Lista: [10, 14, 29, 13, 37]
3. Comparar 29 y 13. Intercambiar, ya que 29 > 13.
   Lista: [10, 14, 13, 29, 37]
4. Comparar 29 y 37. No intercambiar, ya que 29 < 37.
   Lista: [10, 14, 13, 29, 37]

**Tercera pasada:**
1. Comparar 10 y 14. No intercambiar, ya que 10 < 14.
   Lista: [10, 14, 13, 29, 37]
2. Comparar 14 y 13. Intercambiar, ya que 14 > 13.
   Lista: [10, 13, 14, 29, 37]
3. Comparar 14 y 29. No intercambiar, ya que 14 < 29.
   Lista: [10, 13, 14, 29, 37]
4. Comparar 29 y 37. No intercambiar, ya que 29 < 37.
   Lista: [10, 13, 14, 29, 37]

**Cuarta pasada:**
1. Comparar 10 y 13. No intercambiar, ya que 10 < 13.
   Lista: [10, 13, 14, 29, 37]
2. Comparar 13 y 14. No intercambiar, ya que 13 < 14.
   Lista: [10, 13, 14, 29, 37]
3. Comparar 14 y 29. No intercambiar, ya que 14 < 29.
   Lista: [10, 13, 14, 29, 37]
4. Comparar 29 y 37. No intercambiar, ya que 29 < 37.
   Lista: [10, 13, 14, 29, 37]

En este punto, la lista está completamente ordenada.

#### Lista final: [10, 13, 14, 29, 37]

Este proceso de comparación e intercambio continúa hasta que la lista esté completamente ordenada.

