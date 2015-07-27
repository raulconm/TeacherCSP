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
	:prefix: csp-3-4-

.. highlight:: java
   :linenothreshold: 4


Cómo se evalúan las expresiones
================================

El orden en que se ejecutan las expresiones es el mismo que en matemáticas, tal como se muestra en la siguiente tabla, de mayor a menor prioridad. Cuando dos símbolos tienen la misma prioridad se evalúan de izquierda a derecha.
   

+------------------------+----------------------------------------------------+
|Operador                | Nombre                                             |
+------------------------+----------------------------------------------------+
| -x                     | Negación                                           |
+------------------------+----------------------------------------------------+
| x * y, x / y, x % y    | Multiplicación, División, y Módulo                 |
+------------------------+----------------------------------------------------+
| x + y, x - y           | Suma y resta                                       |
+------------------------+----------------------------------------------------+

.. fillintheblank:: 3_4_1_Order1
   :correct: ^-2$
   :feedback1: ('.*','¿Has ejecutado ya el programa?')
   :blankid: order1Blank

   ¿Qué va a imprimir el siguiente programa cuando pulses el botón de ejecutar? :textfield:`order1Blank::small`

.. activecode:: Expression_Order1
    :tour_1: "Line-by-line Tour"; 1: ex1-line1; 2: ex1-line2; 
    :nocodelens:
    
    resultado = 4 + -2 * 3
    print(resultado)
   
Puedes cambiar el orden de ejecución de las expresiones añadiendo paréntesis para agruparlas.

.. fillintheblank:: 3_4_2_Order2
   :correct: ^6$
   :feedback1: ('.*','¿Has ejecutado el programa?')
   :blankid: order2Blank

   ¿Qué imprimirá el siguiente programa cuando pulses el botón de ejecutar? :textfield:`order2Blank::small`

.. activecode:: Expression_Order2
    :tour_1: "Line-by-line Tour"; 1: ex1-line1; 2: ex1-line2; 
    :nocodelens:
    
    resultado = (4 + -2) * 3
    print(resultado)

