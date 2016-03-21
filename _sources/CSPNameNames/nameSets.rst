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
	:prefix: csp-6-6-
	
.. highlight:: java
   :linenothreshold: 4

Nombrar conjuntos de procedimientos
===================================

Hasta ahora hemos visto c�mo se asignan nombres a valores, por ejemplo, las variables que almacenan cadenas de caracteres o n�meros. Tambi�n hemos aprendido a nombrar (*definir*) funciones o procedimientos y a usar otros nombres paa guardar las entradas a esas funciones y procedimientos.

En ocasiones, te parecer� �til disponer de un grupo completo de funciones y/o procedimientos, y necesitar�s almacenarlos en alg�n lugar, y *dar un nombre* a ese *conjunto de funciones y procedimientos*. Ver�s que puedes hacerlo. Es m�s, ya lo has hecho.

.. index::
	single: import, from import

Es lo que haces cuando ejemcutas una instrucci�n como ``from turtle import *``. Es en ese momento cuando se definen procedimientos como ``forward`` y ``right``, y funciones como ``Screen``. Se pueden meclar los procedimientos y funciones que *nosotros* definimos con otros procedimientos y funciones que *importamos*.

.. activecode:: Squares_Pattern
  :tour_1: "Important lines tour"; 1-9: sqM-line1-9; 11-13: sqM-line11-13; 14: sqM-line14; 15: sqM-line15; 16: sqM-line16; 17: sqM-line17; 18: sqM-line18; 19: sqM-line19; 20: sqM-line20; 21: sqM-line21; 22: sqM-line22; 23: sqM-line23; 
  :nocodelens:

  def cuadrado(tortuga,tam�o):
      tortuga.forward(tam�o)
      tortuga.right(90)
      tortuga.forward(tam�o)
      tortuga.right(90)
      tortuga.forward(tam�o)
      tortuga.right(90)
      tortuga.forward(tam�o)
      tortuga.right(90)

  from turtle import *      
  espacio = Screen()          
  emilia= Turtle()          # crea una tortuga llamada emilia
  emilia.setheading(90)      # apunta al norte
  emilia.forward(10)         
  emilia.right(18)           
  cuadrado(emilia,100)   	# dibuja un cuadrado de tama�o 100
  emilia.forward(10)         
  emilia.right(18)           
  cuadrado(emilia,100) 		
  emilia.forward(10)         
  emilia.right(18)           
  cuadrado(emilia,100)  		

.. mchoicemf:: 6_6_1_Function_Use_Q1
   :answer_a: cuadrado
   :answer_b: forward
   :answer_c: right
   :answer_d: Todos los anteriores
   :correct: d
   :feedback_a: Puedes usar cuadrado porque ya lo has definido antes, pero tambi�n puedes utilizar otros.
   :feedback_b: Puedes utilizar forward porque lo has importado, pero tambi�n puedes usar otros.
   :feedback_c: Puedes utilizar right porque lo has importado, pero tambi�n puedes usar otros.
   :feedback_d: S�, puedes utilizar todos los procedimientos y funciones de tortugas porque los has importado, y adem�s puedes usar cuadrado porque lo has definido.
   
   Imagina que quieres a�adir una l�ne al programa anterior. �Qu� procedimiento puedes utilizar con seguridad, porque ya se ha definido? 


