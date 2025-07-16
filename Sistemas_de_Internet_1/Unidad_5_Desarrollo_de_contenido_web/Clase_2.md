**Clase 2: Tablas, Formularios y Multimedia en HTML**  
**Duración:** 1 hora y 20 minutos  

---

### **1. Tablas en HTML (25 minutos)**  

#### **Definiciones y Estructura:**  
- **¿Qué es una tabla HTML?**  
  Estructura para organizar datos en filas (`<tr>`) y columnas (`<td>` o `<th>` para encabezados).  

- **Sintaxis Básica:**  
  ```html
  <table border="1">  <!-- El atributo border es opcional -->
      <tr> <!-- Fila -->
          <th>Nombre</th> <!-- Celda de encabezado -->
          <th>Edad</th>
      </tr>
      <tr>
          <td>Ana</td> <!-- Celda de dato -->
          <td>25</td>
      </tr>
  </table>
  ```  

#### **Ejemplo Práctico:**  
Crear una tabla de horario de clases:  
```html
<table>
    <tr>
        <th>Hora</th><th>Lunes</th><th>Miércoles</th>
    </tr>
    <tr>
        <td>8:00</td><td>Matemáticas</td><td>Programación</td>
    </tr>
</table>
```  
*Resultado:*  

| Hora  | Lunes       | Miércoles    |  
|-------|-------------|--------------|  
| 8:00  | Matemáticas | Programación |  

#### **Actividad:**  
- Cada estudiante crea una tabla con 3 compañeros ficticios (Nombre, Email, Teléfono).  

---

### **2. Formularios HTML (35 minutos)**  

#### **Definiciones y Elementos Clave:**  
- **Propósito:** Recopilar datos del usuario (ej: login, contacto).  
- **Estructura Básica:**  
  ```html
  <form action="/procesar" method="POST"> <!-- action: URL destino -->
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" required> <!-- required: campo obligatorio -->
      <input type="submit" value="Enviar">
  </form>
  ```  

#### **Tipos de Input Comunes:**  
| **Tipo**       | **Uso**                     | **Ejemplo**                          |  
|----------------|-----------------------------|--------------------------------------|  
| `text`         | Texto corto                 | `<input type="text" name="usuario">` |  
| `email`        | Validación de email         | `<input type="email" name="correo">` |  
| `password`     | Contraseña (oculta)         | `<input type="password" name="clave">` |  
| `checkbox`     | Selección múltiple          | `<input type="checkbox" name="intereses" value="deportes"> Deportes` |  
| `radio`        | Selección única             | `<input type="radio" name="genero" value="femenino"> Femenino` |  
| `textarea`     | Texto largo                 | `<textarea name="comentario"></textarea>` |  

#### **Ejemplo Completo:**  
Formulario de registro:  
```html
<form>
    <label>Email: <input type="email" required></label><br>
    <label>Contraseña: <input type="password" required></label><br>
    <label>Edad: <input type="number" min="18"></label><br>
    <label><input type="checkbox"> Acepto términos</label><br>
    <input type="submit" value="Registrarse">
</form>
```  

#### **Actividad:**  
- Crear un formulario para una "pizza online" con:  
  - Tipo de masa (radio buttons: delgada/gruesa).  
  - Ingredientes (checkboxes: jamón, champiñones, etc.).  
  - Dirección de entrega (textarea).  

---

### **3. Multimedia (20 minutos)**  

#### **Insertar Audio y Video:**  
- **Video:**  
  ```html
  <video controls width="300"> <!-- controls: muestra reproductor -->
      <source src="video.mp4" type="video/mp4">
      Tu navegador no soporta video.
  </video>
  ```  
- **Audio:**  
  ```html
  <audio controls>
      <source src="audio.mp3" type="audio/mpeg">
  </audio>
  ```  

#### **Insertar Video de YouTube (Embed):**  
```html
<iframe width="560" height="315" 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
    frameborder="0" allowfullscreen>
</iframe>
```  

#### **Actividad Rápida:**  
- Añadir un video de YouTube y un reproductor de audio local a la página personal creada en la Clase 1.  

---

### **Cierre y Tarea (5 minutos)**  
- **Resumen:**  
  - *"Las tablas organizan datos, los formularios capturan información, y multimedia enriquece la experiencia web."*  
- **Tarea:**  
  - Crear una página con:  
    1. Tabla de productos (Nombre, Precio, Stock).  
    2. Formulario de contacto (Nombre, Email, Mensaje).  
    3. Un video incrustado.  

---

### **Recursos Adicionales:**  
- **Validador de Formularios:** [W3C Validator](https://validator.w3.org/).  
- **Ejemplo de Código:**  
  ```html
  <!-- Tabla + Formulario + Video -->
  <!DOCTYPE html>
  <html>
  <body>
      <table>...</table>
      <form>...</form>
      <iframe>...</iframe>
  </body>
  </html>
  ```  

**Nota:** Usar analogías como *"Un formulario es como un cuestionario que el usuario llena para 'hablar' con el servidor"*. Para dudas técnicas, mostrar ejemplos en tiempo real con [CodePen](https://codepen.io/).