# Integración API móvil

`authService.ts` y `translationService.ts` consumen servicios configurados por `src/config/network.ts`; AsyncStorage conserva token, usuario y ajustes locales. La cámara usa `AI_WEBSOCKET_URL` y `/ws/recognize`. El código móvil usa por defecto API `8084` e IA `8001`, mientras el servicio IA auditado arranca en `8000`; configure `EXPO_PUBLIC_AI_WS_URL` para resolver esa discrepancia antes de probar. La conectividad en dispositivo físico sigue pendiente.
