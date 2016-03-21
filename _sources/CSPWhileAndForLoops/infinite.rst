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
	:prefix: csp-8-1-
	
.. highlight:: java
   :linenothreshold: 4
   
	
Bucles - While y For
=======================

*Objetivos de aprendizaje:*

- Introducir el concepto de *bucle infinito*
- Utilizar un bucle ``while`` para repetir código
- Comparar y diferenciar un bucle ``while`` y un bucle  ``for``

..	index:
	single: while
	single: variable
	single: variable índice
	single: bucle infinito
	pair: instrucciones; while
	pair: instrucciones; for

Bucles infinitos
================

Hacer que un ordenador repita pasos es sencillo. Decirle que pare es un poco más complicado. Una forma simple de decirle que repita pasos es usando un bucle ``while``. Un bucle ``while`` consiste en una expresión lógica seguida de un bloque de instrucciones. Este bloque de instrucciones se ejecutarán repetidamente **MIENTRAS LA EXPRESIÓN LÓGICA SEA CIERTA**.

..	index::
	single: bucle infinito
	pair: bucle; infinito
	
Entonces, veamos un programa que se ejecuta para siempre. 

.. sourcecode:: python

  	while 1 == 1:
  	    print("Bucle")
  	    print("Infinito")

Como ``1`` siempre será igual a ``1`` las dos instrucciones ``print`` se ejecutarán hasta el infinito. A esto le llamamos **bucle infinito**, que significa que el bucle se ejecutará sin fin, o hasta que lo interrumpamos. Ejecuta esto en un ordenador que puedas apagar sin problemas: 

.. sourcecode:: python

 	>>> while 1==1:
 	        print ("Bucle")
 	        print ("Infinito")
	Bucle
	Infinito
	Bucle
	Infinito
	Bucle
	Infinito
	Bucle
	Infinito

(Cuando llegues a este punto apaga el ordenador...)

