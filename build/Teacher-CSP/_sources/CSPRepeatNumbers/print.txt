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
	:prefix: csp-7-6-
	
.. highlight:: java
   :linenothreshold: 4


|bigteachernote| Nota para el profesor: Print() es tu amigo
===========================================================
El objetivo de este capítulo es desarrollar un modelo mental sobre cómo funciona el programa. ¿Podrán los estudiantes observar un programa y *predecir* qué es lo que va a ocurrir al ejecutarlo? ¿Serán capaces de deducir qqué valores tendrán las variables en cada momento? Incluye todos los ``print()`` que cnsideres que pueden ser útiles en las llamadas a las funciones. Deja que los estudiantes hagan predicciones sobre los valores de las variables, y después inserta ``prints()`` para que el programa vaya mostrando los valores de las variables, y ejecuta el programa para ver si su predicción ha sido acertada. Ejecuta esa versión para ver qué se imprime.

.. activecode:: Numbers_Sum_Print
    :tour_1: "Code tour"; 2: accL_line2; 4: accL_line4; 5: accL_line5; 7: accL_line7; 8: accL_line8; 10: accL_line10; 12: accL_line12;
	
    # PASO 1: INICIALIZA EL ACUMULADOR 
    suma = 0  # Comienza con 0
    # PASO 2: OBTIENE LOS DATOS
    numeros = range(0,101,2)
    print("Todos los números:",numeros)
    # PASO 3: BUCLE PARA RECORRER LOS DATOS
    for numero in numeros:
    	print("Numero:",numero)
    	# PASO 4: ACUMULA
    	suma = suma + numero
    # PASO 5: PROCESA EL RESULTADO
    print(suma)
    
.. parsonsprob:: 7_6_1_Print-Sum-Evens

   El siguiente código es el correcto para imprimir la suma de todos los números pares desde el 0 al 100 utilizando un patrón acumulador, pero las instrucciones están desordenadas. Arrastra los bloques de la izquierda y colócalos en orden en el lado derecho. No te olvides de indentar los bloques dentro del bucle. Para ello arrástralos un poco más hacia la derecha que el resto. Haz clic n el botón <i>Check Me</i> para comprobar la solución.</p>

   -----
   suma = 0  
   =====
   numeros = range(0,101,2)
   =====
   for numero in numeros:
   =====
       print("Número:",numero)
   =====
       suma = suma + numero
   =====
       print(suma)


