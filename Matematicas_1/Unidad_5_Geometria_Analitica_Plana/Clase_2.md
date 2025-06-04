**Clase 2: La Recta y sus Ecuaciones**  
**Duración:** 90 minutos  
**Objetivos:**  
1. Definir rectas mediante ecuaciones generales, punto-pendiente y explícita.  
2. Calcular pendientes y ángulos de inclinación.  
3. Aplicar en trayectorias de señales y diseño de redes.  

---

### **1. Ecuación General de la Recta (20 minutos)**  
**Definición:**  
Toda recta en el plano puede expresarse como:  
\[
\boxed{Ax + By + C = 0}
\]  
- **A, B, C:** Constantes reales (\(A\) y \(B\) no simultáneamente nulas).  
- **Interpretación:**  
  - Si \(B \neq 0\), se puede despejar \(y\): \(y = -\frac{A}{B}x - \frac{C}{B}\).  
  - Si \(B = 0\), recta vertical: \(x = -\frac{C}{A}\).  

**Ejemplos:**  
1. *Recta horizontal:* \(2y - 6 = 0\) → \(y = 3\) (paralela al eje X).  
2. *Recta vertical:* \(3x + 4 = 0\) → \(x = -\frac{4}{3}\) (paralela al eje Y).  
3. *Recta oblicua:* \(2x - 3y + 6 = 0\) → \(y = \frac{2}{3}x + 2\).  

**Aplicación en telecomunicaciones:**  
- *Tendido de fibra óptica:* Una recta entre dos postes en \((0, 0)\) y \((30, 15)\):  
  \[
  \frac{y - 0}{x - 0} = \frac{15 - 0}{30 - 0} \implies y = \frac{1}{2}x \implies x - 2y = 0
  \]  

---

### **2. Pendiente e Inclinación (25 minutos)**  
**Definición:**  
- **Pendiente (\(m\)):** Razón de cambio vertical/horizontal.  
  \[
  m = \frac{y_2 - y_1}{x_2 - x_1} = \tan \theta
  \]  
  - \(\theta\): Ángulo de inclinación (medido desde el eje X positivo).  

| **Tipo de recta** | **Pendiente (\(m\))** | **Ángulo (\(\theta\))** |  
|-------------------|------------------------|--------------------------|  
| Horizontal        | \(0\)                  | \(0^\circ\)              |  
| Vertical          | Indefinida             | \(90^\circ\)             |  
| Creciente         | \(m > 0\)              | \(0^\circ < \theta < 90^\circ\) |  
| Decreciente       | \(m < 0\)              | \(90^\circ < \theta < 180^\circ\) |  

**Ejemplos:**  
1. *Fibra óptica entre postes:* De \((0, 0)\) a \((30, 15)\):  
   \[
   m = \frac{15 - 0}{30 - 0} = 0.5 \quad \Rightarrow \quad \theta = \arctan(0.5) \approx 26.57^\circ
   \]  
2. *Antenas en terreno inclinado:* De \((-4, 3)\) a \((2, -5)\):  
   \[
   m = \frac{-5 - 3}{2 - (-4)} = \frac{-8}{6} \approx -1.33 \quad \Rightarrow \quad \theta \approx 126.87^\circ
   \]  

---

### **3. Ecuación Punto-Pendiente (20 minutos)**  
**Fórmula:**  
Dado un punto \((x_1, y_1)\) y pendiente \(m\):  
\[
\boxed{y - y_1 = m(x - x_1)}
\]  

**Ejemplos:**  
1. *Recta con \(m = -2\) que pasa por \((3, 4)\):*  
   \[
   y - 4 = -2(x - 3) \implies y = -2x + 10
   \]  
2. *Diseño de torre de soporte:*  
   - Punto de anclaje en \((5, 10)\), pendiente requerida \(m = 0.8\):  
     \[
     y - 10 = 0.8(x - 5) \implies y = 0.8x + 6
     \]  

**Ejercicio rápido:**  
Hallar la ecuación de la recta que pasa por \((-1, 3)\) con \(m = 4\).  
**Solución:** \(y - 3 = 4(x + 1) \implies y = 4x + 7\).  

---

### **4. Actividad Práctica (25 minutos)**  
**Problema 1 (Individual):**  
*Un cable subacuático une dos puntos: \(A(-2, 5)\) y \(B(4, -7)\).*  
a) Calcular pendiente y ángulo de inclinación.  
b) Escribir ecuación general.  

**Solución:**  
a) \(m = \frac{-7 - 5}{4 - (-2)} = \frac{-12}{6} = -2\), \(\theta = \arctan(-2) \approx 116.57^\circ\).  
b) \(y - 5 = -2(x + 2) \implies 2x + y - 1 = 0\).  

**Problema 2 (Grupal):**  
*Diseñar una ruta recta para fibra óptica que pase por:*  
- Torre 1: \((10, 20)\)  
- Torre 2: \((50, 40)\)  
- Torre 3: ¿Debe estar alineada? Verificar con ecuación.  

**Solución:**  
- Pendiente \(m = \frac{40-20}{50-10} = 0.5\).  
- Ecuación: \(y - 20 = 0.5(x - 10) \implies y = 0.5x + 15\).  
- Para Torre 3 en \((70, 50)\): \(50 \overset{?}{=} 0.5(70) + 15 = 50\). ¡Sí está alineada!  

---

### **5. Tarea y Cierre**  
**Tarea (Moodle):**  
1. Calcular pendiente entre torres en \((12.345, -67.890)\) y \((12.350, -67.885)\).  
2. Hallar ecuación de recta que pasa por \((0, 0)\) con \(\theta = 60^\circ\).  
3. Investigar: ¿Cómo se usa la pendiente en el tendido de redes 5G?  

**Recursos:**  
- Software: [Desmos](https://www.desmos.com) para graficar rectas.  
- Video: "Pendiente en Telecomunicaciones" (5 min).  

---  
**Nota:** Todos los ejemplos simulan escenarios reales, vinculando matemáticas con aplicaciones profesionales.