# Sesión 08 - 05/06
# ESTADOS Y CÁMARA WEB

Sketch con estados diferentes 
- 3 pantallas y que se vuelva a reiniciar(El examen)

1. Crear y definir variable de estados:
- Al principio de tu código (fuera de las funciones), debes crear una variable que guarde en qué pantalla nos encontramos. Empezará en 0.
- let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final

2. Configurar el lienzo(function setup):
- Creamos el lienzo de fondo 
<img width="422" height="218" alt="Captura de pantalla 2026-06-19 201352" src="https://github.com/user-attachments/assets/32832bba-50d8-4a1c-bd36-efb34333df17" />

3. Crear la estructura del estado(Function draw):
- Break es para salir de un ciclo
- Aquí usamos un switch Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.
<img width="285" height="361" alt="Captura de pantalla 2026-06-19 201432" src="https://github.com/user-attachments/assets/fca19aa8-b8f1-47dd-b1cb-bf290ed9e743" />

4. Programar visualmente cada estado(Funciones propias):
- Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.
<img width="855" height="715" alt="Captura de pantalla 2026-06-19 201513" src="https://github.com/user-attachments/assets/d53a005c-a2c5-4a13-b563-cf32320d709f" />

5. La lógica del cambio y del reinicio:
- Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función
mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.
- Para el examen poner width /2, height/2 para poner algo al centro porque si no se va a deformar
- Se puede programar que cambie de pantalla con un enter
- Ej profe: (https://editor.p5js.org/PoliMujica/sketches/9vHePO158)

## HAY MUCHAS FORMAS DIFERENTES DE CAMBIAR DE UN ESTADO A OTRO
1. Interacción con el Teclado: 
- 1.1. Por barra espaciadora o Enter:
<img width="628" height="203" alt="Captura de pantalla 2026-06-19 201557" src="https://github.com/user-attachments/assets/8a310366-eb95-4451-81d0-578c8fce0644" />

- 1.2. Por teclas específicas (ej. Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.
<img width="606" height="182" alt="1" src="https://github.com/user-attachments/assets/0154ff3a-ffe4-4a2e-9f23-62e81573874a" />

- Ej profe: https://editor.p5js.org/PoliMujica/sketches/4lzOYE8KL

2. Botones Reales en la Pantalla: En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js. Esto es mucho más profesional para menús.
- Ej profe: https://editor.p5js.org/PoliMujica/sketches/peTm3oGty
<img width="572" height="360" alt="1" src="https://github.com/user-attachments/assets/34e56801-d89c-4b45-a99e-03d6272d0aaa" />

3. Zonas de Clic (Botones dibujados con rect o ellipse): Si no quieres usar botones de
HTML y prefieres dibujar tus propios botones con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.
- Ej profe:https://editor.p5js.org/PoliMujica/sketches/iw-gjFhK8
<img width="738" height="228" alt="1" src="https://github.com/user-attachments/assets/38aa9e26-78de-4e72-9198-a0f9fbff6de3" />

4. Interacciones Automáticas (Por Tiempo o Puntaje): Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que dura 3 segundos y pasa sola al menú.
- Ej profe: https://editor.p5js.org/PoliMujica/sketches/_AunxbPWQ
<img width="442" height="87" alt="1" src="https://github.com/user-attachments/assets/cdcd22f1-6ede-4c17-b6f0-a90873d8a8ae" />

- Processing community day: 26 y 27 junio
- Las notas del examen se promedia con la de los encargos que vale un 15%

### INTERACCIÓN CON EL MUNDO FÍSICO
CÁMARA WEB
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del
computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.

3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
- Ejemplo profe: https://editor.p5js.org/PoliMujica/sketches/PhkuD7kWU
<img width="392" height="302" alt="1" src="https://github.com/user-attachments/assets/036a6a0a-e847-4119-9b77-572739622665" />

- Ejemplos cámara interactiva
    * FILTROS: (https://editor.p5js.org/PoliMujica/sketches/sK_BYepGn)
(https://p5js.org/reference/p5/filter/)

    * LOADPIXELS: (https://editor.p5js.org/PoliMujica/sketches/OVsazOghk)
(https://p5js.org/reference/p5/loadPixels/)

    * PINCEL DE (https://editor.p5js.org/PoliMujica/sketches/cYCPjuXft)

    * Volumen del micro: (https://editor.p5js.org/PoliMujica/sketches/L9QBzREF3)
