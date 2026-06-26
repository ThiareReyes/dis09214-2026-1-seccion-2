

# SOLEMNE 2
---

## Contador de Ausencias

### AUTOR
Tomás Jorquera

##### HERRAMIENTA UTILIZADA
> p5.js

---

## DESCRIPCIÓN DEL PROYECTO

Es un sketch interactivo codificado en p5.js que busca representar la violencia, invisibilización y marginalizacion de personas trans a traves de un sistema visual que tiene un contador, fechas flotantes y imágenes parpadeantes. En pantalla hay un fondo negro junto a un contador rojo ubicado en el centro, el cual aumenta automáticamente con el paso del tiempo. Alrededor del contador aparecen fechas flotantes mientras imágenes del pride y la memoria visual trans aparecen y desaparecen constantemente. Además, el mouse deja un rastro con los colores de la bandera trans cambiando de color y recuperando visibilidad.

---

## EL CONCEPTO

La idea del proyecto es representar cómo muchas de las muertes de personas trans terminan siendo invisibilizadas por completo con el paso del tiempo. El sistema fue diseñado para funcionar como un memorial interactivo donde las fechas representan vidas perdidas y el contador simboliza la continuidad constante de la violencia. La lógica principal del proyecto se basa en que mientras más cerca está el usuario de las fechas, mayor visibilidad y color recuperan, representando la memoria, atención y reconocimiento social. Cuando nadie interactúa con ellas, las fechas son grises y apagadas, representando la ausencia y olvido. Además, el contador aumenta constantemente para reflejar que esta problemática continúa ocurriendo en el presente y no es algp del pasado.

---

## REGLAS DE ORO

> Mientras más cerca está el usuario de las fechas, mayor visibilidad y color recuperan.

También:

> Cada cierto tiempo el contador aumenta automáticamente y el sistema genera nuevas ausencias.”

---

## INPUT/OUTPUT

El sistema recibe distintos datos de entrada como la posición del mouse mediante `mouseX` y `mouseY`, el tiempo utilizando `millis()`, la cantidad de frames mediante `frameCount` y los clicks realizados por el usuario utilizando `mousePressed()`. Estos datos son procesados constantemente para calcular distancias, tiempos y posiciones aleatorias generadas con `random()`. El sistema transforma la información en respuestas visuales como cambios de color, movimiento de las fechas, aparición de nuevas fechas, flashes rojos, rotaciones del contador, transparencias, escalas dinámicas e imágenes intermitentes. Como resultado, el sketch genera una experiencia visual donde el usuario modifica temporalmente la visibilidad y comportamiento de los elementos presentes en pantalla.

### INPUT
- Movimiento del mouse (`mouseX`, `mouseY`)
- Tiempo (`millis()`)
- Frames del programa (`frameCount`)
- Clicks del mouse (`mousePressed()`)

### OUTPUT
- Fechas interactivas.
- Cambios visuales según proximidad.
- Imágenes intermitentes.
- Movimiento constante.
- Flash rojo.
- Rastro del mouse.
- Contador dinámico.

---

## PENSAMIENTO COMPUTACIONAL

Cuando el mouse se acerca a una fecha, esta cambia de color utilizando tonos de la bandera trans. Cuando transcurre cierta cantidad de tiempo, el contador aumenta automáticamente, aparece un flash rojo y se genera una nueva fecha en una posición aleatoria. Si una fecha pierde toda su duración, desaparece y es reemplazada por otra nueva. Además, el rastro del mouse mantiene una cantidad limitada de puntos para evitar que el sistema acumule información infinita. La interacción principal ocurre mediante el movimiento del mouse, permitiendo que el usuario participe activamente del memorial digital al modificar la visibilidad de las “ausencias” representadas en pantalla. El proyecto utiliza distintas herramientas de p5.js como `random()`, `map()`, `push()`, `pop()`, `translate()`, `rotate()`, `scale()` y estructuras condicionales y repetitivas que permiten construir el sistema visual e interactivo completo.

### REGLAS DEL SISTEMA

- Si el mouse se acerca a una fecha:
  - La fecha cambia de color.
- Si pasa cierta cantidad de tiempo:
  - El contador aumenta.
  - Se activa un flash rojo.
  - Se genera una nueva fecha.
- Si una fecha pierde su vida:
  - Desaparece.
  - Se reemplaza por otra nueva.
- Si el trail del mouse supera el límite:
  - Se eliminan puntos antiguos.

---
 
## LINK P5.JS
https://editor.p5js.org/tomas1000000/sketches/Wog50zU3M

---

## REFERENTES VISUALES
<img width="735" height="490" alt="NEW MERCAT FONT SET - Toormix Design Agency" src="https://github.com/user-attachments/assets/fa4d055d-c818-4102-a96e-db74143a00e6" />
<img width="736" height="736" alt="Monobotics – Alphamark™" src="https://github.com/user-attachments/assets/5766591d-ec4c-41d1-9df8-0fcad344612d" />
<img width="736" height="906" alt=" " src="https://github.com/user-attachments/assets/379a1f4c-40e7-49ba-9bad-b31bece6efd2" />

Esta composición se inspira en la estética técnica de las interfaces de sistemas con el activismo político, tratando los datos de decesos como si fueran registros de error en una pantalla de computadora. Al utilizar una disposición saturada propia del diseño de terminales de comandos, la pieza transforma la memoria histórica en una interfaz fría y urgente, donde el contraste entre el archivo fotográfico en blanco y negro y el rojo vibrante del "contador" funciona como una señal de advertencia crítica, revelando la deshumanización de las estadísticas frente a la realidad de la violencia.

---

### DIAGRAMA DE FLUJO

<img width="2662" height="6008" alt="Sin título" src="https://github.com/user-attachments/assets/ff63370b-5a00-4eb0-8843-e45dc288a344" />


---

### CODIGO

```
// VARIABLES
let contador = 281; // contador inicial, guarda el momento en que el contador debe aumentar otra vez.
let tiempoCambio = 0; // tiempo para cambiar contador, guarda posiciones anteriores del mouse.
let nombres = []; // array fechas, guarda todos los objetos flotando.
let trail = []; // array trail mouse, guarda posiciones anteriores del mouse.

// FECHAS DE NACIMIENTO
let textos = [
  //variable fechas
  " † 03•09•2023", //fecha 1
  " † 12•04•2024", //fecha 2
  " † 23•05•2020", //fecha 3
  " † 31•06•2025", //fecha 4
  " † 07•08•2024", //fecha 5
  " † 26•12•2025", //fecha 6
  " † 09•01•2023", //fecha 7
  " † 17•02•2021", //fecha 8
  " † 04•08•2020", //fecha 9
  " † 02•02•2022", //fecha 10
];

let flash = 0; // variable flash rojo

// IMAGENES
let img1; // guarda las imagenes cargadas
let img2; // guarda las imagenes cargadas
let img3; // guarda las imagenes cargadas
let img4; // guarda las imagenes cargadas
let img5; // guarda las imagenes cargadas

// PRECARGA DE IMAGENES
function preload() {
  // cargar todas las imágenes
  img1 = loadImage("img1.png"); // carga la imagen 1
  img2 = loadImage("img2.png"); // carga la imagen 2
  img3 = loadImage("img3.jpg"); // carga la imagen 3
  img4 = loadImage("img4.png"); // carga la imagen 4
  img5 = loadImage("img5.png"); // carga la imagen 5
}

// SETUP
function setup() {
  createCanvas(500, 500); // tamaño del lienzo (500 x 500)
  textFont("Verdana"); // tipografia Verdana para todo el texto
  textAlign(CENTER, CENTER); // alinea todo el texto del canvas al centro
  for (let i = 0; i < 10; i++) {
    crearNombre(); // crear nombres iniciales
  }
  tiempoCambio = millis() + random(1000, 3000);
} // definicion de medicion de tiempo a milisegundos y entrega un numero aleatorio

// DRAW
function draw() {
  // función que se ejecuta una sola vez al inicio
  background(0, 40); // fondo negro

  // IMÁGENES PARPADEANTES
  // IMAGEN 1
  if (frameCount % 90 < 35) {
    // hace aparecer la imagen solo en algunos frames.
    tint(255, 70); // añade transparencia a la imagen
    image(img1, 10, 10, 220, 150); // tamaño y posicion de la imagen
  }

  // IMAGEN 2
  if (frameCount % 120 < 40) {
    // hace aparecer la imagen solo en algunos frames.
    tint(255, 70); // añade transparencia a la imagen
    image(img2, 260, 20, 220, 150); // tamaño y posicion de la imagen
  }

  // IMAGEN 3
  if (frameCount % 150 < 35) {
    // hace aparecer la imagen solo en algunos frames.
    tint(255, 70); // añade transparencia a la imagen
    image(img3, 80, 150, 250, 170); // tamaño y posicion de la imagen
  }

  // IMAGEN 4
  if (frameCount % 180 < 40) {
    // hace aparecer la imagen solo en algunos frames.
    tint(255, 70); // añade transparencia a la imagen
    image(img4, 220, 250, 240, 160); // tamaño y posicion de la imagen
  }

  // IMAGEN 5
  if (frameCount % 210 < 35) {
    // hace aparecer la imagen solo en  algunos frames.
    tint(255, 70); // añade transparencia a la imagen
    image(img5, 20, 320, 220, 150); // tamaño y posicion de la imagen
  }
  noTint(); // elimina la transparencia para las demas imagenes

  // FLASH ROJO
  if (flash > 0) {
    // si flash es visible
    fill(255, 0, 0, flash); // color rojo transparente
    noStroke(); // quitar borde del flash

    rect(0, 0, width, height); // rectángulo pantalla completa
    flash = flash - 8; // disminuir flash
  }

  // RASTRO DEL MOUSE
  trail.push({
    // agrega un anueva posicion al array trail
    // guardar posición mouse
    x: mouseX, // posicion x del mouse
    y: mouseY, // posicion y del mouse
  });

  if (trail.length > 20) {
    // limitar el tamaño de rastro tamaño trail
    trail.shift(); // elimina el primer elemento del array para que no sea infinito
  }

  for (let i = 0; i < trail.length; i++) {
    // recorre todos los puntos guardados dentro del trail
    let p = trail[i]; // guardar punto actual

    // colores bandera trans
    if (i % 3 == 0) {
      fill(91, 206, 250, 120); // rellena con color rosado transparente
    } else if (i % 3 == 1) {
      fill(245, 169, 184, 120); // rellenar con rosado claro transparente
    } else {
      fill(255, 255, 255, 120); // rellena con blanco transparente
    }

    noStroke(); // quitar borde
    circle(p.x, p.y, 10); // dibujar círculo usando posicion x, y y tamaño
  }

  // FECHAS
  for (let i = 0; i < nombres.length; i++) {
    // repasar todas las fechas guardadas
    let n = nombres[i]; // guardar la fecha actual
    n.y = n.y + sin(frameCount * 0.02 + n.offset) * 0.2; // mover suavemente la fecha actual en forma de seno
    let d = dist(mouseX, mouseY, n.x, n.y); // calcula la distancia entre la fecha y el mouse

    if (d < 80) {
      // si la fecha esta cerca del mouse se activan

      if (n.color == 0) {
        // si el color random es 0
        fill(91, 206, 250); // rellena con color azul claro
      } else if (n.color == 1) {
        // si el color random es 1
        fill(245, 169, 184); // rellena con color rosado claro
      } else {
        // en cualquier otro caso
        fill(255); // rellena con color blanco
      }
    } else {
      // en cualquier otro caso
      fill(150); // rellena con color gris
    }
    noStroke(); // quita el borde del texto
    textSize(n.size); // define el tamaño texto
    text(n.texto, n.x, n.y); // dibuja los nombres

    n.vida--; // dsiminuir la duracion de la vida de la fecha

    if (n.vida < 0) {
      // si la duracion de vida de la fecha termina reemplazar por una nueva
      nombres[i] = nuevoNombre(); // reemplazar por una fecha nueva
    }
  }

  // CONTADOR
  fill(220, 20, 20); // color rojo de los numeros del contador
  noStroke(); // sin borde para el contador
  let tamañoContador = map(mouseX, 0, width, 55, 85); // define el tamaño para el texto de el contador
  textSize(tamañoContador); // define eltamaño del contador
  push(); // guarda las transformaciones para que no afecten a otros elementos
  translate(width / 2, height / 2); // mueve el punto de origen al centro del canvas
  scale(1); // aplica escala de tamaño normal al contador
  rotate(sin(frameCount * 0.02) * 0.02); // rota suavemente el contador usando una funcion seno
  fill(220, 20, 20); // rellena con color negro
  textSize(tamañoContador); // define el tamaño del contador con la variable
  text(contador, 0, 0); // dibujar el contador en la posicion 0,0
  pop(); // restaura las transformaciones para que rotate y translate no afecten el resto del código
  
  // RECUADRO TEXTO SUPERIOR
  noStroke(); // quitar borde del recuadro superior
  fill(0, 180); // rellena de color negro del recuadro
  rect(width / 2 - 120, 8, 240, 24); // dibuja el rectangulo detras del texto superior

  // TEXTO SUPERIOR
  fill(220, 20, 20); // rellena con color rojo el recuadro
  textSize(15); // define el tamaño del texto
  text("CONTADOR DE DECESOS", width / 2, 20); // dibuja el texto superior

  // RECUADRO TEXTO INFERIOR
  noStroke(); // quitar borde
  fill(0, 180); // color negro
  rect(width / 2 - 100, height - 32, 200, 24); // dibuja el rectangulo detras del texto inferior

  // TEXTO INFERIOR
  fill(220, 20, 20); // color rojo
  textSize(10); // define el tamaño del texto
  text("TRANS LIVES MATTER", width / 2, height - 20); // dibuja el texto inferior

  // CONTADOR DE VIDAS
  if (millis() > tiempoCambio) {
    // si ya pasó el tiempo
    contador++; // aumentar el numero del contador
    flash = 120; // activar flash rojo al cambiar el numero
    crearNombre(); // crear fecha nueva
    tiempoCambio = millis() + random(1000, 4000); // nuevo tiempo random
  }
}

// NOMBRES
function crearNombre() {
  // array fechas
  nombres.push(nuevoNombre()); // agrega una fecha al array fecha
}

// NUEVO NOMBRE
function nuevoNombre() {
  // funcion que genera una fecha random y define la posicion de las fechas
  return {
    texto: random(textos), // genera un texto random
    x: random(width), // genera una posición random X
    y: random(height), // genera una posición random Y
    size: random(10, 18), // genera un tamaño random
    vida: random(300, 700), // genera una duracion random
    offset: random(100), // genera un movimiento random
    color: floor(random(3)), // genera un color random
  };
}

function mousePressed() {
  // funcion que se activa al presionar click
  crearNombre(); // crear una fecha extra
}
´´´

