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
	:prefix: csp-6-3-
	
.. highlight:: java
   :linenothreshold: 4

Nombrar conjuntos de pasos
==========================

�C�mo se han definido ``abs`` e ``int``? *Definiendo* un nuevo  procedimiento o una funci�n podemos asociar un nombre con una secuencia de pasos. Observa el siguiente programa. �Qu� crees que ocurrir� cuando pulses el bot�n de ejecutar? Haz clic en *Run* y mira lo que sucede.

.. activecode:: First_Function
  :tour_1: "Line by line tour"; 1: dsq-line1; 2: dsq-line2; 3: dsq-line3; 4: dsq-line4; 5: dsq-line5; 6: dsq-line6; 7: dsq-line7; 8: dsq-line8; 9: dsq-line9;
  :nocodelens:

  def cuadrado(unaTortuga):
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)

Si est�s pensando por qu� parece que no ocurre nada cuando pulsas el bot�n *Run*, observa que lo que hace el programa es definir el procedimiento ``cuadrado``, que recoge como entrada una tortuga definida como ``unaTortuga``. Si queremos que el programa ejecute algo m�s tendremos que crear una tortuga y **llamar** al procedimiento como lo hacemos en el siguiente ejemplo.

..	index::
	single: def
	single: functions
	single: calling functions

.. activecode:: First_Function_Call
  :tour_1: "Important lines tour"; 1-9: dsq2-line1-9; 11-13: dsq2-line11-13; 14: dsq2-line14;
  :nocodelens:

  def cuadrado(unaTortuga):
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)
      unaTortuga.forward(100)
      unaTortuga.right(90)

  from turtle import * 	# usa la libreria turtle
  espacio = Screen()     	# crea el espacio para la tortuga
  Mario = Turtle()    	# crea la tortuga Mario
  cuadrado(Mario)       	# dibuja un cuadrado con Mario
  
..	index::
	single: parameter
	pair: programming; parameter    

En el ejemplo anterior *DEFinimos* la palabra ``cuadrado`` para enumerar las instrucciones de Python con las que dibujaremos un cuadrado utilizando una tortuga. El procedimiento ``cuadrado`` toma ``unaTortuga`` como dato de entrada, y con ella dibujar� el cuadrado. Observa que la secuencia de instrucciones incluidas en el procedimiento ``cuadrado`` est� indentada. Esto es que las l�neas de instrucciones no comienzan en la primera columna, debajo de la palabra ``def``, sino unas posiciones m�s a la derecha. Python utiliza la indentaci�n para indicar qu� instrucciones forman parte del procedimiento. El hecho de que la l�nea ``from turtle import *`` no est� indentada significa que esa instrucci�n y las siguientes ya no forman parte del procedimiento ``cuadrado``.

.. Note::
   Observa que hemos definido el procedimiento ``def cuadrado(unaTortuga):`` antes de intentar utilizarlo con ``cuadrado(Mario)``. En Python es necesario que suceda en ese orden, pero no hace falta en otros lenguajes de programaci�n.

.. mchoicemf:: 6_3_1_Functions_Q2
   :answer_a: Es un procedimiento.
   :answer_b: Es una funci�n.
   :correct: b
   :feedback_a: Devuelve un valor, luego es una funci�n.
   :feedback_b: Si devuelve un valor no puede ser un procedimiento.

   �Es ``abs`` un procedimiento, o una funci�n?
   
.. mchoicemf:: 6_3_2_Functions_Q3
   :answer_a: Es un procedimiento.
   :answer_b: Es una funci�n.
   :correct: a
   :feedback_a: No devuelve ning�n valor, as� que es un procedimiento.
   :feedback_b: No puede ser una funci�n, porque no devuelve ning�n valor.

   �Es ``cuadrado`` un procedimiento o una funci�n?
   
F�jate atentamente en el siguiente v�deo para saber c�mo resolver el problema de c�digo desordenado.

.. video:: indentVideo
		   :controls:
		   :thumb: ../_static/video-mixedUpCodeIndent.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/IndentVideo.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/IndentVideo.webm
   
.. parsonsprob:: 6_3_3_Triangle_Procedure

   El siguiente c�digo deber�a definir un procedimiento que dibuje un tri�ngulo, pero puede que las instrucciones est�n desordenadas, e incluso *puede que contenga algunas l�neas de c�digo in�til*. Arrastra a la parte derecha y en el orden correcto las l�neas de c�digo que se necesiten. <b>Recuerda que las l�neas de instrucciones que forman parte del procedimiento deben estar indentadas</b>. Para indentar esas l�neas arr�stralas un poco m�s a la derecha.
 
   -----
   def triangulo(unaTortuga):
   =====
       unaTortuga.left(60)
       unaTortuga.forward(100)
       unaTortuga.right(120)
       unaTortuga.forward(100)
       unaTortuga.right(120)
       unaTortuga.forward(100)
       unaTortuga.right(120)  
   ===== 
       endDef #distractor

