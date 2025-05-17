### **Clase 2 Ampliada: Radicación y Racionalización - Definiciones Profundas y Ejercicios Avanzados**

#### **1. Definiciones Ampliadas con Notación Matemática Rigurosa**

**1.1 Radicación como Operación Inversa:**
\[
\sqrt[n]{a} = b \iff b^n = a \quad \text{donde:}
\]
- \( n \in \mathbb{N} \) (índice, \( n \geq 2 \))
- \( a \in \mathbb{R} \) (radicando)
- \( b \in \mathbb{R} \) (raíz)

**Caso Especial \( n = 2 \):**
\[
\sqrt{a} := \sqrt[2]{a} \quad \text{(Raíz cuadrada principal)}
\]

**1.2 Dominio y Rango:**
| **Índice (n)** | **Dominio de \( a \)** | **Rango de \( \sqrt[n]{a} \)** |
|----------------|------------------------|-------------------------------|
| Par            | \( a \geq 0 \)          | \( \sqrt[n]{a} \geq 0 \)       |
| Impar          | \( a \in \mathbb{R} \)  | \( \sqrt[n]{a} \in \mathbb{R} \)|

**Ejemplo Existencial:**
\[
\sqrt[4]{81} = 3 \quad \text{porque} \quad 3^4 = 81
\]

#### **2. Propiedades Matemáticas con Demostraciones Completas**

**2.1 Propiedad de Homomorfismo Multiplicativo:**
\[
\sqrt[n]{a \cdot b} = \sqrt[n]{a} \cdot \sqrt[n]{b}
\]
*Demostración:*
1. Sea \( x = \sqrt[n]{a} \), \( y = \sqrt[n]{b} \).
2. Entonces \( x^n = a \), \( y^n = b \).
3. \( (x \cdot y)^n = x^n \cdot y^n = a \cdot b \).
4. Por definición: \( \sqrt[n]{a \cdot b} = x \cdot y \). ∎

**2.2 Potencia de un Radical:**
\[
\left( \sqrt[n]{a} \right)^k = \sqrt[n]{a^k} \quad \text{para } k \in \mathbb{N}
\]
*Ejemplo Numérico:*
\[
\left( \sqrt[3]{5} \right)^6 = \sqrt[3]{5^6} = 5^2 = 25
\]

#### **3. Racionalización: Técnicas Extendidas**

**3.1 Casos Complejos con Binomios Irracionales:**
\[
\frac{1}{\sqrt{a} \pm \sqrt{b}} = \frac{\sqrt{a} \mp \sqrt{b}}{a - b}
\]
*Ejemplo Resuelto:*
\[
\frac{3}{\sqrt{7} + \sqrt{2}} = \frac{3(\sqrt{7} - \sqrt{2})}{7 - 2} = \frac{3\sqrt{7} - 3\sqrt{2}}{5}
\]

**3.2 Racionalización con Raíces Cúbicas:**
\[
\frac{1}{\sqrt[3]{a} \pm \sqrt[3]{b}} = \frac{\sqrt[3]{a^2} \mp \sqrt[3]{ab} + \sqrt[3]{b^2}}{a \pm b}
\]
*Ejemplo Práctico:*
\[
\frac{2}{\sqrt[3]{3} + 1} = \frac{2(\sqrt[3]{9} - \sqrt[3]{3} + 1)}{4}
\]

#### **4. Ejercicios Avanzados con Soluciones Detalladas**

**Ejercicio 1 (Simplificación Extrema):**
Simplificar completamente:
\[
\sqrt[5]{32x^{10}y^{15}} \cdot \sqrt{8x^6y^4}
\]
*Solución Paso a Paso:*
1. Convertir a exponentes:
   \[
   2x^2y^3 \cdot 2^{3/2}x^3y^2
   \]
2. Simplificar:
   \[
   2^{5/2}x^5y^5 = 4\sqrt{2}x^5y^5
   \]

**Ejercicio 2 (Ecuación Radical):**
Resolver para \( x \):
\[
\sqrt{3x + 1} + \sqrt{x - 1} = 4
\]
*Procedimiento:*
1. Aislar un radical:
   \[
   \sqrt{3x + 1} = 4 - \sqrt{x - 1}
   \]
2. Elevar al cuadrado:
   \[
   3x + 1 = 16 - 8\sqrt{x - 1} + x - 1
   \]
3. Resolver:
   \[
   x = 5 \quad (\text{Verificar solución})
   \]

#### **5. Aplicaciones Interdisciplinarias Detalladas**

**5.1 En Criptografía:**
Cálculo de raíces primitivas módulo \( p \) para claves Diffie-Hellman:
\[
\text{Encontrar } k \text{ tal que } g^k \equiv a \mod p
\]
*Ejemplo:*
Para \( p = 7 \), \( g = 3 \):
\[
\sqrt[3]{2} \mod 7 \implies 3^2 \equiv 2 \mod 7
\]

**5.2 En Física Cuántica:**
Normalización de funciones de onda:
\[
\int_{-\infty}^\infty |\psi(x)|^2 dx = 1 \implies \psi(x) = \frac{1}{\sqrt{\pi}}e^{-x^2/2}
\]

#### **6. Problemas Teóricos para Demostración**

**Problema 1:**
Demostrar que \( \sqrt{2} + \sqrt{3} \) es irracional.

*Hint:* Suponer racional y elevar al cuadrado.

**Problema 2:**
Probar que para \( a, b > 0 \):
\[
\sqrt{a + b} \leq \sqrt{a} + \sqrt{b}
\]
*Método:* Usar desigualdad de Cauchy-Schwarz.

#### **7. Tabla de Ejercicios de Autoevaluación**

| **Tipo**               | **Ejercicio**                      | **Dificultad** | **Solución**           |
|------------------------|------------------------------------|---------------|------------------------|
| Simplificación         | \( \sqrt{50} + 2\sqrt{18} \)       | Básica         | \( 11\sqrt{2} \)       |
| Racionalización        | \( \frac{5}{2 - \sqrt{3}} \)       | Intermedia     | \( 10 + 5\sqrt{3} \)   |
| Ecuación Radical       | \( \sqrt{x + 5} = x - 1 \)         | Avanzada       | \( x = 4 \)            |
| Aplicación Física      | \( T = 2\pi\sqrt{L/g} \), despejar \( L \) | Intermedia | \( L = \frac{gT^2}{4\pi^2} \) |

#### **8. Errores Comunes con Explicación Matemática**

**Error 1:**
\[
\sqrt{a^2 + b^2} \neq a + b
\]
*Contraejemplo:*
\[
\sqrt{3^2 + 4^2} = 5 \neq 7
\]

**Error 2:**
\[
\sqrt[n]{a + b} \neq \sqrt[n]{a} + \sqrt[n]{b}
\]
*Demostración:*
Tomar \( a = b = 1 \), \( n = 2 \):
\[
\sqrt{2} \neq 2
\]

#### **9. Ejercicios Creativos para Desarrollo de Habilidades**

**Ejercicio 1:**
Crear un problema de aplicación donde se use:
\[
V = \frac{4}{3}\pi r^3 \implies r = \sqrt[3]{\frac{3V}{4\pi}}
\]
*Contexto:* Calcular el radio de un globo esférico con volumen \( V = 288\pi \).

**Ejercicio 2:**
Diseñar una ecuación radical cuya solución sea \( x = 12 \).

*Ejemplo:*
\[
\sqrt{2x - 3} + \sqrt{x} = 7
\]

#### **10. Recursos Visuales Interactivos**

1. **Gráfica Animada:**  
   Comparar \( y = \sqrt{x} \) vs \( y = x^{1/3} \) en \( [-10, 10] \).

2. **Diagrama de Flujo:**  
   Pasos para racionalizar \( \frac{1}{\sqrt{a} \pm \sqrt{b}} \).

---

Esta versión ampliada integra rigor matemático con aplicaciones prácticas, ideal para clases avanzadas o autoestudio.