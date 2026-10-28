# proyecto-web-ia

Explorador interactivo de personajes del universo de **Rick and Morty**, creado con HTML, CSS y JavaScript. La información se obtiene en tiempo real desde [The Rick and Morty API](https://rickandmortyapi.com/documentation).

## Aplicación

- Repositorio: https://github.com/Jand1517/proyecto-web-ia
- GitHub Pages: se añadirá aquí cuando termine el despliegue.

## Funciones

- Consulta la API con fetch() y presenta 20 personajes por página con retrato, estado, especie, género, episodios y origen.
- Busca por nombre y filtra los resultados por estado o especie.
- Ordena alfabéticamente de A a Z o de Z a A. También permite ver primero los registros recientes.
- Guarda favoritos en localStorage y permite mostrar solo los favoritos.
- Muestra el estado de carga y mensajes cuando no hay coincidencias o falla la conexión.
- Adapta la cuadrícula a pantallas de escritorio y celulares. Las estadísticas se actualizan al cambiar los resultados.

## Archivos

- index.html: estructura y controles de la página.
- style.css: colores, tarjetas y diseño adaptable.
- script.js: consulta, filtros, orden, paginación y favoritos.

## Uso

Abre index.html en un navegador con conexión a internet. La aplicación no necesita servidor propio: consulta la API pública directamente. También estará disponible mediante el enlace de GitHub Pages cuando se active la publicación.

1. Escribe un nombre y pulsa **Buscar**.
2. Usa los menús de estado, especie u orden para afinar los resultados.
3. Pulsa el corazón para guardar o quitar un favorito; los favoritos permanecen en ese navegador.
4. Pulsa **Explorar más personajes** para consultar la página siguiente de la API.

## Uso de IA y aprendizaje

Prompts importantes usados durante el desarrollo (resumidos):

1. «Lee las indicaciones del PDF y prepara una aplicación que cumpla sus requisitos usando GitHub web».
2. «Diseña un explorador adaptable con búsqueda, filtros, favoritos persistentes y datos reales de Rick and Morty API».
3. «Revisa el caso en que la API no encuentra resultados y muestra un mensaje claro al usuario».

**Respuesta que requirió corrección:** la primera versión trataba el HTTP 404 como una lista vacía, pero el indicador de carga impedía mostrar el estado vacío. Se cambió la rama 404 para limpiar los resultados y presentar «No se encontraron personajes» explícitamente.

**Error encontrado y solución:** la API responde 404 cuando la búsqueda no tiene coincidencias. Ahora esa respuesta se maneja aparte de los errores de red/servidor, con un mensaje útil; las demás fallas también muestran una indicación para reintentar.

**Modificación adicional:** se agregaron opciones para ordenar por nombre ascendente y descendente. JavaScript aplica localeCompare con configuración en español a los personajes cargados. También se incluyeron estadísticas dinámicas de resultados, favoritos y página.

**Reflexión para que el equipo revise y personalice:** la IA ayudó a estructurar una primera versión y a explicar la lógica, pero fue necesario revisar el comportamiento y corregir el estado vacío. El proyecto permitió practicar cómo fetch() obtiene JSON, cómo el DOM presenta resultados y cómo localStorage conserva datos entre visitas. Cada integrante debe añadir su propia experiencia antes de entregar.

## Equipo y contribuciones

- Jossemyr Andrey Canul Poot (@Jand1517): cuenta identificada en este repositorio y en sus commits actuales.
- Integrantes adicionales: añadir sus nombres y usuarios de GitHub, junto con sus contribuciones reales. No se atribuyen cambios a personas que todavía no han participado.

El historial actual registra el inicio del proyecto, la estructura HTML, el diseño adaptable, la conexión y controles de la API, la corrección del estado vacío y esta documentación. Para cumplir la colaboración solicitada, el equipo debe continuar aportando mediante sus propias cuentas de GitHub.

## GitHub Pages

En el repositorio abre **Settings → Pages**. En **Build and deployment**, elige **Deploy from a branch**, selecciona main y /(root), y guarda. Al completarse la publicación, copia aquí la dirección que muestre GitHub Pages.

## Preguntas para la presentación

- fetch() solicita los datos JSON a la API y permite trabajar con la respuesta mediante promesas.
- HTML define el contenido, CSS presenta el diseño y JavaScript controla la interacción y las consultas.
- El buscador envía el texto como parámetro name a la API y vuelve a dibujar los resultados recibidos.
- Si la API no responde o falla la conexión, se muestra un mensaje de error; si no hay coincidencias, se muestra un estado vacío.
- La IA apoyó la creación de la estructura y la lógica; el equipo debe explicar y personalizar el código y esta reflexión.
- GitHub Pages publica los archivos estáticos del repositorio seleccionado desde main y la carpeta raíz.
