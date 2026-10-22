# Requisitos no funcionales

| ID | Requisito SRS | Evidencia / estado |
| --- | --- | --- |
| RNF1 | Rendimiento | **ESPECIFICADO**; no hay métricas de rendimiento aportadas en esta revisión. |
| RNF2 | Usabilidad | **IMPLEMENTADO FUNCIONALMENTE**: navegación, textos, tema, idioma y pantallas de accesibilidad. La evaluación con usuarios queda pendiente de validación. |
| RNF3 | Compatibilidad | **IMPLEMENTADO FUNCIONALMENTE**: web Vite y Expo con objetivos Android, iOS y web declarados. La matriz de dispositivos queda pendiente de validación. |
| RNF4 | Seguridad | **IMPLEMENTADO FUNCIONALMENTE**: Spring Security, JWT, BCrypt y rutas protegidas. La auditoría de seguridad queda pendiente. |
| RNF5 | Escalabilidad | **ESPECIFICADO**; faltan pruebas de carga y métricas de capacidad. |
| RNF6 | Mantenibilidad | **IMPLEMENTADO FUNCIONALMENTE**: módulos, pruebas backend y changelogs versionados; falta reporte de cobertura ejecutado. |
| RNF7 | Manejo de errores | **IMPLEMENTADO FUNCIONALMENTE**: `GlobalExceptionHandler` y manejo de errores en clientes; falta validación de escenarios completos. |
| RNF8 | Reconocimiento de señas | **IMPLEMENTADO FUNCIONALMENTE** mediante pipeline y modelo; las clases exactas requieren el artefacto de etiquetas. |
| RNF9 | Tiempo de respuesta | **ESPECIFICADO**; faltan mediciones reproducibles. |
| RNF10 | Eficiencia de recursos | **ESPECIFICADO**; Docker IA declara operación en CPU, sin benchmark publicado. |
