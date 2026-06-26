# sesión 04 - 23/03


# ¿Qué es p5.js?

p5.js es una librería de JavaScript pensada para arte, diseño, animación e interactividad visual.

Sirve para:

- hacer dibujos,

- animaciones,

- visuales interactivas,

- proyectos generativos,

- arte digital,

- videojuegos simples.


---

# Estructura básica de p5.js

## setup()

La función `setup()` se ejecuta una sola vez al inicio.

Generalmente se usa para:

- crear el canvas,

- definir colores,

- configurar texto,

- iniciar variables.

Ejemplo:


function setup() {

  createCanvas(500, 500);

}



---

## draw()

La función `draw()` se ejecuta infinitamente mientras el programa está funcionando.

Sirve para:

- animaciones,

- movimiento,

- interacción,

- actualización visual.

Ejemplo:



function draw() {

  background(0);

}



---

# Canvas

El canvas es el espacio donde se dibuja todo.



createCanvas(500, 500);


- primer número = ancho

- segundo número = alto

---

# Coordenadas

El punto `(0,0)` está arriba a la izquierda.

- X mueve horizontalmente

- Y mueve verticalmente
