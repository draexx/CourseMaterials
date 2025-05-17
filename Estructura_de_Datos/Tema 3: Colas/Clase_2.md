### **Clase 2: Colas - Profundización en Definiciones y Ejercicios Avanzados**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Ampliar el concepto de colas con estructuras derivadas.  
2. Implementar colas circulares para optimizar operaciones.  
3. Resolver problemas avanzados con colas prioritarias.  

---

## **Parte 1: Ampliación Teórica (30 minutos)**  

### **1. Tipos de Colas**  
| **Tipo**               | **Descripción**                                  | **Ejemplo de Uso**               |  
|------------------------|------------------------------------------------|----------------------------------|  
| **Cola Estándar (FIFO)** | Primer elemento en entrar es el primero en salir | Filas de atención al cliente     |  
| **Cola Circular**       | Optimizada para evitar desplazamientos de memoria | Sistemas embebidos               |  
| **Cola de Prioridad**   | Elementos con mayor/menor prioridad salen primero | Sala de emergencias              |  
| **Deque (Doble Fin)**   | Permite enqueue/dequeue al inicio o final        | Historial de navegación (adelante/atrás) |  

### **2. Colas Circulares**  
**Problema:**  
- En colas estándar con listas, `dequeue` es ineficiente (`O(n)` por el desplazamiento de elementos).  

**Solución:**  
- Usar un arreglo estático y aritmética modular para manejar índices:  
  ```python  
  class ColaCircular:  
      def __init__(self, capacidad):  
          self.capacidad = capacidad  
          self.cola = [None] * capacidad  
          self.frente = self.final = -1  

      def enqueue(self, item):  
          if (self.final + 1) % self.capacidad == self.frente:  
              print("Cola llena")  
          elif self.frente == -1:  # Cola vacía  
              self.frente = self.final = 0  
              self.cola[self.final] = item  
          else:  
              self.final = (self.final + 1) % self.capacidad  
              self.cola[self.final] = item  

      def dequeue(self):  
          if self.frente == -1:  
              print("Cola vacía")  
          elif self.frente == self.final:  # Último elemento  
              temp = self.cola[self.frente]  
              self.frente = self.final = -1  
              return temp  
          else:  
              temp = self.cola[self.frente]  
              self.frente = (self.frente + 1) % self.capacidad  
              return temp  
  ```  

### **3. Colas de Prioridad**  
**Concepto:**  
- Los elementos tienen una prioridad asociada. Ejemplo:  
  ```python  
  import heapq  

  cola_prioridad = []  
  heapq.heappush(cola_prioridad, (3, "Tarea baja"))  
  heapq.heappush(cola_prioridad, (1, "Tarea urgente"))  
  print(heapq.heappop(cola_prioridad))  # (1, "Tarea urgente")  
  ```  

---

## **Parte 2: Ejercicios Prácticos (45 minutos)**  

### **Ejercicio 1: Sistema de Tickets con Cola Circular**  
**Enunciado:**  
Simular una fila de tickets en un banco con 3 ventanillas (capacidad máxima: 10 personas).  

**Solución:**  
```python  
banco = ColaCircular(10)  

# Llegan clientes  
for i in range(1, 4):  
    banco.enqueue(f"Cliente {i}")  

# Atender clientes  
print("Atendiendo:", banco.dequeue())  # Cliente 1  
print("Atendiendo:", banco.dequeue())  # Cliente 2  
```  

---

### **Ejercicio 2: Gestión de Tareas Urgentes**  
**Enunciado:**  
Implementar un sistema donde las tareas urgentes se procesen antes que las normales.  

**Solución:**  
```python  
class GestorTareas:  
    def __init__(self):  
        self.tareas = []  

    def agregar_tarea(self, nombre, prioridad):  
        heapq.heappush(self.tareas, (prioridad, nombre))  

    def procesar_tarea(self):  
        if self.tareas:  
            return heapq.heappop(self.tareas)[1]  
        return "No hay tareas pendientes"  

gestor = GestorTareas()  
gestor.agregar_tarea("Limpieza", 3)  
gestor.agregar_tarea("Error crítico", 1)  
print("Procesando:", gestor.procesar_tarea())  # Error crítico  
```  

---

### **Ejercicio 3: Búsqueda en Anchura (BFS) con Colas**  
**Enunciado:**  
Usar una cola para recorrer un grafo nivel por nivel.  

**Solución:**  
```python  
from collections import deque  

def bfs(grafo, inicio):  
    visitados = set()  
    cola = deque([inicio])  
    while cola:  
        nodo = cola.popleft()  
        if nodo not in visitados:  
            print("Visitando:", nodo)  
            visitados.add(nodo)  
            for vecino in grafo[nodo]:  
                cola.append(vecino)  

grafo = {  
    'A': ['B', 'C'],  
    'B': ['D'],  
    'C': ['E'],  
    'D': [],  
    'E': []  
}  
bfs(grafo, 'A')  
```  
**Output:**  
```  
Visitando: A  
Visitando: B  
Visitando: C  
Visitando: D  
Visitando: E  
```  

---

## **Parte 3: Cierre y Retroalimentación (5 minutos)**  
- **Discusión:**  
  - ¿Cuándo es mejor usar una cola circular vs una estándar?  
  - ¿Cómo optimizarías una cola de prioridad para 1 millón de elementos?  
- **Tarea:**  
  - Implementar un sistema de impresión que priorice documentos "urgentes".  

---

### **Material Adicional**  
- **Lectura:** [Colas en Python](https://realpython.com/queue-in-python/)  
- **Video:** [Colas de Prioridad](https://youtu.be/IHBBR4yNllE)  

**¿Qué otro problema te gustaría resolver con colas?** 😊