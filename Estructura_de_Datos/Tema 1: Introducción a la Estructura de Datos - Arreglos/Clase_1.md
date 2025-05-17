### **Clase 1: Introducción a Estructuras de Datos y Arreglos (Python)**  
**Duración:** 1 hora 20 minutos  
**Objetivo:** Comprender qué son las estructuras de datos, su clasificación y los fundamentos de listas (arreglos en Python), incluyendo su declaración y operaciones básicas.  

---

### **1. Introducción (15 minutos)**  
**Definiciones clave:**  
- **Estructura de datos:** Forma organizada de almacenar y gestionar datos para acceder y modificarlos eficientemente.  
  - *Ejemplo:*  
    - **Sin estructura:** Notas de estudiantes en papeles sueltos.  
    - **Con estructura:** Notas almacenadas en una lista ordenada en Python.  
- **Tipos de datos en Python:**  
  - **Simples:** `int`, `float`, `str`, `bool`.  
  - **Compuestos:**  
    - **Listas** (similares a arreglos, pero dinámicas).  
    - **Tuplas**, **diccionarios**, **conjuntos**.  

**Importancia:**  
- Permiten resolver problemas complejos de manera eficiente (ej. procesar grandes volúmenes de datos).  
- Son la base de algoritmos como búsqueda y ordenación.  

---

### **2. Listas en Python: Concepto y Sintaxis (25 minutos)**  
**Definición:**  
- Colección ordenada y mutable de elementos (pueden ser de distintos tipos).  
- **Características:**  
  - Tamaño dinámico (pueden crecer o reducirse).  
  - Índices comienzan en `0`.  

**Sintaxis en Python:**  
```python
# Declaración
numeros = [10, 20, 30, 40, 50]  # Lista de enteros
datos_mixtos = [1, "Python", True, 3.14]  # Lista con tipos mezclados

# Acceso
print(numeros[0])  # Output: 10 (primer elemento)
numeros[2] = 99    # Modificación: [10, 20, 99, 40, 50]

# Operaciones básicas
numeros.append(60)  # Añade 60 al final
print(len(numeros)) # Longitud: 6
```

**Ejemplo visual:**  
```
Índices:   0      1      2      3      4  
Valores: [10,   "Python",   True,   3.14,   60]  
```

**Analogía:**  
- Una lista es como una caja de herramientas donde cada compartimento (índice) guarda una herramienta (dato).  

---

### **3. Ejercicio Práctico (30 minutos)**  
**Actividad:** Crear un programa que almacene y procese notas de estudiantes.  
```python
# Paso 1: Crear lista de notas
notas = [15, 18, 12, 20, 10]

# Paso 2: Calcular promedio
promedio = sum(notas) / len(notas)
print(f"Promedio: {promedio}")

# Paso 3: Añadir nueva nota
notas.append(17)
print(f"Notas actualizadas: {notas}")

# Paso 4: Buscar la nota más alta
print(f"Nota máxima: {max(notas)}")
```

**Discusión:**  
- ¿Qué pasa si queremos eliminar una nota? (Usar `notas.remove(12)`).  
- ¿Cómo acceder al último elemento? (`notas[-1]`).  

---

### **4. Cierre y Tarea (10 minutos)**  
**Resumen:**  
- Las listas son estructuras flexibles para almacenar datos secuenciales.  
- Operaciones clave: `append()`, `len()`, acceso por índice.  

**Tarea:**  
- Investigar otras operaciones de listas (`insert()`, `pop()`, slicing).  
- Escribir un programa que guarde nombres de frutas y permita añadir/buscar elementos.  

**Material de apoyo:**  
- [Documentación oficial de listas en Python](https://docs.python.org/3/tutorial/datastructures.html).  

--- 

### **Evaluación:**  
- Participación en el ejercicio práctico (50%).  
- Entrega de la tarea (50%).  

**Nota:** Esta clase sienta las bases para temas avanzados como listas multidimensionales (matrices) y algoritmos de ordenación.