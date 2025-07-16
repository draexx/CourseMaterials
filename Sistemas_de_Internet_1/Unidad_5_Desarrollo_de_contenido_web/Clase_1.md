**Clase 1: Fundamentos de HTML y Estructura Básica**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Introducción a HTML (25 minutos)**  

#### **Definiciones Clave:**  
1. **¿Qué es HTML?**  
   - *Definición:* Lenguaje de Marcado de Hipertexto (HyperText Markup Language) usado para crear páginas web.  
   - *Analogía:* "El esqueleto de un sitio web" (estructura básica sin diseño).  
   - *Ejemplo visual:*  
     ```html
     <!DOCTYPE html> <!-- Declara el tipo de documento -->
     <html> <!-- Contenedor raíz -->
     <head> <!-- Metadatos (no visibles) -->
         <title>Mi primera página</title> <!-- Título de la pestaña -->
     </head>
     <body> <!-- Contenido visible -->
         <h1>¡Hola mundo!</h1>
     </body>
     </html>
     ```  

2. **Estructura Básica de un Documento HTML:**  
   - **`<!DOCTYPE html>`:** Indica que es un documento HTML5.  
   - **`<html>`:** Envuelve todo el contenido.  
   - **`<head>`:** Incluye metadatos como título, enlaces a CSS, etc.  
   - **`<body>`:** Contiene lo que se ve en el navegador.  

#### **Demostración en Vivo:**  
- Abrir el navegador → Click derecho → "Inspeccionar" → Mostrar el código fuente de una página simple (ej: [http://example.com](http://example.com)).  

---

### **2. Etiquetas Básicas (35 minutos)**  

#### **Etiquetas Fundamentales con Ejemplos Prácticos:**  
| **Etiqueta**  | **Función**                     | **Ejemplo**                          | **Resultado Visual**               |  
|---------------|---------------------------------|--------------------------------------|------------------------------------|  
| `<h1>` a `<h6>` | Encabezados (jerarquía)        | `<h1>Título principal</h1>`          | Texto grande y en negrita          |  
| `<p>`         | Párrafo                        | `<p>Este es un párrafo.</p>`         | Texto normal separado en bloques   |  
| `<a>`         | Enlace                         | `<a href="https://google.com">Google</a>` | Texto azul subrayado (clicable) |  
| `<img>`       | Imagen                         | `<img src="logo.png" alt="Logo">`    | Muestra la imagen (alt: texto alternativo) |  

#### **Actividad Guiada:**  
1. Cada estudiante crea un archivo `index.html` con:  
   - Un título (`<h1>`).  
   - Un párrafo (`<p>`) sobre su hobby favorito.  
   - Un enlace a su red social preferida.  
   - Una imagen local (ej: `foto.jpg`).  

2. Validar que el archivo se abre correctamente en el navegador (arrastrar el archivo a la ventana del navegador).  

---

### **3. Validación y Depuración (20 minutos)**  

#### **Errores Comunes y Cómo Solucionarlos:**  
- **Error típico:** Olvidar cerrar una etiqueta (`<p>Texto` sin `</p>`).  
- **Herramienta:** [Validador W3C](https://validator.w3.org/):  
  1. Subir el archivo `index.html`.  
  2. Analizar errores y corregirlos en clase.  

#### **Ejemplo para Depurar:**  
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo con error</title>
</head>
<body>
    <h1>Bienvenidos</h1>
    <p>Este párrafo no está cerrado  <!-- ¡Falta </p>! -->
</body>
</html>
```  
- *Práctica:* Identificar y corregir 3 errores en un código HTML proporcionado.  

---

### **Cierre y Tarea (5 minutos)**  
- **Resumen:**  
  - *"HTML define la estructura de una web usando etiquetas como `<h1>`, `<p>`, `<a>` e `<img>`."*  
- **Tarea:**  
  - Crear una página con:  
    - Un encabezado con tu nombre.  
    - Dos párrafos (uno sobre ti, otro sobre tu carrera).  
    - Una imagen y un enlace a un sitio educativo (ej: Wikipedia).  

---

### **Material Adicional:**  
- **Plantilla HTML:**  
  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>Mi Página</title>
  </head>
  <body>
      <!-- Contenido aquí -->
  </body>
  </html>
  ```  
- **Extensión Recomendada:** *Live Server* en VS Code (para ver cambios en tiempo real).  

**Nota:** Usar comparaciones como *"Las etiquetas HTML son como instrucciones que le dicen al navegador 'esto es un título' o 'esto es un párrafo'"* para reforzar el concepto. Si hay dudas, repetir la práctica con ejemplos cotidianos (ej: una receta de cocina estructurada con HTML).