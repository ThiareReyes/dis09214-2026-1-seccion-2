# Sesión 09 - 12/06
# DISEÑO RESPONSIVO (windowResized)

## Sketch que se adapte a diferentes tamaños de pantalla 
1. Crear un canvas con dimensiones dinámicas:
- Para esto usaremos las variables integradas en el sistema: (windowWidth, windowHeight) estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.
<img width="475" height="102" alt="1" src="https://github.com/user-attachments/assets/8cefd23f-7422-4c87-a1ab-847bfb9e81e7" />

2. Crear un evento = windowResized()
- Si el usuario estira o encoge la ventana del navegador, el lienzo se adaptará al tamaño de la ventana en tiempo real.
<img width="467" height="111" alt="1" src="https://github.com/user-attachments/assets/49c14b8c-77b4-4d94-a980-5ca907430dc3" />

3. Usar valores relativos
- Ahora p5.js actualiza estas variables width y height automáticamente con el tamaño actual
del lienzo.

- Entonces ahora todos los valores de posición y tamaño que ocupemos los tenemos que pensar en relación proporcional a esas variables.

- Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)
<img width="693" height="666" alt="1" src="https://github.com/user-attachments/assets/5b7d497c-65e5-409f-a360-fe3f3cceb575" />

4. Incluir factor de referencia = referencia = min(width, height)
- Creamos una variable global (referencia) y la asignamos para
que calcule el mínimo.

- Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.
<img width="512" height="452" alt="1" src="https://github.com/user-attachments/assets/0e9f26c7-4f2f-4f26-8818-182c1a443185" />

5. Usar translate- push y pop = Consejo para proyectos complejos
- En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para "mover el origen del mundo”.

- Y siempre utilizando push() y pop() para cada figura o elemento.
<img width="377" height="406" alt="1" src="https://github.com/user-attachments/assets/b684e279-cfa5-4afa-8c86-583a386a06db" />

Desafío bandera mío: (https://editor.p5js.org/denisse.delgado2/sketches/o2UsIX1Ay)

### AGREGAR IMÁGENES = loadImage()
1.  Subir la imagen a p5
- a) Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.
- b) Hacer clic en el icono de + o el menú desplegable junto a Files.
- c) Seleccionar Upload file (Subir archivo).
- d) Arrastrar la imagen o buscarla en el computador.
- e) Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

2. Declarar y precargar la imagen = function preload()
- a) Creamos una variable global al inicio del código para guardar la imagen.
- b) Usamos la función dentro de function preload() y cargamos la imagen con loadImage()
<img width="406" height="173" alt="1" src="https://github.com/user-attachments/assets/2aeea2b6-848e-4810-b0ab-9b8ef7469fcd" />

3. Dibujar y dimensionar en el draw
- La imagen se dibuja usando la función image()
- Esta función requiere mínimo 3 argumentos, pero acepta 5 si queremos controlar su tamaño de forma responsiva.
- SINTAXIS: image(nombreVariableImagen, x, y, ancho, alto);
<img width="361" height="292" alt="1" src="https://github.com/user-attachments/assets/ad1dd620-519a-4da3-89d4-ea60feccc37c" />

- Ej mío imagen: https://editor.p5js.org/denisse.delgado2/sketches/ON4_9NxYk

#### EJEMPLOS AVANZADOS DE DISTORSIÓN DE IMAGEN = loadPixels()
- loadPixels() : Entrar en los pixeles
    *  Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.
    *  loadPixels() crea un "puente" temporal para que puedas analizar la información de forma masiva y fluida.

- MODIFICAR LOS PIXELES: 
get(x, y) — Lectura (El "Ojo")
    *  Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.
    *  Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).
    *  Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una copia de respaldo completa del lienzo.
set(x, y, nuevoColor) — Escritura (El "Pincel")
    *  Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por completo el color que existía ahí.
    *  Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo aspecto de la imagen.
updatePixels() — La Actualización
    *  Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la pantalla.
    *  ¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios en un borrador secreto. updatePixels() es el comando que efectivamente "publica" y renderiza el resultado final en el lienzo para que el usuario pueda verlo.

- EJEMPLOS DISTORSIÓN IMAGEN
    * DISTORSIÓN DE PIXELES CAMBIO A SOLO ROJO: (https://editor.p5js.org/PoliMujica/sketches/yX_ljcTGX)

    * DISTORSIÓN DE PIXELES EFECTO ALADINO: (https://editor.p5js.org/PoliMujica/sketches/jaEqYvHew)

    * DISTORSIÓN DE PIXELES ONDA SENO: (https://editor.p5js.org/PoliMujica/sketches/qnqADHqrC)

- Ej filtro mio: (https://editor.p5js.org/denisse.delgado2/sketches/tL_N-GAZB)
