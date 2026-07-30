# HU-004: Mapa zonificado de Huánuco

**Como** visitante, **quiero** ver un mapa zonificado de Huánuco **para** elegir qué zona explorar.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-005 | Mostrar un botón principal "Explorar mapa". |
| RF-003 | Mostrar una descripción breve del proyecto. |
| RF-004 | Mostrar el imagotipo o isotipo principal. |
| RF-002 | Mostrar el slogan "Explorando Huánuco". |
| RF-001 | Mostrar el nombre CaliLand. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant Sistema
    participant API as API/Backend

    Visitante->>Sistema: Accede a la pantalla de selección de mapa
    Sistema->>API: Solicita información de la vista principal y mapa zonificado
    API-->>Sistema: Devuelve datos de bienvenida y configuración del mapa

    loop Renderiza elementos visuales de la vista
        Sistema-->>Visitante: Muestra el nombre "CaliLand" (RF-001)
        Sistema-->>Visitante: Muestra el slogan "Explorando Huánuco" (RF-002)
        Sistema-->>Visitante: Muestra la descripción breve del proyecto (RF-003)
        Sistema-->>Visitante: Muestra el imagotipo o isotipo principal (RF-004)
        Sistema-->>Visitante: Habilita el botón principal "Explorar mapa" (RF-005)
    end

    Visitante->>Sistema: Hace clic en "Explorar mapa" (RF-005)
    Sistema-->>Visitante: Despliega el mapa zonificado de Huánuco para su interacción
