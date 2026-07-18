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


</details>
