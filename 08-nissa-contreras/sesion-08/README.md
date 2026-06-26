# sesión 08 - 22/05
# SOLEMNE 02 


**INFORMACIÓN DEL PROYECTO**   
***Nombre del proyecto:*** Ecos de Aflicción   
***Autores:***  Nissa Contreras/Sofía Díaz  
***Problemática de género elegida:***   Violencia hacía la mujer dentro de una relación 



***¿Qué es el proyecto?:***   
Es una abstracción gráfica que busca evidenciar a través de la interacción con el usuario, el ciclo y los patrones de conducta que experimenta una mujer cuando es víctima de violencia por parte de su pareja dentro de una relación. A través de elementos visuales, se representa cómo estas dinámicas se repiten y transforman con el tiempo, reflejando emociones como el miedo, la dependencia, la inseguridad y la tensión constante que se generan en un contexto de vulnerabilidad.

***¿Qué se ve en pantalla?:***   
Primera parte: 
* El lienzo digital tiene un fondo de color burdeos muy oscuro. En el centro, se observan cinco círculos concéntricos en una escala de tonos rosados (de un centro rosa muy claro a bordes exteriores más oscuros).
* En las cuatro esquinas del lienzo no hay triángulos simples, sino cuatro composiciones cuadradas complejas. Cada una está formada por:
    * Una fotografía en blanco y negro de figuras humanas  artísticas en el centro.
    * Un fondo de estrellas de cuatro puntas rosas que rotan o se desfasan detrás de cada foto.
* Al avanzar los segundos, estas cuatro composiciones de las esquinas comienzan a desplazarse en línea recta y de forma simétrica hacia el centro de la pantalla, disminuyendo la distancia entre ellas y los círculos concéntricos.
*  Justo cuando los elementos de las esquinas colisionan con los círculos concéntricos en el centro, la estructura geométrica se rompe y estalla en una dispersión de esferas o partículas flotantes de color rosa claro sobre el fondo morado oscuro, las cuales se expanden hacia los bordes.
Segunda parte: 
* El video experimenta un salto o transición rápida. Las partículas se contraen o reordenan brevemente hacia el centro. A la derecha de la pantalla, empieza a asomarse un gran círculo de color rosa viejo.
* La animación regresa momentáneamente a la vista de las partículas expandiéndose por todo el fondo morado oscuro, creando un efecto de dispersión aleatoria.
* La pantalla se estabiliza mostrando el gran círculo rosa viejo que ocupa la mayor parte del lado derecho e inferior del lienzo.
* Desde la parte superior interna de este círculo, caen de forma vertical numerosas líneas negras delgadas terminadas en un punto negro, imitando un patrón de goteo o lluvia digital.
* En la zona superior de este semicírculo rosa, aparece escrita de forma clara y en letras mayúsculas la palabra "AGOBIO" en tipografía Acidic negra, orientada de manera vertical/diagonal siguiendo la curvatura del círculo. El video finaliza congelado en esta composición.



***¿Qué elementos visuales aparecen?***   
FORMAS: figuras geométricas tales como, el CÍRCULO al principio, representado, por la mujer violentada, que se va haciendo pequeño por las agresiones, hasta llegar al punto de quedar en mil pedazos y esfumarse quedando en mucho círculos pequeños, y a su vez , un circulo que va aumentado de tamaño dependiendo de el movimiento de el mouse, ejemplificando la magnitud del problema y sus emociones, acompañado de pequeñas y finas LÍNEAS con círculos menores que representan las lagrimas y el dolor que atraviesa esta mujer.

COLORES: 

1. Rosa claro y subtonos: representando la calma y tranquilidad antes de la violencia.
2.  Burdeo / borgoña: representando la oscuridad en la que se va sometiendo y termina a causa de esta relación abusiva.

IMAGENES:  
<img width="750" height="1003" alt="1" src="https://github.com/user-attachments/assets/aa58ed24-5b2a-4687-a83e-37334d0f305f" />


<img width="692" height="692" alt="2" src="https://github.com/user-attachments/assets/0fe69022-0b92-465d-9ce4-0aa687c553d1" />

<img width="736" height="736" alt="3" src="https://github.com/user-attachments/assets/7a57098b-10c1-4faa-adde-f16221c487e7" />

<img width="736" height="736" alt="4" src="https://github.com/user-attachments/assets/c96623d3-b3c4-4f1c-9be0-e03616612bff" />


TEXTO:  
(CONCEPTO)  
-Agobio  
(TIPOGRAFÍAS)   
-Acidic.ttf 

---
**DESCRIPCIÓN CONCEPTUAL**  
***Idea central del proyecto y su relación con el sistema diseñado:***

Aflicción es el concepto central de nuestro proyecto. A través de este, buscamos representar el estado emocional y psicológico que experimenta una mujer al vivir situaciones de violencia de manera prolongada. Este ejercicio tomando al usuario como el hombre(pareja), que interactua con la mujer(el sketch). 
Con el paso del tiempo, esta experiencia va sumiendo a la mujer en una constante sensación de fragilidad, vulnerabilidad y susceptibilidad, afectando su percepción de sí misma y de su entorno. Esta condición genera que las posibilidades de escape o cambio se vuelvan cada vez menos visibles, provocando que el ciclo de violencia y sufrimiento continúe repitiéndose.   

***¿Cuál es la regla de oro de tu sistema?***   

A mayor tamaño de un círculo, más visibilidad de sus emociones. 
A medida de que el círculo que representa la magnitud del problema y estas agresiones, se va agrandando, se va evidenciando su pena y dolor de forma más intensa.   

***¿Cómo se relaciona esta lógica con la problemática de género elegida?***    

Así como ocurre en muchas situaciones de la vida real, los episodios de violencia suelen comenzar de manera silenciosa y casi imperceptible, manifestándose a través de acciones sutiles o minimizadas. Sin embargo, a medida que estos actos aumentan en intensidad y frecuencia, dejan de ser visibles únicamente para la mujer violentada y comienzan también a evidenciarse para quienes la rodean. En este proyecto, ese entorno está representado por el usuario que interactúa con el organismo visual, quien presencia y descubre progresivamente la magnitud de esta situación a través de la experiencia interactiva.   

**INPUT/OUTPUT**   

***¿Qué datos entran?***    
* Inputs de Recursos Estáticos: Las 4 imágenes (1.jpg a 4.jpg) y el archivo de fuente Acidic.TTF.
* Inputs del Sistema (Tiempo): La variable frameCount, un flujo constante de números enteros que incrementa en 1 cada vez que la pantalla se actualiza (a 60 fotogramas por segundo).
* Inputs de Interacción (Usuario): * El evento de clic del mouse (mousePressed).
    * Las coordenadas espaciales del cursor en tiempo real (mouseX y mouseY).
      
***¿Cómo se procesan y transforman?***   
Rotación Acumulativa: La variable giraRect se incrementa en cada ciclo (giraRect = giraRect + 1). Este número se multiplica por 90 dentro de rotate(), transformando un simple contador en un ángulo de rotación continuo para los cuadrados de las esquinas.
Mapeo de Rangos (map()): Traduce una escala de números a otra.
* En la Escena 1, convierte el número de capa (1 al 5) en un tamaño de píxeles (60 a 260px).
* En la Escena 3, convierte el índice de la línea en una posición horizontal en la pantalla (0 a width / 1.5).
Oscilación Trigonométrica (sin() y cos()):
* Ondas de los círculos y líneas: El código toma el tiempo (frameCount), le resta un desfase según la capa o la línea, y le aplica la función Seno (sin()). Esto transforma un número que siempre crece en una fluctuación suave que sube y baja entre -1 y 1, ideal para simular latidos o el vaivén de las líneas.
* Dispersión de la explosión: En la Escena 2, calcula el coseno y seno de un ángulo aleatorio para transformar el tiempo transcurrido en vectores de movimiento $X$ e $Y$, haciendo que las partículas se alejen del centro en todas direcciones.
Condicionales de Estado (if / else): Evalúa el estado de la variable lógica exploto. Transforma el flujo del programa dividiéndolo en 3 estados mutuamente excluyentes (Escena 1, Escena 2 o Escena 3).
Cálculo de Distancia Geométrica (dist()): Aplica el teorema de Pitágoras entre (mouseX, mouseY) y el centro (300, 300) para transformar dos posiciones del plano en un único valor de distancia.

***¿Qué respuesta visual producen?***   
Escena 1:   
Un fondo burdeo donde cuatro portarretratos en las esquinas giran de forma idéntica con sus imágenes al derecho. En el centro, un juego de 5 círculos concéntricos de tonos rosas y morados se expande y se contrae de forma desfasada, produciendo un efecto visual hipnótico de "onda expansiva" o pulsación orgánica.  

Escena 2:   
Una animación caótica y efímera. Al hacer clic en el centro, los elementos rígidos se borran y dan paso a 40 esferas translúcidas de color rosa y morado que "nacen" en el centro y salen disparadas hacia los bordes de la pantalla, perdiendo fuerza hasta desaparecer tras poco más de un segundo (100 frames).  
 
Escena 3:   
Una gráfica asimétrica y tensa.
    * A la izquierda, un conjunto de 50 líneas burdeo con un punto negro en la punta caen desde el techo simulando una cortina líquida o raíces que suben y bajan de forma ondulada gracias a la función sin().
    * A la derecha, la palabra "AGOBIO" se despliega rígidamente en vertical.
    * Al fondo, un círculo rosa pastel muta de tamaño de manera drástica: si el usuario mueve el mouse hacia la izquierda el círculo se encoge, y si lo mueve a la derecha, el círculo crece de forma masiva devorando visualmente el espacio.

**PENSAMIENTO COMPUTACIONAL**   

El sistema está programado para ignorar los clics en cualquier parte de la pantalla, excepto dentro del núcleo central. El clic del usuario actúa como un interruptor de energía que rompe la armonía inicial de la Escena 1.
Una vez que ocurre la explosión, el sistema activa un "reloj de arena" automático. El usuario pierde el control por un instante (100 fotogramas) mientras el sistema procesa la transición autónoma hacia la escena final.
En la última pantalla, la interactividad pasa de ser un "botón" (clic) a ser un sensor de proximidad espacial (mouseX). El sistema vincula el cuerpo del usuario (su mano moviendo el ratón) con la escala de la geometría en la pantalla.    

Reglas:    
REGLA 1:   
El centro de la pantalla funciona como un botón circular invisible. El programa mide la distancia desde donde haces clic hasta el centro exacto de la pantalla.   

Si tu clic cae dentro del círculo central (a menos de 80 píxeles del centro), la bomba se activa y todo explota. Si haces clic en cualquier otra parte o sobre las fotos de las esquinas, el programa lo ignora y no pasa nada.

REGLA 2:
En la primera pantalla, los 5 círculos del centro no se agrandan ni se achican al mismo tiempo.   

El código le dice a cada círculo: "Espera un poquito antes de moverte". El círculo más pequeño empieza primero, el segundo se mueve un milisegundo después, luego el tercero, y así. Esto hace que en vez de un parpadeo aburrido, se vea como una ola o un latido de corazón que viaja hacia afuera.

REGLA 3:
El programa avanza en línea recta y tiene prohibido mezclar las pantallas.

Las tres escenas (El latido, La explosión y El agobio final) están separadas por paredes lógicas. Cuando pasas a la explosión, la primera pantalla se borra por completo de la memoria. No hay vuelta atrás ni se pueden ver dos escenas juntas.

REGLA 4:
En la última pantalla, el círculo rosa de la derecha está amarrado invisiblemente a tu mano.

El tamaño del círculo copia exactamente lo que hace tu mouse. Si mueves el mouse hacia la izquierda (cerca del cero), el círculo se encoge hasta casi desaparecer. Si arrastras el mouse hacia la derecha, el círculo se infla como un globo gigante hasta tapar casi toda la pantalla.

---
**REFERENTES**   

:[Pinterest](https://cl.pinterest.com/pin/343258802874909503/)  
:[Pinterest](https://cl.pinterest.com/pin/343258802874909504/)  
:[Pinterest](https://cl.pinterest.com/pin/343258802874909505/)  
:[Pinterest](https://cl.pinterest.com/pin/343258802874909521/)   

---
**DIAGRAMA DE FLUJO**   
<img width="381" height="2489" alt="DIAGRAMA DE FLUJO" src="https://github.com/user-attachments/assets/3a97f1dd-d813-4380-9fc9-61f0c9eda1aa" />

---
**CÓDIGO DE P5.JS**     
```
let cantidadCapas = 5; // Define cuántos círculos concéntricos tiene el diseño. En este caso, son 5 capas desde el centro hasta el exterior
let velocidadOnda = 0.04; // Controla qué tan rápido van a pulsar los círculos.
let exploto = false; // false = escena inicial, true = comienza la explosión y luego aparece la escena final
let momentoImpacto = 0; // Guarda el frame exacto en que ocurrió el click y calcula cuánto tiempo dura la "explosión"
let cantidad = 50; // Cantidad de líneas verticales de la escena final
let tiempo = 0; // Variable que controla el movimiento de las líneas y le asigno el valor 0
let creceEllip = 0; //Creo una variable llamada giraRect y le asigno el valor 0
let fontAdict; // Creo una variable llamada fontAdict que contiene la tipografía personalizada 
let giraRect = 0; // Variable que controla la rotación de los cuadrados
let img1; // Variables para almacenar las imágenes
let img2; // Variables para almacenar las imágenes
let img3; // Variables para almacenar las imágenes
let img4; // Variables para almacenar las imágenes

function preload() { // Función para cargar archivos externos antes de comenzar el programa

  fontAdict = loadFont('Acidic.TTF'); // Carga la tipografía personalizada
  img1 = loadImage("1.jpg"); // Carga las imágenes
  img2 = loadImage("2.jpg"); // Carga las imágenes
  img3 = loadImage("3.jpg"); // Carga las imágenes
  img4 = loadImage("4.jpg"); // Carga las imágenes
}

function setup() { // Función que se ejecuta una sola vez al inicio del programa

  createCanvas(600, 600); // Crea un lienzo de 600x600 píxeles
  noStroke(); // Elimina el borde de las figuras
}

function draw() { // Función que se ejecuta constantemente en bucle
  if (exploto === false) { // Mientras exploto sea false, se mostrará la escena inicial

    background(51, 2, 30); // Asigna el color burdeo oscuro al fondo del lienzo en valores RGB
    giraRect = giraRect+1; // Aumenta constantemente el valor de giraRect para generar la rotación

    push(); // Guarda el estado actual del lienzo
    rectMode(CENTER); // El cuadrado se dibuja desde el centro
    translate(120, 120); // Se traslada el cuadrado desde el punto de origen de x,y
    rotate(giraRect*90); // Rota el cuadrado según el ángulo definido
    fill(133, 100, 114); // Asigna el color morado al cuadrado en valores RGB
    square(0, 0, 80); //Crea un cuadrado en las coordenadas x,y
    pop(); // Cierra el estado actual del lienzo
    
    push(); // Guarda el estado actual del lienzo
    imageMode(CENTER); // La imagen se posiciona desde el centro
    image(img1, 120, 120, 70, 70); // Dibuja la imagen encima del cuadrado
    pop(); // Cierra el estado actual del lienzo

    
    push(); // Guarda el estado actual del lienzo
    rectMode(CENTER); // El cuadrado se dibuja desde el centro
    translate(480, 120); // Se traslada el cuadrado desde el punto de origen de x,y
    rotate(giraRect*90); // Rota el cuadrado según el ángulo definido
    fill(133, 100, 114); // Asigna el color morado al cuadrado en valores RGB
    square(0, 0, 80); //Crea un cuadrado en las coordenadas x,y
    pop(); // Cierra el estado del lienzo

    push(); // Guarda el estado actual del lienzo
    imageMode(CENTER); // La imagen se posiciona desde el centro
    image(img2, 480, 120, 70, 70); // Dibuja la imagen encima del cuadrado
    pop(); // Cierra el estado actual del lienzo


    push(); // Guarda el estado actual del lienzo
    rectMode(CENTER); // El cuadrado se dibuja desde el centro
    translate(120, 480); // Se traslada el cuadrado desde el punto de origen de x,y
    rotate(giraRect*90); // Rota el cuadrado según el ángulo definido
    fill(133, 100, 114); // Asigna el color morado al cuadrado en valores RGB
    square(0, 0, 80); //Crea un cuadrado en las coordenadas x,y
    pop(); // Cierra el estado del lienzo
    
    push(); // Guarda el estado actual del lienzo
    imageMode(CENTER); // La imagen se posiciona desde el centro
    image(img3, 120, 480, 70, 70); // Dibuja la imagen encima del cuadrado
    pop(); // Cierra el estado actual del lienzo


    push(); // Guarda el estado actual del lienzo
    rectMode(CENTER); // El cuadrado se dibuja desde el centro
    translate(480, 480); // Se traslada el cuadrado desde el punto de origen de x,y
    rotate(giraRect*90); // Rota el cuadrado según el ángulo definido
    fill(133, 100, 114); // Asigna el color morado al cuadrado en valores RGB
    square(0, 0, 80); //Crea un cuadrado en las coordenadas x,y
    pop(); // Cierra el estado del lienzo
    
    push(); // Guarda el estado actual del lienzo
    imageMode(CENTER); // La imagen se posiciona desde el centro
    image(img4, 480, 480, 70, 70); // Dibuja la imagen encima del cuadrado
    pop(); // Cierra el estado actual del lienzo


    push(); // Guarda el estado actual del lienzo

    translate(width / 2, height / 2); // Mueve el sistema de coordenadas al centro

    
    for (let i = cantidadCapas; i > 0; i--) { // Este bucle dibuja los círculos uno por uno, desde atrás hacia adelante

      let tamanoBase = map(i, 1, cantidadCapas, 60, 260); // Asigna que, si la capa es la 1, su tamaño base será 60px, el más pequeño. Si es la capa 5, su tamaño base será 260px, el más grande

      let t = frameCount * velocidadOnda - (i * 0.4); // Asigna que el movimiento sea constante. Se resta 'i * 0.4' para retrasar cada capa según su orden, evitando que pulsen al mismo tiempo, creando el efecto de "onda"

      let oscilacion = sin(t) * 25; // 'sin()' asigna un vaivén suave entre -1 y 1. Al multiplicarlo por 25, el círculo se encoge y agranda hasta 25 píxeles

      let diametroFinal = tamanoBase + oscilacion; // Suma el tamaño fijo de la capa con el vaivén del latido para obtener el diámetro real


      if (i === 1) {
        fill(242, 204, 219); // Si es la capa 1, aplica el rosa claro en valores RGB.

      } else if (i === 2) { 
        fill(224, 178, 198); // Si no, pero es la capa 2, aplica un rosa intermedio en valores RGB

      } else if (i === 3) {
        fill(186, 142, 161); // Si es la capa 3, aplica el tono pastel medio en valores RGB 

      } else if (i === 4) {
        fill(133, 100, 114); // Si es la capa 4, aplica el tono morado claro en valores RGB

      } else {
        fill(74, 55, 63); // Aplica el color morado oscuro a la capa 5 en valores RGB.

      }

      ellipse(0, 0, diametroFinal, diametroFinal); // Dibuja el círculo en el centro (0,0) usando el diámetro dinámico para el ancho y el alto

    }

    pop(); // Cierra el estado actual del lienzo

  } 
  
  else if (frameCount - momentoImpacto < 100) { // Controla cuánto tiempo dura la escena de la explosión

    background(51, 2, 30); // Asigna el color burdeo de fondo en valores RGB

    let tiempoPostImpacto = frameCount - momentoImpacto; // Calcula cuánto tiempo ha pasado desde el click

    
    push(); // Guarda el estado actual del lienzo

    translate(width / 2, height / 2); // Mueve el origen del lienzo al centro


    for (let p = 0; p < 40; p++) { // Crea 40 pelotitas pequeñas 

      randomSeed(p * 500); // Asigna que cada pelotita conserve el mismo patrón aleatorio

      let angulo = random(TWO_PI); // Genera un angulo aleatorio entre 0 y 360 grados

      let fuerzaEmpuje = random(1.5, 5); // Asigna una velocidad distinta a cada pelotita 


      let particulaX = // Dibuja cada pelotita en su poscición correspondiente 
      cos(angulo) * // Convierte el ángulo en coordenadas x para mover las pelotitas en distintas direcciones
      tiempoPostImpacto *
      fuerzaEmpuje;


      let particulaY = // Dibuja cada pelotita en su poscición correspondiente 
      sin(angulo) * // Convierte el ángulo en coordenadas y para mover las pelotitas en distintas direcciones
      tiempoPostImpacto * 
      fuerzaEmpuje;


      let tamanoParticula = random(8, 20); // Asigna una variable llamada tamañoParticula y esto quiere decir que cada pelotita de la explosión varía entre 8 y 20 píxeles


      if (p % 2 === 0) { // Esta condición revisa si p es un número par. Si se cumple, ejecuta el código dentro de las llaves que en este caso cambia el color de las pelotitas. El símbolo % calcula el resto de la división, entonces si al dividir p con 2 y el resto es 0 se cumple la condición 

        fill(242, 204, 219, 180); // Asigna el color rosado a las pelotitas en valor RGB

      } else { // Si la condición anerior no se cumple, se ejecuta la siguiente concidión

        fill(133, 100, 114, 180); // Asigna el color morado a las pelotitas en valor RGB

      }


      ellipse( // Dibuja una ellipse usando las coordenadas particulaX y particula Y para definir su posición
        particulaX,
        particulaY,
        tamanoParticula, // Asigna el alto y ancho de la ellipse
        tamanoParticula  // Asigna el alto y ancho de la ellipse
      );

    }

    pop(); // Cierra el estado actual del lienzo

  } 
  
  
  else { // Si la condición anerior no se cumple, se ejecuta la siguiente concidión

    background(51, 2, 30); // Asigna el color burdeo oscuro al fondo del lienzo en valores RGB

    push(); // Guarda el estado actual del lienzo

    translate(450, 300); // Mueve el origen al lado derecho del canvas
    scale(mouseX / 50); // Asigna que el tamaño del círculo dependa de la posición horizontal del mouse. Mienrtras más se mueve el mouse hacia la derecha, más se agranda
    fill(186, 142, 161); // Asigna el color rosado claro al círculo en valores RGB
    ellipse(0, 0, 50); // Dibuja un círculo en las coordenadas y tamaño asignado

    pop(); // Cierra el estado actual del lienzo

    
    for (let i = 0; i < cantidad; i++) { // Crea las 50 líneas verticales

      push(); // Guarda el estado actual del lienzo

      let x = map(i, 0, cantidad, 0, width / 1.5); // Distribuye las líneas horizontales a lo largo del canvas
      translate(x, 0); // Mueve el sistema de coordenadas horizontalmente según el valor de x, posicionando cada línea en distintos lugares del canvas

      let largoBase = height / 2; // Crea una variable llamada largoBase y le asigna la mitad de la altura del canvas, definiendo el tamaño base de la línea
      let variacion = sin(tiempo + i) * 200; // Genera una variación suave en el tamaño de las línea, creando un movimiento oscilante
      let largo = largoBase + variacion; // Suma el tamaño base con la variación animada para obtener el largo final de cada línea

      stroke(51, 2, 30); // Asigna el color del trazo de la línea en valores RGB
      line(0, 0, 0, largo); // Dibuja una línea vertical desde la coordenada 0, 0 hasta 0, largo
      noStroke(); // Elimina el borde de la figura
      fill(51, 2, 30); // Define el color de relleno de la figura
      ellipse(0, largo, 5); // Dibuja un pequeño círculo al final de la línea, en la poscición donde termina su largo

      pop(); // Cierra el estado actual del lienzo
    }

    tiempo += 0.01; // Aumenta poco a poco el valor de tiempo, permitiendo que la animación de las líneas siga moviendose

    
    // TEXTO
    push(); // Guarda el estado actual del lienzo

    translate(440, 100); // Mueve las coordenadas hacia la poscición 440, 100
    rotate(HALF_PI); // Rota el texto en 90 grados usando la constante HALF_PI
    fill(51, 2, 30); // Asigna el color burdeo al texto en valores RGB
    textFont(fontAdict); // Aplica la tipografía cargada anteriormente
    textSize(40); // Asigna el tamaño del texto en 40 píxeles
    textAlign(CENTER, CENTER); // Centra el texto horizontal y verticalmente
    text("AGOBIO", 0, 0); // Escribe la palabra agobio 

    pop(); // Cierra el estado actual del lienzo

  }

}

// CLICK
function mousePressed() { // Funciónalistas que se activa al momento de hacer click

  let distancia = dist( // Calcula la distancia entre la posición del mouse y el centro del canvas
    mouseX,
    mouseY,
    width / 2,
    height / 2
  );


  if (distancia < 80) { // Comprueba si el click ocurrió dentro del circulo central
    exploto = true; // Cambia el valor de exploto a true para activar la explosión y cambiar de escena 
    momentoImpacto = frameCount; // Guarda el momento exacto en el que ocurrió el click para calcular cuánto dura la explosión

  }

}
```

---
**LINK AL SKETCH EN P5.JS**     

:[p5.js](https://editor.p5js.org/Nissacontreras/sketches/LB1tjcvir)
