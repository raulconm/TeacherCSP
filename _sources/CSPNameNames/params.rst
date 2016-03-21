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


|bigteachernote| Nota para el profesor: Crear procedimientos con parámetros
===================================================================

Seguramente no te encuentres aún muy cómodo creando procedimientos con parámetros. Es normal. Nuestra investigación sobre cómo las personas aprendemos a programar revela que entender cómo los *nombres* pueden representar *otra cosa* requiere de mucha práctica. Los que son nuevos en esto de la programación seguramente preferirán esta opción:

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

Para crear un procedimiento ``cuadrado`` como el que se muestra a continuación

:: 

   def cuadrado(tortuga,tamaño):
       tortuga.forward(tamaño)
       tortuga.right(90)
       tortuga.forward(tamaño)
       tortuga.right(90)
       tortuga.forward(tamaño)
       tortuga.right(90)
       tortuga.forward(tamaño)
       tortuga.right(90)

y llamando entonces al procedimiento ``cuadrado`` de esta manera

:: 

   from turtle import *     # use the turtle library
   espacio = Screen()    	# crea una pantalla(espacio)
   malik = Turtle()   	# crea la tortuga Malik
   cuadrado(malik, 100)     # dibuja un cuadrado de lado 100

 
Cuando las personas se inician en la programación, prefieren ver los valores reales como ``forward(100)`` en lugar de ``forward(tamaño)``. Probablemente pueden reconocer que disponer de una función ``cuadrado`` que construye cuadrados de cualquier tamaño es flexible y potente. Pero, aún se encuentran en el paso de intentar entender los comandos básicos del manejo de tortugas.

..	index::
	single: abstraction 

No te preocupes todavía por la creación de procedimientos con parámetros. Ya llegaremos a eso más tarde, en el capítulo sobre **abstracción**. **Abstracción** se refiere a la acción de poner la atención solamente en los detalles importantes de algo, como por ejemplo en la figura abstracta que permite identificar los servicios para mujeres, como se muestra a continuación. 

.. figure:: Figures/femaleIcon.jpg
    :height: 100px
    :align: center
    :alt: representación abstracta de una mujer 
    :figclass: align-center

    Figura 2: Representación abstracta de una mujer

Por ahora es suficiente con que podamos leer los procedimientos y entender qué sucede cuando los llamamos. A medida que los aprendices se sienten más a gusto con las bases de la programación, pueden encontrase más preparados para utilizar la abstracción, usando nombres para representar cosas a través de nuevos procedimientos y funciones.
