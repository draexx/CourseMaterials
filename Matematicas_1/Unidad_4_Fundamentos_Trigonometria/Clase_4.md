**Clase 4: Leyes de Senos y Cosenos - Resolución de Triángulos Oblicuángulos**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Introducción (15 minutos)**  
**Contexto:**  
Los triángulos oblicuángulos (no rectángulos) requieren métodos especiales para su resolución. Presentaremos las herramientas fundamentales: **Ley de Senos** y **Ley de Cosenos**.

**Ejemplo motivador:**  
*"Un topógrafo necesita medir la distancia entre dos puntos separados por un lago. Solo puede acceder a un tercer punto y medir ángulos y distancias parciales. ¿Cómo resolvería este problema?"*

---

### **2. Ley de Senos (25 minutos)**  
**Definición:**  
Para cualquier triángulo con lados \(a, b, c\) y ángulos opuestos \(A, B, C\) respectivamente:  
\[
\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R
\]  
*(Donde \(R\) es el radio de la circunferencia circunscrita).*

**Casos de Aplicación:**  
- **AAL (Ángulo-Ángulo-Lado):** Se conocen dos ángulos y un lado no incluido.  
- **LAL (Lado-Ángulo-Lado):** Se conocen dos lados y un ángulo opuesto a uno de ellos.  

**Ejemplo 1 (AAL):**  
*Dado: \(A = 40°\), \(B = 60°\), lado \(a = 8\). Hallar los demás elementos.*  
- **Solución:**  
  1. \(C = 180° - 40° - 60° = 80°\).  
  2. \(\frac{8}{\sin 40°} = \frac{b}{\sin 60°} \Rightarrow b \approx 10.78\).  
  3. \(\frac{8}{\sin 40°} = \frac{c}{\sin 80°} \Rightarrow c \approx 12.22\).  

**Ejemplo 2 (LAL):**  
*Dado: \(a = 7\), \(b = 10\), \(A = 30°\). Hallar \(B\).*  
- **Solución:**  
  \[
  \frac{7}{\sin 30°} = \frac{10}{\sin B} \Rightarrow \sin B = \frac{10 \cdot \sin 30°}{7} \approx 0.714 \Rightarrow B \approx 45.58°.
  \]  

---

### **3. Ley de Cosenos (25 minutos)**  
**Definición:**  
Para cualquier triángulo:  
\[
c^2 = a^2 + b^2 - 2ab \cos C
\]  
*(Análogo para lados \(a\) y \(b\)).*

**Casos de Aplicación:**  
- **LLL (Lado-Lado-Lado):** Se conocen los tres lados.  
- **LAL (Lado-Ángulo-Lado):** Se conocen dos lados y el ángulo incluido.  

**Ejemplo 1 (LLL):**  
*Dado: \(a = 5\), \(b = 7\), \(c = 8\). Hallar ángulo \(C\).*  
- **Solución:**  
  \[
  \cos C = \frac{5^2 + 7^2 - 8^2}{2 \cdot 5 \cdot 7} = \frac{10}{70} \approx 0.1429 \Rightarrow C \approx 81.79°.
  \]  

**Ejemplo 2 (LAL):**  
*Dado: \(a = 6\), \(b = 9\), \(C = 45°\). Hallar lado \(c\).*  
- **Solución:**  
  \[
  c^2 = 6^2 + 9^2 - 2 \cdot 6 \cdot 9 \cdot \cos 45° \approx 36 + 81 - 76.37 \approx 40.63 \Rightarrow c \approx 6.37.
  \]  

---

### **4. Actividad Práctica (30 minutos)**  
**Ejercicio Grupal (Aplicación Real):**  
*Un barco navega 12 km hacia el este, luego gira 70° hacia el norte y navega 15 km más. ¿A qué distancia está del punto de partida?*  
- **Solución:**  
  1. Triángulo con lados \(a = 12\), \(b = 15\), ángulo incluido \(C = 110°\) (180° - 70°).  
  2. Aplicar Ley de Cosenos:  
     \[
     c^2 = 12^2 + 15^2 - 2 \cdot 12 \cdot 15 \cdot \cos 110° \approx 144 + 225 - (-123.13) \approx 492.13 \Rightarrow c \approx 22.18 \text{ km}.
     \]  

**Ejercicio Individual:**  
*Dado un triángulo con \(a = 10\), \(B = 50°\), \(C = 75°\). Resolver el triángulo.*  

---

### **5. Cierre y Resumen (5 minutos)**  
**Key Takeaways:**  
- **Ley de Senos:** Ideal para AAL/LAL.  
- **Ley de Cosenos:** Útil para LAL/LLL.  
- **Aplicaciones:** Topografía, navegación, ingeniería.  

**Tarea:**  
1. Resolver: Triángulo con lados \(a = 8\), \(b = 11\), \(c = 13\). Hallar todos los ángulos.  
2. Investigar: ¿Cómo se usan estas leyes en el diseño de redes de telecomunicaciones?  

**Materiales:**  
- Calculadoras científicas.  
- Diagramas de triángulos oblicuángulos para visualización.  

--- 

Esta clase integra teoría, ejemplos numéricos y problemas aplicados para dominar triángulos no rectángulos, esenciales en campos técnicos.