# HU-005: Seleccionar una zona del mapa

**Como** visitante, **quiero** seleccionar una zona del mapa **para** acceder a su información cultural y turística.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-018 | Al pasar el mouse o tocar una zona, esta debe resaltarse visualmente. |
| RF-003 | Mostrar una descripción breve del proyecto. |
| RF-004 | Mostrar el imagotipo o isotipo principal. |
| RF-002 | Mostrar el slogan "Explorando Huánuco". |
| RF-001 | Mostrar el nombre CaliLand. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant UI as Mapa Interactivo (DOM)
    participant API as Backend (Datos Turísticos)

    UI->>UI: Carga componentes globales (RF-001, RF-002, RF-003, RF-004)

    Note over Visitante, UI: Interacción sobre las zonas del mapa

    Visitante->>UI: Pasa el cursor (hover) o toca una zona específica
    UI->>UI: Captura evento de interacción y resalta la zona visualmente (RF-018)
    UI-->>Visitante: Muestra feedback visual inmediato (resalte de zona)

    Visitante->>UI: Hace clic o selecciona la zona resaltada
    UI->>API: GET /api/v1/zonas/{id_zona}/contenido
    activate API
    API-->>UI: Retorna datos turísticos y culturales de la zona
    deactivate API

    UI-->>Visitante: Despliega el panel con la información cultural y turística
