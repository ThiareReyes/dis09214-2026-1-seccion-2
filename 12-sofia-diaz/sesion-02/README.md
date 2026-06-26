# sesión 02 - 27/03
Introducción a p5.js y Pensamiento Computacional  
 **Pensamiento Computacional y Algoritmos:**  
   El pensamiento computacional se basa en la creación de algoritmos.  
   Definición de Algoritmo: Secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas para resolver un problema.  
 
 ***Características:***  
 Precisión: Pasos claros y sin ambigüedades.  
Orden: Secuencia lógica.  
Finitud: Siempre debe tener un fin.  
Definición: Ante los mismos datos de entrada, siempre se obtiene el mismo resultado.  
Estructura básica: Entrada (Input) → Proceso (Algoritmo) → Salida (Output)  

 ***Diagramas de Flujo:***
Representación gráfica de un algoritmo para planificar la lógica antes de programar.  
Simbología básica:Óvalo (Terminal): Inicio o fin del proceso.  
Rectángulo (Proceso): Acción o instrucción.  
Rombo (Decisión): Pregunta que bifurca el camino (Sí/No).  

  **Introducción a p5.js**

   ¿Qué es?:  
   Es una librería de JavaScript. No es un lenguaje nuevo, sino un "vocabulario" especializado para la creación visual y
   animación.  
   
Funciones Principales:  
(Maestras)    
setup(): Se ejecuta una sola vez al inicio. Se usa para configurar el lienzo (createCanvas) y el entorno inicial.  
draw(): Se ejecuta en un bucle infinito (60 fps aprox.). Ideal para animaciones e interacción en tiempo real.   

Configuración del Lienzo y Color Lienzo:   createCanvas(ancho, alto); define el tamaño en píxeles. El punto (0,0) se ubica en la esquina superior izquierda.  
Fondo: background(color);.Grises: background(0) (negro) a background(255) (blanco)  
RGB: background(R, G, B); (valores de 0 a 255).Alpha: Un cuarto valor opcional para transparencia (0-255).    
Modos de Color: Se puede cambiar entre RGB, HSB (Tono, Saturación, Brillo) o HSL.     

Figuras Geométricas 2D:  
point(x, y); : Un píxel.   
line(x1, y1, x2, y2); : Línea entre dos puntos.  
rect(x, y, ancho, alto); : Rectángulo (esquina superior izquierda por defecto)  
ellipse(x, y, ancho, alto); : Óvalo o círculo (desde el centro)  
triangle(x1, y1, x2, y2, x3, y3); : Tres coordenadas para las esquinas.arc(x, y, w, h, inicio, fin); :   
Arcos o medios círculos. Requiere angleMode(DEGREES) para usar grados.    

Estilo (Bordes y Relleno)  
strokeWeight(peso); : Grosor del borde en píxeles.  
stroke(r, g, b); : Color del borde.  
noStroke(); : Elimina el borde.  
fill(r, g, b); : Color de relleno.
