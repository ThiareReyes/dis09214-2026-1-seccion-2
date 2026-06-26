# Solemne 02

SOLEMNE2 
-

PROBLEMÁTICA DE GÉNERO LLEVADA AL CÓDIGO 
-

*Julio Andree, Javiera Corral*
-
Para la solemne 2 de pensamiento computacional nos enfrentamos al desafío de seleccionar una problemática de género y transformar su significado y presencia a un sketch interactivo en la plataforma de P5.js. 
Nosotros como dupla decidimos trabajar con la problemática de  encasillar/ etiquetar a las personas según su apariencia. 

Encasillar / etiquetar personas según apariencias 
-
*Etiqueta (RAE): Calificación estereotipada y simplificadora.*

*Encasillar(RAE): Clasificar personas o hechos con criterios poco flexibles o simplistas.*

El problema con encasillar personas según su apariencia es la consecuencia de quitar o eliminar la diversidad y complejidad que posee el humano, remplazandola por etiquetas simples que promueven el pensamiento estereotipado de quienes nos perciben y de nosotros mismos.  Esto puede llevar a una crisis de identidad personal ya que al no sentirse de acuerdo con la etiqueta que otras personas te otorgan tendemos a sentir una desconexión con nuestro entorno y nosotros mismos.

las etiquetas en si no suelen ser del todo maliciosas pero al ser tan cerradas en su significado (gay, lesbiana, mujer, hombre, trans, etc.) resultan restrictivas y deshumanizantes. 

ejemplos:
-
pensar que una persona es mujer o usa pronombres femeninos solo por vestirse con vestidos y tener pelo largo o pensar que es hombre solo por vestir con pantalones y llevar el pelo estilizado de manera “masculina".


<img width="273" height="272" alt="image" src="https://github.com/user-attachments/assets/6e405375-c861-4599-bd17-23b1362c5d50" />
<img width="424" height="281" alt="image" src="https://github.com/user-attachments/assets/b949ec00-25cf-4921-9924-c7474dcb8ae0" />


"La diversidad nos aporta riqueza en todos los sectores y ámbitos de nuestra vida. Sin embargo, en numerosas ocasiones, por simplificar tendemos a “etiquetar” a las personas dentro de una determinada categoría que los define de una manera concreta, a etiquetarlos con unas características inamovibles y concretas. Al actuar de esta manera, muchas veces inconsciente, no tenemos en cuenta que estamos limitando nuestra percepción de los demás, perdiéndonos toda la complejidad de las personas, sus matices y en definitiva, toda esa riqueza que aporta la diversidad."
*Fragmento extraído de:[divem.accem.es]( https://divem.accem.es/problema-encasillar-personas/)*

IDEA DEL SKETCH
-

*• Descripción objetiva*
-
¿Qué es el proyecto? 

Nuestro proyecto es un código creado en la plataforma de p5.js que tiene como función etiquetar individuos en diferentes identidades sexuales predeterminadas que pueden o no ser acertadas a la realidad.

¿Qué se ve en pantalla? 

la pantalla del sketch muestra la cámara del computador que detecta la cara del individuo frente a ella y le designa una bandera de la comunidad LGBTQ+. al aparecer la opción de la bandera trans la imagen será seguida por confeti que cae de manera oscilante sobre el lienzo mientras el texto "¡¡¡¡¡¡¡¡ES TRANS!!!!!!!!" aparece en la parte superior de la pantalla.

¿Qué elementos visuales aparecen? 

la cámara donde se aprecia la cara del usuario, la bandera LGBTQ+ que se posiciona sobre su frente, el texto que determina la identidad en un solo caso resultante (el de la bandera trans) y el confetti que celebra el resultado (el confetti solo aparece en el caso de que se muestra la bandera trans).

*• Descripción conceptual*
-
Idea central del proyecto y su relación con el sistema diseñado?

Para nuestro sketch nos centraremos en explorar la idea de determinación de identidad sexual tomando las características de diferentes etiquetas e implementarlas en una especie de selección aleatoria. el usuario deberá interactuar para ser encasillado en alguna categoría la cual puede o no ser acertada. la respuesta que dé el usuario al sketch demostrará nuestro pensar sobre la problemática tratada. 

Buscamos con el sketch hacer que el usuario se sienta minimizado a una sola identidad por culpa de un sistema invisible que no pueden controlar. Para esto pensamos implementar en nuestro sketch la cámara para detectar la cara del usuario y utilizando imágenes de las banderas de la comunidad LGBTQ+ seguidas por textos que reafirman la etiqueta seleccionada aleatoriamente por el programa el usuario tendrá el resultado pegado a su frente sin poder deshacerse de él dejando al usuario satisfecho o no con su resultado eso no importa ya que el código no está hecho para tener las emociones humanas en cuenta y el usuario llevará el peso internalizado de la etiqueta que se le asignó.

Para crear ese resultado decidimos crear un sketch algo cómico que demuestre diferentes banderas LGBTQ+ que representan las etiquetas que la sociedad le determina  de manera superficial o algo discriminatoria a cualquier ser humano sin importar su compleja personalidad e identidad, más allá de lo que se ve a simple vista. 

Para crear una sensación de aminorar el sentir o "pasa allevar" que un individuo encasillado puede experimentar se implementa en el código partículas de confeti que acompañan al resultado y le agregan un pequeño morbo a la deshumanización de etiquetar al usuario.

*• Referentes*
-
nuestra mayor inspiración fueron los filtros de tiktok que determinaban qué bandera LGBTQ+ era la persona en pantalla. la mayoría de veces representaban al usuario de manera errónea y en los videos se nos demostraba la emoción que el usuario posee al inicio cambiar. el usuario puede animarse, decaer o hasta indignarse por el resultado adquirido.

<img width="247" height="443" alt="image" src="https://github.com/user-attachments/assets/d2c9a284-76a1-478e-a476-f5c84ba3b766" />

<img width="253" height="449" alt="image" src="https://github.com/user-attachments/assets/34c2bb97-86c1-4cda-a387-33df6af95908" />



FaceMesh de la biblioteca ml5js : utilizamos este referente para lograr mapear la cara del sujeto.
[biblioteca ml5js](https://docs.ml5js.org/#/reference/facemesh?id=methods) 

<img width="355" height="311" alt="image" src="https://github.com/user-attachments/assets/49dfaff0-da30-412f-a70b-9e6654561eb1" />


[Código que se utilizó de base para el confeti](https://editor.p5js.org/aceschen/sketches/A1Yn7XDc8)

(código y más contenido transferido desde SOLEMNE2 folder)

