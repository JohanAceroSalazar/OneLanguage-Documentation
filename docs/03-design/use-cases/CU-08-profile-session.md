# CU-08 — Consultar perfil, permisos y cerrar sesión

**Actor principal:** usuario autenticado. **Requisito:** RF6. Estado: implementado e integrado.

Flujo: consulta `GET /api/users/me`, revisa/actualiza permisos en `/api/feature-permissions` y cierra sesión desde el cliente. No se comprobó invalidación de JWT en servidor.
