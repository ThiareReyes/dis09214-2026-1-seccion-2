# sesión 07 - 15/05

# LOOPS WHILE Y FOR

**Definicion de bucle:**  
- Rizo de cabello en forma helicoidal.  
- Objeto cuya forma recuerda a un bucle.  
- Proceso que se repite indefinidiamente.   
- En Informática, serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.   

### Loop;  
Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida, mientras se cumpla una condición específica hasta que se alcance un estado determinado.  

**While**: Los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repite.  
While (condición booleana) { si es true ejecute este código en bucle } 

- Ejemplo  
Mientras (x sea menor o igual que el alto de mi lienzo) { x incrementará 1 cada vez }  
```while (x <= height) { x=x+1 }```   

**For**  
Una forma de repetir un bloque de código cuando se conoce el número  
de iteraciones. Los bucles `for` son útiles para repetir instrucciones un  
número determinado de veces.  
Son una especie de SHORTCUT para hacer loops y siempre tienen 4  
elementos:  

1. Inicialización de una variable  
2. Condición booleana (V-F)  
3. Actualización ( Incrementación o decrementación)  
4. Lo que queremos que pasé cuando la condición sea TRUE

- Ejemplo

For (inicializo variable;condicion booleana;actualizacion){    
lo que queremos que pase cuando la condicion sea verdadera}  

```for(lex x=0 ; x <= widht; x=x+1) { ellipse(x,200,random(300)) }```  

**Nested loops**  
Loop dentro de otro loop   

-Ejemplo  

for (inicialización variable; condición booleana; actualización){ Lo que queremos que pase cuando la condición sea verdadera  
for (inicialización variable; condición booleana; actualización){  } Lo que queremos que pase cuando la condición sea verdadera }    

```for (let x=0 ; x <= width; x=x+25) { ```  
```for (let y=0 ; y <= height; y=y+25) { fill (0, 0, 255); ellipse (x , y, 15); } }```  

**FrameCount**  
Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de `frameCount` es 0 dentro de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.  





