# CLASE 10

12/6


## Diseño responsivo e imagenes

# Diseño responsivo

Permite que un sketch se adapte a distintos tamaños de pantalla.



**Paso 1**
Crear un canvas con dimensiones dinamicas

Se usan las variables:

- windowWidth
- windowHeight

Estas leen constantemente el ancho y alto de la ventana del navegador.



**Paso 2**
 windowResized()

Si el usuario cambia el tamaño de la ventana, el lienzo se adapta automaticamente.



**Paso 3**
 Usar valores relativos

Las variables width y height se actualizan automaticamente con el tamaño del lienzo.
Las posiciones y tamaños deben pensarse de forma proporcional.



**Paso 4**

 Factor de referencia

referencia = min(width,height)

Compara ancho y alto y se queda con el valor mas pequeño.

Sirve para mantener proporciones.



**Paso 5**

translate() + push() + pop()

Para proyectos complejos es mejor mover el origen del sistema en vez de hacer muchos calculos.

push() y pop() permiten aislar las transformaciones de cada elemento.

---

# Imagenes
 **Paso 1**
Subir imagen a p5

Recomendaciones:

- nombres cortos
- minusculas
- sin espacios
- crear carpeta ASSETS


**Paso 2**
 preload()

Se crea una variable global para guardar la imagen.

La imagen se carga con loadImage() dentro de preload().


**Paso 3**
 image()

La imagen se dibuja con image().

Permite controlar:
- posicion
- ancho
- alto

Tambien se puede usar de forma responsiva.

---

# loadPixels()


Carga los pixeles de una imagen o del lienzo en memoria.

Permite analizar y modificar la informacion pixel por pixel.

---

# Modificar pixeles

**get()**

Funcion = leer el color de un pixel.

Resultado = devuelve los canales:

Tambien permite copiar una imagen.


**set()**

Funcion = escribir un nuevo color en un pixel.

Resultado = modifica la informacion guardada en memoria.


**updatePixels()**

Funcion = aplicar todos los cambios realizados con set().

Sin updatePixels() los cambios no aparecen en pantalla.


