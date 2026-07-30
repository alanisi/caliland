# HU-002: Identidad visual propia de Huánuco

**Como** visitante, **quiero** percibir una identidad visual propia **para** reconocer que la web representa a Huánuco.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-006 | Aplicar la paleta de colores definida: rojo, dorado, azul y verde. |
| RF-007 | Usar tipografía principal para títulos y secundaria para textos. |
| RF-008 | Mantener coherencia visual entre botones, tarjetas, títulos e íconos. |
| RF-009 | Mostrar a Chayqui como elemento visual introductorio. |

## Diagrama de casos de uso

```mermaid
flowchart LR
    Visitante((Visitante)) --> UC2(Percibir identidad visual)
    
    UC2 -. include .-> UC2_1(Apreciar paleta de colores huanuqueña)
    UC2 -. include .-> UC2_2(Visualizar tipografía principal y secundaria)
    UC2 -. include .-> UC2_3(Ver coherencia en botones, tarjetas e íconos)
    UC2 -. extend .-> UC2_4(Interactuar con personaje Chayqui)
