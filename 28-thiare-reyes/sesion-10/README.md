## sesión 06 - 05/06
#Estados y Cámara web

**PASO 1**

CREAR Y DEFINIR VARIABLE ESTADOS
 1. Al principio de tu código (fuera de las funciones), debes crear una
variable que guarde en qué pantalla nos encontramos. Empezará en 0.

<img width="888" height="118" alt="Captura de pantalla 2026-06-26 043134" src="https://github.com/user-attachments/assets/b60a8399-0b3b-4191-a926-771ffb8107db" />


**PASO 2**

CONFIGURAR EL LIENZO (function setup)
2. Creamos el lienzo de fondo donde va a ocurrir toda la magia.

<img width="437" height="238" alt="Captura de pantalla 2026-06-26 043124" src="https://github.com/user-attachments/assets/db8298fa-d5aa-4b7a-bafc-b996b351cc23" />


**PASO 3**

CREAR LA ESTRUCTURA
DEL ESTADO (function draw)
3. Aquí usamos un switch Dependiendo del valor de la variable estado, el programa
dibujará una cosa u otra.

<img width="398" height="440" alt="Captura de pantalla 2026-06-26 043330" src="https://github.com/user-attachments/assets/2b55e43a-77ed-4b7b-829e-c4b1a32726fe" />


**PASO 4**

PROGRAMAR VISUALMENTE
CADA ESTADO (funciones propias)
4. Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente
para que se note el cambio.

<img width="601" height="482" alt="Captura de pantalla 2026-06-26 043451" src="https://github.com/user-attachments/assets/55792110-dc63-4861-929f-8dadfcfd2dc4" />


**PASO 5**

LA LÓGICA DEL CAMBIO Y EL REINICIO
5. Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función
mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después
del estado 2), volverá a 0.

<img width="477" height="243" alt="Captura de pantalla 2026-06-26 043557" src="https://github.com/user-attachments/assets/a13a4cd9-ad11-4bd0-aa3e-c8a69e0fa2b8" />


## MUCHAS FORMAS DIFERENTES DE CAMBIAR DE UN ESTADO A OTRO

  1.Interacción con el Teclado
    1. Por barra espaciadora o Enter:

<img width="500" height="167" alt="Captura de pantalla 2026-06-26 043825" src="https://github.com/user-attachments/assets/9d217ec3-3ed0-4592-bb1f-a9c247cd27c1" />


  2. Por teclas específicas (ej. Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.

<img width="472" height="161" alt="Captura de pantalla 2026-06-26 043938" src="https://github.com/user-attachments/assets/e557008f-b291-4454-9c2d-9d6739076254" />


  2. Botones Reales en la Pantalla
  - En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de
HTML usando la librería de p5.js. Esto es mucho más profesional para menús.

3.Zonas de Clic (Botones dibujados con rect o ellipse)
-  Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(),
puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.

4.Interacciones Automáticas (Por Tiempo)
- Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que
dura 3 segundos y pasa sola al menú.

### CÁMARA WEB

createCapture(VIDEO);

1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del
computador. También definimos tamaño con captura.size(x,y); y es muy importante
agregar captura.hide(); para que esconda el video que HTML pone abajo por default.

3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
