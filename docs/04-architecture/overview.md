# Arquitectura general

**IMPLEMENTADO E INTEGRADO:** dos clientes, una API REST Spring Boot, PostgreSQL versionado y un servicio Python FastAPI/WebSocket. Los contratos REST y WebSocket están implementados entre los componentes; la validación de una ejecución conjunta en el ambiente objetivo sigue pendiente.

```mermaid
flowchart TB
  subgraph Clientes
    WEB[Web: React + Vite]
    MOB[Móvil: React Native + Expo]
  end
  API[Backend: Spring Boot]
  DB[(PostgreSQL)]
  AI[IA: FastAPI + WebSocket]
  MODEL[TensorFlow/Keras\nMediaPipe/OpenCV]
  WEB -->|REST + JWT| API
  MOB -->|REST + JWT| API
  API -->|JPA| DB
  WEB -->|WebSocket /ws/recognize| AI
  MOB -->|WebSocket /ws/recognize| AI
  AI --> MODEL
```

La API administra usuarios, autenticación, recuperación de contraseña, accesibilidad, permisos y traducciones. Los clientes implementan el contrato WebSocket `/ws/recognize` contra IA. El servicio carga `model/lsc_sequence_model.keras` y `model/lsc_labels.json`; esos artefactos no están en el clon auditado. La operación conjunta no se ejecutó.
