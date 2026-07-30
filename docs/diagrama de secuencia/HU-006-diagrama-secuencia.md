# HU-006: Resumen previo de cada zona

**Como** visitante, **quiero** ver un resumen de cada zona antes de entrar **para** saber qué encontraré.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-005 | Mostrar un botón principal "Explorar mapa". |
| RF-003 | Mostrar una descripción breve del proyecto. |
| RF-004 | Mostrar el imagotipo o isotipo principal. |
| RF-002 | Mostrar el slogan "Explorando Huánuco". |
| RF-001 | Mostrar el nombre CaliLand. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant UI as Interfaz / Mapa (Frontend)
    participant API as Backend (Servidor de Contenidos)

    UI->>UI: Renderiza vista base (RF-001, RF-002, RF-003, RF-004, RF-005)

    Note over Visitante, UI: Previsualización de la zona

    Visitante->>UI: Pasa el cursor o selecciona una zona del mapa
    UI->>API: GET /api/v1/zonas/{id_zona}/resumen
    activate API
    API-->>UI: Devuelve resumen rápido (Título, imagen preliminar, descripción corta)
    deactivate API

    UI->>UI: Despliega tarjeta/tooltip con el resumen previo de la zona
    UI-->>Visitante: Muestra la vista previa para que el visitante decida si ingresar
