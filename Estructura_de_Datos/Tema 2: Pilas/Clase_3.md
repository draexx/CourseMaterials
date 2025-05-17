### **Clase 3: Pilas - Recursividad y Algoritmos Avanzados**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Conectar el concepto de pilas con la recursividad.  
2. Implementar algoritmos clásicos basados en pilas.  
3. Resolver problemas complejos con enfoque iterativo vs. recursivo.  

---

## **Parte 1: Teoría - Pilas y Recursividad (25 minutos)**  

### **1. La Pila de Llamadas (Call Stack)**  
- **Definición:** Estructura que registra las llamadas a funciones durante la ejecución de un programa.  
- **Ejemplo con Recursividad:**  
  ```python  
  def factorial(n):  
      if n == 0:  
          return 1  
      return n * factorial(n - 1)  # Cada llamada se apila  
  ```  
  **Visualización:**  
  ```  
  factorial(3)  
  │--> factorial(2)  
  │    │--> factorial(1)  
  │    │    │--> factorial(0)  # Caso base  
  ```  

- **Stack Overflow:** Ocurre cuando la pila de llamadas excede su límite (ej: recursión infinita).  

### **2. Conversión de Recursión a Iteración con Pilas**  
- **Por qué usarla:** Evitar desbordamiento y optimizar memoria.  
- **Estrategia:**  
  1. Apilar los parámetros de la llamada recursiva.  
  2. Procesar iterativamente desapilando.  

---

## **Parte 2: Ejercicios Prácticos (50 minutos)**  

### **Ejercicio 1: Factorial Iterativo con Pila**  
**Enunciado:** Implementar el cálculo del factorial usando una pila en lugar de recursión.  

**Solución:**  
```python  
def factorial_iterativo(n):  
    pila = []  
    resultado = 1  
    # Apilar los valores desde n hasta 1  
    for i in range(n, 0, -1):  
        pila.append(i)  
    # Desapilar y multiplicar  
    while pila:  
        resultado *= pila.pop()  
    return resultado  

print(factorial_iterativo(5))  # 120  
```  

**Discusión:** Comparar el uso de memoria vs. la versión recursiva.  

---

### **Ejercicio 2: Búsqueda en Directorios (DFS con Pila)**  
**Enunciado:** Simular la exploración de un árbol de directorios usando DFS iterativo.  

**Solución:**  
```python  
def explorar_directorios(root):  
    pila = [root]  
    while pila:  
        directorio_actual = pila.pop()  
        print(f"Explorando: {directorio_actual}")  
        # Simular subdirectorios (ej: datos predefinidos)  
        subdirectorios = obtener_subdirectorios(directorio_actual)  
        for subdir in reversed(subdirectorios):  # Para mantener el orden  
            pila.append(subdir)  

# Ejemplo de datos  
def obtener_subdirectorios(dir):  
    estructura = {  
        "C:/": ["C:/Documentos", "C:/Programas"],  
        "C:/Documentos": ["C:/Documentos/Personal"],  
        "C:/Programas": []  
    }  
    return estructura.get(dir, [])  

explorar_directorios("C:/")  
```  
**Salida:**  
```  
Explorando: C:/  
Explorando: C:/Documentos  
Explorando: C:/Documentos/Personal  
Explorando: C:/Programas  
```  

---

### **Ejercicio 3: Eliminar Elementos Adyacentes Duplicados**  
**Enunciado:** Dada una cadena, eliminar caracteres adyacentes duplicados usando una pila (ej: "abbaca" → "ca").  

**Solución:**  
```python  
def eliminar_duplicados(s):  
    pila = []  
    for char in s:  
        if pila and pila[-1] == char:  
            pila.pop()  
        else:  
            pila.append(char)  
    return "".join(pila)  

print(eliminar_duplicados("abbaca"))  # "ca"  
```  

**Aplicación:** Limpieza de datos o procesamiento de texto.  

---

### **Ejercicio 4: Torre de Hanoi (Versión Iterativa con Pila)**  
**Enunciado:** Resolver el problema de la Torre de Hanoi usando pilas en lugar de recursión.  

**Solución:**  
```python  
def hanoi_iterativo(n):  
    pila = []  
    pila.append((n, "A", "C", "B"))  # (discos, origen, destino, auxiliar)  
    while pila:  
        discos, origen, destino, auxiliar = pila.pop()  
        if discos == 1:  
            print(f"Mover disco 1 de {origen} a {destino}")  
        else:  
            pila.append((discos - 1, auxiliar, destino, origen))  
            pila.append((1, origen, destino, auxiliar))  
            pila.append((discos - 1, origen, auxiliar, destino))  

hanoi_iterativo(3)  
```  
**Salida:**  
```  
Mover disco 1 de A a C  
Mover disco 2 de A a B  
Mover disco 1 de C a B  
Mover disco 3 de A a C  
Mover disco 1 de B a A  
Mover disco 2 de B a C  
Mover disco 1 de A a C  
```  

---

## **Parte 3: Cierre y Reflexión (5 minutos)**  
- **Preguntas clave:**  
  - ¿Cuándo preferirías una solución iterativa con pilas sobre una recursiva?  
  - ¿Qué problemas cotidianos podrían modelarse con pilas?  
- **Desafío opcional:**  
  - Implementar un algoritmo para calcular el área de histogramas usando pilas.  

---

### **Material Adicional**  
- **Lectura:** [Call Stack en Python](https://realpython.com/python-call-stack/).  
- **Video:** [Recursión vs. Iteración](https://youtu.be/X32dce7_D48).  

**¿Listos para la próxima clase? Exploraremos pilas en sistemas operativos y compiladores.** 😊