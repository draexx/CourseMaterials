### **Clase 2: Servidores Web y de Correo Electrónico - Definiciones y Aplicaciones Prácticas**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
1. Comprender el funcionamiento de los servidores **HTTP/HTTPS** y de **correo electrónico (SMTP/POP3/IMAP)**.  
2. Identificar ejemplos reales en servicios cotidianos.  
3. Configurar un servidor web básico usando XAMPP.  

---

### **Parte 1: Definiciones Clave (30 minutos)**  

#### **1. Servidor Web (HTTP/HTTPS)**  
**Definición:**  
Software que almacena y entrega páginas web a los clientes mediante los protocolos:  
- **HTTP** (HyperText Transfer Protocol): No cifrado (puerto 80).  
- **HTTPS** (HTTP Secure): Cifrado con SSL/TLS (puerto 443).  

**Ejemplos de servidores web populares:**  
- **Apache:** Usado en el 31% de sitios web (ej: Moodle del TECBA).  
- **Nginx:** Ideal para alto tráfico (ej: Netflix).  
- **Microsoft IIS:** Común en entornos Windows.  

**Caso práctico en TECBA:**  
> *"Cuando accedes al sitio web del instituto (`www.tecbabolivia.edu.bo`), un servidor Apache o Nginx envía los archivos HTML/CSS a tu navegador."*  

---

#### **2. Servidores de Correo Electrónico**  
**Protocolos clave:**  
| **Protocolo** | **Función**                  | **Puerto** | **Ejemplo**                          |  
|---------------|------------------------------|-----------|---------------------------------------|  
| **SMTP**      | Envío de correos             | 25, 587   | Enviar un email desde `@tecbabolivia.edu.bo`. |  
| **POP3**      | Descarga de correos al dispositivo | 110      | Outlook descargando emails para leer offline. |  
| **IMAP**      | Sincronización de correos    | 143       | Gmail mostrando los mismos emails en celular y PC. |  

**Flujo de un correo electrónico:**  
```  
[Tú @tecbabolivia.edu.bo] → SMTP → Servidor TECBA → SMTP → [Destinatario @gmail.com]  
```  

**Ejemplo de seguridad:**  
> *"HTTPS protege tus credenciales al acceder al webmail, mientras que SMTP con STARTTLS (puerto 587) cifra el envío."*  

---

### **Parte 2: Ejemplos y Casos de Uso (20 minutos)**  

#### **Ejemplo 1: Sitios Web con y sin HTTPS**  
- **HTTP inseguro:**  
  - `http://ejemplo.com`: Los datos viajan en texto plano (¡hackeable!).  
- **HTTPS seguro:**  
  - `https://tecbabolivia.edu.bo`: Cifrado con certificado SSL (🔒 en el navegador).  

**Demostración:**  
1. Abrir un sitio HTTP (ej: `http://neverssl.com`) y otro HTTPS (ej: `https://google.com`).  
2. Mostrar la advertencia de "No seguro" en HTTP.  

#### **Ejemplo 2: Configuración de Correo en Thunderbird**  
- **Datos necesarios:**  
  - SMTP: `smtp.tecbabolivia.edu.bo` (puerto 587).  
  - IMAP: `imap.tecbabolivia.edu.bo` (puerto 993).  

---

### **Parte 3: Actividad Práctica (30 minutos)**  

#### **Ejercicio 1: Instalación y Configuración de XAMPP**  
**Pasos:**  
1. Descargar XAMPP desde [Apache Friends](https://www.apachefriends.org/es/index.html).  
2. Instalar e iniciar los módulos **Apache** (servidor web) y **MySQL** (opcional para bases de datos).  
3. Crear un archivo `index.html` en `C:\xampp\htdocs\` con:  
   ```html  
   <h1>¡Mi primer servidor web en TECBA!</h1>  
   ```  
4. Acceder desde el navegador con `http://localhost`.  

**Resultado esperado:**  
![Página mostrando el título en el navegador local](https://via.placeholder.com/400x200?text=Mi+primer+servidor+web)  

#### **Ejercicio 2: Análisis de Protocolos con Wireshark**  
1. Filtrar tráfico HTTP (`http`) vs HTTPS (`ssl`).  
2. Observar cómo HTTPS cifra los datos (texto ilegible).  

---

### **Cierre y Reflexión (10 minutos)**  

#### **Resumen Visual:**  
| **Servidor**  | **Protocolo** | **Uso en TECBA**                |  
|---------------|---------------|----------------------------------|  
| Web           | HTTP/HTTPS    | Sitio institucional, Moodle      |  
| Correo        | SMTP/POP3/IMAP| Emails `@tecbabolivia.edu.bo`    |  

#### **Tarea:**  
- *"Investiga: ¿Qué diferencia hay entre POP3 e IMAP? ¿Cuál recomendarías para los estudiantes del TECBA y por qué?"*  

#### **Material Adicional:**  
- **Video:** *"Cómo funciona HTTPS"* (5 min): [Enlace YouTube](https://youtu.be/ejemplo).  
- **Herramienta:** [Let's Encrypt](https://letsencrypt.org/es/) para certificados SSL gratuitos.  

--- 

**Nota para el docente:**  
- Relacionar con la **seguridad informática**: *"¿Por qué los bancos usan HTTPS obligatoriamente?"*  
- Usar analogías: *"SMTP es como el cartero que lleva tu carta, IMAP es como un archivador compartido donde siempre ves las mismas cartas desde cualquier dispositivo."*  

**Resultado esperado:**  
Los estudiantes podrán explicar cómo se sirven las páginas web y los correos electrónicos, y configurarán su primer servidor web local.