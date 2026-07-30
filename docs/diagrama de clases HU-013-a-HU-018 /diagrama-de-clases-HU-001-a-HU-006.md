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
classDiagram
    class IdentidadVisual {
        -colores: String[]
        -tipografia: String
        +aplicarEstilos()
    }
    class PersonajeChayqui {
        -nombre: String
        -mensajeBienvenida: String
        +mostrarPresentacion()
    }

    IdentidadVisual "1" -- "1" PersonajeChayqui : define estilo de
classDiagram
    class SeccionProposito {
        -titulo: String
        -contenido: String
        +mostrarInformacion()
    }
    class Zona {
        -nombre: String
        -tipo: String
    }

    SeccionProposito "1" o-- "1..*" Zona : informa sobre
classDiagram
    class Mapa {
        -zonas: Zona[]
        +renderizarZonas()
    }
    class Zona {
        -nombre: String
        -delimitacion: String
        +resaltar()
    }

    Mapa "1" *-- "1..*" Zona : contiene
classDiagram
    class Zona {
        -id: String
        -nombre: String
        -estadoSeleccion: boolean
        +resaltar()
        +seleccionar()
    }
    class ContenidoCultural {
        -titulo: String
        -descripcion: String
        +cargarDatos()
    }

    Zona "1" --> "1..*" ContenidoCultural : despliega
classDiagram
    class TarjetaResumen {
        -titulo: String
        -resumen: String
        -imagenUrl: String
        +mostrar()
        +ocultar()
    }
    class Zona {
        -nombre: String
        -resumenTexto: String
        +obtenerResumen()
    }

    Zona "1" -- "1" TarjetaResumen : genera
