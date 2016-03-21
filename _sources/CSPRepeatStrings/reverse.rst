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
    :alt: nota del profesor
    
.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. 	qnum::
	:start: 1
	:prefix: csp-9-2-
	
.. highlight:: java
   :linenothreshold: 4

Invertir un texto
=================

Ejecuta este otro programa, y observa cómo un cambio muy simple en el patrón proporciona un resultado muy distinto. En este caso vamos a combinar el dato *antes* en lugar de *después*, modificando por tanto solamente el paso 4 (cómo se acumulan los datos).  

.. activecode:: Copy_Reverse
    :tour_1: "Lines of code"; 2-3: strR2-line2-3; 5: strR2-line5; 7: strR2-line7; 9: strR2-line9; 10: strR2-line10; 12: strR2-line12; 13: strR2-line13; 14: strR2-line14; 15: strR2-line15;
	
    # PASO 1: INICIALIZAR LOS ACUMULADORES
    nuevaCadenaA = ""
    nuevaCadenaB = ""
    # PASO 2: OBTENER LOS DATOS
    frase = "Felicidades"
    # PASO 3: RECORRER LOS DATOS
    for letra in frase:
    	# PASO 4: ACUMULAR
      	nuevaCadenaA = letra + nuevaCadenaA
      	nuevaCadenaB = nuevaCadenaB + letra
    # PASO 5: PROCESAR EL RESULTADO
    print("Este es el resultado de usar letra + nuevaCadenaA:")
    print(nuevaCadenaA)
    print("Este es el resultado de usar nuevaCadenaB + letra:")
    print(nuevaCadenaB)

.. mchoicemf:: 9_2_1_Copy_Reverse_Q1
   :answer_a: Porque añadimos cada nueva letra al <i>principio</i> de <code>nuevaCadenaA</code>.
   :answer_b: Porque <code>nuevaCadenaA</code> añade los caracteres de izquierda a derecha.
   :answer_c: Porque llamamos a una función que invierte.
   :answer_d: Porque el bucle <code>for</code> la está invirtiendo.
   :correct: a
   :feedback_a: Cada letra nueva se va añadiendo al final, creándose una cadena invertida.
   :feedback_b: ¿Y cómo se invertiría la otra cadena?
   :feedback_c: En este programa no hay ninguna función que invierta.
   :feedback_d: El mismo bucle <code>for</code> está creando una copia ordenada de la cadena y una copia invertida. El bucle <code>for</code> es el mismo en ambos casos.

   ¿Por qué crees que ``nuevaCadenaA`` contiene todas las letras, pero en orden inverso?
