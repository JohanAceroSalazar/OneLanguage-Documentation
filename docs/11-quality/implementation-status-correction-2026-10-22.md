# Corrección del estado de implementación — 2026-10-22

## Motivo

La auditoría inicial empleó una clasificación basada solo en la lectura del código para diferenciarla de la ejecución durante la revisión. Esa redacción podía interpretarse como una interfaz visual sin lógica, lo cual no corresponde a la evidencia de One Language.

## Criterio aplicado

- **Implementado funcionalmente:** existe lógica ejecutable en el componente.
- **Implementado e integrado:** los componentes incluyen la conexión REST, WebSocket, persistencia o servicio correspondiente.
- **Implementado y verificado:** existe evidencia de pruebas o ejecución documentada.
- **Implementado, pendiente de validación en ejecución:** la lógica y la integración existen, pero esta revisión no ejecutó el escenario en el ambiente objetivo.

## Reclasificaciones trazables

| Área | Clasificación corregida | Evidencia |
| --- | --- | --- |
| Registro, login, perfil, permisos e historial | Implementado e integrado | Clientes web/móvil, controladores Spring Boot, servicios y repositorios. |
| Recuperación de contraseña | Implementado e integrado | Clientes, controladores, token de recuperación y servicio de correo; SMTP requiere validación de ambiente. |
| Cámara, reconocimiento y texto | Implementado e integrado, pendiente de validación en ejecución | `getUserMedia`, `expo-camera`, WebSocket `/ws/recognize`, `web_service.py` y manejo de mensajes `prediction`. |
| Audio | Implementado funcionalmente, pendiente de validación en ejecución | `SpeechSynthesis` web y `expo-speech` móvil. |
| Accesibilidad | Implementado e integrado, pendiente de validación en ejecución | API de ajustes, i18n, tema y persistencia local. |
| Docker y despliegue | Implementado y documentado | Dockerfiles/Compose y evidencia de despliegue en Drive; vigencia de infraestructura requiere comprobación directa. |

Esta corrección no afirma pruebas que no se hayan aportado; corrige exclusivamente la clasificación de funcionalidades cuya lógica e integración están presentes en el código auditado.
