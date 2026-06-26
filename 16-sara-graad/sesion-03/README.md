# sesión 03 - 27/03
## Lo Básico: Pensamiento Computacional
Un **algoritmo** es una lista de pasos ordenados y lógicos para resolver un problema.
* **Input:** Los datos que entran.
* **Proceso:** La lógica o fórmulas que transforman los datos.
* **Output:** El resultado visual en pantalla.

*Usamos **Diagramas de Flujo** para dibujar y planificar esta lógica antes de tirar líneas de código.*

---

##  2. ¿Qué es p5.js?
Es una biblioteca de JavaScript para **programación creativa**. Tiene dos funciones principales que controlan todo:
1.  `setup()`: Se ejecuta **una sola vez** al inicio. Configura el lienzo (`createCanvas`).
2.  `draw()`: Bucle infinito (**60 veces por segundo**). Sirve para animar e interactuar.

---

##  3. El Lienzo y el Color
* **Coordenadas:** El punto `(0,0)` es la **esquina superior izquierda**. 
    * `X` avanza a la derecha.
    * `Y` avanza hacia abajo.
* **Color (RGB):** Valores de 0 a 255.
    * `background(255, 0, 0);` -> Rojo puro.
    * Un cuarto número dentro del paréntesis controla el **Alpha** (transparencia).

---

##  4. Formas Básicas y Estilos
* `line(x1, y1, x2, y2);` -> Línea entre dos puntos.
* `rect(x, y, ancho, alto);` -> Rectángulo desde su esquina superior izquierda.
* `ellipse(x, y, ancho, alto);` -> Círculo o elipse desde su centro.
* `triangle(x1, y1, x2, y2, x3, y3);` -> Tres esquinas de un triángulo.
* `fill()` / `noFill()` -> Color de relleno / Sin relleno.
* `stroke()` / `noStroke()` -> Color de borde / Sin borde.
* `strokeWeight(px)` -> Grosor de la línea en píxeles.

---


###  ¿Qué tiene que llevar este GitHub para el 7?
1.  **Info:** Nombre del proyecto y del equipo.
2.  **Bitácora:** Texto corto explicando cómo replicamos el dibujo y qué nos costó programar.
3.  **Código:** El código de p5.js pegado aquí abajo y **bien comentado** (explicando qué hace cada parte).
4.  **Evidencia:** Links al editor de p5.js y fotos del dibujo original en papel.

📅 **Fecha de Entrega:** Viernes 10 de Abril.
