# HU-003: Conocer el propósito de CaliLand

**Como** visitante, **quiero** conocer el propósito de CaliLand **para** saber qué puedo explorar dentro de la web.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-010 | Mostrar una sección "¿Qué es CaliLand?". |
| RF-011 | Explicar que es una experiencia digital introductoria de Huánuco. |
| RF-012 | Indicar que se exploran zonas culturales y turísticas. |

## Diagrama de casos de uso

```mermaid
flowchart LR
    Visitante((Visitante)) --> UC3(Leer sección '¿Qué es CaliLand?')
    
    UC3 -. include .-> UC3_1(Ver explicación de experiencia digital)
    UC3 -. include .-> UC3_2(Conocer zonas culturales y turísticas)
