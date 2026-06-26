# sesión 03 - 27/03

========================================
 APUNTES DE CLASE — INTRODUCCIÓN A p5.js
========================================

p5.js es una librería de JavaScript orientada al
Creative Coding.

Se utiliza para:
- Crear gráficos
- Hacer animaciones
- Generar interacciones visuales
- Programar experiencias en tiempo real

Sitio oficial:
https://p5js.org/

Referencia:
https://p5js.org/reference/


========================================
 PENSAMIENTO COMPUTACIONAL
========================================



Un algoritmo es una secuencia de instrucciones:

✔ Lógicas
✔ Ordenadas
✔ Definidas
✔ Finitas

Sirve para resolver un problema o realizar
una tarea específica.

----------------------------------------
 CARACTERÍSTICAS DE UN ALGORITMO
----------------------------------------

1. Precisión
   Cada paso debe ser claro.

2. Orden
   Los pasos siguen una secuencia lógica.

3. Finitud
   Debe terminar en algún momento.

4. Definición
   Mismos datos → mismo resultado.


----------------------------------------
 ESTRUCTURA DE UN ALGORITMO
----------------------------------------

INPUT  → información de entrada

PROCESO → transformación lógica

OUTPUT → resultado final


----------------------------------------
 EJEMPLO
----------------------------------------

INPUT:
Ingredientes + utensilios

PROCESO:
Preparar un sandwich

OUTPUT:
Sandwich terminado


========================================
 DIAGRAMAS DE FLUJO
========================================

Un diagrama de flujo es la representación
gráfica de un algoritmo.

Se utiliza para:
- Planificar programas
- Visualizar lógica antes de programar
- Comunicar procesos


========================================
 LENGUAJES DE PROGRAMACIÓN
========================================

Existen miles de lenguajes de programación.

Categorías comunes:

GENERAL
- Python
- Java
- C++
- C#

WEB
- JavaScript
- TypeScript
- PHP

BAJO NIVEL
- C
- Rust
- Go

CIENCIA DE DATOS
- Python
- R
- Julia

MÓVIL
- Swift
- Kotlin


========================================
 ¿QUÉ ES REALMENTE p5.js?
========================================

p5.js NO es un lenguaje nuevo.

Es una librería de JavaScript que agrega
funciones simples para:

- Dibujar
- Animar
- Crear experiencias visuales
- Interactuar en tiempo real


========================================
 FUNCIONES PRINCIPALES EN p5.js
========================================

----------------------------------------
 setup()
----------------------------------------

Se ejecuta UNA sola vez al inicio.

Se utiliza para:
- Crear el canvas
- Configurar variables
- Cargar recursos

Ejemplo:
*/

function setup() {
  createCanvas(500, 500);
}

/*
----------------------------------------
 draw()
----------------------------------------

Se ejecuta constantemente en bucle
(~60 FPS).

Se utiliza para:
- Animaciones
- Movimiento
- Interacción
- Actualización visual

Ejemplo:
*/

function draw() {
  background(220);
}

/*
========================================
 CANVAS
========================================

----------------------------------------
 createCanvas()
----------------------------------------

Crea el área de dibujo.

Sintaxis:
createCanvas(width, height);

Ejemplo:
createCanvas(500, 500);

----------------------------------------
 RENDERIZADORES
----------------------------------------

P2D   → Renderizado 2D (default)

WEBGL → Renderizado 3D


========================================
 BACKGROUND
========================================

----------------------------------------
 background()
----------------------------------------

Define el color de fondo del canvas.

Sintaxis:
background(r, g, b, alpha);

Ejemplos:

background(220);
background(255, 0, 0);
background('blue');
background(0, 0, 255, 50);

IMPORTANTE:

En setup()
→ el fondo queda fijo.

En draw()
→ limpia el canvas constantemente.


========================================
 ESPACIOS DE COLOR
========================================

----------------------------------------
 RGB
----------------------------------------

colorMode(RGB);

R → Red
G → Green
B → Blue

Rango:
0 - 255


----------------------------------------
 HSB / HSV
----------------------------------------

colorMode(HSB);

H → Hue
S → Saturation
B → Brightness


----------------------------------------
 HSL
----------------------------------------

colorMode(HSL);

H → Hue
S → Saturation
L → Lightness


========================================
 SISTEMA DE COORDENADAS
========================================

En p5.js:

(0,0)
está en la esquina superior izquierda.

Eje X:
→ aumenta hacia la derecha

Eje Y:
↓ aumenta hacia abajo


========================================
 FIGURAS GEOMÉTRICAS BÁSICAS
========================================

Funciones principales:

point(x, y);

line(x1, y1, x2, y2);

rect(x, y, w, h);

ellipse(x, y, w, h);

circle(x, y, d);

square(x, y, size);

triangle(x1, y1, x2, y2, x3, y3);

quad(x1, y1, x2, y2, x3, y3, x4, y4);


========================================
 BORDES Y LÍNEAS
========================================

----------------------------------------
 strokeWeight()
----------------------------------------

Define el grosor del borde.

Ejemplo:
strokeWeight(10);


----------------------------------------
 stroke()
----------------------------------------

Define el color del borde.

Ejemplo:
stroke(255, 0, 0);


----------------------------------------
 strokeCap()
----------------------------------------

Define la forma de los extremos de línea.

Ejemplos:

strokeCap(ROUND);

strokeCap(SQUARE);

strokeCap(PROJECT);


----------------------------------------
 noStroke()
----------------------------------------

Elimina bordes.

Ejemplo:
noStroke();


========================================
 RELLENO
========================================

----------------------------------------
 fill()
----------------------------------------

Define color de relleno.

Ejemplo:
fill(252, 159, 216);


========================================
 FIGURAS AVANZADAS
========================================

----------------------------------------
 arc()
----------------------------------------

Permite dibujar arcos o semicircunferencias.

Sintaxis:
arc(x, y, w, h, start, stop);

Ejemplo:
arc(250, 250, 100, 100, 270, 90);


========================================
 ÁNGULOS EN p5.js
========================================

Por defecto:

0°   → Derecha
90°  → Abajo
180° → Izquierda
270° → Arriba

RECOMENDACIÓN:
*/

angleMode(DEGREES);

/*
========================================
 RECURSOS ÚTILES
========================================

Editor p5.js:
https://editor.p5js.org/

Documentación createCanvas():
https://p5js.org/reference/#/p5/createCanvas

Documentación background():
https://p5js.org/reference/#/p5/background

Documentación arc():
https://p5js.org/reference/#/p5/arc

Color Picker RGB:
https://rgbcolorpicker.com/

HTML Color Codes:
https://htmlcolorcodes.com/


========================================
 EJEMPLO COMPLETO
========================================

Este ejemplo utiliza:
- Canvas
- Background
- Fill
- Stroke
- Figuras
- Arc
*/

function setup() {
  createCanvas(600, 400);

  angleMode(DEGREES);
}

function draw() {

  // Fondo
  background(30);

  // Rectángulo
  fill(255, 0, 0);
  stroke(255);
  strokeWeight(3);

  rect(50, 50, 120, 80);

  // Círculo
  fill(0, 150, 255);
  circle(300, 200, 100);

  // Línea
  stroke(255, 255, 0);
  strokeWeight(5);

  line(0, 0, mouseX, mouseY);

  // Arco
  noFill();
  stroke(0, 255, 120);

  arc(500, 200, 120, 120, 270, 90);

}
