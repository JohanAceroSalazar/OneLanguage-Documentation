# Diagnóstico

| Síntoma | Comprobación segura |
| --- | --- |
| API no inicia | Revise conectividad PostgreSQL, changelog, variables y logs sin copiar secretos. |
| Servicio no expuesto por HTTPS/WSS | Revise Nginx y certificados con `nginx -t`; el documento de despliegue ubica API e IA detrás del proxy, no expuestos directamente. |
| No hay reconocimiento | Verifique cámara, permiso, modelo y `lsc_labels.json`, CORS/URL WebSocket y clase soportada. |
| Móvil no conecta a IA | Verifique `EXPO_PUBLIC_AI_WS_URL`: el código móvil usa `8001` por defecto y el Compose IA publica `8000` por defecto. |
| Resultado inestable | Revise iluminación, manos visibles, encuadre y umbrales; no fuerce una etiqueta. |
| Recuperación falla | Revise configuración de correo y token temporal sin exponerlos. |
