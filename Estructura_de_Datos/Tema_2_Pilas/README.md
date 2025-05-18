### **Planificación de la Unidad Temática 2: Pilas**  
**Duración:** 4 clases de 1 hora 20 minutos cada una.  
**Lenguaje:** Python.  
**Objetivo General:**  
Al finalizar la unidad, los estudiantes serán capaces de implementar y manipular pilas, entender su lógica LIFO y aplicarlas en problemas reales.  

---

## **Clase 1: Introducción a Pilas y Operaciones Básicas**  
**Objetivo:** Comprender el concepto de pila, sus operaciones básicas y su implementación en Python.  

### **1. Teoría (30 min)**  
- **Definición de pila:** Estructura LIFO (Last In, First Out).  
- **Operaciones básicas:**  
  - `push()`: Insertar un elemento.  
  - `pop()`: Eliminar el último elemento.  
  - `peek()`: Observar el tope sin eliminarlo.  
  - `is_empty()`: Verificar si está vacía.  
- **Analogías:** Pila de platos, historial de navegación.  

### **2. Implementación en Python (20 min)**  
- Usar listas para simular pilas:  
  ```python
  pila = []
  pila.append(1)  # push
  pila.pop()      # pop
  ```

### **3. Ejercicios (30 min)**  
1. Crear una pila y realizar operaciones `push`/`pop`.  
2. Verificar si una pila está vacía.  
3. Implementar `peek`.  

---

## **Clase 2: Aplicaciones de Pilas y Validación de Paréntesis**  
**Objetivo:** Aplicar pilas en problemas clásicos como validación de expresiones.  

### **1. Teoría (20 min)**  
- **Aplicaciones comunes:**  
  - Validación de paréntesis en código.  
  - Evaluación de expresiones postfijas.  

### **2. Ejercicio Guiado (30 min)**  
**Validar paréntesis balanceados:**  
```python
def validar_parentesis(expresion):
    pila = []
    for char in expresion:
        if char == '(':
            pila.append(char)
        elif char == ')':
            if not pila:
                return False
            pila.pop()
    return len(pila) == 0
```

### **3. Actividad Práctica (30 min)**  
- Extender el ejercicio para incluir `{}` y `[]`.  
- Ejemplo: `"{[()]}" → True`, `"[(])" → False`.  

---

## **Clase 3: Pilas en Algoritmos y Recursividad**  
**Objetivo:** Relacionar pilas con recursividad y algoritmos.  

### **1. Teoría (20 min)**  
- **Pilas en la memoria:** Call stack en funciones recursivas.  
- **Ejemplo:** Cálculo de factorial recursivo.  

### **2. Ejercicio Guiado (30 min)**  
**Simular recursividad con pilas:**  
```python
def factorial_iterativo(n):
    pila = [n]
    resultado = 1
    while pila:
        num = pila.pop()
        resultado *= num
        if num > 1:
            pila.append(num - 1)
    return resultado
```

### **3. Actividad (30 min)**  
- Implementar Fibonacci con pilas.  
- Comparar rendimiento recursivo vs. iterativo con pila.  

---

## **Clase 4: Proyecto Integrador**  
**Objetivo:** Aplicar pilas en un proyecto real.  

### **1. Consigna (15 min)**  
**Desarrollar un "Historial de Navegación" (como un navegador web):**  
- Usar una pila para almacenar URLs visitadas.  
- Operaciones:  
  - `navegar(url)`: Agrega una URL.  
  - `atras()`: Retrocede a la URL anterior.  

### **2. Implementación (45 min)**  
```python
historial = []

def navegar(url):
    historial.append(url)

def atras():
    if len(historial) > 1:
        historial.pop()
        return historial[-1]
    return None
```

### **3. Presentación y Retroalimentación (20 min)**  
- Grupos comparten sus soluciones.  
- Discusión: ¿Qué pasaría si usáramos una cola en lugar de una pila?  

---

### **Evaluación Continua:**  
- **Participación en ejercicios.**  
- **Código entregado en cada clase.**  
- **Proyecto final (historial de navegación).**  

### **Materiales:**  
- Diapositivas con ejemplos visuales.  
- Jupyter Notebook con ejercicios resueltos.  
- Vídeo opcional: "Cómo Python maneja el call stack".  

--- 
