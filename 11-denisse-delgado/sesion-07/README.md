# Sesión 07 - 15/05
# Github
- Código del curso
dis09214-2026-1-seccion-2

- fork
- Editar en el readme las clases
- ´´´javascript para subir el código
- commit y pol recuest

## LOOPS WHILE & FOR 
- Loops son infinitos
- Definición rae bucle: 
1. Rizo de cabello en forma helicoidal.
2. Objeto cuya forma recuerda la del bucle.
3. Proceso que se repite indefinidamente.
4. Informática. Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.

- Loop: Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.

- While(Mientras): Parecido al if: Los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repiten.

    * While(condición booleana){ejecuta este código si es true}

    * Ejemplos míos while: (https://editor.p5js.org/denisse.delgado2/sketches/9mVeo4N-K)
while cuadrícula: (https://editor.p5js.org/denisse.delgado2/sketches/ODwQv0wSu)
círculo gradiente: (https://editor.p5js.org/denisse.delgado2/sketches/rU9SoLlFW)

<img width="823" height="428" alt="2026-05-21 (8)" src="https://github.com/user-attachments/assets/4cee18ea-f95c-4285-b197-1d928fda7c97" />

- For: Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles `for` son útiles para repetir instrucciones un número determinado de veces. Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:

<img width="930" height="413" alt="2026-05-21 (9)" src="https://github.com/user-attachments/assets/a5ad3b34-ded2-418d-8089-67500ec725e5" />

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

    * for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}
    * for (let x=0 ; x <= width; x=x+1) { ellipse (x , 200, random(300))}
    * Ejemplos profe: (https://editor.p5js.org/PoliMujica/sketches/sY2ZhJjXP)
    * Ejemplos mío:
for movimiento: (https://editor.p5js.org/denisse.delgado2/sketches/RPfJf2ORJ)
Al poner el framRate en el setup hace que vayan más lento

### NESTED LOOPS: Un loop dentro de otro loop

<img width="1129" height="588" alt="2026-05-21 (10)" src="https://github.com/user-attachments/assets/0bc3600a-26a9-4e63-ad3f-f34c9b8cc289" />
<img width="674" height="450" alt="2026-05-21 (11)" src="https://github.com/user-attachments/assets/99f8ebf7-2229-4453-89b2-d0af8328c0d7" />

- Va ha hacer primero el for que está adentro(el de abajo)
- Un for dentro de otro for: 
    * for (inicialización variable; condición booleana; actualización){ Lo que queremos que pase cuando la condición sea verdadera
for (inicialización variable; condición booleana; actualización){
}
Lo que queremos que pase cuando la condición sea verdadera
}

    * Ejemplos mío nested loop: (https://editor.p5js.org/denisse.delgado2/sketches/YmzQN2GHO)
nested loop con mouse x y: (https://editor.p5js.org/denisse.delgado2/sketches/YmzQN2GHO)
HSB: (https://editor.p5js.org/denisse.delgado2/sketches/GCxLBmbWo)
sin loop cuadrados: (https://editor.p5js.org/denisse.delgado2/sketches/IURASpE1u)

- HSB: Saturación y brillo
-noLoop: Sin loop
- Se permite usar la ia pero nos va a interrogar en la solemne 2

- frameCount: Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de `frameCount` es 0 dentro de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.
