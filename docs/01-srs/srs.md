# SRS — One Language

## Propósito y alcance

One Language ofrece interfaces web y móvil para capturar señas mediante cámara, reconocer solo clases previamente entrenadas, presentar texto y permitir audio. Incluye registro, sesión, recuperación de contraseña, perfil, historial, permisos y accesibilidad. El SRS define el alcance y el código evidencia integración REST/WebSocket entre clientes, API e IA; su validación conjunta en el ambiente objetivo queda pendiente.

## Fuera de alcance

- Reconocimiento total de la LSC, conversaciones continuas o precisión garantizada al 100 %.
- Sustitución de intérpretes profesionales.
- Traducción avanzada bidireccional con avatar/animación 3D.
- Cambio de contraseña, el SRS limita el alcance a recuperación y restablecimiento.

## Actores

| Actor               | Interacción                                                                        |
| ------------------- | ----------------------------------------------------------------------------------- |
| Usuario             | Se registra, se autentica, configura accesibilidad, usa reconocimiento e historial. |
| Servicio de correo  | Envía el mecanismo de recuperación cuando la configuración esté disponible.     |
| Cámara/dispositivo | Proporciona imágenes con autorización del usuario.                                |
| Servicio IA         | Procesa secuencias para las clases del modelo.                                      |

Las restricciones principales son conexión para servicios remotos, cámara funcional con permiso, calidad de captura y conjunto cerrado de señas. Fuente: SRS vigente; vea [audit](../source-audit.md).
