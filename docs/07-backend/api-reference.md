# API REST confirmada

Autenticación requerida significa que la configuración de seguridad debe permitir la ruta solo con JWT; valide el comportamiento al desplegar.

| Método y ruta                                      | Función                          | Requiere JWT de sesión | Controlador                         |
| --------------------------------------------------- | --------------------------------- | ----------------------- | ----------------------------------- |
| POST `/api/users`                                 | Registro                          | No                      | `UserController`                  |
| GET `/api/users/me`                               | Perfil actual                     | Sí                     | `UserController`                  |
| POST `/auth/login`                                | Inicio de sesión                 | No                      | `AuthController`                  |
| POST `/auth/forgot-password`                      | Solicitar recuperación           | No                      | `PasswordResetController`         |
| POST `/auth/reset-password`                       | Restablecer contraseña           | No, con token de reset  | `PasswordResetController`         |
| GET/PUT `/api/accessibility-settings`             | Consultar/actualizar preferencias | Sí                     | `AccessibilitySettingsController` |
| GET/PUT `/api/feature-permissions`                | Consultar/actualizar permisos     | Sí                     | `FeaturePermissionController`     |
| POST `/api/translations`                          | Crear traducción                 | Sí                     | `TranslationController`           |
| POST `/api/translations/with-recording`           | Crear con archivo multipart       | Sí                     | `TranslationController`           |
| GET `/api/translations`                           | Listar historial                  | Sí                     | `TranslationController`           |
| GET `/api/translations/{translationId}/recording` | Obtener grabación                | Sí                     | `TranslationController`           |
| DELETE `/api/translations/{translationId}`        | Eliminar una                      | Sí                     | `TranslationController`           |
| DELETE `/api/translations`                        | Eliminar colección               | Sí                     | `TranslationController`           |

Contratos de entrada confirmados por DTO/controlador:

| Ruta                                      | Entrada confirmada                                                                                                      |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `POST /api/users`                       | JSON: `fullName`, `email`, `password`; devuelve 201.                                                              |
| `POST /auth/login`                      | JSON: `email`, `password`; devuelve `token` y `user` en `AuthResponseDto`.                                    |
| `POST /auth/forgot-password`            | JSON: `email`.                                                                                                        |
| `POST /auth/reset-password`             | JSON: `tokenIdentifier` (UUID), `token`, `newPassword`, `confirmPassword`.                                      |
| `POST /api/translations`                | JSON `CreateTranslationRequestDto`; el cliente envía `translatedText` y `confidence`.                            |
| `POST /api/translations/with-recording` | Multipart: `recording` obligatorio, `translatedText` obligatorio (máx. 2000), `confidence` opcional entre 0 y 1. |

Ejemplo de login: `{"email":"usuario@ejemplo.com","password":"********"}`. Los cuerpos de error y la semántica exacta de todos los códigos requieren prueba de contrato; no se infieren aquí.
