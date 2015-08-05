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
	:prefix: csp-3-9-

.. highlight:: java
   :linenothreshold: 4

Calcular una factura
====================

Podemos utilizar variables para resolver problemas como los que habitualmente resolvemos utilizando una hoja de cáculo. Imagina que tienes una hoja de cálculo con una factura del material de oficina para una empresa. 

.. figure:: Figures/invoice.png
    :width: 600px
    :align: center
    :alt: a spreadsheet
    :figclass: align-center
    
    Imagen 3: Una hoja de cálculo con información de una factura

A continuación se muestra un programa que calcula el precio total de la factura. Haz clic en el botón  |audiobutton| para entender todo lo que ocurre en el programa.

.. activecode:: Invoice1
    :tour_1: "Line by line tour"; 1: inv-line1; 2: inv-line2; 3: inv-line3; 4: inv-line4; 5: inv-line5; 6: inv-line6; 7: inv-line7; 8: inv-line8; 

    cantidad1 = 2
    precioUnitario1 = 2.90
    total1 = cantidad1 * precioUnitario1
    cantidad2 = 4
    precioUnitario2 = 4.30
    total2 = cantidad2 * precioUnitario2
    totalFactura = total1 + total2
    print(totalFactura)

.. mchoicemf:: 3_9_1_Invoice1_Q1
		   :answer_a: 7
		   :answer_b: 6
		   :answer_c: 5
		   :answer_d: 2
		   :correct: a
		   :feedback_a: Así es, cantidad1, precioUnitario1, total1, cantidad2, precioUnitario2, total2, totalFactura.
		   :feedback_b: Hay tres variables por línea, dos líneas, y un total.
		   :feedback_c: Hay tres variables por línea, dos líneas, y un total.
		   :feedback_d: Hay tres variables por línea, dos líneas, y un total.

		   ¿Cuántas variables hay en este programa?

En realidad no necesitamos crear nuevas variables ``cantidad2`` y ``precioUnitario2``. Sólo las empleamos para calcular el total de cada línea, y por lo tanto podríamos reutilizar las anteriores.

.. codelens:: Invoice2

  cantidad = 2
  precioUnitario = 2.90
  total1 = cantidad * precioUnitario
  cantidad = 4
  precioUnitario = 4.30
  total2 = cantidad * precioUnitario
  totalFactura = total1 + total2
  print(totalFactura)

.. mchoicemf:: 3_9_2_Invoice2_Q1
		   :answer_a: 7
		   :answer_b: 6
		   :answer_c: 5
		   :answer_d: 2
		   :correct: c
		   :feedback_a: En este caso tenemos dos variables menos.
		   :feedback_b: Tenemos un total por cada línea (dos), una cantidad, un precioUnitario, y un totalFactura.
		   :feedback_c: Las variables son cantidad, precioUnitario, total1, total2, y totalFactura. 
		   :feedback_d: En este caso tenemos un total para cada línea (dos), una cantidad, un precioUnitario, y un totalFactura.

		   ¿Cuántas variables hay en este programa?
		   
.. Note::
   Es muy conveniente utilizar nombres de variables que tengan sentido, como ``totalFactura`` y ``cantidad``, en lugar de otros que no signifiquen nada, como ``estaVariableEsMiAmiga``, o ``Juan``. El nombre debe ayudarnos a identificar qué dato está representando la variable.   

Imagina que las manzanas cuestan 0.30 euros por pieza, y que las peras cuestan 0.50 euros por pieza. Modifica el siguiente programa para que calcule el coste total.

.. activecode:: Complete_Assignment

   manzanas = 4
   peras = 3
   precioTotal =
   print(precioTotal)

Si lo prefieres, puedes probar con las siguientes respuestas, copiándolas y pegándolas dentro del programa,antes de responder a la pregunta: 

.. mchoicemf:: 3_9_3_Make_An_Assignment_Q1
  :answer_a: precioTotal = manzanas + peras
  :answer_b: precioTotal = (0.30 * manzanas) + (0.50 * peras)
  :answer_c: precioTotal = (0.30 * peras) + (0.50 * manzanas)
  :answer_d: precioTotal = (0.30 + apples) * (0.50 + peras)
  :correct: b
  :feedback_a: No se está considerando el precio de las manzanas ni de las peras.
  :feedback_b: Necesitamos multiplicar el precio de una manzana por el número de manzanas, y sumarle el precio de una pera por el número de peras.
  :feedback_c: Esta fórmula tiene los precios al revés.
  :feedback_d: Está fórmula para hallar el precio total es erronea.

   ¿Cuál de estas líneas de código calculará correctamente el valor de ``precioTotal`` si la colocamos en la línea 3 del programa?


