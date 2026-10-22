# HU-02 — Inicio de sesión

Como usuario registrado, quiero iniciar sesión para acceder a mi información y recursos protegidos.

- Requisito: RF1.2. Prioridad: alta. Estado: **IMPLEMENTADO E INTEGRADO**.
- Aceptación: dado credenciales válidas, cuando inicio sesión, entonces recibo la respuesta de autenticación; con credenciales inválidas, recibo un error sin revelar la contraseña.
- Evidencia: `AuthController`, `AuthServiceImpleTest`.
