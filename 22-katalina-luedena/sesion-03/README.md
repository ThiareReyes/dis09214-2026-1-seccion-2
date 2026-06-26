# sesión 03 - 27/03
## Hola P5.js    

#### Algoritmo  
Es una secuencia instrucciones paso a paso,lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  

#### Características fundamentales  
*  Presición.
*  Orden.
*  Finitud.
*  definición.

## Estructura  
*  Input (Entrada): La información o los ingredientes que necesites para emepzar.
*  proceso: Los pasos lógicos que transforman esa entrada.
*  Output (Salida): El resultado final o la solucion al problema.

#### Ejemplo  
1.  Ingresientes y utensilios necesarios para hacer un sandwich (INPUT).
2.  Lista de instrucciones para hacer un sandwich (ALGORITMO).
3.  Sandwich terminado (OUTPUT).

## DIAGRAMA DE FLUJO  
*  Representación gráfica de un algoritmo  de los pasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar la lógica de un proghrama.

*  Se usan componentes Estándar (Simbología), para que cualquier programador pueda entenderlo.

## Lenguajes de programación  
#### ¿Cuántos lenguajes de programación existen?  
Existen entre 700 y 900 lenguajes de programación.   

Si incluimos lenguajes antiguos (muchos ya en desuso), dialectos específicos y lenguajes creados para investigación, la cifra supera los 8,000 o incluso 9,000.  

## P5.js  
#### Lenguaje de programación  
Utiliza principalmente el lenguaje __JavaScript__.  

#### Librería Javascript  
p5.js no es un lenguaje nuevo desde cero, sino una biblioteca (library) de JavaScript. Esto significa que usa toda la potencia y la sintaxis de JavaScript, pero te regala un "vocabulario" especializado para crear cosas visuales de forma mucho más sencilla. 

## Funciones maestras  
#### Setup(){ 
Se ejecuta una sola vez al principio (para crear el lienzo). Su propósito es configurar el entorno inicial. Lo que sucede es que se define el tamaño del lienzo (createCanvas), cargas imágenes o sonidos, y estableces configuraciones que no cambiarán (como el clor de fondo inicial).}  

#### Draw(){  
Se ejecuta en un bucle infinito (normalmente 60 veces por segundo), lo que permite crear animaciones. Crea movimiento y responder a la interacción en tiempo real. Aquí dibujas formas que cambian de posición, detectas dónde está el ratón o cambias colores gradualmente.}  

## Create canvas  
#### Sintaxis  
createCanvas([widt],[height],[render],[canvas];  
#### Ejemplo
createCanvas(100,100);  

#### crateCanvas (width,height)  
Nos sirve para crear el lienzo (canvas) y determinar su tamaño en pixeles, solo se pone __una vez y siempre dentro del setup()__.  
#### renderer
Define el motor de renderizado. 
#### canvas
Este es el parámetro "oculto" y menos utilizado, pero súper útil si eres desarrollador web.  

## Background  
#### Sintaxis 
background(v1, v2, v3, [a]);   
#### Ejemplo
background(250, 150, 228,150);  
#### background(v1,v2,v3,[a]);
Nos sirve para designar el color de nuestro lienzo (canvas). Se puede poner en setup(); o en el draw(), pero tienes resultados diferentes.    
#### [v1,v2,v3]  
Son los valores de R,G,B.   
#### [a]  
Este es el parámetro para el canal alpha, nos sirve para darle semitransparencia al color del fondo. (0-255) Donde 1 será MUY transparente y 255 MUY poco transparente.
*Se puede usar sin este parámetro.  

## Dibujar en p5.js  
Para dibujar en p5 tenemos que entender que el canvas funciona con un sistema de coordenadas (x,y) como un plano cartesiano, pero hay que tener en cuenta que el punto (0,0) no está en el centro, sino en la esquina superior izquierda.  

## Figuras geométricas 2D  
*  point(x, y); Dibuja un solo píxel en las coordenadas dadas.
*  line(x1, y1, x2, y2); Dibuja una línea desde un punto inicial hasta un punto final.
*  rect(x, y, ancho, alto); Dibuja un rectángulo. Por defecto, x e y definen la esquina superior izquierda.
*  ellipse(x, y, ancho, alto); Dibuja un óvalo o círculo. A diferencia del rectángulo, x e y definen el centro de la figura.
*  circle(x, y, diámetro); Una versión simplificada de la elipse cuando quieres un círculo perfecto.
*  square(x, y, lado); Un rectángulo donde todos los lados son iguales.
*  triangle(x1, y1, x2, y2, x3, y3); Necesitas darle las coordenadas de sus tres esquinas.
*  quad(x1, y1, x2, y2, x3, y3, x4, y4); Un cuadrilátero. Sirve para hacer formas irregulares de cuatro lados.

## Tamaño del borde  
#### Sintaxsis  
strokeWeight(weight);
#### Ejemplo  
strokeWeight(25);  
#### strokeWeight();  
Establece el tamaño deñ borde de las figuras o el ancho de la linea o punto. Siempre se pone arriba del stroke();.  
#### noStroke();  
Se usa para que mi figura no tenga borde.   

## Color del borde   
#### Sintaxis 
stroke(v1,v2,v3,[alpha]);  
#### Ejemplo  
stroke(245,0,0);  
#### stroke();  
Establece el color que se utiliza para dibujar puntos, lineas y contornos de figuras. Se pone arriba de la lina de código de la figura.  

## Forma del borde/linea  
#### Sintaxis  
strokeCap(cap);   
#### Ejemplo  
strokeCap(SAQUARE);  
#### strokeCap(); 
Define la forma de la linea o borde de nuestras figuras.  

Las constantes son:  
*  ROUND
*  SQUARE
*  PROJECT
Por defecto siempre es ROUND

## Relleno de color  
#### Sintaxis 
fill(v1,v2,v3,[alpha];  
#### Ejemplo  
fill(252,159,216);  
#### fill();  
Establece el COLOR de relleno para las figuras. Se pone arriba de la figura que quiero colorear.  

## Figuras geométricas 2D avanzadas  
#### sintaxis  
arc(x,y,w,h,start,stop)  
#### Ejemplo  
arc(250,250,100,100,270,90)  
#### arc();   
Nos sirve para hacer arcos o medio círculo. X e y son las coordenadas del centro del círculo que contiene este arco, w y h son la anchura y alto del círculo que contiene este arco, star y stop, es donde comienza y termina el ángulo de este arco.  

Se sugiere activar el modo ángulos en el SETUP(); para que sea más fácil: angleMode(DEGREES);. 

En p5.js (y en la mayoría de los lenguajes de programación), el grado 0 no está arriba, sino a la derecha (en el eje X positivo). Y se mueve en el sentido del reloj.
*  0° / 0 rad: A las 3 en punto (derecha).
*  90° / HALF_PI: A las 6 en punto (abajo).
*  180° / PI: A las 9 en punto (izquierda).
*  270° / (PI + HALF_PI): A las 12 en punto (arriba).









