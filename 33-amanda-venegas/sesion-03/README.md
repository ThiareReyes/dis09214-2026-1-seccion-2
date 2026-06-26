# 🌸 Clase 27-03-2026  Introducción al pj5 🌸

#### ¿Que es un algoritmo? 

Es una secuencia instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que
permiten solucionar un problema o realizar una tarea específica.

Debe ser preciso, ordenado, tiene que terminar en algun momento, debes obtener siempre el mismo resultado.

INPUT:  Entrada  --->  PROCESO: Algoritmo ---> Output : Salida resultado final 

### ¿Que es un diagrama de flujo?

Representación gráfica de un algoritmo o de lospasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código.

### Lenguajes de programación 

Existen entre 700 y 900 lenguajes de programación que se utilizan en la industria ( me acuerda a la programacion que son solo moo jjajaj) 

Algunos más populares 

- Python, Java, C++ , C# , JavaScript, TypesScript etc...


### P5.JS

Utiliza principalmente el lenguaje de JavaScript, es un vocabulario especializdo para dibujar,animar y crear cosas visuales de forma más sencilla

Hay funciones maestras
- Setup: Se ejecuta una sola vez para crear el lienzo, configura el entorno inicial.  

- Draw: se ejecuta en un bucle infinito lo que te permite crear animaciones, crea movimiento y responde a la interacion en tiempo real
  
---

createCanvas : el tamaño del lienzo (W,H)

background: designa el color del lienzo en RGB los primeros 3 rojo verde azul, y cuarto le puedes dar transparencia - [htmlcolorcode](https://htmlcolorcodes.com/) 

Figuras geometricas 

<img width="585" height="178" alt="image" src="https://github.com/user-attachments/assets/c9f778f4-99cc-4608-85b4-04806c5855e2" />

Tamaño del borde 

strokeweight(); : ancho

noStroke(); para que no tenga borde 

Fill(); 

establece el color del relleno de las figuras (RGB)

Arc(); primero se activa el angleMode(DEGREES) en la parte de funcione 
arc(x,y,w,h,start,stop);

<img width="209" height="142" alt="image" src="https://github.com/user-attachments/assets/ae617cd1-e156-4886-a79f-83a7cd9809e0" />

----

[Desafio 1](https://editor.p5js.org/amanda.venegas1/sketches/3sZlCZAKz)

[Desafio2]( https://editor.p5js.org/amanda.venegas1/sketches/9wSdfU8Yw)

---
# ENTREGA 09/04/2026 

Deben inspirarse en alguna pintura de algún artist@ geométric@ o geométric@ abstract@ y hacer un dibujo
en papel milimetrado, usando solamente figuras primitivas 2D; puntos, lineas rectas, cuadrados,
rectángulos, círculos, elipses, triángulos y arcos (medialuna). Usar todas las figuras mencionas.

Mi primera idea de composicion era esta : 

![entrega](https://github.com/user-attachments/assets/e827c599-51dd-4659-a2a0-6ec9a76eb53c)

Despues cambio a esto :

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/af5401bd-871a-4452-a78f-a174d7159a35" />

Artista referente: 

Mi inspiración principal fue Wassily Kandinsky pintor ruso y pionero del arte abstracto. Mi proceso no se basó en una obra específica, sino en una actividad inspirada en él, vista en una imagen : lanzar dados y dibujar lo señalado. 

También tuve como referencia visual la obra "Klinom krasnym bey belykh" (Golpea a los blancos con la cuña roja)

<img width="227" height="277" alt="image" src="https://github.com/user-attachments/assets/46a08bba-4c48-4bae-8097-1fae00a850f6" />

Desarollo en el P5JS: 

Lo primero que realicé fue cambiar el tamaño del lienzo a 500 × 500 px. Luego, ajusté el fondo a color blanco con valores RGB (250, 250, 250) que despues cambie por un color mas neutro cafe

Para llevar mi diseño desde el formato tradicional a la pantalla, hice un cálculo para determinar la equivalencia de coordenadas. Mi lienzo original estaba dividido en una cuadrícula de 25 × 25, por lo que multipliqué cada coordenada por 20 para escalarla correctamente.

Este es un cálculo proporcional.
Por ejemplo, si un punto estaba en (2, 5), lo multiplicaba por 20:
(2 × 20, 5 × 20) → (40, 100) en pantalla.

De esta manera, fui ubicando las primeras figuras: triángulos, rectángulos, cuadrados, medios círculos, círculos, líneas y puntos. También utilicé el comando noStroke, que más adelante me generó algunas dificultades con los puntos y las líneas.

### Mi proceso 

![progreso](https://github.com/user-attachments/assets/b57511c2-50b4-4123-9e9b-7410e8700681)

Las principales complicaciones que encontré fueron:

- El medio círculo y el círculo, ya que una de las medidas corresponde al diámetro total y no al radio.
- El medio círculo en particular, porque al inicio no se dibujaba correctamente, esto se debía a que había olvidado incluir angleMode(DEGREES); en la función setup.
- El posicionamiento de las figuras, es decir, cuál debía ir encima y cuál debajo.
- Los puntos y las líneas, ya que al tener activado noStroke, no se actualizaban y solo se dibujaban una vez.
- El cuadrado no se genera colocando todos los puntos si no que solo la cordenada de arriba, más el tamaño.
-  luchar con la pantalla de mi laptop ya que no tiene una buena calibracion de color lo cual al verlo en otras pantallas me di cuenta que se veia raro
- y mi torpeza por que borre mi codigo en clase perooo tenia un respaldo antiguo, pero pude avanzar a partir de eso

Algunas de las cosas tuve que investigar en la misma pagina [reference](https://p5js.org/es/reference/)

## Resultado 

<img width="374" height="375" alt="image" src="https://github.com/user-attachments/assets/caddf2f8-7f37-4e35-95e7-557402dae0a4" />
