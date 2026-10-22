# CU-06 — Gestionar historial

**Actor principal:** usuario autenticado. **Requisito:** RF4. Estado: RF4.1, RF4.2 y RF4.4 implementados e integrados; RF4.3 pendiente de implementación o decisión.

Flujo: guardar mediante `POST /api/translations`, consultar con `GET /api/translations` y eliminar una o todas con `DELETE`. Alterno: token ausente o recurso ajeno debe rechazarse conforme a seguridad. El filtro por fecha del SRS requiere verificación adicional.
