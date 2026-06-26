# Sesión 10 - 19/06
# SONIDO EN P5.JS = loadSound()

1. Paso 1: Subir el sonido a p5:
- a) Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.
- b) Hacer clic en el icono de + o el menú desplegable junto a Files.
- c) Seleccionar Upload file (Subir archivo).
- d) Arrastrar el archivo de sonido. Formatos recomendados: .mp3 o .wav
- e) Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS
<img width="268" height="381" alt="1" src="https://github.com/user-attachments/assets/e21a22bc-4627-4843-876a-f954cb52837c" />

2. Paso 2: Declarar y precargar el sonido = function preload()
- a) Creamos una variable global al inicio del código para guardar nuestro sonido.
- b) Usamos la función function preload() inicializamos nuestra variable y cargamos el sonido con loadSound()
<img width="392" height="143" alt="1" src="https://github.com/user-attachments/assets/5c793bc8-936e-4d5d-ae7e-0a041ecbb256" />

3. Paso 3: Activar mi sonido
- Le damos play al sonido en el function setup con: nombreVariable.play();

- Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.

- Ej profe: (https://editor.p5js.org/PoliMujica/sketches/lGzqNdYKy)
<img width="495" height="348" alt="1" src="https://github.com/user-attachments/assets/4d9b9927-3c4d-46c7-aa8e-9e20b424cdd2" />

LO IDEAL ES ACTIVAR MI SONIDO CON UN MOUSEPRESSED
<img width="437" height="280" alt="1" src="https://github.com/user-attachments/assets/daf9bf5d-658a-49e6-ab19-2e6439058367" />

## ¿CÓMO CONTROLAR MI SONIDO?

Métodos de control de sonido
- nombreVariable.play() : Reproduce el sonido una vez.
- nombreVariable.loop() : Reproduce el sonido en bucle infinito.
- nombreVariable.stop() : Detiene el sonido por completo.
- nombreVariable.pause() : Pausa el sonido en el segundo actual.

- nombreVariable.setVolume(valor) : Modifica el volumen.
    * Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).
nombreVariable.rate(valor) : Modifica la velocidad de reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0 es el doble (suena más agudo).

Métodos de consulta o estados del sonido
- nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.
- nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().
- nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().
- nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).
- nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).
- nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0 y 1.0).
- nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el doble).

Ejemplos del desafío radio play / pause
- Beyonce (https://editor.p5js.org/PoliMujica/sketches/FyCvI7vbc)
- Piano: 
    * Sin optimizar: (https://editor.p5js.org/PoliMujica/sketches/J7Ke6QogL)
    * Optimizado: (https://editor.p5js.org/PoliMujica/sketches/LrtntncIA)
    * Teclado clásico: (https://editor.p5js.org/PoliMujica/sketches/UDQ92bgRn)

### SÍNTESIS DE AUDIO p5.sound()

3 Componentes de un sintetizador básico
- El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas de onda" que cambian el timbre del sonido:
    * 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).
    * 'triangle' (onda triangular: sonido intermedio).
    * 'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los
80).
    * 'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).
- La Frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).
- La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el volumen. Va de 0.0 (silencio) a 1.0 (máximo).

- Ejemplo sintetizador básico: (https://editor.p5js.org/PoliMujica/sketches/FhD6y43H7)
<img width="417" height="303" alt="1" src="https://github.com/user-attachments/assets/a231d4cc-7e4e-4768-9f6a-12d872152c55" />

- Tutoriales de sonido: (https://www.youtube.com/playlist?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
