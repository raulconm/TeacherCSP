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
	:prefix: csp-10-1-

Utilizar repeticiones con tortugas
==================================

*Objetivos de aprendizaje:*

- Usar un bucle ``for`` para repetir pasos con tortugas.
- Utilizarlo para dibujar un polígono.

..	index::
	pair: instrucciones; for

Ya hemos utilizado antes tortugas para dibujar cuadrados. Le indicábamos a la tortuga que avanzara y girara a la derecha cuatro veces, pero no utilizábamos *explícitamente* el concepto *cuatro veces*. Podemos pedirle al ordenador de forma explícita que haga algo un número determinado de veces utilizando un bucle ``for``. 


.. activecode:: Turtle_For
    :tour_1: "Lines of code"; 1: tR1-line1; 2: tR1-line2; 3: tR1-line3; 4: tR1-line4; 5: tR1-line5; 6: tR1-line6; 7: tR1-line7;
    :nocodelens:
	
    from turtle import *	# usar la librería turtle
    space = Screen()   	# crear el espacio para la tortuga
    alicia = Turtle()  	# crear la tortuga alicia
    alicia.setheading(90)  	# apuntar al norte
    for lados in [1,2,3,4]:	# repetir 4 veces lo siguiente
    	   alicia.forward(100)      # avanzar 100 unidades
    	   alicia.right(90)         # girar 90 grados

.. mchoicemf:: 10_1_1_Turtle_For_Q1
   :answer_a: [0,1,2,3]
   :answer_b: [0,1,2]
   :answer_c: [2,3,4,5]
   :answer_d: [1,2,3,4,5]
   :correct: b
   :feedback_a: Este cuadrado tendrá cuatro lados, aunque estén numerados de otra forma.
   :feedback_b: Esto sólo dibujará tres lados, porque la lista sólo tiene tres elementos.
   :feedback_c: Este cuadrado tendrá cuatro lados, aunque estén numerados de otra forma.
   :feedback_d: Esta opción <i>sí</i> dibujará un cuadrado. La tortuga pasará dos veces por el primer lado.

   Lo más importante en la lista ``[1,2,3,4]`` no son los números. Es el hecho de que la lista contiene *cuatro* elementos. Solamente una de estas opciones *no* va a construir un cuadrado. ¿Sabes cuál es? (No es trampa probar a ejecutar el programa usando cada una de ellas, para ver cuál es el resultado). 
   
.. parsonsprob:: 10_1_2_Rectangle

   El siguiente programa utiliza una tortuga para dibujar un rectángulo como el que ves a la izquierda, , <img src="../_static/TurtleRect.png" width="150" align="left" hspace="10" vspace="5" /> pero las líneas de código están desordenadas. El programa primero debe crear  el entorno necesario y crear la tortuga. Después, debe pasar dos veces por el bucle, y cada una de las veces la tortuga debe avanzar 175 pixels, girar 90 grados a la derecha, avanzar 150 pixels, y girar 90 grados a la derecha. Una vez terminado el bucle, establecer que la ventana se cierre cuando el usuario haga clic sobre ella.<br /><br /><p>Arrastra los bloques de la parte izquierda y colócalos en orden y con la indentación adecuada en la parte derecha. Haz clic en <i>Check Me</i> para ver si lo has hecho correctamente. El ejercicio te indicará si alguna línea no está en su sitio, o si la indentación es incorrecta.</p>
   
   -----
   from turtle import *      
   =====   
   espacio = Screen()
   carlos = Turtle()
   =====
   # repite 2 veces
   for i in [1,2]:  
   =====   
       carlos.forward(175)
   =====
       carlos.right(90)
   =====  
       carlos.forward(150)
       carlos.right(90)
   
Cuando no importa realmente qué hay en la lista, sino que tenga por ejemplo *cuatro* elementos, hay una forma especial de escribir el bucle. Se trata de utilizar la función ``range``.

.. activecode:: Turtle_For_Range
  :tour_1: "Line-by-line tour"; 1: tR2-line1; 2: tR2-line2; 3: tR2-line3; 4: tR2-line4; 7: tR2-line7; 8: tR2-line8; 9: tR2-line9;
  :nocodelens:
 
  from turtle import *	# usar a libreria turtle
  espacio = Screen()   	# crear el espacio
  marco = Turtle()  		# crear la tortuga
  marco.setheading(90)	# apuntar al norte
  
  # Dibuja el cuadrado
  for lados in range(4):	# repetir lo siguiente 4 veces
      marco.forward(100)   # avanzar 100 unidades
      marco.right(90)      # girar 90 grados


La función ``range`` devuelve un valor para indicarle al bucle *for* cuantas iteraciones debe hacer. En este caso hace que la tortuga avance y gire a la derecha *cuatro* veces.

.. |turtlegeometry| image:: Figures/turtle-geometry.jpg
    :width: 200px
    :align: top
    :alt: teachernote




