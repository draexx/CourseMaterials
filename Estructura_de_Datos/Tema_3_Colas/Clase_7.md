Basado en tu solicitud, desarrollaré la **Clase 1** sobre aplicaciones de colas en Python, enfocada en un sistema de cola de impresión, incluyendo **definiciones y ejemplos** como se indica en el syllabus (unidad 9.1: "Definición y ejemplos de colas"). La clase tendrá una duración de **1 hora y 20 minutos**, estará en **español**, y se alineará con los objetivos del curso, utilizando aprendizaje activo, resolución de problemas y prácticas de laboratorio (FORM-B2). El nivel es intermedio (unidades 9.1–9.8), y se usará Python como lenguaje de programación, según el syllabus y tu preferencia. La clase incluirá un ejercicio práctico y un artefacto con el código envuelto en la etiqueta `<xaiArtifact/>`.

---

### Clase 1: Definiciones, Ejemplos y Aplicación de Colas en un Sistema de Cola de Impresión
**Duración**: 1 hora y 20 minutos  
**Objetivo**: Los estudiantes comprenderán la definición de colas, explorarán ejemplos prácticos y aplicarán colas en Python para simular un sistema de cola de impresión, gestionando datos en orden FIFO (First In, First Out).  
**Nivel**: Intermedio (unidades 9.1–9.8 del syllabus).  
**Prerrequisitos**: Conocimiento básico de Python y comprensión de estructuras de datos lineales (e.g., listas).

#### Estructura de la Clase
1. **Introducción y Definiciones (10 minutos)**  
   - **Objetivo**: Explicar la definición de colas y su importancia en aplicaciones prácticas.  
   - **Actividades**:  
     - Breve exposición con diapositivas (según FORM-B2) sobre la definición de colas:  
       - **Definición**: Una cola es una estructura de datos lineal que sigue el principio FIFO (First In, First Out), donde los elementos se insertan (encolan) al final y se eliminan (desencolan) desde el principio.  
       - Características clave:  
         - Operaciones principales: `enqueue` (añadir elemento), `dequeue` (eliminar elemento), `peek` (ver el primer elemento sin eliminarlo).  
         - Representaciones: estática (arreglo de tamaño fijo) y dinámica (lista enlazada).  
       - Ejemplos prácticos:  
         - Cola de impresión: Los trabajos de impresión se procesan en el orden en que llegan.  
         - Cola de atención al cliente: Los clientes son atendidos según su turno.  
         - Buffer en streaming: Los datos se procesan en el orden recibido.  
     - Plantear un problema: "¿Cómo podemos usar una cola para gestionar trabajos de impresión en una impresora?"  
   - **Recursos**: Diapositivas, pizarrón acrílico.

2. **Ejemplos y Discusión (15 minutos)**  
   - **Objetivo**: Reforzar la comprensión de colas mediante ejemplos y aprendizaje basado en problemas.  
   - **Actividades**:  
     - Mostrar ejemplos en el pizarrón:  
       - **Ejemplo 1**: Cola de impresión con 3 trabajos: ["Doc1", "Doc2", "Doc3"].  
         - Encolar: Añadir "Doc4" → ["Doc1", "Doc2", "Doc3", "Doc4"].  
         - Desencolar: Procesar "Doc1" → ["Doc2", "Doc3", "Doc4"].  
       - **Ejemplo 2**: Cola de clientes en un banco: ["Cliente1", "Cliente2"].  
         - Encolar: Añadir "Cliente3".  
         - Desencolar: Atender "Cliente1".  
     - Discusión en grupo: Los estudiantes proponen otros ejemplos de colas en la vida real (e.g., cola de tareas en un sistema operativo, cola de mensajes en un chat).  
     - Pregunta guía: "¿Qué pasaría si usáramos una pila en lugar de una cola para la impresión?" (Respuesta: Se procesarían los trabajos en orden inverso, rompiendo el principio FIFO).  
   - **Recursos**: Pizarrón, participación estudiantil.

3. **Ejercicio de Codificación: Simulador de Cola de Impresión (35 minutos)**  
   - **Objetivo**: Implementar una cola en Python para simular un sistema de cola de impresión, aplicando las operaciones `enqueue` y `dequeue`.  
   - **Actividades**:  
     - **Problema**: Crear un sistema que gestione trabajos de impresión (nombre del documento, número de páginas) en orden FIFO, mostrando el tiempo estimado de impresión (1 segundo por página). Los estudiantes extenderán el código para calcular el tiempo total de los trabajos en la cola.  
     - **Código Base**:  
       ```python
       class Queue:
           def __init__(self):
               self.items = []
           
           def is_empty(self):
               return len(self.items) == 0
           
           def enqueue(self, item):
               self.items.append(item)
           
           def dequeue(self):
               if not self.is_empty():
                   return self.items.pop(0)
               return None
           
           def peek(self):
               if not self.is_empty():
                   return self.items[0]
               return None

       class PrintJob:
           def __init__(self, name, pages):
               self.name = name
               self.pages = pages
           
           def __str__(self):
               return f"Documento: {self.name}, Páginas: {self.pages}"

       class Printer:
           def __init__(self):
               self.queue = Queue()
           
           def add_job(self, name, pages):
               job = PrintJob(name, pages)
               self.queue.enqueue(job)
               print(f"Añadido: {job}")
           
           def process_job(self):
               job = self.queue.dequeue()
               if job:
                   print(f"Procesando: {job}, Tiempo estimado: {job.pages} segundos")
               else:
                   print("No hay trabajos en la cola")

       # Ejemplo de uso
       printer = Printer()
       printer.add_job("Informe.pdf", 5)
       printer.add_job("Foto.jpg", 2)
       printer.process_job()
       printer.add_job("Carta.docx", 3)
       ```
     - **Tarea en clase**: Los estudiantes trabajan en parejas para añadir una función `total_time` que calcule el tiempo total de impresión (suma de páginas de todos los trabajos en la cola). Ejemplo de extensión:  
       ```python
       def total_time(self):
           total = sum(job.pages for job in self.queue.items if job is not None)
           print(f"Tiempo total de impresión: {total} segundos")
           return total
       ```
     - **Actividad de Laboratorio**: Usar Visual Studio Code o PyCharm (según FORM-B2) para probar el código. Los estudiantes ejecutan el programa, añaden trabajos y verifican el tiempo total.  
   - **Recursos**: Plataforma SAETA (Moodle), Visual Studio Code/PyCharm, guías de laboratorio.

4. **Cierre y Retroalimentación (20 minutos)**  
   - **Objetivo**: Consolidar el aprendizaje, conectar con el proyecto del curso y recoger retroalimentación.  
   - **Actividades**:  
     - Los estudiantes presentan su función `total_time` y muestran resultados.  
     - Discutir cómo las colas pueden aplicarse en el proyecto final (FORM-C, e.g., app de gestión de tareas con colas).  
     - Proporcionar retroalimentación sobre la eficiencia y corrección del código (retroalimentación continua, FORM-B2).  
     - Tarea: Extender el sistema para priorizar trabajos urgentes (e.g., mover un trabajo al frente de la cola).  
   - **Recursos**: Pizarrón, entregas vía SAETA.

---

### Notas Adicionales
- **Alineación con el Syllabus**:  
  - La clase cubre la definición y ejemplos de colas (unidad 9.1), operaciones (unidad 9.2) y aplicaciones (unidad 9.8), reforzando habilidades de programación en Python y resolución de problemas (FORM-B1).  
  - Se implementan metodologías de aprendizaje activo, basado en problemas y prácticas de laboratorio (FORM-B2).  
  - El ejercicio práctico prepara a los estudiantes para el proyecto final (FORM-C), que requiere usar estructuras de datos en aplicaciones reales.  
- **Recursos**: Diapositivas, código y guías se suben a SAETA (Moodle). Se usan Visual Studio Code o PyCharm, según los requerimientos del syllabus.  
- **Tarea**: La tarea fomenta la creatividad y refuerza el uso de colas en contextos prácticos.  
- **Retroalimentación**: Se proporciona durante las presentaciones y mediante entregas en SAETA.

Si necesitas ajustar el contenido, incluir más ejemplos o desarrollar otra aplicación, ¡avísame!