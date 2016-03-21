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
	:prefix: csp-7-3-
	
.. highlight:: java
   :linenothreshold: 4

¿Qué es una lista?
==================

Una **lista** contiene elementos en orden. Las **listas** en Python están encerradas entre ``[`` y ``]``, y puede contener valores separados por comas, ``[1,2,3,4,5,6,7,8,9,10]``. Seguramente utilices **listas** continuamente. Con frecuencia las personas hacemos listas antes de ir a comprar, o para no olvidar las cosas que tenemos que hacer. Una **lista** tiene un orden, y cada elemento ocupa una posición,de forma que hay un elemento en la primera posición, y otro en la última.   

.. figure:: Figures/lists.jpg
    :height: 250px
    :align: center
    :alt: a shopping list
    :figclass: align-center

    Figura 2: Lista de la compra

¿Fue 55 el resultado cuando ejecutaste el código de la sección anterior? Ésa es la suma de los números del 1 al 10. Aquí tienes de nuevo el programa. Ejecútalo si no te acuerdas de lo que imprimió antes. 

.. activecode:: Numbers_Repeat2
    :tour_1: "Line by line tour"; 1: for1_line1; 2: for1_line2; 3: for1_line3; 4: for1_line4; 5: for1_line5;
    :tour_2: "High level tour"; 1-2: for1_line1-2; 3-4: for1_line3-4; 5: for1_s_line5;
	
    suma = 0  # Valor inicial
    cosasQueAnadir = [1,2,3,4,5,6,7,8,9,10]
    for numero in cosasQueAnadir:
    	suma = suma + numero
    print(suma)

.. mchoicemf:: 7_3_1_Numbers_Repeat2_Q1
   :answer_a: 55
   :answer_b: 0
   :answer_c: 3628800
   :answer_d: Error - el número es demasiado alto
   :correct: c
   :feedback_a: Esa es la suma
   :feedback_b: Obtendrás esto si dejas suma como 0. Multiplicar algo por 0 siempre da 0
   :feedback_c: Eso sería 1*2*3*4*5*6*7*8*9*10
   :feedback_d: Realmente debería funcionar

   Ahora, modifica el programa para que multiplique en lugar de sumar (remplaza el signo ``+`` por ``*``, y cambia el valor inicial ``0`` de la ``suma``  por ``1``). ¿Qué obtendrás en este caso cuando ejecutes el programa?

|bigteachernote| Nota para el profesor: Los nombres son solamente palabras
======================================================
Una vez que hayas modificado el programa anterior para que utilice ``*`` en lugar de ``+`` verás que está aún usando el nombre (*variable*) ``suma`` para representar el `producto`de todos los números contenidos en ``cosasQueAnadir``. Será más *correcto* que el programa utilice el nombre adecuado para la variable: ``producto`` en lugar de ``suma``, ya que hemos cambiado suma (``+``) por multiplicación (``*``). Sin embargo el programa *funciona*. En realidad, los nombres de las variables son para mejor comprensión de los *humanos*, no de los *ordenadores*. Al ordenador no le importa si la variable se llama `xyzzy1776`. También *funcionará* con un nombre inapropiado. Simplemente será más difícil de comprender. **Debes acostumbrarte a escribir programas de forma que otras personas puedan entenderlos facilmente, no solamente los ordenadores.**

Elegir nombres adecuados para las variables 
-------------------------------------------

Vamos a escribir de nuevo el programa con un nombre de variable más apropiado. Le daremos a la variable que almacena el resultado del cálculo el nombre ``producto`` en lugar de llamarle ``suma``. Pulsa el botón *Forward* para que el programa avance, y observa qué valor va tomando la variable ``numero`` con cada vuelta del bucle. Fíjate también que la variable ``producto`` va cambiando durante la ejecución del bucle.

.. codelens:: Numbers_Product
	
    producto = 1  # Inicialmente vale 1
    numeros = [1,2,3,4,5,6,7,8,9,10]
    for numero in numeros:
    	producto = producto * numero
    print(producto)
    
.. mchoicemf:: 7_3_2_Numbers_Product_Q1
   :answer_a: 1
   :answer_b: 2
   :answer_c: 3
   :answer_d: 4
   :answer_e: 10
   :correct: c
   :feedback_a: Ese es el valor que tiene al dar la primera vueelta al bucle
   :feedback_b: Ese es el valor que tiene al dar la segunda vuelta al bucle
   :feedback_c: Ese es el valor que tiene al dar la tercera vuelta al bucle
   :feedback_d: Ese es el valor que tiene al dar la cuarta vuelta al bucle
   :feedback_e: Ese es el valor que tiene al dar la última vuelta al bucle

   ¿Qué valor tiene numero al dar la tercera vuelta al bucle?
   
.. mchoicemf:: 7_3_3_Numbers_Product_Q2
   :answer_a: 6
   :answer_b: 10
   :answer_c: 24
   :answer_d: 120
   :correct: c
   :feedback_a: Ese es el valor que tiene al dar la tercera vuelta al bucle
   :feedback_b: Ese es el valor si estuviéramos sumando los valores en lugar de multiplicándolos
   :feedback_c: Ese es el valor que tiene al dar la cuarta vuelta al bucle
   :feedback_d: Ese es el valor que tiene al dar la quinta vuelta al bucle

   ¿Cuánto valdrá el producto después de dar la cuarta vuelta al bucle?



