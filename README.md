# 🐍 CYBER SNAKE — Nanobot Hunter

Videojuego de una serpiente cibernética construido con **Three.js (r128)** en un único archivo HTML.

## 🎮 Cómo jugar
- **Movimiento:** flechas `↑ ↓ ← →` o `W A S D`, deslizando en móvil o con el D-PAD táctil.
- **Turbo:** mantén `ESPACIO` o el botón `⚡ TURBO` (velocidad ×3).
- **Objetivo:** absorbe nanobots para crecer y subir de nivel. Evita obstáculos y tu propio cuerpo.

## ✨ Características visuales
- **Efecto de absorción de color:** al tragar un nanobot, el elemento parpadea, encoge y vuela hacia la cabeza de la serpiente mientras esta **adopta su color** (con una ola de energía que recorre el cuerpo, destello de luces del mundo, sacudida de cámara y HUD teñido del color absorbido).
- **Sensación de profundidad:** niebla atmosférica, skyline de torres de neón alrededor de la arena, pilares de cristal en las esquinas, orbes flotantes, estrellas en capas y luz hemisférica/rim.
- **Nanobots con variantes:** núcleo con escudo de cristal, anillos orbitales, anillo de base y glow billboard; cada 10% de nanobots son **de oro (+2 puntos)** y algunos **negros**.
- **Luces ambientales personalizables:** modo `CYBER` (cian/magenta) o `CUSTOM` (tono/saturación/intensidad configurables desde el menú).
- **Efectos extra:** ondas de choque al absorber/expirar, destellos de pantalla, toasts de colores, explosiones mejoradas, viñeta y scanlines CRT.
- **HUD dinámico:** la puntuación se tiñe con el último color absorbido y pulsa al sumar puntos.

## 🛠️ Técnica
- Juego 3D completo (Three.js r128) renderizado en WebGL con sprites billboard de glow generados proceduralmente (sin assets externos).
- Todo el juego vive en `index.html`; récords, velocidad y ajustes de luces se guardan en `localStorage`.

## ✅ Verificación
- Suite de pruebas headless (jsdom + three.js real) que cubre: movimiento, absorción/cambio de color, crecimiento, subida de nivel, colisiones (obstáculo y cuerpo), pausa, modos de luz, expiración de nanobots y 200 frames de estabilidad.

## 🚀 Despliegue
Abre `index.html` directamente en el navegador o súrvelo con cualquier servidor estático:

```bash
python3 -m http.server 8100
```
