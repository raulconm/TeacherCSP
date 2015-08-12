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
	
Hemos visto cómo podemos utilizar nombres para representar números (enteros como ``3`` y ``-325``, o decimales como ``2.4`` y ``-322.9392``), cadenas (como ``"Hola a todos"``), tortugas, e imágenes. Cuando hacemos cálculos utilizando los nombres, el ordenador buscará qué valor está asociado a cada nombre, y utilizará esos valores en los cálculos. También podemos dar un nombre a una secuencia de instrucciones, e indicarle al ordenador que ejecute la secuencia cada vez que utilicemos su nombre. Es algo parecido a cuando le pedimos a alguien que baile de acuerdo a los pasos conocidos para ese tipo de baile, como la `Salsa <http://en.wikipedia.org/wiki/Salsa_(dance)>`_ o las Sevillanas. Una vez que conoces el baile puedes ejecutar sus pasos.

.. figure:: Figures/salsaDancer.jpg
    :height: 100px
    :align: center
    :alt: a women dancing Salsa
    :figclass: align-center

    Imagen 1: Una bailrina de Salsa.
    
En programación existen dos términos distintos para nombrar una secuencia de instrucciones: **procedimiento** y **función**. Un **procedimiento** lleva a cabo una tarea para que suceda algo, pero no nos devuelve ningún valor. Una **función**, por el contrario, sí devuelve un resultado. En Python existen muchos procedimientos y funciones ya creados para que los usemos. La función ``abs`` devuelve el valor absoluto del valor que le damos como dato de entrada a la función. La función ``int`` toma un número decimal como entrada y devuelve su parte entera.

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
   :feedback_a: La función abs quitará el signo negativo.
   :feedback_b: Se modificará el número original.
   :feedback_c: La función int quitará la parte decimal.
   :feedback_d: La función abs convertirá el número en positivo, y l función int lo dejará como 16.
   
   ¿Qué crees que imprimirá la instrucción  `print(int(abs(-16.789)))`?

