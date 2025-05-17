### **Clase 4: Proyecto Integrador con Pilas - Resolución de Problemas del Mundo Real**  
**Duración:** 1 hora 20 minutos  
**Objetivos:**  
1. Aplicar pilas en un proyecto práctico que simule un escenario real.  
2. Integrar todos los conceptos aprendidos en la unidad.  
3. Fomentar el trabajo en equipo y la creatividad en la solución de problemas.  

---

## **Parte 1: Presentación del Proyecto (15 minutos)**  
**Proyecto:** *Sistema de Gestión de Versiones de Documentos* (como Git simplificado).  

**Requisitos:**  
- Usar pilas para manejar el historial de cambios (`undo`/`redo`).  
- Permitir "guardar" versiones y navegar entre ellas.  
- Opcional: Añadir un sistema de branches (ramas) usando múltiples pilas.  

**Ejemplo de Interfaz:**  
```python  
class VersionControl:  
    def __init__(self):  
        self.versiones_actuales = []  # Pila para el historial  
        self.versiones_deshacer = []  # Pila para el "redo"  
        self.documento = ""           # Contenido actual  

    def guardar_version(self, texto):  
        self.versiones_actuales.append(self.documento)  
        self.documento = texto  
        self.versiones_deshacer = []  # Limpiar redo al guardar  

    def deshacer(self):  
        if self.versiones_actuales:  
            self.versiones_deshacer.append(self.documento)  
            self.documento = self.versiones_actuales.pop()  

    def rehacer(self):  
        if self.versiones_deshacer:  
            self.versiones_actuales.append(self.documento)  
            self.documento = self.versiones_deshacer.pop()  

    def mostrar_historial(self):  
        print("Historial de versiones:", self.versiones_actuales)  
```  

---

## **Parte 2: Desarrollo en Equipo (45 minutos)**  
**Actividad:** Implementar el sistema en grupos de 3-4 estudiantes.  

### **Tareas Clave:**  
1. **Base:**  
   - Implementar `guardar_version`, `deshacer`, y `rehacer`.  
   - Probar con un documento de ejemplo (ej: "Hola" → "Hola Mundo" → "Hola Mundo!").  

2. **Extensión (Opcional):**  
   - Añadir branches (ej: `main` y `develop`). Usar un diccionario de pilas:  
     ```python  
     self.branches = {  
         "main": Pila(),  
         "develop": Pila()  
     }  
     ```  
   - Implementar `cambiar_branch(nombre)` y `fusionar_branch(origen, destino)`.  

3. **Bonus:**  
   - Guardar metadata (fecha, autor) en cada versión.  

**Ejemplo de Prueba:**  
```python  
vc = VersionControl()  
vc.guardar_version("Versión 1")  
vc.guardar_version("Versión 2")  
vc.deshacer()  
print(vc.documento)  # "Versión 1"  
vc.rehacer()  
print(vc.documento)  # "Versión 2"  
```  

---

## **Parte 3: Presentaciones y Retroalimentación (20 minutos)**  
- Cada equipo demuestra su solución (5 minutos por equipo).  
- **Preguntas clave:**  
  - ¿Cómo manejan conflictos al fusionar branches?  
  - ¿Qué estructura usaron para almacenar metadata?  
- **Discusión grupal:** Ventajas/desventajas de usar pilas vs. bases de datos para este sistema.  

---

### **Rúbrica de Evaluación**  
| **Criterio**               | **Puntos** |  
|----------------------------|------------|  
| Funcionalidad básica       | 40%        |  
| Implementación de branches | 30%        |  
| Creatividad y extras       | 20%        |  
| Presentación clara         | 10%        |  

---

### **Material Adicional**  
- **Lectura:** [Cómo funciona Git internamente](https://git-scm.com/book/en/v2/Git-Internals).  
- **Video:** [Undo/Redo en editores de código](https://youtu.be/7sSY4qFE-8k).  

**¿Qué otro proyecto te gustaría implementar con pilas?** 😊  

--- 

**Nota:** Adaptar la complejidad según el nivel del grupo. Para principiantes, enfocarse en la parte básica; para avanzados, profundizar en branches y merging.