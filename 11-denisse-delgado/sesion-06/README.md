# Sesión 06 - 24/04
# Github aclaraciones:
- Poner .md en el nombre
- Para poner el código hay que poner entre comillas
<img width="939" height="470" alt="2026-05-21 (6)" src="https://github.com/user-attachments/assets/bf4ac506-d88c-40ef-bb40-9ca58d93ab91" />

---

## 4 Partes fundamentales del pensamiento computacional
- 4 pilares: DESCOMPOSICIÓN, RECONOCIMIENTO DE PATRONES, ABSTRACCIÓN y ALGORITMOS

1.  Descomposición
- “Dividir para conquistar”
- Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y manejables.
    * En diseño: Si quieres visualizar la "Brecha Salarial", no programas todo de una vez.
Primero diseñas cómo se ve el "Sueldo A", luego el "Sueldo B", luego la "Interacción" y
finalmente el "Fondo".
    * En el código: Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante,
tienes una función dibujarIconos() y otra calcularDiferencia(), etc.

2. Reconocimiento de patrones
- “Encontrar similitudes”
- Es observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una lógica constante, podemos automatizarlo.
    * En diseño: Notas que para representar a 100 personas, no necesitas dibujar 100 veces.
Notas que todas son un círculo con una posición x distinta.
    * En el código: Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por ti con solo tres líneas.

3. Abstracción
- “Lo importante vs el detalle”
- Es filtrar la información innecesaria y quedarse solo con las características que definen el
problema. Es crear una representación simbólica de la realidad.
    * En diseño: Para representar la "presión social" no necesitas dibujar a toda la sociedad;
quizás un círculo que se achica cuando el mouse se acerca es suficiente.
    * En el código: Se traduce en el uso de Variables y la función map(). Una posición de
mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.

4. Algoritmos
- “La receta paso a paso”, el plan de acción
- Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el "plan de
acción" que debe seguir el sistema.
    * En diseño: Es el flujo de la experiencia. "Si el usuario hace esto, pasa aquello; si no,
pasa esto otro”.
    * En el código: Se traduce en el Diagrama de Flujo y en las Condicionales (if/else). Es el
mapa lógico que conecta todas las partes anteriores.

---

### Tipos de interacción 
1. Interacción discreta(eventos): Clic 
- Es cuando curre un evento específico (clic) y el sistema responde con una acción única (aparecen círculos). Es un interruptor de "encendido/apagado" o "acción/reacción".
    * En el código: Se suele usar dentro de la función mousePressed() o con un if(mouseIsPressed).

2. Interacción continua(Input de Datos)
- Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad de hacer algo específico (clic).
    * En el código: Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad de algo.

---

#### Funciones propias
- Permite darle modularidad al código y reusabilidad
- Ejemplos profe: 
(https://editor.p5js.org/PoliMujica/sketches/4RDCn4eXJ)

(https://editor.p5js.org/PoliMujica/sketches/vC47zgguc)

(https://editor.p5js.org/PoliMujica/sketches/vAQgFOKSy)

(https://editor.p5js.org/PoliMujica/sketches/oQCGBN6wX)

(https://editor.p5js.org/PoliMujica/sketches/MbBrMlrus)

- Sintaxis: Abajo del draw: function Nombredelafunción(){   }
- Ejemplo: 
function (){
Aquí al medio tiene que ir lo que queremos que haga
}

<img width="576" height="465" alt="2026-05-21 (7)" src="https://github.com/user-attachments/assets/1a21da7c-3932-4814-a533-a64246dcb4b8" />

- print: Sirve para saber si lo que hicimos está bien, se pone print(“algo”)
- funciones se ponen después del cierre del draw
