# Guía de despliegue controlado

Orden recomendado por los documentos internos: respaldo → migraciones → API → IA → clientes → prueba de extremo a extremo. El documento de despliegue registra una implementación con VPS, Nginx como proxy, TLS/Certbot y WSS para IA; además recomienda comprobaciones no destructivas como `docker compose ps`, logs, `nginx -t` y consultas HTTP. Antes de publicar, valide JWT, CORS, permisos de cámara, seña soportada, persistencia de historial, logs y rollback. Estado: **despliegue documentado; estado actual no verificado independientemente**.
