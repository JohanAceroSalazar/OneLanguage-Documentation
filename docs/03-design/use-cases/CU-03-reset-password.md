# CU-03 — Restablecer contraseña

**Actor principal:** usuario. **Requisito:** RF1.3. **Estado:** IMPLEMENTADO E INTEGRADO; envío SMTP pendiente de validación en ejecución.

Flujo: 1) solicita recuperación con correo; 2) API procesa `POST /auth/forgot-password`; 3) recibe token por el mecanismo configurado; 4) presenta token y nueva contraseña a `POST /auth/reset-password`; 5) API valida y actualiza. Excepción: token inválido o vencido. La entrega de correo no fue ejecutada durante la auditoría.
