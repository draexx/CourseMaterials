### **Clase 1: Introducción a Colas - Definiciones y Ejemplos Prácticos**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Comprender el concepto de cola (FIFO) y sus operaciones básicas.  
2. Implementar una cola en Python desde cero.  
3. Aplicar colas en problemas simples de la vida real.  

---

## **Parte 1: Teoría (30 minutos)**  

### **1. Definición de Cola**  
- **Estructura FIFO** (*First In, First Out*): El primer elemento en entrar es el primero en salir.  
- **Analogías:**  
  - Fila en un banco: La primera persona en llegar es la primera en ser atendida.  
  - Cola de impresión: Los documentos se imprimen en el orden en que se enviaron.  

### **2. Operaciones Básicas**  
| **Operación** | **Descripción**                          | **Ejemplo en Python**       |  
|---------------|------------------------------------------|-----------------------------|  
| `enqueue(x)`  | Agrega `x` al final de la cola.         | `cola.append(x)`            |  
| `dequeue()`   | Remueve y devuelve el primer elemento.   | `primer_elemento = cola.pop(0)` |  
| `front()`     | Observa el primer elemento sin removerlo.| `primer_elemento = cola[0]` |  
| `is_empty()`  | Verifica si la cola está vacía.          | `len(cola) == 0`            |  

### **3. Implementación con Listas en Python**  
```python  
class Cola:  
    def __init__(self):  
        self.items = []  

    def enqueue(self, item):  
        self.items.append(item)  

    def dequeue(self):  
        if not self.is_empty():  
            return self.items.pop(0)  
        raise IndexError("La cola está vacía")  

    def front(self):  
        return self.items[0] if not self.is_empty() else None  

    def is_empty(self):  
        return len(self.items) == 0  

    def __str__(self):  
        return str(self.items)  
```  

**Nota:** Usar `pop(0)` es ineficiente para listas grandes (O(n)). En clases futuras se optimizará con colas circulares.  

---

## **Parte 2: Ejemplos Prácticos (40 minutos)**  

### **Ejemplo 1: Simulación de Fila de Atención al Cliente**  
**Enunciado:**  
Simular una fila donde los clientes son atendidos en orden de llegada.  

**Solución:**  
```python  
fila = Cola()  

# Llegan clientes  
fila.enqueue("Cliente 1")  
fila.enqueue("Cliente 2")  
fila.enqueue("Cliente 3")  

print("Fila actual:", fila)  # Output: ['Cliente 1', 'Cliente 2', 'Cliente 3']  

# Atender clientes  
print("Atendiendo a:", fila.dequeue())  # Output: Cliente 1  
print("Fila actual:", fila)  # Output: ['Cliente 2', 'Cliente 3']  
```  

---

### **Ejemplo 2: Procesamiento de Pedidos en un Restaurante**  
**Enunciado:**  
Los pedidos se procesan en el orden en que se reciben.  

**Solución:**  
```python  
pedidos = Cola()  
pedidos.enqueue({"id": 1, "plato": "Pizza"})  
pedidos.enqueue({"id": 2, "plato": "Ensalada"})  

while not pedidos.is_empty():  
    pedido_actual = pedidos.dequeue()  
    print(f"Preparando: {pedido_actual['plato']} (ID: {pedido_actual['id']})")  
```  
**Output:**  
```  
Preparando: Pizza (ID: 1)  
Preparando: Ensalada (ID: 2)  
```  

---

### **Ejemplo 3: Validación de una Cola en un Juego de Turnos**  
**Enunciado:**  
Verificar si los jugadores reciben su turno en el orden correcto.  

**Solución:**  
```python  
turnos_esperados = ["Jugador1", "Jugador2", "Jugador3"]  
turnos_reales = Cola()  
turnos_reales.enqueue("Jugador1")  
turnos_reales.enqueue("Jugador2")  
turnos_reales.enqueue("Jugador3")  

for turno_esperado in turnos_esperados:  
    turno_real = turnos_reales.dequeue()  
    if turno_esperado != turno_real:  
        print(f"Error: Se esperaba {turno_esperado}, pero salió {turno_real}")  
        break  
else:  
    print("Todos los turnos son correctos!")  
```  

---

## **Parte 3: Ejercicios para Realizar en Clase (10 minutos)**  
1. **Ejercicio 1:**  
   - Implementar una función que revierta el orden de una cola usando solo operaciones de cola.  
   **Pista:** Usar una pila como estructura auxiliar.  

2. **Ejercicio 2:**  
   - Simular una cola de mensajes en un chat donde los mensajes se muestran en orden de llegada.  

---

## **Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿Qué problemas surgieron al implementar las colas?  
  - ¿En qué otros escenarios cotidianos se usan colas?  
- **Tarea:**  
  - Implementar una cola que además de `enqueue` y `dequeue`, tenga un método `size()` que devuelva el número de elementos.  

---

### **Material Adicional**  
- **Video Recomendado:** [Colas en Python - Explicación Visual](https://youtu.be/rUUrmGKYwHw).  
- **Lectura:** [Documentación oficial de Python sobre listas](https://docs.python.org/3/tutorial/datastructures.html).  

**¿Qué otro ejemplo te gustaría explorar en la próxima clase?** 😊