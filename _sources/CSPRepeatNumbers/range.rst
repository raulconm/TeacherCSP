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
	:prefix: csp-7-4-
	
.. highlight:: java
   :linenothreshold: 4

La función Range
====================

Esa larga lista de valores de la variable ``numeros`` (``numeros = [1,2,3,4,5,6,7,8,9,10]``), se puede generar también usando la función ``range``. Esta función puede tomar dos valores de ``entrada``. El primero es el valor inicial de la lista, y el segundo es el valor final, **PERO**, este último no está incluido en el rango. Si pasamos solamente un valor como entrada a la función ``range``, nos devolverá una lista cuyo valor inicial es cero.  

.. activecode:: Numbers_Range
	
    print range(10)
    print range(1,10)
    print range(11)
    print range(1,11)

.. mchoicemf:: 7_4_1_Numbers_Range_Q1
   :answer_a: print range(10)
   :answer_b: print range(1,10)
   :answer_c: print range(11)
   :answer_d: print range(1,11)
   :correct: d
   :feedback_a: Esto incluye el cero y no incluye el diez: [0,1,2,3,4,5,6,7,8,9]
   :feedback_b: Esto no incluye el diez: [1,2,3,4,5,6,7,8,9]
   :feedback_c: Esto incluyo el cero: [0,1,2,3,4,5,6,7,8,9,10]
   :feedback_d: Esto devuelve [1,2,3,4,5,6,7,8,9,10]

   ¿Cuál de las líneas siguientes nos da los números que necesitamos para calcular el producto de todos los números del 1 al 10? 
   
Reescribamos el programa que calcula el producto utilizando esta vez la función ``range`` para generar la lista de números, como se muestra a continuación.

.. activecode:: Numbers_Product2
    :tour_1: "Line by line tour"; 1: for2_line1; 2: for2_line2; 3: for2_line3; 4: for2_line4; 5: for2_line5;
	
    producto = 1  # El valor inicial es 1
    numeros = range(1,11)
    for numero in numeros:
    	producto = producto * numero
    print(producto)

.. mchoicemf:: 7_4_2_Numbers_Product_Q3
   :answer_a: 121645100408832000
   :answer_b: 3628800
   :answer_c: 362880
   :answer_d: 2432902008176640000
   :correct: d
   :feedback_a: Ese es el producto de todos los números del 1 al 19 (es decir, has cambiado el 11 por un 20)
   :feedback_b: Ese es el producto de todos los números del 1 al 10 (es decir, n hay cambios)
   :feedback_c: Ese es el producto de todos los números del 1 al 9 (has cambiado el 11 por un 10)
   :feedback_d: Ese es el producto de todos los números del 1 al 20 (es decir, has cambiado el 11 por un 21)

   Modifica solamente UN número en el programa anterior para que calcule el producto de todos los números del 1 al 20.



