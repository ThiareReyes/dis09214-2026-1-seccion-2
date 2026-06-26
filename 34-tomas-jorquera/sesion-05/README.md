# sesión 04 - 10/04

# sesión 04 - 10/04

# Movimientoooo

La clase fue básicamente:

## “ok ya hicimos dibujos estáticos, ahora hagamos que se muevan”

Entramos al mundo del:

- movimiento,

- interacción,

- mouse,

- variables,

- caos controlado,

- números random.

---

# mouseX y mouseY

Las variables más importantes de la clase.


mouseX

mouseY


Sirven para saber:

- dónde está el mouse en X,

- dónde está el mouse en Y.

Ejemplo:


circle(mouseX, mouseY, 100);


El círculo sigue al mouse.

Literal magia.

---

# Variables integradas en p5

p5 ya trae variables listas.

Algunas importantes:

width

height


guardan tamaño del canvas.

---

frameCount


cuenta frames desde que inicia el sketch.

---


mouseIsPressed



detecta si el mouse está apretado.

---



key


detecta teclas.

---

# Crear variables propias

Usamos:


let



para crear variables dinámicas.

Ejemplo:


let x = 100;


También existe:


const



para variables que no cambian.
