### **Clase 2: Segmentación de Red y DMZ - Definiciones y Ejemplos Prácticos**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
1. Comprender el concepto de **segmentación de red** y sus beneficios.  
2. Identificar el rol de una **DMZ (Zona Desmilitarizada)** en la seguridad de redes.  
3. Aplicar los conceptos mediante ejemplos reales y ejercicios interactivos.  

---

### **Parte 1: Definiciones Clave (30 minutos)**  

#### **1. Segmentación de Red**  
**Definición:**  
División de una red en subredes más pequeñas para mejorar el rendimiento, la seguridad y la gestión.  

**Características:**  
- 🔒 **Mayor seguridad:** Aísla problemas (ej: un virus en una subred no afecta a las demás).  
- 🚀 **Mejor rendimiento:** Reduce la congestión del tráfico.  
- 🏢 **Control de acceso:** Permite restringir quién accede a cada segmento.  

**Ejemplo en TECBA:**  
*"El instituto podría tener:  
- Una subred para **aulas** (acceso a materiales).  
- Otra para **administración** (datos sensibles).  
- Una más para **invitados** (Wi-Fi público limitado)."*  

---

#### **2. DMZ (Zona Desmilitarizada)**  
**Definición:**  
Subred aislada que actúa como zona intermedia entre una red interna (privada) e Internet, para alojar servicios accesibles desde fuera (ej: servidores web).  

**Características:**  
- 🛡️ **Protege la red interna:** Si un hacker ataca la DMZ, no llega a los datos críticos.  
- 🌐 **Servicios públicos:** Aloja lo que debe ser accesible desde Internet (ej: sitio web del instituto).  

**Ejemplo en TECBA:**  
*"El **sitio web del instituto** está en la DMZ, pero la **base de datos de calificaciones** está en la red interna (protegida)."*  

**Analogía:**  
*"La DMZ es como la recepción de un edificio: los visitantes (tráfico de Internet) pueden entrar allí, pero no a las oficinas privadas (red interna)."*  

---

### **Parte 2: Ejercicios Prácticos (40 minutos)**  

#### **Ejercicio 1: Diseña la Segmentación del TECBA**  
**Instrucciones:**  
1. En grupos, dibujen un esquema de red para el instituto con:  
   - **Red interna:** Aulas y administración.  
   - **DMZ:** Servidor web público.  
   - **Internet:** Conexión externa.  
2. Usen flechas para mostrar el flujo de tráfico.  

**Ejemplo de solución:**  
```  
[Internet]  
    ↓  
[Firewall]  
    ↓  
[DMZ: Servidor web del TECBA]  
    ↓  
[Firewall interno]  
    ↓  
[Red Interna: Aulas + Administración]  
```  

**Pregunta clave:**  
*"¿Por qué el servidor web no debe estar en la red interna?"*  
*(Respuesta: Porque sería vulnerable a ataques directos desde Internet).*  

---

#### **Ejercicio 2: Caso de Estudio - Ataque a una Red no Segmentada**  
**Escenario:**  
*"Un estudiante descarga un virus en la red Wi-Fi del instituto, y este se propaga a todos los dispositivos (aulas, administración, servidores)."*  

**Preguntas:**  
1. ¿Cómo podría evitarse esto con segmentación?  
   - *(Respuesta: Aislando las redes: el virus solo afectaría la subred del estudiante).*  
2. ¿Qué servicios pondrías en la DMZ para proteger los datos internos?  
   - *(Ejemplo: Solo el sitio web, no el servidor de correo interno).*  

**Discusión en grupo:**  
*"¿Qué otros riesgos hay si no se usa DMZ?"*  
*(Ejemplo: Exposición de datos sensibles como expedientes estudiantiles).*  

---

### **Parte 3: Cierre y Reflexión (10 minutos)**  

#### **Resumen Visual:**  
| **Concepto**       | **Propósito**                  | **Ejemplo TECBA**              |  
|--------------------|--------------------------------|--------------------------------|  
| Segmentación       | Aislar y proteger subredes     | Aulas vs. Administración       |  
| DMZ                | Proteger servicios públicos    | Sitio web institucional        |  

#### **Tarea para la próxima clase:**  
- *"Investiga: ¿Qué empresas en Bolivia usan DMZ? (Ejemplo: Bancos para sus páginas web)."*  

#### **Material Adicional:**  
- **Herramienta interactiva:** [Simulador de redes Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer).  
- **Video recomendado:** *"Cómo configurar una DMZ"* (7 min): [Enlace a YouTube](https://youtu.be/ejemplo).  

---

**Nota para el docente:**  
- Usar **ejemplos locales** para hacerlo más relatable (ej: "Imaginen que el sistema de la Alcaldía de Sucre tiene una DMZ").  
- Si hay acceso a PCs, mostrar un ejemplo real con `ipconfig` para ver subredes.  

**Resultado esperado:**  
Los estudiantes entenderán cómo la segmentación y la DMZ protegen redes críticas, y podrán aplicarlo a entornos educativos o empresariales.