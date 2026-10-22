# ADR-001 — Separación por componentes

**Estado:** constatado en repositorios. Se mantienen clientes web/móvil, API Java, esquema PostgreSQL y componente IA Python en repositorios independientes. Esto permite evolución específica de cada frente, pero exige contratos versionados y pruebas de integración; estos últimos son pendientes documentados.
