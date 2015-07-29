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
	:prefix: csp-3-7-

.. highlight:: java
   :linenothreshold: 4

Consideraciones generales sobre las asignaciones
======================================================

Vamos a ver algunas generalidades sobre las asignaciones. Intenta trazar el siguiente ejemplo.

.. codelens:: Assign_Basic

   a = 1
   b = 12.3
   c = "Alfredo"
   d = b

.. mchoicemf:: 3_7_1_Assignment_Q1
   :answer_a: 1
   :answer_b: 12.3
   :answer_c: "b"
   :answer_d: "d"
   :correct: b
   :feedback_a: Para definir el valor de la variable b no se ha utilizado la variable a.
   :feedback_b: La variable d ha copiado su valor a partir del valor de la variable b.  La variable también b sigue conteniendo el valor 12.3.  
   :feedback_c: A la variable d se le ha asignado el valor que estaba almacenado en b. 
   :feedback_d: La variable d ha tomado el valor de la variable b.  

   ¿Cuál es el valor de la variable ``d`` una vez ejecutado el programa?

Es muy importante la *secuencia* de las instrucciones en un programa. Una asignación no crea una relación entre los nombres, como ocurre en matemáticas. La variable ``a`` puede ser igual a ``12`` en un momento, e igual a ``15`` en otro. Una instrucción de asignación es una acción que ocurre en un momento, y que puede cambiar después.    

.. codelens:: Assign_Multiple

	    var1 = 45
	    var1 = 17.3
	    var2 = var1

.. mchoicemf:: 3_7_2_Assignment_Multiple_Q1
		   :answer_a: var1 es 45, var2 es 45
		   :answer_b: var1 es 45, var2 es "var1"
		   :answer_c: var1 es 17.3, var2 es 45
		   :answer_d: var1 es 17.3, var2 es 17.3
		   :correct: d
		   :feedback_a: A la variable var1 se le ha asignado el valor 45, pero esto cambia en la línea 2, antes incluso de que var2 haya tenido ningún valor.
		   :feedback_b: Ambas variables contienen valores numéricos, porque así son los valores que existen en este programa.
		   :feedback_c: A la variable var2 nunca se le ha asignado el valor 45 en el programa.
		   :feedback_d: A la variable var1 se le asigna primero el valor 45, y a continuación se le asigna el valor 17.3, y finalmente, a la variable var2 se le asigna el valor contenido en var1.

		   ¿Cuáles son los valores de ``var1`` y ``var2`` una vez ejecutado este programa?

Podemos ver los valores (también los contenidos en las variables) imprimiéndolos. Es un método muy útil para saber qué está ocurriendo en el programa. Ejecuta este programa de ejemplo donde se calcula el número de días que hay en tres semanas: 

.. activecode:: Assign_Days
   :tour_1: "Line by line tour"; 1: calcDays-line1; 2: calcDays-line2; 3: calcDays-line3; 4: calcDays-line4; 5: calcDays-line5; 6: calcDays-line6;

   diasEnSemana = 7
   print(diasEnSemana)
   numeroDeDias = 7 * 3
   print(numeroDeDias)
   numeroDeDias2 = diasEnSemana * 3
   print(numeroDeDias2)

.. mchoicemf:: 3_7_3_Assign_Days_Q1
		   :answer_a: 7, 7*3, diasEnSemana*3
		   :answer_b: diasEnSemana, numeroDeDias, numeroDeDias2
		   :answer_c: 7, 21, 21
		   :answer_d: 7, 21, 3
		   :correct: c
		   :feedback_a: Se imprimen los números, una vez calculado su valor.
		   :feedback_b: No se imprimen nombres de variables.
		   :feedback_c: El primer print imprime el valor de diasEnSemana (7), el segundo imprime el valor de numeroDeDias (21), y el tercero imprime el valor de numeroDeDias2 (21).
		   :feedback_d: Para hacer el cálculo se utiliza el valor de diasEnSemana, y a continuación se asigna el resultado a numeroDeDias2.

		   ¿Cuáles son los tres valores que se imprimen al ejecutar este programa?
   
.. parsonsprob:: 3_7_4_Per_Person_Cost

   Este programa calcula el coste por persona de una cena, incluyendo la propina. Pero los bloques están mezclados. Arrástralos desde la parte izquierda y colócalos a la derecha en el orden correcto. Haz clic en <i>Check Me</> para comprobar la solución.</p>

   -----
   cuenta = 89.23
   =====
   propina = cuenta * 0.20
   =====
   total = cuenta + propina
   =====
   numeroDePersonas = 3
   costePorPersona = total / numeroDePersonas
   =====
   print(costePorPersona)



