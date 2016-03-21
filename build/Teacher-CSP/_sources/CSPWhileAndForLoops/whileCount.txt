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
	:prefix: csp-8-2-
	
.. highlight:: java
   :linenothreshold: 4

Bucles para contar
==================

Es muy fácil hacer que un ordenador repita algo un número definido de veces. Por ejemplo, podemos pedirle a un ordendor que cuente de 1 a 10 muy facilmente. Utilizaremos una variable ``contador`` que se irá **incrementando** dentro del bucle. **Incrementar** se refiere a que su valor irá aumentando de uno en uno.

.. codelens:: While_Counter
   :showoutput: 

   contador = 1
   while contador <= 10:
       print(contador)
       contador = contador + 1

.. mchoicemf:: 8_2_1_While_Counter_Q1
		  :answer_a: Porque incrementa la variable contador. 
		  :answer_b: Como la variable contador se usa en la comprobación del bucle while, si no fuera cambiando el bucle sería infinito. 
		  :correct: b
		  :feedback_a: Pero, ¿por qué está en el bucle?
		  :feedback_b: Debe cambiar dentro del bucle para que el bucle pare

	   	  ¿Por qué es importante tener la instrucción  ``contador = contador + 1`` dentro del bucle?


.. mchoicemf:: 8_2_2_While_Counter_Q2
	  :answer_a: 1
	  :answer_b: 10
	  :answer_c: 11
	  :correct: c
	  :feedback_a: Contador se incrementa en 1.
	  :feedback_b: El último valor a imprimir es 10.
	  :feedback_c: Contador se incrementa a 11 después de imprimirse, después el while compara el valor, y como contador > 10 se para.

   	  ¿Cuál es el valor del contador cuando termina el programa?
   	
.. parsonsprob:: 8_2_3_While_Countdown

   </p>A continuación se muestra el programa apropiado para imprimir una cuenta atrás de 10 a 0, pero está desordenado. Arrastra los bloques de la izquierda y colócalos en orden en la parte derecha. No te olvides de indentar los bloques en el cuerpo del bucle. Para hacerlos simplemente arrastra los bloques un poco más a la derecha. Haz clic en el botón <i>Check Me</i> para comprobar si la solución es correcta.</p> 
   -----
   contador = 10
   while contador >= 0:
       print(contador)
       contador = contador - 1 

.. index::
	pair: instrucciones; for
	single: definite loop
	
.. parsonsprob:: 8_2_4_While_Count_Even

   Este ejercicio muestra el código adecuado para imprimir los números pares del 0 al 10, pero contiene algunas instrucciones adicionales que no son necesarias. Arrastra los bloques necesarios desde la parte izquierda y colócalos a la derecha en el orden adecuado. No te olvides de indentar los bloques en el cuerpo del mensaje. Simplemente tienes que arrastrar los bloques un poco más a la derecha para indentarlos. Haz clic en el botón <i>Check Me</i> para comprobar tu solución.</p> 
   -----
   contador = 0
   =====
   while contador <= 10:
   =====
       print(contador)
   =====
       contador = contador + 2
   =====
       contador = contador + 1 #para distraer
    

.. index::
	pair: statements; for
	single: definite loop

Como es muy frecuente utilizar un bucle para contar, existe un bucle específico para *bucles finitos* (bucles que se repiten un número finito de veces). Se trata del bucle ``for`` que ya vimos en el capítulo anterior. ``El bucle ``for`` contiene una variable contador  que va tomando los valores de un ``rango``. Para construir un bucle que se ejecute un número determinado de veces es más sencillo usar un bucle ``for`` que un bucle ``while``. A continuación puedes ver el mismo programa del contador pero utilizando un bucle ``for``.

.. codelens:: For_Counter
	:showoutput: 

	for contador in range(1,10):
	    print(contador)

Antes de trazar el programa anterior hasta el final, comprueba si eres capaz de ccontestar a esta pregunta:

.. mchoicemf:: 8_2_5_For_Counter_Q1
		  :answer_a: 9
		  :answer_b: 10
		  :answer_c: 11
		  :correct: a
		  :feedback_a: Un rango comprende los valores desde el inicial hasta uno **menos** que el final. Si queremos contar hasta 10 debemos utilizar la instrucción range(1,11).
		  :feedback_b: Pruébalo. No, nunca llega a 10.
		  :feedback_c: De hecho, ni siquiera llegará a 10, ¡pruébalo!

	   	  ¿Qué valor será el último que se imprima?

Dentro de cualquier bucle podemos incluir... ¡otro bucle! He aquí una programa muy simple que genera todas las tablas de multiplicar del 0 al 10. Utiliza la función ``str(()'' para convertir todos los valores numéricos en cadenas de caracteres. 

.. codelens:: Times_Table
	:showoutput: 

	for x in range(0,11):
	    for y in range(0,11):
	        print(str(x) + " * " + str(y) + " = " + str(x*y))
		

A continuación se muestran el programa de dos formas distintas. En primer lugar se observa la *estructura* del programa, es decir, lo que podemos entender simplemente **mirando** el programa.

.. video:: timesTableStructure
		   :controls:
		   :thumb: ../_static/timesTableStructure.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopStructure.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopStructure.webm


En el siguiente vídeo se muestra la *ejecución* del programa, es decir, qué es lo que hace realmente cuando el ordenador lo *ejecuta*.

.. video:: timesTableTrace
		   :controls:
		   :thumb: ../_static/timesTableTrace.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopTrace.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopTrace.webm
