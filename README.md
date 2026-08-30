# Cyber-snake
Videojuego de una serpiente cibernética

## ✨ Novedades visuales

- **Bloom (post-procesado)** con UnrealBloomPass de Three.js para un auténtico brillo neón. Se desactiva automáticamente si el dispositivo va justo de rendimiento, y puedes alternarlo con la tecla **B**.
- **Mayor sensación de profundidad**: skyline retro-futurista animado en el horizonte (sol sintético con rayas, edificios con ventanas parpadeantes, balizas y estrellas), niebla atmosférica, fragmentos de datos flotantes con parallax, haces de luz en las esquinas del campo, charcos de luz bajo la serpiente, el nanobot y los obstáculos, y viñeta cinematográfica.
- **Cámara cinemática**: balanceo sutil constante, golpe de zoom al tragar, sacudida al morir.
- **Efecto de cambio de color al tragar**: cada nanobot aparece con un color neón distinto (con halo, luz puntual y charco de luz a juego). Al tragarlo:
  - **El elemento** parpadea y vuela hacia la boca de la serpiente encogiéndose (animación de absorción), con explosión de chispas, onda expansiva, pilar de luz y flash de pantalla de su color.
  - **La serpiente** es recorrida de la cabeza a la cola por una onda luminosa del color devorado; la cabeza destella y el segmento nuevo conserva el tinte durante unos segundos antes de volver al degradado original.
- **Nanobot con cuenta atrás visible**: parpadea cada vez más rápido cuando está a punto de expirar.
- Animaciones basadas en *delta-time* (velocidad consistente en cualquier pantalla) y liberación de memoria de geometrías/materiales al recrear la serpiente.

## Controles

- **↑ ↓ ← →** o **W A S D** para mover
- **Desliza** o usa el **D-PAD** táctil
- **ESPACIO / TURBO** para velocidad x3
- **P / ESC** pausa
- **B** activar/desactivar bloom

## Ejecutar

Abre `index.html` en un navegador o sírvelo con cualquier servidor estático:

```bash
python3 -m http.server 8080
```
