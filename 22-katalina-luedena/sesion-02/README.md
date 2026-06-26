# sesión 03 - 27/03
# clase-makdown
Es una plataforma en la nube que permite almacenar, gestionar y compartir código fuente utilizando el sistema de control de versiones Gift. Funciona como una “red social“ para programadores, facilitando la colaboración, el seguimiento de cambios y el desarrollo de proyectos de software, tanto públicos como privado.


MARKDOWN- Es un lenguaje de marcado ligero. En términos simples, es una forma de escribir texto con formato.  

SALTOS DE LINEA- párrafo nuevo enter dos veces.  

BAJAR UNA LINEA- dos espacios al final más enter.  

FORZAR SALTO- <BR  
ENCABEZADOS-  
#título nivel 1  
##nivel 2  
###nivel 3, y así.  
#Formato de texto:

# Breve hisitoria de la computación  
## Maquina diferencial/ Charles Babbage, 1822.  
### "La primera computadora del mundo"  
Babbage diseñó esta máquina para sistematizar el cálculo de la tabulación de funciones polinómicas, tareas que hasta entonces se realizaban manualmente y eran propensas al error. Era un gran dispositivo mecánico de gran escala, compuesto íntegramente por engranajes que servía para resolver ecuaciones e imprimir los resultados en forma de tablas matemáticas.

## Máquina diferencial II/ Museo de las ciencias de Londres, 1991.  
### The difference Engine.  
El Museo de ciencias de Londres construyó la Difference Engine No.2 siguiendo exactamente los planos originales de Babbage. Funcionó perfectamente, demostrando que su diseño era correcto y que se pudo haber construido en la época victoriana si la gestión hubiera sido diferente.

## Máquina analitica/ Charles Babbage, 1834-1837.  
La máquina analitica fué diseñada para realizar cualquier tipo de cálculo establecido anteriormente y para tener una capacidad de análisis aún mayor que la Máquina diferecial original. Se concidera la primera Máquina de cálculo completamente automática.

## Telar de Jacquard/ Joseph Marie Jacquard, 1801.  
 - Primer sistema de almacenamiento de información binaria.
 - El telar usaba un sistema de tarjetas perforadoras para lograr diseños complejos y automatizados.
 - Si había agujero: La varilla pasaba, el gancho se activaba y levantaba el hilo (podemos llamarlo un 1 o "encendido").
 - Si no había agujero: La varilla chocaba contra la tarjeta, el gancho no se movía y el hilo se quedaba abajo (podemos llamarlo un 0 o "apagado").

## Tres conceptos fundamentales de la computación moderna:  
1. ### La separación entre hadware y software
   **Hadware**: El telar en sí (la máquina física, los granajes, los hilos).
   **Software**: Las tarjetas perforadas.

   Antes de Jacquard, si queríamos que una máquina hiciera algo diferente, teníamos que reconstruirla o cambiar sus piezas. Con Jacquard la máquina no cambia; solo cambias las tarjetas (el programa) y obtienes un rsultado totalmente distinto.

3. ### El sistema binario
   Aunque Jacquard no pensaba en matemáticas, creó un sistema de lógica binaria. La aunsencia o presencia de materia (agujero o cartón) determinaba una acción.

4. ### El píxel y la imagen rasterizada
      Podemos entender el tejido como una forma primigenia de imagen de mapa de bits: la tela constituye la rejilla (grid) de soporte, donde cada intersección entre trama y urdimbre funciona como un píxel individual. La tarjeta perforada opera como el archivo digital (el .jpg), enviando instrucciones precisas sobre qué puntos activar para componer la imagen visual.

## Ada Lovelace  
### "La primera programadora"  
Ada Lovelace fué una matemática y escritora del siglo XIX, considerada la primera programadora de la historia, trabajó junto a Charles Babbage en el desarrolo de la máquina analítica. Aunque Babbage pensaba que la máquina era solo para cálculos numéricos, Ada antendió que podía procesar cualquier tipo de información (como música o arte).  
Inspirada en el telar de Jacquard, vio que las tarjetas perforadas podían usarse para crear instrucciones o programas, por esto, se le conoce por anticipar el concepto de programación mucho antes de que existieran los computadores.

### El primer algoritmo  
Entre 1842 y 1843, Lovelace tradujo al inglés y revisó un artículo del ingeniero italiano Luigui Menabrea sobre la máquina analítica de Babbage. En sus anotaciones, Lovelace incluyó un conjunto de algoritmos diseñado específicamente para su implementación en un "computador", para que la máquina calculara una serie de números de bernoulli. Estos algoritmos se consideran actualmente como el primer programa de computación, lo que convierte a Lovelace en la primera programadora de la historia.

## La máquina de Turing  
Originalmente fue definida por el matemático inglés Alan Turing como la "máquina automática" en 1936 en la revista Proceedings of the London Mathematical Society.  

No es una máquina física es un **experimento mental** (una máquina teórica). Turing imaginó una cinta infinita, un cabezal que lee/escribe símbolos, y un cpnjunto de reglas, (estados).  

Define la **Computabilidad Universal**. Turing demostró que una máquina simple, con las instrucciones correctas, puede simular a cualquier otra máquina.  

El hadware se vualve irrelevante; lo que importa es **el código (las instrucciones)**.

# El despertar visual  
## Artistas y algoritmos  
La mayoría de los esfuerzos por usar la computadora para crear arte comenzaron en la década de 1960, en medio de una escena artística efervescente y diversa. Artistas como **Vera Molnár**, **Manfred Mohr**, **Georg Nees**, entre otros.

# John & James Whitney  
Fueron pioneros en el trabajo con Computer Graphics Animation.  

Whitney no usó una computadora digital al principio. Recuperó un **compuatdor análogo de la Segunda Guerra Mundial** (un director de tiro antiaéreo M-5) y lo que modificó. En lugar de calcular trayectorias para derribar aviones, convirtió los voltajes en movimientos de cámara y luz para pintar sobre celuloide.  

Introducen el concepto de Diseño Paramétrico y Movimiento Armónico.

# Sketchpad Ivan Sutherland  
En 1963, Sutherland creó el primer programa informático que permitía dibujar directamente en una pantalla usuando un lápiz óptico.  

Este sistema introdujo la manipulación directa de objetos gráficos, pionero en la interacción humano-computador (HCI), sentando las bases de los programas de diseño asistido por computador.  

Introdce la Programación Orientada a Objetos (POO) de forma visual: podía dibujar una "rueda maestra" y luego crear 50 copias; si cambiaba la maestra, cambiaban todas.

# Democratización del Creative Coding  
## Software libre  
Nace formalmente en 1983, cuando Richard Stallman anunció el inicio del Proyecto GNU.  

La idea del proyecto era crear un sistema operativo libre.  

En 1985 se publica el Manifesto GNU y se funda la **Free Software Fundation (FSF)**.  

Este movimiento surgió como respuesta a la creciente privatización del software.  

#### Buscan garantizar 4 libertades esenciales:  
1. **Libertad 0 (uso):** La libertad de ejecutar el programa como se desee, con cualquier propósito.
2. **Libertad 1 (estudio):** La libertad de esrudiar cómo funciona  el programa y cambiarlo para que haga lo que el usuario quiera. El acceso al código fuente es una condición necesaria.
3. **Libertad 2 (distribución):** La libertad de redistribuir copias para ayudar a otros.
4. **Libertad 3 (mejira):** La libertad de mejorar el programa y hacer públicas las mejoras, para que toda la comunidad se beneficie. El acceso a código fuente es necesario.

#### Principios fundamentales adicionales de la FSF:  
1. **Libertad, no prec* El software libre es una cuestión de libertad de los usuarios de computadores, no de precio.
2. **Copyleft:** Se promueve la distribución bajo términos de copyleft, que garantizan que el software y sus versiones modificadas sigan siendo libres.
3. **Lucha contra restricciones:** Campañas activas contra patentes de software, Gesatión Digital de Restricciones (DRM) y otras amenazas a la libertad de los usuarios.
4. **Desarrollo del proyecto GNU:** Fomento del desarrollo de un sistema operativo completamente libre.

## Desing by numbers, John Maeda  
Experimento educativo radical, lanzado en 1999 por John Maeda en el MIT Media Lab.  
Consistía en un lenguaje de prgramación y entorno diseñado específicamente para enseñar a diseñadores visuales a programar.  

- Todo el espacio de tranajo es una cuadrícula fija de 100x100 píxeles.
- No había colores RGB complejos. Solo existía el "porcentaje de tinta".0 era blanco (papel vacío) y 100 era negro total.
- Maeda eliminó los puntos y comas, las llaves complejas y las declaraciones de tipos variables. El código se leía fácilmente: line 10 10 90 90 (dibuja una línea de x10, y10 a x90,y90).

## Procesing, Casey reas y Ben Fry  
Software libre, de código abierto y gratuito, diseñado para la enseñanza de prgramación en contextos visuales, permite a artistas, diseñadores y principiantes crear gráficos, animaciones e intereacciones, estando disponible paea Windows, macOS, Linux.  

Creado en el MIT Medialab por 2 estudiantes de John Maeda; Ben Fry y Casey Reas, en el año 2001.  

Quisieron expandir las limitaciones del Desing by Numbers (DBN).  

Agregaron la paleta de color y tamaño variable.  

Mantuvieron la simplicidad en la sistaxis en el código y la idea del #sketchbook".io:*
