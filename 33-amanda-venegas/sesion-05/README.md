# 🌸 Clase 17/04 - Transformaciones y condicionales 🌸

### Rotacion de figuras 

La funcion *rotate()* sirve para rotar el sistema de cordenadas 

"rotare(angulo)": ->  este angulo se puede trabajar de dos maneras en radianes o en algulos  

O° son 0 radiales   
90° seria PI/2  
180 son Pi radiales     
360 son TWO_PI     

TWO_PI 360 ̊  
PI 180 ̊  
HALF_PI 90 ̊  
---
---

### Expresion booleana:  
Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles:

Verdadero (True) o Falso (False).  

**Es como hacer una afirmación y preguntarse: ¿esto es cierto o no?**

5 > 3 → verdadero  
10 == 7 → falso  

Para construir este tipo de expresiones se utilizan **3 tipos de elementos:**

1.  Operandos (o Valores): 

Son los datos básicos que se evalúan. Pueden ser:

- Variables: (como x, y o mouseX, mouseY, etc).

- Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanos True y False.

2. Operadores de Comparación:

Permiten contrastar dos valores.

== (Igual a)  
!= (Diferente de)  
> o < (Mayor o menor que)
> >= o <= (Mayor o igual / Menor o igual)  

3. Operadores Lógicos: 

Sirven para combinar varias expresiones.

AND (&&): Es verdadero solo si ambas partes son verdaderas.  
OR (||): Es verdadero si al menos una de las partes es verdadera.  
NOT (!): Invierte el valor (si era verdadero, pasa a ser falso).  

(5 > 3) AND (2 < 4) → verdadero  
(10 == 5) OR (3 > 1) → verdadero  
NOT (7 < 2) → verdadero 

<img width="879" height="495" alt="image" src="https://github.com/user-attachments/assets/7ea65db7-1bf1-4c79-908f-0a31237ee85b" />
<img width="879" height="495" alt="image" src="https://github.com/user-attachments/assets/aaa14145-a2bf-46a3-80d1-6a33172ec84c" />
<img width="878" height="493" alt="image" src="https://github.com/user-attachments/assets/6d4db318-8a4d-4f61-b099-f721b365a2e6" />


---
---
# Sentencia condicional

### ¿como puede un programa tomar diferentes caminos ?
Comparando valores 

Permite a un programa tomar decisiones "si se cumple esta condición, haz esto; si no, haz otra cosa”.

## If - else if - else 

La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición –expresada como un booleano– y ejecuta una pieza de código contenida dentro de las llaves { }

If -> if (condicion) {accion}

Ejemplo :
Si la edad es mayor o igual a 18, se muestra el mensaje 'Eres mayor de edad'. De lo contrario, se muestra 'Eres menor de edad'."

edad = 18

if (edad >= 18) {
    imprimir("Eres mayor de edad")
} else {
    imprimir("Eres menor de edad")
}

## Variantes  else if 

if (Si...): Es la primera pregunta. Si es verdad, entra aquí y ignora todo lo demás.

else if (Pero si...): Solo se pregunta esto si la primera fue falsa. Puedes tener tantos como quieras.

else (Si nada de lo anterior funcionó...): Es tu plan de reserva, lo que pasa si ninguna condición se cumplió.

Ejemplo 

Si la nota es mayor que 6 sale mensaje de aprobado si no cumple con lo anterior peros si la nota es mayor que 4 sale mensaje de recuperacion y si no cumple ninguna de las anteriores sale mensaje de reprobado 

if (nota >= 6) {  
    imprimir("Aprobado")  
} else if (nota >= 4) {  
    imprimir("Recuperación")  
} else {  
    imprimir("Reprobado")  
}  

--- 
Tarea / Desafio 

Deben crear un Sketch LIBRE, que incluya:

- Varias figuras geométricas
- Rotación
- Translate
- Push Pop
- Scale
- Texto https://p5js.org/es/search/?term=text
- Imagen https://p5js.org/es/search/?term=image https://editor.p5js.org/PoliMujica/sketches/nm0fj2seC
- 2 sentencias condicionales completas (If - else if - else)

Mi entrega : https://editor.p5js.org/amanda.venegas1/sketches/baVQi8Xlj

---
---
# Cuatro pilares 

1. Descomposición
2. Reconocimiento de patrones
3. Abstracción
4. Algoritmos 

## 1- Descomposición 
"Dividir para conquistar"

Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y
manejables.

- En diseño: Si quieres visualizar la "Brecha Salarial", no programas todo de una vez.
Primero diseñas cómo se ve el "Sueldo A", luego el "Sueldo B", luego la "Interacción" y
finalmente el "Fondo".

- En el código: Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante,
tienes una función dibujarIconos() y otra calcularDiferencia(), etc.

## 2- Reconocimiento de patrones 

"Encontrar similitudes"

Es observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una
lógica constante, podemos automatizarlo.

- En diseño: Notas que para representar a 100 personas, no necesitas dibujar 100 veces.
Notas que todas son un círculo con una posición x distinta.

- En el código: Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por
ti con solo tres líneas.

## 3.Anstracción 

"Lo importante vs. el detalle"

Es filtrar la información innecesaria y quedarse solo con las características que definen el
problema. Es crear una representación simbólica de la realidad.

-  En diseño: Para representar la "presión social" no necesitas dibujar a toda la sociedad;
quizás un círculo que se achica cuando el mouse se acerca es suficiente.

-  En el código: Se traduce en el uso de Variables y la función map(). Una posición de
mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.


## 4- Algoritmos 

"La receta paso a paso”

Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el "plan de
acción" que debe seguir el sistema.

- En diseño: Es el flujo de la experiencia. "Si el usuario hace esto, pasa aquello; si no,
pasa esto otro”.
- En el código: Se traduce en el Diagrama de Flujo y en las Condicionales (if/else). Es el
mapa lógico que conecta todas las partes anteriores.

---
# Tipos de interacción 

### 1. Interacción Discreta (Eventos)

Es cuando curre un evento específico (clic) y el sistema responde con una acción única (aparecen
círculos). Es un interruptor de "encendido/apagado" o "acción/reacción".

- En el código: Se suele usar dentro de la función mousePressed() o con un if(mouseIsPressed).

### 2. Interacción Continua (Input de Datos)
   
Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad
de hacer algo especifico (clic).

- En el código: Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad
de algo.

## Funciones propias 
se divide en ** Modularidad** y **Reusabilidad**



---
---

## Solemne 2 

1. El Desafío
   
El objetivo de esta Solemne no es demostrar expertiz técnica en programación, sino demostrar capacidad de razonamiento
lógico y sistémico. Deberán diseñar un "organismo visual" en p5.js que funcione mediante reglas preestablecidas para
visibilizar una problemática de genero.
Lo más importante es cómo traduces un problema social a una regla de comportamiento computacional.

2. Marco Conceptual: Las 4 Columnas del PC
   
Su proyecto será evaluado bajo los cuatro pilares del pensamiento computacional:

- Descomposición: ¿Dividiste tu problemática en partes más pequeñas y manejables (funciones)?

- Reconocimiento de Patrones: ¿Usaste ciclos para crear estructuras o repeticiones con sentido (loops -for)?

- Abstracción: ¿Lograste que un movimiento o cambio visual represente un concepto real (ej. usar map para que el mouse
represente "presión social")?

- Algoritmos: ¿Tu diagrama de flujo explica paso a paso cómo funciona tu sistema?
