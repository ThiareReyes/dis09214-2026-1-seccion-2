# sesión 10 - 05/06

# Estados y cámara web
- Esto también tiene que tener nuestro examen, por lo menos 3 estados , que se resete con una tecla o interacción con el mouse, etc... (los 3 estados pueden ser uno igual entre los 3)
- Tratar de hacer cosas nuevas!!! con lo que nos enseñan.

------------------------------------------
**¿Cómo creamos un sketch con estados diferentes?**

1) PASO 
-----> Al principio del código (a fuera de las funciones), debemos crear una variable que guarde en qué pantalla nos encontramos. Empieza en 0
* let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final

⭐ Podemos colocar cuantos queramos (estados)

⭐ Se declara arriba del todo

2) PASO: Function setup
-----> Creamos el lienzo de fondo donde va a ocurrir todo LO MAGICO!
<img width="335" height="163" alt="Captura de pantalla 2026-06-06 174054" src="https://github.com/user-attachments/assets/92bd218c-eb7a-439a-8cd7-3c9674df8f94" />

3) PASO: Function draw
-----> Creamos la estructura del estado (function draw) : Aqui usamos un **switch**, dependiendo del valor de la variable **estado**, el programa dibujará una cosa u otra.
<img width="306" height="407" alt="image" src="https://github.com/user-attachments/assets/7c99d903-0d40-4295-88e7-af4ebde2dd9c" />

⭐ Colocamos un switch dependiendo el valor que tengan las variables del estado, se recomienda usar una función propia (ahí colocamos todo lo que va en la pantalla de inicio)

⭐ El break es para detener la pantalla, no sigue avanzando.

4) PASO: Funciones propias
-----> Ahora creamos las funciones que inventamos en el paso anterior y cada una tendrá un diseño y un color diferente para que se note el cambio que vamos hacer.
<img width="537" height="455" alt="Captura de pantalla 2026-06-06 183634" src="https://github.com/user-attachments/assets/75524fc1-eda8-41f2-b59b-ac326611911f" />

5) PASO: Lógica del cambio y del inicio
------> Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0, o sea se reinicia (* para el examen debemos ocupar esto*)
<img width="537" height="455" alt="Captura de pantalla 2026-06-06 183634" src="https://github.com/user-attachments/assets/131c72d2-a93e-4ace-b038-52f8435a5a3b" />

⭐ Para que funcione el mouse pressed o key pressed se tiene que colocar al final del codigo.
[Ej profe](https://editor.p5js.org/PoliMujica/sketches/9vHePO158) 


## OJO igual hay otras formas distintas de cambiar de estado a otro

-------------------------------------------------------------
### A) Interacción con el teclado

🩷 Por barra espaciadora o enter :
<img width="456" height="125" alt="Captura de pantalla 2026-06-07 144749" src="https://github.com/user-attachments/assets/e4b1142d-b067-402f-89c3-071c1927989b" />

💛 Por teclas específicas:
<img width="282" height="120" alt="Captura de pantalla 2026-06-07 144754" src="https://github.com/user-attachments/assets/2c0f7884-adfc-48ca-a7ce-44e32c9fc1d4" />

[EJ profe](https://editor.p5js.org/PoliMujica/sketches/peTm3oGty) 

### B) Botones reales en la pantalla

💙 En lugar de hacer click en la pantalla , creamos un boton con HTML (es de la libreria de p5.js), se ocupa para que quede mas professional
<img width="487" height="322" alt="Captura de pantalla 2026-06-07 145050" src="https://github.com/user-attachments/assets/c53fb873-276c-4d46-890a-51dca0e713a9" />

[EJ profe](https://editor.p5js.org/PoliMujica/sketches/peTm3oGty) 

### C) Con zonas de click

💚 Si no queremos usar HTML, nosotros podemos definir el lugar en donde queramos apretar nuestro botón, podemos oucpar rect (es más facil, que hacer ellipse)
<img width="505" height="137" alt="Captura de pantalla 2026-06-07 145453" src="https://github.com/user-attachments/assets/5c6f8653-a03a-4b92-bb87-0886d5157df4" />

[Ej profe](https://editor.p5js.org/PoliMujica/sketches/iw-gjFhK8)

### D) Interacciones automáticas x tiempo

🤎 Esto es ideal para que una pantalla dure una cierta cantidad de tiempo que queramos (es como un splash) y pasa sola al menú
* Se pone en el function draw();
<img width="472" height="90" alt="Captura de pantalla 2026-06-07 145925" src="https://github.com/user-attachments/assets/5220f620-872b-4009-a169-474d6199a96e" />

[EJ profe](https://editor.p5js.org/PoliMujica/sketches/_AunxbPWQ) 

------------------------------------------------------------
# Camara WEB

**¿Como se crea?**

- createCapture(VIDEO); -----> Este es el comando **ESPECIAL**
1) Esto crea la variable para la captura, se declara una variable global que guarda el flujo de video de tu cámara web.
2) Se parte/inicializa la cámara en la function setup() utilizamos el comando especial **createCapture(VIDEO)** esto pedirá permiso al navegador para encender la cámara del computador. También definimos el tamaño con captura.size(x,y); y SUPER importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
3) Dibujamos la cámara en el **function draw()** , usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
[EJ para entender mejor](https://editor.p5js.org/gabyferradaexe/sketches/pFQSwPDp9) 

📸 EJEMPLOS DE CÁMARA INTERACTIVA (profe) yupiii
* [Encender y apagar cámara](https://editor.p5js.org/PoliMujica/sketches/Xdk0YBVbQ)
* [Filtro](https://editor.p5js.org/PoliMujica/sketches/sK_BYepGn)
* [Pixel reaccionan al volumen](https://editor.p5js.org/PoliMujica/sketches/L9QBzREF3)

