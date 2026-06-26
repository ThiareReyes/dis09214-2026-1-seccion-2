# Solemne 02

# Repo solemne 2

---

# *Información del Proyecto*

## *Nombre del proyecto*  
Desigualdad de Género en la Política Chilena

## *Autores*  
Benjamin Ávila y Sara Graadt

---

# *Descripción Objetiva*

## *¿Qué es el proyecto?*

Es una visualización interactiva desarrollada en p5.js que representa *estadísticas reales sobre la representación femenina y masculina en distintos espacios de la política chilena durante 2024*. El proyecto busca evidenciar la notable baja participación del género femenino en cargos políticos y de toma de decisiones en Chile, mostrando cómo históricamente los hombres han ocupado la mayor parte de estos espacios de poder, representado a través de gráficos comparativos que permite observar de una manera clara la desigualdad de género presente en instituciones políticas como el Senado, la Cámara de Diputadas y Diputados y las alcaldías del país.

---

## *¿Qué se ve en pantalla?*

En la pantalla se observa una composición visual interactiva de un tamaño de 800x500 píxeles con una fotografía del Palacio de la Moneda de Chile con una pequeña trasnparencia y una mínima capa oscura para que se lea bien como fondo principal. A ambos lados aparecen ilustraciónes de figuras políticas femenina y masculina, mientras que en el centro se despliega un gráfico de barras comparativo que cambia mediante interacción del usuario.

Además, se visualizan sobres de votación animados que caen constantemente desde la parte superior de la pantalla, utilizando colores rojos y azules para simbolizar la desigualdad de representación política entre mujeres y hombres.

---

## *¿Qué elementos visuales aparecen?*

- Fotografía de fondo del Palacio de la Moneda de Chile.
- Ilustración de figura política femenina.
- Ilustración de figura política masculina.
- Panel central con gráficos de barras comparativos con datos verídicos del país.
- Sobres rojos y azules animados cayendo en pantalla.
- Título animado palpitante.
- Indicadores visuales de navegación.
- Textos explicativos y porcentajes.
- Textos con fuentes que confirman la información.

-----

# *Descripción Conceptual*

## *Idea central del proyecto y relación con el sistema diseñado*

Nuestro proyecto busca visibilizar la desigualdad de género en la política chilena mediante una traducción visual de estadísticas con porcentajes reales. El sistema convierte datos numéricos en relaciones visuales de tamaño, color, movimiento y cantidad.

Las barras comparativas permiten observar inmediatamente la diferencia entre representación masculina y femenina, mientras que la lluvia de los votos animados simbolizan la distribución desigual del poder político.

La interacción convierte la visualización en una experiencia dinámica que invita a reflexionar sobre la brecha de género en espacios importantes de toma de decisiones del país.

---

## *Regla de oro del sistema*

> “A mayor porcentaje masculino en el cargo político, mayor altura tendrá la barra azul y mayor cantidad de sobres azules aparecerán en pantalla.”

---

## *¿Cómo se relaciona esta lógica con la problemática de género?*

Cada componente visual representa directamente una desigualdad estructural existente en la política chilena.

- Los sobres azules predominan sobre los rojos para representar la mayor presencia masculina en los cargos políticos.
- La altura de las barras evidencia visualmente la diferencia de representación.
- El color de las barras femeninas cambia según el nivel de desigualdad:
  - Rojo fuerte → representación crítica
  - Rojo medio → representación baja
  - Rojo claro → acercamiento parcial a la paridad

De esta manera, el sistema no solo comunica datos, sino también genera una percepción visual de desequilibrio y desproporción al momento de representar las estadisticas analizadas.

---

# *Input / Output y Sistema*

## *¿Qué datos entran? (INPUT)*

- Clic del mouse del usuario.
- Posición horizontal del mouse (`mouseX`).
- Datos estadísticos reales sobre representación política.
- Contador de fotogramas (`frameCount`).

### *Datos utilizados*

| Institución | Mujeres | Hombres |
|---|---|---|
| Cámara de Diputadas/os | 35,5% | 64,5% |
| Senado | 24% | 76% |
| Alcaldías | 16,5% | 83,5% |
| Candidaturas Alcalde 2024 | 25% | 75% |

*Fuentes utilizada:* MinMujeryEG / CEPAL / El Mostrador 2024


---

## *¿Cómo se procesan y transforman?*

- `mousePressed()` cambia la estadística visualizada.
- `map()` transforma porcentajes en alturas visuales de barras.
- `random()` genera posiciones aleatorias para los sobres.
- `rotate()` aplica rotación dinámica a los votos en movimiento.
- `sin(frameCount)` genera pulsaciones suaves en el título.

---

## *¿Qué respuesta visual producen? (OUTPUT)*

- Cambio dinámico de gráficos comparativos.
- Modificación del color de las barras femeninas.
- Animación continua de votos cayendo.
- Título con efecto de pulso.
- Variación de brillo en textos interactivos
- Circulos inferiores de paginación.

---

# *Pensamiento Computacional*

## *Reglas que gobiernan el sistema*

| Elemento | Regla |
|---|---|
| Barras | `altura = map(porcentaje, 0, 100, 0, 160)` |
| Color barra mujer | Condicional según porcentaje |
| Votos | Nacen cada 4 frames |
| Color sobres | 15% rojos / 85% azul |
| Eliminación de votos | Se borran fuera de pantalla |
| Título | Pulso con `sin(frameCount)` |
| Brillo texto | `map(mouseX, 0, width, 120, 255)` |

---

## *Explicación del sistema de interactividad*

La interacción principal ocurre mediante clics del mouse en el rectangulo del centro. Cada clic cambia la categoría estadística visualizada mediante la variable `slideActual`.

Esto modifica:

- Altura de barras
- Porcentajes
- Colores
- Textos
- Datos visualizados

Además, el movimiento horizontal del mouse altera el brillo del texto inferior (Clic para cambiar estadística), generando una interacción secundaria bastante más sutil.

---

# *Referentes*

## *Referentes Visuales*

### *Barbara Kruger*
Artista visual feminista reconocida por utilizar tipografía, fotografía y mensajes políticos directos para cuestionar las estructuras de poder, el género y los medios de comunicación. Inspiró el uso de un contraste visual dentro del proyecto.

### *Wind Map*  
Visualización de corrientes de viento mediante partículas animadas, referente directo para el sistema de votos en movimiento.

### *Lotty Rosenfeld*
Artista chilena perteneciente a la Escena de Avanzada. Utilizó intervenciones urbanas y símbolos visuales para cuestionar el poder político y las estructuras patriarcales en Chile durante la dictadura. Referente por el uso del espacio visual como denuncia política.

---

## *Referentes Teóricos*

### *Feminism for the 99%*  
Texto sobre desigualdad estructural de género en sistemas políticos y económicos.

### *CEPAL*  
Fuente de datos estadísticos sobre igualdad de género en América Latina.

### *Ministerio de la Mujer y la Equidad de Género*  
Fuente oficial de indicadores de género utilizados en el proyecto.

### *Simone de Beauvoir*
Autora de “El segundo sexo”, obra fundamental para comprender la desigualdad histórica entre hombres y mujeres y la exclusión femenina en espacios de poder.

---

## *Referentes Históricos*

### *Sufragio femenino en Chile (1949)*  
Contexto histórico fundamental para comprender la representación política femenina en Chile.

## *Sufragistas chilenas*
Movimiento feminista que logró el derecho a voto femenino en elecciones presidenciales en Chile en 1949. Referente histórico clave para contextualizar la baja representación política femenina actual.

### *Revuelta feminista chilena de 2018*
Movimiento estudiantil y social que visibilizó masivamente desigualdades estructurales de género en Chile, utilizando performance, gráfica y activismo visual como herramientas de protesta. :contentReference[oaicite:1]{index=1}

### *CEPAL — Observatorio de Igualdad de Género*
Fuente oficial de estadísticas e investigaciones sobre participación política femenina en América Latina y Chile.

---

# *Diagrama de Flujo*
<img width="1024" height="1535" alt="image" src="https://github.com/user-attachments/assets/b9828e90-4ae7-47e6-ad84-a2c6f21c2d55" />

# *Imagen del boceto*

<img width="976" height="1446" alt="image" src="https://github.com/user-attachments/assets/737c8df7-22a6-4944-80d2-b8a3750e44ce" />

---

# *Código de p5.js*

```javascript
// ==============================================================
// DESIGUALDAD DE GÉNERO EN LA POLÍTICA CHILENA
// ==============================================================

// --- 1. NUESTRAS VARIABLES GLOBALES ---
// Las declaramos aquí arriba para que todo el programa las pueda leer y modificar.

let slideActual = 0; // Es el "número de página" actual. Controla cuál de las 4 estadísticas se muestra (0, 1, 2 o 3).
let imgFondo; // Caja vacía donde guardaremos la foto de La Moneda.
let imgMujer; // Caja vacía para la ilustración de la mujer.
let imgHombre; // Caja vacía para la ilustración del hombre.
let velocidadPulso = 0.03; // Qué tan rápido va a "latir" el tamaño del título principal.

// --- LISTAS (ARRAYS) PARA LA LLUVIA DE SOBRES ---
// Como caen muchos sobres a la vez, guardamos las propiedades de cada uno en listas independientes.
let votosX = []; // Guarda la posición horizontal (izquierda/derecha) de cada sobre.
let votosY = []; // Guarda la posición vertical (arriba/abajo) de cada sobre.
let votosGenero = []; // Guarda el color/género de cada sobre (0 para mujer, 1 para hombre).

// --- BASE DE DATOS DEL PROYECTO ---
// Guardamos la información real recopilada para que el gráfico la use de forma automática.
let categorias = [
  "Cámara de Diputadas/os",
  "Senado",
  "Alcaldías",
  "Candidaturas Alcalde 2024",
];
let porcentajeMujer = [35.5, 24, 16.5, 25]; // Alturas para la barra roja.
let porcentajeHombre = [64.5, 76, 83.5, 75]; // Alturas para la barra azul.

// ==============================================================
// FUNCIÓN PRELOAD: Precarga de archivos externos
// Le dice al computador que no arranque el programa hasta que estas imágenes web estén bien descargadas.
// ==============================================================
function preload() {
  imgFondo = loadImage(
    "https://upload.wikimedia.org/wikipedia/commons/9/9e/La_Moneda_vista_desde_Plaza_de_la_Constituci%C3%B3n.jpg"
  );
  imgMujer = loadImage(
    "https://media.istockphoto.com/id/584857500/es/vector/vector-ilustraci%C3%B3n-pol%C3%ADtica-mujer-dando-discurso.jpg?s=612x612&w=0&k=20&c=Y7sQlAPKUsJXivxdrYD4LRLfuT-d2oL8gQrKN_imZNs="
  );
  imgHombre = loadImage(
    "https://media.istockphoto.com/id/665421982/es/vector/rostrum-con-altavoz.jpg?s=612x612&w=0&k=20&c=EQ9dk-YlzEUcOYvlXcgZHVHdwTfAndgHxWlKA9xSSjU="
  );
}

// ==============================================================
// FUNCIÓN SETUP: Configuración inicial
// Se ejecuta una sola vez apenas se abre la página web. ==============================================================
function setup() {
  createCanvas(800, 500); // Define el tamaño de nuestra pantalla de juego (800 píxeles de ancho por 500 de alto).
  textFont("Arial"); // Configura el tipo de letra para todos los textos del proyecto.
}

// =============================================================
// FUNCIÓN DRAW: El motor de animación
// p5.js ejecuta este bloque en un bucle infinito (60 veces por segundo) para crear el movimiento.
// ==============================================================
function draw() {
  background(30); // Pinta el fondo gris oscuro. Sirve para "borrar" el fotograma anterior y que nada se vea borroso al moverse.

  // --- DIBUJO DE LA IMAGEN DE FONDO ---
  tint(255, 110); // Le da un toque de transparencia (capa del 43%) a la imagen que viene abajo.
  image(imgFondo, 0, 0, width, height); // Dibuja la foto de La Moneda estirada en todo el ancho y alto disponible.
  noTint(); // Desactiva la transparencia para que no afecte a los personajes ni a las barras.

  // --- MÁSCARA OSCURA DE CONTRASTE ---
  fill(0, 0, 0, 30); // Color negro muy suave y casi transparente.
  noStroke(); // Le quita el borde negro a la figura.
  rect(0, 0, width, height); // Dibuja un rectángulo gigante encima del fondo para que los textos blancos se lean bien.

  // --- ORDEN DE CAPAS (AQUÍ SE LOGRA LA PROFUNDIDAD) ---
  actualizarYDibujarVotos(); // Primero movemos y dibujamos los sobres (quedan al fondo, detrás de todo).
  dibujarPersonajes(); // Luego colocamos los contenedores de los políticos a los lados.
  dibujarBarras(); // Encima ponemos el cuadro estadístico central.

  // --- EFECTO VISUAL: TÍTULO QUE "LATE" ---
  // map() toma el conteo del tiempo transcurrido (frameCount), lo pasa por una onda senoidal y calcula un tamaño entre 19 y 24 píxeles.
  let tam = map(sin(frameCount * velocidadPulso), -1, 1, 19, 24);
  fill(255, 210, 50); // Color amarillo
  noStroke(); // que no tenga borde
  textSize(tam); // Aplica el tamaño dinámico que cambia en cada fotograma.
  textAlign(CENTER); // Centra el texto respecto a su posición.
  text("Desigualdad de Género en la Política Chilena", width / 2, 40);

  // --- LÍNEA ESTÁTICA DIVISORIA ---
  stroke(255, 210, 50, 160); // Borde dorado con un poco de transparencia.
  strokeWeight(1.5); // Define el grosor de la línea.
  line(0, 58, 800, 58); // Traza una línea horizontal justo debajo del título.

  // --- PIE DE PÁGINA INTERACTIVO ---
  // map() detecta dónde está tu mouse en el eje X (mouseX) y cambia el color del texto de azul oscuro a brillante.
  let brillo = map(mouseX, 0, width, 120, 255);
  fill(brillo, brillo, 255); // Genera un color azul dinámico reactivo al usuario.
  noStroke(); // sin borde
  textSize(12); // tamaño del texto
  textAlign(CENTER);
  // Muestra un mensaje interactivo con el número de página actual. Sumamos 1 porque la programación empieza en 0 (ej: muestra "1/4").
  text(
    "Clic para cambiar estadística (" +
      (slideActual + 1) +
      "/" +
      categorias.length +
      ")",
    width / 2,
    height - 15
  );
}

// ==============================================================
// FUNCIÓN PROPIA #1: Tarjetas laterales de personajes
// Separa el código para que draw() no se sature. Agregamos los marcos y las fotos de los políticos.
// ==============================================================
function dibujarPersonajes() {
  // ---- LADO IZQUIERDO: MUJER ----
  fill(212, 40, 40); // Fondo de la tarjeta en color rojo.
  noStroke(); // sin borde en el rectangulo
  rect(15, 100, 130, 165, 8); // Dibuja el rectángulo contenedor con bordes redondeados (radio 8).
  image(imgMujer, 22, 108, 115, 150); // Ajusta la ilustración de la mujer dentro del marco rojo.

  fill(235, 63, 63); // Color rojo claro para el texto.
  textSize(18); // tammaño del texto
  textAlign(CENTER); // Centra el texto respecto a su posición.
  text("Mujer en Política", 80, 282); // texto para el subtitulo de la categoria

  // Sistema protector de posiciones para animaciones aisladas
  push(); // Guarda la configuración original de la pantalla.
  translate(80, 90); // Mueve el centro del lienzo a la tarjeta de la mujer.
  rotate(frameCount * 0.01); // Genera un ángulo de rotación continuo basándose en el reloj del programa.
  scale(1.0); // Mantiene el tamaño real.
  pop(); // Borra los cambios anteriores para no arruinar la posición del resto

  // ---- LADO DERECHO: HOMBRE ----
  fill(34, 150, 243); // Fondo de la tarjeta en color azul.
  rect(655, 100, 130, 165, 8); // Marco del hombre figura rectangular.
  image(imgHombre, 662, 108, 115, 150); // foto del hombre en su casilla

  fill(100, 180, 255); // Color celeste para el texto.
  textSize(18); // tamaño de texto
  textAlign(CENTER); // Centra el texto respecto a su posición.
  text("Hombre en Política", 720, 282); // texto subcategoria "hombre en politica"

  // Sistema protector idéntico para el lado derecho
  push(); // Guarda la configuración original de la pantalla.
  translate(720, 90); // Mueve el centro del lienzo a la tarjeta de la mujer.
  rotate(frameCount * 0.01); // Genera un ángulo de rotación continuo basándose en el reloj del programa.
  scale(1.0); // Mantiene el tamaño real.
  pop(); // Borra los cambios anteriores para no arruinar la posición del resto
}

// ==============================================================
// FUNCIÓN PROPIA #2: Gráfico de barras central
// Controla el panel azul oscuro, las barras matemáticas y los puntitos indicadores.
// ==============================================================
function dibujarBarras() {
  let cx = width / 2; // Encuentra el centro exacto del lienzo en horizontal (cx = 400 píxeles).
  let baseY = 390; // Coordenada vertical que sirve de suelo o piso para sostener las barras.
  let alturaMax = 160; // El tamaño máximo en píxeles que alcanzará una barra si llega al 100%.

  // --- PANEL DE FONDO ---
  fill(15, 20, 50, 210); // Azul marino oscuro con un toque sutil de transparencia.
  stroke(200, 160, 40, 120); // Borde dorado suave.
  strokeWeight(1); // grosor de la linea
  rect(cx - 155, 165, 310, 245, 8); // Dibuja la caja central que aloja los gráficos.

  // --- TÍTULO DE LA ESTADÍSTICAS ---

  fill(255, 220, 80); // Texto color amarillo
  textSize(25); // tamaño del texto
  textAlign(CENTER); // Busca dinámicamente el nombre de la categoría correspondiente a la página que estamos mirando.
  text(categorias[slideActual], cx, 192); // texto que cambia segun estadisticas

  // --- TRADUCCIÓN MATEMÁTICA CON MAP() ---
  // Transforma los porcentajes reales (de 0 a 100%) a distancias físicas legibles por la pantalla (de 0 a 160 píxeles).
  let hM = map(porcentajeMujer[slideActual], 0, 100, 0, alturaMax);
  let hH = map(porcentajeHombre[slideActual], 0, 100, 0, alturaMax);

  // --- LÓGICA CONDICIONAL TRIPLE (REQUISITO EXPLICADO VISUALMENTE) ---
  // Cambia el tono de rojo de la barra femenina según qué tan baja y crítica sea su presencia en el poder.
  if (porcentajeMujer[slideActual] < 20) {
    fill(143, 6, 6); // Rojo fuerte: Representación crítica(caso Alcaldías).
  } else if (porcentajeMujer[slideActual] < 30) {
    fill(209, 42, 42); // Rojo medio: Representacion baja (caso Senado).
  } else {
    fill(247, 69, 69); // Rojo claro: Acercamiento parcial a la paridad (caso Diputados).
  }
  //  a la barra de las mujeres le restamos la altura recalculada (baseY - hM) porque en programación las pantallas se dibujan de arriba hacia abajo.
  rect(400 - 130, baseY - hM, 70, hM, 4, 4, 0, 0);
  // rect( X, Y, Ancho, Alto, esquina1, esquina2, esquina3, esquina4 );

  // --- BARRA DE LOS HOMBRES ---
  fill(60, 120, 220); // Color azul estándar para la representación masculina.
  rect(460, 269, 70, 121, 4, 4, 0, 0); // Dibuja la barra derecha de los hombres
  // rect( X, Y, Ancho, Alto, esquina1, esquina2, esquina3, esquina4 );

  // --- INDICADOR CENTRAL TRANGULAR ---
  fill(255, 210, 50); // Triángulo dorado que actúa como decoración estética en el suelo del gráfico.
  triangle(380, 400, 400, 380, 420, 400); // tamaño triangulo segun posiciones de los ejes

  // --- TEXTOS DE LOS PORCENTAJES EN VIVO ---
  fill(255); // Color blanco puro.
  textSize(17); // tamaño texto
  textAlign(CENTER); // Escribe los números actuales sumándoles el símbolo "%" flotando arriba de cada columna.
  text(porcentajeMujer[slideActual] + "%", cx - 95, baseY - hM - 8); //// Muestra el número (ej: "35.5%") centrado a la izquierda (cx-95) y flotando 8 píxeles arriba de la barra de mujeres (baseY - hM - 8)

  text(porcentajeHombre[slideActual] + "%", cx + 95, baseY - hH - 8); //Muestra el número (ej: "64.5%") centrado a la derecha (cx(400)+95) y flotando 8 píxeles arriba de la barra de hombres (baseY - hH - 8)

  // Etiquetas de los ejes
  textSize(16); // tamaño del texto
  fill(235, 63, 63); // color de texto rojo
  text("Mujeres", cx - 95, baseY + 16); // texto subtitulo de barra " mujeres"
  fill(100, 180, 255); // color de texto azul
  text("Hombres", cx + 95, baseY + 16); // texto subtitulo de barra "hombres"

  // Texto legal / Créditos de información
  fill(150, 150, 160); // color de texto (gris)
  textSize(9); // tamaño del texto
  text("Fuente: MinMujeryEG / CEPAL / El Mostrador 2024", cx, baseY + 32); // fuente pagina informativa donde encontramos los datos y la informacion

  // --- EL BUCLE FOR: Círculos inferiores de paginación ---
  // Recorre un ciclo que se repite tantas veces como estadísticas tengamos (4 vueltas). Agregamos los puntitos de navegación.
  for (let i = 0; i < categorias.length; i++) {
    // Si la vuelta del bucle concuerda con la página que el usuario está viendo...
    if (i === slideActual) {
      fill(255, 210, 50); // Pinta el puntito activo de color amarillo resplandeciente.
    } else {
      fill(100, 100, 100); // Deja los demás puntitos apagados en color gris.
    }

    // Dibujamos el círculo. Multiplicamos la variable del ciclo 'i' por 22 para ordenarlos en fila india sin que se amontonen.
    ellipse(cx - 30 + i * 22, baseY + 50, 10, 10);
  } //  un círculo de 10px separado por 22px del anterior para armar la fila de páginas

  // --- LÍNEA REGULADORA INFERIOR ---
  stroke(255, 210, 50); // color de la linea
  strokeWeight(1); // grosor de la linea
  line(160, height - 28, 640, height - 28); // pocicion de la linea en en canvas
}

// =============================================================
// FUNCIÓN MOUSEPRESSED: Evento de Interacción directa por clic
// Captura el clic físico en el mouse y reconfigura las variables de dibujo de inmediato.
// =============================================================
function mousePressed() {
  // Le suma 1 a la página actual. El operador de porcentaje (%) es un reiniciador automático:
  // Si la página llega a ser 4 (un dato que no existe), el sistema calcula el residuo matemático y lo devuelve limpiamente a 0.
  slideActual = (slideActual + 1) % categorias.length;
}

// =============================================================
// FUNCIÓN AUXILIAR DE PARTÍCULAS: Creador de sobres individuales
// ============================================================
function generarNuevoVoto(y) {
  votosX.push(random(width)); // Elige una posición horizontal al azar a lo largo del techo de la pantalla.
  votosY.push(y); // Posiciona la altura del voto en el inicio especificado (0).

  votosGenero.push(random(40) < 6 ? 0 : 1); // Esta línea de código se encarga de decidir si un voto que va cayendo por la pantalla será de mujer o de hombre, pero lo hace usando un truco de probabilidad para imitar la desigualdad de la realidad.
}

// =============================================================
// SISTEMA FÍSICO DE CAÍDA: Simulación dinámica de los sobres de votación
// =============================================================
function actualizarYDibujarVotos() {
  // Si el reloj interno del sistema determina que el fotograma actual es divisible por 4, da a luz un nuevo voto en el techo.
  if (frameCount % 4 === 0) {
    generarNuevoVoto(0);
  }

  // Recorremos la lista de votod de atrás hacia adelante. Esto evita que la pantalla parpadee o salte cuando borramos elementos.
  for (let i = votosY.length - 1; i >= 0; i--) {
    votosY[i] += 3; // Añade 3 píxeles hacia abajo en cada ciclo. Esto genera el efecto físico de velocidad de caída constante.

    push(); // Aísla los comandos de movimiento para que afecten únicamente a este sobre específico.
    translate(votosX[i], votosY[i]); // Mueve el centro de coordenadas del canvas justo encima del voto en su viaje.
    rotate(votosY[i] * 0.02); // Provoca un movimiento rotatorio orgánico simulando la resistencia del papel en el aire.

    // Comprueba el casillero de género guardado para decidir el color del voto.
    if (votosGenero[i] === 0) {
      fill(235, 63, 63); // Si es 0, pinta el sobre electoral de color Rojo (Mujer).
    } else {
      fill(34, 150, 243); // Si es 1, pinta el sobre electoral de color Azul (Hombre).
    }

    rectMode(CENTER); // Configura el motor para dibujar el rectángulo usando su centro exacto como eje guía.
    stroke(255, 150); // Añade un trazo blanco semi-transparente para simular los bordes del sobre de papel.
    rect(0, 0, 24, 16, 2); // Dibuja el sobre proporcional de votación (24 píxeles de ancho x 16 de alto con esquinas de 2px).
    line(-12, -4, 12, 4); // Traza la línea en diagonal simulando el doblez de la pestaña del sobre cerrado.
    pop(); // Restaura la pantalla a su estado por defecto para procesar la siguiente figura sin errores.

    // --- RECOLECTOR DE BASURA (OPTIMIZACIÓN DE MEMORIA RAM) ---
    // Si detectamos que un voto cruzó la frontera inferior de la pantalla (height)...
    if (votosY[i] > height) {
      // Usamos .splice() para eliminar permanentemente los registros de ese voto de las tres listas del sistema.
      // Si no hiciéramos esto, la lista crecería al infinito, consumiendo la memoria del PC hasta congelar el programa.
      votosX.splice(i, 1);
      votosY.splice(i, 1);
      votosGenero.splice(i, 1);
    }
  }
}

```
---
# *Link al sketch en P5.js en formato EDITABLE.*

https://editor.p5js.org/saragraadt/sketches/hANDK2uSp