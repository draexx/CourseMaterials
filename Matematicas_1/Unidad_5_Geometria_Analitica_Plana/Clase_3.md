**Clase 3: Circunferencia y Parábola**  
**Duración:** 90 minutos  
**Objetivos:**  
1. Definir circunferencias y parábolas mediante ecuaciones.  
2. Relacionar con cobertura de antenas y diseño de reflectores.  
3. Resolver problemas técnicos en telecomunicaciones.  

---

### **1. Circunferencia (40 minutos)**  
#### **Definición:**  
Conjunto de puntos equidistantes de un centro \((h, k)\). La distancia fija es el radio \(r\).  

#### **Ecuación Canónica:**  
\[
\boxed{(x - h)^2 + (y - k)^2 = r^2}
\]  

#### **Elementos Clave:**  
- **Centro \((h, k)\):** Punto de referencia.  
- **Radio \(r\):** Distancia al centro.  

#### **Ejemplos:**  
1. **Básico:**  
   - Centro \((2, -3)\), radio \(4\):  
   \[
   (x - 2)^2 + (y + 3)^2 = 16
   \]  
   - Punto de prueba \((5, -3)\):  
     \[
     (5-2)^2 + (-3+3)^2 = 9 < 16 \quad \text{(Dentro del área)}
     \]  

2. **Conversión a forma canónica:**  
   - Dada ecuación general: \(x^2 + y^2 - 6x + 4y - 12 = 0\)  
     - Completar cuadrados:  
       \[
       (x^2 - 6x + 9) + (y^2 + 4y + 4) = 12 + 9 + 4
       \]  
       \[
       (x - 3)^2 + (y + 2)^2 = 25
       \]  
     - Centro: \((3, -2)\), Radio: \(5\).  

#### **Aplicación en Telecomunicaciones:**  
- **Cobertura de antena:**  
  - Antena en \((5, 4)\) con alcance \(8\) km:  
    \[
    (x - 5)^2 + (y - 4)^2 = 64
    \]  
  - Verificar si un cliente en \((10, 10)\) tiene cobertura:  
    \[
    \sqrt{(10-5)^2 + (10-4)^2} = \sqrt{25 + 36} = \sqrt{61} \approx 7.81 < 8 \quad \text{(Sí)}
    \]  

---

### **2. Parábola (45 minutos)**  
#### **Definición:**  
Conjunto de puntos equidistantes de un foco \((F)\) y una recta directriz \((d)\).  

#### **Ecuaciones Estándar:**  
| **Orientación** | **Ecuación** | **Foco** | **Directriz** |  
|-----------------|--------------|----------|---------------|  
| Vertical (↑↓) | \((x - h)^2 = 4p(y - k)\) | \((h, k + p)\) | \(y = k - p\) |  
| Horizontal (→←) | \((y - k)^2 = 4p(x - h)\) | \((h + p, k)\) | \(x = h - p\) |  

#### **Elementos Clave:**  
- **Vértice \((h, k)\):** Punto de inflexión.  
- **Parámetro \(p\):** Distancia entre vértice y foco.  
- **Lado recto:** Longitud \(|4p|\).  

#### **Ejemplos:**  
1. **Parábola vertical:**  
   - Vértice \((0, 0)\), foco \((0, 2)\) → \(p = 2\):  
     \[
     x^2 = 8y
     \]  
     - Directriz: \(y = -2\).  

2. **Parábola horizontal:**  
   - Vértice \((3, -1)\), foco \((1, -1)\) → \(p = -2\) (abre a izquierda):  
     \[
     (y + 1)^2 = -8(x - 3)
     \]  

#### **Aplicación Técnica: Antenas Parabólicas**  
- **Diseño de reflector:**  
  - Foco en \((0, 0.5)\), vértice \((0, 0)\) → \(p = 0.5\):  
    \[
    x^2 = 4 \times 0.5 \times y \implies x^2 = 2y
    \]  
  - Calcular profundidad a \(1\) m del vértice (\(x = 1\)):  
    \[
    1^2 = 2y \implies y = 0.5 \text{ m}
    \]  

---

### **3. Actividad Práctica (5 minutos)**  
**Problema:**  
*Una antena parabólica tiene foco en \((0, 1.5)\) y vértice en \((0, 0)\).*  
1. Hallar su ecuación.  
2. Calcular su profundidad en \(x = 2\) m.  

**Solución:**  
1. \(p = 1.5 \quad \Rightarrow \quad x^2 = 6y\).  
2. \(2^2 = 6y \implies y = \frac{4}{6} \approx 0.67 \text{ m}\).  

---

### **4. Tarea y Recursos**  
**Tarea (Moodle):**  
1. Convertir \(x^2 + y^2 - 10x + 6y + 30 = 0\) a forma canónica.  
2. Dada \(y^2 = 16x\), hallar foco y directriz.  
3. Problema aplicado:  
   *"Una torre en \((3, -2)\) cubre un radio de \(7\) km. ¿Un edificio en \((10, 3)\) recibe señal?"*  

**Recursos:**  
- [Simulador GeoGebra - Cónicas](https://www.geogebra.org/m/DRHKY3N7)  
- Video: "Antenas Parabólicas: Enfoque de Señales" (4 min).  

---

**Nota:** Todos los ejemplos incluyen aplicaciones reales en telecomunicaciones para reforzar la relevancia profesional. Las parábolas se enfocan en diseño de antenas, y las circunferencias en modelado de cobertura.