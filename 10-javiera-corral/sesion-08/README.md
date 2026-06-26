# sesión 08 - 29/05

Repaso diagrama de flujo: 

🩷Input (Entrada): La
información o los ingredientes
que necesitas para empezar.

💜Proceso(algoritmo): Los pasos
lógicos que transforman
esa entrada.

💙Output (Salida):
El resultado final o la
solución al problema.

Arrays & Class  
-

ARRAYS (listas/arreglos)
-
DEFINICIÓN

Un contenedor con compartimentos numerados donde puedes
guardar múltiples datos bajo un mismo nombre. Es una lista que
mantiene varios datos ordenados. Los arreglos (Arrays) son muy
útiles para almacenar datos relacionados.

contendor o compartimiento numerado que contien multiples datos de cualquier tipo guardados bajo el mismo nombre (en programación se cuenta desde 0 en adelante)

let nombreArray =[e0, e1, e3, e4, e5] ; 
llamar a los valores: nombreArray [n° elemento]  

 *para distinguir entre array y función los array deben escribirse con mayuscula al inicio a diferencia de las funciones.
 *nombreArray.length = total de elmentos en el array.
 

 

ejemplo1 array básico: Colores🟥🟧🟨🟩🟦🟪

```
let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];
let index = 0; 

function setup() {
  createCanvas(400, 400);
  frameRate(2);
}

function draw() {
  //background(Colores[5]);
  
  
  background(Colores[index]);


  index = index + 1;

  if (index >= Colores.length) {
   index = 0; 
  }
}
```

ejemplo2 diametro y elipse:

```
let Diametro = [0,10, 50, 100, 150, 200, 250, 300, 350, 400]; // Array con numeros
let index = 0; // creamos e incializamos variable para guardar la posición del Array

function setup() {
  createCanvas(400, 400);
  background(0, 200, 150);
  frameRate(1);
  
}

function draw() {
  
  fill(252,30,200,50);
  ellipse (200,200, Diametro[index]);
  index = index + 1;
  print(index);
  
  if(index>= Diametro.length){
    index=0;
  }
}

function mousePressed(){
  background(0, 200, 150);
}

``` 

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/944d4d19-d56d-4739-87c2-4562af4645e9" />

ejemplo3 bandera gay:

```
let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];

function setup() {
  createCanvas(850, 600);
}

function draw() {
  background(220);

  // Creamos, definimos e inicializamos una variable para determinar la altura de cada franja de color

  let alturaFranja = height / Colores.length; //colores.lenght en este caso es = a 6

  //Repite el loop mientras "i" sea menor que el total de elementos en el array colores, aumentando "i" de 1 en 1 - esto es lo que se llama recorrer un Array

  for (let i = 0; i < Colores.length; i++) {
    fill(Colores[i]); // Cambia el color de relleno por cada elemento
    noStroke();
    rect(0, i * alturaFranja, width, alturaFranja); // Dibuja un rectángulo en una posición x,y calculada por el índice i y la alturaFranja
  }
}
```

<img width="327" height="190" alt="image" src="https://github.com/user-attachments/assets/c6ac0228-4feb-4f31-829c-a86d855581d8" />

ejemplo4 palabras:(hice algunos cambios):

``` 
let palabras = ["akrilla", "gaga", "XCX", "princesa"]; // Array con palabras
let index = 0; // creamos e incializamos variable para guardar la posición del Array

function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
}

function draw() {
  background(
42, 245, 39
);

  textSize(100);
  fill(0);
  text(palabras[index], 200, 190);
}

function mousePressed() {
  index = index + 1;

  if (index >= palabras.length) {
    index = 0;
  }
}

```

<img width="200" height="200" alt="Captura de pantalla 2026-05-29 113220" src="https://github.com/user-attachments/assets/c8563c18-0743-4638-8313-0b6bba8f3fe7" />

ejemplo5 imagenes artistas (usar.jpg):

``` 
// Declaramos las variables globales para que funcionen en todo el código

let Fotos = []; //creamos un Array vacío que se llama Fotos
let index = 0; // creamos variable para guardar la posición actual en el array

// Creamos también las variables para las imágenes individuales
let foto0, foto1, foto2, foto3;

function preload() {
  // precargamos las imágenes
  foto0 = loadImage("assets/akri.jpg");
  foto1 = loadImage("assets/princesa.png");
  foto2 = loadImage("assets/mena.jpg");
  foto3 = loadImage("assets/gianluca.jpg");
}

function setup() {
  createCanvas(600, 600);

  // Llenamos el array global que declaramos arriba (sin usar "let" aquí)
  Fotos = [foto0, foto1, foto2, foto3];
}

function draw() {
  background(220);

  image(Fotos[index], 0, 0, width, height);
}

function mousePressed() {
  index = index + 1;

  if (index >= Fotos.length) {
    index = 0;
  }
}
```

Class (molde)
-
DEFINICIÓN

Una clase (class) es un molde o plantilla abstracta que define la
estructura, los datos (propiedades) y los comportamientos
(métodos) que tendrá un tipo de objeto específico.

Imagínala como el plano de diseño de una casa o un
cortador de galletas: no es el objeto real en sí, sino
las instrucciones empaquetadas para fabricar infinitas
copias independientes basadas en ese mismo modelo
utilizando la palabra clave new

La sintaxis básica de una clase
-
en JavaScript se estructura
siempre en tres partes dentro
de un bloque de llaves:  
1. La palabra clave class +
nombre que le quiera dar.

2. El método constructor
(donde se definen las
propiedades del objeto
usando .this)

3. Las funciones
personalizadas que definen lo
que hace el objeto.


ejemplo6 class cuadrado:

```
function setup() {
  createCanvas(500, 500);
  cuadrado1 = new cuadrado();
  cuadrado2 = new cuadrado();
  cuadrado3 = new cuadrado();
}

function draw() {
  background(129, 167, 242);

  cuadrado1.move();
  cuadrado1.show();
  cuadrado2.move();
  cuadrado2.show();
  cuadrado3.move();
  cuadrado3.show();
}

class cuadrado {
  constructor() {
    this.x = 150;
    this.y = 150;
  }

  move() {
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }
  show() {
    stroke(179, 255, 127);
    strokeWeight(4);
    noFill();
    rect(this.x, this.y, 200, 200);
  }
}
```


<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/e71e7bf6-3f3b-4c82-8795-fd715d02ed47" />

CLASS + ARRAY 
-
ejemplo7 cuadrados 

```
// Declaramos un array vacío global para almacenar los 10 objetos cuadrados
let cuadrados = [];

function setup() {
  createCanvas(500, 500); // Creamos un lienzo de 500x500 píxeles
  frameRate(20); // Ralentizamos el código a solo 2 fotogramas por segundo

  //  Loop de inicialización: se ejecuta 10 veces al arrancar el programa
  for (let i = 0; i < 10; i++) {
    // Fabricamos un objeto real usando el molde de la clase y lo guardamos en la posición 'i'
    cuadrados[i] = new Cuadrado();
  }
}

function draw() {
  background(129, 167, 242); // Pintamos el fondo de color lila

  //  Loop de actualización: recorre los 10 cuadrados guardados en el array
  for (let i = 0; i < cuadrados.length; i++) {
    cuadrados[i].show(); // Le pide al cuadrado actual que se dibuje en la pantalla
    cuadrados[i].move(); // Le pide al cuadrado actual que cambie su posición
  }
}

// El molde o Clase
class Cuadrado {
  // El constructor define las propiedades iniciales de cada cuadrado cuando nace
  constructor() {
    this.x = 250; // Todos nacen exactamente en el centro horizontal (500 / 2)
    this.y = 200; // Todos nacen exactamente en el centro vertical (500 / 2)
  }

  // Método para alterar la posición del objeto
  move() {
    // Al valor actual de X e Y se le suma un número al azar entre -5 y 5
    // Esto genera un movimiento tembloroso
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }

  // Método para renderizar (dibujar) el objeto en el lienzo
  show() {
    // Define un color de borde aleatorio en sus tres canales (Rojo, Verde, Azul)
    stroke(random(255), random(255), random(255));
    strokeWeight(4); // Define un grosor de borde de 4 píxeles
    noFill(); // Hace que el interior del cuadrado sea transparente

    // Dibuja el cuadrado usando sus coordenadas internas 'this.x' y 'this.y' con tamaño 20x20
    rect(this.x, this.y, 20, 20);
  }
}
``` 

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/56c6d580-bc35-4b82-ac3a-2774844766ba" />


{ENCARGO 5}
-

• Deben crear su propio sistema de partículas, con 5 imágenes (mínimo) en .PNG
• Pueden crear ustedes sus diseños o usar fotos recortadas.
• Sean Creativos - tema LIBRE

• FECHA DE ENTREGA: Antes de la clase del viernes 5 de junio
• CARPETA DE ENTREGA:
• https://drive.google.com/drive/folders/1bxa1eLaDP5t0ACkSEbhzwS7g2mveRgsz?usp=sharing



