### **Clase 4 Ampliada: Resolución de Ecuaciones Lineales - Definiciones Extendidas y Fundamentos Teóricos**

#### **1. Ecuación Lineal: Definición Profunda**
Una ecuación lineal es una **igualdad algebraica** que involucra una o más variables elevadas exclusivamente a la primera potencia (grado 1) y que no contiene productos entre variables. Se expresa en su forma general como:

\[
ax + b = 0 \quad \text{(una variable)}
\]
\[
ax + by + c = 0 \quad \text{(dos variables)}
\]

**Características Clave:**
- **Grado de la ecuación:** Siempre 1 (los exponentes de las variables son 1).
- **Solución:** Valor(es) que satisfacen la igualdad. En una variable, existe **exactamente una solución**, a menos que sea degenerada (ejemplo: \(0x = 5\)).

**Ejemplo Teórico:**
La ecuación \(3x - 6 = 0\) tiene solución única \(x = 2\), pues \(3(2) - 6 = 0\).

---

#### **2. Métodos de Resolución: Explicación Detallada**

##### **A. Método Algebraico (Despeje)**
**Fundamento:** Aplicar operaciones inversas para aislar la variable, manteniendo la igualdad.

**Pasos Rigurosos:**
1. **Simplificación:** Eliminar paréntesis y combinar términos semejantes.
   - Ejemplo: \(2(x - 3) + 4x = 10\) → \(2x - 6 + 4x = 10\) → \(6x - 6 = 10\).
2. **Aislamiento:** Mover términos con variables a un lado y constantes al otro.
   - \(6x = 16\).
3. **Normalización:** Dividir por el coeficiente de la variable.
   - \(x = \frac{16}{6} = \frac{8}{3}\).

**Teorema Subyacente:**  
Si \(a \neq 0\), \(ax + b = 0\) tiene solución única \(x = -\frac{b}{a}\).

---

##### **B. Método Gráfico (Geometría Analítica)**
**Fundamento:** Representar la ecuación como una recta en el plano cartesiano.

**Procedimiento:**
1. **Forma Pendiente-Intersección:** Convertir a \(y = mx + b\).
   - Ejemplo: \(2x + 3y = 6\) → \(y = -\frac{2}{3}x + 2\).
2. **Intersección con Ejes:**
   - **Corte con eje x (\(y = 0\)):** \(2x = 6\) → \(x = 3\).
   - **Corte con eje y (\(x = 0\)):** \(3y = 6\) → \(y = 2\).
3. **Solución Gráfica:** La intersección de dos rectas representa la solución del sistema.

**Interpretación Geométrica:**  
La solución de \(ax + b = 0\) es el punto donde la recta \(y = ax + b\) cruza el eje x.

---

##### **C. Ecuaciones con Coeficientes Fraccionarios**
**Estrategia:** Eliminar denominadores multiplicando por el MCM.

**Ejemplo Detallado:**
\[
\frac{2x - 1}{3} = \frac{x + 4}{2}
\]
1. **MCM de 3 y 2:** 6.
2. **Multiplicar ambos lados:**
   \[
   6 \cdot \left(\frac{2x - 1}{3}\right) = 6 \cdot \left(\frac{x + 4}{2}\right) \implies 2(2x - 1) = 3(x + 4)
   \]
3. **Resolver:**
   \[
   4x - 2 = 3x + 12 \implies x = 14.
   \]

**Teorema de Equivalencia:**  
Multiplicar ambos lados por un número distinto de cero preserva la igualdad.

---

#### **3. Casos Especiales: Análisis Teórico**

##### **A. Ecuación Sin Solución (Inconsistente)**
**Forma General:**  
\(0x = b\) (donde \(b \neq 0\)).

**Ejemplo:**  
\(5x - 5x = 2\) → \(0 = 2\).  
**Interpretación:** No existe \(x\) que satisfaga la igualdad. Gráficamente, representa rectas paralelas que nunca se cruzan.

---

##### **B. Infinitas Soluciones (Ecuación Dependiente)**
**Forma General:**  
\(0x = 0\).

**Ejemplo:**  
\(4x - 8 = 4(x - 2)\) → \(4x - 8 = 4x - 8\) → \(0 = 0\).  
**Interpretación:** Todos los números reales son soluciones. Gráficamente, es la misma recta.

---

#### **4. Aplicaciones Avanzadas y Modelado Matemático**

##### **A. Problemas de Optimización**
**Ejemplo:**  
*"Un servidor puede procesar \(3x + 10\) GB por hora. Si tiene 100 GB para procesar, ¿cuánto tiempo tardará?"*  
**Modelado:**  
\(3x + 10 = 100\) → \(x = 30\) horas.  
**Análisis Dimensional:**  
Verificar unidades: \(3x\) (GB/hora) \(\times x\) (horas) + 10 (GB) = 100 (GB).

---

##### **B. Geometría Analítica**
**Ejemplo:**  
*"Un triángulo con lados \(2x + 1\), \(3x - 2\), y \(x + 5\) tiene perímetro 24. Hallar \(x\)."*  
**Modelado:**  
\[
(2x + 1) + (3x - 2) + (x + 5) = 24 \implies 6x + 4 = 24 \implies x = \frac{20}{6} = \frac{10}{3}.
\]  
**Validación:**  
Cada lado debe ser positivo:  
\(2x + 1 > 0\) → \(x > -0.5\) (siempre válido para \(x = \frac{10}{3}\)).

---

#### **5. Ejercicios Teóricos y Demostraciones**

##### **Ejercicio 1: Demostración de Unicidad de la Solución**
**Teorema:**  
Si \(a \neq 0\), \(ax + b = 0\) tiene solución única.  
**Demostración:**  
1. Supongamos dos soluciones \(x_1\) y \(x_2\):  
   \(ax_1 + b = 0\) y \(ax_2 + b = 0\).  
2. Restando: \(a(x_1 - x_2) = 0\).  
3. Como \(a \neq 0\), \(x_1 - x_2 = 0\) → \(x_1 = x_2\).  

---

##### **Ejercicio 2: Ecuación Lineal en Dos Variables**
**Ejemplo:**  
Resolver \(2x + 3y = 12\) para \(y\).  
**Solución:**  
\(y = \frac{12 - 2x}{3}\).  
**Interpretación:**  
Familia infinita de soluciones (una para cada valor de \(x\)).

---

### **Resumen Teórico Final**
| **Concepto**               | **Definición**                                                                 | **Ejemplo**                      |
|----------------------------|-------------------------------------------------------------------------------|----------------------------------|
| **Ecuación Lineal**         | Igualdad polinómica de grado 1 en sus variables.                              | \(3x - 6 = 0\)                   |
| **Solución Única**          | Existe un único valor que satisface la ecuación.                              | \(x = 2\) en \(3x - 6 = 0\)      |
| **Sin Solución**            | Ningún valor satisface la ecuación (rectas paralelas).                       | \(0x = 5\)                       |
| **Infinitas Soluciones**    | Todos los valores reales son solución (misma recta).                         | \(0x = 0\)                       |
| **Método Gráfico**          | Solución como intersección de rectas.                                        | \(y = 2x + 1\) vs \(y = -x + 3\) |

---

### **Asignación de Profundización**
1. **Demostrar** que la ecuación \(ax + b = cx + d\) tiene solución única si \(a \neq c\).  
2. **Modelar** un problema de economía donde el costo total \(C\) sea lineal con la producción \(x\) y encontrar el punto de equilibrio.  

---

Esta ampliación teórica proporciona una base rigurosa para entender no solo cómo resolver ecuaciones lineales, sino también por qué los métodos funcionan y cómo se aplican en contextos avanzados.