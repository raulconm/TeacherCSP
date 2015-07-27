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
	:prefix: csp-3-3-

.. highlight:: java
   :linenothreshold: 4



Tipos generales de expresiones
==============================

+------------+--------------------------------------------------------------------------------------------+
| Expresión  | Significado aritmético                                                                     |
+------------+--------------------------------------------------------------------------------------------+
| 1 + 2      | Suma, el resultado es 3                                                                    |
+------------+--------------------------------------------------------------------------------------------+
| 3 * 4      | Multiplicación, el resultado es 12                                                         |
+------------+--------------------------------------------------------------------------------------------+
| 1 / 3      | División de enteros, es 0 en entorno clásicos de Python, pero aquí es 0.333333333333       |
+------------+--------------------------------------------------------------------------------------------+
| 2.0 / 4.0  | División, el resultado es 0.5, porque estás escribiendo números decimales                  |
+------------+--------------------------------------------------------------------------------------------+
| 2 % 3      | Módulo (resto), el resultado es 2                                                          |
+------------+--------------------------------------------------------------------------------------------+
| -1         | Negación, el resultado es -1                                                               |
+------------+--------------------------------------------------------------------------------------------+

.. mchoicemf:: 3_3_1_intDiv_Q1
   :answer_a: 0
   :answer_b: 1
   :answer_c: 0.75
   :answer_d: 0.25
   :correct: c
   :feedback_a: Si los dos valores son números enteros, en la mayoría de los entornos Python el resultado será también un entero. Pero, como en este libro traducimos Python a JavaScript, el resultado es un número decimal.
   :feedback_b: Sería cierto si el resultado se redondeara al alza antes de que la parte decimal se descartara, pero no sucede así.   
   :feedback_c: Aunque no es eso lo que harían la mayoría de entornos de programación en Python, en este libro traducimo de Python a Javascript, y por eso el resultado es un número decimal.
   :feedback_d: Sería cierto si el código fuera <code>1 / 4</code>, <code>1.0 / 4</code>, or <code>1 / 4.0</code>

   ¿Cuál es el resultado de ``3 / 4``?
    
.. mchoicemf:: 3_3_2_mod_Q1
   :answer_a: 0
   :answer_b: 1
   :answer_c: 2
   :answer_d: 3
   :correct: d
   :feedback_a: Sería cierto si fuera <code>18 % 2</code>, pero ¿cuál es el resto de dividir 18 entre 5? 
   :feedback_b: Sería verdadero si fuera <code>18 % 17</code>, puesto que 17 cabe una vez en 18 y el resto es 18 - 17 = 1.  
   :feedback_c: ¿Cuál es el mayor múltiplo de 5 que además es menor o igual a 18? El resto es 18 - ese número.
   :feedback_d: El resto es 3 porque 5 cabe tres veces en 18 (15) y 18 - 15 = 3.  

   ¿Cuál es el resultado de ``18 % 5``?
   
.. mchoicemf:: 3_3_3_mod_Q2
   :answer_a: 0
   :answer_b: 1
   :answer_c: 2
   :answer_d: 6
   :correct: c
   :feedback_a: Sería cierto si fuera <code>6 % 2</code>.  
   :feedback_b: Sería correcto fuera cualquier número impar dividido entre 2, pero no es así en este caso.
   :feedback_c: 6 cabe en 2 cero veces y sobran 2.  
   :feedback_d: Si tienes un número menor y lo divides por un número mayor, el resto siempre es el número menor. 

   ¿Cuál es el resultado de ``2 % 6``?

