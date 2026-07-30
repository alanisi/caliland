# Diagrama de Clases Unificado — HU-001 a HU-006

```mermaid
classDiagram
    %% HU-001: Página de inicio
    class LandingPage {
        -nombre: String
        -slogan: String
        -descripcion: String
        +mostrarInicio()
        +irAlMapa()
    }

    %% HU-002: Identidad visual
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

    %% HU-003: Propósito
    class SeccionProposito {
        -titulo: String
        -contenido: String
        +mostrarInformacion()
    }

    %% HU-004 y HU-005: Mapa y Zonas
    class Mapa {
        -estadoCarga: boolean
        -zonas: Zona[]
        +cargarCapas()
        +renderizarZonas()
    }

    class Zona {
        -id: String
        -nombre: String
        -tipo: String
        -delimitacion: String
        -resumenTexto: String
        -estadoSeleccion: boolean
        +resaltar()
        +seleccionar()
        +obtenerResumen()
    }

    %% HU-005: Contenido
    class ContenidoCultural {
        -titulo: String
        -descripcion: String
        +cargarDatos()
    }

    %% HU-006: Tarjeta Resumen
    class TarjetaResumen {
        -titulo: String
        -resumen: String
        -imagenUrl: String
        +mostrar()
        +ocultar()
    }

    %% RELACIONES UNIFICADAS DEL SISTEMA
    LandingPage "1" --> "1" Mapa : dirige a
    IdentidadVisual "1" -- "1" PersonajeChayqui : define estilo de
    SeccionProposito "1" o-- "1..*" Zona : informa sobre
    Mapa "1" *-- "1..*" Zona : contiene
    Zona "1" --> "1..*" ContenidoCultural : despliega
    Zona "1" -- "1" TarjetaResumen : genera
