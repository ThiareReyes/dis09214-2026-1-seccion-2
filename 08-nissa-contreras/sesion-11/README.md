# sesión 06 - 12/06
---
# Para crear un scketch QUE SE ADAPTE A DIFERENTES se deben seguir los siguentes pasos:

### paso 1: Crear un canvas con dimensiones dinámicas 

* Para esto usaremos las variables integradas en el sistema: (windowWidth, windowHeight) estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.

```
function setup() {
  createCanvas(windowWidth, windowHeight);
```  


### paso 2: Crear un evento windowResized() 

* Si el usuario estira o encoge la ventana del navegador, el lienzo se adaptará al tamaño de la ventana en tiempo real.

```
function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
```


### paso 3: Usar valores relativos

* Ahora p5.js actualiza estas variables width y height automáticamente con el tamaño actual del lienzo.
* Entonces ahora todos los valores de posición y tamaño que ocupemos los tenemos que pensar en **relación proporcional a esas variables.**
* Usaremos fracciones y proporciones:
Ejemplo: Centro del lienzo: (width / 2, height/ 2)
Ejemplo: A un cuarto de la pantalla en eje x: ( width * 0.25)

```
function setup() {
  createCanvas(windowWidth, windowHeight);
}

function draw() {
  background(0);
  
  fill(150, 150, 250);
  noStroke();
  rect(width * 0.05, height * 0.05, width * 0.2, height * 0.15);
  
  fill(250, 100, 100);
  ellipse(width * 0.5, height * 0.5, width * 0.2, height * 0.2);
  
  stroke(255);
  strokeWeight(width * 0.005); 
  noFill();
  ellipse(width * 0.5, height * 0.5, width * 0.25, height * 0.25);
  
  fill(100, 200, 150);
  noStroke();
  triangle(
    width * 0.85, height * 0.1,
    width * 0.75, height * 0.25,
    width * 0.95, height * 0.25
  );

  fill(240, 200, 100);
  quad(
    width * 0.05, height * 0.75,
    width * 0.2, height * 0.7,
    width * 0.25, height * 0.9,
    width * 0.08, height * 0.88
  );
```


### paso 4: Incluir un factor de referencia  
**referencia = min(width, height)**

* Creamos una variable global (referencia) y la asignamos para que calcule el mínimo.
* Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.

```
let referencia;

function setup() {
  createCanvas(windowWidth, windowHeight);
  referencia = min(width, height);
}

function draw() {
  background(0);

  let xCentro = width / 2;
  let yCentro = height / 2;
  
  // El diámetro será siempre el 40% del lado más corto de la ventana
  let diametro = referencia * 0.4; 

  fill(250, 100, 100);
  noStroke();
  ellipse(xCentro, yCentro, diametro, diametro);
  print(width, height);
 
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
  referencia = min(width, height); 
}
```


### paso 5: Usar translate- push y pop  
**Consejo para proyectos complejos

* En lugar de hacer matemáticas complejas en cada **rect()** o **ellipse()**, usamos **translate()** para "mover el origen del mundo”.
* Y siempre utilizando **push()** y **pop()** para cada figura o elemento.

```
let referencia; 

function setup() {
  createCanvas(windowWidth, windowHeight);
  referencia = min(width, height);
}

function draw() {
  background(240);
  
  // Rectángulo (Posicionado arriba a la izquierda)
  push();
  translate(width * 0.05, height * 0.05);
  fill(150, 150, 250);
  noStroke();
  rect(0, 0, referencia * 0.3, referencia * 0.2);
  pop();
  
  // Círculos (Posicionados en el centro de la pantalla)
  let diametro = referencia * 0.25; 
  push();
  translate(width / 2, height / 2);
  
  fill(250, 100, 100);
  noStroke();
  ellipse(0, 0, diametro, diametro);
  
  stroke(50);
  strokeWeight(referencia * 0.004); 
  noFill();
  ellipse(0, 0, diametro * 1.25, diametro * 1.25);
  pop();
```

## Desafío
```
function setup() {
  createCanvas(windowWidth, windowHeight);
  let = min(width, height);
}

function draw() {
  background(255);
  
  // Rectángulo azul
  push();
  fill(40, 30, 179);
  noStroke();
  rect(0, 0, width/3, height/2);
  pop();
  
  // Rectángulo rojo
  push();
  translate(0, height/2);
  fill(214, 32, 32);
  noStroke();
  rect(0, 0, width, height/2);
  pop();
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
  referencia = min(width, height);
}
```

---

## Imágenes loadImage

### PASO 1: Subir la imagen a p5

* Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.  
* Hacer clic en el icono de + o el menú desplegable junto a Files.  
* Seleccionar Upload file (Subir archivo).  
* Arrastrar la imagen o buscarla en el computador.  
* ¡Usar nombres de archivo cortos, en minúsculas y sin espacios! Hacer una carpeta llamada ASSETS


### PASO 2: Declarar y precargar la imagen
**function preload()**

* Creamos una variable global al inicio del código para guardar la imagen.  
* Usamos la función loadImage() dentro de function preload().


### PASO 3: Dibujar y dimensionar en el draw  
La imagen se dibuja usando la función image()

* Esta función requiere mínimo 3 argumentos, pero acepta 5 si queremos controlar su tamaño de forma responsiva.

Sintaxis: image(nombreVariableImagen, x, y, ancho, alto);

---

## EJEMPLOS AVANZADOS DE DISTORSIÓN DE IMAGEN

**loadPixels()**  
Entrar en los píxeles

* Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.  
* loadPixels() crea un "puente" temporal para que puedas analizar la información de forma masiva y fluida.

### Modificar los píxeles

* **get(x, y) Lectura (El "Ojo")**
Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.

Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).

Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una copia de respaldo completa del lienzo.


* **set(x, y, nuevoColor) Escritura (El "Pincel")**
Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por completo el color que existía ahí.

Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo aspecto de la imagen.


* **updatePixels() — La Actualización**
Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la pantalla.

¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios en un borrador secreto. updatePixels() es el comando que efectivamente "publica" y renderiza el resultado final en el lienzo para que el usuario pueda verlo.
