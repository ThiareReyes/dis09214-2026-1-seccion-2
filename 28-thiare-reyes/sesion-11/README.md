# DISEÑO RESPONSIVO (windowResized)

**PASO 1**

CREAR UN CANVAS CON DIMENSIONES DINÁMICAS
* Para esto usaremos las variables integradas en el sistema:
(windowWidth, windowHeight) estas variables leen constantemente
el ancho y alto disponibles de la ventana del navegador.

<img width="842" height="172" alt="Captura de pantalla 2026-06-26 051311" src="https://github.com/user-attachments/assets/f760abb5-f144-4ce8-a080-bb82f9165e35" />

**PASO 2**

CREAR UN EVENTO windowResized()

* Si el usuario estira o encoge la ventana del navegador, el lienzo se
adaptará al tamaño de la ventana en tiempo real.

<img width="805" height="166" alt="Captura de pantalla 2026-06-26 051416" src="https://github.com/user-attachments/assets/13a12fac-ca32-4c2d-867e-4398196ccfe5" />

**PASO 3**

USAR VALORES RELATIVOS

* Ahora p5.js actualiza estas variables width y
height automáticamente con el tamaño actual
del lienzo.

Entonces ahora todos los valores de posición y
tamaño que ocupemos los tenemos que pensar
en relación proporcional a esas variables.

Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)

<img width="432" height="410" alt="Captura de pantalla 2026-06-26 051606" src="https://github.com/user-attachments/assets/8c100acf-67e7-4fc9-8c00-f127636fec8a" />

**PASO 4**

INCLUIR UN FACTOR DE REFERENCIA
referencia = min(width, height)

* Creamos una variable global
(referencia) y la asignamos para
que calcule el mínimo.

Observa el ancho y el alto de la
ventana, los compara, y se queda
solo con el que sea más pequeño
en ese momento.

<img width="452" height="382" alt="Captura de pantalla 2026-06-26 051821" src="https://github.com/user-attachments/assets/6e25cbcf-4a8b-4547-ab32-09d9022f2dd1" />

PASO 5

USAR TRANSLATE - PUSH Y POP
Consejo para proyectos complejos

* En lugar de hacer matemáticas
complejas en cada rect() o
ellipse(), usamos translate()
para "mover el origen del mundo”.

Y siempre utilizando push() y
pop() para cada figura o
elemento.

<img width="462" height="377" alt="Captura de pantalla 2026-06-26 051937" src="https://github.com/user-attachments/assets/64c93bea-9515-4a96-aff5-a3aedb4faff1" />

### AGREGAR IMÁGENES
loadImage()

**PASO 1**

SUBIR LA IMAGEN A P5
* 1. Hacer clic en la pequeña flecha hacia la derecha (>)
ubicada en la esquina superior izquierda del editor
(debajo del botón de Play). Esto abrirá el menú de
archivos laterales.

* 2. Hacer clic en el icono de + o el menú desplegable junto a
Files.

* 3. Seleccionar Upload file (Subir archivo).

* 4. Arrastrar la imagen o buscarla en el computador.

* 5. Recomendación: usar nombres de archivo cortos, en
minúsculas y sin espacios. Hacer una carpeta llamada
ASSETS.

**PASO 2**
DECLARAR Y PRECARGAR LA IMAGEN
function preload()

* 1. Creamos una variable global al
inicio del código para guardar la
imagen.

* 2. Usamos la función dentro de
function preload() y cargamos la
imagen con loadImage()

<img width="452" height="237" alt="Captura de pantalla 2026-06-26 052545" src="https://github.com/user-attachments/assets/69113aec-dc18-410e-8631-481da641a069" />

**PASO 3**

DIBUJAR Y DIMENSIONAR EN EL DRAW

* La imagen se dibuja usando la función image()

Esta función requiere mínimo 3 argumentos, pero
acepta 5 si queremos controlar su tamaño de
forma responsiva.

- SINTAXIS:

image(nombreVariableImagen, x, y, ancho, alto);

<img width="432" height="426" alt="Captura de pantalla 2026-06-26 052732" src="https://github.com/user-attachments/assets/e0a9bbf7-4635-48cd-a834-040ed0ec362d" />

## SONIDO EN p5.js
loadSound()

**PASO 1**

SUBIR SUS SONIDOS A P5

1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada
en la esquina superior izquierda del editor (debajo del botón de
Play). Esto abrirá el menú de archivos laterales.

2. Hacer clic en el icono de + o el menú desplegable junto a Files.

3. Seleccionar Upload file (Subir archivo).

4. Arrastrar el archivo de sonido.
Formatos recomendados: .mp3 o .wav

5. Recomendación: usar nombres de archivo cortos, en
minúsculas y sin espacios. Hacer una carpeta llamada ASSETS.

**PASO 2**

DECLARAR Y PRECARGAR EL SONIDO
function preload()

1. Creamos una variable global al inicio
del código para guardar nuestro
sonido.

2. Usamos la función function
preload() inicializamos nuestra
variable y cargamos el sonido con
loadSound()

<img width="428" height="193" alt="Captura de pantalla 2026-06-26 052952" src="https://github.com/user-attachments/assets/e7e958b7-2beb-4e52-b514-0ed02e36bffc" />

**PASO 3**

ACTIVAR MI SONIDO

Le damos play al sonido en el function setup con:

nombreVariable.play();

* Con esta instrucción, el sonido va a comenzar
cuando le demos play a nuestro sketch.

<img width="433" height="337" alt="Captura de pantalla 2026-06-26 053106" src="https://github.com/user-attachments/assets/de32b709-8cba-41a9-9448-b08f2e66f52b" />

**LO IDEAL ES ACTIVAR MI SONIDO CON UN MOUSEPRESSED**

<img width="567" height="353" alt="Captura de pantalla 2026-06-26 053158" src="https://github.com/user-attachments/assets/0b68ba6e-5707-4534-b6bd-8c01c201376a" />
