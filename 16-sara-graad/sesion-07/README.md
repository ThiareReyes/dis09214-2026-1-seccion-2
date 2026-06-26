# sesión 07 - 15/05
**Loops, while and for**  
¿que es un loop?   
Bucle: objeto cuyo forma recuerda la del bucle
Rae: informatica, serie de instrucciones que se reoiten idefinidamente mientras no se cumpla una condicion previamente establecida.

*loop*
es una estructura de control que permite ejecutar un bloque de instruccioes de manera repetida mientras se cumpla una condicion especifica o hasta que se alcance un estado determinado.  

#While#
3 elementos  
los bucles while son utiles para repetir instrucciones mientras una condicion sea verdadera. son como sentencias if
While ( condicion booleana) {ejecuta este codigo si es true}  
...
while(x < = height) {x = x + 1}
...  

**for**
Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles `for` son útiles para repetir instrucciones un
número determinado de veces.
Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

ejemplo: 
for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}

for (let x=0 ; x <= width; x=x+1) {ellipse (x , 200, random(300))}
