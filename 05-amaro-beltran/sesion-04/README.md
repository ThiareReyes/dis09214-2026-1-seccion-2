# sesión 04 - 10/04  
# Datos dinámicos y Variables  

## Posición del mouse  
**mouseX;** - **mouseY;**  
Variables de sistema numérico que determinan la posición del mouse en las coordenadas X e Y.  
(mouseX, mouseY);  
ej: ellipse(mouseX, mouseY, 100, 100);  

## Crea variables propias  
Para declarar una variable podemos usar **let** para variables dinámicas y **const** para variables constantes.  
declarar variables (ej: let circuloAzul=0;)
indicar variables (ej: circuloAzul = circuloAzul+1; )
usar variables (ej: ellipse(circuloAzul,200,50,50); )  

## Javascript objects  
Sirve para organizar el código, permite agrupar valores relacionados bajo un mismo nombre.  
ej: ```let circulo = {
x:0,
y:200,
diameter:50,
};```  
Luego se accede a la información por medio de notación de puntos.  

## random();function  
Devuelve un número aleatorio dentro de un rango definido.  
ej: ```random(20,50);```  

## (width,height);  
Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.  

## (windowWidth, windowHeight);  
Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el createCanvas.  

## map();function  
``` map(valor, min_original, max_original, min_nuevo, max_nuevo);```  
valor: la variable a mapear (ej:mouseX)  
min/max_original: rango actual de ese valor  
min/max_nuevo: rango al cual transformar el valor  


