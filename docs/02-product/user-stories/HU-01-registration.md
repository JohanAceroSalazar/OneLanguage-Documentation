# HU-01 — Registro

Como visitante, quiero registrar una cuenta para acceder a funcionalidades protegidas.

- Requisito: RF1.1. Prioridad: alta. Estado: **IMPLEMENTADO E INTEGRADO**.
- Precondición: correo no registrado y datos válidos.
- Aceptación: dado un formulario válido, cuando se envía, entonces la API crea el usuario; dado un correo existente, entonces responde con error controlado.
- Evidencia: `UserController`, `UserServiceImplTest`.
