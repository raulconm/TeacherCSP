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
	:prefix: csp-6-8-
	
.. highlight:: java
   :linenothreshold: 4

Renombrar las funciones de Python
=================================

Las funciones ``abs`` e ``int`` son *nombres*. Son los nombres de unas *variables* cuyos valores son el conjunto de instrucciones que sirven para un objetivo concreto. Más adelante sabremos lo suficiente sobre programación como para crear nuestras propias funciones ``abs`` e ``int``. Lo importante ahora es comprender que ``abs`` e ``int`` son los *nombres* con los que nos referimos a estas dos funciones. Puedes crear varios nombres diferentes que tengan el mismo valor. Como cuando una persona tiene un nombre y también un apodo. En el siguiente programa veremos que puedes incluso crear nombres nuevos para las funciones de Python. 

.. activecode:: Rename_Internal
  :tour_1: "Line-by-line tour"; 1: funName-line1; 2: funName-line2; 3: funName-line3; 4: funName-line4; 5: funName-line5; 6: funName-line6;

  absoluto = abs
  print("Valor absoluto de -5:")
  print(absoluto(-5))
  noDecimal = int
  print("Parte entera de 34.2")
  print(noDecimal(34.2))

.. mchoicemf:: 6_8_1_Rename_Internal_Q1
   :answer_a: -16
   :answer_b: -16.789
   :answer_c: 16.789
   :answer_d: 16
   :correct: d
   :feedback_a: No, absoluto cambiará el negativo
   :feedback_b: No, se cambiará el número original
   :feedback_c: No, noDecimal quitará a parte decimal
   :feedback_d: ¡Sí! absoluto lo hará positivo, y noDecimal descartará los valores después de la coma dejando solamente el 16.
   
   Si añades una línea más al programa anterior, `print(noDecimal(absoluto(-16.789)))`, qué imprimirá?
   

