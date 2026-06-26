# sesión 07 - 15/05
# LOOPS — WHILE & FOR — p5.js

# ¿Qué es un Loop?

## Qué es

- Un loop es un bucle
- Repite instrucciones automáticamente
- Funciona mientras se cumpla una condición

## Definición

- Serie de instrucciones que se repiten
- Puede repetirse muchas veces
- Puede detenerse cuando una condición cambia

# Loops en Programación

## Qué hacen

- Automatizan tareas repetitivas
- Evitan escribir el mismo código muchas veces
- Sirven para crear patrones y animaciones

# `while`

## Qué es

- Repite código mientras una condición sea verdadera
- Funciona parecido a un `if`, pero en bucle

## Sintaxis

```javascript
while (condicion) {

}
```

## Ejemplo básico

```javascript
let x = 0;

while (x < 10) {
  console.log(x);

  x = x + 1;
}
```

## Explicación

- `x < 10` → condición
- Mientras sea `true`, el loop continúa
- `x = x + 1` evita un loop infinito

# Ejemplo en p5.js

```javascript
let x = 0;

while (x <= height) {

  ellipse(200, x, 20);

  x = x + 20;
}
```

# Loops Infinitos

## Qué son

- Loops que nunca terminan
- Ocurren cuando la condición nunca cambia

## Ejemplo incorrecto

```javascript
let x = 0;

while (x < 10) {

  ellipse(200, x, 20);

}
```

## Problema

- `x` nunca cambia
- La condición siempre es `true`

# `for`

## Qué es

- Loop que repite código una cantidad determinada de veces
- Es más corto y ordenado que `while`

## Sintaxis

```javascript
for (inicializacion; condicion; actualizacion) {

}
```

# 4 Elementos del `for`

## 1. Inicialización

```javascript
let x = 0
```

- Crea la variable

## 2. Condición

```javascript
x <= width
```

- Define cuándo continúa el loop

## 3. Actualización

```javascript
x = x + 1
```

- Cambia la variable en cada repetición

## 4. Acción

```javascript
ellipse(x, 200, 20);
```

- Lo que ocurre dentro del loop

# Ejemplo Básico

```javascript
for (let x = 0; x <= width; x = x + 20) {

  ellipse(x, 200, 20);

}
```

# Explicación

- Empieza en `0`
- Continúa mientras `x` sea menor o igual a `width`
- Incrementa `20` cada vez

# `random()` dentro de Loops

## Ejemplo

```javascript
for (let x = 0; x <= width; x = x + 20) {

  ellipse(x, 200, random(50));

}
```

## Qué hace

- Crea círculos con tamaños aleatorios

# Nested Loops

# Qué son

- Un loop dentro de otro loop
- También llamados loops anidados

# Sintaxis

```javascript
for () {

  for () {

  }

}
```

# Ejemplo

```javascript
for (let x = 0; x <= width; x = x + 25) {

  for (let y = 0; y <= height; y = y + 25) {

    ellipse(x, y, 15);

  }

}
```

# Qué hace

- Crea una grilla de figuras
- El loop exterior controla `x`
- El loop interior controla `y`

# `frameCount`

## Qué es

- Variable automática de p5.js
- Cuenta los frames desde el inicio

## Qué hace

- Aumenta en `1` cada frame
- Sirve para animaciones y tiempo

## Ejemplo

```javascript
function draw() {

  background(220);

  ellipse(frameCount, 200, 50);

}
```

# Explicación

- La figura se mueve porque `frameCount` aumenta constantemente

# Ejemplo Completo

```javascript
function setup() {
  createCanvas(800, 600);
}

function draw() {

  background(0);

  for (let x = 0; x <= width; x = x + 40) {

    for (let y = 0; y <= height; y = y + 40) {

      fill(random(255), random(255), random(255));

      ellipse(x, y, random(20));

    }

  }

}
```

