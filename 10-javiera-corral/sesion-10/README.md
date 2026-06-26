# sesión 10 - 12/06
DISEÑO RESPONSIVO
-
(windowResised)

¿CÓMO CREAR UN SKETCH
QUE SE ADAPTE A DIFERENTES
TAMAÑOS DE PANTALLA?
-

1 CREAR UN CANVAS CON DIMENSIONES DINÁMICAS
-
usar las variables integradas en el sistema:
(windowWidth, windowHeight) estas variables leen constantemente
el ancho y alto disponibles de la ventana del navegador.

function windowResised 
resizeCanvas (windowWidth, windowHeight)

usar valores relativos 
usar fraciones y proporciones para organizar mis elementos del sketch 
(width / 2, height / 2) división 
(width . 0.25) multiplicación

si solamente utilizo estos comandos se va a deformar el dibujo 

estos e usa para arreglar ese problema 
incluir factor de referencia 
let referencia 
referencia=min(width, height) 

para crear figuras que no se deformen se deben crear variables que determinen una medida especifica que se utilizara de referencia y luego se incorporan a los valores relativos 

tambine es mejor usar translate push y pop 

2 CREAR UN EVENTO windowResized()
-

Si el usuario estira o encoge la ventana del navegador, el lienzo se
adaptará al tamaño de la ventana en tiempo real.

3 USAR VALORES RELATIVOS
-

Ahora p5.js actualiza estas variables width y
height automáticamente con el tamaño actual
del lienzo.

Entonces ahora todos los valores de posición y
tamaño que ocupemos los tenemos que pensar
en relación proporcional a esas variables.

Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)

ejemplo de codigo:

``` 
function setup() {
  createCanvas(windowWidth, windowHeight);
}

function draw() {
  background(0);
  
 
  
  fill(250, 100, 100);
  ellipse(width/2 , height/2, width, height);
  
  }

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
}
```

4 INCLUIR VALOR DE REFERENCIA 
referencia = min(width, height)
-

Creamos una variable global
(referencia) y la asignamos para
que calcule el mínimo.

Observa el ancho y el alto de la
ventana, los compara, y se queda
solo con el que sea más pequeño
en ese momento.

ejemplo:

``` 
let referencia;

function setup() {
  createCanvas(windowWidth, windowHeight);
  referencia = min(width, height);
}

function draw() {
  background(0);

  let xCentro = width / 2;
  let yCentro = height / 2;
  
  // El diámetro será siempre el 40% del lado más corto de la ventana
  let diametro = referencia * 0.4; 

  fill(250, 100, 100);
  noStroke();
  ellipse(xCentro, yCentro, diametro, diametro);
  print(width, height);
 
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
  referencia = min(width, height); 
}
```


5 USAR TRANSLATE-PUSH Y POP
-


En lugar de hacer matemáticas
complejas en cada rect() o
ellipse(), usamos translate()
para "mover el origen del mundo”.

Y siempre utilizando push() y
pop() para cada figura o
elemento.

ejemplo:


let referencia;

``` 
function setup() {
  createCanvas(windowWidth, windowHeight);
  referencia = min(width, height);
}

function draw() {
  background(0);
  
  push();
  
  translate (width / 2, height / 2);

  // El diámetro será siempre el 40% del lado más corto de la ventana
  let diametro = referencia * 0.4;
  fill(250, 100, 100);
  noStroke();
  ellipse(0, 0, diametro, diametro);
  
  pop();
  print(width,height);
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
  referencia = min(width, height); 
}
```

AGREGAR IMAGENES 
-
(la profe lo dejo de desafio la otra vez pero habia gente confundida asi que ahora hizo full tutorial)


``` 
let miImagen;

function preload() {
  miImagen = loadImage('ASSETS/poli.jpg'); 
}

function setup() {
  createCanvas(windowWidth, windowHeight);
}

function draw() {
  background(127,255,139);
  image(miImagen, 50, 50, 300, 300); 
}
```
