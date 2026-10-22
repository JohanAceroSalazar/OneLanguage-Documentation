# Instalación por componente

1. Base de datos: use `OneLanguage-Database/docker-compose.yml`, su `.env.example` y `changelog-master.yaml`; PostgreSQL se expone en host `5438` y Liquibase espera su healthcheck. Revise primero los rollbacks.
2. Backend: configure variables desde `.env.example`, apunte a PostgreSQL y ejecute Maven o su contenedor. El Compose publicado expone `8084` y requiere datasource, JWT y SMTP.
3. IA: instale `requirements.txt`, monte `model/` con pesos y etiquetas compatibles, y arranque `web_service.py`/Docker. El servicio y Compose IA usan por defecto `8000`, con healthcheck en `/health` y WebSocket `/ws/recognize`.
4. Web: en `web/`, instale dependencias y ejecute `npm run dev` o `npm run build`; configure `VITE_API_URL` y `VITE_AI_WS_URL` según ambiente.
5. Móvil: en `mobile/`, instale dependencias y ejecute `npm start`; configure `EXPO_PUBLIC_API_URL`/`EXPO_PUBLIC_AI_WS_URL`. Su valor por defecto de IA es `8001`, distinto del servicio IA (`8000`), por lo que exige configuración explícita o alineación de puertos.

Los puertos y variables citados provienen de la configuración implementada. La ejecución conjunta y la conectividad real requieren validación en el ambiente objetivo.
