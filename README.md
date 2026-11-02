# El Manual del GLA

Colección de herramientas web para jugadores de **Grand Line Adventures** (GLA), el juego de Roblox basado en One Piece. El objetivo es facilitar la búsqueda de información y ayudar con los desafíos de eventos como Foxy Count.

Todo funciona directamente en el navegador, sin instalación ni servidor propio: es HTML, CSS y JavaScript puro.

## Herramientas

| Herramienta | Archivo | Descripción |
|---|---|---|
| **Página principal** | `index.html` | Portal con el contador del próximo evento, enlaces a la comunidad y el Registro de Actividades. |
| **Foxy Count** | `foxycount.html` | Filtra personajes por rango (Diamante, Oro, Plata, Bronce), clase, tripulación y color de pelo para resolver los desafíos del evento. |
| **Foxy Memory** | `foxymemory.html` | Ayuda para el minijuego de memoria de colores. Se asignan colores a una cuadrícula de 12 casillas y las casillas con color único parpadean. |
| **Foxy Quiz** | `foxyquiz.html` | Buscador de preguntas del quiz con sus respuestas (verdadero/falso), en español y portugués. |
| **Pacientes Kureha** | `kureha.html` | Elige los 7 pacientes del castillo de Kureha y muestra remedios, ingredientes, ubicaciones y audios. Incluye total de materiales y tutorial guiado. |
| **Antorchas Noland** | `puzzle_antorchas.html` | Solucionador del puzzle de las 8 antorchas de Noland. Calcula qué antorchas pulsar y en qué orden, con modo de práctica. |
| **Tierlist PVE** | enlace externo | Tierlist de personajes para PVE en TierMaker. |
| **Videoguías** | enlace externo | Lista de reproducción de YouTube con guías del juego. |

### Registro de Actividades

Permite crear cuentas y marcar las actividades semanales de cada una (bosses, raids, eventos Foxy, etc.), además de seguir el progreso de medallas y estrellas para el desbloqueo de personajes Diamante. Los datos se guardan en el navegador (IndexedDB), por lo que no se suben a ningún lado, y las actividades se reinician cada semana.

## Estructura del proyecto

```
├── index.html, foxycount.html, foxymemory.html,
│   foxyquiz.html, kureha.html, puzzle_antorchas.html
├── css/        Estilos (versión .min usada en producción)
├── js/         Lógica de cada página
├── Img/        Imágenes, íconos y medallas
└── audios/     Sonidos de los pacientes de Kureha
```

## Uso local

No requiere dependencias. Basta con clonar el repositorio y abrir `index.html` en el navegador:

```bash
git clone <url-del-repositorio>
cd <carpeta>
```

Algunos navegadores restringen funciones como IndexedDB al abrir archivos directamente; si algo no carga, conviene servir la carpeta con un servidor local, por ejemplo `python -m http.server`.

Notas:
- El contador del próximo evento consulta una API externa, por lo que necesita conexión a internet.
- Las fuentes e íconos (Google Fonts, Font Awesome) y el tutorial de Kureha (Shepherd.js) se cargan desde CDN.

## Créditos

- Desarrollado por **Droflax** ([canal de YouTube](https://www.youtube.com/@Droflax/videos)).
- Grand Line Adventures y One Piece pertenecen a sus respectivos creadores. Este es un proyecto de fans, sin fines de lucro y sin afiliación oficial.

## Comunidad

- [Discord de El Manual del GLA](https://discord.gg/invite/eKZaYBKd3W)
- [Discord de Grand Line Adventures](https://discord.gg/grandlineadventures)
- [WikiGLA (portugués)](https://wiki.gla.com.br/index.php)
