# 🌸 Clase 22/05 Solemne 2 🌸 

## Manspreading -  Amanda Venegas 

Mi proyecto busca representar de manera sencilla el fenómeno del manspreading, buscando evidenciar cómo este comportamiento afecta el espacio de otras personas en lugares públicos.

### ¿Qué es el manspreading?

El manspreading es una costumbre en la que algunos hombres abren excesivamente las piernas al sentarse, ocupando más espacio del necesario y llegando a incomodar a la persona que está al lado.
Aunque puede parecer una acción cotidiana o automática, ha sido analizada como una práctica que evidencia el uso desigual del espacio compartido.

Para desarrollar esta idea, utilicé como escenario el metro, ya que es un lugar donde esta práctica puede ocurrir con frecuencia debido a la cercanía entre las personas y la falta de espacio personal. El metro evidencia cómo pequeñas acciones pueden tener un impacto directo en los demás.

En la escena se observa el dibujo de un hombre y una mujer sentados uno al lado del otro. A través de la interacción, el personaje masculino comienza a expandirse progresivamente, ocupando cada vez más espacio.

La idea principal del proyecto es mostrar de forma visual e interactiva cómo, con cada clic, el personaje va ocupando más espacio con sus piernas. A mayor cantidad de clics, mayor es el espacio que invade dentro del asiento.

Este proyecto se relaciona con la problemática de género porque representa cómo ciertos comportamientos cotidianos, como el manspreading, pueden reflejar dinámicas de desigualdad en el uso del espacio público. Aunque no siempre es intencional, evidencia cómo el espacio puede ser ocupado de manera desproporcionada, generando incomodidad en otras personas.

El input corresponde a las acciones del usuario al hacer clic sobre la pantalla. Esto modifica variables del programa, como el tamaño del personaje y la apertura de sus piernas, que van aumentando progresivamente. Como resultado, el personaje ocupa cada vez más espacio dentro de la escena, lo que provoca que la mujer se aparte, mostrando incomodidad y enojo.

Lo que busco es mostrar situaciones cotidianas desde otra perspectiva, evidenciando cómo acciones pequeñas pueden tener un impacto en la experiencia de otras personas en espacios compartidos.

<img width="530" height="528" alt="image" src="https://github.com/user-attachments/assets/c952ae96-5887-430b-bc97-d176c587ad48" />

<img width="532" height="528" alt="image" src="https://github.com/user-attachments/assets/e04e34f1-184b-4c19-9324-59b54c3c2465" />


---
### Diagrama de flujo 

<img width="475" height="1183" alt="Sin título (1)" src="https://github.com/user-attachments/assets/a7bf3bb6-e238-4d05-b0e2-f0465eaa131d" />

---

### Referentes

Me inspiré en una imagen encontrada en RedNote, aunque no logré identificar al autor original.

<img width="451" height="640" alt="image" src="https://github.com/user-attachments/assets/26182615-0403-4dac-8791-052bee865f94" />

Universitat Oberta de Catalunya. (2023, 22 de marzo). Mansplaining, manspreading y gaslighting. UOC News. https://www.uoc.edu/es/news/2023/074-mansplaining

---
### Link de trabajo : https://editor.p5js.org/amanda.venegas1/sketches/Ia93yVeeX
---

### Codigo 

```javascript
// estas son variables para guardar las imagenes 
let imagenFondo;
let chicaI;
let chicoI;
let enojoI;

// declare y agrupe variables 

let chico = {  // Todas las variables del chico 
  
// Posicion de la imagen del chico en x y Y 
  x: 546,
  y: 380,
  
// Tamaño de la imagen
  
  ancho: 290,
  alto: 360,
  
// Medida del lado del cuadrado azul 
  lado: 120,

  //variables de la posición de las piernas derecha,izquierda y Tamaño 
  piernaD: 570,
  piernaI: 480,
  tamPierna: 60
};


let chica = { // Variables de la chica 
  x: 180, // Posición de la imagen de la chica en x 
  y: 200, // Posición de la imagen de la chica em y 
  circuloX: 310, // valor de x del circulo que es la cabeza 
};

let click = 0; // cuenta cuantas veces el usuario hace clic 
let rojo; // variable de color rojo despues usada en el map 

function preload() { // sirve para cargar imagenes antes que empiece el programa 
  imagenFondo = loadImage("metrofondo.jpg");
  chicaI = loadImage("chica.png");
  chicoI = loadImage("chico.png");
  enojoI = loadImage("enojo.png");
}

function setup() { // Es una funcion que se ejecuta solo una vez en el prograama 
  createCanvas(800, 800); // Crea un lienzo en x,y 
  frameRate(20); // Es una funcion que limita cuantas veces se ejecuta el draw se mide en fps 
}

function draw() {  // Es una función que se ejecuta constantemente en bucle mientras este funcionando 
// Esto sirve para que el programa ejecute estas funciones en ese orden
// Separe cada elementos en funciones para mantener el codigo mas ordenado y mas facil de entender
  backgroundS(); // Organiza los elementos del fondo 
  patron(); // El patron de puntos 
  boy(); // Dibuja los elementos del chico 
  girl(); // Dibuja los elementos / partes de la chica 
  titulo(); // Dibuja los elementos del titulo
  enojo(); // Dibuja la imagen de simbolo de enojo 
}

// Funcion de los elementos del fondo - map - imagen del fondo - lineas 

function backgroundS() {

  rojo = map(chico.ancho, 290, 350, 0, 255); // Para convertir un valor de un rango a otro rango de 0 a 255  map(valor, mínimo1, máximo1, mínimo2, máximo2)

  background(rojo, 0, 0); // Crea un fondo en rgb ( rojo, verde y green )

  image(imagenFondo, 0, 0, width, height);  // carga la imagen de fondo en la posicion 0,0 oero con medidas del ancho y alto del lienzo 

  fill(rojo, 0, 0, 150); // rellena el lienzo de un cuadrado rojo con cierta trasparencia 
  rect(0, 0, width, height); // tamaño del cuadrado rojo que tambien mide a}el mismo ancho y alto del lienzo  
}



function patron() { // cree una funcion solo para el patron del fondo 

  

  strokeWeight(3); // grosor del punto 
  stroke(0); // color negro 

 
  for (let x = 300; x < 750; x += 20) { // comienza a dibujar en  300 del eje X y avanza hasta 750, saltando de 20 en 20.
    for (let y = 0; y < 300; y += 20) { // comienza a dibujar en  0 del eje Y y avanza hasta 300, saltando de 20 en 20.
      point(x, y); // Dibuja un punto en esa coordenada.
    }
  }
}

function girl() { // Elementos de la chica 

  noStroke(); // Quita el borde de las figuras.

  image(chicaI, chica.x, chica.y); // coloca la imagen en los valores de x,y 

  
  // Si el usuario ha hecho exactamente 6 clics el circulo cambia random el color en rojo, verde y azul y si no hay 6 clics deja el color fijo en esos valores 
  if (click == 6) { 

    fill(random(255), random(255), random(255)); 
    circle(chica.circuloX, 285, random(200));

  } else {

    fill(238, 157, 225);
    circle(chica.circuloX, 285, 120); // circle(posiciónX, posiciónY, diámetro);
  }
}



function boy() {  // Esta función se encarga de dibujar al personaje chico.

  push(); // Guarda la configuración actual del dibujo (colores, modos)

  fill(91, 69, 169); // Define el color de relleno
  noStroke(); // Quita el borde de las figuras.
  
// pierna izquierda 
  rect(chico.piernaI, 540, chico.tamPierna, 220);
  
// pierna derecha 
  
  rect(chico.piernaD, 540, chico.tamPierna, 220);

  imageMode(CENTER); // Hace que las imágenes se dibujen desde el centro.
  rectMode(CENTER); // Hace que los rectángulos también se dibujen desde el centro.

  image(chicoI, chico.x, chico.y, chico.ancho, chico.alto); // Dibuja la imagen del chico. (iamgen,x,y, ancho , alto)

  square(chico.x, chico.y - chico.alto / 2 + 105, chico.lado); // Dibuja un cuadrado encima del personaje ajustando su posición para que quede sobre la cabeza. chico.y - chico.alto / 2 + 105  ajusta la altura para colocarlo sobre la cabeza
  
  pop(); // Vuelve a la configuración original para que los cambios de esta función no afecten al resto del programa 
}


function titulo() {  // Esta función se encarga de dibujar el título 

  fill(255); // Define el color blanco para el texto.
  textSize(30); // Define el tamaño del texto en pixles 
  textFont("Georgia"); // Declara que tipografia utilizar 

  text("¿Como ocupas el espacio?", 250, 60); // Dibuja el titulo (texto, posición X, posición Y)

  fill(0); // rellena el color en valores rgb pero solo esta declarado en 0 que es negro

  quad(0, 0, 800, 0, 800, 20, 0, 20); // Dibuja un cuadrilátero en la parte superior de la pantalla en sentido horario 
  
  quad(0, 800, 800, 800, 800, 780, 0, 780); // // Dibuja un cuadrilátero en la parte superior de la pantalla en sentido horario 
}

function enojo() { // Elementos de la imagen enojo 
  
   if (click >= 5) { // Despues de 5 clics realiza lo siguiente 
     
     push (); //  Guarda la configuración actual del dibujo 
    translate(300, 250); // Mueve el sistema de coordenadas a la posición (300, 250)
    rotate(frameCount * 0.05); // Rota la imagen continuamente con el tiempo, frameCount es un contador de cuadros

    imageMode(CENTER); //Hace que la imagen se dibuje desde su centro.
    image(enojoI, 0, 0, 70,70); // coloca la imagen en el lienzo en image(imagen, x, y, ancho, alto);
     
     pop(); // Cierra la configuracion  para que no afecte a las siguientes partes del programa 
     
     
}
}

function mousePressed() { // // Esta función se ejecuta cada vez que el usuario hace clic con el mouse.

  if (click < 6) { // Si el usuario da menos de 6 clics ejecuta lo siguiente 

    chico.ancho += 10; // aumenta el ancho de la imagen del chico 
    chico.alto += 25; // aumenta el alto 
    chico.lado += 15; // aumenta el tamaño del cuadrado del chico 

    chico.piernaD += 15; // Mueve la pierna derecha hacia la derecha 
    chico.piernaI -= 25; // mueve la pierna izquierda hacia la izquierda 
    chico.tamPierna += 5; // aumenta sutilmente el tamaño de las piernas.

    click++; //Suma 1 al contador de clics.
  }

  if (click == 5) { // si el usuario dio 5 clicks realiza esto 

    chica.x -= 50; // mueve a la chica a la izquierda 
    chica.circuloX -= 50; // mueve también el circulo 
  }
}
```








