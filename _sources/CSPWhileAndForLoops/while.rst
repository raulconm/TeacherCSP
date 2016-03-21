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
	:prefix: csp-8-3-
	
.. highlight:: java
   :linenothreshold: 4


No sabemos cuándo terminará el bucle 
====================================

¿Cómo podemos decirle al ordenador que haga algo solamente hasta que ocurra algo que queremos que suceda? Tenemos que construir los programas de forma que todas las partes juntas hagan que una expresión sea cierta *hasta* que queramos que sea falsa. 

Imaginemos que queremos encontrar la raiz cuadrada de un número. En algunos casos, el resultado no va a ser exacto. Digamos que vamos a buscar un número que, al multiplicarlo por sí mismo, está a menos de `0.01`del número cuya raiz cuadrada buscamos. ¿Cómo vamos a hacer esto? Podemos aplicar un método clásico para hacerlo. 

1. Comencemos tomando el número `2`.
2. Elevémosolo al cuadrado.
3. ¿El resultado está cerca del número buscado? Si está a menos de `0.01``, hemos terminado. Si nos hemos pasado tomaremos el valor absoluto de la diferencia. La función Python para obtener el valor absoluto es ``abs``.
4. Si no estamos lo suficientemente cerca del número buscado, dividimos el número buscado entre nuestro número, y hacemos la media con nuestro número.
5. El resultado es nuestro nuevo número. Lo elevamos al cuadrado y volvemos al paso #3.

A continuación se muestra el programa para seguir exactamente estos pasos. Pruébalo con diferentes números, y comprueba si este método para hallar la raiz cuadrada de un número es suficientemente preciso.

.. activecode:: Square_Root
  :tour_1: "Line by line tour"; 1: sqR_line1; 2: sqR_line2; 3: sqR_line3; 4: sqR_line4; 5: sqR_line5; 6: sqR_line6; 7: sqR_line7; 8: sqR_line8;

  buscado = 6
  estimado = 2
  estimadoAlCuadrado = estimado * estimado
  while abs(buscado-estimadoAlCuadrado) > 0.01:
      acercar = buscado / estimado
      estimado = (estimado + acercar) / 2.0
      estimadoAlCuadrado = estimado * estimado
  print("La raiz cuadrada de ", buscado," es ", estimado)

.. mchoicemf:: 8_3_1_Square_Root_Q1
  :answer_a: No hay error, ya que lo calculamos dentro del bucle.
  :answer_b: Nos daría un error.
  :answer_c: Necesitamos calcularlo antes de comenzar el bucle, pero no necesitamos calcularlo de nuevo dentro.
  :correct: b
  :feedback_a: Tenemos que calcularlo antes, si no abs(buscado-estimadoAlCuadrado) > 0.01 nos dará un error.
  :feedback_b: Es obligatorio declarar (crear) una variable antes de utilizarla.
  :feedback_c: Ambos son necesarios. El primero permite hacer la comprobación. El que está dentro del bucle sirve para actualizar estimadoAlCuadrado.

   ¿Qué pasa si no calculamos ``estimadoAlCuadrado`` antes del bucle ``while``?

Supongamos que queremos calcular la raiz cuadrada de 6. ¿Cuántas veces se ejecutará el cuerpo del bucle ``while``? Podemos averiguarlo trazando el programa.  

.. video:: trace-squareroot
   :controls:
   :thumb: ../_static/squareRootTrace.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/square-root-trace.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/square-root-trace.webm

.. mchoicemf:: 8_3_2_Count_Loops_Q1
  :answer_a: Solamente una.
  :answer_b: Dos veces.
  :answer_c: Tres veces.
  :answer_d: Cuatro veces.
  :correct: c
  :feedback_a: En la primera ejecución del bucle el número estimado será 2, y 2 * 2 es 4, que no es igual a 6.
  :feedback_b: En la segunda ejecución del bucle el estimado es 2.5 (la media de 3 y de 2). Pero 2.5 * 2.5 no está aún a menos de 0.01 de 6.
  :feedback_c: En la tercera ejecución del bucle el estimado es 2.45, que es un resultado suficientemente bueno para la raiz cuadrada de 6.
  :feedback_d: No habrá una cuarta vez. Estimado será 2, luego 2.5, y finalmente 2.45, y entonces el programa parará.

   ¿Cuántas veces se ejecutará el cuerpo del bucle cuando ``buscado = 6``? (en el vídeo)

Y si buscamos la raiz de 25? ¿Y de 2356? Es complicado saber de antemano cuántas veces se va a ejecutar el bucle. Es en estos casos en los que necesitamos el bucle ``while``, cuando podemos especificar cuál es la condición para que termine ( o para que *continúe*).
