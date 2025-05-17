### **Clase 5: Resolución de Ecuaciones Cuadráticas - Ampliación de Definiciones y Ejercicios**

---

#### **1. Definición Profundizada de Ecuación Cuadrática**
Una ecuación cuadrática es una igualdad algebraica de **segundo grado** que puede expresarse en su **forma estándar**:
\[ ax^2 + bx + c = 0 \quad (a \neq 0) \]
donde:
- \( a, b, c \): Coeficientes reales o complejos.
- \( x \): Variable independiente.

**Casos Especiales:**
- **Ecuación cuadrática pura**: \( ax^2 + c = 0 \) (falta el término lineal).
- **Ecuación cuadrática mixta**: \( ax^2 + bx = 0 \) (falta el término independiente).

**Ejemplo Conceptual:**
La ecuación \( 3x^2 - 12 = 0 \) es cuadrática pura:
\[ 3x^2 = 12 \implies x^2 = 4 \implies x = \pm 2 \]

---

#### **2. Discriminante y Naturaleza de las Raíces**
El **discriminante** (\( \Delta \)) determina el tipo de soluciones:
\[ \Delta = b^2 - 4ac \]

| **Valor de \( \Delta \)** | **Tipo de Raíces**               | **Ejemplo**                    |
|---------------------------|-----------------------------------|--------------------------------|
| \( \Delta > 0 \)          | 2 raíces reales distintas        | \( x^2 - 5x + 6 = 0 \) (\( \Delta = 1 \), \( x = 2, 3 \)) |
| \( \Delta = 0 \)          | 1 raíz real doble                | \( x^2 - 4x + 4 = 0 \) (\( \Delta = 0 \), \( x = 2 \)) |
| \( \Delta < 0 \)          | 2 raíces complejas conjugadas    | \( x^2 + 4 = 0 \) (\( \Delta = -16 \), \( x = \pm 2i \)) |

**Ejemplo Avanzado:**
Para \( 2x^2 - 4x + 3 = 0 \):
\[ \Delta = (-4)^2 - 4 \cdot 2 \cdot 3 = -8 \]
**Soluciones complejas:**
\[ x = \frac{4 \pm \sqrt{-8}}{4} = \frac{4 \pm 2i\sqrt{2}}{4} = 1 \pm \frac{i\sqrt{2}}{2} \]

---

#### **3. Métodos de Resolución Detallados**

##### **A. Factorización (Casos Avanzados)**
**Caso 1: Trinomio Cuadrático Perfecto**
\[ x^2 + 6x + 9 = (x + 3)^2 \]

**Caso 2: Suma/Producto de Raíces**
Para \( x^2 - (r_1 + r_2)x + r_1r_2 = 0 \), donde \( r_1 \) y \( r_2 \) son raíces.  
**Ejemplo:**  
\( x^2 - 9x + 20 = 0 \) → Raíces \( 4 \) y \( 5 \) (pues \( 4+5=9 \) y \( 4 \times 5=20 \)).

**Ejercicio:**  
Factorizar \( 6x^2 - x - 2 \).  
**Solución:**  
\[ 6x^2 - x - 2 = (2x + 1)(3x - 2) \]

---

##### **B. Fórmula Cuadrática (Derivación)**
Partiendo de \( ax^2 + bx + c = 0 \):
1. Dividir por \( a \): \( x^2 + \frac{b}{a}x = -\frac{c}{a} \).
2. Completar el cuadrado:
   \[ x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 = -\frac{c}{a} + \left(\frac{b}{2a}\right)^2 \]
3. Factorizar:
   \[ \left(x + \frac{b}{2a}\right)^2 = \frac{b^2 - 4ac}{4a^2} \]
4. Despejar \( x \):
   \[ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \]

**Ejemplo:**  
Resolver \( x^2 - 6x + 8 = 0 \):  
\[ x = \frac{6 \pm \sqrt{36 - 32}}{2} = \frac{6 \pm 2}{2} \implies x = 4 \text{ o } x = 2 \]

---

##### **C. Completar el Cuadrado (Aplicación Gráfica)**
**Ejemplo:**  
Convertir \( y = x^2 + 8x + 5 \) a forma vértice.  
1. Aislar términos en \( x \):  
   \( y - 5 = x^2 + 8x \).  
2. Completar el cuadrado:  
   \( y - 5 + 16 = x^2 + 8x + 16 \) → \( y + 11 = (x + 4)^2 \).  
3. Forma vértice:  
   \( y = (x + 4)^2 - 11 \).  
**Vértice:** \( (-4, -11) \) (mínimo de la parábola).

---

#### **4. Aplicaciones Interdisciplinarias**

##### **A. Física: Movimiento Parabólico**
La altura \( h(t) \) de un proyectil está dada por:  
\[ h(t) = -4.9t^2 + v_0t + h_0 \]  
**Problema:**  
Un cohete se lanza con \( v_0 = 50 \) m/s desde \( h_0 = 0 \). ¿Cuándo alcanza 100 m?  
**Solución:**  
\[ -4.9t^2 + 50t = 100 \implies 4.9t^2 - 50t + 100 = 0 \]  
\[ t = \frac{50 \pm \sqrt{2500 - 1960}}{9.8} \approx 2.04 \text{ s y } 10.0 \text{ s} \]

##### **B. Informática: Algoritmos de Búsqueda**
En machine learning, las ecuaciones cuadráticas modelan **funciones de costo**.  
**Ejemplo:**  
Minimizar \( C(x) = x^2 - 10x + 25 \):  
\[ C(x) = (x - 5)^2 \implies \text{Mínimo en } x = 5 \]

##### **C. Economía: Maximización de Beneficios**
La ganancia \( P \) de un producto es:  
\[ P(x) = -2x^2 + 40x - 100 \]  
**Vértice:** \( x = -\frac{b}{2a} = 10 \) → \( P(10) = 100 \).

---

#### **5. Ejercicios de Consolidación**

##### **Nivel Básico**
1. Resolver \( x^2 - 9 = 0 \).  
   **Solución:** \( x = \pm 3 \).

2. Factorizar \( x^2 - 10x + 25 \).  
   **Solución:** \( (x - 5)^2 \).

##### **Nivel Intermedio**
3. Resolver \( 2x^2 + 5x - 3 = 0 \) (usar fórmula cuadrática).  
   **Solución:** \( x = \frac{1}{2} \) y \( x = -3 \).

4. Completar el cuadrado: \( x^2 + 12x + 32 = 0 \).  
   **Solución:** \( (x + 6)^2 = 4 \) → \( x = -4, -8 \).

##### **Nivel Avanzado**
5. Hallar las raíces de \( 3x^2 + 2x + 1 = 0 \).  
   **Solución:** \( x = \frac{-1 \pm i\sqrt{2}}{3} \).

6. Problema: Un terreno rectangular tiene área \( 84 \) m² con lados \( x + 5 \) y \( x - 2 \). Hallar \( x \).  
   **Solución:** \( x^2 + 3x - 94 = 0 \) → \( x \approx 8.1 \) (descartar negativo).

---

### **Tabla Resumen: Métodos de Resolución**
| **Método**            | **Ventajas**                          | **Limitaciones**               |
|------------------------|---------------------------------------|--------------------------------|
| **Factorización**      | Rápido para trinomios simples         | No aplicable si \( \Delta \) no es cuadrado perfecto |
| **Fórmula Cuadrática** | Siempre funciona (incluso con \( \Delta < 0 \)) | Cálculos complejos con coeficientes grandes |
| **Completar Cuadrado** | Útil para forma vértice en gráficas   | Laborioso para ecuaciones con \( a \neq 1 \) |

---

### **Cierre y Asignación**
**Tarea:**  
1. Resolver \( 4x^2 - 20x + 25 = 0 \) y clasificar las raíces.  
   **Solución:** \( x = \frac{5}{2} \) (raíz doble).  

2. Problema: Un algoritmo tiene tiempo de ejecución \( T(x) = x^2 - 8x + 20 \). Hallar \( x \) para \( T \) mínimo.  
   **Solución:** \( x = 4 \) → \( T(4) = 4 \).

**Reflexión:**  
¿Por qué las ecuaciones cuadráticas son fundamentales en modelado 3D?  
**Respuesta:** Describen superficies curvas como parábolas, esenciales en gráficos por computadora.

---
