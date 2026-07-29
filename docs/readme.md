# CaliLand — Explorando Huánuco

Plataforma interactiva para la difusión cultural y turística del departamento de Huánuco. Desarrollada como una aplicación web dinámica con arquitectura basada en componentes y persistencia de datos relacional.

## Descripción del Proyecto

CaliLand es una solución digital orientada a centralizar y optimizar el acceso a la información turística de la región Huánuco. A través de un mapa interactivo por provincias, la plataforma permite a los usuarios explorar atractivos arqueológicos, naturales y gastronómicos mediante interfaces dinámicas y rutas sugeridas de viaje. El flujo de usuario cuenta con el acompañamiento visual de Chayqui, la mascota oficial del proyecto, diseñada para guiar la experiencia de navegación.

### Problemática

La dispersión y desactualización de la información turística regional limita el impacto del sector en Huánuco. Este proyecto resuelve la falta de plataformas unificadas ofreciendo un entorno web de alta fidelidad, interactivo y optimizado tanto para dispositivos móviles como de escritorio.

---

## Módulos y Arquitectura (Trabajo Asignado: HU-001 a HU-006)

La documentación técnica y el modelado del sistema correspondientes a las historias de usuario de la 1 a la 6 se estructuran dentro del directorio `/docs` de la siguiente manera:

* **Diagramas de Secuencia (`docs/diagrama de secuencia`)**: Representación del flujo de control, llamadas de métodos y ciclo de vida de los procesos principales correspondientes a las HU asignadas.
* **Diagramas de Casos de Uso (`docs/diagrama casos de uso`)**: Definición de los límites del sistema, interacciones de los actores y los casos de uso del núcleo de la aplicación.
* **Diagrama de Clases (`docs/diagrama de clases`)**: Estructura estática del sistema, detallando las entidades del dominio, atributos y sus relaciones directas.
* **Stack Tecnológico (`docs/stack`)**: Especificación de dependencias y requerimientos de entorno.

---

## Componentes Tecnológicos

La arquitectura de la aplicación está construida sobre las siguientes tecnologías estables de desarrollo:

* **Frontend**: Vue.js 3 en conjunto con Vite para la gestión del entorno de desarrollo y compilación optimizada.
* **Estilos y Maquetación**: Tailwind CSS 3.4 para un diseño basado en clases utilitarias altamente responsivo.
* **Persistencia de Datos**: PostgreSQL 18 para la gestión y almacenamiento relacional de las entidades turísticas, usuarios y rutas.

---

## Configuración del Entorno Local

Para clonar el repositorio y levantar el servidor de desarrollo localmente, ejecute las siguientes instrucciones en la terminal:

```bash
# Clonar el proyecto
git clone https://github.com

# Acceder al directorio
cd caliland

# Instalar dependencias del package.json
npm install

# Inicializar servidor local
npm run dev
```
