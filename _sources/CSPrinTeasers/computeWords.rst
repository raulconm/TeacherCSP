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


Computaci�n con palabras
========================

..	index::
	single: string
	pair: programming; string

Los ordenadores pueden tambi�n trabajar con palabras, o dicho de una forma m�s precisa, con **cadenas** formadas por una sucesi�n de caracteres. Se le llama **cadena** a cualquier cosa que se puede escribir entre comillas dobles (``"Hola"``) o sencillas (``'Hola'``). Se pueden "hacer c�lculos" con palabras utilizando alguno de los operadores artim�ticos b�sicos -- aqu� tienen una funci�n diferente. Probemos a generar algunas letras tontas para una canci�n usando ``+`` para combinar (sumar) dos cadenas, y ``*`` para repetirlas.

Debajo del siguiente programa, a la derecha del bot�n *Run* |runbutton|, ver�s un bot�n que abre la gu�a de sonido para este programa: |audiobutton|. Haz clic en ese bot�n y despu�s pulsa sobre "Guiar l�nea por l�nea" para oir la gu�a de sonido. Puedes utilizar los bot�nes para detener, reproducir, saltar hacia adelante o hacia atr�s.

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

Tambi�n se puede generar una nueva cadena en la que cambiemos alguna cosa respecto de una cadena original. En el siguiente ejemplo, tomamos una cadena en may�suculas y la convertimos a min�suculas. Este ejemplo utiliza una **notaci�n con punto** (``sentence.lower()``), que es la forma de decirle a la cadena en qu� queremos que cambie. 

.. activecode:: String_Methods
   :tour_1: "Line-by-line Tour"; 1: str2-line1; 2: str2-line2; 3: str2-line3; 4: str2-line4; 5: str2-line5;
   :nocodelens:
   
   frase = "ESTO ES UNA PRUEBA"
   mejor = frase.lower()
   print(mejor)
   mejortodavia = mejor.capitalize() + "."
   print(mejortodavia)
   
.. mchoicemf:: 1_3_1_String_Methods_Q1
   :answer_a: Buenos d�as
   :answer_b: Buenosd�as
   :answer_c: Buenos d�as Buenos d�as
   :answer_d: Buenosd�asBuenosd�as
   :answer_e: Buenosd�as2
   :correct: d
   :feedback_a: Cuando sumas cadenas est�s copiando la segunda justo a continuaci�n de la primera, sin a�adir espacios
   :feedback_b: Recuerda que * 2 repite dos veces la misma cadena
   :feedback_c: Sumar cadenas y repetirlas no a�ade espacios entre ellas
   :feedback_d: Las cadenas se suman sin que se a�adan espacios, y se repiten sin agregar tampoco ning�n espacio
   :feedback_e: * 2 repite la cadena dos veces
   
   �Qu� imprimir� este c�digo?
   
   :: 
   
      primero = "Buenos"
      segundo = "d�as"
      print ((primero + segundo) * 2)

