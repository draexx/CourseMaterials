### **Clase 2: Direccionamiento IP y Enrutamiento**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
- Entender qué es una dirección IP y su función en las redes.  
- Comprender los conceptos básicos de enrutamiento y su importancia en la comunicación entre redes.  

---

### **1. Definiciones y Ejemplos**  

#### **A. Direccionamiento IP**  

**Definición:**  
Una **dirección IP** (Internet Protocol) es un identificador único asignado a cada dispositivo en una red, que permite su localización y comunicación.  

**Tipos de direcciones IP:**  
1. **IPv4:**  
   - Formato: 4 números separados por puntos (ej: `192.168.1.1`).  
   - Rango: 0.0.0.0 a 255.255.255.255.  
   - Ejemplo: La IP de tu router en casa (ej: `192.168.0.1`).  

2. **IPv6:**  
   - Formato: 8 grupos hexadecimales separados por dos puntos (ej: `2001:0db8:85a3::8a2e:0370:7334`).  
   - Razón: IPv4 se está agotando, IPv6 ofrece más direcciones.  

**Direcciones Públicas vs. Privadas:**  
- **Pública:** Identifica tu red en Internet (ej: la IP que ve Google cuando navegas).  
- **Privada:** Usada dentro de una red local (ej: `192.168.x.x`, `10.x.x.x`).  

**Ejemplo práctico:**  
> *"Cuando te conectas a Netflix, tu celular usa una IP privada dentro de tu casa, pero tu router la 'traduce' a una IP pública para comunicarse con los servidores de Netflix."*  

---

#### **B. Máscara de Subred**  

**Definición:**  
La máscara de subred (ej: `255.255.255.0`) define qué parte de la IP identifica la red y qué parte identifica el dispositivo.  

**Ejemplo:**  
- IP: `192.168.1.10`  
- Máscara: `255.255.255.0`  
  - **Red:** `192.168.1.0` (primeros 3 números).  
  - **Host:** `10` (último número).  

**Analogía:**  
> *"La máscara de subred es como el código de área de un número telefónico: el '042' (red) y el '1234567' (host)."*  

---

#### **C. Enrutamiento (Routing)**  

**Definición:**  
Proceso de dirigir datos entre redes diferentes usando **routers**.  

**Conceptos clave:**  
1. **Router:** Dispositivo que "une" redes (ej: el módem de tu casa conecta tu LAN a Internet).  
2. **Gateway:** Puerta de enlace (ej: la IP del router en tu red local, como `192.168.1.1`).  
3. **Tabla de enrutamiento:** Reglas que usa el router para decidir a dónde enviar los datos.  

**Ejemplo cotidiano:**  
> *"Cuando visitas www.google.com desde el instituto, el router de TECBA envía tu solicitud a través de varios routers (salto a salto) hasta llegar a los servidores de Google."*  

---

### **2. Metodología de la Clase**  

#### **Parte 1: Explicación teórica (30 min)**  
- Presentación visual: Comparación IPv4 vs. IPv6 con ejemplos reales.  
- Preguntas rápidas:  
  - *"¿Tu smartphone tiene IP pública o privada cuando usa Wi-Fi?"* (Respuesta: privada).  
  - *"¿Qué pasa si dos dispositivos en una red tienen la misma IP?"* (Conflicto de IP, no funcionaría la red).  

#### **Parte 2: Actividad práctica (40 min)**  
1. **Ejercicio de subnetting básico:**  
   - Dada la IP `192.168.2.15` y máscara `255.255.255.0`, identificar la red y el host.  
2. **Simulación con Packet Tracer:**  
   - Configurar direcciones IP en PCs y routers virtuales.  
   - Verificar comunicación entre redes.  

#### **Parte 3: Cierre (10 min)**  
- Resumen con analogía:  
  - *"La IP es como tu dirección postal, el router es el cartero que decide la ruta."*  
- Tarea opcional:  
  - *"Usa `ipconfig` (Windows) o `ifconfig` (Linux) para ver la IP de tu computadora y anota si es pública o privada."*  

---

### **Material de Apoyo**  
- **Herramienta interactiva:** [Subnetting Calculator Online](https://www.calculator.net/ip-subnet-calculator.html).  
- **Video recomendado:** *"Cómo funciona el enrutamiento en Internet"* (ej: [YouTube](https://www.youtube.com)).  

**Nota:** Adaptar ejemplos a redes locales de Bolivia (ej: IPs comunes usadas por Entel o Tigo).