## CONTENIDOS

<details>
<summary><strong> Estructuras Condicionales </strong></summary>
Son estructuras de control que permiten bifurcar el flujo de ejecución de un programa dependiendo de si se cumple o no una determinada condición booleana.

## Tipos de Estructuras Condicionales
- **Condicional Simple (Si / If):** Evalúa una condición. Si es verdadera, ejecuta un bloque de código; si es falsa, no hace nada.

<img width="737" height="248" alt="image" src="https://github.com/user-attachments/assets/984e5e80-0e7e-4fb6-8ce8-c1e30ecbcfbc" />

- **Condicional Compuesta (Si-Sino / If-Else):** Evalúa una condición. Si es verdadera ejecuta un bloque de código, y si es falsa ejecuta un bloque alternativo.

<img width="739" height="269" alt="image" src="https://github.com/user-attachments/assets/f9867b47-0322-4fb5-9ec2-207c6f5b063b" />

- **Condicional Múltiple (Según / Switch-Case):** Compara una variable o expresión con múltiples valores posibles (casos) y ejecuta el bloque correspondiente al primer valor que coincida.

<img width="738" height="465" alt="image" src="https://github.com/user-attachments/assets/3950b557-5e38-4060-9c32-ee4ac20ab1a4" />
</details>

<details>
<summary><strong> Bucles Repetitivos </strong></summary>

# Estructuras Repetitivas (Bucles)
Permiten ejecutar un bloque de código varias veces consecutivas mientras se cumpla una condición o un número determinado de ocasiones.

## Tipos de Estructuras Repetitivas
- **Mientras (While):** Evalúa la condición antes de entrar al bucle. Si la condición es falsa desde el inicio, el bloque de código nunca se ejecuta.

  <img width="737" height="310" alt="image" src="https://github.com/user-attachments/assets/7ed77447-4e6c-4951-ad6b-902930e9d780" />

- **Hacer-Mientras (Do-While):** Ejecuta el bloque de código al menos una vez y luego evalúa la condición al final del ciclo.

  <img width="737" height="308" alt="image" src="https://github.com/user-attachments/assets/3217759a-aad3-44b3-b506-695811a762bc" />

- Para (For): Se utiliza cuando se conoce de antemano la cantidad exacta de iteraciones que se van a realizar. Maneja de forma interna la inicialización, la condición y el incremento/decremento de un contador.

  <img width="735" height="304" alt="image" src="https://github.com/user-attachments/assets/20f6b8f8-fd62-46fa-8696-a16f81f6d135" />

</details>

<details>
<summary><strong> Ejemplo </strong></summary>

## **Planteamiento del problema**

- Desarrollar un programa que permita al usuario ingresar su saldo inicial y realizar 5 operaciones. En cada operación podrá retirar dinero. El programa deberá verificar si tiene saldo suficiente para realizar el retiro y actualizar el saldo disponible.
  
**Análisis del problema**
**Entradas:**
- Saldo inicial.
- Monto a retirar.

**Proceso:**
- Repetir 5 veces:
- Solicitar monto de retiro.
- Verificar si el saldo es suficiente.
- Si es suficiente, descontar el monto.
- Si no, mostrar mensaje de fondos insuficientes.

**Salidas:**
- Resultado de cada operación.
- Saldo final.

## **Código**
<img width="288" height="364" alt="image" src="https://github.com/user-attachments/assets/4106998d-4273-467a-b4c1-8bb089b29bb6" />

## **Diagrama**
<img width="6437" height="2070" alt="Diagrama en blanco (2)" src="https://github.com/user-attachments/assets/a8544112-386e-44c0-9638-90d82cdff90c" />

## **Salida en terminal**
<img width="712" height="343" alt="image" src="https://github.com/user-attachments/assets/92aa86f6-2a17-4ca4-af87-8310b6b5cd57" />

## **Pruebas de escritorio**
| Operación | Retiro ($) | Saldo Antes ($) | Resultado            | Saldo Después ($) |
| --------- | ---------- | --------------- | -------------------- | ----------------- |
| 1         | 100        | 500             | Retiro exitoso       | 400               |
| 2         | 50         | 400             | Retiro exitoso       | 350               |
| 3         | 400        | 350             | Fondos insuficientes | 350               |
| 4         | 100        | 350             | Retiro exitoso       | 250               |
| 5         | 50         | 250             | Retiro exitoso       | 200               |

</details>
<details>
<summary><strong> Principales Dificultades</strong></summary>

Una de las principales dificultades fue controlar correctamente el saldo disponible después de cada retiro, ya que era necesario actualizar el valor de la variable en cada iteración. También se presentó el reto de validar que el usuario no pudiera retirar una cantidad mayor al saldo existente, utilizando adecuadamente las estructuras condicionales dentro del ciclo repetitivo.

</details>
<details>
<summary><strong> Reflexión Crítica </strong></summary>

Este ejercicio permitió comprender la importancia de combinar estructuras repetitivas y condicionales para resolver situaciones reales. Además, ayudó a fortalecer el razonamiento lógico al verificar condiciones antes de ejecutar una acción, garantizando que las operaciones realizadas sean válidas y que el programa funcione de manera correcta y segura.
</details>
<details>
<summary><strong> Bibliografía </strong></summary>
[1] L. Joyanes Aguilar, Fundamentos de Programación: Algoritmos, Estructuras de Datos y Objetos, 4.ª ed. Madrid, España: McGraw-Hill, 2008.

[2] H. M. Deitel y P. J. Deitel, C Cómo Programar, 8.ª ed. México: Pearson Educación, 2016.

[3] B. W. Kernighan y D. M. Ritchie, El Lenguaje de Programación C, 2.ª ed. México: Pearson Educación, 2004.

[4] J. Paredes Velasco, Algoritmos y Programación Estructurada, Madrid, España: RA-MA Editorial, 2014.

[5] A. V. Aho, J. E. Hopcroft y J. D. Ullman, Fundamentos de Ciencias de la Computación. México: CECSA, 2000.
</details>

<details>
<summary><strong> Uso de IA </strong></summary>
Para la elaboración de este portafolio se utilizó una herramienta de inteligencia artificial únicamente como apoyo para conocer la forma adecuada de desglosar y organizar los temas desarrollados. El análisis, desarrollo de actividades, ejercicios, conclusiones y otros contenidos fueron realizados por el estudiante.
</details>
