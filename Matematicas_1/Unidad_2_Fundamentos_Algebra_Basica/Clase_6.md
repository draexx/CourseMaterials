**Clase 6: Aplicaciones del Álgebra en Informática**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Introducción y Repaso (15 minutos)**  
**Objetivo:**  
Revisar conceptos clave de la unidad y conectar el álgebra con problemas reales en informática.  

**Actividad de inicio:**  
- *Pregunta rápida:* "¿Cómo creen que se usa el álgebra en programación o diseño de algoritmos?"  
- Ejemplos breves:  
  - Fórmulas en hojas de cálculo (Excel).  
  - Cálculo de complejidad algorítmica (notación Big-O).  

---

### **2. Aplicaciones Prácticas del Álgebra (30 minutos)**  
#### **A. Optimización de Recursos**  
**Definición:**  
Uso de ecuaciones para maximizar o minimizar variables (ejemplo: memoria, tiempo de ejecución).  

**Ejemplo 1:**  
*"Un servidor puede procesar 500 solicitudes en 2 horas. Si cada solicitud adicional aumenta el tiempo un 0.1%, ¿cuántas solicitudes manejará en 3 horas?"*  
- **Planteamiento:**  
  \[
  T(n) = 2 + 0.001n \quad \text{(Tiempo para \(n\) solicitudes)}  
  \]  
  \[
  3 = 2 + 0.001n \Rightarrow n = 1000 \text{ solicitudes.}
  \]  

#### **B. Geometría Computacional**  
**Definición:**  
Álgebra para calcular distancias, áreas o intersecciones en gráficos 2D/3D.  

**Ejemplo 2:**  
*"Un juego necesita calcular si un punto \((x, y)\) está dentro de un círculo de radio 5 centrado en \((0,0)\)."*  
- **Fórmula:**  
  \[
  x^2 + y^2 \leq 25.
  \]  

#### **C. Criptografía**  
**Definición:**  
Ecuaciones modulares en algoritmos de encriptación (ejemplo: RSA).  

**Ejemplo 3 (Simplificado):**  
*"Si \(m^e \mod n = c\), y \(n = 15\), \(e = 3\), \(c = 9\), hallar \(m\)."*  
- **Solución por fuerza bruta:**  
  \(m = 3\) (porque \(3^3 = 27 \mod 15 = 9\)).  

---

### **3. Ejercicios Prácticos (30 minutos)**  
#### **Ejercicio Grupal (Optimización):**  
*"Una app de delivery tiene 2 repartidores. El primero hace 10 entregas en 4 horas; el segundo, 8 en 3 horas. ¿Cuántas entregas harán juntos en 6 horas?"*  
- **Solución:**  
  \[
  \text{Repartidor 1: } \frac{10}{4} = 2.5 \text{ entregas/hora.}  
  \]  
  \[
  \text{Repartidor 2: } \frac{8}{3} \approx 2.67 \text{ entregas/hora.}  
  \]  
  \[
  \text{Total: } (2.5 + 2.67) \times 6 \approx 31 \text{ entregas.}
  \]  

#### **Ejercicio Individual (Geometría):**  
*"Un píxel en \((3,4)\) debe moverse a la derecha hasta tocar la circunferencia \(x^2 + y^2 = 100\). ¿Cuál es su nueva posición?"*  
- **Solución:**  
  \[
  \text{Nuevo } x: \sqrt{100 - 4^2} = \sqrt{84} \approx 9.17 \Rightarrow (9.17, 4).
  \]  

---

### **4. Actividad Colaborativa (20 minutos)**  
**Problema Desafío:**  
*"Diseñen un algoritmo para calcular el costo óptimo de enviar paquetes, donde:*  
- *Cada paquete cuesta \$5 si pesa ≤1kg, \$8 si pesa ≤3kg, \$12 si pesa >3kg.*  
- *El presupuesto es \$100. ¿Cuántos paquetes de cada tipo se pueden enviar?"*  

**Solución Esperada:**  
- Sistema de inecuaciones:  
  \[
  5x + 8y + 12z \leq 100 \quad \text{(\(x, y, z\): cantidades de paquetes).}  
  \]  
- Soluciones posibles: \((20,0,0)\), \((0,12,0)\), etc.  

---

### **5. Cierre y Reflexión (5 minutos)**  
**Conclusiones:**  
- El álgebra es esencial para optimizar recursos, diseñar gráficos y proteger datos.  
- Invitar a investigar aplicaciones avanzadas (ejemplo: machine learning con matrices).  

**Tarea Final:**  
- Investigar cómo se usan las matrices en inteligencia artificial (ejemplo: redes neuronales).  

**Material Adicional:**  
- Código Python para resolver el problema de optimización:  
  ```python
  from scipy.optimize import linprog
  # Ejemplo simplificado
  ```  

--- 

Esta clase integra teoría, ejercicios aplicados y trabajo colaborativo para demostrar el poder del álgebra en la informática, cerrando la unidad con un enfoque práctico y motivador.