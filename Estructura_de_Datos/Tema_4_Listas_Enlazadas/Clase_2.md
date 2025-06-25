### **Clase 2: Operaciones Avanzadas en Listas Enlazadas Simples**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Dominar operaciones avanzadas: inversión de lista y eliminación por posición.  
2. Implementar algoritmos de búsqueda y gestión de memoria.  
3. Resolver problemas complejos con listas enlazadas.  

---

## **Parte 1: Teoría (20 minutos)**  

### **1. Inversión de Lista Enlazada**  
- **Concepto:** Revertir el orden de los nodos (el último se convierte en el primero).  
- **Enfoques:**  
  - **Iterativo:** Usar tres punteros (previo, actual, siguiente).  
  - **Recursivo:** Invertir el resto de la lista y ajustar punteros.  

### **2. Eliminación por Posición**  
- **Desafío:** Eliminar un nodo en posición `n` sin conocer el tamaño previo.  
- **Estrategia:**  
  1. Avanzar `n-1` nodos desde la cabeza.  
  2. Reenlazar el nodo anterior con el siguiente del nodo eliminado.  

### **3. Complejidad Algorítmica**  
| **Operación**         | **Complejidad** | **Explicación**               |  
|-----------------------|----------------|-------------------------------|  
| Inversión iterativa   | O(n)           | Recorre todos los nodos 1 vez |  
| Búsqueda por posición | O(n)           | En el peor caso recorre toda la lista |  

---

## **Parte 2: Implementación Práctica (40 minutos)**  

### **1. Inversión Iterativa**  
```python  
def invertir_iterativo(self):  
    previo = None  
    actual = self.cabeza  
    while actual:  
        siguiente = actual.siguiente  # Guardar referencia  
        actual.siguiente = previo     # Invertir enlace  
        previo = actual               # Mover previo  
        actual = siguiente            # Mover actual  
    self.cabeza = previo  # Nuevo cabeza es el último nodo  
```  
**Ejemplo:**  
```python  
lista = ListaEnlazadaSimple()  
lista.insertar_final(1)  
lista.insertar_final(2)  
lista.insertar_final(3)  
lista.invertir_iterativo()  
lista.recorrer()  # Salida: 3 -> 2 -> 1 -> None  
```  

### **2. Inversión Recursiva**  
```python  
def invertir_recursivo(self, nodo):  
    if not nodo or not nodo.siguiente:  
        return nodo  
    nueva_cabeza = self.invertir_recursivo(nodo.siguiente)  
    nodo.siguiente.siguiente = nodo  # Invertir enlace  
    nodo.siguiente = None  
    return nueva_cabeza  

# Llamada desde la lista  
lista.cabeza = invertir_recursivo(lista.cabeza)  
```  

### **3. Eliminar por Posición**  
```python  
def eliminar_posicion(self, pos):  
    if pos == 0:  
        self.eliminar_inicio()  
        return  
    actual = self.cabeza  
    contador = 0  
    while actual and contador < pos - 1:  
        actual = actual.siguiente  
        contador += 1  
    if not actual or not actual.siguiente:  
        return  # Posición inválida  
    actual.siguiente = actual.siguiente.siguiente  # Saltar nodo  
```  

---

## **Parte 3: Ejercicios Integrados (30 minutos)**  

### **Ejercicio 1: Encontrar el Nodo Medio**  
**Implementar función que devuelva el nodo medio (sin conocer tamaño):**  
```python  
def nodo_medio(self):  
    lento = self.cabeza  
    rapido = self.cabeza  
    while rapido and rapido.siguiente:  
        lento = lento.siguiente  
        rapido = rapido.siguiente.siguiente  
    return lento.dato if lento else None  
```  
**Prueba:**  
```python  
lista = ListaEnlazadaSimple()  
lista.insertar_final(10)  
lista.insertar_final(20)  
lista.insertar_final(30)  
print(lista.nodo_medio())  # 20  
```  

### **Ejercicio 2: Detectar Ciclos (Algoritmo de Floyd)**  
**Implementar detección de bucles:**  
```python  
def tiene_ciclo(self):  
    lento = self.cabeza  
    rapido = self.cabeza  
    while rapido and rapido.siguiente:  
        lento = lento.siguiente  
        rapido = rapido.siguiente.siguiente  
        if lento == rapido:  
            return True  
    return False  
```  
**Prueba:**  
```python  
# Crear ciclo manualmente  
nodo1 = Nodo(10)  
nodo2 = Nodo(20)  
nodo1.siguiente = nodo2  
nodo2.siguiente = nodo1  # Ciclo!  
lista.cabeza = nodo1  
print(lista.tiene_ciclo())  # True  
```  

### **Ejercicio 3: Unir Dos Listas Ordenadas**  
**Combinar listas manteniendo el orden:**  
```python  
def unir_listas_ordenadas(lista1, lista2):  
    dummy = Nodo(0)  # Nodo temporal  
    actual = dummy  
    while lista1 and lista2:  
        if lista1.dato < lista2.dato:  
            actual.siguiente = lista1  
            lista1 = lista1.siguiente  
        else:  
            actual.siguiente = lista2  
            lista2 = lista2.siguiente  
        actual = actual.siguiente  
    actual.siguiente = lista1 if lista1 else lista2  
    return dummy.siguiente  
```  

---

## **Parte 4: Cierre y Retroalimentación (10 minutos)**  
- **Discusión:**  
  - ¿Cuándo es útil la inversión recursiva vs. iterativa?  
  - ¿Cómo optimizarías la búsqueda en listas grandes?  
- **Tarea:**  
  - Implementar una lista que mantenga elementos ordenados al insertar.  
  - Resolver: [LeetCode #21 - Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/).  

---

### **Material Adicional**  
- **Lectura:** [Inversión de listas en GeeksforGeeks](https://www.geeksforgeeks.org/reverse-a-linked-list/).  
- **Video:** [Algoritmo del ciclo de Floyd](https://youtu.be/gBTe7lFR3vc).  

**¿Qué problema te gustaría resolver en la próxima clase?** 😊