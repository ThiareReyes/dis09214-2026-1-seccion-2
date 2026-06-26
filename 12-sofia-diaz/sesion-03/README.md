# sesión 03 - 10/04

**Datos Dinámicos y Variables en p5.js**  
***Variables Integradas (System Variables)***:  
Son variables que p5.js ya tiene definidas y cuyo valor se actualiza automáticamente.  

Posición del Mouse  
mouseX: Posición horizontal (eje X) actual del cursor.  
mouseY: Posición vertical (eje Y) actual del cursor.  
pmouseX: Posición horizontal del mouse en el cuadro anterior (útil para calcular velocidad).  

Dimensiones del Lienzo y Ventana   
width: Ancho del lienzo definido en createCanvas().  
height: Alto del lienzo definido en createCanvas().  
windowWidth: Ancho total de la ventana del navegador.  
windowHeight: Alto total de la ventana del navegador.  
Nota: Estas últimas permiten que el lienzo se ajuste al tamaño de la pantalla   

Interacción y Tiempo   
mouseIsPressed: Booleano (true/false) que indica si se está presionando un botón del mouse.  
keyIsPressed: Indica si hay alguna tecla presionada.  
frameCount: Contador de cuadros transcurridos desde que inició el sketch.  

***Creación de Variables Propias***   
Para gestionar datos personalizados se deben seguir tres pasos:  
Declarar: Se crea el nombre de la variable usando let (para valores que cambian) o const (para valores fijos). 
Ejemplo: let circuloX = 0;.  
Inicializar: Se le asigna un valor inicial, usualmente fuera de las funciones o en setup().  
Usar: Se emplea la variable dentro de funciones como draw() para generar cambios.  

Objetos en JavaScript:  
Estructura de datos que permite agrupar múltiples valores relacionados (pares de clave y valor) bajo un solo nombre para mantener el código ordenado.  
Sintaxis: Se definen entre llaves {} y se accede a sus propiedades usando la notación   

Funciones Útiles:  
random():  
Genera números aleatorios para crear comportamientos impredecibles.
 Decimal entre 0 y 1.  
random(max): Decimal entre 0 y el valor máximo.  
random(min, max): Decimal entre un rango específico.

map(): 
Reasigna un valor de un rango a otro proporcionalmente.  
Sintaxis: map(valor, min_original, max_original, min_nuevo, max_nuevo).  
Uso común: Convertir la posición del mouse (0 a width) en un color (0 a 255).
