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
	:prefix: csp-8-4-
	
.. highlight:: java
   :linenothreshold: 4

	
|bigteachernote| Nota para el profesor: los bucles for son más naturales
================================================================

Algunos investigadores han estudiado la forma en que la gente describe los programas con un estilo "natural". En uno de esos estudios, se le mostraban a estudiantes de primaria vídeos de alguien jugando a un juego del estilo de "Pokemon", y se le preguntaba:

	"Imagínate que vas a programar un ordenador para que haga este vídeojuego. ¿Qué crees que le dirías al ordenador para que lo hiciera?".

Rara vez los participantes describían iteraciones como las de un bucle ``while``. Normalmente decía cosas como "Para todas las carpetas, yo haría..." o "Para cada uno de los personajes, haz..." Es muy común que se utilice la expresión hacer algo "para todo". Como hemos visto, podemos utilizar bucles ``for`` para casos como esos. Por ejemplo, *para cada uno de los elementos de una lista*. En general, los bucles ``for`` son mucho más parecidos al modo en que las personas hablamos en lenguaje natural sobre los bucles.

Pero es frecuente que los estudiantes de programación lleguen a una conclusión más práctica: 

	"Un bucle ``while`` puede hacer todo lo que hace un bucle ``for``, y además es más flexible. Lo aprenderé".

Mark Guzdial, uno de los autores de este libro, lo utilizaba para enseñar *Diseño Orientado a Objetos*  en segundo curso. Quería saber cuál era el nivel de los alumnos sobre programación antes de empezar el curso. Un año, les propuso el reto de escribir las tablas de multiplicar, tal como hemos visto hace poco en el libro. Utilizando un bucle ``for`` son tres líneas de código. De setenta y cinco estudiantes, solamente quince utilizaron un bucke ``for``. *Todos* los demás usaron un bucle ``while``. Con ``while`` son necesarias más líneas de código, y es más fácil cometer un error (muchos lo cometieron). Pero los estudiantes se sentían más *cómodos* con el bucle ``while``, porque es el tipo de bucle que más habían empleado hasta entonces. 

Comienza por utilizar en tus clases el bucle ``for``, como hemos hecho en el capítulo anterior. Será más fácil y más natural para tus alumnos. 

