# sesión 05 - 17/04  
# Transformaciones y condicionales  

**p5 mide ángulos en radianes.**  
**Radian:** medida cuando el perímetro exterior de un ángulo mide lo mismo que el radio.  

## Rotación: sirve para rotar elementos desde el punto de origen (0,0), se usa con translate para moverlo a otro punto, o rectMode(CENTER) para rotar desde el centro de la figura.  
( rotate(valor radianes o grados); )  

## Translate: traslada el punto de origen (0,0) a otra coordenada del canvas.  
( translate(x,y); )  

## Guardar y restaurar ( push(); pop(); )  
Trabajan juntas como un sistema de memoria temporal para el estilo y transformaciones del lienzo.  

## Escala ( scale(); )  
ajusta la escala del sistema de coordenadas actual por el especificado.  
( scale(x,y); )  

## Condicionales  
**expresión booleana:** enunciado, dato o instrucción que arroje verdadero o falso.  

**Operadores de Comparación:**
Permiten contrastar dos valores.  
* == (Igual a)
* != (Diferente de)
* \> o < (Mayor o menor que)
* \>= o <= (Mayor o igual / Menor o igual)  

**Operadores Lógicos:** Sirven para
combinar varias expresiones.
* AND (&&): Es verdadero sólo si
ambas partes son verdaderas.
* OR (||): Es verdadero si al menos
una de las partes es verdadera.
* NOT (!): Invierte el valor (si era
verdadero, pasa a ser falso).
  

## Sentencia condicional if-else if- else 
La sentencia if es una estructura especial que existe en casi todos los lenguajes de
programación; toma una condición –expresada como un booleano– y ejecuta una
pieza de código contenida dentro de las llaves { }  

La sentencia if puede complementarse con la sentencia else if, que añade
condiciones de prueba complementarias a la original, y con la sentencia else, que

implica todos los casos que no cumplen con la condición original.
(Nota: puedes añadir tantas sentencias else if como desees).  

If (condición) {ejecuta este código si es true} (Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar).
else if (condición 2) {ejecuta este código si es true} (Si no se cumple lo anterior SI la ayudante se levanta de su silla, la profesora debe cantar).
else {ejecuta este código si ambas condiciones son falsas} (Y SI NO SE CUMPLEN NINGUNA DE LAS ANTERIORES, los estudiantes guardan silencio).  




