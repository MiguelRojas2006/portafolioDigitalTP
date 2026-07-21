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
