# sesión 06 
# TRANSFORMACIONES Y CONDICIONALES EN p5.js

## Ángulos

Por defecto p5.js usa radianes.

```javascript
angleMode(DEGREES);
```

Cambia el sistema a grados.

---

## rotate()

Rota figuras.

```javascript
rotate(45);
```

### Ejemplo

```javascript
function setup() {
  createCanvas(500, 500);
  angleMode(DEGREES);
}

function draw() {
  background(220);

  translate(250, 250);

  rotate(frameCount);

  rectMode(CENTER);

  rect(0, 0, 100, 100);
}
```

---

## translate()

Mueve el punto de origen.

```javascript
translate(200, 200);
```

---

## push() y pop()

Guardan y restauran transformaciones.

```javascript
push();

translate(250, 250);
rotate(45);

rect(0, 0, 100, 100);

pop();
```

---

## scale()

Cambia el tamaño de las figuras.

```javascript
scale(2);
```

### Ejemplo

```javascript
function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  translate(250, 250);

  scale(1.5);

  circle(0, 0, 100);
}
```

---

# CONDICIONALES

## if

Ejecuta código si una condición es verdadera.

```javascript
if (mouseX > 250) {
  background(255, 0, 0);
}
```

---

## if - else

```javascript
if (mouseX > 250) {
  background(0, 255, 0);
} else {
  background(0);
}
```

---

## if - else if - else

```javascript
if (mouseX < 200) {
  background(255, 0, 0);

} else if (mouseX < 400) {
  background(0, 255, 0);

} else {
  background(0, 0, 255);
}
```

---

# Operadores de comparación

```javascript
==  igual
!=  diferente
>   mayor que
<   menor que
>=  mayor o igual
<=  menor o igual
```

---

# Operadores lógicos

```javascript
&&  AND
||  OR
!   NOT
```

---

# Ejemplo completo

```javascript
function setup() {
  createCanvas(500, 500);
  angleMode(DEGREES);
}

function draw() {
  background(30);

  push();

  translate(width / 2, height / 2);

  rotate(frameCount);

  scale(1.2);

  rectMode(CENTER);

  if (mouseX < width / 2) {

    fill(255, 0, 0);

  } else if (mouseY < height / 2) {

    fill(0, 255, 0);

  } else {

    fill(0, 0, 255);
  }

  rect(0, 0, 150, 150);

  pop();

  textSize(20);
  fill(255);
  text("Transformaciones en p5.js", 120, 40);
}
```

---

# Conceptos aprendidos

- rotate()
- translate()
- push() y pop()
- scale()
- if / else
- operadores lógicos
- transformaciones
- condicionales

---

# Links útiles

- https://p5js.org/es/
- https://p5js.org/reference/

