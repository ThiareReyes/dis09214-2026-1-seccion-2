# sesión 011 - 19/06

AGREGAR SONIDO EN P5* loadSound
-
SUBIR EL SONIDO A P5

1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada
en la esquina superior izquierda del editor (debajo del botón de
Play). Esto abrirá el menú de archivos laterales.

2. Hacer clic en el icono de + o el menú desplegable junto a Files.

3. Seleccionar Upload file (Subir archivo).

4. Arrastrar el archivo de sonido.
Formatos recomendados: .mp3 o .wav

5. Recomendación: usar nombres de archivo cortos, en
minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

DECLARAR Y PRECARGAR EL SONIDO
function preload()

1. Creamos una variable global al inicio
del código para guardar nuestro
sonido.

2. Usamos la función function
preload() inicializamos nuestra
variable y cargamos el sonido con
loadSound()

ACTIVAR MI SONIDO

Le damos play al sonido en el function setup con:

nombreVariable.play();

Con esta instrucción, el sonido va a comenzar
cuando le demos play a nuestro sketch.

ejemplo: 
arreglar el marco de codigo luego

let miSonido;

function preload(){
  miSonido=loadSound("SONIDOS/beyonce.mp3");
}
function setup() {
  createCanvas(400, 400);
  frameRate(20);
  miSonido.play();
  
}

function draw() {
  background(random(255),random(255),random(255));
  textAlign(CENTER);
  textSize(80);
  fill(255);
  text("ENERGY",200,220);
}


control de sonido
-
Métodos de control de sonido:
-

nombreVariable.play() : Reproduce el sonido una vez.
nombreVariable.loop() : Reproduce el sonido en bucle infinito.
nombreVariable.stop() : Detiene el sonido por completo.
nombreVariable.pause() : Pausa el sonido en el segundo actual.

nombreVariable.setVolume(valor) : Modifica el volumen.
Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).
nombreVariable.rate(valor) : Modifica la velocidad de
reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más
grave) y 2.0 es el doble (suena más agudo).

Métodos de consulta o estados del sonido
-

nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.
nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().
nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().
nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).
nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).
nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0
y 1.0).
nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el
doble).

SÍNTESIS DE AUDIO
p5.sound()
-

COMPONENTES DE UN SINTETIZADOR BÁSICO
-
- El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas
de onda" que cambian el timbre del sonido:
• 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).
• 'triangle' (onda triangular: sonido intermedio).
• 'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los
80).
• 'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).
- La Frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor
frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).
- La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el
volumen. Va de 0.0 (silencio) a 1.0 (máximo).

links por revisar: (arreglar links)
https://learningsynths.ableton.com/
https://learningsynths.ableton.com/en/playground

ejemplo sintetizadort basico:


// VARIABLES GLOBALES 

let oscilador;           // variable para guardar los valores del objeto generador de señales de p5.sound
let sliderFreq, sliderAmp; // Variables para guardar los valores del slider Frecuencia y Amplitud
let tipoOnda = 'sine';   // String (cadena de texto) de control para identificar la forma de onda activa
let encendido = false;   // Variable booleana para el botón de encender y apagar

// Variables para interactuar con los elementos estructurales de la botonera HTML
let btnSine, btnTriangle, btnSawtooth, btnSquare; 
let btnPlay;                                      
let miFuente;            // Variable para guardar mi tipografía


// PRECARGA DE ASSETS 

function preload() {
  // precargamos nuestra font
  miFuente = loadFont('Cairo-ExtraLight.ttf');
}


// FUNCIÓN SETUP QUE SE EJECUTA UNA SOLA VEZ AL COMIENZO DEL SISTEMA

function setup() {
  createCanvas(600, 450); // Creamos un lienzo de tamaños  x y

  // LLamamos a nuestras funciones propias
  inyectarEstilosCSS();       
  inicializarOscilador();     
  crearSlidersInterfaz();     
  crearBotonesInterfaz();     
  
  // Modifica los estilos nativos de los elementos HTML que acabamos de crear
  estilarBotonesMinimales();  
}


// función Draw que se ejecuta 60 veces por segundo en loop
function draw() {
  background(0); // Pinta la pantalla de negro 

  // CAPTURA DE DATOS EN TIEMPO REAL (INPUTS)
  // En cada frame (60 veces por segundo) extraemos los valores numéricos de los sliders
  let f = sliderFreq.value(); // variable local para guardar el valor del slider Frecuencia medida en Hertz (Hz)
  let a = sliderAmp.value();  // variable local para guardar el valor del slider Amplitud  (0.0 a 1.0)

  // FLUJO DE DATOS HACIA SUB-SISTEMAS (PROCESAMIENTO Y OUTPUT)
  // Enviamos las variables locales 'f' y 'a' como argumentos a los módulos encargados
  // del audio, el texto y la geometría visual de la onda.
  actualizarSintetizador(f, a); 
  dibujartextosInterfaz(f, a);  
  dibujarOsciloscopio(f, a);    
}

// FUNCIONES PROPIAS

// Inyecta código CSS plano al DOM del navegador para anular la apariencia gris de fábrica
// de los sliders y darles colores personalizados.
function inyectarEstilosCSS() {
  createElement('style', `
    @font-face {
      font-family: 'CairoCustom';
      src: url('Cairo-ExtraLight.ttf');
    }
    input[type=range] {
      -webkit-appearance: none; /* Desactiva el diseño por defecto de Chrome/Safari */
      background: #333;          /* Canal o riel de la barra */
      height: 6px;
      border-radius: 3px;
    }
    input[type=range]::-webkit-slider-thumb {
      -webkit-appearance: none;
      background: #b39ddb;       /* El tirador circular se tiñe de Lila */
      height: 16px;
      width: 16px;
      border-radius: 50%;
      cursor: pointer;
    }
  `);
}

// Construye la instancia del oscilador puramente matemático en la memoria RAM
function inicializarOscilador() {
  oscilador = new p5.Oscillator('sine');
  oscilador.amp(0); // Forzamos volumen en 0 al nacer para respetar políticas del navegador
}

// Creación de los sliders
function crearSlidersInterfaz() {
  sliderFreq = createSlider(100, 1200, 440, 1);
  sliderFreq.position(40, 120);  
  sliderFreq.size(200); 

  sliderAmp = createSlider(0, 1, 0.2, 0.01);
  sliderAmp.position(40, 200);
  sliderAmp.size(200);
}

// Creación de botones 
function crearBotonesInterfaz() {
  btnSine = createButton('SENOIDAL');
  btnSine.position(40, 310);
  btnSine.mousePressed(() => cambiarOnda('sine'));

  btnTriangle = createButton('TRIANGULAR');
  btnTriangle.position(160, 310);
  btnTriangle.mousePressed(() => cambiarOnda('triangle'));

  btnSawtooth = createButton('SIERRA');
  btnSawtooth.position(290, 310);
  btnSawtooth.mousePressed(() => cambiarOnda('sawtooth'));

  btnSquare = createButton('CUADRADA');
  btnSquare.position(390, 310);
  btnSquare.mousePressed(() => cambiarOnda('square'));

  btnPlay = createButton('ENCENDER / APAGAR');
  btnPlay.position(40, 370);
  btnPlay.size(520, 42);
  btnPlay.mousePressed(alternarAudio);
}

// función encargada de actualizar los parámetros del motor de audio (Web Audio API)
function actualizarSintetizador(f, a) {
  oscilador.freq(f); // Modifica la velocidad del ciclo de la onda sinusoidal
  if (encendido) {
    // Si el sintetizador está activo, el volumen se vincula al slider en tiempo real.
    // Usamos una rampa temporal de 0.05 segundos para mitigar chasquidos eléctricos.
    oscilador.amp(a, 0.05); 
  }
}

// función para los textos 
function dibujartextosInterfaz(f, a) {
  noStroke(); 
  textFont(miFuente); 
  
  //título principal
  fill(255);
  textSize(33); 
  text("SINTETIZADOR MODULAR", 40, 55);

  // Frecuencia 
  textSize(20);
  fill(255, 255, 0); 
  text("FRECUENCIA  //  " + f + " Hz", 40, 105);
  
  // Amplitud
  fill(179, 157, 219); 
  text("AMPLITUD  //  " + floor(a * 100) + "%", 40, 185);

  // Tipo de onda
  fill(255, 0, 50); 
  text("TIPO DE ONDA", 40, 285);
  
  // Onda activa
  fill(150); 
  text("ACTIVA: ", 320, 285);
  fill(255); 
  text(tipoOnda.toUpperCase(), 385, 285);
}

// FUNCIÓN para dibujar las ondas
function dibujarOsciloscopio(f, a) {
  stroke(255, 0, 50);  // Configura el trazo en color Rojo 
  strokeWeight(2);     // Grosor de la linea
  noFill();            // Impide que la geometría intente cerrarse con un relleno interior
  
  beginShape(); // Abre el búfer de dibujo complejo por vértices continuos
  
  // Iteración horizontal: mapeamos píxeles de X (de la coordenada 320 a la 560)
  for (let x = 320; x < 560; x++) {
    // Convierte el píxel X a un valor en radianes (Ángulo trigonométrico).
    // El divisor (f / 120) escala la cantidad de ciclos visuales según los Hertz de los sliders.
    let angulo = map(x, 320, 560, 0, TWO_PI * (f / 120));
    let y = 160; // Configura la "línea base" u horizonte del osciloscopio en el eje vertical
    
    // FILTRO GEOMÉTRICO SEGÚN FORMA DE ONDA SELECCIONADA
    // Cada condicional altera la coordenada 'y' aplicando una fórmula trigonométrica o matemática pura,
    // escalada siempre por la amplitud 'a' para modificar el tamaño vertical de la curva.
    if (tipoOnda === 'sine') {
      y += sin(angulo) * (a * 45); // Onda Senoidal pura (Seno perfecto)
    } 
    else if (tipoOnda === 'triangle') {
      y += (abs((angulo % TWO_PI) - PI) - HALF_PI) * (a * 28); // Onda Triangular usando valores absolutos y restos
    } 
    else if (tipoOnda === 'sawtooth') {
      y += ((angulo % TWO_PI) / TWO_PI - 0.5) * (a * -75); // Onda Sierra usando un patrón lineal repetitivo rampeado
    } 
    else if (tipoOnda === 'square') {
      y += (sin(angulo) >= 0 ? 1 : -1) * (a * 45); // Onda Cuadrada: Binaria, salta drásticamente entre dos estados extremos
    }
    
    vertex(x, y); // Añade el punto calculado (X, Y) a la lista de vértices geométricos
  }
  
  endShape(); // Cierra y renderiza la línea continua final en la pantalla
}



// función que ejecuta el cambio físico de timbre en el oscilador digital
function cambiarOnda(nuevaOnda) {
  tipoOnda = nuevaOnda;
  oscilador.setType(tipoOnda); // El método nativo de p5 modifica la geometría de la onda
}

// Gestor maestro encargado del ciclo de vida del audio y los permisos del navegador
function alternarAudio() {
  // DESPERTAR SEGURO DEL NAVEGADOR
  // Si el AudioContext está suspendido, la interacción del clic actúa como permiso legal para reactivarlo
  if (getAudioContext().state !== 'running') {
    getAudioContext().resume();
  }

  // MÁQUINA DE ESTADOS (ON / OFF)
  if (!encendido) {
    oscilador.start(); // Inicia la oscilación eléctrica interna del oscilador
    oscilador.amp(sliderAmp.value(), 0.1); // Aplica volumen con un fundido (fade-in) suave de 100ms
    encendido = true;
    btnPlay.style('background-color', '#00ff66'); // Cambia el color del botón HTML a verde activo
    btnPlay.style('color', '#000000');
  } else {
    oscilador.amp(0, 0.1); // Desvanece el sonido a cero (fade-out) en 100ms para evitar transitorios bruscos
    
    // Retrasamos el apagado del motor del oscilador (.stop) para permitir que el fade-out se complete
    setTimeout(() => { oscilador.stop(); }, 100); 
    encendido = false;
    btnPlay.style('background-color', '#ff0032'); // Restaura el color del botón HTML a Rojo plano
    btnPlay.style('color', '#ffffff');
  }
}

// Inyecta estilos CSS inline a la botonera HTML para un look Flat Design minimalista
function estilarBotonesMinimales() {
  let botonesOnda = [btnSine, btnTriangle, btnSawtooth, btnSquare];
  
  botonesOnda.forEach(b => {
    b.style('background-color', '#8b7fff'); // Fondo sólido lila
    b.style('color', '#ffffff');
    b.style('border', 'none');              // Elimina los contornos grises por defecto
    b.style('border-radius', '3px');        // Suavizado sutil en las esquinas de los botones
    b.style('padding', '8px 16px');
    b.style('font-family', "'CairoCustom', sans-serif"); // Vincula la fuente tipográfica inyectada arriba
    b.style('font-size', '13px');
    b.style('letter-spacing', '0.5px');     
    b.style('cursor', 'pointer');           // Cambia el puntero al pasar sobre el elemento
  });

  // Estilos específicos para el botón maestro de Play/Stop
  btnPlay.style('background-color', '#ff7ff3'); // Inicializa en rosa pastel elegante
  btnPlay.style('color', '#ffffff');
  btnPlay.style('border', 'none');                
  btnPlay.style('border-radius', '3px');
  btnPlay.style('font-family', "'CairoCustom', sans-serif"); 
  btnPlay.style('font-size', '15px');
  btnPlay.style('letter-spacing', '0.5px');
  btnPlay.style('cursor', 'pointer');
}

video tutorial: https://learningsynths.ableton.com/
https://learningsynths.ableton.com/en/playground (arreglar link)
