# sesión 04 
# INTRODUCCIÓN A p5.js

## ¿Qué es p5.js?
p5.js es una biblioteca de JavaScript para crear arte, animaciones y proyectos interactivos.

---

## Funciones principales

### setup()
Se ejecuta una sola vez al inicio.

```javascript
function setup() {
  createCanvas(500, 500);
}
```

### draw()
Se ejecuta continuamente para crear animaciones.

```javascript
function draw() {
  background(220);
}
```

---

## Crear Canvas

```javascript
createCanvas(500, 500);
```

Crea un lienzo de 500x500 píxeles.

---

## Color de fondo

```javascript
background(0);
```

Negro.

```javascript
background(255, 0, 0);
```

Rojo RGB.

---

## Figuras básicas

### Rectángulo

```javascript
rect(50, 50, 100, 100);
```

### Círculo

```javascript
circle(250, 250, 80);
```

### Línea

```javascript
line(0, 0, 500, 500);
```

### Triángulo

```javascript
triangle(200, 100, 100, 300, 300, 300);
```

---

## Colores y bordes

### Relleno

```javascript
fill(255, 0, 0);
```

### Borde

```javascript
stroke(0);
```

### Grosor del borde

```javascript
strokeWeight(5);
```

### Sin borde

```javascript
noStroke();
```

---

## Ejemplo completo

```javascript
function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  fill(255, 0, 0);
  circle(250, 250, 150);

  fill(0, 0, 255);
  rect(100, 100, 80, 80);

  strokeWeight(4);
  line(0, 0, mouseX, mouseY);
}
```

---

## Links útiles

- https://p5js.org/es/
- https://p5js.org/reference/

