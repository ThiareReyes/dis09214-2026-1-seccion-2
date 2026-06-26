# sesión 05 - 10/04
# TRANSFORMACIONES Y CONDICIONALES — p5.js

# Transformaciones

## Qué son

- Permiten mover, rotar y transformar figuras
- Modifican el sistema de coordenadas
- Ayudan a crear animaciones y composiciones

# Ángulos y Radianes

## Qué son los radianes

- p5.js usa radianes por defecto
- Los ángulos se miden en relación al círculo

## `angleMode()`

### Radianes

```javascript
angleMode(RADIANS);
```

### Grados

```javascript
angleMode(DEGREES);
```

## Valores importantes

- `TWO_PI` → 360°
- `PI` → 180°
- `HALF_PI` → 90°
- `QUARTER_PI` → 45°

# `rotate()`

## Qué hace

- Rota elementos
- Siempre rota desde el punto de origen `(0,0)`
- Se recomienda usar con `translate()`

## Sintaxis

```javascript
rotate(valor);
```

## Ejemplo

```javascript
translate(200, 200);
rotate(45);

rect(0, 0, 100, 100);
```

# `translate()`

## Qué hace

- Mueve el punto de origen `(0,0)` a otra posición

## Sintaxis

```javascript
translate(x, y);
```

## Ejemplo

```javascript
translate(200, 200);

ellipse(0, 0, 100, 100);
```

# `push()` y `pop()`

## Qué hacen

- Guardan y restauran transformaciones
- Funcionan como memoria temporal
- Evitan que las transformaciones afecten a otras figuras

## Sintaxis

```javascript
push();
pop();
```

## Ejemplo

```javascript
push();

translate(200, 200);
rotate(45);

rect(0, 0, 100, 100);

pop();

ellipse(50, 50, 50, 50);
```

# `scale()`

## Qué hace

- Cambia el tamaño de las figuras
- Modifica la escala del sistema de coordenadas

## Sintaxis

```javascript
scale(x, y);
```

## Ejemplo

```javascript
scale(2, 2);

rect(50, 50, 100, 100);
```

# Condicionales

## Qué son

- Permiten tomar decisiones en el código
- Funcionan usando condiciones verdaderas o falsas

# Expresión Booleana

## Qué es

- Una expresión que solo puede dar:
  - `true`
  - `false`

## Ejemplo

```javascript
5 > 3
```

- Resultado → `true`

# Operadores de Comparación

## Igual `==`

```javascript
2 == 2
```

- Resultado → `true`

## Diferente `!=`

```javascript
2 != 3
```

- Resultado → `true`

## Mayor que `>`

```javascript
5 > 2
```

- Resultado → `true`

## Menor que `<`

```javascript
2 < 5
```

- Resultado → `true`

## Mayor o igual `>=`

```javascript
5 >= 5
```

- Resultado → `true`

## Menor o igual `<=`

```javascript
3 <= 5
```

- Resultado → `true`

# Operadores Lógicos

# AND `&&`

## Qué hace

- Devuelve `true` solo si ambas condiciones son verdaderas

## Ejemplo

```javascript
true && false
```

- Resultado → `false`

# OR `||`

## Qué hace

- Devuelve `true` si al menos una condición es verdadera

## Ejemplo

```javascript
true || false
```

- Resultado → `true`

# NOT `!`

## Qué hace

- Invierte el valor booleano

## Ejemplo

```javascript
!true
```

- Resultado → `false`

# `if`

## Qué hace

- Ejecuta código solo si la condición es verdadera

## Sintaxis

```javascript
if (condicion) {

}
```

## Ejemplo

```javascript
if (mouseX > 200) {
  background(255, 0, 0);
}
```

# `if - else`

## Qué hace

- Ejecuta un código si la condición es verdadera
- Ejecuta otro código si es falsa

## Sintaxis

```javascript
if (condicion) {

} else {

}
```

## Ejemplo

```javascript
if (mouseIsPressed) {
  background(0);
} else {
  background(255);
}
```

# `if - else if - else`

## Qué hace

- Permite usar varias condiciones

## Sintaxis

```javascript
if (condicion1) {

} else if (condicion2) {

} else {

}
```

## Ejemplo

```javascript
if (mouseX < 200) {
  background(255, 0, 0);

} else if (mouseX < 400) {
  background(0, 255, 0);

} else {
  background(0, 0, 255);
}
```

# Ejemplo Completo

```javascript
let angle = 0;

function setup() {
  createCanvas(800, 600);
  angleMode(DEGREES);
  rectMode(CENTER);
}

function draw() {
  background(220);

  push();

  translate(width/2, height/2);

  rotate(angle);

  scale(1.5);

  if (mouseIsPressed) {
    fill(255, 0, 0);

  } else if (mouseX > width/2) {
    fill(0, 255, 0);

  } else {
    fill(0, 0, 255);
  }

  rect(0, 0, 100, 100);

  pop();

  angle += 1;
}
```


