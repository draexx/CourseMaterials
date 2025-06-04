**Clase 1: Sistema Cartesiano y Distancias**  
**Duración:** 90 minutos  
**Objetivos:**  
1. Comprender el sistema cartesiano ortogonal.  
2. Calcular distancias y puntos medios.  
3. Aplicar en geolocalización de antenas.  

---

### **1. Sistema Cartesiano Ortogonal (25 minutos)**  
**Definiciones:**  
- **Plano cartesiano:** Sistema de coordenadas bidimensional con dos ejes perpendiculares.  
- **Eje X (abscisas):** Horizontal, positivo a la derecha del origen.  
- **Eje Y (ordenadas):** Vertical, positivo arriba del origen.  
- **Cuadrantes:**  
  - **I (+, +)** Ej: \((3, 4)\)  
  - **II (-, +)** Ej: \((-2, 5)\)  
  - **III (-, -)** Ej: \((-1, -3)\)  
  - **IV (+, -)** Ej: \((4, -2)\)  

**Ejemplos en Telecomunicaciones:**  
- *Torre A:* Coordenadas \((0, 0)\) (origen).  
- *Torre B:* Coordenadas \((5, 7)\) (Cuadrante I).  
- *Torre C:* Coordenadas \((-3, 6)\) (Cuadrante II).  

**Actividad:**  
Graficar antenas en \(D(0, 4)\) (eje Y) y \(E(-5, 0)\) (eje X).  

---

### **2. Distancia entre Puntos (30 minutos)**  
**Fórmula:**  
\[
\boxed{d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}}
\]  
**Explicación geométrica:**  
- Teorema de Pitágoras aplicado a los catetos \(\Delta x\) y \(\Delta y\).  

**Ejemplos:**  
1. **Caso básico:**  
   - Puntos \(A(1, 2)\) y \(B(4, 6)\):  
   \[
   d = \sqrt{(4-1)^2 + (6-2)^2} = \sqrt{9 + 16} = \sqrt{25} = 5 \text{ km}
   \]  
   *(Distancia entre dos antenas)*.  

2. **Caso con negativos:**  
   - Puntos \(P(-3, 1)\) y \(Q(2, -4)\):  
   \[
   d = \sqrt{(2 - (-3))^2 + (-4 - 1)^2} = \sqrt{25 + 25} = \sqrt{50} \approx 7.07 \text{ km}
   \]  

**Aplicación técnica:**  
- *Cálculo de interferencia:* Si dos antenas están a menos de 8 km, hay interferencia. ¿Interfieren las antenas en \((3, 1)\) y \((-2, 6)\)?  
  \[
  d = \sqrt{(-2-3)^2 + (6-1)^2} = \sqrt{25 + 25} = \sqrt{50} \approx 7.07 < 8 \quad \text{¡Sí interfieren!}
  \]  

---

### **3. Punto Medio (20 minutos)**  
**Fórmula:**  
\[
\boxed{M = \left( \frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2} \right)}
\]  
**Utilidad:**  
- Ubicar repetidores o nuevas antenas entre dos puntos existentes.  

**Ejemplos:**  
1. **Puntos en el mismo cuadrante:**  
   - Entre \(A(2, 4)\) y \(B(6, 10)\):  
   \[
   M = \left( \frac{2+6}{2}, \frac{4+10}{2} \right) = (4, 7)
   \]  

2. **Puntos en cuadrantes opuestos:**  
   - Entre \(C(-3, 5)\) y \(D(7, -1)\):  
   \[
   M = \left( \frac{-3+7}{2}, \frac{5+(-1)}{2} \right) = (2, 2)
   \]  

**Caso práctico:**  
- *Instalación de repetidor:* Punto medio entre torres en \((10.500, -75.200)\) y \((10.503, -75.205)\):  
\[
M = \left( \frac{10.500 + 10.503}{2}, \frac{-75.200 + (-75.205)}{2} \right) = (10.5015, -75.2025)
\]  

---

### **4. Actividad Integrada (15 minutos)**  
**Problema:**  
*"Tres torres de telecomunicaciones están en:*  
- *Torre 1: \((-2, 3)\)*  
- *Torre 2: \((4, -1)\)*  
- *Torre 3: \((0, 6)\)*  

1. Calcular la distancia entre Torre 1 y Torre 2.  
2. Hallar el punto medio entre Torre 2 y Torre 3.  
3. ¿La distancia Torre 1-Torre 3 es menor que 7 km?"  

**Soluciones:**  
1. \(d = \sqrt{(4 - (-2))^2 + (-1 - 3)^2} = \sqrt{36 + 16} = \sqrt{52} \approx 7.21 \text{ km}\)  
2. \(M = \left( \frac{4+0}{2}, \frac{-1+6}{2} \right) = (2, 2.5)\)  
3. \(d = \sqrt{(0 - (-2))^2 + (6 - 3)^2} = \sqrt{4 + 9} = \sqrt{13} \approx 3.61 < 7 \quad \text{Sí}\)  

---

### **5. Tarea y Recursos**  
**Tarea:**  
1. Calcular distancia entre antenas en \((12.345, -67.890)\) y \((12.350, -67.885)\).  
2. Hallar punto medio entre \((-5.5, 3.2)\) y \((2.3, -4.8)\).  
3. Investigar: ¿Cómo se usa el sistema cartesiano en el GPS?  

**Recursos:**  
- Software: [GeoGebra](https://www.geogebra.org) para practicar coordenadas.  
- Video: "Geolocalización de Antenas" (3 min).  

---  
**Nota:** Todos los ejemplos simulan situaciones reales en telecomunicaciones, reforzando la utilidad práctica de los conceptos.