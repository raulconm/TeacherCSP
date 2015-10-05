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
	:prefix: csp-6-4-
	
.. highlight:: java
   :linenothreshold: 4

Nombrar entradas
================

¿Qué podemos hacer para dibujar un cuadrado de diferente tamaño, por ejemplo uno cuyo lado tenga una longitud de 50? Podríamos modificar cada una de las llamadas a la instrucción ``forward`` como se muestra a continuación.

.. activecode:: Function_Change_Size
  :tour_1: "Important lines tour"; 1-9: sq50-line1-9; 2,4,6,8: sq50-line2468; 11-13: sq50-line11-13; 14: sq50-line14; 
  :nocodelens:

  def cuadrado(turtle):
      turtle.forward(50)
      turtle.right(90)
      turtle.forward(50)
      turtle.right(90)
      turtle.forward(50)
      turtle.right(90)
      turtle.forward(50)
      turtle.right(90)

  from turtle import * 	# usa la librería turtle
  espacio = Screen()    	# crea un espacio para la tortuga
  malik = Turtle()    	# crea una tortuga llamada malik
  cuadrado(malik)          # dibuja un cuadrado con malik
  

Pero, esto implica que tendremos que modificar cuatro veces las instrucciones ``forward``, y podríamos equivocarnos al poner el valor. ¿Hay una manera mejor de hacerlo? ¿Y si creamos la variable ``longitud`` y definimos en ella el valor que queremos que se mueva la tortuga hacia delante?

.. activecode:: Function_Add_Var
  :tour_1: "Important lines tour"; 1-10: sqvar-line1-10; 2: sqvar-line2; 3: sqvar-line3; 4: sqvar-line4; 5-10: sqvar-line5-10; 12-14: sqvar-line12-14; 15: sqvar-line15;
  :nocodelens:

  def cuadrado(tortuga):
      longitud = 50
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)

  from turtle import *	# usa la librería turtle
  espacio = Screen()    	# crea el espacio para la tortuga
  malik = Turtle()    	# crea una tortuga llamada malik
  cuadrado(malik)      	# dibuja un cuadrado con malik
  
.. mchoicemf:: 6_4_1_Function_Var_Q1
   :answer_a: 100
   :answer_b: 50
   :answer_c: 200
   :answer_d: 90
   :correct: c
   :feedback_a: ¿Qué distancia avanzará?
   :feedback_b: ¿Qué valor se le ha dado a longitud?
   :feedback_c: En la línea 2 se ha fijado en 200 el valor de longitud, así que dibujará un cuadrado de 200 unidades de lado.
   :feedback_d: La tortuga gira 90 grados. No avanza 90 grados.  

   ¿Cuál es la longitud del lado en el cuadrado que se dibuja con el siguiente procedimiento? 
   
    :: 
 
     def cuadrado(tortuga):
         longitud = 200
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)

Ahora el programa es más fácil de modificar porque solamente necesitamos cambiar una línea, ``longitud = 50`` para que se dibuje un cuadrado de distinto tamaño. Pero, sigue siendo necesario modificar el programa para que el tamaño del lado sea distinto. ¿Hay una manera mejor de hacerlo?

Podemos agregar una entrada adicional a la función para especificar el tamaño del cuadrado. Separaremos los nombres de las entradas con una coma: ``(tortuga,longitud)`` como se muestra a continuación, y nos aseguraremos de indicar el tamaño cuando hagamos la llamada al procedimiento ``cuadrado(malik, 100)`` o ``cuadrado(malik, 50)``.

.. activecode:: Function_Call2
  :tour_1: "Important lines tour"; 1-9: dsq3-line1-9; 2: dsq3-line2; 11-13: dsq3-line11-13; 14: dsq3-line14; 15: dsq3-line15; 16: dsq3-line16; 17: dsq3-line17;
  :nocodelens:

  def cuadrado(tortuga,longitud):
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)
      tortuga.forward(longitud)
      tortuga.right(90)

  from turtle import *	# usa la librería turtle
  espacio = Screen()    	# crea un espacio para la tortuga
  malik = Turtle()    	# crea la tortuga malik
  cuadrado(malik, 100) 	     # dibuja un cuadrado de lado 100
  cuadrado(malik, 75)   	# dibuja un cuadrado de lado 75
  cuadrado(malik, 50)    	# dibuja un cuadrado de lado 50
  cuadrado(malik, 25)   	# dibuja un cuadrado de lado 25
  
.. mchoicemf:: 6_4_2_Name_The_Shape_Q1
   :answer_a: cuadrado
   :answer_b: rectángulo
   :answer_c: triángulo
   :correct: b
   :feedback_a: Observa el segundo y cuarto forward. ¿Cuánto se va a desplazar hacia delante?
   :feedback_b: Dibujará un rectángulo que con dos lados del tamaño especificado y los otros dos con la mitad de ese valor.  Copia el código en la parte superior y ejecútalo.  
   :feedback_c: Un triángulo tiene tres lados.

   ¿Qué forma geométrica dibujará el siguiente código? 
   
   :: 
 
     def misterio(tortuga,longitud):
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud / 2)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud / 2)
         tortuga.right(90)
      
     from turtle import *	# use la librería turtle
     espacio = Screen()    	# crea el espacio par la tortuga
     malik = Turtle()     	# crea la tortuga malik
     mystery(malik, 100)   	# dibuja algo de longitud = 100


.. index:: 
	single: arguments
.. index:: 
	single: actual parameters
.. index:: 
	single: parameters
.. index:: 
	single: formal parameters
	pair: parameters; formal
	pair: parameters; actual
  
Las entradas especificadas en la definición de una función o procedimiento se llaman también **parámetros** o **parámetros formales**. Así pues ``tortuga`` y ``longitud`` son parámetros (o parámetros formales) del procedimiento ``cuadrado``. Observa que cuando llamamos al procedimiento ``cuadrado`` tenemos que especificar los valores reales para las entradas. A estos valores reales que se pasan como entrada a la función se les llama **argumentos** o **parámetros reales**. En la llamada a ``cuadrado(malik, 50)`` ambos ``malik`` y ``50`` son argumentos (parámetros reales) del procedimiento ``cuadrado``.   

.. mchoicemf:: 6_4_3_Name_Args_Q1
   :answer_a: tortuga y longitud
   :answer_b: malik y 25
   :answer_c: imani y 25
   :correct: c
   :feedback_a: Esos son los nombres de los parámetros (parámetros formales).  
   :feedback_b: Mira de nuevo el código anterior. ¿Es ese el lombre de la tortuga?
   :feedback_c: La tortuga se llama imani y su longitud es 25 en el código: cuadrado(imani, 25). 

   Cuáles son los argumentos (parámetros reales) en este código?  
   
   :: 
 
     def cuadrado(tortuga,longitud):
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
         tortuga.forward(longitud)
         tortuga.right(90)
     
     from turtle import * 	# usa la librería turtle
     espacio = Screen()    	# crea el espacio para la tortuga
     imani = Turtle()    	# crea la tortuga imani
     cuadrado(imani, 25)   # dibuja un cuadrado de lado 25
     
.. parsonsprob:: 6_4_4_Draw_Squares

   Para el siguiente código se asume que se ha definido un procedimiento llamado cuadrado que toma como valor de entrada la longitud del lado. El código debe crear una tortuga y utilizarla para dibujar un cuadrado, moverse a cotninuación hacia delante, y dibujar un segundo cuadrado como el que se muestra a la izquierda, <img src="../_static/SquareForwardSquare.png" width="150" align="left" hspace="10" vspace="5"/> pero las líneas de código están desordenadas. Arrástralas a la zona de la derecha colocándolas en el orden correcto.
 
   -----
   from turtle import *    
   =====
   espacio = Screen()    		
   imani = Turtle()   		
   =====
   cuadrado(imani, 75)
   =====
   imani.forward(100)
   =====
   cuadrado(imani, 50)

