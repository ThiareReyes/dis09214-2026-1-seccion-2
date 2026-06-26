# 🌸 Clase 10/04 - Datos dinámicos "Variables" 🌸

### ¿Que es una variable? 

- Una variable es un nombre que se usa para guardar un valor que puede cambiar.
Es como una caja donde puedes guardar datos (números, texto, etc.) y usarlos después.

### Variable MouseX y MouseY 

- mouseX: sigue la posición horizontal del ratón.
- mouseY: sigue la posición vertical del ratón.

Si pongo background() en draw(), el fondo se borra todo el tiempo. Si lo pongo en setup(), solo se borra una vez.

La función draw() por defecto se ejecuta aproximadamente a 60 fotogramas por segundo.

mousePressed(): es una función que se ejecuta cuando se presiona el botón del mouse. 

<img width="762" height="345" alt="image" src="https://github.com/user-attachments/assets/b8ebb5d4-b0fa-47c4-88d1-a907bf8ad92f" />
<img width="762" height="390" alt="image" src="https://github.com/user-attachments/assets/2887e02b-d757-4860-979d-923da8f75130" />

### ¿Como hago mi propia variable? 

Para declarar una variable podemos usar

- **let** para variables dinámicas 
- **const** para variables constantes

  1. DECLARAR TU VARIABLE
  2. INICIALIZA TU VARIABLE
  3. USA TU VARIABLE

### Incrementation operators aumentar el valor de una variable en 1 o más.
Ejemplo:

let x = 100;   
draw   
x= x +5  O  x += 5  

esto sirve para todas las operaciones matematicas 

### Javascript Objects

- Sirven para guardar y organizar información en una sola estructura.  
- Se forman con pares de clave y valor, como nombre y edad dentro de una persona.  
- Permiten acceder y manejar información de forma más ordenada y fácil de usar.  

let persona = {   
  nombre: "Ana",    
  edad: 15,    
  ciudad: "Santiago"    
};    

### Random()fuction

Su trabajo es devolver un número aleatorio dentro de un rango que tú definas.

- random(): Si no pones nada, devuelve un número decimal entre 0 y 1
- random(máximo): Devuelve un número decimal entre 0 y el máximo que elijas.
- random(mínimo, máximo): Devuelve un número decimal entre esos dos valores.

### (width , height); 
Variables integradas en p5, que correspondena los valores definidos en el createCanvas.

### (windowWidth, windowHeight);
Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana delnavegador. Se usan en el createCanvas.

### map fuction 
Esta función nos permite convertir un valor de un rango a otro.

"map(valor, min_original, max_original, min_nuevo, max_nuevo)" 
---
Desafio 

1. Hacer un duplicado del dibujo que entregaron para la solemne.
2.Darle movimiento al dibujo en p5.js.
3.Usando cada una de las variables y funciones que aprendimos hoy;

•mouseX mouseY
•let creado por mi
•Javascript object
•Random fuction
•Width height
•WindowWidth WindowHeight
•Map función

Mi entrega : https://editor.p5js.org/amanda.venegas1/sketches/Wy4-n-Mfx 
---
