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

    LandingPage "1" --> "1" Mapa : dirige a
    LandingPage "1" --> "1" IdentidadVisual : aplica
    LandingPage "1" *-- "1" PersonajeChayqui : muestra a
