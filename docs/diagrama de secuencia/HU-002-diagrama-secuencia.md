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
    participant DOM as Navegador (DOM)
    participant Engine as Motor de Estilos (CSS)
    participant Assets as Servidor de Recursos

    Visitante->>DOM: Carga la página del proyecto
    DOM->>Assets: Solicita hoja de estilos y recursos gráficos
    Assets-->>DOM: Devuelve fuentes, colores y gráficos vectoriales

    Engine->>Engine: Inyecta paleta de colores (rojo, dorado, azul, verde) (RF-006)
    Engine->>Engine: Aplica fuente principal a títulos y secundaria a textos (RF-007)
    Engine->>Engine: Aplica diseño coherente a botones, tarjetas e íconos (RF-008)
    
    DOM->>Assets: GET /assets/images/chayqui-intro.svg
    Assets-->>DOM: Retorna imagen/vector de Chayqui
    Engine->>DOM: Renderiza a Chayqui como elemento introductorio (RF-009)
    
    DOM-->>Visitante: Muestra la interfaz con la identidad visual completa
