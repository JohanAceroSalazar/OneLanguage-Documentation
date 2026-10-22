# Entornos

Se reconoce desarrollo local y un despliegue productivo documentado en `Despliegue OneLanguage.docx`: VPS Hostinger con Nginx como proxy inverso, HTTPS/WSS, web hacia puerto local `8080`, backend en `127.0.0.1:8084`, IA en `127.0.0.1:8000` y PostgreSQL privado en red Docker. El documento registra `GET /health` de IA con HTTP 200 y uso de Compose. La vigencia actual de dominio, certificados, contenedores y configuración requiere validación directa en VPS. No se encontró evidencia de CI/CD ni de un ambiente QA.
