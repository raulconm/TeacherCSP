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
	:prefix: csp-3-1-

.. highlight:: java
   :linenothreshold: 4

Asignar un nombre
==================

*Objetivos de aprendizaje:*

- Comprender el concepto de variable
- Asignar un valor a una variable
- Usar ese nombre para hacer cálculos
- Conocer los errores que cometen los estudiantes al asignar nombres
- Reutilizar las variables a lo largo del programa
	
..	index::
	single: variable
	pair: programming; variable
	
Un ordenador puede asociar un nombre con un valor. Esto se consigue creando una **variable**, que es un espacio de la memoria del ordenador que representa a un valor. Un ejemplo de **variable** puede ser el marcador de un videojuego. Normalmente este marcador se inicia con 0, y se va incrementando según el juego avanza. El marcador puede cambiar o *variar* durante el juego, de ahí el nombre de **variable**. También asocias un nombre a un número cuando añades un nuevo nombre y número de teléfono en la agenda de tu móvil. Cuando le pides que llame a "María", tu móvil buscará el número de teléfono asociado a ese nombre y llamará.

.. figure:: Figures/pongScore.png
    :width: 400px
    :align: center
    :figclass: align-center
    
    Imagen 1: Un juego de pong en `Scratch <http://scratch.mit.edu>`_ con un marcador en la esquina superior izquierda.
    
Imagina que una variable es como una caja que tiene una etiqueta, dentro de la cual puedes guardar un valor. El valor será cualquier cosa que se pueda representar en un ordenador, y que pueda almacenar en su memoria. La memoria de un ordenador está formada únicamente por números (en realidad por patrones de voltajes, pero podemos tomarlos como números). Todo lo que un ordenador puede recordar en su memoria se traduce a números -- pero no te preocupes ahora de cómo sucede esto.  

.. figure:: Figures/assignA.png
    :align: center
    :width: 60
    :figclass: align-center
    
    Imagen 2: Crear una variable y definir su valor en la memoria.

..	index::
	single: assignment
	pair: programming; assignment
	
En los lenguajes de programación, dar un nombre a una variable se conoce como **asignar**. Una instrucción como ``a = 4`` significa que el símbolo ``a`` hace referencia a un espacio (en la memoria del ordenador) que tiene asignado el valor ``4``. Cuando en el programa utilicemos el símbolo ``a``, el ordenador sabrá que nos referimos al valor ``4``. Si más adelante cambiamos el valor almacenado en ``a``, por ejemplo con la instrucción ``a = 7.2``, diremos que la variable ``a`` vale ahora ``7.2``, lo que significa que el valor contenido en la caja (de memoria) asociada con el nombre ``a`` se ha cambiado por ``7.2``.  

.. figure:: Figures/changeA.png
    :align: center
    :width: 60
    :figclass: align-center
    
    Imagen 3: Cambiar el valor de una variable en la memoria.

**Haz clic en el icono de reproducir para ver el siguiente vídeo.**

.. video:: intro_assignment
   :controls:
   :thumb: ../_static/video-think-about-assignment.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-v2-small.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-v2-small.webm
   
Nombres permitidos para las variables
-------------------------------------

..	index::
	single: variable names

Hay algunas restricciones sobre los nombres que puedes darle a las variables. 

* Deben comenzar por una letra (mayúscula como ``A`` o minúscula como ``a``) o por el símbolo de subrayado ``_``
* Puede contener números, como ``1`` o ``9``, pero no empezar por un número.
* No puede ser una palabra reservada de Python, como ``and``, ``def``, ``elif``, ``else``, ``for``, ``if``, ``import``, ``in``, ``not``, ``or``, ``return``, o ``while``.  Estas palabras tienen ya un significado en Python, son parte del lenguaje.
* Las mayúsculas y minúsuculas son importantes.  Una variable llamada ``resultado`` no es la misma que otra llamada ``Resultado``.

Como no están permitidos los espacios en el nombre de las variables, puedes unir palabras poniendo en mayúscula la primera letra de cada nueva palabra, como ``alturaEnCentimetros`` o utilizar el subrayado entre palabras, ``altura_en_centimetros``. 

.. mchoicemf:: 3_1_1_varNames_Q1
   :answer_a: _a1
   :answer_b: mi_nombre
   :answer_c: muchasCosas
   :answer_d: BMP
   :answer_e: 1A
   :correct: e
   :feedback_a: Sí puedes utilizar un signo de subrayado como primer carácter del nombre de una variable.
   :feedback_b: Sí puedes utilizar el subrayado entre las palabras del nombre de una variable.
   :feedback_c: En el nombre de una variable se pueden mezclar mayúsuculas y minúsculas.
   :feedback_d: Sí puedes utilizar sólo mayúsuculas en el nombre de una variable.
   :feedback_e: No está permitido que los nombres de variables comiencen por un número.

   ¿Cuál de los siguientes *no* es un nombre permitido para una variable?
   
.. mchoicemf:: 3_1_2_varNames_Q2
   :answer_a: _mi_nombre
   :answer_b: mi nombre
   :answer_c: minombre
   :answer_d: miNombre
   :answer_e: mi_nombre
   :correct: b
   :feedback_a: Está permitido, pero no es habitual que el nombre de una variable comience por subrayado.
   :feedback_b: Los nombres de variables no pueden contener espacios.  
   :feedback_c: Puede ser difícil de leer, pero está permitido.  
   :feedback_d: Como no están permitidos los espacios, una manera de facilitar la lectura es poner en mayúsucula la primera letra de cada palabra del nombre de la variable.  
   :feedback_e: Como no están permitidos los espacios en el nombre de las variables, puedes sustituirlos por subrayados.  

   ¿Cuál de los siguientes *no* es un nombre permitido para una variable?


