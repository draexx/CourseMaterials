### **Clase 3: Sistemas Distribuidos y Arquitectura Cliente-Servidor**  
**Duración:** 1 hora y 20 minutos  

---

#### **Objetivos:**  
1. Comprender el concepto de **sistemas distribuidos** y su importancia en Internet.  
2. Diferenciar entre **arquitectura cliente-servidor** y P2P.  
3. Identificar ejemplos reales en servicios cotidianos.  

---

### **Parte 1: Definiciones Clave (30 minutos)**  

#### **1. Sistemas Distribuidos**  
**Definición:**  
Conjunto de computadoras independientes que trabajan juntas como un sistema único para el usuario.  

**Características:**  
- 🌐 **Recursos compartidos:** Procesamiento, almacenamiento y datos.  
- 🔄 **Transparencia:** El usuario no sabe dónde están físicamente los recursos.  
- ⚡ **Tolerancia a fallos:** Si un nodo falla, otros continúan trabajando.  

**Ejemplos Prácticos:**  
| **Servicio**       | **Cómo usa sistemas distribuidos**                  |  
|--------------------|---------------------------------------------------|  
| Google Drive       | Tus archivos se almacenan en múltiples servidores alrededor del mundo |  
| Netflix            | Las películas vienen de centros de datos cercanos a tu ubicación |  
| Bancos en línea    | Tu saldo se replica en varios servidores para evitar pérdidas |  

**Caso TECBA:**  
*"Cuando subes un trabajo a Moodle, este se guarda en un servidor que podría estar en otra ciudad, pero tú lo ves como si estuviera local."*  

---

#### **2. Arquitectura Cliente-Servidor vs. P2P**  

**A. Cliente-Servidor:**  
- **Definición:** Modelo donde el **cliente** (tu dispositivo) solicita servicios al **servidor** (proveedor).  
- **Ejemplos:**  
  - Navegar en Facebook (tu navegador = cliente, servidores de Meta = servidor).  
  - Consultar tu correo institucional.  

**B. Redes P2P (Peer-to-Peer):**  
- **Definición:** Todos los dispositivos son iguales (clientes y servidores al mismo tiempo).  
- **Ejemplos:**  
  - Torrents (cada computadora comparte fragmentos del archivo).  
  - Blockchain (como Bitcoin).  

**Comparación Visual:**  
```  
Cliente-Servidor: [Cliente] ←→ [Servidor Central]  
P2P:           [Nodo A] ↔ [Nodo B] ↔ [Nodo C]  
```  

---

### **Parte 2: Ejercicios Prácticos (40 minutos)**  

#### **Ejercicio 1: Identifica la Arquitectura**  
**Instrucciones:** Clasifica estos servicios como **Cliente-Servidor (C/S)** o **P2P (P)**:  
1. Spotify (música en streaming). → **C/S**  
2. Skype (llamadas antiguas entre usuarios). → **P**  
3. Plataforma de pagos Tigo Money. → **C/S**  
4. Archivos compartidos por WhatsApp. → **P** (aunque los servidores de Meta median).  

**Discusión:**  
*"¿Por qué WhatsApp no es 100% P2P?"*  
*(Porque los mensajes pasan por servidores centrales de Meta primero).*  

---

#### **Ejercicio 2: Diseña un Sistema Distribuido**  
**Escenario:**  
*"El TECBA quiere un sistema para que los estudiantes accedan a materiales desde cualquier campus (Sucre, La Paz, Cochabamba)."*  

**Pasos:**  
1. Dibuja cómo distribuirías los servidores:  
   - ¿Dónde ubicarías los datos? *(Ej: Réplicas en cada ciudad)*.  
   - ¿Cómo asegurarías que funcione si falla un servidor?  
2. Explica por qué es un sistema distribuido.  

**Ejemplo de solución:**  
```  
[Estudiante en Sucre] ←→ [Servidor en Sucre]  
                           ↑↓ Sincronización  
[Estudiante en La Paz] ←→ [Servidor en La Paz]  
```  

---

### **Parte 3: Cierre y Reflexión (10 minutos)**  

#### **Resumen Visual:**  
| **Concepto**         | **Clave**                          | **Ejemplo TECBA**              |  
|----------------------|-----------------------------------|--------------------------------|  
| Sistemas Distribuidos | Recursos compartidos globalmente  | Moodle accesible desde cualquier campus |  
| Cliente-Servidor     | Centralizado                     | Plataforma de notas            |  
| P2P                  | Descentralizado                  | Compartir archivos en clase via LAN |  

#### **Tarea:**  
- *"Investiga: ¿Qué arquitectura usa Uber? ¿Y Airbnb?"* *(Pista: Ambas son cliente-servidor con sistemas distribuidos).*  

#### **Material Adicional:**  
- **Video recomendado:** *"Cómo Netflix usa sistemas distribuidos"* (5 min): [Enlace a YouTube](https://youtu.be/ejemplo).  
- **Herramienta:** Wireshark para analizar tráfico cliente-servidor (demostración opcional).  

---

**Nota para el docente:**  
- Usar analogías cotidianas: *"Cliente-Servidor es como un restaurante (tu pides, la cocina sirve). P2P es como un potluck (todos traen comida)."*  
- Relacionar con tecnologías bolivianas: *"¿Cómo creen que funciona la app de Pago Fácil?"*  

**Resultado esperado:**  
Los estudiantes podrán explicar cómo funcionan servicios como Google o Netflix detrás de cámaras, y diseñar soluciones básicas distribuidas.