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

## **Ejemplo**
**Planteamiento del problema**

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
