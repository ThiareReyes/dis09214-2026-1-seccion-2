# sesión 08 - 22/05 solemne 2
# Estereotipos de género  
**Amaro Beltrán**  

## Descripción  
Este proyecto busca exponer la problemática de género sobre los estereotipos de género mediante una animación o sketch de p5.js.  
 
En la pantalla se puede apreciar una figura estereotipada masculina,y otra femenina, con un fondo gris, lineas negras que cruzan de izquierda a derecha a través del lienzo y un círculo negro en el centro, ademas de dos figuras que sostienen al hombre y mujer, acompañado de la frase **¿Qué me define?**.  

luego según las variables y transformaciones, cambia la frase respondiendo a la pregunta con un nada, al presionar el mouse el fondo se vuelve de colores además de aparecer círculos de colores en posiciones aleatorias y un triángulo rosa que gira.  

## Descripción conceptual  
El proyecto busca exponer conceptualmente los estereotipos de género desde una mirada emocional, sobre el cómo se siente estar bajo esa situación, mediante el uso de diversos elementos que relatan esa transición hasta finalmente ser capaz de darse cuenta y romper con esa estructura planteada por la sociedad.  
Cada elemento tiene su significado, partiendo por el color del background el cual es un tono gris, dando una sensación de frialdad y falta de emocionalidad y personalidad al no poder demostrarse como es realmente, las líneas negras buscan crear y potenciar este espacio e idea de sentirse prisionero dentro de este estereotipo, el circulo negro que tiene la capacidad de crecer tambien representa este vacio, por otro lado al activar las condicionales se rompe con el estereotipo, los fondos de colores y circulos de colores, ademas dela respuesta nada representan la diversidad y el entendimiento de que nadie encaja 100% dentro de esta estructura y hay diversas formas de expresar el genero dependiendo de cada persona.  

La regla principal es la condicional if mouseIsPressed, ya que esta es la que cambia por completo el carácter del sketch dando paso a este ambiente más diverso que se plantea en cuanto a romper con los estereotipos de género.  

<img width="1024" height="1536" alt="diagrama de flujo" src="https://github.com/user-attachments/assets/d39d0828-8583-430a-9117-e0b43ab9c7c0" />

## Código  
```let hombre; //variable para guardar imagen de hombre
let mujer; //variable para guardar imagen de mujer
let anguloRot = 0; // declara variable anguloRot=0
let x, y, r, g, b; //declaro todas las variables juntas

function preload() {
  // función, se ejecuta antes para cargar imagen
  hombre = loadImage("hombre.png"); //carga imagen hombre
  mujer = loadImage("mujer.png"); //carga imagen mujer
}

function setup() {
  createCanvas(600, 600); //crea canvas de 600x600
  frameRate(24); //frames por segundo
  noStroke(); //quita los bordes a las figuras
}

function draw() {
  background(189, 189, 189); //da un color gris al fondo
  anguloRot = anguloRot + 0.5; // define que la variable anguloRot se incrementará en 1 cada vez que se hace el loop del draw
  x = random(width); //inicializo cada variable con random fuction
  y = random(height);
  r = random(255);
  g = random(255);
  b = random(255);

  print(frameCount);

  push(); //imagen hombre
  translate(50, 210); //mueve la imagen al punto 50,210
  scale(0.45); //escala la imagen en 0.45 de su tamaño original
  image(hombre, 0, 0);
  pop();

  push(); //imagen mujer
  translate(300, 200); //mueve la imagen al punto 300,200
  scale(0.5); //escala la imagen en 0.5 de su tamaño original
  image(mujer, 0, 0);
  pop();

  push(); // base rectangulo hombre
  fill(0); //da color negro al rectangulo
  translate(115, 435); //mueve el rectangulo al punto 115, 435
  rect(0, 0, 100, 50); //crea un rectangulo en 0,0, ancho 100, alto 50
  pop();

  push(); //base rectangulo mujer
  fill(0); //da el color negro
  translate(380, 435); //mueve el rectangulo al punto 380,435
  rect(0, 0, 100, 50); //crea rectangulo en 0,0, ancho 100, alto 50
  pop();

  push();
  for (let y = 0; y <= 600; y = y + 60) {
    //bucle, inicializa variable y es igual a 0, si y es menor o igual a 600, y es igual al valor de y + 60, crea lineas cada 60 pixeles
    stroke(0); //da color negro a la linea
    strokeWeight(5); // da un grosor de 5 pixeles a la linea
    line(0, y, 600, y); //linea en cordenadas 0, y, 600, y, y segun la variable definida dentro del for
  }
  pop();

  let diameter = map(mouseY, 0, height, 20, 600);
  fill(0);
  circle(width / 2, height / 2, diameter);

  if (mouseIsPressed === true) {
    //si el mouse es presionado
    background(random(255), random(255), random(255));
    noStroke(); //no rellena figura
    fill(r, g, b, 200); // uso cada variable para rellenar las elipses de colores
    ellipse(x, y, 100); //crea elipses de diametro 100 en lugares aleatorios
  }

  if (frameCount <= 250) {
    //cuando el valor es menor a 250
    textSize(50); //tamaño de texto 50
    text("¿Qué me define?", 100, 100); //texto
  } else {
    // si es mayor a 250
    textSize(100); //tamaño de texto 100
    text("NADA", 150, 200); //texto
  }
  if (keyIsPressed) {
    //se reinicia el sketch si se presiona una tecla
    frameCount = 0;
  }
  if (mouseY > 300 && mouseIsPressed) {
    // si el mouse está en coordenada y mayor que 300 y presionado
    fill(255, 117, 183); //rellena de color rosado
    rotate(anguloRot * 2); //rota el triangulo segun la variable anguloRot * 2
    triangle(300, 400, 360, 500, 240, 500); // crea un triangulo en 300,400,360,500,240,500
  }
} ```

