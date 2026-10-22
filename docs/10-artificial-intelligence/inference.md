# Inferencia

El servicio recibe bytes JPEG por WebSocket en `/ws/recognize`, los decodifica, extrae características y responde JSON `ready`, `prediction` o `error`. El cliente espera estados como `no_hands`, `idle` y `translated`; cuando recibe `translated` usa `text`, `confidence` e `is_new_translation`. Tiene `GET /health` y `GET /model-info`. `web_service.py` y su Compose usan `8000` por defecto. El contrato está **IMPLEMENTADO E INTEGRADO** en ambos clientes; requiere validación en ejecución junto con modelo y red.
