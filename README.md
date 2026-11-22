# GRIU — Gestión de Reportes de Incidentes Urbanos

Plataforma web híbrida para la radicación anónima, el seguimiento y la gestión
administrativa de incidentes urbanos en Neiva (Huila, Colombia).

**Nivel de madurez:** TRL 5 · **Fase 4** · Curso Proyecto de Grado (202016907_72) ·
Universidad Nacional Abierta y a Distancia (UNAD) · 2026

---

## 1. Problema que resuelve

La gestión de incidentes urbanos en el área urbana de Neiva enfrenta limitaciones
operativas que afectan la movilidad, la seguridad y el bienestar de sus habitantes.
El canal institucional de Peticiones, Quejas, Reclamos, Sugerencias, Denuncias y
Felicitaciones (PQRSDF) carece de funcionalidades clave: geolocalización en tiempo
real, carga de evidencia fotográfica y mecanismos ágiles de trazabilidad.

El diagnóstico aplicado a 30 ciudadanos del área urbana de Neiva lo confirma:

- El **83,33 %** observa incidentes urbanos con alta frecuencia (diaria o semanal).
- El **61,9 %** de los 21 usuarios que radicaron un reporte esperó más de 30 días
  hábiles o no recibió respuesta.
- La satisfacción general con el canal es reprobatoria (**M = 1,93 / 5,00**).
- El **43,33 %** señala los registros engorrosos como la principal barrera de acceso.

Como consecuencia, los reportes se dispersan en canales informales, se pierde
información y la administración municipal pierde capacidad para priorizar
intervenciones.

## 2. Descripción general de la solución

GRIU combina dos módulos sobre un mismo modelo de datos geoespacial:

| Módulo | Actor | Funciones principales |
|---|---|---|
| **Público y consulta ciudadana** | Ciudadano | Radicación anónima con geolocalización y evidencia fotográfica, código alfanumérico de radicado, consulta de estado sin registro, mapa público con filtros por categoría y comuna |
| **Acceso y panel administrativo** | Funcionario municipal | Inicio de sesión con validación anti-bot, tablero de indicadores, listado y filtrado de reportes, cambio de estado (Radicado → En Proceso → Resuelto), mapa de calor, notificaciones y exportación a PDF y Excel |

**Requerimientos:** 8 funcionales (RF-01 a RF-08) y 6 no funcionales (RNF-01 a
RNF-06), derivados del diagnóstico y priorizados con MoSCoW.
**Product Backlog:** 17 historias de usuario, 11 Must have (35 puntos) que definen
el alcance del MVP.
**Arquitectura objetivo:** tres capas con patrón MVC, MySQL con tipos de datos
espaciales, HTML5/CSS3/Bootstrap/JavaScript sobre XAMPP.

## 3. Equipo

| Integrante | Rol en el proyecto | Rol Scrum |
|---|---|---|
| Andrés Felipe León Zuleta | Estudiante formulador | Equipo de desarrollo |
| María Isabel Irreño Marín | Estudiante formuladora | Equipo de desarrollo |
| Camilo Durán Suárez | Estudiante formulador | Equipo de desarrollo |

**Vinculación:** académica UNAD · **Semillero:** GRUSLIN · **Grupo:** Byte In Design

## 4. Prototipo interactivo (Figma)

**Enlace:** https://www.figma.com/proto/dJxD7bfTBqfYPDgdcoHXF4/Proyecto-GRIU-2.0?page-id=0%3A1&node-id=33-320&viewport=-1917%2C-195%2C0.13&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=33%3A320

Se recorre en el **modo Presentar** del archivo (no en el modo de edición). El
archivo se organiza en **13 secciones temáticas y 3 subsecciones**, con **204
frames** que incluyen pantallas, modales y estados de interacción.

| Sección | Contenido |
|---|---|
| 01 · Público y consulta ciudadana | Inicio, fichas de detalle, reportes recientes y ayuda |
| 01B · Mapa ciudadano | Variantes de mapa por categoría y comuna, y fichas de detalle |
| 02 · Acceso y panel administrativo | Login y estados de acceso, tablero, perfil, recuperación de contraseña, fichas y modales de cambio de estado |
| 03 · Creación de reporte | Formulario, errores, evidencia cargada, envío y confirmación con código |
| 04 · Total de reportes (estado inicial) | Tabla base, variantes de filtro, paginación, fichas y modales |
| 04B · Búsqueda por filtro (estado inicial) | Variantes de búsqueda por comuna, categoría y estado |
| 05 · Total de reportes (estado posterior) | Tabla con el reporte recién creado |
| 05B · Búsqueda por filtro (estado posterior) | Variantes de búsqueda tras la creación |
| 06 · Mapa de calor e indicadores | Mapa de calor e indicadores agregados |
| 07 · Componentes de formulario | Hoja de componentes reutilizables |
| 08 · Componentes de navegación | Barra lateral, barra superior, menú e iconografía |
| 09 · Borradores | Frame de verificación, excluido de la entrega |
| 10 · Notificaciones | Bandejas y fichas de detalle |
| 11 · Copiar y exportar | Estados de copiado y exportación a PDF y Excel |
| 12 · Menú lateral colapsado | Variantes de menú y menú de usuario |
| 13 · Caso 4C7E | Radicado, gestión y consulta de un caso completo |

### Cómo recorrerlo en 5 minutos

1. **Radicar:** sección 03 → diligenciar el formulario → verificar la ubicación en
   el mapa → adjuntar evidencia → «Enviar reporte» → anotar el código generado.
2. **Consultar:** sección 01 → campo de consulta por código → ficha de detalle con
   estado y trazabilidad.
3. **Gestionar:** sección 02 → iniciar sesión → sección 04 → filtrar por comuna,
   categoría o estado → abrir un reporte → cambiar su estado.
4. **Leer el territorio:** sección 06 → mapa de calor e indicadores agregados.
5. **Exportar:** sección 11 → copiar reportes o descargar PDF/Excel.

## 5. Video demostrativo

**Enlace:** https://youtu.be/oQZq4o5fSys · Duración máxima: 10 minutos · Cámaras encendidas

Presenta el manejo y las funciones principales del prototipo: radicación de un
incidente, consulta por código, gestión administrativa y visualización geográfica.

## 6. Estructura del repositorio

```
GRIU-gestion-incidentes-urbanos/
├── README.md                  Este archivo
├── LICENSE                    Condiciones de uso y autoría
├── .gitignore                 Exclusiones de archivos temporales y credenciales
├── docs/                      Informe final
│   └── Fase4_DocumentoMaestro_GRIU_Proyecto1_72.pdf
├── src/                       Material del prototipo
│   └── Proyecto GRIU 2.0.fig  Exportación del archivo de Figma
├── data/                      Datos del diagnóstico
│   ├── 02_Matriz_Respuestas_n30_Google_Sheets.xlsx
│   ├── graficosEncuesta.xlsx
│   ├── resumenRepuestasGraficosGoogleForms.docx
│   └── cuestionario_15_preguntas.md
└── evidencias/                Evidencia de ejecución
    ├── capturas/              Figuras 25 a 30 del documento maestro
    ├── verificacion/          Registro CP-01 a CP-08 y escenarios E1 a E5
    ├── scrum/                 Ceremonias y bitácora de sesiones
    └── video/                 Enlace al video demostrativo
```

## 7. Alcance y nivel TRL 5

El incremento de la Fase 4 es un **prototipo funcional e interactivo de alta
fidelidad**, no una implementación codificada. La decisión es coherente con la
definición de TRL 5 adoptada: la tecnología se valida en un entorno relevante
mediante un prototipo que demuestra la integración de sus componentes.

- **Cobertura del MVP:** 11 de 11 historias Must have verificadas (35 de 35 puntos,
  100 % del alcance comprometido), por encima del umbral del 80 % fijado para la fase.
- **Verificación funcional:** 5 escenarios de extremo a extremo (E1 a E5) y 8 casos
  de prueba (CP-01 a CP-08) recorridos en el modo Presentar del archivo.
- **Criterio de terminado (DoD):** pantallas construidas y conectadas, criterio de
  aceptación BDD verificado sobre el flujo, validaciones visibles en la interfaz,
  recorrido sin interrupciones y evidencia archivada en este repositorio.

## 8. Limitaciones declaradas

- No es un despliegue en producción ni una prueba en entorno operativo.
- No incluye persistencia real en base de datos: el alcance de la fase se concentra
  en el prototipo interactivo.
- La verificación se realizó por inspección de los flujos sobre datos de prueba
  precargados; **no incorporó una muestra de usuarios**, por lo que no arroja
  puntuaciones de usabilidad.
- La prueba con usuarios y la aplicación del cuestionario SUS (Brooke, 1996)
  corresponden al **TRL 6**, junto con la implementación codificada.

## 9. Licencia

Contenido académico bajo **Creative Commons Atribución-NoComercial-CompartirIgual
4.0 Internacional (CC BY-NC-SA 4.0)**. Ver [LICENSE](LICENSE).

---

**Cómo citar este repositorio**

> León Zuleta, A. F., Irreño Marín, M. I., & Durán Suárez, C. (2026). *GRIU:
> Gestión de Reportes de Incidentes Urbanos* [Prototipo interactivo y repositorio
> documental]. Universidad Nacional Abierta y a Distancia.
