### **Clase 5: Colas en Sistemas Reales - Proyecto Integrador**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Implementar un sistema de gestión de tareas con colas FIFO y prioritarias.  
2. Analizar el uso de colas en arquitecturas de software reales.  
3. Resolver problemas de concurrencia básicos con colas.  

---

## **Parte 1: Teoría Avanzada (25 minutos)**  

### **1. Colas en Arquitecturas de Software**  
| **Aplicación**         | **Uso de Colas**                          | **Ejemplo**                     |  
|-------------------------|------------------------------------------|---------------------------------|  
| **Microservicios**      | Comunicación entre servicios (RabbitMQ)  | Pedidos en e-commerce           |  
| **Procesamiento Batch** | Encolar trabajos pesados                 | Generación de reportes          |  
| **Sistemas en Tiempo Real** | Buffer de datos (Kafka)              | Monitoreo de sensores           |  

### **2. Concurrencia con Colas**  
- **Problema:** Múltiples hilos/productores y consumidores.  
- **Solución:** Uso de colas thread-safe:  
  ```python  
  import queue  
  cola_segura = queue.Queue(maxsize=10)  # Thread-safe por defecto  
  ```

---

## **Parte 2: Proyecto Práctico (50 minutos)**  

### **Sistema de Gestión de Tareas**  
**Requisitos:**  
- Dos colas: Normal (FIFO) y Urgente (Prioridad).  
- Múltiples "workers" que consumen tareas.  
- Estadísticas de procesamiento.  

**Implementación:**  
```python  
import threading  
import time  
import queue  

class GestorTareas:  
    def __init__(self):  
        self.cola_normal = queue.Queue()  
        self.cola_urgente = queue.PriorityQueue()  
        self.estadisticas = {"normal": 0, "urgente": 0}  

    def agregar_tarea(self, nombre, urgente=False, prioridad=0):  
        if urgente:  
            self.cola_urgente.put((prioridad, nombre))  
        else:  
            self.cola_normal.put(nombre)  

    def worker(self):  
        while True:  
            # Priorizar tareas urgentes  
            if not self.cola_urgente.empty():  
                prioridad, tarea = self.cola_urgente.get()  
                print(f"[URGENTE] Procesando: {tarea}")  
                self.estadisticas["urgente"] += 1  
            elif not self.cola_normal.empty():  
                tarea = self.cola_normal.get()  
                print(f"[NORMAL] Procesando: {tarea}")  
                self.estadisticas["normal"] += 1  
            time.sleep(1)  # Simular trabajo  

# Uso  
gestor = GestorTareas()  

# Llenar colas  
gestor.agregar_tarea("Backup diario")  
gestor.agregar_tarea("Error crítico", urgente=True, prioridad=1)  

# Iniciar workers  
for _ in range(2):  # 2 workers  
    hilo = threading.Thread(target=gestor.worker, daemon=True)  
    hilo.start()  

# Mantener el programa activo  
time.sleep(5)  
print("Estadísticas:", gestor.estadisticas)  
```  

**Salida:**  
```  
[URGENTE] Procesando: Error crítico  
[NORMAL] Procesando: Backup diario  
Estadísticas: {'normal': 1, 'urgente': 1}  
```  

---

## **Parte 3: Ejercicios Adicionales (20 minutos)**  

### **Ejercicio 1: Buffer Circular con Thread-Safety**  
**Enunciado:** Implementar un buffer que almacene los últimos 5 mensajes de un chat con protección contra accesos concurrentes.  

**Solución:**  
```python  
class BufferChat:  
    def __init__(self):  
        self.buffer = deque(maxlen=5)  
        self.lock = threading.Lock()  

    def agregar_mensaje(self, mensaje):  
        with self.lock:  
            self.buffer.append(mensaje)  

    def obtener_mensajes(self):  
        with self.lock:  
            return list(self.buffer)  
```  

---

### **Ejercicio 2: Rate Limiter con Cola**  
**Enunciado:** Limitar a 10 solicitudes por minuto usando una cola temporal.  

**Solución:**  
```python  
class RateLimiter:  
    def __init__(self):  
        self.cola_tiempos = deque()  

    def permitir_solicitud(self):  
        ahora = time.time()  
        # Eliminar registros mayores a 1 minuto  
        while self.cola_tiempos and ahora - self.cola_tiempos[0] > 60:  
            self.cola_tiempos.popleft()  
        if len(self.cola_tiempos) < 10:  
            self.cola_tiempos.append(ahora)  
            return True  
        return False  
```  

---

## **Cierre y Retroalimentación (5 minutos)**  
- **Discusión:**  
  - ¿Cómo escalarían este sistema para 1000 workers?  
  - Ventajas de usar colas externas (Redis, RabbitMQ) vs. en memoria.  
- **Tarea Final:**  
  - Implementar un sistema de notificaciones con prioridad y reintentos.  

---

### **Material Adicional**  
- **Libro:** ["Designing Data-Intensive Applications" - Martin Kleppmann](https://dataintensive.net/) (Cap. 4).  
- **Herramienta:** [Redis como cola distribuida](https://redis.io/docs/data-types/streams/).  

**¿Qué componente te gustaría profundizar en la próxima clase?** 😊