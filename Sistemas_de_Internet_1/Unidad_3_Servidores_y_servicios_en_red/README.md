### **Unidad Temática 3: "Servidores y Servicios en Red"**  
**Duración:** 3 clases de 1 hora y 20 minutos cada una.  

---

## **Clase 1: Fundamentos de Servidores de Red (DHCP y DNS)**  
**Objetivos:**  
1. Comprender el rol de los servidores **DHCP** y **DNS** en redes.  
2. Configurar parámetros básicos de estos servicios.  

### **Contenidos:**  
#### **1. Servidor DHCP**  
- **Definición:** Asigna direcciones IP automáticamente a dispositivos en una red.  
- **Ejemplo:**  
  ```  
  Cuando te conectas al Wi-Fi del TECBA, tu celular recibe una IP como 192.168.1.10 gracias al DHCP.  
  ```  
- **Parámetros clave:**  
  - Rango de IPs.  
  - Gateway y DNS.  
  - Tiempo de arrendamiento.  

#### **2. Servidor DNS**  
- **Definición:** Traduce nombres de dominio (ej: `www.tecbabolivia.edu.bo`) a direcciones IP.  
- **Ejemplo:**  
  ```  
  Al escribir "google.com", el DNS lo convierte a 172.217.0.142 para cargar la página.  
  ```  
- **Tipos de consultas:**  
  - **Recursiva:** El DNS resuelve todo por ti.  
  - **Iterativa:** Te guía paso a paso.  

### **Actividades:**  
1. **Simulación en Packet Tracer:**  
   - Configurar un servidor DHCP para repartir IPs en una LAN.  
2. **Ejercicio de diagnóstico:**  
   - Usar `ipconfig /all` (Windows) o `nmcli` (Linux) para ver la IP asignada por DHCP y el DNS usado.  

---

## **Clase 2: Servidores Web y de Correo (HTTP, SMTP/POP3)**  
**Objetivos:**  
1. Entender cómo funcionan los servidores **HTTP** y de **correo electrónico**.  
2. Configurar un servidor web local con XAMPP.  

### **Contenidos:**  
#### **1. Servidor HTTP/HTTPS**  
- **Definición:** Entrega páginas web usando los protocolos HTTP (no seguro) o HTTPS (seguro).  
- **Ejemplo:**  
  ```  
  Apache o Nginx alojan el sitio web del TECBA.  
  ```  
- **Puertos comunes:**  
  - HTTP: 80  
  - HTTPS: 443  

#### **2. Servidores de Correo (SMTP/POP3/IMAP)**  
- **SMTP:** Envía correos (puerto 25 o 587).  
- **POP3/IMAP:** Recibe correos (puerto 110 o 143).  
- **Ejemplo:**  
  ```  
  Cuando envías un correo desde tu cuenta @tecbabolivia.edu.bo, SMTP lo dirige al destinatario.  
  ```  

### **Actividades:**  
1. **Práctica con XAMPP:**  
   - Instalar Apache y crear una página HTML básica accesible desde la red local.  
2. **Análisis de tráfico:**  
   - Usar Wireshark para capturar paquetes HTTP vs HTTPS.  

---

## **Clase 3: Servidores de Acceso Remoto y Transferencia de Archivos (FTP/Telnet)**  
**Objetivos:**  
1. Explorar protocolos de acceso remoto (**Telnet**) y transferencia de archivos (**FTP**).  
2. Identificar sus usos y riesgos de seguridad.  

### **Contenidos:**  
#### **1. Servidor FTP**  
- **Definición:** Transfiere archivos entre cliente y servidor (puerto 21).  
- **Ejemplo:**  
  ```  
  Subir archivos al Moodle del TECBA usa FTP detrás de cámaras.  
  ```  
- **Alternativas seguras:** SFTP (SSH) o FTPS (SSL).  

#### **2. Servidor Telnet**  
- **Definición:** Permite controlar dispositivos remotamente (puerto 23).  
- **Riesgos:**  
  ```  
  ¡Telnet envía datos en texto plano! Por eso se usa SSH (puerto 22) en su lugar.  
  ```  

### **Actividades:**  
1. **Demo de FTP vs SFTP:**  
   - Usar FileZilla para conectarse a un servidor FTP público (ej: `ftp.gnu.org`).  
2. **Debate:**  
   - *"¿Por qué Telnet está obsoleto en redes modernas?"*  

---

### **Evaluación y Recursos:**  
- **Proyecto final:** Configurar una mini-red en Packet Tracer con:  
  - DHCP + DNS + Servidor web.  
- **Recursos:**  
  - [Guía de XAMPP](https://www.apachefriends.org/es/index.html).  
  - [Wireshark para análisis de tráfico](https://www.wireshark.org/).  

**Nota:** Adaptar ejemplos a infraestructuras locales (ej: servidores de Entel o Tigo en Bolivia).