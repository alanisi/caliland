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
    participant Sistema
    participant API as API/Backend

    Visitante->>Sistema: Navega hacia la sección de información/propósito
    Sistema->>API: Solicita datos del propósito del proyecto
    API-->>Sistema: Devuelve información institucional y descripciones

    loop Renderiza información del propósito
        Sistema-->>Visitante: Muestra el nombre "CaliLand" (RF-001)
        Sistema-->>Visitante: Muestra el slogan "Explorando Huánuco" (RF-002)
        Sistema-->>Visitante: Muestra la sección "¿Qué es CaliLand?" (RF-010)
        Sistema-->>Visitante: Muestra la explicación de experiencia digital introductoria (RF-011)
        Sistema-->>Visitante: Muestra la indicación de exploración de zonas culturales y turísticas (RF-012)
    end
