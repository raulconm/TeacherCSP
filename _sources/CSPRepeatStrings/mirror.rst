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
    
.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. 	qnum::
	:start: 1
	:prefix: csp-9-3-
	
.. highlight:: java
   :linenothreshold: 4

Texto reflejado
===============

�Qu� ocurrir� si a�adimos la letra a *ambos* lados de la cadena nueva?

.. activecode:: Copy_Mirror
    :tour_1: "Lines of code"; 2: strR3-line1; 4: strR3-line2; 6: strR3-line3; 8: strR3-line4; 10: strR3-line5;
	
    # PASO 1: INICIALIZAR EL ACUMULADOR 
    nuevaCadena = ""
    # PASO 2: OBTENER LOS DATOS
    frase = "Esto es una prueba"
    # PASO 3: RECORRER LOS DATOS
    for letra in frase:
      	# PASO 4: ACUMULAR
      	nuevaCadena = letra + nuevaCadena + letra
    # PASO 5: PROCESAR EL RESULTADO
    print(nuevaCadena)

Prueba con otra frase y mir� qu� efectos puede tener.

.. mchoicemf:: 9_3_1_Copy_Mirror_Q1
   :answer_a: Escribe la frase <code>"Esta es una frase invertida*"</code>
   :answer_b: Modifica <code>nuevaCadena</code> en la l�nea 1 para que sea <code>"*"</code> en lugar de <cod>""</code>
   :answer_c: Cambia el lado derecho de la l�nea 4 por <code>letra + "*" + nuevaCadena + letra</code>
   :answer_d: Cambia el lado derecho de la l�nea 4 por <code>letra + nuevaCadena + "*" + letra</code>
   :correct: b
   :feedback_a: Eso nos dar�a como resultado <code>*aditrevni esarf anu se atsEEsta es una frase invertida*</code>.
   :feedback_b: Tambi�n puede inicializarse el acumulador con un contenido (*).
   :feedback_c: Eso nos dar�a <code>a*d*i*t*r*e*v*n*i* *e*s*a*r*f* *a*n*u* *s*e* *a*t*s*E*Esta es una frase invertida</code> -- con asteriscos entre cada letra en la mitad izquierda de la cadena reflejada.
   :feedback_d: Eso nos dar�a <code>aditrevni esarf anu se atsE*E*s*t*a* *e*s* *u*n*a* *f*r*a*s*e* *i*n*v*e*r*t*i*d*a</code> -- con asteriscos entre cada letra en la mitad derecha de la cadena reflejada.

   Modifica el programa para crear un reflejo de la frase ``"Esta es una frase invertida."`` con un asterisco en el medio, de tal forma que el resultado sea ``aditrevni esarf anu se atsE*Esta es una frase invertida``. �C�mo crees que puedes hacer eso? 

El acumulador no tiene por qu� ser inicialmente una cadena vac�a. Podemos darle un valor inicial y dicho valor aparecer� entonces en el centro de la frase reflejada. 

.. codelens:: Char_In_Middle

    nuevaCadena = "."
    frase = "Vamos a ver a un mago."
    for letra in frase:
        nuevaCadena = letra + nuevaCadena + letra
    print(nuevaCadena)

.. mchoicemf:: 9_3_2_Count_Exclamations_Q1
   :answer_a: Uno
   :answer_b: Dos
   :answer_c: Tres
   :answer_d: Cuatro
   :correct: a
   :feedback_a: S�lo est� el que tiene el acumulador como valor inicial.
   :feedback_b: Ser�a correcto, al final del programa, si solamente hubi�ramos reflejado la frase. Pero hemos definido un valor inicial para el acumulador.
   :feedback_c: Eso es cierto al terminar el programa, pero no cuando la variable letra contiene la ``m`` de <code>"mago"</code>
   :feedback_d: Como mucho, en <code>nuevaCadena</code> puede haber tres.

   Cuando la variable ``letra`` contiene la ``m`` de ``mago``, �Cu�ntos signos ``.`` hay en ``nuevaCadena``? 

.. parsonsprob:: 9_3_3_Palindrome

   <p>La frase <code>"D�bale arroz a la zorra el abad"</code> es un <b>pal�ndromo</b>. Tiene las mismas letras ley�ndose al derecho o al rev�s. El siguiente programa genera la cadena <code>"daba le arroz al a zorra el abaD<=>Dabale arroz a la zorra el abad"</code>. Ordena las l�neas con la indentaci�n apropiada.</p>
   -----
   nuevaCdn = "<=>"
   frase = "Dabale arroz a la zorra el abad"
   =====
   for letra in frase:
   =====
       nuevaCdn = letra + nuevaCdn + letra
   =====
   print(nuevaCdn)
