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
	:prefix: csp-1-2-


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

Computación con números
=======================

No utilizaremos muchas matemáticas en este eBook, así que no te preocupes si no son tu fuerte. Ejecutarás y modificarás programas que trabajan con palabras, tortugas (virtuales), e imágenes, además de con números. La únicas operaciones matemáticas que vas a necesitar son suma, resta, multiplicación, y división.

..	index::
	single: variable
	pair: programming; variable

Los ordenadores se utilizaron inicialmente para calcular. Puede que estés acostumbrado a usar la calculadora, pero suele ser más sencillo calcular si *das un nombre* a los números con los que estás trabajando. Cuando le das un nombre a un número, o al resultado de una operación de cálculo, estás creando una **variable**. Una **variable** es un nombre que se da a la memoria del ordenador que puede almacenar un valor, y que puede cambiar. Un ejemplo de **variable** es el marcador de los puntos en un juego. El marcador comienza valiendo cero, y se incrementa según vamos jugando. 

.. figure:: Figures/pongScore.png
    :width: 400px
    :align: center
    :alt: A game in Scratch with a score
    :figclass: align-center
    
    Imagen 2: Juego de pong en `Scratch <http://scratch.mit.edu>`_ con un marcador en la parte superior izquierda.


Un valor que puedes calcular es el **Indice de Masa Corporal**.    El `Indice de Masa Corporal (IMC) <http://es.calcuworld.com/deporte-y-ejercicio/calculadora-de-imc/>`_ mide la cantidad de grasa que hay en el cuerpo, y es útil para determinar problemas de salud. En términos generales: 

- Un IMC igual o inferior a 18.5 se considera *bajo peso*
- Un IMC entre 18.5 y 24.9 se considera *saludable*
- Un IMC entre 25-29.9 se considera *sobrepeso*
- Un IMC igual o superior a 30 indica *obesidad* 

Para poder calcular el IMC necesitas saber la altura en metros y el peso en kilos. Debes elevar la altura al cuadrado (multiplicándola por sí misma), y a continuación dividir el peso por esa altura al cuadrado. 

En el cuadro de abajo puedes ver un programa que calcula el IMC de una persona que mide 1,60 metros y pesa 50 kilos.

Pulsa el botón |runbutton| para que el ordenador ejecute estos pasos. A la derecha verás el resultado de ejecutar el programa. 

Pulsa el botón |audiobutton| para abrir una ventana donde se explica qué hace el programa, línea por línea.

Sólo podrás utilizar los botones *Guardar* y *Cargar* si has iniciado sesión. El botón *Guardar* permite conservar el programa actual, y el botón *Cargar* sirve para recuperar un programa que se ha guardado previamente.

.. activecode:: BMI
    :tour_1: "Line-by-line Tour"; 1: BMI-line1; 2: BMI-line2; 3: BMI-line3; 4: BMI-line4; 5: BMI-line5; 6: BMI-line6; 7: BMI-line7; 
    :nocodelens:
    
    altura = 1.60    # en metros. La coma decimal debe expresarse como punto
    peso = 50   # en kilos
    alturaalcuadrado = altura * altura
    IMC = peso / alturaalcuadrado
    print("IMC: ")
    print(IMC)

Modifica en el programa los valores de altura y peso y haz clic en el botón *Run* para calcular un nuevo IMC. No olvides que la coma decimal debe expresarse como un punto.

.. Note::
   Al dar un nombre a los valores (usando variables) de altura y peso es más fácil saber qué valor se cambia en cada momento.

.. mchoicemf:: 1_2_1_BMI_Q1
   :answer_a: 26,2
   :answer_b: 26,2345679012
   :answer_c: 26
   :answer_d: 27
   :correct: b
   :feedback_a: Has estado cerca, pero el ordenador te va a dar más decimales.
   :feedback_b: ¡Bien hecho!
   :feedback_c: No, el resultado va a contener una coma, y cifras decimales.
   :feedback_d: No, el ordenador no redondea el resultado.
   
   Imagina que mides 1,80 metros y pesas 85 kilos. ¿Cuál sería tu IMC?

