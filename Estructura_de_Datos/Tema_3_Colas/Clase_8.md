Basado en tu solicitud y el syllabus de "Estructura de Datos", desarrollaré la **Clase 2** sobre aplicaciones de colas en Python, enfocada en un sistema de atención al cliente (e.g., un banco), incluyendo **definiciones y ejemplos** como se indica en la unidad 9.1 del syllabus ("Definición y ejemplos de colas"). La clase tendrá una duración de **1 hora y 20 minutos**, estará en **español**, y se alineará con los objetivos del curso, utilizando aprendizaje activo, resolución de problemas y prácticas de laboratorio (FORM-B2). Se usará una **cola circular** (unidad 9.6) para gestionar un número fijo de clientes, y el nivel será intermedio a avanzado (unidades 9.1–9.8). La clase incluirá un ejercicio práctico con código envuelto en la etiqueta `<xaiArtifact/>`.

---

### Clase 2: Definiciones, Ejemplos y Aplicación de Colas Circulares en un Sistema de Atención al Cliente
**Duración**: 1 hora y 20 minutos  
**Objetivo**: Los estudiantes comprenderán la definición de colas y colas circulares, explorarán ejemplos prácticos y aplicarán una cola circular en Python para simular un sistema de atención al cliente, gestionando datos en orden FIFO (First In, First Out) con capacidad limitada.  
**Nivel**: Intermedio a Avanzado (unidades 9.1–9.8 del syllabus).  
**Prerrequisitos**: Conocimiento de colas (FIFO, operaciones de encolar/desencolar), colas circulares y programación básica en Python.

#### Estructura de la Clase
1. **Introducción y Definiciones (10 minutos)**  
   - **Objetivo**: Explicar la definición de colas y colas circulares, destacando su utilidad en aplicaciones prácticas.  
   - **Actividades**:  
     - Breve exposición con diapositivas (según FORM-B2):  
       - **Definición de Cola**: Una estructura de datos lineal que opera bajo el principio FIFO (First In, First Out). Los elementos se añaden (encolan) al final y se eliminan (desencolan) desde el principio.  
       - **Definición de Cola Circular**: Una cola implementada en un arreglo de tamaño fijo donde el final y el principio están conectados, permitiendo reutilizar espacios vacíos tras desencolar. Usa índices `front` y `rear` para rastrear el primer y último elemento.  
       - Operaciones clave: `enqueue` (añadir), `dequeue` (eliminar), `is_empty`, `is_full`, `peek` (ver el primer elemento).  
       - Ventajas de la cola circular: Optimiza el uso de memoria al evitar desperdicio de espacio en arreglos.  
       - Ejemplo práctico: Sistema de turnos en un banco, donde solo un número limitado de clientes (e.g., 5) puede estar en espera.  
     - Plantear un problema: "¿Cómo usar una cola circular para gestionar turnos en un banco con capacidad limitada?"  
   - **Recursos**: Diapositivas, pizarrón acrílico.

2. **Ejemplos y Discusión (15 minutos)**  
   - **Objetivo**: Reforzar la comprensión de colas circulares mediante ejemplos y aprendizaje basado en problemas.  
   - **Actividades**:  
     - Mostrar ejemplos en el pizarrón:  
       - **Ejemplo 1**: Cola circular con capacidad 3.  
         - Estado inicial: Vacía (`front=-1`, `rear=-1`).  
         - Encolar "Cliente1": `items=["Cliente1", None, None]`, `front=0`, `rear=0`.  
         - Encolar "Cliente2": `items=["Cliente1", "Cliente2", None]`, `front=0`, `rear=1`.  
         - Desencolar: Eliminar "Cliente1" → `items=[None, "Cliente2", None]`, `front=1`, `rear=1`.  
         - Encolar "Cliente3": `items=[None, "Cliente2", "Cliente3"]`, `front=1`, `rear=2`.  
       - **Ejemplo 2**: Buffer circular en streaming de video, donde los datos se encolan y desencolan en un espacio fijo.  
     - Discusión en grupo: Los estudiantes proponen otros ejemplos (e.g., cola de tareas en un procesador, buffer de red).  
     - Pregunta guía: "¿Por qué usar una cola circular en lugar de una cola normal para un sistema de turnos?" (Respuesta: La cola circular evita desperdiciar espacio en un arreglo fijo).  
   - **Recursos**: Pizarrón, participación estudiantil.

3. **Ejercicio de Codificación: Simulador de Atención al Cliente con Cola Circular (35 minutos)**  
   - **Objetivo**: Implementar una cola circular en Python para simular un sistema de turnos en un banco con capacidad limitada.  
   - **Actividades**:  
     - **Problema**: Crear un sistema que gestione turnos de clientes (ID y tiempo de atención) en una cola circular con capacidad fija (e.g., 5 clientes). Los estudiantes extenderán el código para calcular el tiempo total de espera de los clientes en la cola.  
     - **Código Base**:  
       ```python
       class CircularQueue:
           def __init__(self, capacity):
               self.capacity = capacity
               self.items = [None] * capacity
               self.front = -1  # Índice del primer elemento
               self.rear = -1   # Índice del último elemento
               self.size = 0    # Número de elementos en la cola
           
           def is_empty(self):
               return self.size == 0
           
           def is_full(self):
               return self.size == self.capacity
           
           def enqueue(self, item):
               if self.is_full():
                   print("Cola llena, no se puede añadir cliente")
                   return
               if self.is_empty():
                   self.front = 0
               self.rear = (self.rear + 1) % self.capacity
               self.items[self.rear] = item
               self.size += 1
               print(f"Añadido: {item}")
           
           def dequeue(self):
               if self.is_empty():
                   print("Cola vacía, no hay clientes")
                   return None
               item = self.items[self.front]
               self.items[self.front] = None
               self.front = (self.front + 1) % self.capacity
               self.size -= 1
               if self.is_empty():
                   self.front = -1
                   self.rear = -1
               return item
           
           def peek(self):
               if not self.is_empty():
                   return self.items[self.front]
               return None

       class Customer:
           def __init__(self, id, time):
               self.id = id
               self.time = time
           
           def __str__(self):
               return f"Cliente {self.id}, Tiempo de atención: {self.time} min"

       class BankQueue:
           def __init__(self):
               self.queue = CircularQueue(5)  # Capacidad para 5 clientes
           
           def add_customer(self, id, time):
               customer = Customer(id, time)
               self.queue.enqueue(customer)
           
           def serve_customer(self):
               customer = self.queue.dequeue()
               if customer:
                   print(f"Atendiendo: {customer}")
               else:
                   print("No hay clientes en la cola")

       # Ejemplo de uso
       bank = BankQueue()
       bank.add_customer("C1", 5)
       bank.add_customer("C2", 3)
       bank.serve_customer()
       bank.add_customer("C3", 4)
       ```
     - **Tarea en clase**: Los estudiantes trabajan en parejas para añadir una función `total_waiting_time` que calcule el tiempo total de espera (suma de los tiempos de atención de todos los clientes en la cola). Ejemplo de extensión:  
       ```python
       def total_waiting_time(self):
           total = sum(customer.time for customer in self.queue.items if customer is not None)
           print(f"Tiempo total de espera: {total} minutos")
           return total
       ```
     - **Actividad de Laboratorio**: Usar Visual Studio Code o PyCharm (según FORM-B2) para probar el código. Los estudiantes ejecutan el programa, añaden clientes y verifican el tiempo total de espera.  
   - **Recursos**: Plataforma SAETA (Moodle), Visual Studio Code/PyCharm, guías de laboratorio.

4. **Cierre y Retroalimentación (20 minutos)**  
   - **Objetivo**: Consolidar el aprendizaje, conectar con el proyecto del curso y recoger retroalimentación.  
   - **Actividades**:  
     - Los estudiantes presentan su función `total_waiting_time` y muestran resultados.  
     - Discutir cómo las colas circulares pueden aplicarse en el proyecto final (FORM-C, e.g., app de gestión de turnos o buffer de datos).  
     - Proporcionar retroalimentación sobre la eficiencia y corrección del código (retroalimentación continua, FORM-B2).  
     - Tarea: Extender el sistema para priorizar clientes VIP (e.g., mover un cliente al frente de la cola).  
   - **Recursos**: Pizarrón, entregas vía SAETA.

---

### Notas Adicionales
- **Alineación con el Syllabus**:  
  - La clase cubre la definición y ejemplos de colas (unidad 9.1), colas circulares (unidad 9.6), operaciones (unidad 9.2) y aplicaciones (unidad 9.8), reforzando habilidades de programación en Python y resolución de problemas (FORM-B1).  
  - Se implementan metodologías de aprendizaje activo, basado en problemas y prácticas de laboratorio (FORM-B2).  
  - El ejercicio práctico prepara a los estudiantes para el proyecto final (FORM-C), que requiere usar estructuras de datos en aplicaciones reales.  
- **Recursos**: Diapositivas, código y guías se suben a SAETA (Moodle). Se usan Visual Studio Code o PyCharm, según los requerimientos del syllabus.  
- **Tarea**: La tarea fomenta la creatividad y refuerza el uso de colas circulares en contextos prácticos.  
- **Retroalimentación**: Se proporciona durante las presentaciones y mediante entregas en SAETA.

Si necesitas más ejemplos, ajustes en el código o un enfoque diferente, ¡avísame!