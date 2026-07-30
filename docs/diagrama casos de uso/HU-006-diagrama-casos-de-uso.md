# HU-006: Resumen de cada zona

**Como** visitante, **quiero** ver un resumen de cada zona antes de entrar **para** saber qué encontraré.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-003 | Mostrar una descripción breve del proyecto/zona. |
| RF-005 | Permitir la vista previa en tarjeta flotante o tooltip. |

## Diagrama de casos de uso

```mermaid
flowchart LR
    Visitante((Visitante)) --> UC6(Previsualizar zona)
    
    UC6 -. include .-> UC6_1(Ver tarjeta de resumen rápido)
    UC6 -. extend .-> UC6_2(Confirmar e ingresar a la zona)
