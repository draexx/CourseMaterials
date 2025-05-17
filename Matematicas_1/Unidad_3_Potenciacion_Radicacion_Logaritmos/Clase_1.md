### **Clase 1: Potenciación - Definiciones Ampliadas y Fundamentos Teóricos**

#### **1. Potenciación: Concepto y Origen**
La potenciación es una operación matemática que **extiende la multiplicación** para casos donde un número (base) se multiplica por sí mismo varias veces (exponente). Surge de la necesidad de expresar:
- Crecimientos exponenciales
- Escalas geométricas
- Operaciones repetitivas de forma compacta

**Definición formal:**
Para todo número real a ≠ 0 y n ∈ ℕ:
aⁿ = a × a × ... × a (n veces)

**Caso especial 0⁰:**
Es una forma indeterminada en matemáticas avanzadas, pero en muchos contextos se define como 1 por convención.

#### **2. Dominio de los Exponentes**
Los exponentes pueden extenderse más allá de los números naturales:

| **Tipo de Exponente** | **Definición** | **Ejemplo** | **Restricciones** |
|-----------------------|----------------|-------------|-------------------|
| Natural (n ∈ ℕ) | aⁿ = a×a×...×a | 2³ = 8 | Ninguna |
| Cero | a⁰ = 1 | (-5)⁰ = 1 | a ≠ 0 |
| Entero negativo | a⁻ⁿ = 1/aⁿ | 3⁻² = 1/9 | a ≠ 0 |
| Racional (fracción) | a^(m/n) = ⁿ√(aᵐ) | 8^(1/3) = 2 | a > 0 cuando n es par |
| Real | Límite de sucesiones | 2^π ≈ 8.82498 | a > 0 |

#### **3. Propiedades Fundamentales (Teoremas)**
1. **Teorema del Producto de Potencias:**
   ∀a ∈ ℝ, m,n ∈ ℤ:
   aᵐ × aⁿ = aᵐ⁺ⁿ
   *Demostración:*
   Si m,n > 0: Por definición de potencia natural.

2. **Teorema de Potencia de Potencia:**
   (aᵐ)ⁿ = aᵐⁿ
   *Demostración:*
   Caso base n=1: trivial.
   Paso inductivo: (aᵐ)ⁿ⁺¹ = (aᵐ)ⁿ × aᵐ = aᵐⁿ × aᵐ = aᵐ⁽ⁿ⁺¹⁾

3. **Teorema de Distributividad:**
   (a×b)ⁿ = aⁿ×bⁿ
   *Demostración:*
   Por inducción sobre n usando conmutatividad del producto.

#### **4. Casos Especiales y Curiosidades**
1. **Potencias de 10 en Informática:**
   - 1 KB = 2¹⁰ bytes = 1024 bytes (no 1000)
   - Diferencia entre sistema binario (base 2) y decimal

2. **Potencias Negativas:**
   - 10⁻³ segundos = 1 milisegundo
   - 2⁻¹ = 0.5 (relación con bits en probabilidad)

3. **Notación Científica:**
   - 6.02×10²³ (Número de Avogadro)
   - 1.6×10⁻¹⁹ C (carga del electrón)

#### **5. Ejercicios Teóricos Avanzados**
1. **Demostración de Propiedades:**
   Probar que ∀a ≠ 0, a⁻ⁿ = 1/aⁿ usando inducción matemática.

2. **Generalización:**
   ¿Se cumple (a+b)ⁿ = aⁿ + bⁿ? Analizar para distintos conjuntos numéricos.

3. **Límites y Continuidad:**
   Estudiar la función f(x) = xˣ cuando x → 0⁺.

#### **6. Aplicaciones Interdisciplinares**
1. **Física Cuántica:**
   - Función de onda ψ(x) = Ae^(-kx²)
   - Decaimiento exponencial N(t) = N₀e^(-λt)

2. **Teoría de Algoritmos:**
   - Complejidad exponencial O(2ⁿ)
   - Crecimiento de árboles binarios completos (2ʰ-1 nodos)

3. **Finanzas:**
   - Interés compuesto A = P(1 + r/n)^(nt)
   - Modelos de crecimiento económico

#### **7. Errores Comunes y Precauciones**
1. **Falacia del Exponente:**
   (a+b)ⁿ ≠ aⁿ + bⁿ (excepto cuando n=1)

2. **Prioridad Operacional:**
   -2² = -4 vs (-2)² = 4

3. **Indeterminaciones:**
   0⁰, ∞⁰, 1^∞ (requieren análisis con límites)

#### **8. Ejercicios de Aplicación Profunda**
1. **Simplificación Extrema:**
   Simplificar completamente:
   \[
   \left( \frac{x^{2a+3b}y^{4a-b} \right)^{1/2} \div \left( \frac{x^{5a-2b}}{y^{a+3b}} \right)^{-1/3}
   \]

2. **Problema de Optimización:**
   Encontrar el valor mínimo de f(x) = 2^(x²-4x+5)

3. **Demostración:**
   Probar que no existen enteros a, b, n > 2 tales que aⁿ + bⁿ = (a+b)ⁿ

#### **9. Recursos Visuales**
1. **Gráfica Comparativa:**
   Comparar el crecimiento de:
   - f(x) = 2ˣ
   - g(x) = x²
   - h(x) = x!

2. **Diagrama de Propiedades:**
   Mapa conceptual que relacione todas las propiedades de potencias.

#### **10. Evaluación de Comprensión**
1. **Preguntas Teóricas:**
   - ¿Por qué a⁰ = 1 cuando a ≠ 0?
   - Explicar la relación entre potencias fraccionarias y radicales.

2. **Problemas Conceptuales:**
   - ¿Es (-1)^(1/3) real o complejo? Justificar.
   - Analizar la continuidad de x^y en (0,0).

Esta ampliación teórica proporciona una base rigurosa para entender la potenciación desde sus fundamentos hasta aplicaciones avanzadas, integrando conexiones con otras disciplinas y enfatizando el rigor matemático.