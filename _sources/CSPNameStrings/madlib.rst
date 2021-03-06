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

.. 	qnum::
	:start: 1
	:prefix: csp-4-2-

Historias al azar
==================

Tal vez cuando eras peque�o jugabas con tus amigos o amigas a construir historias al azar. Tom�bais algunos datos, como el nombre de un amigo, un verbo, y un juego favorito (por ejemplo), y los a�ad�ais dentro de una historia que otro u otra hab�a inventado. Como no conoc�ais la historia de antemano, os sorprend�ais al saber qu� le suced�a en ella a vuestro amigo o amiga.

.. activecode:: Story1
   :tour_1: "Line by line tour"; 1: StEx-line1; 2: StEx-line2; 3: StEx-line3; 4: StEx-line4; 5: StEx-line5; 6: StEx-line6; 7: StEx-line7; 8: StEx-line8; 9: StEx-line9; 10: StEx-line10; 11: StEx-line11; 12: StEx-line12; 13: StEx-line13; 14: StEx-line14; 15: StEx-line15;
   :tour_2: "Structural tour"; 1-5: StEx-line1-5; 6-10: StEx-line6-10; 11-15: StEx-line11-15;

   nombre = "Patricia"
   apellido = "Sanchez"
   genero = "una chica"
   direccion = " la Plaza del Ayuntamiento numero 2"
   verbo = "comer"
   comienzo = "Erase una vez  " + genero + " que se llamaba " + nombre + "."
   siguiente1 = nombre + " vivia en " + direccion + "."
   siguiente2 = "Un dia, una bruja se acerco a casa de la familia " + apellido + "."
   siguiente3 = "La malvada bruja se queria " + verbo + " a " + nombre + "."
   final = "Pero " + nombre + " se dio cuenta de sus intenciones y se libro de ella."
   print(comienzo)
   print(siguiente1)
   print(siguiente2)
   print (siguiente3)
   print(final)


.. mchoicemf:: 4_2_1_Story1_Q1
   :answer_a: finalReal = nombre + " llamo a la policia y la detuvieron."
   :answer_b: print(nombre + " llamo a la policia y la detuvieron.")
   :answer_c: print("Patricia llamo a la policia y la detuvieron.")
   :correct: b
   :feedback_a: Esta opci�n s�lo ser�a correcta si a�adieras la instrucci�n <code>print(finalReal)</code> a continuaci�n.
   :feedback_b: Esta es la forma adecuada porque la l�nea que se imprime incluye el nombre correcto. Tambi�n puedes construir primero una cadena llamada <code>finalReal</code>, y despu�s imprimirla.
   :feedback_c: Esto <i>podr�a</i> servir.  Pero si cambias el contenido de la variable <code>nombre</code> �ste no  cambiar�a al imprimir la historia.  Prueba con una opci�n m�s adecuada.

   Imagina que quieres ampliar la historia para que diga algo as�: "Patricia llam� a la polic�a y la detuvieron." �Cu�l de las siguientes l�neas debes a�adir para que eso ocurra? (Pista: �Es una buena opci�n *probar* con cada una de ellas!)


**Qu� hacer a continuaci�n:** Ejecuta este programa para comprobar qu� texto genera, y modifica el contenido de las variables para construir diferentes historias. Prueba con otros nombres, o con verbos distintos. 


.. activecode:: Story2
   :tour_1: "Line by line tour"; 1: story-line1; 2: story-line2; 3: story-line3; 4: story-line4; 5: story-line5; 6: story-line6; 7: story-line7; 8: story-line8; 9: story-line9; 10: story-line10; 11: story-line11; 12: story-line12; 13: story-line13; 14: story-line14; 15: story-line15; 

   nombre = "Sofia"
   apellido = "Diaz"
   genero = "una chica"
   direccion = " la Avenida de la Paz numero 8"
   verbo = "cocinar"
   comienzo = "Erase una vez  " + genero + " que se llamaba " + nombre + "."
   siguiente1 = nombre + " vivia en " + direccion + "."
   siguiente2 = "Un dia, una bruja se acerco a casa de la familia " + apellido + "."
   siguiente3 = "La malvada bruja se queria " + verbo + " a " + nombre + "."
   final = "Pero " + nombre + " se dio cuenta de sus intenciones y se libro de ella."
   print(comienzo)
   print(siguiente1)
   print(siguiente2)
   print (siguiente3)
   print(final)

   
.. mchoicemf:: 4_2_2_Story2_Q1
   :answer_a: S�
   :answer_b: No
   :correct: a
   :feedback_a: La �nica diferencia es el orden de las l�neas en el c�digo, pero la historia se imprime igual.
   :feedback_b: �Lo has ejecutado? Copia el c�digo en el recuadro del programa y ejec�talo.
 
   �Imprimir� el siguiente c�digo la historia igual que antes? 
   
   :: 

     nombre = "Sofia"
     apellido = "Diaz"
     genero = "una chica"
     direccion = "la Avenida de la Paz numero 8"
     verbo = "cocinar"
     comienzo = "Erase una vez " + gender + " que se llamaba " + nombre + "."
     print(comienzo)
     siguiente1 = nombre + " vivia en " + direccion + "."

     print(siguiente1)
     siguiente2 = "Un dia, una bruja se acerco a casa de la familia " + apellido + "."
     print(siguiente2)
     siguiente3 = "La malvada bruja se queria " + verbo + " a " + nombre + "."
     print(siguiente3)
     final = "Pero " + nombre + " se dio cuenta de sus intenciones y se libro de ella."
     print(final)
     
.. mchoicemf:: 4_2_3_StringVsVariableName
   :answer_a: Cinco es Cinco
   :answer_b: Cinco es 5
   :answer_c: 5 es Cinco
   :answer_d: 5 es 5
   :correct: b
   :feedback_a: No hay comillas delimitando el �ltimo Cinco, as� que utilizar� el valor de la variable Cinco.
   :feedback_b: El primer Cinco est� entre comillas, as� que se imprimir� la cadena Cinco. Y el segundo Cinco no est� entre comillas, as� que se imprimir� el valor de la variable Cinco.
   :feedback_c: El primer "Cinco" est� entre comillas, y el segundo no.
   :feedback_d: El primer Cinco est� entre comillas as� que es una cadena, y por tanto se imprimir�n todos los caracteres que contiene.
 
   �Qu� imprimir� el siguiente c�digo?
   
   :: 

     Cinco = 5
     print("Cinco" + " es " + str(Cinco))
     
.. Note::
   Cuando en Python se imprime una cadena (una secuencia de caracteres encerrados entre comillas simples o dobles) se imprimir�n exactamente sus caracteres, tal como se han especificado entre las comillas. Cuando se imprime una variable, lo que se imprimir� ser� el valor de dicha variable.
     
.. parsonsprob:: 4_2_4_Poem

   Coloca los bloques siguientes en el orden correcto para que se imprima una conocido trabalenguas.     
   -----
   print("El cielo est� enladrillado.")  	
   ===== 
   print("Qui�n lo desenladrillar�.)
   =====                
   print("El desenladrillador que lo desenladrille.")
   =====
   print("Buen desenladrillador ser�.")
     
.. parsonsprob:: 4_2_5_Story

   Coloca los siguientes bloques en el orden adecuado para declarar primero las variables e imprimir despu�s la siguiente historia. Un d�a Juan fue a la tienda. Quer�a comprar unos zapatos. Pero ning�n le gust�. As� que Juan regres� a casa.  
   -----
   nombre = "Juan"
   cosa = "unos zapatos"
   =====
   print("Un d�a " + nombre + " fue a la tienda.")  	
   ===== 
   print("Qu�ria comprar " + cosa + ".")
   =====                
   print("Pero ninguno le gust�.")
   =====
   print("As� que " + nombre + " regres� a casa.")
   

