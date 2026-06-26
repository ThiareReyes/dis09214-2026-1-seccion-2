# sesión 05 
# DATOS DINÁMICOS Y VARIABLES EN p5.js

## Variables integradas

### Posición del mouse

```javascript
ellipse(mouseX, mouseY, 50, 50);
```

- `mouseX` → posición horizontal
- `mouseY` → posición vertical

---

## Variables del canvas

```javascript
width
height
```

Representan el tamaño del lienzo.

---

## Crear variables propias

```javascript
let x = 100;
let velocidad = 2;
```

`let` sirve para crear variables dinámicas.

---

## Movimiento básico

```javascript
let x = 0;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  circle(x, 250, 50);

  x = x + 2;
}
```

---

## random()

Genera números aleatorios.

```javascript
random(100);
```

Número entre 0 y 100.

### Ejemplo

```javascript
let tamaño;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(0);

  tamaño = random(20, 100);

  circle(mouseX, mouseY, tamaño);
}
```

---

## map()

Transforma valores de un rango a otro.

```javascript
map(valor, min1, max1, min2, max2);
```

### Ejemplo

```javascript
let tamaño;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  tamaño = map(mouseX, 0, width, 20, 200);

  circle(250, 250, tamaño);
}
```

---

## windowWidth y windowHeight

Permiten que el canvas se adapte a la pantalla.

```javascript
createCanvas(windowWidth, windowHeight);
```

---

## Ejemplo completo

```javascript
let x = 0;
let tamaño;

function setup() {
  createCanvas(windowWidth, windowHeight);
}

function draw() {
  background(30);

  tamaño = map(mouseX, 0, width, 50, 200);

  fill(random(255), random(255), random(255));

  circle(x, height / 2, tamaño);

  x = x + 3;

  if (x > width) {
    x = 0;
  }
}
```

---

## Conceptos aprendidos

- Variables
- Movimiento
- mouseX y mouseY
- random()
- map()
- width y height
- windowWidth y windowHeight

---

## Links útiles

- https://p5js.org/es/
- https://p5js.org/reference/



# *Sesion 6*

# FUNCIONES PROPIAS EN p5.js

## ¿Qué es una función?

Una función es un bloque de código que realiza una tarea específica.

```javascript
function miFuncion() {

}
```

---

# Pensamiento Computacional

## 4 pilares

1. Descomposición  
2. Reconocimiento de patrones  
3. Abstracción  
4. Algoritmos  

---

## Descomposición

Dividir un problema grande en partes pequeñas.

### Ejemplo

```javascript
function dibujarFondo() {

}

function dibujarPersonaje() {

}
```

---

## Reconocimiento de patrones

Identificar cosas que se repiten.

### Ejemplo con for

```javascript
for (let i = 0; i < 10; i++) {

  circle(i * 50, 250, 30);

}
```

---

## Abstracción

Usar solo la información importante.

### Ejemplo

```javascript
let tamaño;

tamaño = map(mouseX, 0, width, 20, 200);
```

---

## Algoritmos

Pasos ordenados para resolver un problema.

### Ejemplo

```javascript
if (mouseIsPressed) {

  background(255, 0, 0);

} else {

  background(0);

}
```

---

# Tipos de interacción

## Interacción discreta

Sucede con eventos.

```javascript
function mousePressed() {

  circle(mouseX, mouseY, 50);

}
```

---

## Interacción continua

Reacciona constantemente al usuario.

```javascript
circle(mouseX, mouseY, 80);
```

---

# Funciones propias

## Sintaxis

```javascript
function nombreFuncion() {

}
```

---

## Ejemplo simple

```javascript
function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  dibujarCara();
}

function dibujarCara() {

  fill(255);

  circle(250, 250, 200);

  fill(0);

  circle(220, 220, 20);

  circle(280, 220, 20);

}
```

---

# Modularidad

Separar el código en partes ordenadas.

```javascript
function dibujarFondo() {

}

function dibujarTexto() {

}

function dibujarObjeto() {

}
```

---

# Reusabilidad

Una función puede usarse muchas veces.

```javascript
function estrella(x, y) {

  circle(x, y, 20);

}

estrella(100, 100);

estrella(200, 200);

estrella(300, 300);
```

---

# Ejemplo completo

```javascript
function setup() {
  createCanvas(600, 400);
}

function draw() {

  background(30);

  dibujarTitulo();

  dibujarFigura(mouseX, mouseY);

}

function dibujarTitulo() {

  fill(255);

  textSize(24);

  text("Funciones Propias", 180, 40);

}

function dibujarFigura(x, y) {

  fill(0, 200, 255);

  circle(x, y, 80);

}
```

---

# Conceptos aprendidos

- Funciones propias
- Modularidad
- Reusabilidad
- Interacción discreta
- Interacción continua
- Pensamiento computacional
- for
- if / else

---

# Links útiles

- https://p5js.org/es/
- https://p5js.org/reference/
