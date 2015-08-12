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
	:prefix: csp-6-2-
	
.. highlight:: java
   :linenothreshold: 4

Nombrar procedimientos y funciones
========================================

..	index::
	single: procedure
	pair: programming; procedure
	
..	index::
	single: function
	pair: programming; function	
	
Hemos visto c�mo podemos utilizar nombres para representar n�meros (enteros como ``3`` y ``-325``, o decimales como ``2.4`` y ``-322.9392``), cadenas (como ``"Hola a todos"``), tortugas, e im�genes. Cuando hacemos c�lculos utilizando los nombres, el ordenador buscar� qu� valor est� asociado a cada nombre, y utilizar� esos valores en los c�lculos. Tambi�n podemos dar un nombre a una secuencia de instrucciones, e indicarle al ordenador que ejecute la secuencia cada vez que utilicemos su nombre. Es algo parecido a cuando le pedimos a alguien que baile de acuerdo a los pasos conocidos para ese tipo de baile, como la `Salsa <http://en.wikipedia.org/wiki/Salsa_(dance)>`_ o las Sevillanas. Una vez que conoces el baile puedes ejecutar sus pasos.

.. figure:: Figures/salsaDancer.jpg
    :height: 100px
    :align: center
    :alt: a women dancing Salsa
    :figclass: align-center

    Imagen 1: Una bailrina de Salsa.
    
En programaci�n existen dos t�rminos distintos para nombrar una secuencia de instrucciones: **procedimiento** y **funci�n**. Un **procedimiento** lleva a cabo una tarea para que suceda algo, pero no nos devuelve ning�n valor. Una **funci�n**, por el contrario, s� devuelve un resultado. En Python existen muchos procedimientos y funciones ya creados para que los usemos. La funci�n ``abs`` devuelve el valor absoluto del valor que le damos como dato de entrada a la funci�n. La funci�n ``int`` toma un n�mero decimal como entrada y devuelve su parte entera.

.. activecode:: Functions
  :tour_1: "Line by line tour"; 1: fun-line1; 2: fun-line2; 3: fun-line3; 4: fun-line4;

  print("Valor absoluto de -5:")
  print(abs(-5))
  print("Parte entera de 34.2")
  print(int(34.2))
  
.. mchoicemf:: 6_2_1_Functions_Q1
   :answer_a: -16
   :answer_b: -16.789
   :answer_c: 16.789
   :answer_d: 16
   :correct: d
   :feedback_a: La funci�n abs quitar� el signo negativo.
   :feedback_b: Se modificar� el n�mero original.
   :feedback_c: La funci�n int quitar� la parte decimal.
   :feedback_d: La funci�n abs convertir� el n�mero en positivo, y l funci�n int lo dejar� como 16.
   
   �Qu� crees que imprimir� la instrucci�n  `print(int(abs(-16.789)))`?

