# Solemne 02

# Repo solemne 2
# Solemne 2 pensamiento computacional

## Información del proyecto:

**Nombre del proyecto:** Nunca es suficiente 

**Autora:** Denisse Delgado  

---

# Descripción objetiva

## ¿Qué es el proyecto?
  * Este proyecto es una visualización interactiva realizada en p5.js que representa la presión estética y social ejercida principalmente sobre las mujeres. A través de imágenes, movimiento, texto y transformación visual, el sistema muestra cómo las expectativas externas pueden afectar la percepción de la identidad y del cuerpo.

---

## ¿Qué se ve en pantalla?

  * En pantalla aparecen dos figuras femeninas, una más grande y otra más pequeña y triste, conectadas mediante una flecha que representa una transformación progresiva.

  * El usuario puede interactuar moviendo el mouse horizontalmente, lo que modifica el comportamiento visual de los elementos.

  * También aparece una nube compuesta por palabras relacionadas con estándares de belleza y exigencias sociales, además de partículas y elementos gráficos ambientales.

---

## ¿Qué elementos visuales aparecen?

- Dos imágenes femeninas
- Palabras flotantes relacionadas con presión social estética principalmente
- Partículas en movimiento
- Círculos superpuestos que forman una nube visual
- Líneas y grillas decorativas
- Textos reflexivos
- Cambios de color en el fondo
- Movimiento y rotación dinámica

---

# Descripción conceptual

## Idea central del proyecto y relación con el sistema diseñado

  * La idea central del proyecto es representar cómo la presión estética externa puede modificar la percepción corporal y emocional de una persona, lo cúal está dirigido principalmente a mujeres.

  * El sistema utiliza la interacción del mouse como metáfora de la presión social: mientras más avanza el usuario hacia la derecha, mayor es la intensidad visual de las exigencias sociales, por eso cambia de color y distintas figuras se agrandan.

  * La transformación de las figuras, el aumento del ruido visual y el cambio de ambiente simbolizan cómo estas expectativas afectan la autoimagen.

---

## Regla de oro del sistema:

  * “A mayor presión social, mayor distorsión de la percepción corporal.”

Esta regla se traduce visualmente mediante:
- Reducción de una figura femenina
- Crecimiento de la segunda figura
- Intensificación del fondo
- Mayor presencia de palabras y ruido visual

---

## Relación con la problemática de género

   * El proyecto aborda la presión estética impuesta históricamente sobre las mujeres por medios de comunicación, redes sociales y estándares culturales.

   * Las palabras flotantes representan discursos repetitivos asociados a la apariencia física, juventud y perfección.

   * El sistema busca evidenciar cómo estas exigencias externas pueden alterar la percepción de la identidad y generar tensión emocional.

---

# Input / Output y sistema

## INPUT

- Los datos de entrada del sistema son:
    * Posición horizontal del mouse (`mouseX`)
    * Click del mouse (`mousePressed`)
    * Tiempo/frames (`frameCount`)

---

## Procesamiento

- El sistema procesa los datos utilizando:
    * Condicionales (`if / else`)
    * Mapeo de valores (`map()`)
    * Funciones matemáticas (`sin()`)
    * Escalado (`scale()`)
    * Rotación (`rotate()`)
    * Traducción (`translate()`)

- El valor de `mouseX` controla:
    * Escala de las imágenes
    * Intensidad del fondo
    * Tamaño del texto
    * Velocidad de rotación
    * Sensación de presión visual

---

## OUTPUT

- La respuesta visual del sistema incluye:
    * Cambio de tamaño de las figuras
    * Movimiento oscilatorio
    * Cambio de color del fondo
    * Aparición más intensa de palabras
    * Rotación de la nube visual
    * Ambiente dinámico mediante partículas

---

# Pensamiento computacional

## Reglas del sistema

### Input
El usuario interactúa mediante el movimiento del mouse.

### Procesos
El sistema interpreta la posición del mouse y transforma variables visuales usando:
- Condicionales
- Mapeos numéricos
- Funciones 
- Animación en tiempo real

### Output
El sistema genera cambios visuales que representan distintos niveles de presión emocional y estética.

---

## Explicación de la interactividad

- La interacción principal ocurre con el movimiento horizontal del mouse.

- Hacia la izquierda:
     * Ambiente más calmado
     * Menor presión visual
     * Figura principal más grande

- Hacia la derecha:
     * Fondo más intenso
     * Más ruido visual
     * Figura principal más pequeña
     * Mayor protagonismo de la figura secundaria

- El click del mouse también modifica aleatoriamente el color del fondo.

---

# Referentes

## Referentes visuales

### Barbara Kruger:
- Uso de texto como crítica social y cuestionamiento de los estándares impuestos sobre el cuerpo femenino.

### Jenny Holzer:
- Uso de frases y mensajes como elemento visual y político.

---

## Referentes conceptuales

### Presión estética y género
- El proyecto toma como referencia las problemáticas relacionadas con:
    * Estándares irreales de belleza
    * Autoimagen corporal
    * Influencia de redes sociales
    * Exigencias culturales hacia las mujeres

---

# Diagrama de flujo
<img width="1024" height="1536" alt="Flujo visual" src="https://github.com/user-attachments/assets/83446b40-0b83-499b-a763-2ff4b43a635b" />

# Código:

```
// Imágenes principales del proyecto
let mujerGrande; // Imagen “mujer grande” (Representa estado inicial o más fuerte)
// Funciona como punto de partida de la transformación visual causada por la presión social.
let mujerPequena; // Imagen “mujer pequeña” (Representa el efecto de la presión estética constante)

// Palabras dentro de la nube
let palabras = [
  // Lista frases o palabras que representan discursos sociales internalizados, exigencias estéticas repetitivas que afectan la autoimagen, generando una “voz externa” constante dentro del espacio visual.
  "Sé perfecta",
  "Más delgada",
  "Sin arrugas",
  "Más delicada",
  "Piel perfecta",
  "Cintura pequeña",
  "Simétrica",
  "Más bonita",
  "Más flaca",
  "Naiz perfecta",
  "Sempre joven",
  "Maquillada",
  "Cuerpo perfecto",
];

// Partículas ambientales que se mueven por el canvas
let particulas = []; // Contiene partículas que simulan “ruido visual” o ambiente nostálgico

// Variables propias
let presion = 0; // Nivel de presión (Derivado del mouse)

let colorFondo = 10; // Color del fondo dinámico según interacción con el mouse

let rotacionNube = 0; // Controla la rotación progresiva de la nube de palabras.

// Carga de imágenes
function preload() {
  // Carga de imágenes antes de iniciar el programa
  mujerGrande = loadImage("k1.png");

  mujerPequena = loadImage("k2.png");
}

// Configuración inicial
function setup() {
  createCanvas(600, 550);

  // Centra imágenes y texto para facilitar composición visual
  imageMode(CENTER);
  textAlign(CENTER, CENTER);

  noCursor(); // Oculta el cursor para una experiencia más inmersiva

  // Partículas que se mueven por el canvas
  for (let i = 0; i < 100; i++) {
    // Genera partículas aleatorias que caen verticalmente
    particulas.push({
      x: random(width), // Posición horizontal aleatoria
      y: random(height), // Posición vertical aleatoria
      size: random(1, 4), // Tamaño pequeño tipo polvo/ruido
      speed: random(0.2, 1), // Velocidad de caída
      alpha: random(20, 120), // Transparencia variable (Profundidad visual)
    });
  }
}

// Bucle principal
function draw() {
  actualizarPresion(); // Actualiza estado de presión según mouse
  background(colorFondo); // Fondo dinámico

  // Dibujo de capas visuales
  dibujarFondo(); // Grilla + ambiente
  dibujarParticulas(); // Partículas flotantes
  dibujarBurbuja(); // Nube/presión social
  dibujarTransformacion(); // Relación visual entre dos estados corporales
  dibujarTexto(); // Mensajes narrativos

  rotacionNube += map(mouseX, 0, width, 0.0005, 0.03); // Rotación progresiva de la nube de presión
}

// Cambia el fondo de color
function actualizarPresion() {
  // Convierte posición del mouse en un valor entre 0 y 1
  presion = map(mouseX, 0, width, 0, 1);
  // Cambia el color del fondo según la posición del mouse
  // Esto representa distintos niveles de tensión emocional

  // If/Else
  if (mouseX < width / 3) {
    colorFondo = color(10, 10, 18); // Más oscuro / Calmado
  } else if (mouseX < width / 1.5) {
    colorFondo = color(35, 10, 20); // Intermedio / Tensión
  } else {
    colorFondo = color(80, 0, 20); // Más intenso / Presión social alta
  }
}

// Transformación del tamaño de las imágenes
function dibujarTransformacion() {
  // Escala de la imagen grande (Se reduce con la presión social)
  let escalaGrande = map(mouseX, 0, width, 1, 0.25);

  // Escala de la imagen pequeña (Aumenta con la presión social)
  let escalaTriste = map(mouseX, 0, width, 0.15, 1);

  // Movimiento suave tipo “Respiración”
  let movimientoY = sin(frameCount * 0.03) * 8;

  // Mujer grande(Izquierda)
  push();

  translate(180, 360 + movimientoY);
  rotate(sin(frameCount * 0.02) * 0.03);
  scale(escalaGrande);
  tint(255, 230);
  image(mujerGrande, 0, 0, 160, 350);

  pop();

  // Flecha simbólica de transformación
  fill(255, 120, 140);
  noStroke();
  textSize(45);
  text("→", 320, 350);

  // Mujer triste(Derecha)
  push();
  translate(420, 310 - movimientoY);
  scale(escalaTriste);
  rotate(sin(frameCount * 0.04) * 0.02);
  image(mujerPequena, 0, 0, 220, 300);
  pop();
}

// Nube / Burbuja que se produce al sobrepensar debido a todo el estrés externo que las espectativas producen
function dibujarBurbuja() {
  // Nube de círculos aleatorios que representan ruido mental/social
  push();
  translate(390, 150);
  rotate(rotacionNube);
  noFill();

  for (let i = 0; i < 120; i++) {
    stroke(255, 35);

    ellipse(
      random(-70, 70),
      random(-70, 70),

      random(50, 70),
      random(50, 70)
    );
  }

  pop();

  // Círculos decorativos adicionales (Sensación de presión)
  noFill();
  stroke(255, 60);

  ellipse(250, 130, 20);
  ellipse(220, 155, 15);
  ellipse(202, 180, 10);
  ellipse(450, 260, 20);
  ellipse(460, 300, 15);
  ellipse(450, 330, 10);

  // Palabras(Representan las expectativas que comúnmente recaen sobre las mujeres) que se mueven
  push();
  for (let i = 0; i < palabras.length; i++) {
    fill(255, 160, 190);

    noStroke();

    // Random()
    let tamaño = map(mouseX, 0, width, 0, 16); // Tamaño de texto depende del mouse (Más presión = Más grande, visible, asfixiante)
    textSize(tamaño);

    // Movimiento ondulatorio de las palabras
    let x = 403 + sin(frameCount * 0.01 + i) * 100;
    let y = 90 + i * 10;

    textAlign(CENTER);
    text(palabras[i], x, y);
  }
  pop();
}

// Partículas
function dibujarParticulas() {
  for (let p of particulas) {
    noStroke();
    fill(255, p.alpha);

    ellipse(p.x, p.y, p.size); // Dibujar partículas
    p.y += p.speed; // Movimiento vertical constante

    if (p.y > height) {
      // Reinicio cuando sale del canvas
      p.y = 0;
    }
  }
}

// Fondo

function dibujarFondo() {
  // Grilla sútil que genera estructura visual

  for (let i = 0; i < width; i += 40) {
    stroke(255, 10);

    line(i, 0, i, height);

    line(0, i, width, i);
  }

  // Forma decorativa transparente tipo base
  noStroke();
  fill(255, 100, 150, 18);

  ellipse(width / 2.5, height - 20, 350, 30);
}

// Textos
function dibujarTexto() {
  noStroke();
  textAlign(LEFT); // Texto alineado a la izquierda (Mensaje interno)
  textSize(14);
  fill(255, 120, 140);

  text(
    "La presión no cambia quién eres,\nsolo distorsiona cómo te ves.",
    30,
    60
  );

  textAlign(RIGHT); // Texto alineado a la derecha (Mensaje de reflexión)
  text("Apaga el ruido exterior,\nsolo escúchate a ti.", 560, 500);

  // Líneas decorativas (Encuadre visual)
  stroke(255, 40);
  line(20, 40, 20, 80);
  line(570, 520, 570, 480);
}

// Interacción con el mouse
function mousePressed() {
  // Cambia el fondo de forma aleatoria al deslizar
  colorFondo = color(random(0, 40), 0, random(10, 30));
}
```

- Link a su Sketch en p5.js (con permiso de edición)
(https://editor.p5js.org/denisse.delgado2/sketches/5aRY-Q9a7)