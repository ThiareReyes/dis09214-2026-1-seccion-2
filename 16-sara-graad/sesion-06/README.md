# sesión 06 - 14/04
---
#  Transformaciones y Condicionales


---

## 1. Ángulos en p5.js (Radianes vs Grados)
Por defecto, p5.js mide los ángulos en **radianes** (donde una vuelta completa al círculo es `TWO_PI`).
* Para trabajar con los grados que usamos siempre (0 a 360°), hay que cambiar la configuración dentro de `setup()`.

```javascript
function setup() {
  createCanvas(400, 400);
  angleMode(DEGREES); // Cambia el sistema a grados (0-360)
}
