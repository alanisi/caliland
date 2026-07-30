# HU-001: Página de inicio atractiva de CaliLand

**Como** visitante, **quiero** ver una página de inicio atractiva **para** entender rápidamente qué es CaliLand y poder explorar el mapa.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-001 | Mostrar el nombre CaliLand. |
| RF-002 | Mostrar el slogan "Explorando Huánuco". |
| RF-003 | Mostrar una descripción breve del proyecto. |
| RF-004 | Mostrar el imagotipo o isotipo principal. |
| RF-005 | Mostrar un botón principal "Explorar mapa". |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant UI as Frontend (CaliLand)
    participant API as Backend/API

    Visitante->>UI: Solicita ingresar a la web
    UI->>API: GET /api/v1/config/landing
    activate API
    API-->>UI: Retorna datos de presentación (Marca, Slogan, Logo)
    deactivate API

    UI->>UI: Renderiza Header (RF-001, RF-002, RF-004)
    UI->>UI: Renderiza sección de bienvenida (RF-003)
    UI->>UI: Habilita el botón CTA "Explorar mapa" (RF-005)
    UI-->>Visitante: Muestra la pantalla principal lista

    Visitante->>UI: Hace clic en "Explorar mapa" (RF-005)
    UI-->>Visitante: Redirige a la sección del mapa
