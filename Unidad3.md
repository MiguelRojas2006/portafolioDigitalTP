## CONTENIDOS

<details>
<summary><strong> Modularidad </strong></summary>

## ¿Qué es la Modularidad?

Es el principio de diseño que consiste en descomponer un programa grande y complejo en unidades pequeñas, autónomas y manejables llamadas módulos (funciones en C). 

**Ventaja principal:** Permite la reutilización de código; una vez creada una función (ej. para leer una tarjeta de bus), puedes usarla en diferentes partes del programa sin reescribirla.  

**Abstracción:** Oculta los detalles internos de cómo se ejecuta una tarea. El usuario de la función solo necesita saber qué recibe (parámetros) y qué devuelve.  

## Mecanismos de paso de parámetros

## 1. Paso por valor (Value)

- **Funcionamiento:** La función recibe una copia del valor de la variable original.

- **Efecto:** Si la función modifica el valor, el cambio ocurre solo dentro de la función. La variable original en el main() permanece intacta.

- **Cuándo usarlo:** Cuando solo necesitas consultar un dato sin alterar la fuente original (ej. calcular un promedio de notas).

## 2. Paso por referencia (Reference)

- **Funcionamiento:** La función recibe la dirección de memoria (&) de la variable original utilizando punteros.
  
- **Efecto:** Cualquier cambio realizado dentro de la función altera directamente la variable original, ya que ambos comparten la misma ubicación en memoria.
  
- **Cuándo usarlo:** Cuando necesitas que una función actualice múltiples valores o modifique una estructura de datos externa (ej. actualizar el saldo de una tarjeta en tu proyecto de bus).

### Comparativa: Paso por Valor vs. Paso por Referencia

| Característica | Paso por Valor | Paso por Referencia |
| :--- | :--- | :--- |
| **¿Qué se envía?** | Una copia del dato | La dirección de memoria (`&`) |
| **Sintaxis** | `void func(int n)` | `void func(int *n)` |
| **Impacto en original** | Ninguno (es local) | Directo y permanente |
| **Uso en memoria** | Mayor (se crea copia) | Menor (se usa la misma) |
| **Uso práctico** | Consultar datos | Modificar/actualizar datos |
</details>

<details>
<summary><strong> Arreglos </strong></summary>

## 📌 Introducción
Un **arreglo** (o *array*) es una estructura de datos homogénea y de acceso directo que almacena una colección finita de elementos del mismo tipo en posiciones contiguas de memoria. Este portafolio recopila los fundamentos teóricos, implementaciones prácticas y ejercicios resueltos sobre arreglos unidimensionales (vectores) y bidimensionales (matrices) en el lenguaje C.

---

## 🧠 Fundamentos Teóricos

### 1. Arreglos Unidimensionales (Vectores)
Un vector es una lista secuencial de elementos. Se accede a cada valor mediante un índice numérico que inicia en `0`.

* **Declaración:** `tipo_de_dato nombre_arreglo[tamaño];`
* **Acceso a memoria:** La dirección del elemento `i` se calcula como:  
  $$\text{Dirección} = \text{Dirección Base} + (i \times \text{tamaño\_tipo})$$

### 2. Arreglos Bidimensionales (Matrices)
Una matriz es una estructura de datos organizada en filas y columnas.

* **Declaración:** `tipo_de_dato nombre_matriz[filas][columnas];`
* **Representación en memoria:** En C, las matrices se almacenan en el esquema **Row-Major Order** (orden por filas contiguas).

---

## 💻 Ejemplos de Código (C)

### 1. Operaciones Búsicas con Vectores
Ejemplo de lectura, llenado y cálculo del promedio en un arreglo unidimensional:

```c
#include <stdio.stdio.h>

#define TAM 5

int main() {
    int numeros[TAM];
    int suma = 0;
    float promedio;

    // Llenado del vector
    printf("Ingrese %d números enteros:\n", TAM);
    for (int i = 0; i < TAM; i++) {
        printf("Elemento [%d]: ", i);
        scanf("%d", &numeros[i]);
        suma += numeros[i];
    }

    promedio = (float)suma / TAM;
    printf("\nLa suma es: %d\n", suma);
    printf("El promedio es: %.2f\n", promedio);

    return 0;
}
```

### 2. Recorrido de Matrices
Ejemplo de inicialización e impresión de una matriz de $3 \times 3$:

```c
#include <stdio.h>

#define FILAS 3
#define COLS 3

int main() {
    int matriz[FILAS][COLS] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    printf("Contenido de la matriz:\n");
    for (int i = 0; i < FILAS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("%d\t", matriz[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

---

## ⚡ Algoritmos Clave sobre Arreglos

| Algoritmo | Descripción | Complejidad Temporal |
| :--- | :--- | :--- |
| **Búsqueda Secuencial** | Recorre el arreglo elemento por elemento hasta encontrar el objetivo. | $O(n)$ |
| **Búsqueda Binaria** | Requiere que el arreglo esté ordenado. Divide el rango a la mitad en cada paso. | $O(\log n)$ |
| **Ordenamiento Burbuja** | Compara e intercambia elementos adyacentes si están en el orden incorrecto. | $O(n^2)$ |

---

## 🚀 Conclusiones
1. Los arreglos son fundamentales para gestionar colecciones de datos con acceso rápido $O(1)$ mediante índices.
2. Tienen un tamaño estático definido en tiempo de compilación, por lo que la gestión eficiente del espacio de memoria es crucial.
3. El uso adecuado de bucles anidados permite manipular estructuras multidimensionales complejas de manera ordenada.

```

---

</details>
