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
	:prefix: csp-10-3-

Patrones dentro de patrones
===========================

Ya sabemos c�mo utilizar un patr�n para construir cualquier pol�gono. Ahora podemos meter este patr�n dentro de otro para crear un `espir�grafo <https://es.wikipedia.org/wiki/Espir%C3%B3grafo>`_ .  En el siguiente ejemplo se utilizan pent�gonos, pero se puede hacer tambi�n con cualquier otro pol�gono.

..	index::
	pair: bucles for; anidados
	single: setExecutionLimit

.. note::
   En la l�nea 8 del siguiente c�digo, el bucle ``for`` m�s externo se ejecuta veinte veces, mientras que en la l�nea 13 el bucle ``for`` interno se ejecuta cinco veces por cada una de las veces del bucle externo. Cinco veces cuando el bucle externo vale 0, cinco veces cuando el bucle externo vale 1, cinco veces cuando el bucle externo vale 2, y as� sucesivamente. El bucle interno se ejecuta un total de 20 * 5 = 100 veces. A la tortuga puede llevarle un tiempo para completar este patr�n. Normalmente el c�digo dentro del navegador est� limitado para que la ejecuci�n dure un m�ximo de diez segundos. Pero podemos usar el procedimiento ``setExecutionLimit(milliseconds)`` de la librer�a ``sys`` (abreviatura de system) para especificar un n�mero diferente de milisegundos de ejecuci�n. Un segundo son 1.000 milisegundos, as� que 50.000 son cincuenta segundos.

.. activecode:: Turtle_Spirograph1
    :tour_1: "Lines of code"; 1-2: tr3-line1-2; 3: tr3-line3; 4: tr3-line4; 5: tr3-line5; 6: tr3-line6; 8: tr3-line8; 9: tr3-line9; 10: tr3-line10; 13: tr3-line13; 14: tr3-line14; 15: tr3-line15;
    :nocodelens:
	
    from turtle import *     
    from sys import *        # usar la libreria system
    setExecutionLimit(50000) # establece 50 segundos de ejecucion
    espacio = Screen()         
    fede = Turtle()           
    fede.setheading(90)       
    
    for repeticion in range(20):   # patron de veinte veces
      	fede.forward(10)         	# desplaza un poco la figura
      	fede.right(18)             	# y gira unos grados
      
      	# Esta parte dibuja un pentagono
      	for lados in range(5):    # repite cinco veces
      	    fede.forward(50)         
      	    fede.right(72)           

Si cambiamos el color del trazo, podremos distinguir entre la parte que dibuja las figuras geom�tricas y la que dibuja el resto.

.. activecode:: Turtle_Spirograph2
    :tour_1: "Lines of code"; 1-2: tr3-line1-2; 3: tr3-line3; 4: tr3-line4; 5: tr3-line5; 6: tr3-line6; 8: tr3-line8; 9: ts2-line9; 10: ts2-line10; 11: ts2-line11; 12: ts2-line12; 15: ts2-line15; 16: ts2-line16; 17: ts2-line17; 
    :nocodelens:
	
    from turtle import *      
    from sys import *         
    setExecutionLimit(50000)  
    espacio = Screen()          
    fede = Turtle()            
    fede.setheading(90)        
    
    for repeticion in range(20):    
      	fede.pencolor("green")     # cambia a color verde
      	fede.forward(10)            
      	fede.right(18)              
      	fede.pencolor("red")       # cambia a color rojo
      
     	# Esta parte dibuja el pentagono
      	for lados in range(5):     
            fede.forward(50)          
            fede.right(72)            


.. parsonsprob:: 10_3_1_Turtle_Spiro

   Hay una forma de colocar las siguientes instrucciones para que se cree esta imagen.<img src="../_static/TurtleColoredImage.png" width="200" align="left" hspace="10" vspace="5" /> Arrastra los bloques de c�digo de la parte izquierda y col�calos en orden en la parte derecha, respetando la indentaci�n correcta.
   -----
   from turtle import *
   from sys import *    
   setExecutionLimit(50000)  
   wn = Screen()
   mateo = Turtle()
   mateo.setheading(90)
   
   =====
   for repeticion in range(20):
   =====
       mateo.pencolor("red")
       mateo.forward(10)
       mateo.left(18)
      
   =====
       for lados in range(3):
   =====
           mateo.pencolor("blue")
           mateo.forward(50) 
           mateo.right(120)
         


