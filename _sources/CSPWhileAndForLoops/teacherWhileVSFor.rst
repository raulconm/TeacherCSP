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

	
|bigteachernote| Nota para el profesor: los bucles for son m�s naturales
================================================================

Algunos investigadores han estudiado la forma en que la gente describe los programas con un estilo "natural". En uno de esos estudios, se le mostraban a estudiantes de primaria v�deos de alguien jugando a un juego del estilo de "Pokemon", y se le preguntaba:

	"Imag�nate que vas a programar un ordenador para que haga este v�deojuego. �Qu� crees que le dir�as al ordenador para que lo hiciera?".

Rara vez los participantes describ�an iteraciones como las de un bucle ``while``. Normalmente dec�a cosas como "Para todas las carpetas, yo har�a..." o "Para cada uno de los personajes, haz..." Es muy com�n que se utilice la expresi�n hacer algo "para todo". Como hemos visto, podemos utilizar bucles ``for`` para casos como esos. Por ejemplo, *para cada uno de los elementos de una lista*. En general, los bucles ``for`` son mucho m�s parecidos al modo en que las personas hablamos en lenguaje natural sobre los bucles.

Pero es frecuente que los estudiantes de programaci�n lleguen a una conclusi�n m�s pr�ctica: 

	"Un bucle ``while`` puede hacer todo lo que hace un bucle ``for``, y adem�s es m�s flexible. Lo aprender�".

Mark Guzdial, uno de los autores de este libro, lo utilizaba para ense�ar *Dise�o Orientado a Objetos*  en segundo curso. Quer�a saber cu�l era el nivel de los alumnos sobre programaci�n antes de empezar el curso. Un a�o, les propuso el reto de escribir las tablas de multiplicar, tal como hemos visto hace poco en el libro. Utilizando un bucle ``for`` son tres l�neas de c�digo. De setenta y cinco estudiantes, solamente quince utilizaron un bucke ``for``. *Todos* los dem�s usaron un bucle ``while``. Con ``while`` son necesarias m�s l�neas de c�digo, y es m�s f�cil cometer un error (muchos lo cometieron). Pero los estudiantes se sent�an m�s *c�modos* con el bucle ``while``, porque es el tipo de bucle que m�s hab�an empleado hasta entonces. 

Comienza por utilizar en tus clases el bucle ``for``, como hemos hecho en el cap�tulo anterior. Ser� m�s f�cil y m�s natural para tus alumnos. 

