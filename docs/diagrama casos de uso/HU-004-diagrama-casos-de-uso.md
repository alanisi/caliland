# HU-004: Mapa zonificado de Huánuco

**Como** visitante, **quiero** ver un mapa zonificado de Huánuco **para** elegir qué zona explorar.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-005 | Mostrar un botón principal "Explorar mapa". |
| RF-018 | Delimitar las zonas en el mapa interactivo. |

## Diagrama de casos de uso

```mermaid
flowchart LR
    Visitante((Visitante)) --> UC4(Ver mapa zonificado)
    
    UC4 -. include .-> UC4_1(Visualizar delimitación de zonas)
    UC4 -. extend .-> UC4_2(Presionar botón 'Explorar mapa')
