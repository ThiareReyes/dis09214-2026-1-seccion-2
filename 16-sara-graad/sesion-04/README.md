# sesión 04 - 23/03
------

##  1. ¿Qué es una Variable?
Es un contenedor con un nombre que guarda un dato que puede cambiar.
* **Antes:** Se usaba `var`.
* **Ahora:** Usamos `let` (para cosas que cambian) y `const` (para valores fijos que nunca cambian).

### Pasos para usar tus propias variables:
1. **Declarar:** Crearla arriba del todo (`let miVariable;`).
2. **Inicializar:** Darle su valor inicial (`miVariable = 10;`).
3. **Usar:** Meterla en tus figuras (`ellipse(miVariable, 200, 50);`).

---

##  2. Variables del Sistema (Ya vienen listas en p5.js)
No necesitas crearlas, p5.js ya sabe lo que significan:

*  **Mouse:**
    * `mouseX` / `mouseY` -> Posición actual del cursor en X e Y.
    * `pmouseX` -> Posición del mouse en el cuadro anterior (sirve para medir velocidad).
    * `mouseIsPressed` -> Devuelve `true` o `false` si estás haciendo clic.
*  **Lienzo y Ventana:**
    * `width` / `height` -> El ancho y alto de tu `createCanvas`.
    * `windowWidth` / `windowHeight` -> El tamaño completo de la ventana del navegador.
*  **Tiempo:**
    * `frameCount` -> Cuántos fotogramas han pasado desde que inició el sketch.

---

## 3. Funciones Clave para Dar Vida

### `random()` -> El generador de azar
Devuelve números aleatorios para que nada sea estático.
* `random(100);` -> Tira un número al azar entre 0 y 100.
* `random(20, 50);` -> Tira un número al azar entre 20 y 50.

### `map()` -> El traductor de escalas
Toma un número que está en una escala y lo traduce proporcionalmente a otra.
* **Sintaxis:** `map(valor, min_original, max_original, min_nuevo, max_nuevo);`
* *Ejemplo:* Traducir la posición del mouse (0 a 400) para que controle el color del fondo (0 a 255).

---

## 4. Objetos en JavaScript (`Objects`)
Sirven para agrupar muchas variables relacionadas dentro de un solo "contenedor" para tener el código ordenado.

```javascript
// Así se crea un objeto
let circulo = {
  x: 100,
  y: 200,
  diametro: 50
};

function draw() {
  // Así se usa (con el puntito)
  ellipse(circulo.x, circulo.y, circulo.diametro);
  circulo.x++; // Movimiento continuo
}
