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
	:prefix: csp-3-5-

.. highlight:: java
   :linenothreshold: 4

Conducir de M�laga a Santander
==============================

..	index::
	single: CodeLens
	
Imag�nate que est�s planeando un viaje de M�laga a Santander. Si sabes cu�ntos kil�metros por litro puede recorrer tu coche, y cu�ntos kil�metros de distancia hay de una ciudad a otra, puedes calcular el n�mero de litros que vas a consumir.

Utiliza el siguiente *CodeLens* para observar c�mo ejecutar�a un ordenador el siguiente programa:

- Pulsa |codelensfwd| para ejecutar el programa l�nea por l�nea.
- Pulsa |codelenslast| para ejecutar todas las l�neas del programa de una vez.

.. codelens:: Malaga_2_Santander

   distancia = 948.1
   kpl = 16
   litros = distancia / kpl
   
..	index::
	single: camel case

Adem�s, si sabemos cu�l es el coste medio de un litro de combustible, podemos calcular cu�nto nos va a costar el viaje en coche de M�laga a Santander.  

.. Note::

   Observa que estamos utilizando nombres de variables como ``costePorLitro`` y ``costeDelViaje``. Un nombre de variable no puede contener espacios, as� que una forma de hacer que la variable sea m�s f�cil de leer cuando contiene m�s de una palabra es escribiendo en may�scula la primera letra de cada nueva palabra, como en ``costePorLitro`` y ``costeDelViaje``. F�jate que esta diferencia entre may�sculas y min�suclas es importante en Python, porque ``costedelviaje`` y ``costeDelViaje`` ser�n variables distintas.   

.. codelens:: Malaga_2_Santander_Coste

   distancia = 948.1
   kpl = 16
   litros = distancia / kpl
   costePorLitro = 1.22
   costDelViaje = litros * costePorLitro
   
..	index::
	single: tracing
	single: string
	single: print
	pair: programming; tracing
	
Esto que hemos hecho se llama **trazar** el programa. Normalmente lo que hacemos es **ejecutar** un programa -- le decimos al ordenador que ejecute cada paso del programa tan r�pido como pueda. Cuando lo hacemos, no podemos ver los valores que va tomando cada variable, como hemos hecho aqu�. Podemos saber qu� valores tiene cada variable haciendo que se muestren en la pantalla del ordenador. La funci�n ``print`` puede tomar una *entrada* (el nombre de una variable indicada entre par�ntesis) y mostrar su contenido, su valor, por pantalla. Con ``print`` tambi�n se puede imprimir en pantalla una **cadena de caracteres** (como ``"Coste para ir de M�laga a Santander"``), que es una secuencia de caracteres delimitada por comillas, como en la l�nea 6. Esto imprimir� el contenido exacto de la cadena, y es muy �til para indicar qu� valores se est�n mostrando.

Pulsa |runbutton| para ejecutar este programa a velocidad normal.

.. activecode:: Trip_Calculator
   :tour_1: "Line by line tour"; 1: trp-line1; 2: trp-line2; 3: trp-line3; 4: trp-line4; 5: trp-line5; 6: trp-line6; 7: trp-line7; 

   distancia = 948.1
   kpl = 16
   litros = distancia / kpl
   costePorLitro = 1.22
   costeDelViaje = litros * costePorLitro
   print("Coste del viaje de Malaga a Santander")
   print(costeDelViaje)

�C�mo funciona este programa? Pulsa el bot�n |audiobutton| para escuchar una explicaci�n al programa. 

Modifica el programa anterior y ejec�talo para contestar a esta pregunta:

.. mchoicemf:: 3_5_1_Malaga_2_Santander_Q1
   :answer_a: S�.
   :answer_b: No.
   :answer_c: Ser�a mejor ir en avi�n.
   :correct: a
   :feedback_a: S�, el coste ser�a 69.922375 euros (lo has confirmado al modificar y ejecutar el programa anterior).
   :feedback_b: Pru�balo -- est� justo por debajo del l�mite de 70 euros.
   :feedback_c: Puede que tengas raz�n, pero mejor calcula el coste modificando en programa.

    Si el precio por litro fuera de 1.18 euros, �podr�amos conducir de M�laga a Santander por menos de 70 euros de combustible?
   
.. mchoicemf:: 3_5_2_Malaga_2_Santander_Q2
   :answer_a: 1.22
   :answer_b: 1.18
   :answer_c: costePorLitro
   :correct: c
   :feedback_a: Ser�a cierto si estuvi�ramos imprimiendo el valor de la variable original.
   :feedback_b: Ser�a as� si estuvi�ramos imprimiendo el valor de la variable una vez modificado para calcular la pregunta anterior.
   :feedback_c: Como <code>costPorLitro</code> est� entre comillas el programa lo considera una cadena, y por tanto imprime extactamente los caracteres que contiene la cadena.

   �Qu� imprimir� la instrucci�n ``print("costePorLitro")`` si a�adimos esta l�nea al final del programa?



