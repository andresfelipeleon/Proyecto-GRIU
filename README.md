# GRIU - Gestión de Reportes de Incidentes Urbanos

**Proyecto Aplicado - Fase 4: Prototipo Funcional de Alta Fidelidad (TRL 5)**
*Universidad Nacional Abierta y a Distancia (UNAD)*
*Curso: Proyecto de Grado (202016907_72)*

## 📌 Descripción del Proyecto
GRIU es una plataforma web híbrida diseñada para optimizar la radicación, seguimiento y atención de incidentes urbanos en la ciudad de Neiva. El sistema permite a los ciudadanos reportar de forma anónima problemas de infraestructura (malla vial, acueducto, semaforización y alumbrado público) con geolocalización GPS y evidencia fotográfica, mientras provee a la administración municipal un panel administrativo seguro para la gestión y priorización de dichos reportes.

Para esta fase (TRL 5), la validación funcional de extremo a extremo se realiza mediante un **prototipo interactivo de alta fidelidad** desarrollado en Figma, estructurado con base en los requerimientos funcionales y no funcionales levantados en la fase de diagnóstico.

## 👥 Integrantes del Proyecto
*   Andrés Felipe León Zuleta
*   María Isabel Irreño Marín
*   Camilo Durán Suárez
*   **Tutor:** Daniel Andrés Guzmán Arevalo

## 🛠️ Tecnologías y Herramientas
*   **Prototipado UI/UX:** Figma (12 secciones, 139 frames interactivos).
*   **Metodología de Desarrollo:** CDIO + Scrum.
*   **Backend (Diseño lógico):** PHP (Patrón MVC).
*   **Base de Datos:** MySQL (con tipos de datos espaciales).
*   **Frontend (Diseño lógico):** HTML5, CSS3, JavaScript, Bootstrap.
*   **Cartografía:** OpenStreetMap + Leaflet.
*   **Seguridad:** Google reCAPTCHA.

## ⚙️ Funcionalidades del Prototipo (MVP)
1.  **Módulo Ciudadano:**
    *   Radicación anónima de reportes (sin creación de cuenta).
    *   Simulación de geolocalización GPS automática.
    *   Carga de evidencia fotográfica.
    *   Generación de código alfanumérico único de seguimiento.
    *   Consulta pública de estado del reporte.
    *   Mapa interactivo público con incidentes reportados.
    *   Validación de seguridad (reCAPTCHA).
2.  **Módulo Administrativo:**
    *   Autenticación de funcionarios (Login).
    *   Panel de gestión de reportes (Listar, filtrar por categoría).
    *   Actualización de estado del reporte (Radicado, En Proceso, Resuelto).
    *   Priorización de incidentes por categoría.

## 🔗 Enlaces de Interés (Entregables Fase 4)
*   🎨 **Prototipo Interactivo en Figma:** <a href="https://www.figma.com/proto/dJxD7bfTBqfYPDgdcoHXF4/Proyecto-GRIU-2.0?page-id=0%3A1&node-id=33-320&viewport=-1917%2C-195%2C0.13&t=XGCxUJrXjoNt6ULH-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=33%3A320" target="_blank">Proyecto GRIU</a>


*   🎥 **Video Demostrativo (TRL 5):** **Pendiente por realizar**

*   📄 **Documento Maestro Completo:** Ver carpeta `/docs` de este    repositorio.

## 📂 Contenido del Repositorio (Estructuración Tabla 37)

El repositorio replica la organización de carpetas definida en la Tabla 37 del Documento Maestro:

| Elemento | Contenido | Ubicación |
| :--- | :--- | :--- |
| **Documentación** | README con nombre, objetivo, descripción, integrantes e instrucciones de uso. | `README.md` |
| **Archivos del prototipo**| Exportación del archivo de Figma, PDF de pantallas y hoja de componentes. | `/src` |
| **Informe final** | Documento maestro en formato PDF. | `/docs` |
| **Datos y recursos** | Matriz de respuestas del instrumento (n = 30), gráficos y cuestionario. | `/data` |
| **Evidencias** | Capturas de pantalla, video demostrativo, acta de validación y registros de prueba. | `/evidencias` |
| **Licencia** | Condiciones de uso y autoría del proyecto. | `LICENSE` |

## 🚀 Instrucciones de Uso
1.  **Para ver el prototipo:** Ingrese al enlace de Figma proporcionado en la sección de enlaces. Utilice el modo "Presentación" para navegar por los flujos de ciudadano y administrador.
2.  **Para revisar los artefactos:** Diríjase a la carpeta `/docs` para leer el documento maestro y a la carpeta `/data` para revisar el diagnóstico investigativo (n=30).
3.  **Para validar el TRL 5:** Consulte los archivos en la carpeta `/evidencias`, donde encontrará el acta de validación y el video demostrativo del flujo operativo.

## 📄 Licencia
Este proyecto es de uso académico y fue desarrollado como trabajo de grado para la Universidad Nacional Abierta y a Distancia (UNAD). Consulte el archivo `LICENSE` para más detalles sobre los términos de uso y autoría.
