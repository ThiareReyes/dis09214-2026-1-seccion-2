# sesión 06 - 24/04

## IMPORTANTE
- Para nuestros apuntes de clase , SIEMPRE DEBEMOS OCUPAR .md ( es el que se usa para texto  y nos acepta el formato markdown )
- Llevar siempre al dia las bitacoras!!!
- Para agregar código de programación en nuestros apuntes de clases, debemos usar también el formato de markdown!!! . Se hace así: **``` código p5 ```**(bloque de código) **`código p5`** (Se usa entre medio de una oración)
- Cuando comentemos el código TIENE que ser con MAYOR DETALLE y PRECISIÓN , tenemos que pensar,  que si lo ve alguien que no sabe programar, esa persona lo pueda entender y replicar
- No es que angleMode(DEGREES) me sirva para hacer arcos o semi círculos, esta linea de comando solo configura el modo de medir los ángulos en grados

-----------------------------
### Pensamiento computacional 

⭐ 4 Pilares 
* **Descompoción:** Tomamos un problema grande y complejo, lo desmenuzamos, rompemos en las partes más pequeñas y manejables. Se traduce como **Funciones propias** (En lugar de un draw() gigante, tenemos una función dibujarIconos() y otra calcularDiferencia(), etc.....)
* **Reconocimiento de patrones:** Observamos tendencias o regularidades dentro de un problema, **SI** algo se repite o sigue una lógica constante, podemos automatizarlo, es como el **Bucles (for);** (Si hay un patrón, el código lo repite por ti con solo tres líneas)
* **Abstracción:** Filtramos la info innecesaria y nos quedamos solo con las características que definen el problema. O sea , es crear una representación simbólica de la realidad (Se traduce en el uso de **Variables y la función map()**. // Una posición de mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.
* **Algoritmos:** Es el diseño de una serie de reglas ordenadas para resolver el problema.Es el **"plan de acción"** que debe seguir el sistema (Se traduce en el **diagrama de flujo** y en las **condicionales (if/else)**. // Es el mapa lógico que conecta todas las partes anteriores

----------------------------------
### Tipos de interacción

1) Interacción discreta (EVENTOS) ------> Es un cuando ocurre un evento en especifico (clic) y el sistema responde **con una acción única** (EJ: aparecen círculos). Es un interruptor de *"encendido/apagado"* o *"acción/reacción"*. // SE suele ocupar en el mousePressed() o en el ifmouseIsPressed();
2) Interacción continua (INPUT DE DATOS) -----> Es cuando el sistema reacciona constantemente al mov o estado del usuario, sin necesidad de hacer algo especifico (clic). // Se puede usar EJ: mouseX o mouseY para hacer degradacion, afectar el color, tamaño, velocidad, etc....

----------------------------------------------
### FUNCIONES PROPIAS (Modularidad-Reusabilidad)

🪴 FUNCIÓN
  function(){
  }

* **Sintaxis:** function Nombredelafunción() { }
* **EJ:** [Pelota rebotando en las paredes como dvd]([https//url.com](https://editor.p5js.org/PoliMujica/sketches/oQCGBN6wX))


function draw() {

background(147, 104, 166);

DibujarFiguras();
}


Function Dibujarfiguras() {

stroke(70, 162, 247);
strokeWeight(4);

fill(40, 199, 64);

ellipse(pelota.x, pelota.y, 24, 24);
}



