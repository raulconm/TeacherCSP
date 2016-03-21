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
	:prefix: csp-7-2-
	
.. highlight:: java
   :linenothreshold: 4

Repeticiones con números
========================

..	index::
	single: lista

..	index::
	single: bucle for
	pair: bucle; for
	pair: bucle; cuerpo
	pair: bucle; indentación
	

Vamos a utilizar un bucle ``for``. El bucle ``for`` es un tipo de bucle, o una forma de repetir una instrucción o conjunto de instrucciones en un programa. Un bucle ``for`` utiliza una variable, y hace que dicha variable vaya tomando cada vez uno de los números de una **lista**. Fíjate que la línea 3 del programa siguiente termina con un ``:``, y que la línea 4 está **indentada**, que significa que comienza debajo de la letra ``n`` de ``número``. **Indentado** significa que la línea comienza con espacios, de modo que el texto no empieza justo al principio de la línea. En un bucle son necesarios tanto el signo ``:`` como la indentación. La instrucción de la línea 3 determina el comienzo del bucle ``for``, y la línea 4 es el **cuerpo** del bucle. El **cuerpo** se repite para cada uno de los valores de la lista ``cosasQueAñadir``.
  

¿Cuánto vale la suma de todos los números del 1 al 10? Eecuta el programa siguiente para conocer la respuesta.

.. activecode:: Numbers_Repeat1
    :tour_1: "Line by line tour"; 1: for1_line1; 2: for1_line2; 3: for1_line3; 4: for1_line4; 5: for1_line5;
    :tour_2: "High level tour"; 1-2: for1_line1-2; 3-4: for1_line3-4; 5: for1_s_line5;
	
    suma = 0  # Inicialmente el valor es 0
    cosasQueAñadir = [1,2,3,4,5,6,7,8,9,10]
    for numero in cosasQueAñadir:
    	suma = suma + numero
    print(suma)
    
.. mchoicemf:: 7_2_1_Numbers_Repeat1_Q1
   :answer_a: Imprime lo mismo que antes.
   :answer_b: Imprime el valor de la suma diez veces y la suma es distinta cada vez que se imprime.
   :answer_c: Imprime el mismo número diez veces.
   :answer_d: Nos da un error.
   :correct: b
   :feedback_a: ¿De verdad lo has probado?
   :feedback_b: Ahora las líneas 4 y 5 están en el cuerpo del bucle, y se ejecutan con cada vuelta del bucle. 
   :feedback_c: La suma debería ir cambiando.  
   :feedback_d: El cuerpo del bucle puede contener más de una línea.

   ¿Qué imprimirá el programa si haces que la línea 5 esté indentada de la misma forma que la 4?
   
.. mchoicemf:: 7_2_2_Numbers_Repeat1_Q2
   :answer_a: Imprime lo mismo que antes.
   :answer_b: Imprime diez veces el valor de la suma y la suma es distinta cada vez.
   :answer_c: Imprime diez veces la misma suma.
   :answer_d: El programa muestra un error.
   :correct: d
   :feedback_a: ¿De verdad lo has probado?
   :feedback_b: Ni la línea 4 ni la 5 están ya dentro del bucle.
   :feedback_c: ¿Se repite ahora el bucle? 
   :feedback_d: Debes incluir al menos una instrucción dentro del cuerpo del bucle.

   ¿Qué va a imprimir el programa si lo modificas para que no estén indentadas ni la línea 4 ni la 5?
   


