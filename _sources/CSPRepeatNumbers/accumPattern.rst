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
	:prefix: csp-7-5-
	
.. highlight:: java
   :linenothreshold: 4


�Aqu� hay un patr�n!
=====================================

Hay en estos programas un patr�n, algo que es com�n cuando est� procesando los datos. Es lo que llamamos el **Patr�n Acumulador**. En el primer programa **acumulamos** los valores en la variable ``suma``. En los programas posteriores **acumulamos** el producto en la variable ``producto``.

Veamos los cinco pasos identificados en este patr�n.

1. Se establece la variable del acumulador a su valor inicial. Es el valor que queremos que tenga cuando no todav�a no se ha procesado ning�n dato.
2. Se genera la lista de datos a procesar.
3. Recorremos el conjunto de datos con un bucle ``for``, procesando todos ellos secuencialmente.
4. Incluimos cada dato en el acumulador.
5. Hacemos algo con el resultado.

Utilizar el patr�n acumulador
=====================================

�Cu�nto vale la suma de todos los n�meros del 0 al 100?? Podemos conocer facilmente la respuesta a esta pregunta utilizando un patr�n.

.. activecode:: Numbers_Sum
    :tour_1: "Code tour"; 2: accum_line2; 4: accum_line4; 6: accum_line6; 8: accum_line8; 10: accum_line10;
	
    # PASO 1: INICIALIZAR EL ACUMULADOR 
    suma = 0  # Comenzamos con cero
    # PASO 2: TOMA LOS DATOS
    numeros = range(101)
    # PASO 3: RECORRE EN BUCLE TODOS LOS DATOS
    for numero in numeros:
    	# PASO 4: ACUMULA 
    	suma = suma + numero
    # PASO 5: PROCESA EL RESULTADO
    print(suma)
    
.. parsonsprob:: 7_5_1_Sum_100

   
   A continuaci�n se muestra el c�digo apropiado para imprimir la suma de todos los n�meros impares del 1 al 100 utilizando un patr�n acumulador, pero el c�digo est� desordenado. Toma los bloques del lado izquierdo y col�calos en orden en la parte derecha. <b>�Recuerda que dentro del cuerpo de un bucle las instrucciones deben estar indentadas!</b> Para indentar un bloque arr�stralo un poco m�s a la derecha. Haz clic en el bot�n <i>Check Me</i> para comprobar la ssoluci�n.</p>

   -----
   suma = 0  
   =====
   numeros = range(1,100,2)
   =====
   for numero in numeros:
   =====
       suma = suma + numero
   =====
   print(suma)

Existe una variaci�n m�s de la funci�n `range`, que vamos a utilizar. Si le proporcionamos a la funci�n **tres** valores como entrada, le estaremos especificando el valor *inicial*, el valor *final* (que ya sabemos qu es uno m�s que el �ltimo de la lista) y el valor del *intervalo* -- esto es, cu�ntos n�meros hay *entre* un n�mero y el siguiente de la lista.   

.. activecode:: Range_Examples

  print range(10)
  print range(1,11)
  print range(0,11,2)
  print range(1,11,3)

Ahora contestemos a una pregunta un poco m�s dif�cil: �Cu�l es la suma de todos los n�meros *pares* desde el 0 hasta el 100? Con nuestro patr�n la respuesta es f�cil. 
  
.. activecode:: Numbers_Sum_Even
    :tour_1: "Code tour"; 2: accE_line2; 4: accE_line4; 6: accE_line6; 8: accE_line8; 10: accE_line10;
	
    # PASO 1: INICIALIZA EL ACUMULADOR 
    suma = 0  # Comienza sin datos
    # PASO 2: TOMA LA LISTA DE DATOS
    numeros = range(0,101,2)
    # PASO 3: RECORRE LA LISTA DE DATOS
    for numero in numeros:
    	# PASO 4: ACUMULA 
    	suma = suma + numero
    # PASO 5: PROCESA EL RESULTADO
    print(suma)

.. mchoicemf:: 7_5_2_Numbers_Even_Q1
   :answer_a: Porque hemos comenzado con el 0
   :answer_b: Porque queremos incluir el 100
   :answer_c: Porque el ordenador s�lo entiende unos y ceros
   :answer_d: Porque estamos saltando de dos en dos
   :correct: b
   :feedback_a: Quer�amos incluir el 100.
   :feedback_b: Si el valor final es 101, se incluir� e 100.
   :feedback_c: Internamente s�, pero en Python se pueden utilizar todos los n�meros decimales.
   :feedback_d: Eso realmente no es importante.

   �Por qu� el valor final del programa anterior es 101?

.. mchoicemf:: 7_5_3_Numbers_Even_Q2
   :answer_a: Porque si empezamos en el 1 obtendremos la lista de n�meros impares
   :answer_b: Porque todas las listas comienzan con un 0
   :answer_c: Porque terminamos en 101
   :correct: a
   :feedback_a: Esto nos devuelve [0,2,4,6...98,100].
   :feedback_b: No tiene que comenzar por 0.  
   :feedback_c: Es cierto, pero en este caso no importa.

   �Por qu� comenzamos por cero?

�C�mo sabemos qu� hace realmente este programa? �C�mo podemos saber que *n�mero* va tomando todos los valores pares del 0 al 100? Una forma es utilizando CodeLens con un escenario m�s reducido, de 0 a 20. Podemos recorrer el programa l�nea por l�nea, o ir directamente al final haciendo clic en el bot�n *Last*, y desde ah� volver hacia atr�s.

.. codelens:: Numbers_Sum_Step
	
    # PASO 1: INICIALIZA EL ACUMULADOR 
    suma = 0  # Comenzamos sin valor
    # PASO 2: GENERA LA LISTA DE DATOS
    numeros = range(0,21,2)
    # PASO 3: RECORRE LA LISTA
    for numero in numeros:
    	# PASO 4: ACUMULA
    	suma = suma + numero
    # PASO 5: PROCESA EL RESULTADO
    print(suma)

.. mchoicemf:: 7_5_4_Numbers_Add_Odds_Q1
   :answer_a: Cambia en el rango el valor del salto de 2 a 3
   :answer_b: Cambia el valor final del rango de 101 a 100
   :answer_c: Cambia el valor final del rango de 101 a 99
   :answer_d: Cambia el valor incial del rango de 0 a 1
   :correct: d
   :feedback_a: Esto nos devuelve [0,3,6,9,12...99].
   :feedback_b: Esto nos devuelve los n�meros pares desde el 0 hasta 98.
   :feedback_c: Esto nos devuelve los n�meros pares desde el 0 hasta el 98.
   :feedback_d: Estoo nos devuelve [1,3,5,...99].

   Modifica el programa anterior (in ActiveCode 3: Numbers_Sum_Even) para calcular la suma de todos los n�meros IMPARES incluyendo el 99. La respuesta deber�a ser 2500. �Qu� modificaci�n habr�a que hacer en el programa?
   
.. parsonsprob:: 7_5_5_Sum_From_50

   El siguiente c�digo es el correcto para imprimir la suma de todos los n�meros pares desde el 50 al 100 utilizando un patr�n acumulador, pero las instrucciones est�n desordenadas. Arrastra los bloques de la izquierda y col�calos en orden en el lado derecho. No te olvides de indentar los bloques dentro del bucle. Para ello arr�stralos un poco m�s hacia la derecha que el resto. Haz clic n el bot�n <i>Check Me</i> para comprobar la soluci�n.</p>
   -----
   suma = 0  
   =====
   numeros = range(50,101,2)
   =====
   for numero in numeros:
   =====
       suma = suma + numero
   =====
   print(suma)
   =====
   numeros = range(50,100,2) #para distraer :)




