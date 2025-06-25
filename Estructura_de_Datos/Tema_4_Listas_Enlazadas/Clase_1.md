### **Clase 1: Introducción a Listas Enlazadas Simples**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Comprender la estructura fundamental de nodos y punteros.  
2. Implementar operaciones básicas: inserción, eliminación y recorrido.  
3. Comparar listas enlazadas con arreglos tradicionales.  

---

## **Parte 1: Teoría (30 minutos)**  

### **1. Definición de Lista Enlazada Simple**  
- **Estructura:** Secuencia de nodos donde cada nodo contiene:  
  - **Dato:** Valor almacenado.  
  - **Puntero:** Referencia al siguiente nodo (`siguiente`).  
- **Ventajas vs. Arreglos:**  
  - Inserción/eliminación eficiente en tiempo O(1) en el inicio.  
  - Tamaño dinámico (no requiere redimensionamiento).  
- **Desventajas:**  
  - Acceso secuencial (no acceso aleatorio O(1) como en arreglos).  

**Analogía:**  
- Como un tren de vagones, donde cada vagón (nodo) está conectado solo al siguiente.  

### **2. Operaciones Básicas**  
| **Operación**       | **Descripción**                              | **Complejidad** |  
|---------------------|---------------------------------------------|----------------|  
| `insertar_inicio(x)`| Añade `x` al inicio de la lista.            | O(1)           |  
| `eliminar_inicio()` | Elimina el primer nodo.                     | O(1)           |  
| `recorrer()`        | Imprime todos los elementos.                | O(n)           |  
| `buscar(x)`         | Devuelve True si `x` está en la lista.      | O(n)           |  

---

## **Parte 2: Implementación en Python (20 minutos)**  

### **Clase Nodo y Lista Enlazada Simple**  
```python  
class Nodo:  
    def __init__(self, dato):  
        self.dato = dato  
        self.siguiente = None  

class ListaEnlazadaSimple:  
    def __init__(self):  
        self.cabeza = None  # Puntero al primer nodo  

    def insertar_inicio(self, dato):  
        nuevo_nodo = Nodo(dato)  
        nuevo_nodo.siguiente = self.cabeza  
        self.cabeza = nuevo_nodo  

    def eliminar_inicio(self):  
        if self.cabeza:  
            self.cabeza = self.cabeza.siguiente  

    def recorrer(self):  
        actual = self.cabeza  
        while actual:  
            print(actual.dato, end=" -> ")  
            actual = actual.siguiente  
        print("None")  
```  

**Ejemplo de uso:**  
```python  
lista = ListaEnlazadaSimple()  
lista.insertar_inicio(3)  
lista.insertar_inicio(2)  
lista.insertar_inicio(1)  
lista.recorrer()  # Salida: 1 -> 2 -> 3 -> None  
lista.eliminar_inicio()  
lista.recorrer()  # Salida: 2 -> 3 -> None  
```  

---

## **Parte 3: Ejercicios Prácticos (30 minutos)**  

### **Ejercicio 1: Insertar al Final**  
**Implementar el método `insertar_final(dato)`:**  
```python  
def insertar_final(self, dato):  
    nuevo_nodo = Nodo(dato)  
    if not self.cabeza:  # Lista vacía  
        self.cabeza = nuevo_nodo  
    else:  
        actual = self.cabeza  
        while actual.siguiente:  # Avanzar hasta el último nodo  
            actual = actual.siguiente  
        actual.siguiente = nuevo_nodo  
```  
**Prueba:**  
```python  
lista.insertar_final(4)  
lista.recorrer()  # Salida: 2 -> 3 -> 4 -> None  
```  

---

### **Ejercicio 2: Búsqueda de Elementos**  
**Implementar el método `buscar(x)`:**  
```python  
def buscar(self, x):  
    actual = self.cabeza  
    while actual:  
        if actual.dato == x:  
            return True  
        actual = actual.siguiente  
    return False  
```  
**Prueba:**  
```python  
print(lista.buscar(3))  # True  
print(lista.buscar(5))  # False  
```  

---

### **Ejercicio 3: Eliminar por Valor**  
**Implementar el método `eliminar(x)`:**  
```python  
def eliminar(self, x):  
    if not self.cabeza:  
        return  

    if self.cabeza.dato == x:  # Caso especial: eliminar cabeza  
        self.cabeza = self.cabeza.siguiente  
        return  

    actual = self.cabeza  
    while actual.siguiente:  
        if actual.siguiente.dato == x:  
            actual.siguiente = actual.siguiente.siguiente  
            return  
        actual = actual.siguiente  
```  
**Prueba:**  
```python  
lista.eliminar(3)  
lista.recorrer()  # Salida: 2 -> 4 -> None  
```  

---

## **Parte 4: Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿Cuándo es preferible usar una lista enlazada sobre un arreglo?  
  - ¿Cómo manejaríamos memoria en lenguajes sin recolector de basura (ej: C++)?  
- **Tarea:**  
  - Implementar una función que devuelva el tamaño de la lista.  
  - Investigar aplicaciones reales de listas enlazadas (ej: sistema de archivos).  

---

### **Material Adicional**  
- **Video:** [Listas Enlazadas en 5 minutos](https://youtu.be/WwfhLC16bis)  
- **Simulador interactivo:** [Linked List Visualizer](https://visualgo.net/en/list)  

**¿Qué dudas o temas te gustaría profundizar en la próxima clase?** 😊