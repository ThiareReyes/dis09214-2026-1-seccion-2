# sesión 05 - 17/04

# Transformaciones & Condicionales { If- else } 

* Si coloco * , multiplico
* Si coloco / divido
* Si coloco - en una variable, va para el otro sentido del reloj

### TRANSFORMACIONES

**¿Que son los radianes?**

-------> Es una unidad de medida de ángulos

<img width="277" height="236" alt="Captura de pantalla 2026-05-21 170430" src="https://github.com/user-attachments/assets/496fcba5-6b34-408b-92a4-4c8640d6f8c9" />

----------------------------
### ÁNGULOS
* **angleMode();**

⭐ Por defecto p5.js usa RADIANES para medir los ángulos
 **angleMode(RADIANS)**
⭐ Para cambiar a grados se usa esto en el fuction SETUP
 **angleMode(DEGREES)**

- Se mueven COMO LAS AGUJAS DEL RELOJ!

**TWO_PI 360** ̊  / 
**PI 180 ̊**  / 
**HALF_PI 90 ̊**  / 
**QUARTER_PI 45 ̊**  /

<img width="445" height="378" alt="Captura de pantalla 2026-05-21 170923" src="https://github.com/user-attachments/assets/1345353d-d234-40f7-ae7a-39de58b8db99" />

-----------------------------------------
### ROTACIÓN
* **rotate();**

-----> Sirve para rotar elementos. **SIEMPRE ROTA ALREDEDOR DEL PUNTO 0,0**
  * Se recomienda usarlo con translate(); y en algunos casos con rectMode(CENTER);
  * El reactMode(CENTER); si lo coloco en el setup, TODAS mis figuras giran en el centro
  * Si ocupamos translate , siempre va a estar primero translate y despues rotate, porque si no se buguea

⭐ Sintaxis: rotate(valor radianes o en grados);
⭐ EJ: rotate(20);
<img width="1175" height="461" alt="Captura de pantalla 2026-05-21 171402" src="https://github.com/user-attachments/assets/d030b699-ce5b-4131-aeb9-8f5e08a3cfb3" />

### TRASLADAR
* **translate();**

-----> Sirve para trasladar el **PUNTO DE ORIGEN (0,0)** a otra cordenada de mi canvas

⭐ Sintaxis: translate(x,y);
⭐ EJ: translate(200,200);

-------------------------------------------
### GUARDAR Y RESTAURAR
* **push(); y pop();**

*  Se ocupan SIEMPRE juntas , si no no funcionan
*  Son funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo
*  Es para que las variables que colocamos, no afecten a las demas 

⭐ Sintaxis: push(); y pop();
⭐ EJ: <img width="271" height="187" alt="Captura de pantalla 2026-05-21 172234" src="https://github.com/user-attachments/assets/c35a9352-3c03-4fd4-9865-8ef7bdcb8818" />

- Se pueden ocupar con varias funciones.

-------------------------------------------
### ESCALA
* **scale();**

-----> Ajusta la escala del sistema de coordenadas actual por el factor especificado
* Es como si hiciera un ZOOM en el canvas, a la figura, sin cambiar su borde, simplemente agranda la figura

⭐ Sintaxis: scale(x,y);
⭐ EJ: scale(2,2); // puede ser con cualquier n°
<img width="1346" height="377" alt="Captura de pantalla 2026-05-21 172659" src="https://github.com/user-attachments/assets/94eee7f2-304f-417c-80c0-b5c61aa4dd00" />

--------------------------------------------------
## CONDICIONALES: EXPRESIÓN BOOLEANA Y LÓGICA CONDICIONAL

* **EXPRESIÓN BOOLEANA**
------> Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: **verdadero (True**) o **falso (False)**
💮 EJ: Si algún estudiante apaga por completo las luces de la sala, la profesora debe hacer un backflip

* Para que construir este tipo de expresiones se ***UTILIZAN 3 TIPOS DE ELEMENTOS***

#### OPERADORES

💜 **Operandos (o Valores):** Son los datos básicos que se evalúan, pueden ser:
• Variables: (como x, y o mouseX,mouseY, etc)
• Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanos True y False

💙 **Operadores de Comparación:** Permiten contrastar dos valores
• == (Igual a)
• != (Diferente de)
• > o < (Mayor o menor que)
• >= o <= (Mayor o igual / Menor o igual)

🧡 **Operadores Lógicos:** Sirven para combinar varias expresiones
• AND (&&): Es verdadero solo si ambas partes son verdaderas
• OR (||): Es verdadero si al menos una de las partes es verdadera
• NOT (!): Invierte el valor (si era verdadero, pasa a ser falso)

------------------------------------------
### SENTENCIA CONDICIONAL: IF-ELSE IF-ELSE

-------> La sentencia **if** es una **estructura especial** que existe en casi todos los lenguajes de programación; toma una condición ***–expresada como un booleano–*** y ejecuta una pieza de código contenida dentro de las llaves { }

* If (condicion) {ejecuta este código si es true} // Es si pasa esto.....
  EJ: Si algún estudiante aplaude, la profesora debe cantar.

* SE PUEDE COMPLEMENTAR el **If** con: **else if** que (añade condiciones de prueba complementarias a la original) y la **else** (que implica todos los casos que no cumplen con la condición original)
* Podemos AÑADIR cuantas sentencias queramos!!!

- if (condicion){ejecuta este código si es true}
- else if(condicion 2){ejecuta este código si es true}
- else{ejecuta este código si ambas condiciones son falsas}

⭐ O SEA : 
- Si algún estudiante aplaude, la profesora debe cantar
- Si no se cumple lo anterior SI la ayudante se levanta de su silla, la profesora debe bailar cueca
- Y SI NO SE CUMPLEN NINGUNA DE LAS ANTERIORES, los estudiantes colocan cara de enojados
  
- EJ: <img width="1468" height="501" alt="Captura de pantalla 2026-05-21 174834" src="https://github.com/user-attachments/assets/d8c38eb2-3650-4756-915b-73acc3556798" />

-------------------------------------------
**ENCARGO 4**
[Encargo 4 p5.js ]([https//url.com](https://editor.p5js.org/gabyferradaexe/sketches/WvXsEv_6y)) 






