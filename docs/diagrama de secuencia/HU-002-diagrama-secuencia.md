# HU-002: Identidad visual propia de Huánuco

**Como** visitante, **quiero** percibir una identidad visual propia **para** reconocer que la web representa a Huánuco.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-006 | Aplicar la paleta de colores definida: rojo, dorado, azul y verde. |
| RF-007 | Usar tipografía principal para títulos y secundaria para textos. |
| RF-008 | Mantener coherencia visual entre botones, tarjetas, títulos e íconos. |
| RF-009 | Mostrar a Chayqui como elemento visual introductorio. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant Sistema
    participant API as API/Backend

    Visitante->>Sistema: Accede a la interfaz web
    Sistema->>API: Solicita recursos de diseño y elementos visuales
    API-->>Sistema: Devuelve assets (paleta de colores, fuentes, estilos, Chayqui)

    loop Carga y aplica la identidad visual
        Sistema-->>Visitante: Aplica paleta de colores (rojo, dorado, azul, verde) (RF-006)
        Sistema-->>Visitante: Renderiza títulos con tipografía principal y textos con secundaria (RF-007)
        Sistema-->>Visitante: Aplica coherencia visual en botones, tarjetas e íconos (RF-008)
        Sistema-->>Visitante: Muestra personaje/elemento Chayqui como introducción (RF-009)
    end
