# sesión 07 - 15/05  
# LOOPs, WHILE, FOR  

## loop  
repetición en bucle (infinita), serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida (RAE).  
Estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.  

## while (3 elementos)  
los bucles while son para repetir instrucciones mientras una condición sea verdadera, son como sentencias if que se repiten.  
while (condición booleana){si es true ejecuta este código en bucle}  
ej: ```while (x<= height){x=x+1}```  

## for (4 elementos)  
forma de repetir un bloque de código, cuando se conoce el número de iteraciones.Los bucles `for` son útiles para repetir instrucciones un número determinado de veces.
Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:  

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE  

for (inicialización variable; condición booleana; actualización){

Lo que queremos que pase cuando la condición sea verdadera
}  

ej: ```for (let x=0 ; x <= width; x=x+1) {
ellipse (x , 200, random(300))
} ``` 

## Nested loop (loop dentro de otro loop)  

for (inicialización variable; condición booleana; actualización){

Lo que queremos que pase cuando la condición sea verdadera

for (inicialización variable; condición booleana; actualización){
}
Lo que queremos que pase cuando la condición sea verdadera
}  

ejemplo: ```for (let x=0 ; x <= width; x=x+25) {  
for (let y=0 ; y <= height; y=y+25) {
fill (0, 0, 255);
ellipse (x , y, 15);
}  
} ``` 

## frameCount  
Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de `frameCount` es 0 dentro de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.  

