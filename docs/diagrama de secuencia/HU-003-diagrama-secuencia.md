# HU-003: Conocer el propósito de CaliLand

**Como** visitante, **quiero** conocer el propósito de CaliLand **para** saber qué puedo explorar dentro de la web.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-010 | Mostrar una sección "¿Qué es CaliLand?". |
| RF-011 | Explicar que es una experiencia digital introductoria de Huánuco. |
| RF-012 | Indicar que se exploran zonas culturales y turísticas. |
| RF-002 | Mostrar el slogan "Explorando Huánuco". |
| RF-001 | Mostrar el nombre CaliLand. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant UI as Interfaz (Frontend)
    participant API as API / Servidor de Contenido

    Visitante->>UI: Navega hacia la sección de propósito / información
    UI->>API: GET /api/v1/propósito-caliland
    activate API
    API-->>UI: Devuelve textos institucionales y lista de zonas
    deactivate API

    UI->>UI: Renderiza sección "¿Qué es CaliLand?" (RF-010)
    UI->>UI: Muestra la explicación de experiencia introductoria (RF-011)
    UI->>UI: Despliega información sobre zonas culturales y turísticas (RF-012)
    UI->>UI: Muestra el nombre "CaliLand" (RF-001) y slogan "Explorando Huánuco" (RF-002)

    UI-->>Visitante: Presenta la sección de propósito completamente cargada
