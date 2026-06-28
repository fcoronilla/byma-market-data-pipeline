# Pipeline architecture

El pipeline sigue una arquitectura Lakehouse simple basada en tres capas: Bronze, Silver y Gold.

## Flujo general

```mermaid
flowchart TD
    A[CSV operaciones BYMA] --> B[Bronze]
    B --> C[Silver]
    C --> D[Gold]
    D --> E[Consultas SQL / Analytics]