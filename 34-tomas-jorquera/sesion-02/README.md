# sesión 03 - 27/03

# sesión 03 - 27/03
# BREVE HISTORIA DE LA COMPUTACION  
***Telar de Jacquard:*** Hito clave para la gráfica. Usaba tarjetas perforadas para automatizar diseños complejos en la tela, CREADO EN 1801

***Ada Lovelace:*** La primera programadora. Fue la primera en entender que la máquina leía símbolos, no solo servía para calcular números, sino que podía generar música o patrones artísticos. Escribió el primer algoritmo de la historia.

***Máquina de Turing:*** No era una máquina física, sino un experimento matemático de Alan Turing. Demostró que el hardware es irrelevante; lo que realmente importa para que la máquina funcione son las instrucciones. Creada en 1936.

### Inicios del Arte Computacional: Artistas de los 60s (como Vera Molnár y el Computer Technique Group) empezaron a usar el computador para generar arte.

Hermanos Whitney: Pioneros de la animación gráfica. Modificaron un computador analógico balístico de la Segunda Guerra Mundial y lo usaron para pintar con luz sobre celuloide, introduciendo el concepto de Diseño Paramétrico.

Douglas Engelbart Aportó conceptos de usabilidad que hoy son básicos: ventanas, bitmapping y la invención del mouse.

#### DEMOCRATIZACIÓN DEL CREATIVE CODING
Software Libre vs Open Source: El movimiento de Software Libre es ético y defiende 4 libertades: usar, estudiar, distribuir y mejorar el código. El Open Source es un enfoque práctico para que la comunidad mejore el código en conjunto.
##### "Libre" no significa siempre que sea gratis.


John Maeda creó Design By Numbers en el MIT para enseñar a programar a diseñadores visuales usando una cuadrícula y tonos de negro. Su visión era que el computador no es una herramienta más, sino un nuevo material para diseñar.

Processing : Casey Reas y Ben Fry tomaron la idea de Desing by Numbers y la expandieron agregando color y tamaño variable. Es un software libre súper visual pensado como un cuaderno de código para artistas y diseñadores

# clase-markdown

MARKDOWN es un lenguaje de marcado ligero, una frma de escribir texto con formato, añadiendo simples marcas al texto con caracteres comunes del teclado.

SALTO DE LINEA
Si se necesita separar dos parrafos, se presiona la tecla enter dos veces, esto deja un espacio entre los bloques.

#### PARRAFO NUEVO: Enter dos veces
#### BAJAR UNA LINEA: Dos espacios al final + Enter
#### FORZAR EL SALTO: < > br  


OPTION + ALTERISCO= ~
~~TEXTO~~
_TEXTO_
__TEXTO__
***TEXTO***
\

1. elemento 1
2. elemento 2   
   3.1 elemento 2.1

  
[VIDEO DEL SIGLO](https://www.youtube.com/watch?v=vBynw9Isr28)
  [![GAGA](https://offloadmedia.feverup.com/secretmanchester.com/wp-content/uploads/2025/10/07132101/GettyImages-2213271076-1024x683.jpg)](https://www.ladygaga.com/us-en/)           
  [![ADDISON](https://idols2rivals.com/wp-content/uploads/2025/06/addissosonn.png)](https://www.youtube.com/watch?v=beNFK2cdnKU)



# CLASE P5

***Algoritmo:*** es una secuencia de instrucciones paso a paso, logicas, definidad, ordenadas y finitas que ejecutan una tarea especifica.
#### Estructura
__Imput (entrada) -  Algoritmo - Salida (output)__ 

### DIAGRAMA DE FLUJO
Representacion grafia de los pasos de un proceso o de un algoritmo, se utiliza como una herramienta para visulaizar la logica de un programa antes de escribir una sola linea de codigo.
Se utilizan componentes Estandar para qu cualquier programador pueda entenderlo.

***CREATE CANVAS***
Nos sirve para crear un lienzo y determinar su tamaño en pixeles, solo se pone una vez y dentro del setup.
__render:__ Define el motor de renderizado

***background***
Nos sirve para definir el colord e nuestro lienzo, se piuede poner en el setup o en el draw, pero nhay diferentes resultados.

### DIBUJAR en p5.js
Para dibujar tenemos que entender que el canvas funciona como un sistema de coordenadas, como una plano cartesiano, pero el punto 0,0 no esta en el centro, sino en la esquina superior izquierda

***COLOR DEL BORDE***
stroke: establece el color que se utiliza para dibujar puntos, lieas y contornos de figuras o el ancho de linea o punto. Siempre se pone arriba de Stroke

