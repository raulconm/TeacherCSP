..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

..  shortname:: Chapter: What You Can Do with a Computer
..  description:: Some tidbits of what you can do with a computer

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-1-4-


.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |teachernote| image:: Figures/apple.jpg
    :width: 26px
    :align: bottom
    :alt: teacher note



Computación con tortugas
========================

No, aquí la tortuga no es un animal. 
Vams a trabajar con una tortuga virtual, una idea de los años sesenta. La tortuga robótica original llevaba un lapiz. Los estudiantes de programación la desplazaban utilizando programas que ellos escribían, y creaban así dibujos con el lapiz. 

.. figure:: Figures/mindstorms_turtle.jpg 
    :width: 200px
    :align: center
    :alt: Children playing with a Logo turtle robot that can draw with a pen
    :figclass: align-center
    
    Imagen 3: Niños jugando con un robot tortuga de Logo, que podía hacer dibujos con el lapiz
    
..	index::
	single: comment
	single: library
	single: screen
	pair: turtle; screen
	pair: turtle; library
	pair: programming; comment
	pair: program; comment
    
Hoy en día podemos jugar con tortugas virtuales sin tener que emplear robots, y en un entorno gráfico completo. El siguiente programa en Python comienza cargando una **librería** que contiene el código que nos permite trabajar con las tortugas (``from turtle import *``). A continuación crea una **Screen**, un espacio donde la tortuga se puede mover, y dibujar (``espacio = Screen()``). Después crea una tortuga llamada ``alex`` (``alex = Turtle()``), y finalmente mueve a ``alex`` por la pantalla (``alex.forward(150)``), de manera que según se va desplazando va también dibujando. Cualquier texto precedido por un caracter ``#`` se llama comentario. Python y el ordenador ignorarán cualquier cosa que aparezca en la línea a continuación de ``#``. Los **comentarios** explican lo que hacen los programas, y sirven para que los lean las personas, no los ordenadores.
    
Haz clic en |runbutton| para ver lo que hace el siguiente programa.

.. activecode:: Turtle_1
    :tour_1: "Line-by-line Tour"; 1: first-turtle-line-1; 2: first-turtle-line-2; 3: first-turtle-line-3; 4: first-turtle-line-4; 5: first-turtle-line-5; 6: first-turtle-line-6;
    :nocodelens:
	
    from turtle import *  # carga la librería turtle para utilizarla
    espacio = Screen()	  # crea el espacio donde va a estar la tortuga
    alex = Turtle()   	  # crea una tortuga y la llama alex
    alex.forward(150)	  # se mueve hacia adelante ciento cincuenta unidades
    alex.left(90)   	  # gira noventa grados
    alex.forward(75)	  # se mueve hacia adelante setenta y cinco unidades 
   
   
..	index::
	single: dot notation
	
.. Note::
    Fíjate que le decimos a ``alex`` qué hacer utilizando **notación por punto**: ``alex.forward(150)``, ``alex.left(90)``, y ``alex.forward(75)``. Así es como te comunicas con la tortuga. Utilizas su nombre seguido de un ``.``, y a continuación indicas lo que quieres que haga.

.. mchoicemf:: 1_4_1_Turtle_Q1
   :answer_a: Norte
   :answer_b: Oeste
   :answer_c: Sur
   :answer_d: Este
   :correct: d
   :feedback_a: Comprueba en qué dirección ha comenzado alex a moverse
   :feedback_b: Comprueba en qué dirección ha comenzado alex a moverse
   :feedback_c: Comprueba en qué dirección ha comenzado alex a moverse
   :feedback_d: La tortuga apunta inicialmente al este
   
   ¿En qué dirección se va a mover alex cuando se ejecute este código?   

   :: 
   
      from turtle import *       
      espacio = Screen()    		  
      alex = Turtle()   		
      alex.forward(100)  

Simplemente moviéndola hacia adelante, hacia atrás, a izquierda y a derecha, podemos hacer que la tortuga dibuje una forma.

.. fillintheblank:: 1_4_2_Shape
   :correct: ^cuadrado$|^Cuadrado$|^CUADRADO$
   :feedback1: ('.*','¿Has ejecutado el programa?')
   :blankid: shapeBlank

   ¿Qué forma dibujará el siguiente programa cuando hagas clic en el botón *Run*? :textfield:`shapeBlank::medium`
   

.. activecode:: Turtle_2
    :tour_1: "Line-by-line Tour"; 1: t1-line1; 2: t1-line2; 3: t1-line3; 4: t1-line4; 5: t1-line5; 6: t1-line6; 7: t1-for100-1; 8: t1-right90-1; 9: t1-for100-2; 10: t1-right90-2; 11: t1-for100-3; 12: t1-right90-3; 
    :nocodelens:
	
    from turtle import *	# utiliza la librería turtle
    espacio = Screen()    	# crea un espacio para la tortuga (espacio)
    juan = Turtle()   		# crea una tortuga llamada juan
    juan.setheading(90) 	# la orienta hacia el norte
    juan.forward(100)   	# le dice a juan que se mueva cien unidades hacia adelante
    juan.right(90)       	# gira noventa gados
    juan.forward(100)   	# le dice a juan que se mueva cien unidades hacia adelante
    juan.right(90)       	# gira noventa gados
    juan.forward(100)   	# le dice a juan que se mueva cien unidades hacia adelante
    juan.right(90)      	# gira noventa gados
    juan.forward(100)   	# le dice a juan que se mueva cien unidades hacia adelante
    juan.right(90)      	# gira noventa gados
   
