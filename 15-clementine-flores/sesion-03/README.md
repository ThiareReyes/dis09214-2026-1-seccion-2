# sesión 03 - 27/03
## ***P5.js***
- *Algoritmo*: Secuencia de instrucciones finitas, específicas, ordenadas, definidas y sin ambigüedad

- *Preparación de sandwich*:
* Input(entrada): Información o ingredientes y utensilios para empezar}

* Algoritmo: Pasos lógicos que transforman esa entrada(Instrucción)

* Output: Sandwich terminado, resultado o la solución al problema
- *Diagrama de flujo*: Representación gráfica del algoritmo o de los pasos, se usa simbología

* Simbología:
![diagrama](./4.png)
![diagrama](./1.jpg)

- *Lenguaje de programación*:
![Lenguaje](./2.jpg)

* Los más conocidos son javascript, python, etc.
* En p5 se usa una simplificación de javascript
## ***P5.js***
- *Reference*: diccionario
- Start coding
- *Función setup* : Una sola vez al principio, el tamaño del lienzo, sonido, etc. configuraciones
que no van a ir cambiando
- *createCanvas*: Cambia el tamaño del lienzo(ancho, largo)
* ancho, largo, renderer(p2d o 3d, si esta en 2d no se usa), canvas(parámetro oculto)
- *Función draw*: Las repite una y otra vez(60 veces por segundo), crea movimiento
* 220 es un gris
- *Background*: Colores
* Escala de grises 220, 0 es negro y 255 es blanco
* rgb 3 números (255, 0, 0) (rojo, verde, azul)
* Nombre de colores: (‘blue’) siempre entre comillas
* Transparencia: 4 números (0, 0, 255) rgb y el cuarto
- *RGB*:
* Negro(0, 0, 0)
* Blanco(255, 255, 255)
* rojo(255, 0, 0), verde(0, 255, 0), azul(0, 0, 255)

- Se puede cambiar el modo de color en el setup: en colorMode(HSB)
- Para desactivar una linea de codigo se pone: //
- Comentar el código: Se pone en español al lado con // antes
- Cada línea de código hay que comentarla y puede pedir que cambiemos el color
- Dibujar en p5: y,x
* y(vertical) x(horizontal
* 0,0 está en la esquina superior derecha
- *Figuras geométricas*:
* point: crea un punto (ej: 300, 300) son las coordenadas
* stroke: color del punto (el borde)
* strokeweight: tamaño del borde(ej:30)
* line: se define dónde empieza y dónde termina(x1,y1,x2,y2)
* rect: se define dónde empieza y dónde termina(x1,y1,x2,y2)
* *tiene un borde y fondo(strokeweight es el tamaño del borde)
* *fill: fondo de la figura
* ellipse: ahora la x e y son el centro del círculo(x1,y1,x2,y2) x1 y y1 son las coordenadas y
x2 y2 es el tamaño
* circle: 3 coordenadas: xy y el diámetro
* *Para quitar borde es: noStroke()
* square(x, y, lado)
* triangle: cada punta tiene una xy(x1,y1,x2,y2,x3,y3)
* quad: (x1,y1,x2,y2,x3,y3,x4,y4)
* arc: se pone en el setup: angleMode(DEGREES)
![Arc](./3.jpg)
* *primero es el centro, esquina derecha, como las agujas del reloj
* *(x1,y1,x2,y2,x3,y3) x1 y1 es el centro del circulo, x2y2 son los lados, x3y3 es el angulo
* strokeCap(SQUARE): linea cuadrada
* strokeCap(ROUND): linea cuadrada
* guardar: file + save
* para ordenar el codigo: edit + tindy code
* file + share + edition



Propuesta final y dibujo:







Link de p5: https://editor.p5js.org/clementine.flores/sketches/N3EjNOHZC 
