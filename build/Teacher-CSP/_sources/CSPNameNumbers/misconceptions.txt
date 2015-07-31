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
	:prefix: csp-3-8-

.. highlight:: java
   :linenothreshold: 4

|bigteachernote| Nota para el profesor: Ideas equivocadas
=========================================================

..	index::
	pair: misconceptions; assignment
	single: assignment move misconception
	single: assignment relationship misconception

Hay muchos estudios que demuestran que el concepto de asignación es difícil de comprender para los estudiantes que se inician en la programación. `En un estudio elaborado por diseñadores gráficos profesionales que aprendieron a programar de forma autodidacta  <http://doi.acm.org/10.1145/1753326.1753430>`_, se manifestaba que la instrucción de asignación era la más difícil de asimilar. ¿Por qué es así?

Puede ser porque las asignaciones requieren que el programador entienda y anticipe qué es lo que ocurre en el programa. En las asignaciones siempre el *valor especificado en el lado derecho* del signo igual se copia al espacio de memoria (en la memoria del ordenador) referido por *la variable indicada en el lado izquierdo*. `Investigadores de la Universidad Middlesex en Inglaterra <http://www.eis.mdx.ac.uk/research/PhDArea/saeed/>`_ descubrieron que el hecho de comprender rápidamente que una instrucción de asignación **siempre** funciona de la misma manera es un buen indicador del éxito que una persona tendrá programando.

**¿Qué errores cometen los estudiantes en las asignaciones?** Aquí se muestran tres. El primero es creer que una asignación consiste en *mover* un valor (en lugar de *copiar*). Es decir, que los estudiantes crean que después de ejecutarse ``var1 = var2`` la variable ``var1`` tiene el valor que tenía ``var2`` y que la variable ``var2`` se queda con valor cero, o sin valor.

**Haz clic en el icono para reproducir el siguiente vídeo.**
   
.. video:: assignment_zero
   :controls:
   :thumb: ../_static/video-misconception-zeroing.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-zeroed-small.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-zeroed-small.webm  

El segundo caso, tal vez más común, consiste en entender equivocadamente la asignación como una *relación*. Así, una vez ejecutada la instrucción ``var1 = var2`` el estudiante cree que cualquier cambio posterior en ``var2`` cambiará automáticamente el valor almacenado en ``var1``. El problema aquí reside en que el estudiante no entiende la instrucción de la asignación como una *acción*. Si el estudiante no comprende que una asignación es una acción, también le costará entender por qué es importante que las instrucciones se ejecuten en un *orden* determinado.

.. video:: assignment_relationship
   :controls:
   :thumb: ../_static/video-misconception-relationship.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-relationship-small.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/assignment-relationship-small.webm 
   
Un tercer problema se debe a que algunos estudiantes tienen *dislexia en las asignaciones*. Esto se traduce en que en lugar de escribir el nombre de la variable en el lado izquierdo del `=` y el valor en el lado derecho, ellos intercambian las posiciones, como se muestra en el ejemplo siguiente.

:: 

   7 = diasEnSemana
   
El ordenador entiene esta instrucción como un intento de modificar el valor de 7, y eso no está permitido. Esta instrucción mostrará un error cuando intentes ejecutarla.  

**¿Cómo podemos ayudar a los estudiantes a comprender las asignaciones?** Es importante que ellos tracen programas que incluyan asignaciones, y que vayan dibujando recuadros en un papel que representen los espacios de la memoria del ordenador, escribiendo dentro los valores que contienen. Si observamos que están asumiendo equivocadamente uno de estos modelos que hemos indicado, podemos utilizar algunos de los ejemplos mostrados en esta sección -- de forma que intenten trazar primero el programa por sí mismos, y después lo ejecuten en el ordenador. De esta forma ellos mismos podrán comprobar que su modelo no se corresponde con lo que realmente hace el ordenador. 

Digamos que le muestras a Ana este programa:

.. sourcecode:: python

	numero2 = 32
	numero1 = numero2
	numero2 = 17

Entonces le preguntas a Ana: "¿Cuál es el valor de la variable `numero1`?"

.. mchoicemf:: 3_8_1_Diagnosing_Assignment_Q1
  :answer_a: Ana puede entender la asignación como un movimiento.
  :answer_b: Ana puede entender la asignación como una copia.
  :answer_c: Ana puede ver la asignación como una relación.
  :correct: c
  :feedback_a: Como un movimiento significa que numero1 es 32 y numero2  es 17, pero que numero2 se queda vacío o con valor cero después de la instrucción numero1 = numero2
  :feedback_b: La asignación realmente es una copia, así que esto no es un error. Comprender la asignación como una copia significa que numero1 NO tiene nunca el valor 17.
  :feedback_c: Si Ana cree que siempre que se cambie el valor de numero2 se cambiará también el de numero1, significa que está asumiendo erroneamente que una asignación establece una relación.

   Si su respuesta es `17`, ¿qué tipo de idea equivocada está teniendo Ana?


