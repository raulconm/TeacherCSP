..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |teachernote| image:: Figures/apple.jpg
    :width: 30px
    :align: top
    :alt: teacher note
    
.. |bigteachernote| image:: Figures/apple.jpg
    :width: 50px
    :align: top
    :alt: teacher note

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |codelensfirst| image:: Figures/codelens-first.png
    :height: 20px
    :align: top
    :alt: move to first button

.. |codelensback| image:: Figures/codelens-back.png
    :height: 20px
    :align: top
    :alt: back button

.. |codelensfwd| image:: Figures/codelens-forward.png
    :height: 20px
    :align: top
    :alt: forward (next) button

.. |codelenslast| image:: Figures/codelens-last.png
    :height: 20px
    :align: top
    :alt: move to last button
    
.. 	qnum::
	:start: 1
	:prefix: csp-3-2-

.. highlight:: java
   :linenothreshold: 4



Expresiones
=============

..	index::
	single: expressions
	single: arithmetic expressions

Lo que hay *a la derecha* del igual en una asignación no tiene por qué ser obligatoriamente un valor. También puede ser una *expresión aritmética*, como ``2*2``. En ese caso se evaluará la expresión y el resultado se almacenará en la variable.  

.. fillintheblank:: 3_2_1_Mult
   :correct: ^4$
   :feedback1: ('.*','¿Has ejecutado el programa?')
   :blankid: multBlank

   ¿Qué imprimirá el programa cuando pulses el botón para ejecutar el siguiente código? :textfield:`multBlank::small`

.. activecode:: Expression_Mult
    :tour_1: "Line-by-line Tour"; 1: ex1-line1; 2: ex1-line2; 
    :nocodelens:
    
    result = 2 * 2
    print(result)
    
|bigteachernote| Nota para el profesor: Dislexia en las asignaciones
--------------------------------------------------------------

..	index::
	single: assignment dyslexia

Algunos estudiantes escribirán la expresión en el lado izquiero de ``=`` y el nombre de la variable en el lado derecho (``2 * 2 = a``). Esto se llama dislexia en la asignación, y originará un error. El nombre de la variable *siempre* debe ir a la izquierda del ``=`` en una asignación. 

División de números enteros
---------------------------

..	index::
	single: integer division
   
Puedes utilizar cualquiera de los símbolos matemáticos habituales. 

.. fillintheblank:: 3_2_2_Div
   :correct: ^0.333333333333$
   :feedback1: ('.*','¿Has ejecutado el programa?')
   :blankid: divBlank

   ¿Qué se va a mostrar cuando pulses el botón de ejecutar en el siguiente código? :textfield:`divBlank::medium`
   
.. activecode:: Expression_Div
    :tour_1: "Line-by-line Tour"; 1: ex2-line1; 2: ex1-line2; 
    :nocodelens:
    
    result = 1 / 3
    print(result)

.. note::
   En este libro se utiliza Python 3.0, y el resultado de un cálculo entre enteros como ``1 / 3`` devuelve un valor decimal. Si hubiéramos ejecutado ``1 / 3`` en una versión más antigua de Python el resultado hubiera sido ``0``. En muchos lenguajes, si en los cálculos estás utilizando solamente números enteros (como -3, 65, -39028, 602939) el resultado será también un entero, y se ignorará la parte decimal, la que aparecería detrás del punto (en los lenguajes de programación la coma decimal se representa como un punto). En esos entornos de programación más antiguos es fudamental expresar valores decimales en las operaciones (como ``1.0 / 2``, ``1 / 2.0``, o ``1.0 / 2.0``) si quieres que el resultado sea decimal.  
   
Módulo 
---------

..	index::
	single: modulo
	single: remainder
   
También se pueden utilizar algunos otros símbolos de formas que no te esperas.  

.. fillintheblank:: 3_2_3_Mod
   :correct: ^0$
   :feedback1: ('.*','¿Has ejecutado ya el programa?')
   :blankid: modBlank

   ¿Qué valor se mostrará cuando pulses el botón de ejecutar en el siguiente código? :textfield:`modBlank::small`
   
.. activecode:: Expression_Mod
    :tour_1: "Line-by-line Tour"; 1: ex3-line1; 2: ex1-line2; 
    :nocodelens:
    
    result = 4 % 2
    print(result)

Es posible que no estés familiarizado con el operador **módulo** (resto) ``%``. Este operador devuelve el resto de dividir el primer número entre el segundo. Muy probablemente hiciste esto hace mucho tiempo, cuando estabas aprendiendo a dividir. En el caso de ``4 % 2``, ``2`` "cabe" dos veces dentro de ``4`` y no sobra nada, luego el resto es ``0``. El resultado de ``5 % 2`` sería ``1``, porque ``2`` cabe dos veces dentro de ``5`` y el resto es ``1``. En la práctica, por ejemplo, si el resultado de ``X % 2`` es igual a ``1`` significa que ``X`` es impar, y si el resultado es ``0`` significará que ``X`` es par. 

.. figure:: Figures/mod-py.png
    :width: 150px
    :align: center
    :figclass: align-center
    
    Imagen 3: Desarrollo de una división donde se muestra el resultado y el resto.
    
.. note::
   El resultado de ``x % y`` cuando ``x`` es más pequeño que ``y`` es siempre ``x``. El valor de ``y`` no caben en ``x``, puesto que ``x`` es más pequeño que ``y``, luego el resultado es simplemente ``x``. Así pues, el resultado de ``2 % 3`` es ``2``. Puedes comprobarlo por ti mismo modificando el código anterior. 

