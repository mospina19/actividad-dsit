# Actividad práctica DSIT

Herramienta web de un solo archivo (`index.html`: HTML, CSS y JavaScript) para la actividad práctica de la Sesión DSIT de la Universidad de los Andes. Se publica con GitHub Pages desde la rama `main`, carpeta raíz: https://mospina19.github.io/actividad-dsit/

## Flujo de trabajo

- Todos los cambios se hacen en `index.html`. No agregues archivos ni dependencias de instalación.
- Al terminar un cambio: revisa que el JavaScript no tenga errores, haz commit en español con un mensaje claro y haz `git push` a `main`. GitHub Pages publica solo.
- Si el cambio afecta algo descrito en `README.md` (recorrido, niveles, puntajes, estructura), actualízalo en el mismo commit.
- El mismo archivo también se publica como artefacto en claude.ai. Ahí existe `window.claude` (base de datos en vivo para la vista del facilitador y descargas). Fuera de Claude esas funciones no existen y el código debe seguir funcionando sin ellas.

## Dónde está el contenido

Al inicio del `<script>`, separado de la lógica:

- `MESAS`: los 6 casos (título, requerimiento, área, participantes, notas).
- `GUIA`: las 7 preguntas clave, siempre redactadas en «ustedes».
- `MATRIZ`: criterios, puntajes, puntajes de corte y niveles de cada equipo.
- `OPT_TITLES`: títulos cortos de las opciones de la matriz.

## Reglas de contenido

- Equipos: **Experiencia**, **Gestión del Cambio** y **Posicionamiento y Comunicaciones**.
- Niveles para los tres equipos: **Autogestión**, **Consultivo** y **Necesario**.
- La herramienta le habla al grupo en «ustedes» («Elijan», «Escriban»).
- Se dice «grupo» al elegir y «Caso N» en la barra superior y la presentación.
- Las preguntas de la evaluación y de la decisión son para el «equipo Transversal» o «el equipo de [nombre]».
- En la evaluación no se muestran puntos: cada opción tiene un título corto y una descripción. El puntaje solo se usa por dentro para calcular el nivel.

## Diseño: sistema ID Uniandes

- Tipografías Source Sans 3 (interfaz) y Source Serif 4 (cifras, niveles, citas). Íconos de Material Symbols.
- Colores solo desde los tokens definidos en `:root`, con modo oscuro. El amarillo (`--yellow`) nunca se usa en textos; solo en el hover de botones primarios, separadores y la barra de avance del tiempo.
- Esquinas rectas en botones, campos y tarjetas. Los chips son redondeados.
- Componentes en uso: Navbar secundaria (56 px, fondo `brand-black`, logo SVG incrustado), Stepper de 6 pasos siempre visible bajo la barra (compacto en celular), Tabs para los equipos en la evaluación, Chip para niveles y para «Su grupo», Accordion para «¿Qué significa cada nivel?», botones primario, secundario y terciario.
- No redibujes el logo: usa el SVG que ya está en el encabezado.

## Pruebas

Antes de hacer push, recorre los 6 pasos en un navegador (también en ancho de celular, 360 px): elegir grupo, iniciar el tiempo, responder preguntas clave, marcar la evaluación con al menos un «Aún no lo sabemos», revisar la decisión y exportar la presentación como PNG.
