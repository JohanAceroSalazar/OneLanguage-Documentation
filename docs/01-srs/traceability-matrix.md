# Matriz de trazabilidad

| Requisito | Historia | Caso de uso | Componente | Prueba / evidencia | Estado |
| --- | --- | --- | --- | --- | --- |
| RF1.1 | HU-01 | CU-01 | API usuarios, web/móvil registro | `UserController`, clientes y `UserServiceImplTest` | Implementado e integrado |
| RF1.2 | HU-02 | CU-02 | Auth/JWT, login | `AuthController`, clientes, `AuthServiceImpleTest`, `JwtAuthenticationFilterTest` | Implementado e integrado |
| RF1.3 | HU-03 | CU-03 | Password reset, correo | Controladores, clientes y `PasswordResetServiceImplTest` | Implementado e integrado; SMTP pendiente de validación |
| RF2.1–RF2.5 | HU-04 | CU-04 | Cámara, IA, `Translate`/`camera` | WebSocket `/ws/recognize`, `web_service.py`, `expo-camera` | Implementado e integrado; pendiente de validación en ejecución |
| RF3.1–RF3.3 | HU-05 | CU-05 | `expo-speech` / `SpeechSynthesis` | Llamadas de cliente | Implementado funcionalmente; pendiente de validación en ejecución |
| RF4.1–RF4.2, RF4.4 | HU-06 | CU-06 | `TranslationController`, History | Clientes, controladores y repositorio | Implementado e integrado |
| RF4.3 | HU-06 | CU-06 | Historial | SRS; sin filtro observado en controlador/UI | Pendiente de implementación o decisión |
| RF5.1–RF5.4 | HU-07 | CU-07 | Ajustes de accesibilidad | API, i18n, tema, almacenamiento y `AccessibilitySettingsServiceTest` | Implementado e integrado; pendiente de validación en ejecución |
| RF6.1–RF6.3 | HU-08 | CU-08 | Perfil, permisos y sesión | Controladores, clientes y `FeaturePermissionServiceTest` | Implementado e integrado |
