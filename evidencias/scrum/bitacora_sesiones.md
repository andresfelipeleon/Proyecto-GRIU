# Bitácora de ejecución y ceremonias Scrum — GRIU

**Proyecto:** GRIU · Fase 4 · Curso 202016907_72 · UNAD
**Metodología:** CDIO + Scrum · **Equipo:** 3 estudiantes formuladores

Este documento reúne la evidencia de ejecución de la metodología descrita en el
apartado de metodología de desarrollo de software del documento maestro. La primera
tabla consolida, por sprint, el objetivo comprometido, el incremento obtenido, el
resultado de la revisión y la acción de mejora de la retrospectiva. La segunda
registra la bitácora de las diecinueve sesiones de trabajo: las diez primeras
corresponden a la Fase 3 y las nueve restantes a la Fase 4.

## 1. Ceremonias y resultados por sprint

| Sprint | Objetivo del sprint | Incremento obtenido | Revisión: resultado y decisión | Retrospectiva: acción de mejora |
|---|---|---|---|---|
| Sprint 0 (4 semanas) | Definir el catálogo de requerimientos y el Product Backlog priorizado a partir del diagnóstico. | Instrumento validado, matriz de respuestas (n = 30), análisis por pregunta y Product Backlog con quince historias estimadas (49 puntos). | Se acepta la priorización MoSCoW y se fijan las once historias Must have (35 puntos) como alcance del MVP. | La revisión documental se concentró en pocas sesiones; acción: fijar dos sesiones semanales de trabajo. |
| Sprint 1 (5 semanas) | Diseñar la arquitectura, el modelo de datos y los mockups de las interfaces. | Arquitectura en tres capas, modelo entidad-relación y cuatro mockups (Figuras 21 a 24); versión preliminar del archivo de Figma. | Se acepta el diseño y se decide ampliar el archivo a trece secciones para la Fase 4. | La curva de aprendizaje de Figma retrasó los mockups; acción: construir una biblioteca de componentes reutilizables (secciones 07 y 08). |
| Sprint 2 (5 semanas) | Llevar el módulo de radicación ciudadana a un prototipo navegable. | Sección 03 con formulario, estados de error, evidencia y confirmación con código; consulta pública en la sección 01. | HU-01, HU-03 y HU-04 pasan a Verificada; HU-02 y HU-06 se cierran en el Sprint 4. | El bloqueo anti-bot se dejó para el final; acción: construir la validación en la misma sesión del formulario. |
| Sprint 3 (5 semanas) | Construir el panel administrativo con gestión de estados, filtros e indicadores. | Secciones 02, 04, 05, 06, 10 y 11; quince modales de cambio de estado y mapa de calor. | HU-07, HU-08 y HU-11 pasan a Verificada, junto con HU-13, HU-14 y HU-15; HU-05 y HU-09 se cierran en el Sprint 4. | El número de variantes de filtro creció sin control; acción: congelar el alcance de frames y priorizar las historias Must have. |
| Sprint 4 (4 semanas) | Verificar los flujos de extremo a extremo sobre el prototipo y consolidar el registro de verificación funcional. | Prototipo interactivo completo con los ocho casos de prueba ejecutados (CP-01 a CP-08) y las once historias Must have verificadas (35/35 puntos, 100 % del MVP). | Se acepta el incremento: cobertura del 100 % del alcance Must have, por encima del umbral del 80 %; el cuestionario SUS se traslada al TRL 6. | La verificación se concentró en el modo Presentar del archivo; acción: incorporar la prueba con usuarios y el cuestionario SUS en la fase TRL 6. |
| Cierre (3 semanas) | Consolidar el documento maestro, el repositorio y el video demostrativo. | En ejecución: documento maestro ampliado, anexos y video. | Revisión integral del 14 de noviembre de 2026: se acepta el documento con ajustes de coherencia. | Acción: mantener la bitácora desde la primera sesión en las próximas fases. |

## 2. Bitácora de sesiones de trabajo

| Fecha | Sprint | Tipo de sesión | Avance registrado | Decisión o bloqueo |
|---|---|---|---|---|
| 28/09/2026 | Sprint 0 | Revisión documental | Revisión de la Ley 1755 de 2015 y de los canales PQRSDF; ajuste del cuestionario diagnóstico. | Se fija el instrumento de quince preguntas en tres módulos. |
| 01/10/2026 | Sprint 0 | Validación y despliegue | Validación del instrumento y publicación del formulario en Google Forms con consentimiento informado. | El formulario queda habilitado para la aplicación. |
| 02/10/2026 | Sprint 0 | Aplicación del instrumento | Aplicación del cuestionario a treinta ciudadanos de Neiva y cierre de la recolección. | Muestra cerrada en n = 30. |
| 03/10/2026 | Sprint 0 | Análisis de datos | Tabulación, estadística descriptiva y consolidación de la matriz de respuestas. | Se adopta el análisis por pregunta con tabla, gráfico e interpretación. |
| 04/10/2026 | Sprint 0 | Definición de requerimientos | Redacción de los ocho requerimientos funcionales y seis no funcionales derivados de los hallazgos. | Se aprueba el catálogo de requerimientos. |
| 06/10/2026 | Sprint 1 | Planificación del sprint | Construcción del Product Backlog con priorización MoSCoW y estimación en puntos de historia. | Once historias Must have (35 puntos) definen el MVP. |
| 10/10/2026 | Sprint 1 | Diseño técnico | Arquitectura en tres capas, diagrama de componentes y modelo entidad-relación con soporte geoespacial. | Se adopta el patrón MVC sobre el stack previsto. |
| 14/10/2026 | Sprint 1 | Prototipado | Apertura del archivo de Figma: páginas, estilos y biblioteca de componentes reutilizables. | Se define la organización en secciones temáticas. |
| 16/10/2026 | Sprint 1 | Prototipado | Mockups de las cuatro pantallas clave: formulario, consulta, ficha de detalle y panel administrativo. | Se aprueban los cuatro mockups de la Fase 3. |
| 18/10/2026 | Sprint 1 | Revisión del incremento | Recorrido del prototipo navegable preliminar y redacción de los once casos de uso. | Se decide ampliar el archivo a trece secciones para la Fase 4. |
| 28/10/2026 | Sprint 2 | Configuración | Definición de estados, datos de prueba y navegación del archivo para la Fase 4. | Se habilita la interacción de extremo a extremo. |
| 31/10/2026 | Sprint 2 | Prototipado | Formulario público con validaciones, estados de error, carga de evidencia y confirmación con código. | Se cierra el flujo de radicación (HU-01 y HU-03). |
| 03/11/2026 | Sprint 2 | Revisión del incremento | Consulta pública por código y ficha de detalle con trazabilidad de estados. | HU-04 pasa a Verificada; HU-02 y HU-06 quedan pendientes. |
| 04/11/2026 | Sprint 3 | Prototipado | Acceso al panel administrativo, control de sesión y tablero con indicadores agregados. | HU-07 pasa a Verificada. |
| 05/11/2026 | Sprint 3 | Prototipado | Listado de reportes con filtros por categoría y estado, y paginación. | Se fija el repertorio de variantes de filtro. |
| 08/11/2026 | Sprint 3 | Prototipado | Modales de cambio de estado con historial y bandejas de notificación al ciudadano. | HU-08 y HU-12 pasan a Verificada. |
| 12/11/2026 | Sprint 3 | Revisión del incremento | Mapa de calor, indicadores por categoría y exportación a PDF y Excel. | HU-13, HU-14 y HU-15 pasan a Verificada. |
| 14/11/2026 | Sprint 4 | Revisión del incremento | Recorrido completo del prototipo en modo Presentar, ejecución de los casos de prueba CP-01 a CP-08 y verificación de la cobertura de las historias Must have. | Se acepta el incremento con el 100 % de cobertura del MVP; HU-02, HU-05, HU-06, HU-09 y HU-10 pasan a Verificada. |
| 18/11/2026 (prevista) | Cierre | Retrospectiva y consolidación (prevista) | Retrospectiva del proyecto, consolidación del documento maestro y preparación de la entrega. | Se acordará mantener la bitácora desde la primera sesión en próximas fases. |

## 3. Artefactos asociados

- Product Backlog priorizado (17 historias; 11 Must have = 35 puntos).
- Sprint Backlog de los sprints 0 a 4 y de la fase de cierre.
- Definition of Done con cinco condiciones de terminado.
- Registro de verificación funcional (`evidencias/verificacion/registro_verificacion.md`).
