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

```plaintext
función hanoi(n, source, target, auxiliary)
    si n es 1
        imprimir "Mover disco 1 de " + source + " a " + target
    de lo contrario
        hanoi(n-1, source, auxiliary, target)
        imprimir "Mover disco " + n + " de " + source + " a " + target
        hanoi(n-1, auxiliary, target, source)
