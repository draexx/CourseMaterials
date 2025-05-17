### **Clase 1: Servidores DHCP y DNS - Fundamentos y Operación Práctica**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
1. Comprender la función crítica de los servidores **DHCP** y **DNS** en redes.  
2. Identificar ejemplos cotidianos de su uso en entornos educativos y empresariales.  
3. Realizar configuraciones básicas mediante herramientas de simulación.  

---

### **Parte 1: Definiciones Clave (30 minutos)**  

#### **1. Servidor DHCP (Dynamic Host Configuration Protocol)**  
**Definición:**  
Servicio que asigna **automáticamente** direcciones IP y parámetros de red a dispositivos.  

**¿Por qué es importante?**  
- Elimina la configuración manual de IPs.  
- Evita conflictos de direcciones en la red.  

**Parámetros que asigna:**  
- 📌 **Dirección IP** (ej: `192.168.1.10`).  
- 🚪 **Gateway predeterminado** (puerta de enlace a Internet).  
- 🔍 **Servidores DNS** (para resolver nombres de dominio).  

**Ejemplo en TECBA:**  
> *"Cuando te conectas al Wi-Fi del instituto, tu laptop recibe una IP como `192.168.5.20` gracias al DHCP del router."*  

**Caso real:**  
- **Problema:** Si el DHCP falla, los dispositivos no podrán navegar (a menos que se configuren IPs manuales).  

---

#### **2. Servidor DNS (Domain Name System)**  
**Definición:**  
El "directorio telefónico" de Internet: traduce nombres de dominio (ej: `www.tecbabolivia.edu.bo`) a direcciones IP (ej: `200.58.100.25`).  

**Jerarquía DNS:**  
1. **Raíz:** Servidores globales (`.`).  
2. **TLD:** Dominios como `.com`, `.org`, `.bo`.  
3. **Autoritativo:** Guarda la IP real del dominio.  

**Ejemplo práctico:**  
> *"Al escribir `facebook.com` en tu navegador, el DNS lo convierte a `31.13.65.36` para conectarte."*  

**Importancia:**  
- Sin DNS, tendríamos que memorizar IPs numéricas para cada sitio web.  

**Ejemplo en Bolivia:**  
- Los servidores DNS de **Entel** o **Tigo** resuelven las peticiones de sus usuarios.  

---

### **Parte 2: Ejemplos y Casos de Uso (20 minutos)**  

#### **Ejemplo 1: DHCP en Redes Domésticas**  
- **Escenario:**  
  - Router Hogar: Asigna IPs como `192.168.0.100` a tu celular, `192.168.0.101` a tu smart TV.  
  - **Rango típico:** `192.168.0.1` a `192.168.0.254`.  

#### **Ejemplo 2: DNS en Educación**  
- **Escenario TECBA:**  
  - El dominio `moodle.tecbabolivia.edu.bo` apunta a la IP del servidor interno de Moodle (ej: `10.0.0.5`).  

#### **Ejemplo 3: Fallos Comunes**  
- **Problema DHCP:**  
  - *"¡No tengo internet!"* → Verificar si el dispositivo recibió una IP válida (`ipconfig` en Windows).  
- **Problema DNS:**  
  - *"El sitio no carga, pero sí funciona con la IP."* → Cambiar a DNS públicos como Google (`8.8.8.8`).  

---

### **Parte 3: Actividad Práctica (30 minutos)**  

#### **Ejercicio 1: Simulación de DHCP en Packet Tracer**  
**Pasos:**  
1. Arrastrar un **router** (servidor DHCP) y 2 PCs a la topología.  
2. Configurar el DHCP en el router:  
   - Rango de IPs: `192.168.1.10` a `192.168.1.50`.  
   - Gateway: `192.168.1.1`.  
   - DNS: `8.8.8.8`.  
3. Verificar que las PCs reciben IP automáticamente.  

**Captura esperada:**  
```  
PC1> ipconfig  
IP: 192.168.1.10  
Gateway: 192.168.1.1  
DNS: 8.8.8.8  
```  

#### **Ejercicio 2: Diagnóstico de DNS**  
**Instrucciones:**  
1. En tu computadora real (o simulada):  
   - Usar `nslookup google.com` (Windows/Linux) para ver la IP de Google.  
   - Probar con otros dominios: `youtube.com`, `tecbabolivia.edu.bo`.  

**Resultado típico:**  
```  
> nslookup google.com  
Dirección: 172.217.0.142  
```  

---

### **Cierre y Reflexión (10 minutos)**  

#### **Resumen Visual:**  
| **Servidor** | **Función**                  | **Ejemplo TECBA**               |  
|--------------|------------------------------|----------------------------------|  
| DHCP         | Asigna IPs automáticamente   | Wi-Fi del instituto              |  
| DNS          | Traduce nombres a IPs        | Acceso a moodle.tecbabolivia.edu.bo |  

#### **Tarea:**  
- *"Investiga: ¿Qué DNS públicos alternativos existen (aparte de Google)? Ejemplo: Cloudflare (`1.1.1.1`)."*  

#### **Material Adicional:**  
- **Video:** *"Cómo funciona DHCP en 3 minutos"* → [Enlace YouTube](https://youtu.be/ejemplo).  
- **Herramienta:** `Wireshark` para capturar paquetes DHCP (opcional).  

--- 

**Nota para el docente:**  
- Relacionar con problemas comunes: *"¿Por qué a veces el Wi-Fi dice 'Sin Internet' aunque esté conectado?"* (Fallo en DHCP/DNS).  
- Usar analogías: *"El DHCP es como un repartidor de direcciones en una ciudad nueva, y el DNS es el mapa que te dice dónde está cada lugar."*  

**Resultado esperado:**  
Los estudiantes podrán explicar cómo obtienen su IP y cómo se resuelven los nombres de dominio, aplicándolo a redes reales.