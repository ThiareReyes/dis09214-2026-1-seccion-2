# sesión 04 - 17/04

**Transformaciones y Condicionales en p5.js**  
***Ángulos y Modos***  
Por defecto, p5.js utiliza Radianes para medir ángulos. Para trabajar de forma más intuitiva, podemos cambiar a Grados.
angleMode(DEGREES);: Se coloca en el setup() para usar grados (0 a 360).

Equivalencias clave:  
HALF_PI = 90°  
PI = 180°  
TWO_PI = 360°  

***Transformaciones***  
Las transformaciones alteran el sistema de coordenadas del lienzo. Es fundamental entender que no mueves el objeto, mueves el papel (lienzo).  

translate(x, y): Desplaza el punto de origen (0,0) a una nueva posición.  
rotate(ángulo): Rota el lienzo sobre el punto de origen actual.  

push(): Guarda el estado actual de la configuración (estilos y transformaciones).  
pop(): Restaura la configuración al estado guardado por el último push().  
Uso: Evitan que una transformación (como un rotate) afecte a todo lo que se dibuja después.  

***Condicionales (Estructuras de Control)***  
Permiten que el programa tome decisiones basándose en si una condición es verdadera (true) o falsa (false).

Estructura if / else
if (Si): Ejecuta el código solo si la condición se cumple.  
else if (Si no, si): Evalúa una nueva condición si la anterior fue falsa.  
else (Si no): Ejecuta un código por defecto si ninguna de las condiciones anteriores se cumplió.  

***Operadores de Comparación y Lógicos***  
Se usan dentro de los paréntesis del if.

Comparación:

> (Mayor que) / < (Menor que)

>= (Mayor o igual) / <= (Menor o igual)

=== (Igual a) / !== (Distinto de)

Lógicos:

&& (AND / Y): Ambas condiciones deben ser verdaderas.

|| (OR / O): Al menos una condición debe ser verdadera.

! (NOT / NO): Invierte el valor (lo que es verdadero pasa a ser falso).  

***Interacción de Teclado***  
key: Variable que almacena la última tecla presionada (ej: 'a', 'b').  
keyCode: Se usa para teclas especiales como UP_ARROW, DOWN_ARROW, ENTER, SHIFT.  
