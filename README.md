# Cyber-snake
Videojuego de una serpiente cibernética

## 🌀 Agujero cuántico (nuevo)

Al tragar el nanobot número 10 (el umbral de crecimiento), el orbe **se sustituye por un agujero cuántico** que aparece en el tablero: un vórtice violeta con anillos de acreción y partículas espiralando hacia dentro. Entra en él para **descender al piso inferior**:

- La serpiente es succionada, atraviesa el vórtice y aterriza en el piso de abajo.
- El mapa se amplía **conservando el mapa actual intacto**: la serpiente, los obstáculos y el tablero existente **no se desplazan ni un solo cuadro** (el mapa crece anclado por su esquina superior izquierda, hacia la derecha y hacia abajo).
- Los obstáculos nuevos del piso aparecen **sólo en la zona recién añadida**, nunca sobre el mapa actual ni bajo la serpiente (esto corrige el fallo anterior por el que la serpiente se desplazaba y a veces aparecía sobre un obstáculo).

## 👁 Vista en primera persona (nuevo)

Pulsa **V** o el botón **👁** del HUD para alternar entre la vista cenital habitual y una **vista en primera persona desde arriba de la cabeza de la serpiente**, mirando al frente y con giro suave de cámara en cada curva.

- **Sólo en primera persona** aparecen **dos teclas luminosas a los laterales de la cabeza** (◄ cian a la izquierda, ► magenta a la derecha). Latidos con más brillo que el resto de elementos, y **al pulsarlas (clic o toque) la serpiente gira** hacia ese lado. Destellan al accionarlas.
- Las teclas no se ven ni funcionan en la vista cenital.

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
- **V / 👁** alternar vista cenital ↔ primera persona
- **◄ ►** (teclas laterales de la cabeza, sólo en 1ª persona) girar a izquierda/derecha

## Ejecutar

Abre `index.html` en un navegador o sírvelo con cualquier servidor estático:

```bash
python3 -m http.server 8080
```
