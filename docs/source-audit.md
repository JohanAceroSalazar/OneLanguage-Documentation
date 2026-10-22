# Auditoría de fuentes

Fecha de auditoría: 22 de octubre de 2026. Las fuentes de Drive se leyeron mediante la conexión autorizada; los repositorios se clonaron temporalmente solo para inspección.

| Fuente | Ubicación / versión | Disponibilidad | Información utilizada | Observaciones |
| --- | --- | --- | --- | --- |
| SRS One Language | Drive, `1Vl47fsrOjjvEH4PZ-lH5G3zFZLaIsceE`, mod. 2026-10-07 | Disponible | Alcance, RF1–RF6, RNF1–RNF10 y casos de uso | Referencia funcional principal. |
| Diseño y análisis | Drive, `1lyAQ…`, `1rXhz…` | Disponible | Flujos y decisiones previstas | Especificación; no prueba de implementación. |
| Pruebas, manuales y despliegue | Drive, `1yE3…`, `1Y2W…`, `1l-Dt…`, `1ntT…` | Disponible | Planes, operación, despliegue VPS/Nginx/Docker documentado y condiciones de entrega | El documento de despliegue aporta registros declarados; no se accedió al servidor para validarlos independientemente. |
| Lista ADSO | Drive, `1dpI5ibemcIRqGG7uRZhScVZpozMKSLGA` | Disponible | Inventario de entregables académicos | No indica por sí sola que el entregable esté terminado. |
| Referencia estructural | project-drivique/Documentation, `main` | Disponible | Organización numerada de documentación | Se usó solo estructura, no contenido funcional. |
| Frontend | `JohanAceroSalazar/OneLanguage_Frontend`, `dev`, `affcbba` | Disponible | Estructura `web/` y `mobile/`, dependencias, pantallas, REST y WebSocket IA | Revisión estática; no se ejecutó cliente. |
| Backend | `JohanAceroSalazar/OneLanguage-Backend`, `dev`, `17eb4c1` | Disponible | Controladores, DTO, seguridad, pruebas y Docker | Revisión estática; no se levantó API. |
| Base de datos | `JohanAceroSalazar/OneLanguage-Database`, `dev`, `6693f13` | Disponible | changelogs, DDL/DML, índices y rollbacks | No se aplicaron migraciones. |
| IA | `Juan282007/OneLanguage-AI`, `develop`, `e1b2034` | Disponible | pipeline, entrenamiento, evaluación y servicio FastAPI/WS | No se hallaron pesos/dataset en el clon inspeccionado. |

## Limitaciones

No se ejecutaron los componentes ni se verificaron credenciales, valores de entorno, precisión del modelo o integración extremo a extremo. Drive contiene documentación y registros declarados de despliegue y pruebas; no se accedió a los ambientes para verificarlos independientemente. Estos puntos deben distinguirse como evidencia documental, no como ejecución de esta auditoría.
