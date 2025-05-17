**Clase 2: Potenciación, Radicación y Sistema Métrico Decimal**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Dominar propiedades de potencias y raíces.  
2. Convertir unidades en el sistema métrico decimal.  
3. Aplicar estos conceptos a problemas técnicos en telecomunicaciones.  

---

### **1. Repaso y Contextualización (10 minutos)**  
**Conexión con la Clase Anterior:**  
"En telecomunicaciones, el cálculo de potencias de señal y la conversión de unidades son esenciales para diseñar redes eficientes. Hoy trabajaremos con estas herramientas."  

**Ejemplo motivador:**  
*"Si la potencia de una señal se cuadruplica cada 2 amplificadores, ¿cómo expresamos esto matemáticamente?"*  

---

### **2. Potenciación: Definiciones y Propiedades (25 minutos)**  
**Conceptos Clave:**  
- **Definición:** \( a^n = a \times a \times ... \times a \) (n veces).  
- **Exponente cero:** \( a^0 = 1 \) (para \( a \neq 0 \)).  
- **Exponente negativo:** \( a^{-n} = \frac{1}{a^n} \).  

**Propiedades Fundamentales:**  
1. \( a^m \times a^n = a^{m+n} \)  
2. \( \frac{a^m}{a^n} = a^{m-n} \)  
3. \( (a^m)^n = a^{m \times n} \)  
4. \( (a \times b)^n = a^n \times b^n \)  

**Ejemplos Resueltos:**  
1. \( 2^3 \times 2^5 = 2^{8} = 256 \)  
2. \( \frac{5^4}{5^2} = 5^{2} = 25 \)  
3. \( (3^2)^3 = 3^{6} = 729 \)  

**Aplicación Técnica:**  
*Cálculo de pérdida de señal en decibelios (dB):*  
\[
P_{final} = P_{inicial} \times 10^{-n/10}  
\]  
*Ejemplo:* Si una señal pierde 3 dB, \( n = 3 \):  
\[
P_{final} = P_{inicial} \times 10^{-0.3} \approx P_{inicial} \times 0.5  
\]  

---

### **3. Radicación: Conceptos y Operaciones (25 minutos)**  
**Definición:**  
\( \sqrt[n]{a} = b \) significa que \( b^n = a \).  

**Propiedades:**  
1. \( \sqrt[n]{a \times b} = \sqrt[n]{a} \times \sqrt[n]{b} \)  
2. \( \sqrt[n]{\frac{a}{b}} = \frac{\sqrt[n]{a}}{\sqrt[n]{b}} \)  
3. \( \sqrt[m]{\sqrt[n]{a}} = \sqrt[m \times n]{a} \)  

**Ejercicios Prácticos:**  
1. \( \sqrt{36} = 6 \)  
2. \( \sqrt[3]{8} = 2 \)  
3. Simplificar: \( \sqrt{50} = 5\sqrt{2} \)  

**Caso de Estudio:**  
*Cálculo de impedancia en circuitos:*  
\[
Z = \sqrt{R^2 + X^2}  
\]  
*Donde:*  
- \( R = \) Resistencia (Ohms)  
- \( X = \) Reactancia (Ohms)  

---

### **4. Sistema Métrico Decimal (20 minutos)**  
**Unidades Básicas:**  
| Magnitud | Unidad Base | Símbolo |  
|----------|-------------|---------|  
| Longitud | Metro | m |  
| Masa | Gramo | g |  
| Tiempo | Segundo | s |  

**Prefijos Comunes:**  
| Prefijo | Símbolo | Factor |  
|---------|---------|--------|  
| Kilo- | k | \( 10^3 \) |  
| Centi- | c | \( 10^{-2} \) |  
| Mili- | m | \( 10^{-3} \) |  
| Micro- | μ | \( 10^{-6} \) |  

**Ejercicios de Conversión:**  
1. 3 km = 3000 m  
2. 500 ms = 0.5 s  
3. 2500 MHz = 2.5 GHz  

**Aplicación en Telecomunicaciones:**  
*Ancho de banda de canales:*  
- 20 MHz = 20,000 kHz  
- 0.1 GHz = 100 MHz  

---

### **5. Actividad Integradora (15 minutos)**  
**Problema 1:**  
*Un amplificador aumenta la potencia de señal al cubo. Si la entrada es 2 mW, ¿cuál es la salida?*  
\[
P_{salida} = (2 \text{ mW})^3 = 8 \text{ mW}^3 \text{ (Nota: en práctica sería 8 mW por linealización)}
\]  

**Problema 2:**  
*Convertir 0.05 km a cm:*  
\[
0.05 \text{ km} = 50 \text{ m} = 5000 \text{ cm}
\]  

**Problema 3 (Desafío):**  
*Si la atenuación en un cable es \( \sqrt{16} \) dB/km, ¿cuánto se atenúa en 3 km?*  
\[
Atenuación = 4 \text{ dB/km} \times 3 \text{ km} = 12 \text{ dB}
\]  

---

### **6. Cierre y Tarea (5 minutos)**  
**Resumen Visual:**  
| Concepto | Fórmula | Ejemplo |  
|----------|---------|---------|  
| Potenciación | \( a^m \times a^n = a^{m+n} \) | \( 2^3 \times 2^2 = 32 \) |  
| Radicación | \( \sqrt[n]{a^n} = a \) | \( \sqrt[3]{27} = 3 \) |  
| Conversión | 1 km = 1000 m | 5 km = 5000 m |  

**Tarea:**  
1. Simplificar: \( (3^2 \times 3^4) \div 3^3 \)  
2. Convertir: 7500 μm a mm  
3. Problema aplicado: *"Si la potencia de una señal es \( \sqrt{81} \) mW, ¿cuál es su valor en lineal?"*  

**Recursos Adicionales:**  
- Calculadora científica para verificar ejercicios.  
- Tabla de prefijos métricos para consulta rápida.  

--- 

Esta clase combina fundamentos matemáticos con aplicaciones directas en telecomunicaciones, utilizando ejemplos técnicos para reforzar el aprendizaje.