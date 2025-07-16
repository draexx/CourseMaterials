**Clase 2: Seguridad en Servidores Web y Servicios Avanzados**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Seguridad Básica en Servidores Web (30 minutos)**  

#### **Definiciones Clave:**  
1. **Listas de Control de Acceso (ACLs):**  
   - *Definición:* Reglas que definen qué usuarios o sistemas pueden acceder a recursos específicos en el servidor.  
   - *Ejemplo:* Bloquear el acceso a la carpeta `/admin/` para todas las IPs, excepto la del administrador.  
   - *Demostración:* Editar el archivo `.htaccess` en Apache:  
     ```apache
     Order Deny,Allow
     Deny from all
     Allow from 192.168.1.100
     ```  

2. **Autenticación Básica:**  
   - *Definición:* Método para proteger directorios con usuario/contraseña.  
   - *Ejemplo:* Crear credenciales para acceder a `http://localhost/reportes/`.  
   - *Pasos:*  
     - Crear archivo de contraseñas con `htpasswd`:  
       ```bash
       htpasswd -c /ruta/.htpasswd usuario1
       ```  
     - Configurar Apache para requerir autenticación:  
       ```apache
       AuthType Basic
       AuthName "Área Restringida"
       AuthUserFile /ruta/.htpasswd
       Require valid-user
       ```  

3. **Firewall y Puertos:**  
   - *Definición:* Filtro que bloquea accesos no autorizados a puertos.  
   - *Ejemplo:* Cerrar el puerto `22` (SSH) si no se usa, y abrir solo `80` (HTTP) y `443` (HTTPS).  

---

### **2. Servicios Avanzados (30 minutos)**  

#### **A. FTP (File Transfer Protocol):**  
- *Definición:* Protocolo para transferir archivos entre cliente y servidor.  
- *Ejemplo práctico:*  
  1. Instalar FileZilla Server en el servidor.  
  2. Crear un usuario FTP con acceso solo a la carpeta `/var/www/html/`.  
  3. Subir un archivo desde el cliente (FileZilla Client) al servidor.  

#### **B. Acceso Remoto Seguro:**  
- **SSH vs. Telnet:**  
  | **Protocolo** | **Seguridad** | **Uso Recomendado** |  
  |--------------|---------------|---------------------|  
  | **Telnet**   | Sin cifrado (riesgo) | Solo redes internas |  
  | **SSH**      | Cifrado (seguro) | Uso en Internet |  
- *Demostración:* Conexión SSH con PuTTY:  
  ```bash
  ssh usuario@direccion_ip -p 22
  ```  

#### **C. Ataques Comunes y Mitigación:**  
- **Fuerza Bruta:**  
  - *Ejemplo:* 1,000 intentos de inicio de sesión en SSH.  
  - *Solución:* Usar `fail2ban` para bloquear IPs maliciosas.  

---

### **3. Taller Práctico (20 minutos)**  

#### **Actividad:**  
1. **Protección de Directorio:**  
   - Cada estudiante protege una carpeta en su servidor local con autenticación básica.  
   - Verificación: Intentar acceder sin credenciales (debe mostrar error `401`).  

2. **Configuración FTP:**  
   - Crear un usuario FTP que solo pueda leer (no modificar) archivos en `/var/www/public/`.  

3. **Discusión Grupal:**  
   - *Pregunta:* "¿Por qué es peligroso usar Telnet en lugar de SSH en una red pública?"  

---

### **Cierre (5 minutos)**  
- **Resumen:**  
  - *"Hoy aprendimos a proteger servidores con ACLs y autenticación, configurar FTP seguro, y evitar ataques con SSH."*  
- **Tarea:**  
  - Investigar: *"¿Qué es un certificado SSL y cómo se instala en Apache?"* (preparación para HTTPS en la próxima clase).  

---

### **Material de Apoyo:**  
- **Comandos Útiles:**  
  ```bash
  # Ver puertos abiertos en Linux:
  netstat -tuln

  # Bloquear IP en firewall (Linux):
  sudo iptables -A INPUT -s IP_MALICIOSA -j DROP
  ```  
- **Diagrama:**  
  ```  
  Cliente FTP → (Puerto 21) → Servidor FTP → (Autenticación) → Acceso a Archivos  
  ```  

**Nota:** Usar analogías como *"El firewall es como un guardia que revisa los pasaportes (puertos) antes de dejar entrar a alguien (datos)"*. Si hay dudas, repetir la demostración de SSH con capturas de pantalla paso a paso.