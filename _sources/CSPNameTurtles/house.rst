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
	:prefix: csp-5-2-
	
.. highlight:: java
   :linenothreshold: 4

Pedro construye una casa
==============================

Vamos a combinar a hora el c�digo del cuadrado y el del tri�ngulo 
para crear un dibujo sencillo de una casa.

.. Note::
   El siguiente programa tiene l�neas en blanco alternadas con l�neas de c�digo. El ordenador ignora estas l�neas en blanco. Las a�adimos en los programas para agrupar las partes del c�digo que hacen algo concreto, como dibujar un cuadrado, en este caso. Normalmente estas agrupaciones van precedidas de un comentario (comienzan con el caracter ``#``), para indicar qu� hace esa parte del c�digo.

.. activecode:: Turtle_House
  :tour_1: "Section Tour"; 1-3: house-line1-3; 6-12: house-line5-11; 15: house-line13; 18-23: house-line18-23;
  :nocodelens:
  
  from turtle import *      # usa la librer�a de manejar tortugas
  space = Screen()          # crea el �rea para la tortuga (espacio)
  pedro = Turtle()          # crea la tortuga pedro
  
  # Dibuja un cuadrado
  pedro.forward(100)        # le ordena a pedro que avance 100 unidades
  pedro.right(90)           # gira 90 grados a la derecha
  pedro.forward(100)          # le ordena a pedro que avance 100  unidades
  pedro.right(90)           # gira 90 grados a la derecha
  pedro.forward(100)          # le ordena a pedro que avance 100  unidades
  pedro.right(90)           # gira 90 grados a la derecha
  pedro.forward(100)          # le ordena a pedro que avance 100  unidades
  
  # Coloca a pedro para dibujar el tejado
  pedro.right(90)
  
  # Dibuja el tejado
  pedro.forward(100)        # le ordena a pedro que avance 100  unidades

  pedro.right(-120)         # gira 120 grado a la IZQUIERDA
  pedro.forward(100)        # le ordena a pedro que avance 100  unidades
  pedro.right(-120)         # gira 120 grado a la IZQUIERDA
  pedro.forward(100)        # le ordena a pedro que avance 100  unidades
  pedro.right(-120)           # gira 120 grado a la IZQUIERDA

Imagina que quieres crear otro cuadrado incompleto en el tejado para dibujar una "chimenea".

.. image:: Figures/turtle-house.png

.. parsonsprob:: 5_2_1_Turtle_House

   Coloca los siguientes bloques de c�digo paa dibujar una casa y su chimenea, como en la imagen de arriba. Dibuja primero un cuadrado para el cuerpo de la casa, a continuaci�n dibuja el tejado, y finalmente dibuja la chimenea.

   -----
   from turtle import * 
   espacio = Screen()
   pedro = Turtle() 
   =====
   # Dibuja un cuadrado
   pedro.forward(100) 
   pedro.right(90) 
   pedro.forward(100) 
   pedro.right(90) 
   pedro.forward(100) 
   pedro.right(90) 
   pedro.forward(100) 
   =====
   # Coloca para dibujar el tejado
   pedro.right(90)
   =====
   # dibuja el tejado
   pedro.forward(100)   
   pedro.right(-120)   
   pedro.forward(100)   
   pedro.right(-120)   
   pedro.forward(100) 
   pedro.right(-120)  
   =====
   # Coloca para dibujar la chimenea
   pedro.right(-60)
   pedro.forward(40)
   pedro.setheading(90) 
   =====
   # Dibuja la chimenea
   pedro.pencolor("red")
   pedro.forward(30)
   pedro.right(90)
   pedro.forward(30)
   pedro.right(90)
   pedro.forward(30)
   pedro.right(90)



