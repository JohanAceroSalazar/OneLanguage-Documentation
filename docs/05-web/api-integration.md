# Integración API web

`src/services/api.js`, `authService.js`, `translationService.js`, `featurePermissionService.js` y `accessibilityService.js` separan el consumo. El JWT se gestiona mediante `authSession.js`. La URL efectiva de entorno y el contrato WebSocket con IA deben verificarse al ejecutar; no se publican valores `.env`.
