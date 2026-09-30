# Intercambios-de-Variables
# 🔄 Ejercicio 4: Intercambio de Variables (Algoritmo Swap)

Este repositorio ilustra de forma práctica el concepto fundamental del intercambio de valores entre dos variables utilizando una variable auxiliar como puente temporal. Este patrón lógico es el pilar de los algoritmos de ordenamiento (como el método de la burbuja o Quicksort).

**Autor:** Cristian Gómez T.  
**Materia:** Programación / Lógica de Algoritmos  

---

## 📋 1. Definición del Problema

El objetivo es intercambiar los valores contenidos en dos variables numéricas (`A` y `B`). Si asignáramos directamente `A = B`, el valor original de `A` se destruiría (sobrescritura). Para evitar la pérdida de información, se introduce una tercera variable temporal llamada `temp` (auxiliar) que resguarda el primer valor mientras se realiza la transferencia.

---

## 📸 2. Evidencia de Ejecución

Para demostrar la validez del algoritmo, se adjunta la captura del entorno de desarrollo (IDE) con la salida de consola que confirma el intercambio exitoso de los valores:


<img width="927" height="528" alt="image" src="https://github.com/user-attachments/assets/5de3c5b5-a271-4bea-ba20-6aaf9983de8c" />(intercambio.png)

*(Nota: Asegúrate de guardar tu imagen con el nombre "intercambio.png" en la raíz de tu repositorio para que se renderice aquí).*

---

## 📊 3. Análisis de Entradas, Procesos y Salidas

| Componente | Variable | Estado Inicial | Estado Final | Descripción |
| :--- | :--- | :---: | :---: | :--- |
| **Entrada / Estado** | `A` | `5` | `10` | Primera variable entera a intercambiar. |
| **Entrada / Estado** | `B` | `10` | `5` | Segunda variable entera a intercambiar. |
| **Proceso / Auxiliar**| `temp` | *Nulo* | `5` | Almacén temporal del valor de `A`. |

### Flujo del Proceso Paso a Paso:
1. **Resguardo:** Copiar el valor de `A` dentro de `temp` (`temp = A`). Ahora el `5` está a salvo.
2. **Transferencia:** Copiar el valor de `B` dentro de `A` (`A = B`). Ahora `A` vale `10`.
3. **Restauración:** Copiar el valor de `temp` dentro de `B` (`B = temp`). Ahora `B` vale `5`.

---

## 💻 4. Pseudocódigo

```text
Algoritmo Intercambio_Variables
    // Definición de variables
    Definir A, B, temp Como Entero
    
    // Inicialización de valores
    A <- 5
    B <- 10
    
    Escribir "=== Valores Iniciales ==="
    Escribir "A = ", A
    Escribir "B = ", B
    
    // Proceso de intercambio (Algoritmo Swap)
    temp <- A
    A <- B
    B <- temp
    
    Escribir ""
    Escribir "=== Valores Post-Intercambio ==="
    Escribir "A = ", A
    Escribir "B = ", B
FinAlgoritmo
```

---

## ☕ 5. Código Fuente (Java)

A continuación se presenta el código limpio implementado en **Java**, tal como se muestra en la captura del entorno de ejecución:

```java
public class Ejercicio {
    public static void main(String[] args) {
        // 1. Declaración e inicialización de variables
        int A = 5;
        int B = 10;
        int temp;

        // 2. Algoritmo de intercambio matemático
        temp = A; // temp guarda el 5
        A = B;    // A ahora recibe el 10
        B = temp; // B recibe el 5 guardado en temp

        // 3. Salida de resultados en consola
        System.out.println("A = " + A);
        System.out.println("B = " + B);
    }
}
```

---

## 🛠️ Conceptos Clave Demostrados
*   **Asignación Secuencial:** Entendimiento de que las variables en memoria se sobrescriben si no se respaldan previamente.
*   **Variable Auxiliar (Temporal):** Uso de buffers eficientes para la manipulación de estados de memoria a bajo nivel.
*   **Optimización de Datos:** Patrón lógico elemental requerido para reestructurar arreglos o vectores multidimensionales.
