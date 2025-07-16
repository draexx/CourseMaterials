**Clase 1: Fundamentos de Servidores Web y Configuración Básica**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Introducción a Servidores Web (20 minutos)**  

#### **Definiciones Clave:**  
- **Servidor Web:**  
  - *Definición:* Software o hardware que almacena, procesa y entrega páginas web a clientes (navegadores) usando el protocolo HTTP/HTTPS.  
  - *Ejemplo:* Cuando escribes `www.google.com` en tu navegador, tu computadora (cliente) solicita la página al servidor web de Google, que responde enviando los datos para mostrarla.  

- **Protocolos Relacionados:**  
  - **HTTP (Hypertext Transfer Protocol):** Protocolo para transferir hipertexto (páginas web).  
  - **HTTPS:** Versión segura de HTTP (cifrado con SSL/TLS).  
  - **FTP (File Transfer Protocol):** Para transferir archivos entre cliente y servidor.  

#### **Ejemplos de Servidores Web Populares:**  
| **Software** | **Uso Común**                          | **Ejemplo de Empresa que lo Usa** |  
|--------------|----------------------------------------|-----------------------------------|  
| **Apache**   | Sitios web tradicionales               | WordPress, Wikipedia              |  
| **Nginx**    | Sitios de alto tráfico                 | Netflix, Airbnb                   |  
| **IIS**      | Entornos Windows                       | Microsoft                         |  

#### **Demostración Interactiva:**  
1. Abrir el navegador y presionar `F12` (Herramientas de Desarrollo).  
2. Navegar a `www.ejemplo.com` y mostrar:  
   - **Solicitudes HTTP** (pestaña "Network").  
   - **Respuesta del servidor** (código `200 OK`).  

---

### **2. Instalación y Configuración Básica (40 minutos)**  

#### **Paso a Paso con XAMPP:**  
1. **Descargar e Instalar:**  
   - Enlace oficial: [https://www.apachefriends.org](https://www.apachefriends.org).  
   - Instalar con opciones predeterminadas (Apache, MySQL, PHP).  

2. **Iniciar Servicios:**  
   - Abrir el *Panel de Control de XAMPP* y activar Apache.  
   - Verificar en el navegador: `http://localhost` (debe mostrar la página de XAMPP).  

3. **Crear un Sitio Web Básico:**  
   - Ir a la carpeta `C:\xampp\htdocs\`.  
   - Crear una carpeta llamada `mi_sitio` y dentro un archivo `index.html`:  
     ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>Mi Primer Sitio</title>
     </head>
     <body>
         <h1>¡Hola Mundo desde mi Servidor Web!</h1>
     </body>
     </html>
     ```  
   - Acceder en el navegador: `http://localhost/mi_sitio/`.  

4. **Firewall y Puertos:**  
   - Explicar el puerto `80` (HTTP) y `443` (HTTPS).  
   - Mostrar cómo permitir Apache en el firewall de Windows:  
     - `Panel de Control > Firewall > Permitir una aplicación > Seleccionar Apache`.  

---

### **3. Práctica Guiada (20 minutos)**  

#### **Actividad para Estudiantes:**  
1. Cada estudiante repite los pasos anteriores en su computadora.  
2. Personalizan su `index.html` con su nombre y una imagen (usando `<img src="imagen.jpg">`).  
3. Validación:  
   - El docente verifica que todos puedan acceder a `http://localhost/mi_sitio/`.  
   - Discusión rápida: *"¿Qué problemas surgieron durante la instalación?"*.  

---

### **Cierre (5 minutos)**  
- **Resumen:**  
  - *"Hoy aprendimos qué es un servidor web, cómo funciona HTTP, y configuramos nuestro primer sitio local con XAMPP."*  
- **Tarea:**  
  - Investigar: *"¿Qué es un servidor DNS y cómo se relaciona con un servidor web?"* (preparación para la próxima clase).  

---

### **Material de Apoyo:**  
- **Diagrama Visual:**  
  ```  
  Cliente (Navegador) → Solicita página → Servidor Web (Apache) → Responde con HTML  
  ```  
- **Enlaces Útiles:**  
  - [Documentación de Apache](https://httpd.apache.org/docs/).  
  - [W3Schools - HTML Básico](https://www.w3schools.com/html/).  

**Nota:** Ajustar tiempos si hay dudas técnicas durante la instalación. Usar analogías como *"El servidor web es como un mesero que lleva platos (datos) a las mesas (clientes)"* para clarificar conceptos.