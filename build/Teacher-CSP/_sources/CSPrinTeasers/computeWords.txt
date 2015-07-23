..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

..  shortname:: Chapter: What You Can Do with a Computer
..  description:: Some tidbits of what you can do with a computer

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-1-3-


.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |teachernote| image:: Figures/apple.jpg
    :width: 26px
    :align: bottom
    :alt: teacher note


Computación con palabras
========================

..	index::
	single: string
	pair: programming; string

Los ordenadores pueden también trabajar con palabras, o dicho de una forma más precisa, con **cadenas** formadas por una sucesión de caracteres. Se le llama **cadena** a cualquier cosa que se puede escribir entre comillas dobles (``"Hola"``) o sencillas (``'Hola'``). Se pueden "hacer cálculos" con palabras utilizando alguno de los operadores artiméticos básicos -- aquí tienen una función diferente. Probemos a generar algunas letras tontas para una canción usando ``+`` para combinar (sumar) dos cadenas, y ``*`` para repetirlas.

Debajo del siguiente programa, a la derecha del botón *Run* |runbutton|, verás un botón que abre la guía de sonido para este programa: |audiobutton|. Haz clic en ese botón y después pulsa sobre "Guiar línea por línea" para oir la guía de sonido. Puedes utilizar los botónes para detener, reproducir, saltar hacia adelante o hacia atrás.

.. activecode:: String_Operators
  :tour_1: "Line-by-line Tour"; 1: str1-line1; 2: str1-line2; 3: str1-line3; 4: str1-line4; 5: str1-line5; 6: str1-line6; 7: str1-line7; 8: str1-line8; 9: str1-line9; 10: str1-line10;
  :nocodelens:
  
  basico = "Ma"
  print(basico)
  basico3 = basico + basico + basico
  print(basico3)
  siguiente = "Mu"
  siguiente3 = siguiente * 3
  print(siguiente3)
  juntos = (basico * 3) + (siguiente * 2)
  print(juntos)
  print(juntos + "Mmm" + juntos)
  
..	index::
	single: dot-notation
	pair: programming; dot-notation

También se puede generar una nueva cadena en la que cambiemos alguna cosa respecto de una cadena original. En el siguiente ejemplo, tomamos una cadena en mayúsuculas y la convertimos a minúsuculas. Este ejemplo utiliza una **notación con punto** (``sentence.lower()``), que es la forma de decirle a la cadena en qué queremos que cambie. 

.. activecode:: String_Methods
   :tour_1: "Line-by-line Tour"; 1: str2-line1; 2: str2-line2; 3: str2-line3; 4: str2-line4; 5: str2-line5;
   :nocodelens:
   
   frase = "ESTO ES UNA PRUEBA"
   mejor = frase.lower()
   print(mejor)
   mejortodavia = mejor.capitalize() + "."
   print(mejortodavia)
   
.. mchoicemf:: 1_3_1_String_Methods_Q1
   :answer_a: Buenos días
   :answer_b: Buenosdías
   :answer_c: Buenos días Buenos días
   :answer_d: BuenosdíasBuenosdías
   :answer_e: Buenosdías2
   :correct: d
   :feedback_a: Cuando sumas cadenas estás copiando la segunda justo a continuación de la primera, sin añadir espacios
   :feedback_b: Recuerda que * 2 repite dos veces la misma cadena
   :feedback_c: Sumar cadenas y repetirlas no añade espacios entre ellas
   :feedback_d: Las cadenas se suman sin que se añadan espacios, y se repiten sin agregar tampoco ningún espacio
   :feedback_e: * 2 repite la cadena dos veces
   
   ¿Qué imprimirá este código?
   
   :: 
   
      primero = "Buenos"
      segundo = "días"
      print ((primero + segundo) * 2)

