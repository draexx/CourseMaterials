### **Clase 3: Listas Doblemente Enlazadas - Conceptos y Aplicaciones**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Comprender la estructura de nodos con enlaces dobles (anterior/siguiente).  
2. Implementar operaciones básicas y avanzadas.  
3. Analizar ventajas frente a listas simples.  

---

## **Parte 1: Teoría (25 minutos)**  

### **1. Definición de Lista Doblemente Enlazada**  
- **Estructura:**  
  ```python
  class NodoDoble:
      def __init__(self, dato):
          self.dato = dato
          self.anterior = None  # Nuevo puntero
          self.siguiente = None
  ```
- **Ventajas:**  
  - Recorrido bidireccional (adelante/atrás).  
  - Eliminación más eficiente en nodos específicos (O(1) si se tiene referencia).  
- **Desventajas:**  
  - Mayor consumo de memoria (por puntero adicional).  

### **2. Operaciones Clave**  
| **Operación**         | **Complejidad** | **Descripción**                  |
|-----------------------|----------------|----------------------------------|
| `insertar_final(x)`   | O(1)*          | *Si se mantiene puntero al final |
| `eliminar(nodo)`      | O(1)           | Eliminación directa con referencia |
| `buscar_adelante(x)`  | O(n)           | Igual que lista simple           |

---

## **Parte 2: Implementación Práctica (35 minutos)**  

### **1. Clase Completa de Lista Doblemente Enlazada**  
```python
class ListaDoblementeEnlazada:
    def __init__(self):
        self.cabeza = None
        self.cola = None  # Nuevo puntero para acceso rápido al final

    def insertar_final(self, dato):
        nuevo_nodo = NodoDoble(dato)
        if not self.cabeza:  # Lista vacía
            self.cabeza = self.cola = nuevo_nodo
        else:
            nuevo_nodo.anterior = self.cola
            self.cola.siguiente = nuevo_nodo
            self.cola = nuevo_nodo

    def eliminar_nodo(self, nodo):
        if nodo.anterior:  # No es el primer nodo
            nodo.anterior.siguiente = nodo.siguiente
        else:
            self.cabeza = nodo.siguiente
        
        if nodo.siguiente:  # No es el último nodo
            nodo.siguiente.anterior = nodo.anterior
        else:
            self.cola = nodo.anterior
```

### **2. Ejemplo: Historial de Navegación**  
```python
historial = ListaDoblementeEnlazada()
historial.insertar_final("google.com")
historial.insertar_final("youtube.com")
historial.insertar_final("github.com")

# Navegar hacia atrás (usando puntero 'anterior')
actual = historial.cola
while actual:
    print(actual.dato, end=" <- ")
    actual = actual.anterior
# Salida: github.com <- youtube.com <- google.com <-
```

---

## **Parte 3: Ejercicios Avanzados (30 minutos)**  

### **Ejercicio 1: Implementar Inserción Ordenada**  
**Objetivo:** Mantener la lista ordenada al insertar.  
```python
def insertar_ordenado(self, dato):
    nuevo_nodo = NodoDoble(dato)
    if not self.cabeza:  # Lista vacía
        self.cabeza = self.cola = nuevo_nodo
    elif dato <= self.cabeza.dato:  # Insertar al inicio
        nuevo_nodo.siguiente = self.cabeza
        self.cabeza.anterior = nuevo_nodo
        self.cabeza = nuevo_nodo
    else:  # Buscar posición
        actual = self.cabeza
        while actual.siguiente and actual.siguiente.dato < dato:
            actual = actual.siguiente
        # Insertar después de 'actual'
        nuevo_nodo.siguiente = actual.siguiente
        nuevo_nodo.anterior = actual
        if actual.siguiente:
            actual.siguiente.anterior = nuevo_nodo
        else:
            self.cola = nuevo_nodo
        actual.siguiente = nuevo_nodo
```

### **Ejercicio 2: Palíndromo con Lista Doble**  
**Verificar si una lista es palíndromo:**  
```python
def es_palindromo(lista):
    izquierda = lista.cabeza
    derecha = lista.cola
    while izquierda != derecha and derecha.siguiente != izquierda:
        if izquierda.dato != derecha.dato:
            return False
        izquierda = izquierda.siguiente
        derecha = derecha.anterior
    return True
```

---

## **Parte 4: Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿Cuándo preferirías una lista doble sobre una simple? *(Ej: reproductor de música con "anterior/siguiente")*  
  - ¿Cómo implementarías un "undo/redo" avanzado?  
- **Tarea:**  
  - Implementar un carrito de compras con navegación bidireccional.  

---

### **Material Adicional**  
- **Visualización:** [Doubly Linked List Visualizer](https://visualgo.net/en/list)  
- **Video:** [Listas Dobles en 5 Minutos](https://youtu.be/8Ls1RqHCOPw)  

**¿Qué aplicación te gustaría implementar en la próxima clase?** 😊