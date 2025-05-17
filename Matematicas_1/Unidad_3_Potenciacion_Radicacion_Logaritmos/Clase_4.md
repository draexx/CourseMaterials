### **Clase 4: Ecuaciones Exponenciales y Logarítmicas - Dominio Completo**

#### **1. Definiciones Ampliadas y Fundamentos Teóricos**

**1.1 Ecuaciones Exponenciales (Concepto Profundo)**
Son ecuaciones donde la incógnita aparece en el exponente. Forma general:
\[ a^{f(x)} = b^{g(x)} \]
- *Caso especial*: Cuando \( a = b \), se resuelve igualando exponentes:
\[ f(x) = g(x) \]

**Teorema de unicidad**: Para \( a > 0 \), \( a \neq 1 \), si \( a^x = a^y \) entonces \( x = y \).

**Ejemplo existencial**:
\[ 3^{2x-1} = 27 \implies 3^{2x-1} = 3^3 \implies 2x-1 = 3 \implies x = 2 \]

**1.2 Ecuaciones Logarítmicas (Definición Rigurosa)**
Ecuaciones donde la incógnita está afectada por un logaritmo. Forma canónica:
\[ \log_b f(x) = g(x) \]
- *Condición de existencia*: \( f(x) > 0 \) y \( b > 0 \), \( b \neq 1 \)

**Propiedad biyectiva**: Para \( b > 0 \), \( b \neq 1 \):
\[ \log_b x = \log_b y \iff x = y \]

#### **2. Métodos de Resolución con Demostraciones**

**2.1 Método de Igualación de Bases**
*Teorema*: Si \( a^{f(x)} = a^{g(x)} \), entonces \( f(x) = g(x) \).

**Ejemplo avanzado**:
Resolver \( 16^{x-1} = 8^{2x+1} \)
1. Convertir a base común (2):
\[ (2^4)^{x-1} = (2^3)^{2x+1} \]
2. Simplificar exponentes:
\[ 4(x-1) = 3(2x+1) \]
3. Resolver:
\[ x = -3.5 \]

**2.2 Método de Logaritmización**
*Teorema*: Para \( a, b > 0 \), \( a \neq 1 \):
\[ a^{f(x)} = b \implies f(x) = \log_a b \]

**Ejemplo complejo**:
Resolver \( 5^{x-2} = 7 \)
1. Aplicar logaritmo natural:
\[ \ln(5^{x-2}) = \ln7 \]
2. Usar propiedad de logaritmos:
\[ (x-2)\ln5 = \ln7 \]
3. Despejar:
\[ x = 2 + \frac{\ln7}{\ln5} \approx 3.209 \]

#### **3. Casos Especiales y Soluciones No Triviales**

**3.1 Ecuaciones Exponenciales-Logarítmicas Mixtas**
Forma general:
\[ f(x)^{g(x)} = h(x) \]

**Ejemplo resuelto**:
Resolver \( x^{\log x} = 10^4 \)
1. Aplicar logaritmo decimal:
\[ \log x \cdot \log x = 4 \]
2. Simplificar:
\[ (\log x)^2 = 4 \]
3. Soluciones:
\[ \log x = 2 \implies x = 100 \]
\[ \log x = -2 \implies x = 0.01 \]

**3.2 Ecuaciones con Soluciones Extraneas**
**Ejemplo crítico**:
Resolver \( \log_3(x^2 - 4) = \log_3(3x) \)
1. Igualar argumentos:
\[ x^2 - 4 = 3x \]
2. Resolver cuadrática:
\[ x = 4 \text{ o } x = -1 \]
3. Verificar dominio:
\[ x = -1 \text{ no válido (log(negativo))} \]

#### **4. Aplicaciones Avanzadas en Ciencias**

**4.1 Modelado de Crecimiento Bacteriano**
Ecuación:
\[ N(t) = N_0 e^{kt} \]
**Problema**: Si una colonia bacteriana crece de 100 a 1000 en 2 horas, hallar \( k \).

**Solución**:
1. Plantear ecuación:
\[ 1000 = 100e^{2k} \]
2. Simplificar:
\[ 10 = e^{2k} \]
3. Resolver:
\[ k = \frac{\ln10}{2} \approx 1.151 \text{ h}^{-1} \]

**4.2 Decaimiento Radioactivo (Carbono-14)**
Ecuación:
\[ A(t) = A_0 e^{-0.000121t} \]
**Problema**: Un fósil tiene el 25% de carbono-14 original. Estimar su edad.

**Solución**:
1. Plantear:
\[ 0.25A_0 = A_0 e^{-0.000121t} \]
2. Simplificar:
\[ \ln0.25 = -0.000121t \]
3. Resultado:
\[ t \approx 11,460 \text{ años} \]

#### **5. Ejercicios de Alta Complejidad con Soluciones**

**5.1 Sistema de Ecuaciones Exponenciales**
Resolver:
\[
\begin{cases}
2^x \cdot 3^y = 72 \\
2^y \cdot 3^x = 108
\end{cases}
\]

**Solución**:
1. Tomar logaritmos naturales:
\[
\begin{cases}
x\ln2 + y\ln3 = \ln72 \\
y\ln2 + x\ln3 = \ln108
\end{cases}
\]
2. Resolver sistema lineal:
\[ x = 2, y = 3 \]

**5.2 Ecuación Logarítmica Compuesta**
Resolver:
\[ \log_2(x) + \log_x(4) = 3 \]

**Solución**:
1. Cambiar base:
\[ \log_2x + \frac{2}{\log_2x} = 3 \]
2. Sustitución \( y = \log_2x \):
\[ y + \frac{2}{y} = 3 \]
3. Resolver:
\[ y = 1 \implies x = 2 \]
\[ y = 2 \implies x = 4 \]

#### **6. Errores Comunes y Validación de Soluciones**

**6.1 Error de Dominio Clásico**
Ecuación:
\[ \log_5(x^2 - 5x) = 1 \]
**Solución incorrecta**:
\[ x^2 - 5x = 5 \implies x = \frac{5 \pm \sqrt{45}}{2} \]
**Validación**:
Ambas soluciones deben cumplir \( x^2 - 5x > 0 \). Solo \( x = \frac{5 + 3\sqrt{5}}{2} \) es válida.

**6.2 Error de Presunción de Linealidad**
**Falso teorema**:
\[ \log_b(x + y) \neq \log_bx + \log_by \]
**Contraejemplo**:
\[ \log_{10}(10 + 10) = \log_{10}20 \approx 1.301 \]
\[ \log_{10}10 + \log_{10}10 = 2 \]

#### **7. Herramientas Computacionales y Gráficas**

**7.1 Uso de Software para Verificación**
- *Wolfram Alpha*: Para comprobación de soluciones complejas
- *Desmos*: Visualización de funciones exponenciales/logarítmicas

**7.2 Análisis Gráfico**
Ejemplo: Intersección de \( y = 2^x \) con \( y = \log_2x \) muestra que no hay soluciones reales.

#### **8. Problemas de Olimpiadas Matemáticas**

**8.1 Problema IMO 1972**
Resolver:
\[ \log_4(x^2 - 1) = \log_4(x - 1)^2 + \frac{1}{2} \]

**Solución clave**:
1. Unificar logaritmos:
\[ \log_4\left(\frac{x^2 - 1}{(x - 1)^2}\right) = \frac{1}{2} \]
2. Simplificar:
\[ \frac{x + 1}{x - 1} = 2 \]
3. Solución:
\[ x = 3 \]

#### **9. Ejercicios Propuestos con Respuestas**

| **Tipo**                | **Ejercicio**                              | **Respuesta**          |
|-------------------------|-------------------------------------------|------------------------|
| Exponencial pura        | \( 5^{2x} - 6 \cdot 5^x + 5 = 0 \)        | \( x = 0, 1 \)         |
| Logarítmica compuesta   | \( \log(\log x) = 1 \)                    | \( x = 10^{10} \)      |
| Mixta                   | \( x^{1/\log x} = 10 \)                   | \( x = 10^k \) (k≠1)   |
| Aplicación física       | Modelo \( y = 2e^{-0.3t} \), hallar t cuando y=0.5 | \( t \approx 5.03 \) |

#### **10. Demostraciones Teóricas Avanzadas**

**10.1 Irracionalidad de \( \log_2 3 \)**
*Demostración por contradicción*:
1. Suponer \( \log_2 3 = \frac{p}{q} \) con \( p,q \in \mathbb{Z}^+ \)
2. Entonces \( 2^{p/q} = 3 \implies 2^p = 3^q \)
3. Absurdo: par = impar ∎

**10.2 Límite Fundamental**
\[ \lim_{x \to 0^+} x \ln x = 0 \]
*Importancia*: En teoría de algoritmos para análisis asintótico.

---

Esta clase proporciona un dominio completo de ecuaciones exponenciales y logarítmicas, desde fundamentos hasta aplicaciones avanzadas, con rigor matemático y enfoque práctico.