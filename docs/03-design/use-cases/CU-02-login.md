# CU-02 — Iniciar sesión

**Actor principal:** usuario. **Requisito:** RF1.2. **Estado:** IMPLEMENTADO E INTEGRADO.

Flujo: 1) introduce credenciales; 2) cliente invoca `POST /auth/login`; 3) API valida; 4) genera respuesta de autenticación; 5) cliente conserva la sesión según su servicio local. Excepción: credenciales incorrectas generan fallo de login. Postcondición: el usuario puede llamar recursos protegidos con JWT. Referencias: `AuthController`, `JwtAuthenticationFilter`.
