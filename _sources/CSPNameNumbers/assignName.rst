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
	
Un ordenador puede asociar un nombre con una variable. Esto se consigue creando una **variable**, que es un espacio de la memoria del ordenador que representa a un valor. Un ejemplo de **variable** puede ser el marcador de un videojuego. Normalmente este marcador se inicia con 0 se va incrementando según el juego avanza. El marcador puede camviar o *variar* durante el juego, de ahí el nombre de **variable**. También asocias un nombre a un número cuando añades un nuevo nombre y número de teléfono en la agenda de tu móvil. Cuando le pides que llame a "María" tu móvil buscará el número de teléfono asociado a ese nombre y llamará.

.. figure:: Figures/pongScore.png
    :width: 400px
    :align: center
    :figclass: align-center
    
    Imagen 1: Un juego de pong en `Scratch <http://scratch.mit.edu>`_ con un marcador en la esquina superior izquierda.
    
Imagina que una variable es cmo una caja que tiene una etiqueta, y dentro de la cual puedes guarda un valor. El valor será cualquier cosa que se pueda representar en un ordenador, y almacenado en su memoria. La memoria de un ordenador está formada únicamente por números (en realidad por patrones de voltajes, pero podemos tomarlos como números). Todo lo que un ordenador puede recordar en su memoria se traduce a números -- pero no te preocupes ahora de cómo sucede esto.  

.. figure:: Figures/assignA.png
    :align: center
    :width: 60
    :figclass: align-center
    
    Imagen 2: Crear una variable y definir su valor en la memoria.

..	index::
	single: assignment
	pair: programming; assignment
	
In programming languages, setting a variable's value is also called **assignment**.  A statement like ``a = 4`` means that the symbol ``a`` refers to space (in the computer's memory) that is assigned the value ``4``.  When we use the symbol ``a`` in a program the computer will substitute the value ``4``.  If we later change the value stored at ``a``, say by doing ``a = 7.2`` then we say that the variable ``a`` now has the value ``7.2`` meaning that the value in the box (memory) associated with the name ``a`` is changed to ``7.2``.

.. figure:: Figures/changeA.png
    :align: center
    :width: 60
    :figclass: align-center
    
    Figure 3: Changing the value of a variable in memory

**Click on the right arrow below to play the following video.**

.. video:: intro_assignment
   :controls:
   :thumb: ../_static/video-think-about-assignment.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-v2-small.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-v2-small.webm
   
Legal Variable Names
----------------------

..	index::
	single: variable names

There are restrictions on what you can use as a variable name. 

* It must start with a letter (uppercase like ``A`` or lowercase like ``a``) or an underscore ``_``
* It can also contain digits, like ``1`` or ``9``, just not as the first character
* It can't be a Python keyword such as ``and``, ``def``, ``elif``, ``else``, ``for``, ``if``, ``import``, ``in``, ``not``, ``or``, ``return``, or ``while``.  These have special meaning in Python and are part of the language.
* Case does matter.  A variable named ``result`` is not the same as one named ``Result``.

Since you can't have spaces in a variable name you can either join words together by uppercasing the first letter of each new word like ``heightInInches`` or use underscores between words ``height_in_inches``.  Uppercasing the first letter of each new word is called **camel-case** or **mixed-case**.  

.. mchoicemf:: 3_1_1_varNames_Q1
   :answer_a: _a1
   :answer_b: my_name
   :answer_c: amountOfStuff
   :answer_d: BMP
   :answer_e: 1A
   :correct: e
   :feedback_a: You can use an underscore as the first character in a variable name
   :feedback_b: You can use an underscore between words in a variable name.
   :feedback_c: You can use both uppercase and lowercase letters in a variable name.
   :feedback_d: You can use only uppercase letters in a variable name.
   :feedback_e: You can't use a digit as the first letter in a variable name.

   Which of the following is *not* a legal variable name?
   
.. mchoicemf:: 3_1_2_varNames_Q2
   :answer_a: _my_name
   :answer_b: my name
   :answer_c: myname
   :answer_d: myName
   :answer_e: my_name
   :correct: b
   :feedback_a: This is legal, but you don't usually start a variable name with an underscore.
   :feedback_b: You can't have a space in a variable name.  
   :feedback_c: This may be hard to read, but it is legal.  
   :feedback_d: Since you can't have spaces in names, one way to make variable names easier to read is to use camel case (uppercase the first letter of each new word).  
   :feedback_e: Since you can't have spaces in names, one way to make variable names easier to read is to use an underscore between two words.  

   Which of the following is *not* a legal variable name?


