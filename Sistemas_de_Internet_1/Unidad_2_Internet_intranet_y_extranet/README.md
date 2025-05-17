### **Planificación de la Unidad Temática 2: "Internet, Intranet y Extranet"**  
**Duración:** 3 clases de 1 hora y 20 minutos cada una.  

---

## **Clase 1: Conceptos de Internet, Intranet y Extranet**  
**Objetivos:**  
- Diferenciar entre Internet, Intranet y Extranet.  
- Identificar casos de uso en entornos reales.  

### **Contenidos:**  
1. **Internet:**  
   - **Definición:** Red global pública que interconecta redes usando TCP/IP.  
   - **Ejemplo:** Navegación en Google, redes sociales, streaming.  

2. **Intranet:**  
   - **Definición:** Red privada dentro de una organización (solo accesible para miembros).  
   - **Ejemplo:** Sistema interno del Instituto TECBA (ej: plataforma de notas, archivos compartidos).  

3. **Extranet:**  
   - **Definición:** Parte de una Intranet extendida a usuarios externos autorizados (clientes, proveedores).  
   - **Ejemplo:** Portal para estudiantes que muestra horarios y calificaciones (acceso con credenciales).  

### **Metodología:**  
- **Exposición teórica (30 min):**  
  - Comparar con analogías:  
    - *"Internet es como una ciudad abierta, Intranet es una oficina con llave, Extranet es la sala de visitas de esa oficina."*  
- **Actividad práctica (40 min):**  
  - **Análisis de casos:** Identificar ejemplos en el instituto (ej: Moodle = Intranet, sitio web público = Internet).  
  - **Debate:** *"¿Qué pasaría si la Intranet del TECBA fuera pública?"* (Riesgos de seguridad).  
- **Cierre (10 min):**  
  - Resumen con esquema visual (diagrama de Venn: Internet/Intranet/Extranet).  

---

## **Clase 2: Segmentación de Red y DMZ**  
**Objetivos:**  
- Entender la segmentación de redes y su importancia en la seguridad.  
- Comprender el rol de la DMZ (Zona Desmilitarizada).  

### **Contenidos:**  
1. **Segmentación de red:**  
   - **Definición:** División de una red en subredes para mejorar seguridad/rendimiento.  
   - **Ejemplo:** Separar redes administrativas y estudiantiles en el instituto.  

2. **DMZ (Zona Desmilitarizada):**  
   - **Definición:** Subred aislada que aloja servicios públicos (ej: servidor web) para proteger la red interna.  
   - **Ejemplo:** Sitio web del TECBA está en DMZ; la base de datos de notas está en la red interna.  

### **Metodología:**  
- **Exposición teórica (30 min):**  
  - Diagrama de una red con DMZ (usar dibujo en pizarra o herramienta digital).  
- **Actividad práctica (40 min):**  
  - **Simulación en Packet Tracer:** Crear una red con DMZ (servidor web accesible desde Internet y otro interno no accesible).  
  - **Pregunta clave:** *"¿Por qué el correo institucional no debería estar en la DMZ?"*  
- **Cierre (10 min):**  
  - Reflexión: *"¿Dónde ubicarías un servidor de videollamadas en la red del instituto?"*  

---

## **Clase 3: Sistemas Distribuidos y Acceso a Servicios**  
**Objetivos:**  
- Entender cómo funcionan los sistemas distribuidos (cliente-servidor).  
- Configurar servicios básicos en red.  

### **Contenidos:**  
1. **Sistemas distribuidos:**  
   - **Definición:** Recursos compartidos en múltiples dispositivos (ej: nube, bancos de datos).  
   - **Ejemplo:** Google Drive (archivos almacenados en servidores globales).  

2. **Modo cliente-servidor:**  
   - **Cliente:** Solicita servicios (ej: navegador web).  
   - **Servidor:** Responde a solicitudes (ej: servidor Apache que aloja el sitio del TECBA).  

### **Metodología:**  
- **Exposición teórica (20 min):**  
  - Comparar con un restaurante: *"El cliente (usuario) pide un plato (dato), el servidor (cocina) lo prepara y envía."*  
- **Actividad práctica (50 min):**  
  - **Configuración básica en XAMPP:**  
    1. Instalar servidor Apache.  
    2. Crear una página HTML simple y alojarla localmente.  
    3. Verificar acceso desde otro PC en la misma red.  
- **Cierre (10 min):**  
  - Demostración: Mostrar la página web desde el servidor local.  
  - Tarea: *"Investiga cómo Netflix usa sistemas distribuidos para transmitir películas."*  

---

### **Evaluación y Recursos:**  
- **Evaluación formativa:** Participación en simulaciones y debates.  
- **Recursos:**  
  - **Packet Tracer** (Cisco) para simulaciones de red.  
  - **XAMPP** para prácticas de servidor web.  
  - **Video:** *"Cómo funciona una DMZ"* (ej: [YouTube](https://www.youtube.com)).  

**Nota:** Adaptar ejemplos a infraestructuras tecnológicas disponibles en el instituto (ej: servidores reales usados en Telecomunicaciones).