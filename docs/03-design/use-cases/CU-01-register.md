# CU-01 — Registrar usuario

**Actor principal:** visitante. **Requisito:** RF1.1. **Estado:** IMPLEMENTADO E INTEGRADO.

Disparador: el visitante envía el formulario. Precondición: datos requeridos válidos. Flujo: 1) captura datos; 2) el cliente los envía a `POST /api/users`; 3) API valida; 4) crea la cuenta y responde. Alterno: correo existente o datos inválidos devuelve error manejado. Postcondición: cuenta creada solo si la operación finaliza correctamente. Referencias: `UserController`, `UserRequestDto`.
