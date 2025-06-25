**Clase 4: Elipse e Hipérbola**  
**Duración:** 90 minutos  
**Objetivos:**  
1. Definir elipses e hipérbolas mediante ecuaciones.  
2. Identificar elementos clave: focos, vértices, ejes.  
3. Aplicar en órbitas satelitales y sistemas de navegación.  

---

### **1. Elipse (40 minutos)**  
#### **Definición:**  
Conjunto de puntos cuya suma de distancias a dos puntos fijos (**focos**) es constante.  

#### **Ecuaciones Estándar:**  
| **Orientación** | **Ecuación** | **Elementos** |  
|-----------------|--------------|---------------|  
| Eje mayor horizontal | \(\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = 1\) | \(a > b\) |  
| Eje mayor vertical | \(\frac{(x-h)^2}{b^2} + \frac{(y-k)^2}{a^2} = 1\) | \(a > b\) |  

**Elementos Clave:**  
- **Centro:** \((h, k)\).  
- **Vértices:** \((h \pm a, k)\) (horizontal) o \((h, k \pm a)\) (vertical).  
- **Focos:** \((h \pm c, k)\) o \((h, k \pm c)\), donde \(c = \sqrt{a^2 - b^2}\).  
- **Excentricidad:** \(e = \frac{c}{a}\) (\(0 < e < 1\)).  

#### **Ejemplos:**  
1. **Elipse horizontal:**  
   - \(\frac{x^2}{25} + \frac{y^2}{9} = 1\)  
     - Centro: \((0, 0)\).  
     - \(a = 5\), \(b = 3\).  
     - Vértices: \((\pm 5, 0)\).  
     - Focos: \((\pm \sqrt{25-9}, 0) = (\pm 4, 0)\).  
     - \(e = \frac{4}{5} = 0.8\).  

2. **Elipse vertical:**  
   - \(\frac{(x-2)^2}{9} + \frac{(y+1)^2}{16} = 1\)  
     - Centro: \((2, -1)\).  
     - \(a = 4\), \(b = 3\).  
     - Vértices: \((2, -1 \pm 4) = (2, 3)\) y \((2, -5)\).  
     - Focos: \((2, -1 \pm \sqrt{16-9}) = (2, -1 \pm \sqrt{7})\).  

#### **Aplicación en Telecomunicaciones:**  
- **Órbitas satelitales:**  
  *Un satélite sigue una órbita elíptica con centro en \((0,0)\), vértice en \((7000, 0)\) km y foco en \((3000, 0)\) km:*  
  \[
  a = 7000, \quad c = 3000 \quad \Rightarrow \quad b = \sqrt{7000^2 - 3000^2} \approx 6324.56
  \]
  \[
  \text{Ecuación: } \frac{x^2}{49,000,000} + \frac{y^2}{40,000,000} = 1
  \]

---

### **2. Hipérbola (45 minutos)**  
#### **Definición:**  
Conjunto de puntos donde la diferencia absoluta de distancias a dos puntos fijos (**focos**) es constante.  

#### **Ecuaciones Estándar:**  
| **Orientación** | **Ecuación** | **Elementos** |  
|-----------------|--------------|---------------|  
| Eje transversal horizontal | \(\frac{(x-h)^2}{a^2} - \frac{(y-k)^2}{b^2} = 1\) | |  
| Eje transversal vertical | \(\frac{(y-k)^2}{a^2} - \frac{(x-h)^2}{b^2} = 1\) | |  

**Elementos Clave:**  
- **Centro:** \((h, k)\).  
- **Vértices:** \((h \pm a, k)\) (horizontal) o \((h, k \pm a)\) (vertical).  
- **Focos:** \((h \pm c, k)\) o \((h, k \pm c)\), donde \(c = \sqrt{a^2 + b^2}\).  
- **Asíntotas:** \(y - k = \pm \frac{b}{a}(x - h)\) (horizontal).  

#### **Ejemplos:**  
1. **Hipérbola horizontal:**  
   - \(\frac{x^2}{16} - \frac{y^2}{9} = 1\)  
     - Centro: \((0, 0)\).  
     - \(a = 4\), \(b = 3\).  
     - Vértices: \((\pm 4, 0)\).  
     - Focos: \((\pm \sqrt{16+9}, 0) = (\pm 5, 0)\).  
     - Asíntotas: \(y = \pm \frac{3}{4}x\).  

2. **Hipérbola vertical:**  
   - \(\frac{(y-3)^2}{25} - \frac{(x+2)^2}{36} = 1\)  
     - Centro: \((-2, 3)\).  
     - \(a = 5\), \(b = 6\).  
     - Vértices: \((-2, 3 \pm 5) = (-2, 8)\) y \((-2, -2)\).  
     - Focos: \((-2, 3 \pm \sqrt{25+36}) = (-2, 3 \pm \sqrt{61})\).  

#### **Aplicación Técnica:**  
- **Sistema LORAN (navegación):**  
  *Dos estaciones en \((-150, 0)\) y \((150, 0)\). Un barco detecta diferencia de distancia de 200 km:*  
  \[
  2a = 200 \quad \Rightarrow \quad a = 100, \quad c = 150 \quad \Rightarrow \quad b = \sqrt{150^2 - 100^2} \approx 111.8
  \]
  \[
  \text{Ecuación: } \frac{x^2}{10,000} - \frac{y^2}{12,500} = 1
  \]

---

### **3. Actividad Práctica (5 minutos)**  
**Problema:**  
*Una órbita satelital elíptica tiene centro en \((0,0)\), vértice en \((7000, 0)\) km y foco en \((3000, 0)\) km. Hallar excentricidad.*  

**Solución:**  
\[
e = \frac{c}{a} = \frac{3000}{7000} \approx 0.4286
\]

---

### **4. Tarea y Recursos**  
**Tarea (Moodle):**  
1. Dada \(\frac{(x-1)^2}{36} + \frac{(y+2)^2}{16} = 1\), identificar centro, vértices y focos.  
2. Para \(\frac{y^2}{25} - \frac{x^2}{144} = 1\), hallar centro, focos y asíntotas.  
3. Problema aplicado:  
   *"Dos antenas LORAN están separadas 300 km. Un barco detecta diferencia de distancias de 200 km. Si las antenas están en \((-150, 0)\) y \((150, 0)\), escribir la ecuación de la hipérbola."*  

**Recursos:**  
- [Simulador GeoGebra: Cónicas](https://www.geogebra.org/m/DRHKY3N7)  
- Video: "Hipérbolas en Sistemas de Navegación" (5 min).  

---

**Nota:** Los ejemplos integran aplicaciones reales en telecomunicaciones, vinculando conceptos abstractos con tecnología de navegación y satélites. La elipse se aplica a órbitas, mientras la hipérbola se usa en sistemas de localización como LORAN.