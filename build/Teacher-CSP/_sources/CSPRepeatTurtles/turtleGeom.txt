..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |bigteachernote| image:: Figures/apple.jpg
    :width: 50px
    :align: top
    :alt: teacher note
    
.. 	qnum::
	:start: 1
	:prefix: csp-10-2-

|bigteachernote| Nota para el profesor: Geometría de tortuga
============================================================
La tortuga resulta ser una herramienta muy útil para explorar una amplia variedad de los conceptos de la geometría. El libro `Geometría de Tortuga <http://www.amazon.es/Geometría-tortuga-ordenador-exploración-matemáticas/dp/B00IMJXBQQ/ref=sr_1_1?s=books&ie=UTF8&qid=1458544264&sr=1-1&keywords=tortuga+abelson>`_ expone con muy acertadamente cómo pueden utilizarse las tortugas para tratar muchos de los conceptos sobre geometría, matemáticas y ciencia (por ejemplo, utilizar tortugas para modelar el comportamiento de un insecto).  El ejemplo de **patrón** que se expone a continuación se ha extraído de dicho libro. 

.. figure:: Figures/turtle-geometry.jpg
    :width: 200px
    :align: center
    :alt: a scan of the cover of the book about turtle geometry
    :figclass: align-center

    Figura 1: La portada de la versión en inglés


El teorema del viaje completo
=============================

El último fragmento de código es realmente un **patrón**
que sirve para una gran variedad de formas geométricas. Veamos el caso de un triángulo. Puede que no sea algo obvio saber por qué en este programa hacemos giros de ciento veinte grados (120), pero lo será pronto.

.. activecode:: Turtle_Triangle
    :tour_1: "Lines of code"; 1: tR3-line1; 2: tR3-line2; 3: tR3-line3; 4: tR3-line4; 5: tR3-line5; 6: tR3-line6; 7: tR3-line7;
    :nocodelens:
  
    from turtle import *   	# usar la librería turtle
    espacio = Screen()    	# crear el espacio de la tortuga
    juan = Turtle()   		# crear la tortuga Juan
    juan.setheading(90)   	# apuntar al norte
    for lados in range(3):	# repetir tres veces
      	juan.forward(100)    	# avanzar 100
      	juan.right(120)         	# girar 120 grados

Veamos ahora el pentágono.

.. activecode:: Turtle_Pentagon
    :tour_1: "Lines of code"; 1: tR3-line1; 2: tR3-line2; 3: tR4-line3; 4: tR4-line4; 5: tR4-line5; 6: tR4-line6; 7: tR4-line7;
    :nocodelens:
	
    from turtle import *   	
    espacio = Screen()    	
    guille = Turtle()   		
    guille.setheading(90)    	
    for lados in range(5):	
      	guille.forward(100)      	# avanza 100
      	guille.right(72)          	# gira 72 grados

El **Teorema del viaje completo de la tortuga** establece que la tortuga dibujará una figura cerrada de *n* lados cuando la suma de sus ángulos sea múltiplo de 360. En el ejemplo del triángulo ``3 * 120 = 360``, y en el del pentágono ``5 * 72 = 360``. 

En el programa siguiente, cambia los signos ``??`` de la línea 7 por el número de grados que debe girar cada vez para dibujar un polígono de doce lados, también llamado dodecágono. Si lo haces correctamente, la tortuga dibujará un polígono cerrado de doce lados.

.. activecode:: Turtle_Dodecagon
    :tour_1: "Lines of code"; 1: tR3-line1; 2: tR3-line2; 3: tR5-line3; 4: tR5-line4; 5: tR5-line5; 6: tR5-line6; 7: tR5-line7;
    :nocodelens:
	
    from turtle import * 	
    espacio = Screen()   		
    maria = Turtle()   		
    maria.setheading(90)     	
    for lados in range(12):	
      	maria.forward(40)       	
      	maria.right(??)      # cambia ?? por los grados a girar

.. mchoicemf:: 10_2_1_Turtle_Dodecagon_Q1
   :answer_a: 15
   :answer_b: 30
   :answer_c: 12
   :answer_d: 90
   :correct: b
   :feedback_a: No se cerrará la figura
   :feedback_b: ¡Perfecto! 12 * 30 = 360
   :feedback_c: No, 12 * 12 es 144, que no es múltiplo de 360
   :feedback_d: Esto generará un cuadrado, tres veces. 12 * 90 = 1080 = 360 * 3

   ¿Cuánto necesita girar ``maria`` en este programa para crear un dodecágono cerrado (doce lados)? Solo una de las soluciones es válida.
   
.. parsonsprob:: 10_2_2_Triangle

   El siguiente programa utiliza una tortuga para dibujar un triángulo como el que está representado a la izquierda, <img src="../_static/TurtleTriangle.png" width="150" align="left" hspace="10" vspace="5"/> pero las líneas están desordenadas. El programa debería contener todas las instrucciones para crear una tortuga. Después, iterará tres veces en un bucle, y en cda una de esas veces deberá avanzar cien pixels, y girar a la izquierda ciento veinte grados. Después, la pantalla deberá cerrarse cuando el usuario haga clc sobre ella.<br /><br /><p>Arrastra los bloques con las instrucciones que están a la izquierda, y colócalos en la parte derecha en el orden correcto, y con la indentación apropiada. Haz clic en <i>Check Me</i> para comprobar el resultdo. El ejercició te indicará si alguna de las líneas no está en el orden correcto, o si no está bien indentada</p> 
   -----
   from turtle import * 
   =====         
   espacio = Screen()
   maria = Turtle()
   =====
   # repite 3 veces
   for i in range(3): 
   =====   
       maria.forward(100)
   =====
       maria.left(120)



