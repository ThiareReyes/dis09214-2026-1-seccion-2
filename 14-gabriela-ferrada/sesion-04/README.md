# sesión 04 - 10/04

# Datos dinámicos *{ Variables }*
-------> MOVIMIENTO 

* Hay variables que son constantes o que van cambiando

----------------------------------------
### Pocisión del mouse

-----> Son variables del sistema numérico que determinan la pocisión del mouse en las coordenadas X e Y

- mouseX           
- mouseY

Sintaxis: (mouseX,mouseY);
Ejemplo: ellipse (mouseX,mouseY,100,100);

* Cada 60 veces x segundo (se mueve el mouseX) (Cada vez que se mueve el mouse , pinta con mov, no alcanza a ser estela)
<img width="1447" height="483" alt="mouse jpg" src="https://github.com/user-attachments/assets/d86ea1a9-ef91-46aa-a572-43bfcea955b6" />

¿Que pasa si pongo el **background** en el **function setup**? ----> Deja una estela, o sea pinta el fondo (una vez) por decirlo asi.

- Si pongo el mouseX o el mouseY, en fill, empieza a tener una degradación del color (R,G,B)

----------------------------------------------------------

* Hay muchas más variables integradas como: widht, height, mouseIsPressed, mouseBotton,frameCount,etc....

### Crea tus propias variables :D

-----> Para declarar variables podemos usar **LET** PARA VARIABLES DINÁMICAS (para que el n° cambie) Y **CONS** para VARIABLES CONSTANTES (no cambia)
   * Antiguamente se ocupaba *var* en vez de let, en tutoriales antiguos se pueden ver

⭐ HAY 3 PARTES IMPORTANTES:

1) Declarar tu variable: **SIEMPRE OCUPAR LET AL PRINCIPIO DE TODO, ANTES QUE FUNCTION SETUP Y DRAW**
  * Le podemos colocar el nombre que nosotros queramos
     * Siempre en minuscúla y si cambiamos de palabra en MAYÚSCULA
   
- Si coloco en fucntion draw, EJ: (ya lo declare al principio del todo) circuloMorado = circuloMorado + 1 (AUMENTA LA VELOC del ellipse en este caso, si coloco ellipse)
  <img width="832" height="376" alt="Captura de pantalla 2026-05-21 162744" src="https://github.com/user-attachments/assets/8b8ac74a-4e4d-42dd-b427-8f63b7974350" />

2) Si ya declaré el circuloMorado primero, lo puedo ocupar ya todas la veces que yo quiera
- Si colocamos en el background el circuloMorado, cambia la tonalidad de degradación y si lo coloco en EJ: ellipse(circuloMorado,circuloMorado,50,50) CAMBIA random en donde va el ellipse y si le coloco un ----> ellipse(circuloMorado,circuloMorado +2,50,50) VA A IR MÁS RAPIDO.

-----------------------------------------------------------
### JAVASCRIPTS OBJECTS

-----> Nos servirán para organizar nuestro código de una forma adecuada y ordenada, es la forma de agrupar muchas variables dentro de una variable.
* Es una estructura de datos que te permite agrupar valores relacionados bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un **contenedor** que organiza la información mediante pares de clave y valor. Despues podemos acceder a la info de las variables mediante notación de punto.
<img width="1580" height="492" alt="Captura de pantalla 2026-05-21 165142" src="https://github.com/user-attachments/assets/35b97cf7-eb5d-4aaa-98ed-0acc55374cbb" />
EJ: <img width="1320" height="491" alt="Captura de pantalla 2026-05-21 163721" src="https://github.com/user-attachments/assets/f9050ec3-ce81-4875-ac78-88e8456a4776" />

----------------------------------------------------------------
### Random(); function

-----> Es devolver un n° aleatorio dentro de un rango que tú definas

-EJ: random(): Si no pones nada, devuelve un número decimal entre 0 y 1
     Ejemplo: random() da 0.4571.

-EJ: random(máximo): Devuelve un número decimal entre 0 y el máximo que elijas.
     Ejemplo: random(100) da un número entre 0 y 100.

-EJ: random(mínimo, máximo): Devuelve un número decimal entre esos dos valores.
     Ejemplo: random(20, 50) da un número entre 20 y 50.

EJ: <img width="1352" height="507" alt="Captura de pantalla 2026-05-21 164310" src="https://github.com/user-attachments/assets/ed31314a-e9da-4875-af13-e3e95b5f0ac9" />

#### (Width y Height); 

-----> Permiten ajustar el tamaño del lienzo
* y el **(windowWidht,windowHeight); -----> Permiten ajustar el tamaño del lienzo pero en pág web

--------------------------------------------------------------
### map(); function

------> Permite convertir un valor de un rango a otro , o sea toma un n° que está en una *escala* y lo proporcionalmente a una *escala* NUEVA.
* Sintaxis: map(valor, min_original, max_original, min_nuevo, max_nuevo)
  - **Valor:** La variable que quieres "mapear" (por ejemplo, mouseX)
  - **min_original y max_original:** El rango en el que se encuentra ese valor actualmente
  - **min_nuevo y max_nuevo:** El rango al que lo quieres transformar
EJ: <img width="1580" height="492" alt="Captura de pantalla 2026-05-21 165142" src="https://github.com/user-attachments/assets/d59ea203-b342-4997-a0f0-226c3f430ce2" />

------------------------------------------------
**TAREA ROMPER LA ESTÁTICA** 
- Usar las nuevas variables en nuestra solemne 1
[Desafío 2]([https//url.com](https://editor.p5js.org/gabyferradaexe/sketches/2hdQqRwke))
