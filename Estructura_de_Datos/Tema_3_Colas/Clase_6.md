### **Clase 6: Proyecto Final - Sistema de Gestión de Tareas Distribuidas con Colas**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Integrar todos los conceptos de colas en un proyecto realista.  
2. Implementar un sistema distribuido con múltiples consumidores.  
3. Optimizar el rendimiento y manejar fallos.  

---

## **Parte 1: Definiciones Clave (20 minutos)**  

### **1. Colas Distribuidas**  
- **Concepto:** Colas que operan en múltiples servidores o procesos (ej: RabbitMQ, Kafka).  
- **Ventajas:**  
  - Tolerancia a fallos.  
  - Escalabilidad horizontal.  

### **2. Patrón Producer-Consumer**  
- **Roles:**  
  - *Producer:* Genera tareas y las encola.  
  - *Consumer:* Procesa tareas de la cola.  
- **Ejemplo:**  
  ```python  
  import threading  
  import queue  

  cola = queue.Queue()  

  def producer():  
      for i in range(5):  
          cola.put(f"Tarea-{i}")  

  def consumer():  
      while True:  
          tarea = cola.get()  
          print(f"Procesando: {tarea}")  
          cola.task_done()  

  # Iniciar hilos  
  threading.Thread(target=producer).start()  
  for _ in range(3):  # 3 consumers  
      threading.Thread(target=consumer, daemon=True).start()  
  cola.join()  # Esperar a que todas las tareas se procesen  
  ```  

---

## **Parte 2: Proyecto Integrador (50 minutos)**  

### **Sistema de Procesamiento de Pedidos**  
**Requisitos:**  
- Dos colas: `pedidos_normales` (FIFO) y `pedidos_urgentes` (prioridad).  
- Múltiples workers que simulan cocineros en un restaurante.  
- Manejo de errores (reintentos).  

**Implementación:**  
```python  
import random  
import time  
from queue import PriorityQueue  

class Restaurante:  
    def __init__(self):  
        self.pedidos_normales = queue.Queue()  
        self.pedidos_urgentes = PriorityQueue()  
        self.estadisticas = {"completados": 0, "fallidos": 0}  

    def agregar_pedido(self, pedido, urgente=False):  
        if urgente:  
            self.pedidos_urgentes.put((1, pedido))  # Prioridad 1 (alta)  
        else:  
            self.pedidos_normales.put(pedido)  

    def cocinero(self, id):  
        while True:  
            # Priorizar pedidos urgentes  
            if not self.pedidos_urgentes.empty():  
                _, pedido = self.pedidos_urgentes.get()  
            elif not self.pedidos_normales.empty():  
                pedido = self.pedidos_normales.get()  
            else:  
                time.sleep(1)  
                continue  

            print(f"Cocinero-{id} preparando: {pedido}")  
            time.sleep(random.uniform(1, 3))  # Simular tiempo de preparación  

            # 20% de probabilidad de fallo  
            if random.random() < 0.2:  
                print(f"Error con {pedido}! Reencolando...")  
                self.agregar_pedido(pedido, urgente=True)  # Reintentar como urgente  
                self.estadisticas["fallidos"] += 1  
            else:  
                print(f"{pedido} listo!")  
                self.estadisticas["completados"] += 1  

# Uso  
restaurante = Restaurante()  

# Agregar pedidos  
restaurante.agregar_pedido("Pizza")  
restaurante.agregar_pedido("Ensalada")  
restaurante.agregar_pedido("Sopa", urgente=True)  

# Iniciar cocineros  
for i in range(2):  
    threading.Thread(target=restaurante.cocinero, args=(i+1,), daemon=True).start()  

# Simular ejecución  
time.sleep(10)  
print("Estadísticas:", restaurante.estadisticas)  
```  

**Salida:**  
```  
Cocinero-1 preparando: Sopa  
Cocinero-2 preparando: Pizza  
Sopa listo!  
Error con Pizza! Reencolando...  
Cocinero-1 preparando: Pizza  
Pizza listo!  
Estadísticas: {'completados': 2, 'fallidos': 1}  
```  

---

## **Parte 3: Ejercicios de Optimización (20 minutos)**  

### **Ejercicio 1: Balanceo de Carga**  
**Enunciado:** Modificar el sistema para que los workers tomen tareas según su carga actual.  

**Solución:**  
```python  
class CocineroEficiente:  
    def __init__(self):  
        self.carga = 0  # Número de tareas asignadas  

    def tomar_tarea(self):  
        if self.carga < 3:  # Límite de 3 tareas simultáneas  
            self.carga += 1  
            # Procesar tarea...  
            self.carga -= 1  
```  

### **Ejercicio 2: Persistencia en Disco**  
**Enunciado:** Guardar pedidos pendientes en un archivo JSON para recuperar tras un fallo.  

**Solución:**  
```python  
import json  

def guardar_pedidos(restaurante):  
    with open("pedidos.json", "w") as f:  
        data = {  
            "normales": list(restaurante.pedidos_normales.queue),  
            "urgentes": [p[1] for p in restaurante.pedidos_urgentes.queue]  
        }  
        json.dump(data, f)  
```  

---

## **Cierre y Evaluación (10 minutos)**  
- **Presentaciones:** Cada equipo muestra su solución (5 mins/equipo).  
- **Preguntas Clave:**  
  - ¿Cómo manejarían un pico de 1000 pedidos/minuto?  
  - ¿Qué cola externa (Kafka, RabbitMQ) usarían y por qué?  
- **Evaluación:**  
  - **Funcionalidad (50%):** Cumplimiento de requisitos.  
  - **Optimización (30%):** Manejo de errores y eficiencia.  
  - **Creatividad (20%):** Soluciones innovadoras.  

---

### **Material Adicional**  
- **Herramienta:** [Simulador de colas RabbitMQ](https://www.rabbitmq.com/getstarted.html).  
- **Libro:** ["Kafka: The Definitive Guide"](https://www.confluent.io/resources/kafka-the-definitive-guide/).  

**¡Proyecto completado!** Los estudiantes ahora están listos para implementar colas en entornos reales. ¿Qué otro sistema te gustaría modelar? 😊