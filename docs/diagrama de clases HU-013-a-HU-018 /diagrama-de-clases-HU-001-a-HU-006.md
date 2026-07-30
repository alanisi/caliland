# Diagramas de Clases — HU-001 a HU-006

---

## HU-001: Página de inicio atractiva de CaliLand

```mermaid
classDiagram
    class LandingPage {
        -nombre: String
        -slogan: String
        -descripcion: String
        +mostrarInicio()
        +irAlMapa()
    }
    class Mapa {
        -estadoCarga: boolean
        +cargarCapas()
    }

    LandingPage "1" --> "1" Mapa : dirige a
