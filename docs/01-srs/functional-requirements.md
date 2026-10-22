# Requisitos funcionales

Los identificadores proceden del SRS. Los estados distinguen la lógica y las conexiones presentes en código de la validación ejecutada durante esta revisión.

| ID | Nombre | Actor / entrada → salida | Estado y evidencia |
| --- | --- | --- | --- |
| RF1.1 | Registrar usuario | Visitante; datos de cuenta → usuario creado | **IMPLEMENTADO E INTEGRADO**: formularios web/móvil consumen `POST /api/users`; `UserController` y servicio crean el usuario. |
| RF1.2 | Iniciar sesión | Usuario; correo y contraseña → JWT/respuesta de autenticación | **IMPLEMENTADO E INTEGRADO**: clientes consumen `POST /auth/login`; `AuthController` devuelve token y usuario. |
| RF1.3 | Recuperar y restablecer contraseña | Usuario; correo/token/contraseña → solicitud o restablecimiento | **IMPLEMENTADO E INTEGRADO**: clientes y API usan `/auth/forgot-password` y `/auth/reset-password`; el envío SMTP requiere validación en el ambiente configurado. |
| RF2.1 | Activar cámara | Usuario; permiso → vista/captura disponible | **IMPLEMENTADO FUNCIONALMENTE, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: web usa `getUserMedia` y móvil `expo-camera`. |
| RF2.2 | Capturar señas | Usuario; frames → secuencia | **IMPLEMENTADO E INTEGRADO, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: web y móvil envían frames al WebSocket `/ws/recognize`. |
| RF2.3 | Reconocer señas soportadas | Servicio IA; secuencia → etiqueta/confianza | **IMPLEMENTADO FUNCIONALMENTE, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: `web_service.py` carga modelo, procesa frames y responde predicciones. Las clases se leen de `model/lsc_labels.json`, no incluido en el clon auditado. |
| RF2.4–RF2.5 | Convertir y mostrar texto | Usuario; etiqueta → texto en interfaz | **IMPLEMENTADO E INTEGRADO, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: ambos clientes procesan `prediction` y muestran `text` con estado `translated`. |
| RF3.1–RF3.3 | Generar, reproducir y repetir audio | Usuario; texto → audio | **IMPLEMENTADO FUNCIONALMENTE, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: móvil usa `expo-speech` y web `SpeechSynthesis`. |
| RF4.1 | Guardar traducción | Usuario autenticado; texto/metadatos → registro | **IMPLEMENTADO E INTEGRADO**: clientes consumen `POST /api/translations` y `with-recording`; backend persiste por servicio/repositorio. |
| RF4.2 | Consultar historial | Usuario autenticado → lista | **IMPLEMENTADO E INTEGRADO**: `GET /api/translations` y pantallas `History` consumen el historial. |
| RF4.3 | Filtrar traducciones por fecha | Usuario; criterio de fecha → resultados filtrados | **PENDIENTE DE IMPLEMENTACIÓN/DECISIÓN**: controladores y pantallas auditados no evidencian un filtro por fecha. |
| RF4.4 | Eliminar traducciones | Usuario; id o colección → eliminación | **IMPLEMENTADO E INTEGRADO**: clientes y API usan `DELETE /api/translations/{translationId}` y `DELETE /api/translations`. |
| RF5.1–RF5.4 | Tamaño, tema, idioma y aplicación de ajustes | Usuario; preferencias → configuración | **IMPLEMENTADO E INTEGRADO, PENDIENTE DE VALIDACIÓN EN EJECUCIÓN**: API `accessibility-settings`, i18n, tema y almacenamiento local están conectados en clientes. |
| RF6.1 | Visualizar perfil | Usuario autenticado → datos básicos | **IMPLEMENTADO E INTEGRADO**: `GET /api/users/me` y pantallas `Profile`/`user_profile`. |
| RF6.2 | Gestionar permisos | Usuario; permiso cámara/audio → estado | **IMPLEMENTADO E INTEGRADO**: `/api/feature-permissions` y servicios cliente. |
| RF6.3 | Cerrar sesión | Usuario → sesión local terminada | **IMPLEMENTADO FUNCIONALMENTE** en servicios de sesión cliente; la revocación de JWT en servidor no forma parte del flujo observado. |

Reglas de negocio transversales: autenticar recursos privados, no reconocer fuera del conjunto entrenado, solicitar permiso antes de cámara y comunicar estados de confianza del reconocimiento. Fuente: SRS y repositorios auditados.
