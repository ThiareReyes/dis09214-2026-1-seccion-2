## Sesión 4 
# DATOS DINÁMICOS Y VARIABLES — p5.js

## Movimiento y Datos Dinámicos

- Permiten crear movimiento e interacción
- Los valores cambian constantemente
- Se usan variables dinámicas

### Ejemplo

```javascript
ellipse(mouseX, mouseY, 100, 100);
```

# Variables Integradas en p5.js

## Mouse

### `mouseX`

- Posición horizontal del mouse
- Va desde `0` hasta `width`

```javascript
ellipse(mouseX, 200, 50, 50);
```

### `mouseY`

- Posición vertical del mouse
- Va desde `0` hasta `height`

```javascript
ellipse(200, mouseY, 50, 50);
```

### `pmouseX`

- Posición anterior del mouse
- Sirve para calcular movimiento o velocidad

### `mouseIsPressed`

- Detecta si el mouse está presionado
- Devuelve `true` o `false`

```javascript
if (mouseIsPressed) {
  background(0);
}
```

### `mouseButton`

- Detecta qué botón del mouse se presionó
- LEFT
- RIGHT
- CENTER

# Lienzo

## `width`

- Ancho del canvas

## `height`

- Alto del canvas

```javascript
ellipse(width/2, height/2, 100, 100);
```

# Ventana

## `windowWidth`

- Ancho de la ventana del navegador

## `windowHeight`

- Alto de la ventana del navegador

```javascript
createCanvas(windowWidth, windowHeight);
```

# Teclado

## `key`

- Última tecla presionada

```javascript
text(key, 100, 100);
```

## `keyCode`

- Código de teclas especiales

```javascript
if (keyCode === ENTER) {
  background(255);
}
```

## `keyIsPressed`

- Detecta si una tecla está presionada

# Tiempo

## `frameCount`

- Cantidad de frames desde el inicio

## `deltaTime`

- Tiempo entre frames

# Crear Tus Propias Variables

## Variables dinámicas

```javascript
let x;
```

## Variables constantes

```javascript
const tamaño = 100;
```

## Inicializar variables

```javascript
let x = 200;
```

## Usar variables

```javascript
ellipse(x, 100, 50, 50);
```

# JavaScript Objects

## Qué son

- Organizan varias variables en una sola estructura
- Funcionan como contenedores de información
- Usan pares de clave y valor

## Ejemplo

```javascript
let persona = {
  x: 100,
  y: 200,
  size: 50
};

ellipse(persona.x, persona.y, persona.size);
```

## Acceso a datos

```javascript
persona.x
persona.y
```

# `random()`

## Qué hace

- Genera números aleatorios

## `random()`

- Número entre `0` y `1`

```javascript
random();
```

## `random(maximo)`

- Número entre `0` y un máximo

```javascript
random(100);
```

## `random(minimo, maximo)`

- Número entre dos valores

```javascript
random(20, 50);
```

## Ejemplo

```javascript
let x = random(width);
let y = random(height);

ellipse(x, y, 50, 50);
```

# `map()`

## Qué hace

- Convierte un valor de un rango a otro

## Sintaxis

```javascript
map(valor, min_original, max_original, min_nuevo, max_nuevo);
```

## Ejemplo

```javascript
let tamaño = map(mouseX, 0, width, 10, 200);

ellipse(200, 200, tamaño);
```

## Explicación

- `mouseX` → valor original
- `0 y width` → rango original
- `10 y 200` → rango nuevo

# Width y Height

## Qué son

- Variables del tamaño del canvas

```javascript
createCanvas(800, 600);

ellipse(width/2, height/2, 100, 100);
```

# WindowWidth y WindowHeight

## Qué son

- Ajustan el canvas al tamaño de la ventana

```javascript
createCanvas(windowWidth, windowHeight);
```

# Ejemplo Completo

```javascript
let x;

function setup() {
  createCanvas(windowWidth, windowHeight);
  x = width/2;
}

function draw() {
  background(220);

  let tamaño = map(mouseX, 0, width, 20, 200);

  fill(random(255), random(255), random(255));

  ellipse(x, mouseY, tamaño);

  x = x + 1;

  if (x > width) {
    x = 0;
  }
}
```

ntana

