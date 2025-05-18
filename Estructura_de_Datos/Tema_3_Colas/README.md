### **Planificación de la Unidad Temática: Colas (Queues)**  
**Duración:** 6 clases de 1 hora 20 minutos cada una  
**Lenguaje:** Python  
**Objetivo General:**  
Al finalizar la unidad, los estudiantes dominarán la estructura de datos **cola** (FIFO), sus variantes y aplicaciones en problemas reales, implementando soluciones desde cero.  

---

## **Clase 1: Introducción a Colas y Operaciones Básicas**  
**Objetivos:**  
- Comprender el principio FIFO (First In, First Out).  
- Implementar una cola básica con listas en Python.  

**Contenidos:**  
1. **Teoría:**  
   - Definición de cola y analogías (ej: fila en un banco).  
   - Operaciones: `enqueue` (encolar), `dequeue` (desencolar), `front` (frente), `is_empty`.  
2. **Práctica:**  
   - Implementación con listas:  
     ```python  
     cola = []  
     cola.append(1)  # Enqueue  
     cola.pop(0)     # Dequeue (ineficiente en listas grandes)  
     ```  
   - Ejercicio: Simular una fila de atención al cliente.  

**Tarea:** Implementar una cola que maneje errores (ej: desencolar cuando está vacía).  

---

## **Clase 2: Colas Circulares y Eficiencia**  
**Objetivos:**  
- Entender las limitaciones de las listas estándar y la necesidad de colas circulares.  
- Implementar una cola circular con arreglos.  

**Contenidos:**  
1. **Teoría:**  
   - Problemas de rendimiento con `pop(0)` en listas.  
   - Concepto de cola circular y aritmética modular.  
2. **Práctica:**  
   - Implementación de cola circular:  
     ```python  
     class ColaCircular:  
         def __init__(self, capacidad):  
             self.capacidad = capacidad  
             self.cola = [None] * capacidad  
             self.frente = self.final = -1  
     ```  
   - Ejercicio: Manejar desbordamiento (`overflow`) y subdesbordamiento (`underflow`).  

**Tarea:** Medir el tiempo de ejecución de `dequeue` en lista vs. cola circular.  

---

## **Clase 3: Colas de Prioridad**  
**Objetivos:**  
- Introducir colas de prioridad y su uso en algoritmos.  
- Implementar con el módulo `heapq` de Python.  

**Contenidos:**  
1. **Teoría:**  
   - Prioridades: mínimo o máximo primero.  
   - Aplicaciones: sistemas de emergencia, planificación de procesos.  
2. **Práctica:**  
   - Uso de `heapq`:  
     ```python  
     import heapq  
     cola_prioridad = []  
     heapq.heappush(cola_prioridad, (prioridad, dato))  
     heapq.heappop(cola_prioridad)  
     ```  
   - Ejercicio: Simular una sala de emergencias (prioridad por gravedad).  

**Tarea:** Implementar una cola de prioridad sin librerías externas.  

---

## **Clase 4: Colas en Algoritmos (BFS y Scheduling)**  
**Objetivos:**  
- Aplicar colas en BFS (Breadth-First Search) y planificación de procesos.  

**Contenidos:**  
1. **Teoría:**  
   - BFS en grafos: explicación visual.  
   - Algoritmo Round Robin en sistemas operativos.  
2. **Práctica:**  
   - BFS con cola:  
     ```python  
     def bfs(grafo, inicio):  
         visitados = set()  
         cola = [inicio]  
         while cola:  
             nodo = cola.pop(0)  
             for vecino in grafo[nodo]:  
                 if vecino not in visitados:  
                     cola.append(vecino)  
                     visitados.add(vecino)  
     ```  
   - Ejercicio: Simular Round Robin con tiempos de CPU.  

**Tarea:** Resolver un laberinto usando BFS.  

---

## **Clase 5: Colas en Sistemas Reales (Proyecto Parcial)**  
**Objetivos:**  
- Implementar un sistema de mensajería o buffer con colas.  

**Contenidos:**  
1. **Proyecto:**  
   - Sistema de mensajes con colas FIFO y prioridad.  
   - Ejemplo:  
     ```python  
     class SistemaMensajes:  
         def __init__(self):  
             self.cola_normal = []  
             self.cola_urgente = []  

         def enviar_mensaje(self, mensaje, urgente=False):  
             if urgente:  
                 self.cola_urgente.append(mensaje)  
             else:  
                 self.cola_normal.append(mensaje)  

         def procesar_mensaje(self):  
             if self.cola_urgente:  
                 return self.cola_urgente.pop(0)  
             elif self.cola_normal:  
                 return self.cola_normal.pop(0)  
     ```  
2. **Discusión:**  
   - ¿Cómo manejar mensajes duplicados o expirados?  

**Tarea:** Añadir timestamp a los mensajes y descartar los antiguos.  

---

## **Clase 6: Proyecto Integrador y Evaluación**  
**Objetivos:**  
- Implementar un sistema de gestión de tareas con colas y prioridades.  
- Evaluar comprensión con ejercicios cronometrados.  

**Actividades:**  
1. **Proyecto Final:**  
   - Sistema de tareas con:  
     - Cola general (FIFO).  
     - Cola de prioridad (urgente/normal).  
     - Función para procesar tareas en orden mixto.  
2. **Evaluación:**  
   - Ejercicio sorpresa: Implementar una cola doblemente terminada (`deque`) desde cero.  
   - Preguntas teóricas: Diferencias entre cola, pila y lista.  

**Cierre:** Retroalimentación y aplicaciones en la industria (ej: Amazon SQS).  

---

### **Evaluación Continua**  
- **Participación en ejercicios:** 20%  
- **Tareas semanales:** 30%  
- **Proyecto parcial (Clase 5):** 20%  
- **Proyecto final (Clase 6):** 30%  

### **Material Adicional**  
- **Lecturas:**  
  - [Colas en Python](https://docs.python.org/3/library/queue.html).  
  - [Aplicaciones de BFS](https://www.geeksforgeeks.org/applications-of-breadth-first-traversal/).  
- **Videos:**  
  - [Cómo funcionan las colas en sistemas operativos](https://youtu.be/WgIi5ZgC0Xw).  

--- 

**¿Qué ajustes necesitarías para tu grupo?** 😊 ¿Más ejercicios de algoritmos o enfoque en aplicaciones prácticas?