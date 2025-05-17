**Clase 3: MCD, MCM y Notación Científica**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Calcular MCD y MCM para optimización de recursos.  
2. Dominar notación científica para magnitudes técnicas.  
3. Aplicar estos conceptos a problemas de telecomunicaciones.  

---

### **1. Introducción (10 minutos)**  
**Contexto en Telecomunicaciones:**  
"En redes de comunicación, necesitamos sincronizar dispositivos (MCM) y dividir frecuencias eficientemente (MCD). Además, trabajamos con magnitudes muy grandes (GHz) o pequeñas (nW), donde la notación científica es esencial."

**Ejemplo motivador:**  
*"Si dos antenas emiten señales cada 15 y 20 segundos respectivamente, ¿cada cuánto tiempo coincidirán sus emisiones?"*

---

### **2. Máximo Común Divisor - MCD (20 minutos)**  
**Definición:**  
El mayor número que divide exactamente a dos o más números.  

**Métodos de cálculo:**  
1. **Descomposición en factores primos:**  
   - Ejemplo: Hallar MCD de 36 y 24  
     - 36 = 2² × 3²  
     - 24 = 2³ × 3¹  
     - MCD = 2² × 3¹ = 12  

2. **Algoritmo de Euclides:**  
   - 36 ÷ 24 = 1 con resto 12  
   - 24 ÷ 12 = 2 con resto 0 → MCD = 12  

**Ejercicios:**  
1. Calcular MCD de 48 y 60 (Solución: 12)  
2. MCD de 75 y 100 (Solución: 25)  

**Aplicación técnica:**  
*División de ancho de banda:*  
"Si tenemos 24 MHz y 36 MHz, el mayor ancho común para subcanales es 12 MHz (MCD)."

---

### **3. Mínimo Común Múltiplo - MCM (20 minutos)**  
**Definición:**  
El menor número que es múltiplo de dos o más números.  

**Método de cálculo:**  
- Usando factores primos (tomar los mayores exponentes):  
  - MCM de 36 y 24 = 2³ × 3² = 72  

**Ejercicios:**  
1. Calcular MCM de 8 y 12 (Solución: 24)  
2. MCM de 15 y 20 (Solución: 60)  

**Caso práctico:**  
*Sincronización de paquetes de datos:*  
"Si un router envía paquetes cada 15 ms y otro cada 20 ms, coincidirán cada 60 ms (MCM)."

---

### **4. Notación Científica (25 minutos)**  
**Definición:**  
Expresar números como:  
\[ a \times 10^n \quad \text{donde} \quad 1 \leq a < 10 \]  

**Conversión:**  
1. 3,500 = 3.5 × 10³  
2. 0.0042 = 4.2 × 10⁻³  

**Operaciones:**  
1. Multiplicación:  
   \[ (2 \times 10^3) \times (3 \times 10^4) = 6 \times 10^7 \]  
2. División:  
   \[ \frac{8 \times 10^5}{2 \times 10^2} = 4 \times 10^3 \]  

**Ejercicios:**  
1. Expresar 0.00078 en notación científica (Solución: 7.8 × 10⁻⁴)  
2. Calcular: \( \frac{5 \times 10^8}{2.5 \times 10^3} \) (Solución: 2 × 10⁵)  

**Aplicación técnica:**  
*Frecuencias en telecomunicaciones:*  
- 5 GHz = 5 × 10⁹ Hz  
- Señal de 0.000000045 segundos = 45 × 10⁻⁹ s = 45 ns  

---

### **5. Actividad Integradora (20 minutos)**  
**Problema 1 (MCD/MCM):**  
*"Dos satélites orbitan cada 90 y 120 minutos. ¿Cada cuántas horas coincidirán en el mismo punto?"*  
- Solución: MCM de 90 y 120 = 360 minutos = 6 horas  

**Problema 2 (Notación científica):**  
*"La velocidad de la luz es ~300,000 km/s. Expresarla en m/s."*  
- Solución: 3 × 10⁸ m/s  

**Problema 3 (Combinado):**  
*"Un procesador ejecuta tareas cada 12 μs y otro cada 18 μs. ¿Cada cuánto tiempo se sincronizan?"*  
- Solución: MCM de 12 y 18 = 36 μs = 3.6 × 10⁻⁵ s  

---

### **6. Cierre y Tarea (5 minutos)**  
**Resumen visual:**  
| Concepto | Fórmula/Ejemplo | Aplicación |  
|----------|-----------------|------------|  
| MCD | MCD de 24 y 36 = 12 | División de frecuencias |  
| MCM | MCM de 15 y 20 = 60 | Sincronización |  
| Notación científica | 5 GHz = 5 × 10⁹ Hz | Magnitudes técnicas |  

**Tarea:**  
1. Calcular MCD de 84 y 105  
2. Convertir 0.00000025 a notación científica  
3. Problema aplicado: *"Si un servidor procesa datos cada 45 ms y otro cada 60 ms, ¿cada cuánto segundo coinciden?"*  

**Recursos adicionales:**  
- Calculadora científica con función de potencias de 10.  
- Tabla de prefijos métricos (nano, micro, mega, giga).  

--- 

Esta clase integra matemáticas fundamentales con aplicaciones directas en telecomunicaciones, utilizando ejemplos técnicos para reforzar el aprendizaje.