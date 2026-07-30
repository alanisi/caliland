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
    participant Sistema
    participant API as API/Backend

    Visitante->>Sistema: Ingresa a la página de inicio
    Sistema->>API: Solicita datos de bienvenida (nombre, slogan, imagotipo, descripción)
    API-->>Sistema: Devuelve datos de bienvenida

    loop Renderiza elementos de bienvenida
        Sistema-->>Visitante: Muestra nombre "CaliLand" (RF-001)
        Sistema-->>Visitante: Muestra slogan "Explorando Huánuco" (RF-002)
        Sistema-->>Visitante: Muestra descripción breve del proyecto (RF-003)
        Sistema-->>Visitante: Muestra imagotipo o isotipo principal (RF-004)
        Sistema-->>Visitante: Muestra botón "Explorar mapa" (RF-005)
    end

    Visitante->>Sistema: Toca "Explorar mapa"
    Sistema-->>Visitante: Redirige a la vista del mapa
```

