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
	:prefix: csp-5-1-
	
.. highlight:: java
   :linenothreshold: 4

Asignar un nombre a una tortuga
===============================

*Objetivos de aprendizaje:*

- Utilizar las asignaciones para nombrar objetos tortuga
- Indicarle a una tortuga que ejecute acciones
- Entender la importancia de usar el objeto adecuado en el orden correcto para que el programa funcione como queremos

..	index::
	single: objects
	
Es posible asignar nombres a otros objetos, no sólo a números o cadenas. Se puede dar nombres también a tortugas o a "screens" (el espacio de la pantalla reservado para dibujar las tortugas). Las tortugas o las screens, entre otros, se conocen como **objetos**. Un objeto, en programación, es cualquier cosa que puede ejecutar acciones en un programa.     

Ya hemos visto este ejemplo anteriormente.

.. activecode:: Turtle_Names1
    :tour_1: "Line-by-line Tour"; 1: t1-line1; 2: t1-line2; 3: t1-line3; 4: t1-line4; 5: t1-line5; 6: t1-line6; 7: t1-for100-1; 8: t1-right90-1; 9: t1-for100-2; 10: t1-right90-2; 11: t1-for100-3; 12: t1-right90-3;
    :nocodelens:
	
    from turtle import *	# usa la libreria de tortugas
    espacio = Screen()	# crea un espacio para la tortuga
    Juan = Turtle() 		# crea la tortuga Juan
    Juan.setheading(90)	# Apunta al norte
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(90)   		# Gira 90 grados
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(90)   		# Gira 90 grados
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(90)   		# Gira 90 grados
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(90)    	# Gira 90 grados

Ahora prueba con este otro.  

.. activecode:: Turtle_Names2
    :tour_1: "Line-by-line Tour"; 1: tri-line1; 2: tri-line2; 3: tri-line3; 4: tri-line4; 5: tri-line5; 6: tri-line6; 7: tri-line7; 8: tri-line8; 9: tri-line9; 10: tri-line10;
    :nocodelens:
	
    from turtle import *	# usa la libreria de tortugas
    espacio = Screen()	# crea un espacio para la tortuga
    Juan = Turtle() 		# crea la tortuga Juan
    Juan.setheading(90)	# Apunta al norte
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(120)   	# Gira 120 grados
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(120)   	# Gira 120 grados
    Juan.forward(100)		# Le indica a Juan que avance 100 unidades
    Juan.right(120)   	# Gira 120 grados

.. mchoicemf:: 5_1_1_Turtle_Names2_Q1
   :answer_a: Un cuadrado
   :answer_b: Un triángulo
   :answer_c: Un rectángulo
   :correct: b
   :feedback_a: Eso es lo que hace el primer programa, pero no el segundo.
   :feedback_b: Y ahora, que pasaría si ejecutara un forward y un right adicional. ¿Seguiría siendo un triángulo? ¡Pruébalo!
   :feedback_c: Pero, podrías modificar el primer ejemplo para que haga un rectángulo. ¿Te atreves a cambiar dos líneas en el primer programa para que dibuje en rectángulo?

   ¿Qué figura has dibujado?

Esto funciona porque ``Juan`` es una tortuga, que ejecuta cada instrucción de forma precisa y en orden, una después de otra. Si añadimos otra tortuga con otro nombre, el resultado será distinto. 

.. activecode:: Two_Turtles
    :tour_1: "Line-by-line Tour"; 1: tt-line1; 2: tt-line2; 3: tt-line3; 4: tt-line4; 5: tt-line5; 6: tt-line6; 7: tt-line7; 8: tt-line8; 9: tt-line9; 10: tt-line10; 11: tt-line11; 12: tt-line12;
    :nocodelens:
	
    from turtle import * 	# usa la libreria de tortugas
    espacio = Screen()     	# crea un espacio para la tortuga
    Juan = Turtle()     	# crea la tortuga Juan
    Juan.setheading(90) 	# Apunta al norte
    Juan.forward(100)   	# Le indica a Juan que avance 100 unidades
    Juan.right(120)     	# Gira 120 grados a la derecha
    Juan.forward(100)     	# Le indica a Juan que avance 100 unidades
    Juan.right(120)      	# Gira 120 grados a la derecha
    Ana = Turtle()     	# crea la tortuga Ana
    Ana.color("orange")  	# cambiar el color de Ana
    Ana.forward(100)     	# Le dice a Ana que avance 100 unidades
    Ana.right(120)     	# Gira 120 grados a la derecha
    
.. mchoicemf:: 5_1_2_Turtle_Dir_Q1
   :answer_a: Norte
   :answer_b: Sur
   :answer_c: Este
   :answer_d: Oeste
   :correct: c
   :feedback_a: En algunos de los ejemplos las turtugas se apuntan al norte porque le damos la instrucción <code>setheading(90)</code>. ¿En qué dirección se desplaza Ana inicialmente?
   :feedback_b: ¿En qué dirección se mueve inicialmente Ana en este ejemplo? El norte es el lado superior de la pantalla.
   :feedback_c: Las tortugas miran inicialmente hacia el este, o lo que es lo mismo, hacia el lado derecho de la pantalla.
   :feedback_d: ¿En qué dirección se mueve inicialmente Ana en este ejemplo? El norte es el lado superior de la pantalla.

   ¿En qué dirección apunta inicialmete una tortuga, cuando la creamos?
    
**Programas desordenados**

.. parsonsprob:: 5_1_3_Turtle_L

   El siguiente programa utiliza una tortuga para dibujar una L mayúscula, tal como puedes ver en el dibujo, <img src="../_static/TurtleL4.png" width="150" align="left" hspace="10" vspace="5" /> pero las líneas del programa están desordenadas. El programa tiene que indicar todos los pasos necesarios: importar el módulo para manejar tortugas, crear el espacio para la tortuga, y crear la tortuga. Acuérdate de que cuando creas la tortuga siempre apunta hacia el este. Debes girarla para que apunte al sur, y dibujar entonces una línea recta de 150 pixels de longitud. A continuación debe girar hacia el este y dibujar otra línea de una longitud de 75 pixels. Hemos añadido una brújula al dibujo para indicar el norte, sur, este y oeste. <br /><br /><p>Arrastra los bloques de código desde el lado izquierdo al lado derecho colocándolos en el orden correcto. A continuación pulsa <i>Check Me</i> para comprobar si lo has hecho correctamente. El ejercicio te indicará si has colocado algún bloque en el orden equivocado.</p>

   -----
   from turtle import *
   =====
   espacio = Screen()
   pepa = Turtle()
   =====
   pepa.right(90)
   pepa.forward(150)
   =====
   pepa.left(90)
   =====
   pepa.forward(75)
   
.. parsonsprob:: 5_1_4_Turtle_Check

   El programa siguiente usa una tortuga para dibujar un signo como el que puedes ver a la izquierda, <img src="../_static/TurtleCheckmark4.png" width="150" align="left" hspace="10" vspace="5" /> pero de nuevo las líneas de código están desordenadas. El programa tiene que importar el módulo de manejar tortugas, crear la ventana donde dibujar la tortuga, y finalmente crear la tortuga. Hay que hacer que la tortuga apunte hacia el sureste, dibujar una línea de 75 de longitud, girar hacia el noreste, y dibujar una línea de 150 pixels de largo. Hemos añadido una brújula para indicar dónde están norte, sur, este y oeste. <br /><br /><p>Arrastra los bloques con las instrucciones desde la parte izquierda hasta la parte derecha, y colócalos en el orden correcto. El ejercicio te indicará si has cometido algún error.</p>

   -----
   from turtle import *
   =====
   espacio = turtle.Screen()
   pepe = turtle.Turtle()
   =====
   pepe.right(45)
   =====
   pepe.forward(75)
   =====
   pepe.left(90)
   =====
   pepe.forward(150)
   



