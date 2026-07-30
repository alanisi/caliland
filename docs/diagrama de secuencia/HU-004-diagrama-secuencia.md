# HU-004: Mapa zonificado de Huánuco

**Como** visitante, **quiero** ver un mapa zonificado de Huánuco **para** elegir qué zona explorar.

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
    participant UI as Interfaz (Frontend)
    participant API as Servidor API / Mapas

    Visitante->>UI: Accede al módulo del mapa de Huánuco
    UI->>API: GET /api/v1/mapa/zonas-huanuco
    activate API
    API-->>UI: Devuelve coordenadas, polígonos y datos de zonificación
    deactivate API

    UI->>UI: Carga componentes de marca (RF-001, RF-002, RF-004)
    UI->>UI: Renderiza la descripción del proyecto (RF-003)
    UI->>UI: Procesa capas vectoriales y dibuja el mapa zonificado de Huánuco
    UI->>UI: Habilita el botón interactivo "Explorar mapa" (RF-005)

    UI-->>Visitante: Muestra la vista con el mapa zonificado listo para interactuar
