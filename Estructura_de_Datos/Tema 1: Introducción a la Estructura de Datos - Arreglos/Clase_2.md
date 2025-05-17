### **Clase 2: Operaciones Avanzadas con Listas y Arreglos Multidimensionales (Python)**  
**Duración:** 1 hora 20 minutos  
**Objetivo:** Dominar operaciones avanzadas con listas (similares a arreglos) y comprender el uso de listas multidimensionales (matrices) en Python.  

---

## **Parte 1: Repaso y Operaciones Avanzadas con Listas (40 min)**  

### **1. Repaso Rápido (10 min)**  
**Preguntas clave:**  
- ¿Qué es una lista en Python?  
- ¿Cómo se accede a un elemento específico?  
- ¿Qué métodos conocen para modificar listas?  

**Ejemplo de repaso:**  
```python
frutas = ["manzana", "banana", "naranja"]
print(frutas[1])  # ¿Qué imprime?
frutas.append("uva")  # ¿Cómo queda la lista?
```

---

### **2. Operaciones Avanzadas (30 min)**  

#### **A. Métodos Esenciales**  
| Método         | Acción                              | Ejemplo                          |
|----------------|-------------------------------------|----------------------------------|
| `.insert(i, x)`| Inserta `x` en la posición `i`      | `frutas.insert(1, "kiwi")`       |
| `.pop(i)`      | Elimina y retorna el elemento en `i`| `eliminado = frutas.pop(2)`      |
| `.remove(x)`   | Elimina la primera aparición de `x` | `frutas.remove("banana")`        |
| `.reverse()`   | Invierte el orden de la lista       | `frutas.reverse()`               |
| `.sort()`      | Ordena la lista (ascendente)        | `frutas.sort()`                  |

**Ejercicio práctico:**  
```python
# Lista de números
numeros = [5, 2, 8, 1, 9]

# 1. Ordenar la lista
numeros.sort()
print("Ordenada:", numeros)  # [1, 2, 5, 8, 9]

# 2. Insertar el número 3 en la posición 2
numeros.insert(2, 3)
print("Con inserción:", numeros)  # [1, 2, 3, 5, 8, 9]

# 3. Eliminar el número 5
numeros.remove(5)
print("Sin el 5:", numeros)  # [1, 2, 3, 8, 9]
```

#### **B. Slicing (Rebanado)**  
- Sintaxis: `lista[inicio:fin:paso]`  
- Ejemplos:  
  ```python
  letras = ['a', 'b', 'c', 'd', 'e']
  print(letras[1:4])    # ['b', 'c', 'd']
  print(letras[::2])    # ['a', 'c', 'e'] (paso de 2)
  print(letras[::-1])   # ['e', 'd', 'c', 'b', 'a'] (inversa)
  ```

---

## **Parte 2: Listas Multidimensionales (Matrices) (35 min)**  

### **1. Concepto de Matriz**  
- **Definición:** Lista de listas, donde cada sublista representa una fila.  
- **Analogía:** Tabla de Excel (filas y columnas).  

### **2. Creación y Acceso**  
```python
# Matriz 2x3 (2 filas, 3 columnas)
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

# Acceder al elemento en fila 1, columna 2 (valor: 6)
print(matriz[1][2])  # 6
```

### **3. Operaciones Básicas**  
**Ejemplo:** Sumar todas las filas de una matriz.  
```python
matriz = [[1, 2], [3, 4], [5, 6]]
suma_filas = [sum(fila) for fila in matriz]
print("Suma por filas:", suma_filas)  # [3, 7, 11]
```

**Ejercicio guiado:**  
Crear una matriz 3x3 e implementar:  
1. Suma de todos los elementos.  
2. Encontrar el valor máximo.  

```python
matriz = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

# Suma total
suma_total = sum(sum(fila) for fila in matriz)
print("Suma total:", suma_total)  # 450

# Valor máximo
maximo = max(max(fila) for fila in matriz)
print("Máximo:", maximo)  # 90
```

---

## **Cierre y Tarea (5 min)**  
**Resumen:**  
- Métodos avanzados: `insert()`, `pop()`, `sort()`, slicing.  
- Matrices: Listas de listas para datos tabulares.  

**Tarea:**  
1. Crear una lista de números y aplicar 3 métodos diferentes.  
2. Definir una matriz 2x2 y calcular su traza (suma de diagonal principal).  

**Recursos:**  
- [Python Lists (W3Schools)](https://www.w3schools.com/python/python_lists.asp)  
- [Matrices en Python (GeeksforGeeks)](https://www.geeksforgeeks.org/python-matrices/)  

**Evaluación:**  
- Participación en ejercicios (60%).  
- Entrega de tarea (40%).  

--- 

### **Notas Adicionales:**  
- Enfatizar que Python no tiene "arreglos" nativos, pero las listas son su versión flexible.  
- Para proyectos científicos, mencionar brevemente la librería `NumPy` (opcional).  

Esta clase combina teoría y práctica para asegurar la comprensión de estructuras clave en Python.