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
	:prefix: csp-6-5-
	
.. highlight:: java
   :linenothreshold: 4


|bigteachernote| Nota para el profesor: Crear procedimientos con par�metros
===================================================================

Seguramente no te encuentres a�n muy c�modo creando procedimientos con par�metros. Es normal. Nuestra investigaci�n sobre c�mo las personas aprendemos a programar revela que entender c�mo los *nombres* pueden representar *otra cosa* requiere de mucha pr�ctica. Los que son nuevos en esto de la programaci�n seguramente preferir�n esta opci�n:

:: 

   from turtle import *    
   espacio = Screen()    		
   malik = Turtle()   		
   malik.forward(100)
   malik.right(90)
   malik.forward(100)
   malik.right(90)
   malik.forward(100)
   malik.right(90)
   malik.forward(100)
   malik.right(90)

Para crear un procedimiento ``cuadrado`` como el que se muestra a continuaci�n

:: 

   def cuadrado(tortuga,tama�o):
       tortuga.forward(tama�o)
       tortuga.right(90)
       tortuga.forward(tama�o)
       tortuga.right(90)
       tortuga.forward(tama�o)
       tortuga.right(90)
       tortuga.forward(tama�o)
       tortuga.right(90)

y llamando entonces al procedimiento ``cuadrado`` de esta manera

:: 

   from turtle import *     # use the turtle library
   espacio = Screen()    	# crea una pantalla(espacio)
   malik = Turtle()   	# crea la tortuga Malik
   cuadrado(malik, 100)     # dibuja un cuadrado de lado 100

 
Cuando las personas se inician en la programaci�n, prefieren ver los valores reales como ``forward(100)`` en lugar de ``forward(tama�o)``. Probablemente pueden reconocer que disponer de una funci�n ``cuadrado`` que construye cuadrados de cualquier tama�o es flexible y potente. Pero, a�n se encuentran en el paso de intentar entender los comandos b�sicos del manejo de tortugas.

..	index::
	single: abstraction 

No te preocupes todav�a por la creaci�n de procedimientos con par�metros. Ya llegaremos a eso m�s tarde, en el cap�tulo sobre **abstracci�n**. **Abstracci�n** se refiere a la acci�n de poner la atenci�n solamente en los detalles importantes de algo, como por ejemplo en la figura abstracta que permite identificar los servicios para mujeres, como se muestra a continuaci�n. 

.. figure:: Figures/femaleIcon.jpg
    :height: 100px
    :align: center
    :alt: representaci�n abstracta de una mujer 
    :figclass: align-center

    Figura 2: Representaci�n abstracta de una mujer

Por ahora es suficiente con que podamos leer los procedimientos y entender qu� sucede cuando los llamamos. A medida que los aprendices se sienten m�s a gusto con las bases de la programaci�n, pueden encontrase m�s preparados para utilizar la abstracci�n, usando nombres para representar cosas a trav�s de nuevos procedimientos y funciones.
