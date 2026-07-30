
### 2️⃣ HU-002: Carga de Tema y Estilos Visuales
*Enfocado en la inyección de hojas de estilo (CSS), fuentes y assets del personaje Chayqui.*

```markdown
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
    participant Browser as Navegador (DOM)
    participant Engine as Motor de Estilos (CSS/UI)
    participant Server as Servidor Assets

    Visitante->>Browser: Carga cualquier pantalla de la web
    Browser->>Server: Solicita CSS Theme y SVG de Chayqui
    Server-->>Browser: Devuelve Design Tokens & Assets

    Engine->>Engine: Inyecta paleta de colores (Rojo, Dorado, Azul, Verde) (RF-006)
    Engine->>Engine: Aplica fuentes (Principal en títulos, Secundaria en cuerpo) (RF-007)
    Engine->>Engine: Normaliza estilos de componentes (Botones, Tarjetas, Íconos) (RF-008)
    
    Browser->>Server: GET /assets/images/chayqui-intro.svg
    Server-->>Browser: Devuelve vector gráfico de Chayqui
    Engine->>Browser: Renderiza animación/mascota "Chayqui" (RF-009)
    Browser-->>Visitante: Presenta la web con la identidad visual completa

---

### 3️⃣ HU-003: Sección Informativa del Propósito
*Enfocado en la carga interactiva o scroll hacia el módulo sobre "¿Qué es CaliLand?".*

```markdown
# HU-003: Conocer el propósito de CaliLand

**Como** visitante, **quiero** conocer el propósito de CaliLand **para** saber qué puedo explorar dentro de la web.

## Requerimientos cubiertos

| RF | Descripción |
| :--- | :--- |
| RF-010 | Mostrar una sección "¿Qué es CaliLand?". |
| RF-011 | Explicar que es una experiencia digital introductoria de Huánuco. |
| RF-012 | Indicar que se exploran zonas culturales y turísticas. |

## Diagrama de secuencia

```mermaid
sequenceDiagram
    actor Visitante
    participant UI as Frontend (Vista Sobre Nosotros)
    participant CMS as API Contenidos

    Visitante->>UI: Selecciona/Navega a la sección "¿Qué es CaliLand?"
    UI->>CMS: GET /api/v1/about/purpose
    CMS-->>UI: Devuelve textos informativos y categorías del proyecto

    UI->>UI: Construye bloque informativo "¿Qué es CaliLand?" (RF-010)
    UI->>UI: Formatea el texto introductorio sobre Huánuco (RF-011)
    UI->>UI: Despliega badges/tarjetas con zonas culturales y turísticas (RF-012)
    
    UI-->>Visitante: Muestra módulo con el propósito del proyecto
