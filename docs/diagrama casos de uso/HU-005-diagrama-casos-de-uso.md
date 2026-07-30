# HU-005: Seleccionar una zona del mapa

**Como** visitante, **quiero** seleccionar una zona del mapa **para** acceder a su información cultural y turística.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-018 | Al pasar el mouse o tocar una zona, esta debe resaltarse visualmente. |
| RF-003 | Mostrar información detallada de la zona elegida. |

## Diagrama de casos de uso

```mermaid
flowchart LR
    Visitante((Visitante)) --> UC5(Seleccionar zona del mapa)
    
    UC5 -. include .-> UC5_1(Ver resalte visual al pasar el cursor)
    UC5 -. extend .-> UC5_2(Cargar contenido turístico de la zona)
