# Docker y Compose

Se observaron `docker-compose.yml` en backend, base de datos e IA, y Dockerfiles en web, backend e IA. El Compose de base publica `5438:5432` y espera healthcheck; el de IA publica `8000` configurable, monta `model/` como solo lectura y define healthcheck `/health`; el de backend publica `8084` y monta grabaciones. El documento de despliegue describe archivos Compose de producción por componente, no un único Compose presente en las ramas auditadas. La configuración productiva exacta requiere cotejo con el servidor.
