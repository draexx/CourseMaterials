### **Clase 2: Pilas - Profundización Teórica y Ejercicios Prácticos**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Reforzar la comprensión teórica de pilas con definiciones ampliadas.  
2. Resolver ejercicios prácticos de complejidad gradual.  
3. Aplicar pilas en problemas de la vida real.  

---

## **Parte 1: Ampliación Teórica (30 minutos)**  

### **1. Definición Profundizada**  
**Pila (Stack):**  
- Estructura de datos **lineal** que sigue el principio **LIFO** (*Last In, First Out*).  
- **Características clave:**  
  - **Dinámica:** No tiene tamaño fijo (en Python).  
  - **Operaciones atómicas:** Solo se accede al elemento superior (`tope`).  
  - **Eficiencia:** Todas las operaciones son **O(1)** (tiempo constante).  

**Analogías:**  
- **Historial de navegación:** El último sitio visitado es el primero en recuperarse al hacer clic en "Atrás".  
- **Pila de libros:** Solo puedes tomar el libro de la parte superior.  

### **2. Implementación en Python**  
**Opción 1: Usando Listas**  
```python  
pila = []  
pila.append(10)  # Push  
pila.append(20)  
print(pila.pop())  # Pop → 20  
```  

**Opción 2: Clase Personalizada (Encapsulamiento)**  
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

# Uso  
mi_pila = Pila()  
mi_pila.push("A")  
print(mi_pila.peek())  # "A"  
```  

### **3. Aplicaciones Reales**  
- **Undo/Redo:** Editores de texto o gráficos.  
- **Call Stack:** Gestión de llamadas a funciones en programación.  
- **Algoritmos de grafos:** DFS (Depth-First Search).  

---

## **Parte 2: Ejercicios Prácticos (50 minutos)**  

### **Ejercicio 1: Validación de Paréntesis Balanceados**  
**Enunciado:**  
Verificar si una cadena tiene paréntesis `()`, corchetes `[]` y llaves `{}` balanceados.  

**Solución:**  
```python  
def esta_balanceada(expresion):  
    pila = []  
    pares = {')': '(', ']': '[', '}': '{'}  
    for char in expresion:  
        if char in pares.values():  # Si es apertura  
            pila.append(char)  
        elif char in pares:  # Si es cierre  
            if not pila or pila.pop() != pares[char]:  
                return False  
    return len(pila) == 0  

print(esta_balanceada("{[()]}"))  # True  
print(esta_balanceada("{[}]"))    # False  
```  

**Variante:**  
- Añadir soporte para etiquetas HTML (ej: `<div>`, `</div>`).  

---

### **Ejercicio 2: Evaluación de Expresiones Postfijas**  
**Enunciado:**  
Evaluar una expresión en notación postfija (ej: `3 4 + 5 *` = `35`).  

**Solución:**  
```python  
def evaluar_postfija(expresion):  
    pila = []  
    for token in expresion.split():  
        if token.isdigit():  
            pila.append(int(token))  
        else:  
            b, a = pila.pop(), pila.pop()  
            pila.append(eval(f"{a}{token}{b}"))  
    return pila.pop()  

print(evaluar_postfija("3 4 + 5 *"))  # 35  
```  

**Variante:**  
- Convertir una expresión infija (ej: `3 + 4 * 5`) a postfija usando pilas.  

---

### **Ejercicio 3: Simulación de un Editor de Texto (Undo/Redo)**  
**Enunciado:**  
Implementar un sistema de `undo` y `redo` usando dos pilas.  

**Solución:**  
```python  
class EditorTexto:  
    def __init__(self):  
        self.texto = ""  
        self.pila_undo = []  
        self.pila_redo = []  

    def escribir(self, texto):  
        self.pila_undo.append(self.texto)  
        self.texto += texto  
        self.pila_redo = []  # Limpiar redo al hacer una nueva acción  

    def undo(self):  
        if self.pila_undo:  
            self.pila_redo.append(self.texto)  
            self.texto = self.pila_undo.pop()  

    def redo(self):  
        if self.pila_redo:  
            self.pila_undo.append(self.texto)  
            self.texto = self.pila_redo.pop()  

# Uso  
editor = EditorTexto()  
editor.escribir("Hola ")  
editor.escribir("Mundo")  
editor.undo()  
print(editor.texto)  # "Hola "  
editor.redo()  
print(editor.texto)  # "Hola Mundo"  
```  

---

### **Ejercicio 4: Búsqueda en Laberinto (DFS con Pilas)**  
**Enunciado:**  
Usar una pila para implementar DFS y encontrar la salida en un laberinto 2D.  

**Solución Simplificada:**  
```python  
laberinto = [  
    [" ", "#", " ", " "],  
    [" ", "#", " ", "#"],  
    [" ", " ", " ", " "],  
    ["#", "#", " ", "S"]  # S = Salida  
]  

def dfs_laberinto(laberinto, inicio):  
    pila = [inicio]  
    visitados = set()  
    while pila:  
        x, y = pila.pop()  
        if laberinto[x][y] == "S":  
            return True  
        visitados.add((x, y))  
        for dx, dy in [(0, 1), (1, 0), (0, -1), (-1, 0)]:  
            nx, ny = x + dx, y + dy  
            if 0 <= nx < len(laberinto) and 0 <= ny < len(laberinto[0]):  
                if (nx, ny) not in visitados and laberinto[nx][ny] != "#":  
                    pila.append((nx, ny))  
    return False  

print(dfs_laberinto(laberinto, (0, 0)))  # True  
```  

---

## **Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿En qué otros escenarios cotidianos se aplican las pilas?  
  - Ventajas/desventajas vs. otras estructuras (ej: colas).  
- **Desafío Adicional:**  
  - Implementar una pila que además devuelva el elemento mínimo en **O(1)**.  

---

### **Material Complementario**  
- **Lectura recomendada:** [Pilas en aplicaciones de compiladores](https://es.wikipedia.org/wiki/Pila_(inform%C3%A1tica)).  
- **Video:** [Cómo funciona el call stack en Python](https://youtu.be/WjIlcb2PrMI).  

**¿Qué otro aspecto de las pilas te gustaría explorar?** 😊