# Registro de verificación funcional — GRIU (TRL 5)

**Proyecto:** GRIU — Gestión de Reportes de Incidentes Urbanos
**Fase:** 4 · Componente práctico · Curso 202016907_72 · UNAD
**Fecha de la sesión de verificación:** 14 de noviembre de 2026
**Entorno:** prototipo interactivo de alta fidelidad en Figma, recorrido en el modo
**Presentar** del archivo, con datos de prueba precargados.

---

## 1. Alcance y método

La verificación comprueba que los flujos del sistema operan de extremo a extremo
sobre el prototipo interactivo. No es una prueba con usuarios: se realiza por
**inspección funcional** de cada flujo, contrastando el resultado observado con el
criterio de aceptación de la historia de usuario correspondiente.

Se ejecutaron **5 escenarios de extremo a extremo (E1 a E5)** y **8 casos de prueba
(CP-01 a CP-08)**. El criterio de aceptación de la fase se fijó en al menos el 80 %
de las funciones del alcance comprometido; el resultado alcanzó el 100 % de las
historias Must have (35 de 35 puntos).

**Resultado global:** 8 de 8 casos de prueba conformes · 11 de 11 historias Must
have verificadas · 35 de 35 puntos (100 % del MVP).

## 2. Escenarios de extremo a extremo

| Escenario | Flujo evaluado | Historias | Criterio de aceptación | Resultado |
|---|---|---|---|---|
| E1 | Radicación anónima: formulario, validación de campos, geolocalización, evidencia y confirmación | HU-01, HU-02, HU-03 | El flujo concluye en la pantalla de confirmación con el código alfanumérico generado | Conforme |
| E2 | Consulta pública por código y despliegue del estado del reporte | HU-04 | El estado mostrado corresponde al código consultado | Conforme |
| E3 | Gestión administrativa: acceso, filtros, ficha y cambio de estado | HU-07, HU-08, HU-09 | El cambio de estado se refleja en la ficha y en el listado | Conforme |
| E4 | Visualización geográfica e indicadores agregados | HU-05, HU-14 | El mapa presenta los reportes y el mapa de calor responde a los filtros | Conforme |
| E5 | Control de sesión del panel y validación anti-bot del formulario | HU-06, HU-07 | El acceso exige credenciales y el envío se bloquea sin la validación | Conforme |

## 3. Casos de prueba

| ID | Historia | Acción evaluada | Resultado esperado | Tipo | Resultado | Evidencia (sección, nodo) |
|---|---|---|---|---|---|---|
| CP-01 | HU-01 | Enviar el formulario con los campos obligatorios diligenciados | Confirmación con código alfanumérico único | Funcional | Conforme | 03 · `146:464` → `252:1649` |
| CP-02 | HU-01 | Enviar el formulario con campos obligatorios vacíos | Mensajes de error visibles y envío bloqueado | Negativa | Conforme | 03 · `146:464` |
| CP-03 | HU-03 | Adjuntar una imagen como evidencia del incidente | Vista previa de la imagen cargada | Funcional | Conforme | 03 · `361:13720` |
| CP-04 | HU-04 | Consultar un reporte con el código generado | Estado y trazabilidad del reporte | Funcional | Conforme | 01 · `314:13998` |
| CP-05 | HU-08 | Cambiar el estado de un reporte desde el panel | Estado actualizado en la ficha y en el listado | Funcional | Conforme | 02 · `370:23834` · `383:26099` |
| CP-06 | HU-09 | Filtrar el listado por categoría, comuna, estado y criticidad | Listado filtrado y ordenado por criticidad, sin registros inconsistentes | Funcional | Conforme | 04 y 05 · `275:17798` · `267:5152` |
| CP-07 | HU-15 | Exportar el listado a PDF y a Excel | Confirmación de la acción y archivo generado | Funcional | Conforme | 11 · `437:31575` · `437:31824` |
| CP-08 | HU-07 | Acceder al panel sin credenciales válidas | Acceso denegado y mensaje de error | Negativa | Conforme | 02 · `81:3036` · `540:34505` |

## 4. Cobertura por sprint

| Sprint | Historias de usuario | Puntos | Verificadas | Por verificar | Por incorporar |
|---|---|---|---|---|---|
| Sprint 2 | HU-01, HU-02, HU-03, HU-04, HU-06 y HU-10 | 20 | 6 (20 puntos) | 0 | 0 |
| Sprint 3 | HU-05, HU-07, HU-08, HU-09 y HU-11 | 15 | 5 (15 puntos) | 0 | 0 |
| **Total del MVP** | **11 historias** | **35** | **11 (35 puntos)** | **0** | **0** |
| Historias Should y Could | HU-12, HU-13, HU-14 y HU-15 | 14 | 4 (14 puntos) | 0 | 0 |
| **Total del backlog** | **15 historias** | **49** | **15 (49 puntos)** | **0** | **0** |

## 5. Trazabilidad entre historias y pantallas

| HU | Historia de usuario | Pts. | Sección | Evidencia en el prototipo | Estado |
|---|---|---|---|---|---|
| HU-01 | Radicación anónima de incidente | 5 | 03 | CrearReportes (`146:464`) y CrearReporteExitoso con el código 4C7E (`252:1649`) | Verificada |
| HU-02 | Geolocalización automática del incidente | 5 | 03 | CrearReportes · selección de la ubicación sobre el mapa (`146:464`) | Verificada |
| HU-03 | Carga de evidencia fotográfica | 3 | 03 | CrearReportes · Foto cargada (`361:13720`) | Verificada |
| HU-04 | Consulta de estado del reporte | 3 | 01 | PagInicio · Detalle GRIU-2026-89A4 y consulta por código (`314:13998`) | Verificada |
| HU-05 | Visualización en el mapa público | 5 | 01B | Mapa · Malla vial a Mapa · Comuna 7: doce variantes por categoría y comuna (`595:35708` a `595:38876`) | Verificada |
| HU-06 | Validación anti-bot al enviar | 2 | 02 | Login · anti-bot requerido (`540:34505`) | Verificada |
| HU-07 | Acceso seguro al panel administrativo | 3 | 02 | LoginAdministradorGRIU (`81:3036`) y RecuperarContraseña (`453:34305`) | Verificada |
| HU-08 | Gestión y cambio de estado de reportes | 3 | 02 | ModalCambioEstado · 89A4 (`370:23834`) y Caso · Seguimiento ciudadano 89A4 resuelto (`383:26099`) | Verificada |
| HU-09 | Priorización por criticidad | 2 | 04 y 05 | TotalReportes · Filtro categoría (`275:17798`), TotalReportes · Malla vial (`267:5152`) y filtros por estado y comuna | Verificada |
| HU-10 | Diseño adaptable de la interfaz | 2 | 12 y 08 | 01 · Dashboard · menú colapsado (`443:34215`) y Barra administrativa · Menú adaptable (`485:34169`) | Verificada |
| HU-11 | Interfaz intuitiva y accesible | 2 | 07 y 08 | COMPONENTES · crear reporte (`253:1541`) y biblioteca de navegación | Verificada |
| HU-12 | Notificación al ciudadano | 3 | 10 | Dashboard · Notificaciones y sus tres fichas de detalle (`417:25088` a `417:25506`) | Verificada |
| HU-13 | Dashboard con estadísticas agregadas | 3 | 02 y 06 | PanelAdmin (`114:1386`) e Indicadores (`180:4565`) | Verificada |
| HU-14 | Mapa de calor de incidentes | 5 | 06 | MapaCalor (`168:3652`) | Verificada |
| HU-15 | Exportar reportes a PDF y Excel | 3 | 11 | Dashboard · Excel descargado (`437:31575`) y Dashboard · PDF descargado (`437:31824`) | Verificada |
| HU-16 | Aplicación móvil nativa | — | — | Fuera del alcance del proyecto | No aplica |
| HU-17 | Integración con el sistema PQRSDF | — | — | Fuera del alcance del proyecto | No aplica |

## 6. Limitaciones

- No constituye un despliegue en producción ni una prueba en entorno operativo.
- No incluye persistencia real en una base de datos: el alcance de la fase se
  concentra en el prototipo interactivo.
- La verificación se hizo por inspección de los flujos sobre datos de prueba
  precargados; **no incorporó una muestra de usuarios** y, por tanto, no arroja
  puntuaciones de usabilidad.
- La prueba con usuarios y la aplicación del cuestionario SUS (Brooke, 1996)
  corresponden al TRL 6.

## 7. Cómo reproducir la verificación

1. Abrir el prototipo en el modo Presentar:
   https://www.figma.com/proto/dJxD7bfTBqfYPDgdcoHXF4/Proyecto-GRIU-2.0?page-id=0%3A1&node-id=33-320&viewport=-1917%2C-195%2C0.13&t=XGCxUJrXjoNt6ULH-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=33%3A320
2. Recorrer los escenarios E1 a E5 en el orden en que aparecen en la sección 2.
3. Contrastar cada caso de prueba con la evidencia de la sección 3.
4. Registrar el resultado en la columna correspondiente y conservar la captura de
   pantalla en `evidencias/capturas/`.
