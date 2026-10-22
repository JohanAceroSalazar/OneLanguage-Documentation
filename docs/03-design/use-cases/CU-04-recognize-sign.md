# CU-04 — Reconocer seña soportada

**Actor principal:** usuario. **Requisito:** RF2.1–RF2.5. **Estado:** IMPLEMENTADO E INTEGRADO.

Precondiciones: cámara disponible, permiso concedido, modelo y etiquetas montados. Flujo: 1) abre cámara; 2) captura frames; 3) web y móvil envían JPEG al WebSocket `/ws/recognize`; 4) el servicio preprocesa y clasifica; 5) devuelve etiqueta/confianza; 6) cliente muestra texto cuando recibe `translated`. Alternos: permiso denegado, manos no visibles, confianza insuficiente, modelo ausente o seña no entrenada. Postcondición: el resultado se muestra solo si se cumplen umbrales del servicio. El flujo se deriva de código, pero no se ejecutó en la auditoría.
