### **Clase 3: Logaritmos Algebraicos - Teoría Profunda y Aplicaciones Prácticas**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Comprender el concepto de logaritmo como operación inversa a la potenciación.  
2. Dominar las propiedades algebraicas de los logaritmos.  
3. Resolver ecuaciones logarítmicas y exponenciales complejas.  
4. Aplicar logaritmos en problemas de ciencias e ingeniería.  

---

## **1. Definición Rigurosa de Logaritmo (20 minutos)**  
### **1.1 Concepto Fundamental**  
Dados \( b > 0 \), \( b \neq 1 \) y \( a > 0 \), el logaritmo se define como:  
\[
\log_b a = x \iff b^x = a
\]  
- \( b \): Base del logaritmo  
- \( a \): Argumento (o antilogaritmo)  
- \( x \): Exponente al que debe elevarse \( b \) para obtener \( a \)

**Ejemplo Existencial:**  
\[
\log_2 8 = 3 \quad \text{porque} \quad 2^3 = 8
\]

### **1.2 Casos Especiales y Límites**  
| **Caso**               | **Expresión**           | **Explicación**                     |  
|------------------------|-------------------------|-------------------------------------|  
| Logaritmo de 1          | \( \log_b 1 = 0 \)      | Porque \( b^0 = 1 \) ∀ \( b \neq 0 \) |  
| Logaritmo de la base    | \( \log_b b = 1 \)      | Pues \( b^1 = b \)                  |  
| Logaritmo de 0          | \( \log_b 0 \) = Indef. | No existe \( x \) tal que \( b^x = 0 \) |  
| Base \( b = e \)        | \( \ln a \)             | Logaritmo natural (base \( e \))    |  

**Ejemplo Límite:**  
\[
\lim_{x \to 0^+} \log_{10} x = -\infty
\]

---

## **2. Propiedades Algebraicas (Demostraciones Incluidas)**  
### **2.1 Teorema del Producto**  
\[
\log_b (M \cdot N) = \log_b M + \log_b N
\]  
**Demostración:**  
Sean \( x = \log_b M \), \( y = \log_b N \). Entonces:  
\[
b^{x+y} = b^x \cdot b^y = M \cdot N \implies \log_b (M \cdot N) = x + y
\]

### **2.2 Teorema del Cociente**  
\[
\log_b \left( \frac{M}{N} \right) = \log_b M - \log_b N
\]  
**Ejemplo:**  
\[
\log_5 \left( \frac{125}{25} \right) = \log_5 125 - \log_5 25 = 3 - 2 = 1
\]

### **2.3 Teorema de la Potencia**  
\[
\log_b (M^k) = k \cdot \log_b M
\]  
**Aplicación:**  
Simplificar \( \log_3 \sqrt{81} \):  
\[
\log_3 81^{1/2} = \frac{1}{2} \log_3 81 = \frac{1}{2} \cdot 4 = 2
\]

---

## **3. Cambio de Base y Fórmulas Clave**  
### **3.1 Fórmula de Cambio de Base**  
\[
\log_b a = \frac{\log_k a}{\log_k b} \quad \text{(para cualquier } k > 0, k \neq 1)
\]  
**Ejemplo Numérico:**  
Calcular \( \log_2 5 \) usando logaritmos naturales:  
\[
\log_2 5 = \frac{\ln 5}{\ln 2} \approx \frac{1.6094}{0.6931} \approx 2.3219
\]

### **3.2 Identidad Inversa**  
\[
b^{\log_b a} = a \quad \text{y} \quad \log_b (b^x) = x
\]  
**Aplicación en Ecuaciones:**  
Resolver \( 3^{\log_3 7} = x \implies x = 7 \).

---

## **4. Ejercicios Resueltos Paso a Paso**  
### **4.1 Ecuaciones Logarítmicas**  
**Problema 1:**  
Resolver \( \log_2 (x + 3) + \log_2 x = 3 \).  
**Solución:**  
1. Combinar logaritmos:  
   \[
   \log_2 [x(x + 3)] = 3
   \]  
2. Convertir a forma exponencial:  
   \[
   x(x + 3) = 2^3 \implies x^2 + 3x - 8 = 0
   \]  
3. Resolver la cuadrática:  
   \[
   x = \frac{-3 \pm \sqrt{41}}{2} \quad (\text{Solo válida } x > 0)
   \]

**Problema 2:**  
Resolver \( \log(x-1) - \log(x+1) = 1 \) (base 10 implícita).  
**Solución:**  
1. Aplicar cociente:  
   \[
   \log \left( \frac{x-1}{x+1} \right) = 1
   \]  
2. Convertir a exponencial:  
   \[
   \frac{x-1}{x+1} = 10 \implies x = -\frac{11}{9} \quad (\text{No válido, dominio})
   \]  
   **Conclusión:** No hay solución real.

---

## **5. Aplicaciones en Ciencias e Ingeniería**  
### **5.1 Escalas Logarítmicas (Decibelios y Richter)**  
- **Fórmula de Decibelios:**  
  \[
  L = 10 \log_{10} \left( \frac{I}{I_0} \right) \quad (I_0 = 10^{-12} \text{ W/m}^2)
  \]  
  **Ejemplo:**  
  Si \( I = 10^{-5} \text{ W/m}^2 \), calcular \( L \):  
  \[
  L = 10 \log_{10} (10^7) = 70 \text{ dB}
  \]

### **5.2 Crecimiento Exponencial (Biología y Finanzas)**  
- **Modelo de Crecimiento:**  
  \[
  N(t) = N_0 e^{kt} \implies t = \frac{1}{k} \ln \left( \frac{N(t)}{N_0} \right)
  \]  
  **Ejemplo:**  
  Si una bacteria se duplica cada 2 horas (\( k = \ln 2/2 \)), ¿cuánto tarda en crecer 10 veces?  
  \[
  t = \frac{2}{\ln 2} \ln 10 \approx 6.64 \text{ horas}
  \]

---

## **6. Ejercicios de Desafío**  
### **6.1 Problema Integrador**  
Simplificar:  
\[
\log_2 48 - \frac{1}{2} \log_2 9 + \log_2 \sqrt[3]{2}
\]  
**Solución:**  
\[
= \log_2 \left( \frac{48 \cdot 2^{1/3}}{9^{1/2}} \right) = \log_2 \left( \frac{48 \cdot 2^{1/3}}{3} \right) = \log_2 (16 \cdot 2^{1/3}) = \log_2 (2^{4 + 1/3}) = \frac{13}{3}
\]

### **6.2 Demostración Teórica**  
Probar que:  
\[
\frac{\log_a b}{\log_c d} = \frac{\log_a d}{\log_c b}
\]  
*Hint:* Usar cambio de base en ambos lados.

---

## **7. Errores Comunes y Cómo Evitarlos**  
| **Error**               | **Corrección**                    | **Ejemplo**                    |  
|--------------------------|-----------------------------------|--------------------------------|  
| \( \log_b (M + N) \neq \log_b M + \log_b N \) | Usar propiedades correctas | \( \log(10 + 10) \neq 2 \) |  
| \( \log_b (-a) \) = Indefinido | Restringir dominio a \( a > 0 \) | \( \log_2 (-8) \) → No existe |  
| Confundir \( \log_b (M^k) \) con \( (\log_b M)^k \) | Revisar notación | \( \log_3 9^2 = 2 \log_3 9 = 4 \) ≠ \( (\log_3 9)^2 = 4 \) (caso particular) |

---

## **8. Recursos Visuales y Herramientas**  
1. **Gráfica de Funciones Logarítmicas:**  
   Comparar \( y = \log_2 x \) vs \( y = \ln x \) vs \( y = \log_{0.5} x \).  
2. **Calculadora Científica:**  
   Uso de teclas `LOG` (base 10) y `LN` (base \( e \)).  

---

## **9. Evaluación de Comprensión**  
### **Preguntas Teóricas:**  
1. ¿Por qué no existe \( \log_b 0 \)?  
2. Demuestre que \( \log_b \left( \frac{1}{a} \right) = -\log_b a \).  

### **Problema Práctico:**  
En química, el pH se define como \( \text{pH} = -\log [H^+] \). Si \( [H^+] = 3.2 \times 10^{-5} \), calcule el pH.  
**Solución:**  
\[
\text{pH} = -\log (3.2 \times 10^{-5}) \approx 4.49
\]

---

Esta clase integra teoría rigurosa con aplicaciones multidisciplinarias, preparando a los estudiantes para cálculo avanzado y modelado científico.