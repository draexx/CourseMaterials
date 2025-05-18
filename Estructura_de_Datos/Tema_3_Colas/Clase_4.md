### **Clase 4: Colas - Estructuras Derivadas y Aplicaciones Avanzadas**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Explorar estructuras derivadas de colas: *deques* (colas dobles) y colas basadas en listas enlazadas.  
2. Aplicar colas en problemas avanzados de algoritmos y sistemas.  
3. Resolver ejercicios prácticos con implementaciones eficientes.  

---

## **Parte 1: Ampliación Teórica (25 minutos)**  

### **1. Deques (Colas Dobles)**  
**Definición:**  
- Estructura que permite inserción/eliminación al **frente** y **final** en tiempo constante (`O(1)`).  
- **Operaciones clave:**  
  - `append_left(x)`, `append_right(x)`.  
  - `pop_left()`, `pop_right()`.  
- **Aplicaciones:**  
  - Historial de navegación (adelante/atrás).  
  - Algoritmos de caché (LRU Cache).  

**Implementación en Python:**  
```python  
from collections import deque  

# Uso de deque en Python  
historial = deque()  
historial.append("página1")  
historial.append("página2")  
historial.appendleft("página0")  
print(historial.pop())       # "página2"  
print(historial.popleft())   # "página0"  
```  

---

### **2. Colas con Listas Enlazadas**  
**Ventajas:**  
- Inserción/eliminación en `O(1)` sin desplazamientos de memoria.  
- **Nodos:**  
  ```python  
  class Nodo:  
      def __init__(self, dato):  
          self.dato = dato  
          self.siguiente = None  

  class ColaEnlazada:  
      def __init__(self):  
          self.frente = self.final = None  

      def enqueue(self, dato):  
          nuevo_nodo = Nodo(dato)  
          if self.final:  
              self.final.siguiente = nuevo_nodo  
          else:  
              self.frente = nuevo_nodo  
          self.final = nuevo_nodo  

      def dequeue(self):  
          if self.frente:  
              dato = self.frente.dato  
              self.frente = self.frente.siguiente  
              if not self.frente:  
                  self.final = None  
              return dato  
          raise IndexError("Cola vacía")  
  ```  

---

## **Parte 2: Ejercicios Prácticos (45 minutos)**  

### **Ejercicio 1: Historial de Navegación con Deque**  
**Enunciado:**  
Implementar un historial que permita navegar hacia adelante y atrás, con límite de 5 páginas.  

**Solución:**  
```python  
class Navegador:  
    def __init__(self):  
        self.historial_atras = deque()  
        self.historial_adelante = deque()  
        self.pagina_actual = "Inicio"  

    def visitar(self, pagina):  
        self.historial_atras.append(self.pagina_actual)  
        self.pagina_actual = pagina  
        self.historial_adelante = deque()  # Limpiar al visitar nueva página  
        if len(self.historial_atras) > 5:  
            self.historial_atras.popleft()  

    def atras(self):  
        if self.historial_atras:  
            self.historial_adelante.append(self.pagina_actual)  
            self.pagina_actual = self.historial_atras.pop()  

    def adelante(self):  
        if self.historial_adelante:  
            self.historial_atras.append(self.pagina_actual)  
            self.pagina_actual = self.historial_adelante.pop()  

# Uso  
nav = Navegador()  
nav.visitar("google.com")  
nav.visitar("youtube.com")  
nav.atras()  
print(nav.pagina_actual)  # "google.com"  
nav.adelante()  
print(nav.pagina_actual)  # "youtube.com"  
```  

---

### **Ejercicio 2: Número de Islas (BFS con Colas)**  
**Enunciado:**  
Contar el número de islas en una matriz usando BFS (considerando "1" como tierra y "0" como agua).  

**Solución:**  
```python  
from collections import deque  

def numero_islas(matriz):  
    if not matriz:  
        return 0  
    filas, cols = len(matriz), len(matriz[0])  
    contador = 0  

    for i in range(filas):  
        for j in range(cols):  
            if matriz[i][j] == "1":  
                contador += 1  
                cola = deque([(i, j)])  
                matriz[i][j] = "0"  # Marcar como visitado  
                while cola:  
                    x, y = cola.popleft()  
                    for dx, dy in [(-1, 0), (1, 0), (0, -1), (0, 1)]:  
                        nx, ny = x + dx, y + dy  
                        if 0 <= nx < filas and 0 <= ny < cols and matriz[nx][ny] == "1":  
                            cola.append((nx, ny))  
                            matriz[nx][ny] = "0"  
    return contador  

matriz = [  
    ["1", "1", "0", "0"],  
    ["1", "0", "0", "0"],  
    ["0", "0", "1", "1"],  
    ["0", "0", "0", "1"]  
]  
print(numero_islas(matriz))  # 3  
```  

---

### **Ejercicio 3: Buffer de Datos con Cola Circular**  
**Enunciado:**  
Implementar un buffer de tamaño fijo que sobrescriba los datos más antiguos al llenarse.  

**Solución:**  
```python  
class BufferCircular:  
    def __init__(self, capacidad):  
        self.capacidad = capacidad  
        self.buffer = deque(maxlen=capacidad)  

    def agregar_dato(self, dato):  
        self.buffer.append(dato)  

    def obtener_datos(self):  
        return list(self.buffer)  

# Uso  
buffer = BufferCircular(3)  
buffer.agregar_dato("A")  
buffer.agregar_dato("B")  
buffer.agregar_dato("C")  
buffer.agregar_dato("D")  # Sobrescribe "A"  
print(buffer.obtener_datos())  # ["B", "C", "D"]  
```  

---

## **Parte 3: Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿Qué ventajas tiene usar `deque` sobre una lista estándar?  
  - ¿Cómo manejarías un buffer en tiempo real con hilos?  
- **Tarea:**  
  - Implementar un sistema de tickets usando colas enlazadas que priorice clientes VIP.  

---

### **Material Adicional**  
- **Lectura:** [Documentación oficial de `deque`](https://docs.python.org/3/library/collections.html#collections.deque).  
- **Video:** [BFS en problemas de matrices](https://youtu.be/KiCBXu4P-2Y).  

**¿Qué otro problema te interesa resolver con colas?** 😊