# Gestión de riesgos

| Riesgo | Impacto | Mitigación |
| --- | --- | --- |
| Falso reconocimiento | Comunicación equivocada | Umbrales, estado de baja confianza, pruebas con clases soportadas. |
| Mala captura | Resultado inestable | Guía de iluminación/encuadre y detección de manos no visibles. |
| Exposición de datos | Alto | JWT, BCrypt, mínimos privilegios, no registrar tokens/archivos privados. |
| Desalineación SRS-código | Alcance erróneo | Mantener matriz y decidir contradicciones explícitamente. |
| Migración fallida | Pérdida/inconsistencia | Respaldo, Liquibase, rollback y prueba previa. |
