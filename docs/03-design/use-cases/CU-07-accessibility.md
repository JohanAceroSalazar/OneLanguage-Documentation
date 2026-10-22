# CU-07 — Configurar accesibilidad

**Actor principal:** usuario autenticado. **Requisito:** RF5. Estado: implementado e integrado; pendiente de validación en ejecución por plataforma.

Flujo: consulta ajustes con `GET /api/accessibility-settings`, modifica preferencias y persiste mediante `PUT`. La interfaz contiene tema e i18n. La persistencia aplicada en todas las plataformas requiere prueba.
