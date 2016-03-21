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
	:prefix: csp-9-1-
	
.. highlight:: java
   :linenothreshold: 4

Usar repeticiones con cadenas de caracteres
===========================================

*Objetivos de aprendizaje:*

- Mostrar cómo funciona el patrón acumulador con cadenas de caracteres  
- Ver cómo dar la vuelta a una cadena de caracteres
- Mostrar cómo construir una cadena espejo

..	index::
	single: asignación
	pair: cadenas de caracteres; asignación

.. index::
    single: palabras
    single: cadenas de caracteres
	single: bucle for

En el capítulo anterior ya vimos cómo podemos jugar con los números usando Python. Ahora vamos a ver que podemos hacer lo mismo con las palabras. Un conjunto de letras, números, u otros caracteres, por ejemplo espacios, encerrados entre comillas simples o dobles, se conoce como **cadena de caracteres**. El bucle ``for`` de Python nos va a permitir recorrer la cadena letra a letra, y el signo ``+`` sirve para unir cadenas. Lo mejor es que también en este caso puede utilizarse el patrón acumulador.   

Hagamos memoria repasando los cinco pasos del patrón acumulador:

1. Establecer el acumulador en su valor incial. El valor que debe tener cuando no se ha procesado ningún dato.
2. Tomar los datos que se van a procesar.
3. Recorrer los datos utilizando un bucle ``for``, de forma que la variable tome secuencialmente cada uno de los datos.
4. Combinar cada **dato** en el acumulador.
5. Hacer algo con el resultado.

Pulsa el botón |audiobutton| para escuchar cómo funciona este programa. 

.. activecode:: Copy_Words
    :tour_1: "Lines of code"; 2: strR1-line2; 4: strR1-line4; 6: strR1-line6; 8: strR1-line8; 10: strR1-line10;

    # PASO 1: INICIALIZAR EL ACUMULADOR 
    nuevaCadena = ""
    # PASO 2: OBTENER LOS DATOS
    frase = "Pablito clava un clavito."
    # PASO 3: BUCLE PARA RECORRER LOS DATOS
    for letra in frase:
    	# PASO 4: ACUMULAR
    	nuevaCadena = nuevaCadena + letra
    # PASO 5: PROCESAR EL RESULTADO
    print(nuevaCadena)

Ejecuta el programa. No es muy interesante, ¿verdad? Simplemente copia todas las letras de ``frase`` en ``nuevaCadena``.

