### **Clase 3: Servidores de Acceso Remoto y Transferencia de Archivos**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
1. Comprender el funcionamiento de protocolos de acceso remoto (**SSH/Telnet**) y transferencia de archivos (**FTP/SFTP**).  
2. Analizar casos de uso reales y sus implicaciones de seguridad.  
3. Realizar conexiones básicas mediante clientes de acceso remoto.  

---

### **Parte 1: Definiciones Clave (30 minutos)**  

#### **1. Protocolos de Acceso Remoto**  
**a) Telnet (Telecommunication Network):**  
- **Definición:** Protocolo para acceder a dispositivos de red remotamente (puerto 23).  
- **Problema:**  
  ⚠️ **Transmite datos en texto plano** (contraseñas visibles para hackers).  
- **Ejemplo obsoleto:**  
  > "Administrar un router antiguo desde otra ubicación (hoy se usa SSH)".  

**b) SSH (Secure Shell):**  
- **Definición:** Versión segura de Telnet con cifrado (puerto 22).  
- **Ventajas:**  
  - 🔒 Cifrado AES-256.  
  - ✅ Autenticación por clave pública/privada.  
- **Ejemplo actual:**  
  > "El administrador del TECBA usa SSH para configurar servidores Linux desde su casa".  

---

#### **2. Protocolos de Transferencia de Archivos**  
**a) FTP (File Transfer Protocol):**  
- **Definición:** Transfiere archivos entre cliente y servidor (puerto 21).  
- **Riesgos:**  
  - 🔓 Sin cifrado (datos interceptables).  
  - 🛑 **Nunca usarlo para datos sensibles**.  
- **Caso de uso:**  
  > "Subir archivos a un hosting web antiguo".  

**b) SFTP/FTPS (Secure FTP):**  
- **SFTP:** FTP sobre SSH (puerto 22).  
- **FTPS:** FTP + SSL (puerto 990).  
- **Ejemplo seguro:**  
  > "Backup de archivos del TECBA usando SFTP con FileZilla".  

---

### **Parte 2: Ejemplos y Comparativas (20 minutos)**  

#### **Tabla Comparativa:**  
| **Protocolo** | **Puerto** | **Seguridad** | **Uso Recomendado**          |  
|---------------|------------|---------------|-------------------------------|  
| Telnet        | 23         | ❌ Inseguro   | Solo en redes aisladas        |  
| SSH           | 22         | ✅ Cifrado    | Administración remota         |  
| FTP           | 21         | ❌ Inseguro   | Archivos públicos             |  
| SFTP          | 22         | ✅ Cifrado    | Transferencia de datos críticos|  

#### **Ejemplo en Infraestructura TECBA:**  
- **Mala práctica:** Usar FTP para subir calificaciones (¡datos expuestos!).  
- **Buena práctica:** Usar SFTP con autenticación de dos factores.  

---

### **Parte 3: Actividades Prácticas (30 minutos)**  

#### **Ejercicio 1: Conexión SSH con PuTTY (Windows) o Terminal (Linux/Mac)**  
**Pasos:**  
1. Descargar PuTTY ([enlace oficial](https://www.putty.org/)).  
2. Conectarse a un servidor demo:  
   - Host: `demo.testfire.net` (servidor de prueba).  
   - Puerto: 22.  
3. Ver el mensaje de bienvenida.  

**Captura esperada:**  
```  
login as: guest  
guest@demo.testfire.net's password: [no escribir nada, presionar Enter]  
Welcome to Ubuntu 20.04 LTS...  
```  

#### **Ejercicio 2: Transferencia Segura con FileZilla (SFTP)**  
1. Descargar FileZilla ([enlace](https://filezilla-project.org/)).  
2. Conectarse a:  
   - Host: `sftp://demo.wftpserver.com`.  
   - Usuario: `demo-user`.  
   - Contraseña: `demo-user`.  
3. Explorar archivos de prueba.  

---

### **Cierre y Reflexión (10 minutos)**  

#### **Preguntas Clave:**  
1. *"¿Por qué Telnet y FTP siguen existiendo si son inseguros?"*  
   - Respuesta: Compatibilidad con sistemas legacy (ej: equipos industriales antiguos).  

2. *"¿Qué protocolo usarías para enviar los proyectos finales de los estudiantes?"*  
   - Respuesta ideal: **SFTP** con credenciales únicas por alumno.  

#### **Tarea:**  
- *"Investiga un caso real de hackeo por uso de FTP/Telnet (ej: filtración de datos de una universidad en 2023)."*  

#### **Recursos Adicionales:**  
- **Video:** *"SSH vs Telnet: Demostración de Seguridad"* → [Enlace](https://youtu.be/ejemplo).  
- **Laboratorio virtual:** [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) para practicar SSH.  

--- 

**Nota para el docente:**  
- **Demostración opcional:** Mostrar con Wireshark cómo Telnet/FTP exponen contraseñas, versus el tráfico cifrado de SSH/SFTP.  
- **Contexto local:** Mencionar que empresas bolivianas como Entel o Banco Unión migraron de FTP a SFTP para cumplir con estándares de seguridad.  

**Resultado esperado:**  
Los estudiantes entenderán los riesgos de los protocolos obsoletos y configurarán conexiones seguras, aplicables en su futura carrera en telecomunicaciones.