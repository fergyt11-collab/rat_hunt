# Rat Hunt

Juego 3D de terror caricaturesco para una persona. Eres la rata: atrapa a cinco exploradores antes de que roben ocho quesos y escapen.

[Jugar la versión publicada](https://rat-hunt-laberinto.fernado-gonzalezjaco.chatgpt.site)

## Controles
- WASD: moverse. Ratón: mirar (haz clic en el escenario).
- Flechas izquierda/derecha: girar; arriba/abajo: avanzar y retroceder.
- E: olfato, revela temporalmente dirección y distancia de los NPC.
- Espacio: impulso.
- F: entrar a un túnel cercano.
- P o Escape: pausa.
- Móvil: palanca izquierda, deslizar sobre el escenario para mirar y botones táctiles.

## Mecánicas
- Laberinto nuevo en cada partida, cámara en primera persona y paredes altas de queso.
- Cinco exploradores con visión bloqueada por paredes, huida inmediata y memoria breve de la amenaza.
- Ocho jaulas que requieren 4,5 segundos sin interrupciones para conseguir el queso.
- Dos salidas: los NPC consideran la posición de la rata para elegir una ruta.
- Tres pares de túneles exclusivos de la rata, con travesías de 1,4 segundos.
- Protección contra vigilar un queso: aviso a los 7 segundos y traslado animado a los 12.
- El radio de vigilancia es de 31 unidades por rutas transitables, incluyendo atajos. Salir brevemente no reinicia el contador.
- Final animado con celebración o tristeza según el resultado.

## Publicar con GitHub Pages
Los archivos están preparados para publicarse directamente desde la raíz.

1. Abre Settings > Pages en este repositorio.
2. En Build and deployment, selecciona Deploy from a branch.
3. Selecciona la rama main y la carpeta / (root), y guarda.
4. Espera a que GitHub confirme la publicación y usa el enlace que aparezca.

Documentación: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Probar localmente
Con Python instalado, ejecuta en esta carpeta:

```sh
python -m http.server 8000
```

Abre http://localhost:8000. Python solo sirve los archivos; el juego está programado en JavaScript. Se necesita un navegador con WebGL y JavaScript. Abrir index.html con file:// puede bloquear los módulos.

## Estructura
- index.html: interfaz.
- style.css: tipografía, HUD y adaptación a pantallas.
- game.js: renderizado, modelos, controles, IA y reglas.
- three.module.js y three.core.js: Three.js 0.186.1.
- fonts/: fuentes Creepster y Special Elite con sus licencias.
- THREE-LICENSE.txt: licencia de Three.js.

No requiere claves, servicios externos ni instalación de dependencias.

## Validación
Comprobadas mediante simulación: rutas, captura, pausa, reinicio, finales, habilidades, túneles, apertura de jaulas, huida y traslado de quesos. Pendientes pruebas visuales y de rendimiento en navegadores reales.
