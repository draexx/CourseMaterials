**Unidad Temática 5: Desarrollo de Contenido Web con HTML**  
**Duración:** 3 clases de 1 hora y 20 minutos cada una (total: 4 horas)  

---

### **Clase 1: Fundamentos de HTML y Estructura Básica**  
**Duración:** 1 hora y 20 minutos  

#### **Objetivos:**  
- Comprender la sintaxis básica de HTML.  
- Crear un documento HTML con estructura semántica.  

#### **Contenidos y Actividades:**  
1. **Introducción a HTML (20 minutos)**  
   - *Definición:* Lenguaje de marcado para crear páginas web.  
   - *Estructura básica:*  
     ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>Título</title>
     </head>
     <body>
         Contenido visible
     </body>
     </html>
     ```  
   - *Ejemplo:* Analizar el código fuente de una página simple (ej: Google).  

2. **Etiquetas Básicas (30 minutos)**  
   - *Encabezados:* `<h1>` a `<h6>`.  
   - *Párrafos:* `<p>`.  
   - *Enlaces:* `<a href="url">Texto</a>`.  
   - *Imágenes:* `<img src="ruta" alt="texto alternativo">`.  
   - *Práctica:* Crear una página con título, párrafo, enlace e imagen.  

3. **Validación y Depuración (20 minutos)**  
   - Usar [W3C Validator](https://validator.w3.org/) para verificar errores.  
   - Actividad: Corregir errores en un HTML proporcionado por el docente.  

#### **Tarea:**  
- Diseñar una página personal con nombre, foto y enlace a red social.  

---

### **Clase 2: Tablas, Formularios y Multimedia**  
**Duración:** 1 hora y 20 minutos  

#### **Objetivos:**  
- Dominar el uso de tablas y formularios.  
- Integrar multimedia (audio/video) en HTML.  

#### **Contenidos y Actividades:**  
1. **Tablas (25 minutos)**  
   - *Sintaxis:*  
     ```html
     <table>
         <tr><th>Encabezado</th></tr>
         <tr><td>Dato</td></tr>
     </table>
     ```  
   - *Ejemplo práctico:* Crear tabla de horario de clases.  

2. **Formularios (30 minutos)**  
   - *Elementos:* `<form>`, `<input>`, `<select>`, `<textarea>`.  
   - *Atributos:* `type="text|email|password"`, `required`.  
   - *Práctica:* Formulario de contacto con campos nombre, email y mensaje.  

3. **Multimedia (20 minutos)**  
   - *Audio:* `<audio controls><source src="audio.mp3"></audio>`.  
   - *Video:* `<video controls><source src="video.mp4"></video>`.  
   - *Actividad:* Insertar un video de YouTube usando `<iframe>`.  

#### **Tarea:**  
- Crear un formulario de registro con validación básica (campos obligatorios).  

---

### **Clase 3: Maquetación Avanzada y Publicación**  
**Duración:** 1 hora y 20 minutos  

#### **Objetivos:**  
- Aplicar CSS básico dentro de HTML.  
- Publicar un sitio web en un servidor local.  

#### **Contenidos y Actividades:**  
1. **CSS Inline y Interno (30 minutos)**  
   - *Inline:* `<p style="color:red;">Texto</p>`.  
   - *Interno:*  
     ```html
     <style>
         body { font-family: Arial; }
     </style>
     ```  
   - *Práctica:* Dar estilo a la página personal creada en la Clase 1.  

2. **Estructura Semántica (25 minutos)**  
   - *Etiquetas:* `<header>`, `<nav>`, `<section>`, `<footer>`.  
   - *Ejemplo:* Maquetar un blog con cabecera, menú y pie de página.  

3. **Publicación en Servidor Local (20 minutos)**  
   - Subir archivos HTML a `htdocs` en XAMPP.  
   - Acceder desde `http://localhost/mi_pagina`.  
   - *Discusión:* "¿Cómo escalar esto a un servidor en la nube?".  

#### **Proyecto Final:**  
- Entregar un sitio web con:  
  - Página principal (index.html).  
  - Formulario de contacto.  
  - Estilo CSS básico.  

---

### **Evaluación:**  
- **Participación (20%):** Interacción en prácticas.  
- **Tareas (30%):** Página personal, formulario, maquetación.  
- **Proyecto Final (50%):** Funcionalidad y creatividad.  

### **Recursos:**  
- **Herramientas:** Visual Studio Code, XAMPP, W3C Validator.  
- **Bibliografía:** [MDN Web Docs - HTML](https://developer.mozilla.org/es/docs/Web/HTML).  

**Nota:** Ajustar tiempos para resolver dudas técnicas. Usar analogías como *"HTML es el esqueleto, CSS la ropa"* para clarificar roles.