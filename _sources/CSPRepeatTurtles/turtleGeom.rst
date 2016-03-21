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

|bigteachernote| Nota para el profesor: Geometr�a de tortuga
============================================================
La tortuga resulta ser una herramienta muy �til para explorar una amplia variedad de los conceptos de la geometr�a. El libro `Geometr�a de Tortuga <http://www.amazon.es/Geometr�a-tortuga-ordenador-exploraci�n-matem�ticas/dp/B00IMJXBQQ/ref=sr_1_1?s=books&ie=UTF8&qid=1458544264&sr=1-1&keywords=tortuga+abelson>`_ expone con muy acertadamente c�mo pueden utilizarse las tortugas para tratar muchos de los conceptos sobre geometr�a, matem�ticas y ciencia (por ejemplo, utilizar tortugas para modelar el comportamiento de un insecto).  El ejemplo de **patr�n** que se expone a continuaci�n se ha extra�do de dicho libro. 

.. figure:: Figures/turtle-geometry.jpg
    :width: 200px
    :align: center
    :alt: a scan of the cover of the book about turtle geometry
    :figclass: align-center

    Figura 1: La portada de la versi�n en ingl�s


El teorema del viaje completo
=============================

El �ltimo fragmento de c�digo es realmente un **patr�n**
que sirve para una gran variedad de formas geom�tricas. Veamos el caso de un tri�ngulo. Puede que no sea algo obvio saber por qu� en este programa hacemos giros de ciento veinte grados (120), pero lo ser� pronto.

.. activecode:: Turtle_Triangle
    :tour_1: "Lines of code"; 1: tR3-line1; 2: tR3-line2; 3: tR3-line3; 4: tR3-line4; 5: tR3-line5; 6: tR3-line6; 7: tR3-line7;
    :nocodelens:
  
    from turtle import *   	# usar la librer�a turtle
    espacio = Screen()    	# crear el espacio de la tortuga
    juan = Turtle()   		# crear la tortuga Juan
    juan.setheading(90)   	# apuntar al norte
    for lados in range(3):	# repetir tres veces
      	juan.forward(100)    	# avanzar 100
      	juan.right(120)         	# girar 120 grados

Veamos ahora el pent�gono.

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

El **Teorema del viaje completo de la tortuga** establece que la tortuga dibujar� una figura cerrada de *n* lados cuando la suma de sus �ngulos sea m�ltiplo de 360. En el ejemplo del tri�ngulo ``3 * 120 = 360``, y en el del pent�gono ``5 * 72 = 360``. 

En el programa siguiente, cambia los signos ``??`` de la l�nea 7 por el n�mero de grados que debe girar cada vez para dibujar un pol�gono de doce lados, tambi�n llamado dodec�gono. Si lo haces correctamente, la tortuga dibujar� un pol�gono cerrado de doce lados.

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
   :feedback_a: No se cerrar� la figura
   :feedback_b: �Perfecto! 12 * 30 = 360
   :feedback_c: No, 12 * 12 es 144, que no es m�ltiplo de 360
   :feedback_d: Esto generar� un cuadrado, tres veces. 12 * 90 = 1080 = 360 * 3

   �Cu�nto necesita girar ``maria`` en este programa para crear un dodec�gono cerrado (doce lados)? Solo una de las soluciones es v�lida.
   
.. parsonsprob:: 10_2_2_Triangle

   El siguiente programa utiliza una tortuga para dibujar un tri�ngulo como el que est� representado a la izquierda, <img src="../_static/TurtleTriangle.png" width="150" align="left" hspace="10" vspace="5"/> pero las l�neas est�n desordenadas. El programa deber�a contener todas las instrucciones para crear una tortuga. Despu�s, iterar� tres veces en un bucle, y en cda una de esas veces deber� avanzar cien pixels, y girar a la izquierda ciento veinte grados. Despu�s, la pantalla deber� cerrarse cuando el usuario haga clc sobre ella.<br /><br /><p>Arrastra los bloques con las instrucciones que est�n a la izquierda, y col�calos en la parte derecha en el orden correcto, y con la indentaci�n apropiada. Haz clic en <i>Check Me</i> para comprobar el resultdo. El ejercici� te indicar� si alguna de las l�neas no est� en el orden correcto, o si no est� bien indentada</p> 
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



