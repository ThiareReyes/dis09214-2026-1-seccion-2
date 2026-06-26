

# "Supremacía de minorías"
## Katalina Ludueña y Clementine Flores

### Descripción objetiva
#### ¿Qué es el proyecto?
Nuestro proyecto representa en cómo en la actualidad y durante siglos, la supremacía del hombre (cis-hetero-opresores) ante las personas no hombres (mujeres, lesbianas, trans, no binares, etc).

#### ¿Qué se ve en pantalla?
Se ve la opresión, la incomodidad y la inseguridad que han causado y siguen causando los hombres cis-hetero/opresores a toda persona no hombre, y también se muestra un mundo ideal en el que no existe esta opresión y florece la libertad como un lugar seguro en donde puedes ser tu mismx. 
¿Qué elementos visuales aparecen?
*  Figuras geométricas representadas como las personas no hombres (mujeres, lesbianas, trans, no binaries, etc)
*  Símbolo de hombre (supremacía cis-hetero)
*  Frase dicha por Violeta Parra "Soy una hormiguita que busca bajo la tierra dónde poder refugiar su corazón", asociando "hormigas" como esta minoría no hombre.
*  Una imagen de un símbolo masculino y otra imagen de un lirio florecido.

#### Descripción conceptual
Nuestra idea central del proyecto y la relación con nuestro sistema diseñado, es demostrar la realidad actual y no actual, de cómo las personas no hombres son oprimidas. Nuestra regla de oro en el proyecto funciona de esta manera: Mientras el mouse esté presionado, persiste la supremacía y opresión, pero al soltarlo, las personas no hombres pueden florecer libremente en este mundo ideal, o conviviendo con las mismas personas no hombres. La lógica con nuestra problemática se relaciona directamente en representación desde nosotras, como personas no hombres oprimidas por la supremacía diariamente, en cómo nosotras lo hemos vivido, y en que sabemos cómo puede ser vivenciarlo desde primera fuente. 

#### Input / Output y sistema
¿Qué datos entran? (INPUT)
*  La posición del mouse (mouseX y mouseY), que determina dónde aparece el símbolo masculino.
*  La acción de presionar o soltar el mouse (mousePressed() y mouseReleased()), que cambia el estado de la variable opresion.
*  Las imágenes cargadas al inicio (simbolo masculino.png y fondo.jpeg).
*  Los valores aleatorios generados para cada figura, como su posición inicial, tamaño, velocidad, tipo y color.

#### Cómo se procesan y transforman?
Las figuras se desplazan según sus velocidades horizontal y vertical, cuando llegan a los bordes del lienzo, rebotan cambiando la dirección de su movimiento, se calcula la distancia entre cada figura y el símbolo masculino, si una figura se encuentra a menos de 200 píxeles del símbolo, se aleja de él y además presenta un pequeño temblor aleatorio, cuando se presiona el mouse, la variable opresion cambia a true, desaparece el símbolo masculino y se muestra una imagen de fondo. Cuando se suelta el mouse, opresion vuelve a false, reaparece el símbolo masculino y las figuras vuelven a reaccionar ante él. El color de las figuras también cambia según el estado de opresión: son grises cuando el símbolo masculino está presente y recuperan sus colores cuando desaparece.

#### Qué respuesta visual producen? (OUTPUT)
*  Las figuras se desplazan según sus velocidades horizontal y vertical. 
*  Cuando llegan a los bordes del lienzo, rebotan cambiando la dirección de su movimiento.
*  Se calcula la distancia entre cada figura y el símbolo masculino.
*  Si una figura se encuentra a menos de 200 píxeles del símbolo, se aleja de él y además presenta un pequeño temblor aleatorio.
*  Cuando se presiona el mouse, la variable opresion cambia a true, desaparece el símbolo masculino y se muestra una imagen de fondo.
*  Cuando se suelta el mouse, opresion vuelve a false, reaparece el símbolo masculino y las figuras vuelven a reaccionar ante él.
*  El color de las figuras también cambia según el estado de opresión: son grises cuando el símbolo masculino está presente y recuperan sus colores cuando desaparece.

#### Pensamiento computacional
Reglas que gobiernan el sistema (inputs, procesos, outputs)
#### Explicación del sistema de interactividad
La interactividad de este proyecto se basa en el uso del mouse como elemento de control. El usuario puede mover el cursor por la pantalla, haciendo que el símbolo masculino siga su posición. Este símbolo funciona como un agente de opresión, ya que las figuras que representan lo no hombre reaccionan a su cercanía alejándose de él.

El sistema responde a la acción de presionar y soltar el mouse. Cuando el usuario presiona el botón del mouse, la variable opresion cambia de estado, provocando que el símbolo masculino desaparezca, que el fondo se transforme en una imagen de una flor que florece y que las figuras recuperen sus colores vibrantes. Al soltar el mouse, el estado vuelve a la normalidad: reaparece el símbolo masculino, el fondo vuelve a ser gris y las figuras se muestran nuevamente en tonos grises mientras continúan reaccionando a la presencia del símbolo.

De esta manera, la interacción permite que el usuario altere directamente el comportamiento visual de la composición, generando un contraste entre dos estados: uno asociado a la opresión y otro asociado a la liberación. El movimiento del cursor y el clic del mouse son los mecanismos que activan estos cambios y construyen el significado de la obra.

#### Referentes
Listado y breve descripción de referentes visuales, teóricos o históricos.
• Diagrama de Flujo: (En el documento) 

• Código de p5.js (Agregado en formato MarkDown): 
```javascript
// almacena todas las figuras que representan lo no hombre
let noHombres = [];

// Variable que indica si existe o no opresión
let opresion = false;

// Variable para guardar la imagen del símbolo masculino
let simbolomasculino;

// Variables auxiliares utilizadas en los ciclos y cálculos
let i;
let s;
let d;

// Variable para guardar la imagen de fondo cuando el mouse es presionado
let fondo;

// Carga las imágenes antes de iniciar el programa
function preload() {
  simbolomasculino = loadImage("simbolo masculino.png");
  fondo = loadImage("fondo.jpeg");
}

function setup() {

  // Crea un lienzo de 800 x 600 píxeles
  createCanvas(800, 600);

  // Crea 200 figuras aleatorias
  for (i = 0; i < 200; i++) {

    // Agrega cada figura al arreglo
    noHombres.push({

      // Posición inicial aleatoria
      x: random(width),
      y: random(height),

      // Tamaño aleatorio
      size: random(20, 60),

      // Velocidad horizontal aleatoria
      vx: random(-2, 2),

      // Velocidad vertical aleatoria
      vy: random(-2, 2),

      // Tipos de figuras
      type: random(["ellipse", "rect", "triangle", "line"]),

      // Color aleatorio
      col: color(random(255), random(255), random(255)),
    });
  }
}

function draw() {

  // Si existe opresión aparece una imagen de fondo
  if (opresion) {
    image(fondo, 0, 0, width, height);
  }

  // Si no existe opresión aparece un fondo gris
  else {
    background(220);
  }

  // Configuración del texto
  fill(0);
  textSize(18);
  textAlign(LEFT, TOP);

  // Muestra la frase en pantalla
  text(
    "Soy una hormiguita que busca bajo la tierra donde poder refugiar su corazón - Violeta Parra.",
    150,
    10,
    290
  );

  // Si no hay opresión se muestra el símbolo masculino siguiendo al mouse
  if (!opresion) {
    image(simbolomasculino, mouseX, mouseY, 200, 200);
  }

  // Recorre todas las figuras del arreglo
  for (s of noHombres) {

    // Actualiza la posición según su velocidad
    s.x += s.vx;
    s.y += s.vy;

    // Rebota en los bordes izquierdo y derecho
    if (s.x < 0 || s.x > width) {
      s.vx *= -1;
    }

    // Rebota en los bordes superior e inferior
    if (s.y < 0 || s.y > height) {
      s.vy *= -1;
    }

    // Reacción de las figuras frente al símbolo masculino
    if (!opresion) {

      // Calcula la distancia entre la figura y el mouse
      d = dist(s.x, s.y, mouseX, mouseY);

      // Si la figura está cerca del símbolo
      if (d < 200) {

        // Se mueve alejándose horizontalmente
        if (s.x < mouseX) {
          s.x -= 3;
        } else {
          s.x += 3;
        }

        // Se mueve alejándose verticalmente
        if (s.y < mouseY) {
          s.y -= 3;
        } else {
          s.y += 3;
        }

        // Agrega un pequeño temblor al movimiento
        s.x += random(-2, 2);
        s.y += random(-2, 2);
      }
    }

    // Si no hay opresión las figuras recuperan su color
    if (!opresion) {
      fill(120);
    }

    // Si hay opresión las figuras se vuelven grises
    else {
      fill(s.col);
    }

    // Quita el borde de las figuras
    noStroke();

    // Dibuja una elipse
    if (s.type === "ellipse") {
      ellipse(s.x, s.y, s.size);
    }

    // Dibuja un rectángulo
    else if (s.type === "rect") {
      rectMode(CENTER);
      rect(s.x, s.y, s.size, s.size);
    }

    // Dibuja un triángulo
    else if (s.type === "triangle") {
      triangle(
        s.x,
        s.y - s.size / 2,
        s.x - s.size / 2,
        s.y + s.size / 2,
        s.x + s.size / 2,
        s.y + s.size / 2
      );
    }

    // Dibuja una X utilizando dos líneas
    else if (s.type === "line") {

      // Color de las líneas
      stroke(opresion ? s.col : 120);

      // Grosor de las líneas
      strokeWeight(3);

      // Primera diagonal
      line(
        s.x - s.size / 2,
        s.y - s.size / 2,
        s.x + s.size / 2,
        s.y + s.size / 2
      );

      // Segunda diagonal
      line(
        s.x + s.size / 2,
        s.y - s.size / 2,
        s.x - s.size / 2,
        s.y + s.size / 2
      );

      // Elimina el borde
      noStroke();
    }
  }
}

// Cuando se presiona el mouse desaparece el estado de opresión
function mousePressed() {
  opresion = true;
}

// Cuando se suelta el mouse aparece el estado de opresión
function mouseReleased() {
  opresion = false;
}
```


• Link al sketch en P5.js en formato EDITABLE. 
(https://editor.p5js.org/kataluduena/sketches/qvp6PsBBr) 
