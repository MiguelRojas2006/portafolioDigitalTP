## CONTENIDOS

<details>
<summary><strong> Modularidad </strong></summary>

# 🧩 Sección: Modularidad en C

## 🧠 Fundamentación Teórica

La **modularidad** es un principio de diseño de software que consiste en dividir un programa complejo en subprogramas más pequeños, independientes y manejables denominados **funciones** o **procedimientos**. 

### Ventajas de la Modularidad:
* **Reusabilidad:** Reduce la duplicación de código permitiendo invocar la misma lógica múltiples veces.
* **Mantenibilidad:** Facilita la detección y corrección de errores al aislar bloques de código.
* **Legibilidad:** Mejora la estructura global de la aplicación al mantener la función `main()` limpia y enfocada en el flujo principal.

### Mecanismos de Paso de Parámetros en C:
1. **Paso por Valor:** La función recibe una copia exacta del dato alojado en la variable de origen. Cualquier modificación realizada dentro del cuerpo de la función no altera la variable original en la función llamadora.
2. **Paso por Referencia:** Se pasa la dirección de memoria de la variable mediante punteros (`*`). Esto permite a la función acceder directamente a la celda de memoria original y modificar su valor de forma permanente.

---

## 💻 Ejemplos Prácticos en C

### 1. Paso de Parámetros por Valor
* **Descripción:** Cálculo del área de un rectángulo.
* **Comportamiento:** Las variables `base` y `altura` se copian en los parámetros de la función `calcularArea`. Si la función intentara modificar esos parámetros, los valores originales en `main()` permanecerían intactos.

```c
#include <stdio.h>

// Función que recibe parámetros por valor y retorna un resultado de tipo float
float calcularArea(float base, float altura) {
    float area = base * altura;
    return area;
}

int main() {
    float b = 5.0;
    float h = 3.0;

    printf("--- MODULARIDAD: PASO POR VALOR ---\n");
    printf("Base original: %.2f\n", b);
    printf("Altura original: %.2f\n", h);

    // Llamada a la función enviando copias de los valores
    float resultado = calcularArea(b, h);

    printf("El área calculada es: %.2f\n\n", resultado);

    return 0;
}
```

---

### 2. Paso de Parámetros por Referencia
* **Descripción:** Intercambio de valores (*swap*) entre dos variables enteras utilizando punteros.
* **Comportamiento:** Se envían las direcciones de memoria (`&a`, `&b`) a la función `intercambiar`. La función utiliza el operador de desreferencia (`*`) para alterar directamente el contenido de las variables originales.

```c
#include <stdio.h>

// Función que recibe las direcciones de memoria (punteros) de dos enteros
void intercambiar(int *num1, int *num2) {
    int aux = *num1; // Guardamos el valor apuntado por num1 en una variable temporal
    *num1 = *num2;   // Asignamos el valor apuntado por num2 a la dirección de num1
    *num2 = aux;     // Asignamos el valor temporal a la dirección de num2
}

int main() {
    int x = 10;
    int y = 20;

    printf("--- MODULARIDAD: PASO POR REFERENCIA ---\n");
    printf("Valores antes del intercambio: x = %d, y = %d\n", x, y);

    // Se envían las direcciones de memoria utilizando el operador '&'
    intercambiar(&x, &y);

    printf("Valores después del intercambio: x = %d, y = %d\n\n", x, y);

    return 0;
}
```
</details>

<details>
<summary><strong> Arreglos </strong></summary>

# 📊 Sección: Arreglos (Arrays) en C

## 🧠 Fundamentación Teórica

Un **arreglo** es una estructura de datos homogénea y de acceso directo que almacena una colección finita de elementos del mismo tipo en posiciones contiguas de memoria RAM. Los arreglos se clasifican según su dimensión:

1. **Arreglos Unidimensionales (Vectores):** Estructuras lineales accesibles mediante un único índice $i$, donde la dirección en memoria del elemento se calcula a partir de la dirección base.
2. **Arreglos Bidimensionales (Matrices):** Estructuras en forma de tabla organizadas por filas y columnas. En C se ordenan bajo el esquema *Row-Major Order* (almacenamiento por filas contiguas en memoria).
3. **Arreglos Multidimensionales y Cadenas:** Estructuras de 3 o más dimensiones ($N$-dimensionales) o arreglos de arreglos (como colecciones de cadenas de caracteres `char[][]`).

---

## 💻 Ejemplos Prácticos en C por Tipo de Arreglo

### 1. Arreglo Unidimensional (Vector)
* **Descripción:** Cálculo del valor promedio de una serie de calificaciones.
* **Aplicación:** Permite la recolección secuencial y la acumulación de datos en un solo ciclo.

```c
#include <stdio.h>

#define TAM 5

int main() {
    float notas[TAM] = {8.5, 9.0, 7.5, 10.0, 8.0};
    float suma = 0.0;
    float promedio;

    printf("--- ARREGLO UNIDIMENSIONAL (VECTOR) ---\n");
    for (int i = 0; i < TAM; i++) {
        printf("Nota [%d]: %.2f\n", i, notas[i]);
        suma += notas[i];
    }

    promedio = suma / TAM;
    printf("Promedio general: %.2f\n\n", promedio);

    return 0;
}
```

---

### 2. Arreglo Bidimensional (Matriz)
* **Descripción:** Representación y cálculo de la suma de filas de una matriz de $3 \times 3$.
* **Aplicación:** Utilizado para manipulación de tablas, imágenes o sistemas de ecuaciones.

```c
#include <stdio.h>

#define FILAS 3
#define COLS 3

int main() {
    int matriz[FILAS][COLS] = {
        {5, 8, 2},
        {1, 9, 4},
        {6, 3, 7}
    };

    printf("--- ARREGLO BIDIMENSIONAL (MATRIZ) ---\n");
    for (int i = 0; i < FILAS; i++) {
        int sumaFila = 0;
        printf("Fila %d: ", i);
        for (int j = 0; j < COLS; j++) {
            printf("%d ", matriz[i][j]);
            sumaFila += matriz[i][j];
        }
        printf("| Suma de la fila: %d\n", sumaFila);
    }
    printf("\n");

    return 0;
}
```

---

### 3. Arreglo Multidimensional / Matriz de Cadenas de Caracteres
* **Descripción:** Almacenamiento y procesamiento de una lista de nombres utilizando un arreglo de arreglos (`char[FILAS][LONGITUD]`).
* **Aplicación:** Manipulación de colecciones de textos o registros tridimensionales en memoria.

```c
#include <stdio.h>

#define TOTAL_ESTUDIANTES 4
#define MAX_LONGITUD 30

int main() {
    // Arreglo de 2 dimensiones usado como colección de cadenas de texto
    char estudiantes[TOTAL_ESTUDIANTES][MAX_LONGITUD] = {
        "Miguel Rojas",
        "Karen Lalangui",
        "David Luna",
        "Andy Ordonez"
    };

    printf("--- ARREGLO MULTIDIMENSIONAL (CADENAS) ---\n");
    printf("Lista de Integrantes Registrados:\n");
    for (int i = 0; i < TOTAL_ESTUDIANTES; i++) {
        printf("Estudiante #%d: %s\n", i + 1, estudiantes[i]);
    }

    return 0;
}
```
---

</details>
