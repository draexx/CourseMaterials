### **Clase 3: Aplicaciones Prácticas de Listas y Matrices en Python**  
**Duración:** 1 hora 20 minutos  
**Objetivo:** Aplicar listas y matrices para resolver problemas reales, integrando todos los conceptos vistos en las clases anteriores.  

---

## **Parte 1: Repaso y Problemas con Listas (30 min)**  

### **1. Repaso Interactivo (10 min)**  
**Dinámica:** "Corrige el Código"  
- Se muestran 3 fragmentos de código con errores comunes (ej. índices fuera de rango, métodos mal usados).  
- Los estudiantes identifican y corrigen los errores en equipos.  

**Ejemplo:**  
```python
# Error 1: Índice fuera de rango
lista = [10, 20, 30]
print(lista[3])  # ¡Error! ¿Cómo solucionarlo?

# Error 2: Uso incorrecto de remove()
lista.remove(40)  # ¿Qué pasa si el elemento no existe?
```

---

### **2. Problemas Prácticos (20 min)**  
**Ejercicio 1:** Filtrar números pares de una lista.  
```python
numeros = [1, 2, 3, 4, 5, 6]
pares = [x for x in numeros if x % 2 == 0]
print(pares)  # [2, 4, 6]
```

**Ejercicio 2:** Eliminar duplicados de una lista.  
```python
lista = [1, 2, 2, 3, 4, 4, 5]
sin_duplicados = list(set(lista))  # Convertir a conjunto y volver a lista
print(sin_duplicados)  # [1, 2, 3, 4, 5]
```

---

## **Parte 2: Proyecto Integrador con Matrices (45 min)**  

### **1. Contexto del Problema**  
**Situación:**  
"Eres desarrollador en una tienda y debes procesar ventas semanales (7 días) de 3 productos (A, B, C) usando matrices."  

### **2. Implementación**  
**Paso 1:** Crear matriz de ventas (filas = días, columnas = productos).  
```python
ventas = [
    [10, 5, 8],   # Lunes
    [7, 12, 3],   # Martes
    [15, 6, 10],  # Miércoles
    # ... (completar para 7 días)
]
```

**Paso 2:** Calcular total de ventas por producto.  
```python
total_producto_A = sum(fila[0] for fila in ventas)
print("Ventas de A:", total_producto_A)
```

**Paso 3:** Encontrar el día con más ventas.  
```python
ventas_por_dia = [sum(fila) for fila in ventas]
dia_max = ventas_por_dia.index(max(ventas_por_dia)) + 1
print("Día con más ventas:", dia_max)  # Ej: 3 (miércoles)
```

### **3. Ampliación del Problema (Opcional)**  
- Agregar descuentos del 10% si las ventas de un producto superan 50 unidades.  
- Usar diccionarios para dar nombres a los productos (`{"A": 0, "B": 1, "C": 2}`).  

---

## **Cierre y Reflexión (5 min)**  
**Preguntas clave:**  
1. ¿En qué otros escenarios usarían matrices (ej. juegos, procesamiento de imágenes)?  
2. ¿Qué ventajas tienen las listas sobre otros tipos de datos?  

**Tarea Final:**  
- Crear un programa que simule un tablero de Tres en Raya (3x3) usando matrices, donde:  
  - "X" = 1, "O" = -1, vacío = 0.  
  - Verificar si hay un ganador (suma de filas/columnas/diagonales = 3 o -3).  

**Recursos Adicionales:**  
- [Tutorial de Matrices en Python (Real Python)](https://realpython.com/python-matrices/)  
- [Ejercicios de Listas (HackerRank)](https://www.hackerrank.com/domains/python/py-introduction)  

--- 

### **Rúbrica de Evaluación:**  
| Criterio               | Puntos |  
|------------------------|--------|  
| Participación activa   | 30%    |  
| Correcta implementación del proyecto | 50%    |  
| Creatividad en soluciones | 20%    |  

**Nota:** Esta clase cierra el ciclo de arreglos/listas con un enfoque 100% práctico, preparando a los estudiantes para temas avanzados (ordenamiento, búsqueda).