### **Clase 3: Colas de Prioridad y Aplicaciones en Algoritmos**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Dominar el concepto de colas de prioridad y su implementación.  
2. Aplicar colas en algoritmos clásicos (Dijkstra, sistemas de scheduling).  
3. Resolver problemas reales con estructuras prioritarias.  

---

## **Parte 1: Teoría (30 minutos)**  

### **1. Colas de Prioridad**  
**Definición:**  
- Estructura donde cada elemento tiene una prioridad asociada.  
- **Operaciones clave:**  
  - `insertar(elemento, prioridad)`.  
  - `extraer_máximo()` o `extraer_mínimo()`.  

**Implementación con `heapq` (mín-heap por defecto):**  
```python  
import heapq  

cola_prioridad = []  
heapq.heappush(cola_prioridad, (2, "Tarea Media"))  
heapq.heappush(cola_prioridad, (1, "Tarea Urgente"))  
print(heapq.heappop(cola_prioridad))  # (1, "Tarea Urgente")  
```  

**Ejemplo de max-heap (truco con valores negativos):**  
```python  
heapq.heappush(cola_prioridad, (-3, "Tarea Baja"))  # Prioridad inversa  
```  

---

### **2. Aplicaciones en Algoritmos**  
- **Algoritmo de Dijkstra:** Para encontrar el camino más corto en grafos.  
- **Scheduling en Sistemas Operativos:** Planificación de procesos por prioridad.  
- **Merging de K listas ordenadas:** Uso eficiente de colas de prioridad.  

---

## **Parte 2: Ejercicios Prácticos (45 minutos)**  

### **Ejercicio 1: Sistema de Emergencias Hospitalarias**  
**Enunciado:**  
Priorizar pacientes según gravedad (1: crítico, 3: leve).  

**Solución:**  
```python  
class SalaEmergencias:  
    def __init__(self):  
        self.pacientes = []  

    def agregar_paciente(self, nombre, gravedad):  
        heapq.heappush(self.pacientes, (gravedad, nombre))  

    def atender_paciente(self):  
        if self.pacientes:  
            return heapq.heappop(self.pacientes)[1]  
        return "No hay pacientes"  

sala = SalaEmergencias()  
sala.agregar_paciente("Juan", 3)  
sala.agregar_paciente("Ana", 1)  
print(sala.atender_paciente())  # Ana (prioridad 1)  
```  

---

### **Ejercicio 2: Merge de K Listas Ordenadas**  
**Enunciado:**  
Combinar múltiples listas ordenadas en una sola lista ordenada.  

**Solución:**  
```python  
def merge_k_listas(listas):  
    cola_prioridad = []  
    for i, lista in enumerate(listas):  
        if lista:  
            heapq.heappush(cola_prioridad, (lista[0], i, 0))  

    resultado = []  
    while cola_prioridad:  
        val, lista_idx, elem_idx = heapq.heappop(cola_prioridad)  
        resultado.append(val)  
        if elem_idx + 1 < len(listas[lista_idx]):  
            heapq.heappush(cola_prioridad, (listas[lista_idx][elem_idx + 1], lista_idx, elem_idx + 1))  
    return resultado  

listas = [[1, 4, 5], [1, 3, 4], [2, 6]]  
print(merge_k_listas(listas))  # [1, 1, 2, 3, 4, 4, 5, 6]  
```  

---

### **Ejercicio 3: Camino Más Corto (Dijkstra Simplificado)**  
**Enunciado:**  
Encontrar el camino más corto en un grafo ponderado.  

**Solución:**  
```python  
def dijkstra(grafo, inicio):  
    distancias = {nodo: float('inf') for nodo in grafo}  
    distancias[inicio] = 0  
    cola_prioridad = [(0, inicio)]  

    while cola_prioridad:  
        dist_actual, nodo_actual = heapq.heappop(cola_prioridad)  
        for vecino, peso in grafo[nodo_actual].items():  
            distancia = dist_actual + peso  
            if distancia < distancias[vecino]:  
                distancias[vecino] = distancia  
                heapq.heappush(cola_prioridad, (distancia, vecino))  
    return distancias  

grafo = {  
    'A': {'B': 1, 'C': 4},  
    'B': {'A': 1, 'C': 2, 'D': 5},  
    'C': {'A': 4, 'B': 2, 'D': 1},  
    'D': {'B': 5, 'C': 1}  
}  
print(dijkstra(grafo, 'A'))  # {'A': 0, 'B': 1, 'C': 3, 'D': 4}  
```  

---

## **Parte 3: Cierre y Retroalimentación (5 minutos)**  
- **Discusión:**  
  - ¿Cómo optimizarías una cola de prioridad para millones de elementos?  
  - ¿Qué pasa si dos elementos tienen la misma prioridad?  
- **Tarea:**  
  - Implementar un scheduler de tareas que priorice por tiempo de ejecución.  

---

### **Material Adicional**  
- **Lectura:** [Heaps en Python](https://realpython.com/python-heapq-module/).  
- **Video:** [Dijkstra's Algorithm](https://youtu.be/GazC3A4OQTE).  

**¿Qué otro algoritmo te gustaría implementar con colas de prioridad?** 😊