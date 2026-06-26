# Solemne 01  
Para mi proyecto elegi al artista abstracto Robert Motherwell, pintor estadounisdense del expresionismo abstracto. Sus pinturas se caracterizaban por el uso del color negro cubriendo gran parte de su liezo con machas gigantes.  
Quise plasmar esas mismas manchas en la pantalla, que abarcarán gran espacio en el lienzo y sin tenerle miedo al uso del color negro por lo que me inspire en algunas de sus obras para conseguirlo.
### Inspos:  
![Inspo1](https://uploads8.wikiart.org/images/robert-motherwell/mallarme-s-swan-1944.jpg!PinterestSmall.jpg)  
![Inspo2](https://www.caviar20.com/cdn/shop/files/Caviar20_Robert-Motherwell-Seaside-Studio-1990_02_800x.jpg?v=1695127125)  
![Inspo3](https://www.singulart.com/blog/wp-content/uploads/2024/03/Elegy-to-the-Spanish-Republic-1.jpg)  
![Inspo4](https://commonreader.wustl.edu/app/uploads/2024/02/MotherwellCatalonia-rotated.jpeg)  

## Proceso  
  **Contrucción en papel**  
Jaja la verdad es que me había confundido con el tipo de papel y en vez de trabajar con papel milimetrado lo hice con papel cuadriculado lol hací que trabaje mi lienzo en un cuadrado de 25x25, fue un proceso rapido puesto que no utilicé colores ya que lo tenía pensado para cuando trabajara con P5js y aparte en la obra en la que me inspiré solo se usaba un color y negro; al momento de presentarlo en clases me dijerón que le agregue más color, así que eso haré jeje.  
  **Contrucción en P5js**  
La verdad no se me complicó demasiado el uso de P5js puesto que ya había estado familiarizado con el uso de leguaje de progrmación (no lo suficiente) y claro, casi todo se trata de lógica y saber posicionarte bien en las coordenas. Eso siii, como mi liezo inicial era de 25x25 tuve que hacer el trabajo de escalas y eso se me complicó en un inicio ya que soy malo con las matemáticas, hice algunas marcas en el lienzo para que me ayudarán a posicionarme en plano cartesiano, con ayuda de la calculadora me posicione en las coordenas adecuadas en al p5js y trabaje de manera rapida.  
Me acostumbraba de a poco y en algunos casos deje de usar la calculadora para usar la lógica, en algunos casos me confundía con los números y los ponía al revés. Otro incomveniente es que se me olvidaba guardar el trabajo jaja (Como ahora mientras escribo esto) o_0.  

## Resultado  
![Resultado](file:///C:/Users/jandr/Downloads/solemne1.png)  

  **Link a trabajo**  
![Link a proyecto](https://editor.p5js.org/andrenaliine/sketches/fut3InWFh)  

##Fotografía dibujo físico  
![Dibujo Físic](file:///C:/Users/jandr/Downloads/IMG_20260327_095120095.jpg)  
  
## Work In Process  
![1](file:///C:/Users/jandr/Downloads/proceso1.jpg)  
![2](file:///C:/Users/jandr/Downloads/proceso2.jpg)  
![3](file:///C:/Users/jandr/Downloads/proceso3.jpg)  
![4](file:///C:/Users/jandr/Downloads/proceso4.jpg)  

## Codigo Comentado  
  
```function setup() {
  createCanvas(500, 500);
  background(230, 215, 101);
  angleMode(DEGREES);
}

function draw() {
  //Rectangulos
  stroke(0, 0, 0);
  fill(31, 31, 28);
  rect(0, 0, 126, 500); //Rectangulo grande lado izquierdo
  fill(31, 31, 28);
  rect(390, 50, 100, 340); //Rectangulo grande lado derecho
  rect(490, 170, 500, 170); //Rectangulo pequeño extramo derecho
  fill(110, 162, 184);
  rect(190, 310, 80, 180); //Rectangulo celeste

  //Cuadrilateros
  fill(199, 78, 78);
  quad(190, 410, 210, 410, 230, 430, 170, 430); //Cuadrilateros sobre rectangulo
  fill(102, 39, 39);
  quad(170, 430, 230, 430, 250, 450, 150, 450);

  //Circulo
  fill(110, 162, 184);
  circle(170, 220, 50); //Circulo pequeño debajo de gran ellipse negro

  //Ellipse
  fill(31, 31, 28); // Gran ecllipse negro
  ellipse(188, 130, 120, 200);

  //LINEAS
  stroke(0, 0, 0);
  line(125, 30, 390, 30); //Lineas horizontales y verticales superiores
  line(410, 0, 410, 50);

  line(145, 220, 145, 290); //Lineas abajo de circulo azul oscuro
  line(145, 290, 170, 245);
  line(170, 245, 191, 270);
  line(191, 270, 191, 235);

  line(330, 370, 330, 410); //Lineas abajo de doble cuadrado
  line(330, 410, 350, 370);
  line(350, 370, 370, 450);
  line(370, 450, 370, 370);

  line(330, 190, 370, 150); //Lineas horizontales y perpendiculares
  line(350, 190, 370, 190);

  line(150, 350, 150, 410); //Lineas con forma de L junto a los tres circulos
  line(150, 410, 230, 410);

  line(170, 460, 230, 460); //Linea abajo de cuadrilateros

  line(490, 90, 500, 90); //Linea extremo derecha

  //Circulos
  fill(31, 31, 28); //Pequeños circulos negros
  circle(160, 360, 10);
  circle(160, 380, 10);
  circle(160, 400, 10);

  //Cuadrilatero
  fill(31, 31, 28);
  quad(250, 30, 250, 210, 310, 150, 310, 30); //Cuadrilatero negro central

  //Triangulos
  fill(117, 36, 34);
  triangle(390, 390, 490, 490, 390, 490); //Triangulo abajo de rectangulo lado derecho

  //Circulo
  fill(168, 119, 66);
  circle(420, 460, 20); //Pequeño circulo encima de Triangulo

  //Triangulo
  fill(110, 162, 184);
  triangle(390, 390, 490, 490, 490, 390); //Triangulo celeste abajo de rectangulo lado derecho
  triangle(190, 270, 390, 270, 290, 170); //Triangulo morado celste parte posterior
  fill(222, 118, 64);
  triangle(230, 270, 390, 270, 310, 190); //Triangulo naranjo delantero

  //Arco
  fill(65, 78, 65);
  arc(320, 235, 80, 68, 45, 225);

  //Circulo
  fill(31, 31, 28); //Circulo negro
  circle(350, 95, 80);

  //Triangulo
  fill(255, 0, 0); //Triangulo rojo
  triangle(190, 290, 430, 530, 310, 530);

  //Cuadrados
  fill(117, 36, 34); //Cuadrado rojo vino
  square(290, 270, 100);
  fill(222, 118, 64);
  square(310, 290, 60); //Cuadrado naranjo
}```  
