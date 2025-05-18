### **Clase 1: Introducción a Pilas - Fundamentos y Ejercicios Básicos**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Comprender el concepto de pila (LIFO) y sus operaciones básicas.  
2. Implementar una pila en Python desde cero.  
3. Resolver problemas simples usando pilas.  

---

## **Parte 1: Teoría (30 minutos)**  

### **1. Definición de Pila**  
- **Estructura LIFO** (*Last In, First Out*): El último elemento en entrar es el primero en salir.  
- **Analogías:**  
  - Pila de platos: El último plato apilado es el primero en lavarse.  
  - Historial de navegación: La última página visitada es la primera al hacer clic en "Atrás".  

### **2. Operaciones Básicas**  
| **Operación** | **Descripción**                          | **Ejemplo en Python**       |  
|---------------|------------------------------------------|-----------------------------|  
| `push(x)`     | Agrega `x` al tope de la pila.          | `pila.append(x)`            |  
| `pop()`       | Remueve y devuelve el tope de la pila.  | `tope = pila.pop()`         |  
| `peek()`      | Observa el tope sin removerlo.          | `tope = pila[-1]`           |  
| `is_empty()`  | Verifica si la pila está vacía.         | `len(pila) == 0`            |  

### **3. Implementación con Listas en Python**  
```python  
class Pila:  
    def __init__(self):  
        self.items = []  

    def push(self, item):  
        self.items.append(item)  

    def pop(self):  
        if not self.is_empty():  
            return self.items.pop()  
        raise IndexError("La pila está vacía")  

    def peek(self):  
        return self.items[-1] if not self.is_empty() else None  

    def is_empty(self):  
        return len(self.items) == 0  

    def __str__(self):  
        return str(self.items)  
```  

**Ejemplo de uso:**  
```python  
p = Pila()  
p.push(10)  
p.push(20)  
print(p.pop())  # 20  
print(p.peek()) # 10  
```  

---

## **Parte 2: Ejercicios Prácticos (40 minutos)**  

### **Ejercicio 1: Invertir una Cadena**  
**Enunciado:** Usar una pila para invertir una cadena de texto.  

**Solución:**  
```python  
def invertir_cadena(cadena):  
    pila = Pila()  
    for char in cadena:  
        pila.push(char)  
    resultado = ""  
    while not pila.is_empty():  
        resultado += pila.pop()  
    return resultado  

print(invertir_cadena("Python"))  # "nohtyP"  
```  

---

### **Ejercicio 2: Validar Paréntesis Balanceados**  
**Enunciado:** Verificar si una expresión tiene paréntesis balanceados `()`, `[]`, `{}`.  

**Solución:**  
```python  
def parentesis_balanceados(expresion):  
    pila = Pila()  
    pares = {")": "(", "]": "[", "}": "{"}  
    for char in expresion:  
        if char in pares.values():  # Si es apertura  
            pila.push(char)  
        elif char in pares:  # Si es cierre  
            if pila.is_empty() or pila.pop() != pares[char]:  
                return False  
    return pila.is_empty()  

print(parentesis_balanceados("{[()]}"))  # True  
print(parentesis_balanceados("{[}]"))    # False  
```  

---

### **Ejercicio 3: Sistema de "Undo" Básico**  
**Enunciado:** Simular la función "Deshacer" en un editor de texto.  

**Solución:**  
```python  
class EditorTexto:  
    def __init__(self):  
        self.texto = ""  
        self.historial = Pila()  

    def escribir(self, texto):  
        self.historial.push(self.texto)  
        self.texto += texto  

    def deshacer(self):  
        if not self.historial.is_empty():  
            self.texto = self.historial.pop()  

editor = EditorTexto()  
editor.escribir("Hola ")  
editor.escribir("Mundo")  
editor.deshacer()  
print(editor.texto)  # "Hola "  
```  

---

## **Parte 3: Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿En qué otros escenarios se usan pilas en la vida real?  
  - ¿Qué pasa si hacemos `pop()` en una pila vacía?  
- **Tarea:**  
  - Implementar una calculadora que evalúe expresiones postfijas (ej: `3 4 +`).  

---

### **Material Adicional**  
- **Video:** [Cómo funcionan las pilas en memoria](https://youtu.be/F1F2imiOJfk).  
- **Simulador interactivo:** [VisualGED - Pilas](https://visualgo.net/es/list).  

**¿Qué otro problema te gustaría resolver con pilas?** 😊