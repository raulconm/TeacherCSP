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
	:prefix: csp-5-3-
	
.. highlight:: java
   :linenothreshold: 4

Modificar los programas con tortugas
====================================

Ejecuta el siguiente programa.

.. activecode:: Turtle_Names4
    :tour_1: "Line-by-line Tour"; 1: first-turtle-line-1; 2: first-turtle-line-2; 3: first-turtle-line-3; 4: first-turtle-line-4; 5: first-turtle-line-5; 6: first-turtle-line-6;
    :nocodelens:
	
    from turtle import * 	# usa la libreria de tortugas
    espacio = Screen()    	# crea el espacio para la tortuga
    alex = Turtle()      	# crea la tortuga Alex
    alex.forward(150)     	# le dice a Alex que avance 150 unidades
    alex.left(90)       	# le indica que gire 90 grados
    alex.forward(75)      	# le dice a Alex que avance 75 unidades

.. mchoicemf:: 5_3_1_Turtle_Names4_Q1
   :answer_a: Cambiar el 150 por 90
   :answer_b: Cambiar el 75 por 90
   :answer_c: Cambiar el 75 por 150
   :correct: c
   :feedback_a: La tortuga avanza 150 unidades y gira 90 grados.
   :feedback_b: La tortuga avanza 75 unidades y gira 90 grados.
   :feedback_c: As� ambos lados medir�an 150 unidades.

   �Qu� modificaci�n debes hacer en el programa si quieres que ambas l�neas tengan la misma longitud? (�Haz los cambios que consideres y pulsa *Run* para ver si lo has hecho correctamente!)


**Un poco m�s complicado:** Ahora vamos a conectar el punto final con el inicial. Crearemos entonces un tri�ngulo rect�ngulo (que tiene un �ngulo de 90 grados en su interior). El n�mero 57 no se ha elegido al azar -- es aproximadamente el valor de la raiz cuadrada de 40^2 + 40^2.  Sin embargo, en este programa hay un error, y por ello no funciona como se espera.   **�Puedes encontrarlo y arreglarlo?**  

.. activecode:: Turtle_Names5
    :nocodelens:
	
    from turtle import * 	# usa la libreria de tortugas
    espacio = Screen()     	# crea el espacio para la tortuga
    alex = Turtle()      	# crea la tortuga Alex
    alex.forward(40)     	# indica a alex que avance 40 unidades
    alex.left(90)       	# gira 90 grados
    alex.forward(40)     	# completa el segundo lado del triangulo
    alex.left(0)         	# el valor 0 relmente no hace nada
    alex.forward(57)      	# cierra el tri�ngulo


.. mchoicemf:: 5_3_2_Turtle_Names5_Q1
   :answer_a: alex.left(45)
   :answer_b: alex.left(90)
   :answer_c: alex.left(135)
   :correct: c
   :feedback_a: La tortuga ira hacia el exterior, no hacia el interior.
   :feedback_b: Esto dibujar�a otro �ngulo recto, que ser�a lo adecuado para crear un cuadrado.
   :feedback_c: Los �ngulos interiores de un tri�ngulo deben sumar 180. Hasta este momento tenemos un �ngulo de 90, as� que faltar�an dos �ngulos m�s, cuya suma deber�a ser otros 90. Ambos deben ser de 45 grados, pero le indicamos a la tortuga que gire el �ngulo hacia el exterior de forma que 180 - 45 = 135.

   La instrucci�n ``alex.left(0)`` no hace que la tortuga gire en la direcci�n del punto inicial. �Cu�l de las l�neas siguientes ser�a la correcta?
   
.. parsonsprob:: 5_3_3_Turtle-T

   El siguiente programa utiliza una tortuga para dibujar una letra T may�scula, como la que aparece representada a la izquierda, <img src="../_static/TurtleT.png" width="150" align="left" hspace="10" vspace="5"/> pero las l�neas de c�digo est�n desordenadas. El programa debe crear el espacio de trabajo y crear la tortuga. A continuaci�n hay que girar la tortuga hacia el norte, y dibujar una l�nea de 150 pixels, girar despu�s hacia el oeste, y trazar una l�nea de 50 pixels de longitud. Despu�s, la tortuga debe girar 180 grados y dibujar otra l�nea de 100 pixels. Para terminar, hay que indicar que se cierre la ventana cuando el usuario haga clic sobre ella.<br /><br /><p>Arrastra los bloques desde la parte izquierda hasta la derecha en el orden correcto. Pulsa <i>Check Me</i> para comprobar si lo has hecho bien. El ejercicio te indicar� en caso de que hayas cometido cualquier error.</p>
   -----
   from turtle import *
   =====
   espacio = Screen()    	
   marcos = Turtle()
   ===== 
   marcos.setheading(90) 
   =====                
   marcos.forward(150)
   =====
   marcos.left(90)
   marcos.forward(50)
   =====
   marcos.right(180)
   marcos.forward(100)
   


