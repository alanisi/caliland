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
    Visitante((Visitante)) --> UC2(Reconocer marca Huánuco)
    
    UC2 -. include .-> UC2_A(Cargar paleta institucional - Rojo, Dorado, Azul, Verde)
    UC2 -. include .-> UC2_B(Aplicar jerarquía tipográfica)
    UC2 -. include .-> UC2_C(Estilizar componentes visuales - Tarjetas y Botones)
    UC2 -. extend .-> UC2_D(Desplegar presentación con mascota Chayqui)
