# Actividad práctica DSIT

Herramienta web para la actividad práctica de la Sesión DSIT de la Universidad de los Andes. Cada grupo analiza un requerimiento real que llegó a DSIT y decide con qué nivel deben participar los equipos de **Experiencia**, **Gestión del Cambio** y **Posicionamiento y Comunicaciones**.

La herramienta es un solo archivo HTML, sin dependencias de instalación ni servidor. Usa el sistema de diseño **ID Uniandes**.

## Recorrido

| Paso | Pantalla | Qué hace el grupo |
|---|---|---|
| 1 | Bienvenida | Elige su grupo (uno de los 6 casos). |
| 2 | Caso | Lee el requerimiento tal como llegó e inicia el tiempo. |
| 3 | Preguntas clave | Lee las notas de la conversación con el área y responde 7 preguntas. |
| 4 | Evaluación | Marca la matriz transversal para cada equipo. Si no sabe algo, elige «Aún no lo sabemos» y escribe la pregunta. |
| 5 | Decisión | Ve el nivel de participación de cada equipo (Autogestión, Consultivo o Necesario) y las preguntas para el equipo Transversal. |
| 6 | Presentación | Resume el resultado para la plenaria y lo exporta como imagen PNG. |

Además incluye un tiempo total de 20 minutos con música de concentración y un timbre al terminar. La música y el timbre se generan en el navegador, sin archivos de audio.

## Uso

Abre `index.html` en un navegador moderno (Chrome, Edge, Safari o Firefox). Se usa **un dispositivo por grupo**: el avance se guarda en el navegador de ese dispositivo.

Necesita conexión a internet para cargar las fuentes (Google Fonts) y, al exportar la imagen, la librería [html2canvas](https://html2canvas.hertzen.com/) desde cdnjs.

## Publicar con GitHub Pages

1. En el repositorio, ve a **Settings → Pages**.
2. En **Source**, elige **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`.
3. Guarda. En unos minutos la herramienta queda disponible en `https://mospina19.github.io/actividad-dsit/`.

## Editar el contenido

Todo el contenido está al inicio del bloque `<script>` de `index.html`, separado de la lógica:

| Constante | Contenido |
|---|---|
| `MESAS` | Los 6 casos: título, requerimiento, área, participantes y notas de la conversación. |
| `GUIA` | Las 7 preguntas clave. |
| `MATRIZ` | Los criterios de cada equipo, el puntaje de cada opción, los puntajes de corte y los nombres de los niveles. |
| `OPT_TITLES` | Los títulos cortos de las opciones de la matriz. |

### Puntajes de corte

| Equipo | Autogestión | Consultivo | Necesario |
|---|---|---|---|
| Experiencia | Menos de 24 | 24 a 35 | 36 o más |
| Gestión del Cambio | Menos de 24 | 24 a 35 | 36 o más |
| Posicionamiento y Comunicaciones | 8 a 20 | 21 a 36 | 37 o más |

«Aún no lo sabemos» suma el puntaje más alto del criterio: ante la duda, es mejor involucrar al equipo.

## Versión publicada en Claude

El mismo archivo funciona como artefacto publicado en claude.ai. Ahí, además, los resultados de cada grupo llegan en vivo a la **vista del facilitador** (enlace al final de la Bienvenida) y se pueden descargar en CSV. Fuera de Claude esa vista no aparece.

## Estructura

```
.
├── index.html   # La herramienta completa (HTML, CSS y JavaScript, con el logo incrustado)
└── README.md
```

## Diseño

Sigue el sistema de diseño ID Uniandes: tipografías Source Sans 3 y Source Serif 4, tokens de color, Navbar secundaria, Stepper, Tabs, Chip, Accordion y botones rectos. Íconos de Material Symbols.
