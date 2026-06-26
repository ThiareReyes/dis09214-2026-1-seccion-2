# EXAMEN PENSAMIENTO COMPUTACIONAL

**Información del proyecto**

*ROMPER EL SILENCIO*

Thiare Reyes Medina

Este proyecto es un llamado a **ROMPER EL SILENCIO**, la violencia de género es un tema muy latente en nuestra sociedad y en el ultimo tiempo han habido una cantidad enorme de femicidios y/o agreciones hacia las mujeres, con este proyecto quiero hacer ver lo que muchas mujeres han vivido o viven esta agreción. En este proyecto se puede ver en una primera pantalla la cual es una advertencia de contenido sensible que sigue a mostrar, los elementos que se ven son un triángulo rojo parpadeando acompañado de um ícono de ojo tachado, que significa contenido sensible y la palabra "ADVERTENCIA". tiene instrucciones para poder pasar a la otra pantalla, apretando la letra "w".

Al pasar a la siguiente pantalla se puede ver la imagen de una mujer siendo intimidada por un hombre acompañada de una palabra "BASTA". EN esta pantalla se puede interactuar de varias maneras, una de ellas es hacer click en el lado izquierdo de la pantalla y aparece un sonido de llanto de una mujer, otra interacción es, mover el mouse X hacia la derecha, en esto podemos percibir dos cosas, una de ellas es que el sonido se apaga y lo otro el texto o la palabra BASTA se agranda. Para poder pasar a la otra pantalla tiene el mismo metodo que la anterior solo que ahora la letra para pasar es la "d".

En la ultima pantalla ocurre algo inesperado, se prende la cámara y aparecen unas palabras como lluvia de arriba hacia abajo, las palabras son: "PODRÍAS SER TÚ", "LLAMA AL 1355", "VÍCTIMA", en colores rosados. Esto busca tener una reflexión y denunciar estos hechos.
Para poder volver al inicio (pantalla advertencia) se debe apretar la tecla "a".

La regla de oro de este proyecto es "A mayor X, mayor visibilidad del texto y a la vez apagar el sonido”.

Referentes
* En redes sociales al aparecer un contenido fuerte, hay una advertencia y concentimiento de verlo.
* Ediciones de youtube el cual solo tiene imagen y sonido.

### DIAGRAMA DE FLUJO
<img width="1414" height="2000" alt="DIAGRAMA DE FLUJO" src="https://github.com/user-attachments/assets/7b23fd42-0d3c-465f-ae21-c06996b329ed" />

### CÓDIGO DE P5.JS
```
let estado = 0; // Variable que define en cual pantalla nos encontremos.
let iconoOjo;// variable de imagen png, ícono ojo.
let colorAlerta; // variable color triángulo de advertencia.
let captura; // variable para la WebCam.
let fontBold; // variable tipografía bold.
let fontRegular; // variable tipografía regular.
let fontLight; // variable tipografía light.
let mujer; // variable imagen jpg, mujer siendo víctima.
let tamanoTexto = 50; // Variable para animar el texto con map().
let llanto; // sonido mp3 llanto mujer.
let misTextos = []; // array vacio para guardar las particulas.
let palabras = ["LLAMA AL 1455", "PODRÍAS SER TÚ", "VÍCTIMA"]; // array para guardar las palabras.

function preload(){ // carga las imagenes, fonts y sonidos antes de empezar al programa. 
// imagenes cargadas.
  iconoOjo = loadImage('icono ojo.png');
  mujer = loadImage('víctima.jpg'); 

// tipgrafía StackSansHeadline y sus variables.
  fontBold = loadFont('StackSansHeadline-Bold.ttf');
  fontRegular = loadFont('StackSansHeadline-Regular.ttf');
  fontLight = loadFont('StackSansHeadline-Light.ttf');

// sonido mujer llorando.
  llanto = loadSound('llanto.mp3');
}

function setup() {
  createCanvas(windowWidth, windowHeight);// estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.
  textAlign(CENTER, CENTER); // alinea en texto al centro del canvas.
  colorAlerta = color(200, 0, 0); // valor asignado a la variable.
  captura = createCapture(VIDEO); // capturamos la cámara del computador.
  captura.size(windowWidth, windowHeight); // define tamaño de la captura de video.
  captura.hide(); // esconde el duplicado de HTML.

  function mousePressed(){ // función presionar el mouse.
   llanto.loop(); // audio infinito.
  }
// recorre cada palabra del array para crar su versión flotante.
  for (let i = 0; i < palabras.length; i++) { 
// elige una posición X al azar dejando un margen de 50 pixeles a los lados.    
    let x = random(50, width - 50);
    
    let y = random(-300, 0); // valores negativos para que las particulas o el texto flotante empiecen de arriba de la pantalla. 
    
    misTextos.push(new TextoFlotante(palabras[i], x, y)); // agrega un nuevo objeto TextoFlotante al array 'misTextos' con la palabra y su posición inicial.
  }
}
//se ejecuta automáticamente si el usuario estira o encoge la ventana.
function windowResized() { 
  resizeCanvas(windowWidth, windowHeight);
  captura.size(windowWidth, windowHeight);
}

function draw() {
  background(220);
  
// estructura que permite dibujar una cosa u otra en cada estado.
  switch (estado) { 
    case 0:
      pantallaAdvertencia();
      break;
    case 1:
      pantallaSensible();
      break;
    case 2:
      pantallaReflexion();
      break;
  }
}

// ==========================================
// ESTADO 0: PANTALLA ADVERTENCIA
// ==========================================
function pantallaAdvertencia() { // estado 1.
  background(0, 0 ,0);

if (frameCount % 10 === 0) { // condición la cual cambia el color solo una vez cada 10 fotogramas.
    colorAlerta = color(random(200, 255), random(0, 50), random(0, 50)); // Genera un color aleatorio con tonos predominantemente rojos (RGB).
  }
  // triangulo rojo de advertencia
  fill(colorAlerta); // Aplica el color intermitente generado arriba al triángulo.
  triangle(width / 2, height * 0.1, width / 2 - 150, height * 0.5, width / 2 + 150, height * 0.5); // triángulo de advertencia ubicado al centro horizontal y desplazada hacia arriba.

  imageMode(CENTER); // modo para posicionar desde el centro de la imagen.
image(iconoOjo, width / 2, height * 0.35, 180, 110); // imagen ojo tachado dentro del triángulo.
  imageMode(CORNER); // devolvemos a la normalidad para el resto del código.

  fill(250); // color del texto (blanco).
textFont(fontLight); // tipografía fuente delgada.
  textSize(14); // tamaño del texto.
  text("Presiona la tecla (w) para avanzar", width / 2, height * 0.9); // indicación de la tecla para interactuar.
  
  textFont(fontBold); // tipografía fuente negrita.
  textSize(45); // tamaño del texto.
  text("ADVERTENCIA", width / 2, height * 0.65); // palabra centrada en el ancho del canvas y desplazada hacia abajo en lo alto.

  textFont(fontRegular); // tipografía fuente normal.
  textSize(20); // tamaño del texto.
  text("Contenido sensible", width / 2, height * 0.73);   // subtítulo centrado en lo ancho y posicionado abajo.
}

// ==========================================
// ESTADO 1: PANTALLA SENSIBLE
// ==========================================
function pantallaSensible() { // estado 2.
  background(0);

//instrucciones 
  fill(250);
  textFont(fontLight);
  textSize(14);
// paso 1 centrado horizontalmente y abajo en el eje Y.
  text("1. Haz click en el lado izquierdo de la pantalla", width / 2, height * 0.82);
// paso 2 debajo de la primera instrucción.
  text("2. Mueve el mouse en X en dirección hacia la derecha", width / 2, height * 0.86);
   text("Presiona la tecla (d) para avanzar", width / 2, height * 0.9); // indicación de la tecla para interactuar.

   // Imagen responsiva: calcula un tamaño cuadrado adaptable.
  let tamanoImagen = min(width * 0.7, height * 0.5); // tamaño óptimo para que no sature la pantalla.
  imageMode(CENTER);
  image(mujer, width / 2, height * 0.4, tamanoImagen, tamanoImagen); 
  imageMode(CORNER); // devolvemos a la normalidad para el resto del código.

  // si el mouse pasa de la mitad de la pantalla (width / 2) y el audio está sonando:
if (mouseX > width / 2 && llanto.isPlaying()) {
  llanto.stop(); // se detiene el audio por completo.
}
  // tamaño de "BASTA" segun el min. y max. del lienzo.
  let minTam = map(width, 320, 1000, 25, 45);
  let maxTam = map(width, 320, 1000, 50, 80);
  tamanoTexto = map(mouseX, 0, width, minTam, maxTam);
  
  fill(255);
  textFont(fontBold); // tipografía fuente en negrita.
  textSize(tamanoTexto); // tamaño del texto dado por una variable.
  text("BASTA", width / 2, height * 0.4); // centrado sobre la imagen.
}
// controla la reproducción del sonido al hacer clic con el mouse.
function mousePressed(){
  
if (llanto.isPlaying()) {
    llanto.stop(); // si ya está sonando, lo detiene.
  } else {
    llanto.play(); // si está detenido, le da play.
  } 
}

// ==========================================
// ESTADO 2: PANTALLA DE REFLEXIÓN
// ==========================================
function pantallaReflexion() {

  image(captura, 0, 0, width, height); // dibujamos la captura de la cámara web abarcando todo el lienzo.
  
  fill(250); // color del texto (blanco).
  textFont(fontLight); // tipografía fuente delgada.
  textSize(14); // tamaño del texto.
  text("Presiona la tecla (a) para volver al inicio", width / 2, height * 0.9); // indicación de la tecla para interactuar.
  
  textFont(fontBold); // tipografía fuente en negrita.
// recorre y actualiza cada objeto de texto en el array.
   for (let i = 0; i < misTextos.length; i++) {
    misTextos[i].mover(); // actualiza la posición física del texto.
    misTextos[i].mostrar(); // muestra el texto en la pantalla.
  }
}

// estructura para crear textos animados que caen por la pantalla.
class TextoFlotante {
  constructor(miTexto, x, y) { // se ejecuta al crear cada objeto.
    this.txt = miTexto; // almacena la cadena de caracteres.             
    this.x = x; // Posición inicial en el eje X.                  
    this.y = y; // Posición inicial en el eje Y.                   
    
    // velocidad positiva para que sume a la Y y el texto baje.
    this.velY = random(2, 3); // velocidad de caída aleatoria entre 2 y 3 píxeles.
    this.color = color(255, random(14, 255), random(55, 255)); // color aleatorio dentro de tonos rosados/cálidos.
  }

  mover() { // actualiza la posición del texto para simular la caída.
    this.y += this.velY; // al sumar un número positivo, el objeto baja.
    
    //condicional de reinicio, si el texto supera el fondo de la pantalla (height).
    if (this.y > height + 30) {
      this.y = -30; // Reaparece justo arriba de la pantalla.
      this.x = random(50, width - 50); // Cambia de columna para variar su posición en X.
    }
  }

  mostrar() { // dibuja y estiliza el texto en el lienzo.
    fill(this.color); // asigna el color aleatorio guardado en el constructor.
    textSize(26); // tamaño de la fuente a 26 pixeles.
    textAlign(CENTER); // alinea el eje del texto al centro horizontal.
    text(this.txt, this.x, this.y); // dibuja las palabras seleccionadas en el lienzo segun coordenas, valores de ancho y alto definido por el tamaño.
    
  }
}
// ==========================================
// INTERACCIÓN Y NAVEGACIÓN POR TECLADO
// ==========================================
function keyPressed() { 
  if (key === 'a') estado = 0; // la letra "a" te lleva a la pantallaAdvertencia.
  if (key === 'w') estado = 1; // la letra "w" te lleva a la pantallaSensible.
  if (key === 'd') estado = 2; // la letra "d" te lleva a la pantallaReflexion.
} 
```
### LINK SKETCH EXAMEN P5.JS

[P5.js](https://editor.p5js.org/ThiareReyes/sketches/Z2bxgU-lH)


