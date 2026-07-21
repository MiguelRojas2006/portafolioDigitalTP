<details>
<summary><strong> Algoritmos </strong></summary>
Un algoritmo representa una serie de pasos organizados y limitados que se llevan a cabo para solucionar un problema o ejecutar una tarea.

 En otras palabras, es similar a una receta: indica de manera precisa qué acciones realizar, paso a paso, para lograr un resultado específico.

 # Ejemplo simple

 Piensa que deseas preparar un sándwich:

 1. Agarrar dos rebanadas de pan
 2. Añadir jamón y queso
 3. Unir las rebanadas de pan

 Eso se considera un algoritmo, porque ofrece indicaciones claras y en secuencia.

 # En la informática

 En el ámbito de la informática, los algoritmos son esenciales, dado que los softwares utilizan algoritmos para:

 * Resolver problemas matemáticos
 * Organizar datos
 * Localizar información
 * Realizar elecciones

 # Propiedades de un algoritmo

 * Limitado: tiene un punto de conclusión
 * Secuencial: sigue un orden lógico
 * Clarity: cada paso es específico
 * Eficaz: busca solucionar el problema de manera adecuada

</details>

---

<details>
<summary><strong> Pseudocódigo </strong></summary>

El pseudocódigo representa una manera de formular un algoritmo empleando un lenguaje directo, similar al español o al inglés, pero con una organización lógica comparable a la de la programación.

 Este no es un lenguaje que pueda ser comprendido por una computadora, sino una herramienta para conceptualizar y estructurar la solución a un problema antes de implementarla en un programa.

 # Ejemplo

 Situación: imprimir los números del 1 al 3

 Pseudocódigo:

 ```
 Inicio
 Para i de 1 a 3 hacer
 Imprimir i
 FinPara
 Fin
 ```

 # ¿Cuál es su propósito?

 En el ámbito de la programación, el pseudocódigo sirve para:

 * Estructurar ideas antes de la programación
 * Describir algoritmos de forma sencilla
 * Prevenir errores al considerar soluciones

 # Características

 * De fácil comprensión
 * Carece de normas estrictas como un verdadero lenguaje
 * Se centra en la lógica, no en la gramática

</details>

---

<details>
<summary><strong> Diagrama de Flujo </strong></summary>

Un diagrama de flujo es una representación visual de un algoritmo que utiliza símbolos y flechas para ilustrar las etapas de un procedimiento.

 En lugar de redactar directrices (como en el pseudocódigo), aquí ilustras el proceso para facilitar su comprensión visual.

 ---

 # 🔷 Símbolos fundamentales

 * Óvalo → Comienzo / Termino
 * Rectángulo → Acción (actividades)
 * Rombo → Elección (consulta: sí/no)
 * Paralelogramo → Entrada / salida de información
 * Flechas → Señalan el recorrido del proceso

 ---

 # 🧠 Ejemplo básico

 Situación: determinar si un número es positivo

 Secuencia:

 1. Comienzo
 2. Solicitar número
 3. ¿Número &gt; 0?

 * Sí → Indicar “Es positivo”
 * No → Indicar “No es positivo”
 4. Termino

 ---

 # 🧩 ¿Cuál es su propósito?

 En el ámbito de la programación y la computación sirve para:

 * Facilitar la comprensión de un algoritmo
 * Identificar fallos antes de codificar
 * Describir procedimientos de manera clara

</details>

---

<details>
<summary><strong> Prueba de Escritorio </strong></summary>

La verificación manual es un método para analizar un algoritmo de manera secuencial, simulando su funcionamiento a nivel personal, sin recurrir a una computadora.

 Esto ayuda a confirmar si el algoritmo opera adecuadamente antes de implementarlo en código.

 ---

 # 🧠 ¿Cuál es el procedimiento?

 Se emplea una tabla donde se registra cómo las variables evolucionan en cada etapa del algoritmo.

 ---

 # ✏️ Ejemplo

 Algoritmo: añadir dos cifras

 Pseudocódigo:

 ```
 Inicio
 Ingresar A, B
 Suma ← A + B
 Mostrar Suma
 Fin
 ```

 Verificación manual:

 | A | B | Suma |
 | - | - | ---- |
 | 2 | 3 | 5 |

 👉 Se prueban valores (por ejemplo A=2 y B=3) y se confirma si el resultado es el adecuado.

 ---

 # 🧩 ¿Cuál es su propósito?

 En programación, se utiliza para:

 * Identificar errores lógicos
 * Comprender el funcionamiento del algoritmo
 * Garantizar que el resultado sea el correcto

</details>

---

<details>
<summary><strong>🔹Codificación (código fuente) </strong></summary> 

La **codificación** (o **código fuente**) es la etapa donde un algoritmo se convierte en instrucciones reales escritas en un lenguaje de programación que la computadora puede interpretar.

---

### 🧠 ¿Qué es el código fuente?

El **código fuente** es el conjunto de instrucciones escritas por el programador en un lenguaje como C++, Python o Java.

Es básicamente el **programa ya escrito**.

---

### 🔧 Ejemplo

Algoritmo: sumar dos números

**Código fuente en C++:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int A, B, suma;
    cin >> A >> B;
    suma = A + B;
    cout << suma;
    return 0;
}
```

---

### 🧩 ¿Para qué sirve?

En la programación, la codificación permite:

* Crear programas reales
* Ejecutar soluciones en la computadora
* Automatizar tareas

---

### 🔄 Relación con lo anterior

* **Algoritmo** → idea paso a paso
* **Pseudocódigo** → idea escrita
* **Diagrama de flujo** → idea dibujada
* **Código fuente** → idea programada

</details>

---

<details>
<summary><strong> 📌 Resumen </strong></summary>

👉 La **codificación** es pasar la lógica a un lenguaje de programación
👉 El **código fuente** es el resultado final escrito

</details>

---

<details>
<summary><strong> Principales Dificultades </strong></summary>

Muchas dificultades se presentan a manera de no saber los lenguajes de programación de ante mano o tener problemas con diferentes idiomas.

</details>

---

<details>
<summary><strong> 💬 Reflexión Crítica </strong></summary>

Al haber finalizado esta primera unidad podemos saber que no se debería comenzar a desarrollar código de forma inmediata. Muchos principiantes comenten esta equivocación. Si no se realizan actividades como planear el algoritmo o utilizar herramientas como pseudocódigo y diagramas, los programas resultan ser deficientes. Se vuelven complicados de comprender y presentan numerosos errores. Estos pasos preliminares no son solo para aprender. Constituyen fundamentos para razonar de manera ordenada y lógica. El algoritmo configura la solución. El pseudocódigo facilita la comprensión. El diagrama de flujo presenta el proceso de manera visual. Si se ignoran, el programador se basa más en prueba y error que en un pensamiento claro. Sin embargo, en la práctica, algunos programadores con más experiencia suelen omitir estos pasos. Esto se debe a que su experiencia les imparte la lógica. Esto genera un punto interesante. Son cruciales para los principiantes. Para los que ya son expertos, se vuelven una acción habitual. Al final, no deberían ser considerados como una obligación. Deberían ser vistos como un recurso que contribuye a que el software sea comprensible, útil y de alta calidad. Emplearlos desde el inicio mejora los resultados. También establece una buena base para solucionar problemas más complejos en el futuro.

</details>

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/9a039b9f-490b-4555-8101-27cd5c8b2938" />

[🏠 Volver a la Portada](./Portada.md)
