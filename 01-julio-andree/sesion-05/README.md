# sesión 05 - 17/04
## Transformaciones y condicionales {if-else}  
### Angulos angleMode();  
Por defecto p5js usa radiales para medir ángulos. `angleMode(RADIANS)`  
Para cambiarlo a grados usamos `angleMode(DEGREES)` 
### Rotación rotate();  
Sirve para rotar elementos. Siempre rota al rededor del punto de origen(0,0). Se recomiendo usar con traslate(); y en algunos casos con rectMode(Center);  
Sintaxis: rotate(valor radiantes o en grados);  
Ej: `rotate(20);`  
### traslate  
sirve para trasladar el punto de origen origen (0,0) a otra coordenada en mi canvas.  
Sintaxis: traslate(x,y);  
Ej: `traslate(200,200);`  
### Guardar y restaurar {push(); & pop();}  
Funciones que trabajan juntas como "un sistema de memoria temporal". Todo lo que esté entre push y pop es sistema que se guarda para no ser modificado durante el código.  
Sintaxis: `push();` `pop();`  
### Escala scale();  
La función ajusta la escala del sistema del didtema de coordenadas actual por un valor especificado.  
Sintaxis: scale(x,y);  
Ej: `scale(2,2);`  
## Condicionales  
### Lógica condicional y expresión booleana  
### Expesión booleana  
Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: verdadero (True) o falso (false).  
Para construir este tipo de expresiones se utilizan 3 tipos de elementos:  
**Operandos (o Valores):** Son los datos básicos que se evalúan. Pueden ser:  
* Variables: como `x, y` o `mouseX, MouseY`, etc.
* Constantes o Literales: Valores fijos como 5, "hola" o los mismos valores booleanos true y False.
 **Operadores de Coomparación:** Permiten contrastar dos valores.
* `==` (igual a)
* `!=` (diferente de)
* `> o <` (mayor o menor que)
* `>= o <=` (mayor o igual / menor o igual)
**Operadores lógicos:** Sirven para combinar varias expresiones.  
* AND (&&): Es verdadero solo si ambas partes son verdaderas.
* OR (||): Es verdadero si al menos de las dos partes es verdadera.
* NOT (!): invierte el valor (si era verdadero, pasa a ser falso).
## Sentencias Condicionales {if - else if - else}  
La sentencia if es una estructura especial que existeen casi todos los lenguajes de programación; toma la condición -expresada como booleano- y ejecuta una pieza de código contenida dentro de las llaves {}.  
Ej: `if(condición){ejecuta este código si es true}`  
La sentencia **if** puede complementarse con la sentencia **else if**, que añade condiciones de pruebas complementarias a la original, y con la sentensia **else**, que implica todos los casos que no cumplen con la condición original. Puedes agregar tantas sentencias else if como desees.  
Ej: `if(condición) {ejecuta este código si es true} else if (condición 2) {ejecuta este código si es true} else {ejecuta este código si ambas condiciones son falsas}`.  
