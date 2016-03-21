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
	:prefix: csp-6-7-
	
.. highlight:: java
   :linenothreshold: 4


Utilizar una librería para imágenes
===================================

En el ejemplo donde  procesábamos una imagen utilizábamos ``from image import *``. Esta instrucción hacía que estuvieran accesibles las funcciones ``getPixels()`` y ``getRed()``. También se podría definir una nueva función que devolviera un color nuevo, o un procedimiento que modificara la imagen.  

.. raw:: html

    <img src="../_static/arch.jpg" id="arch.jpg" >
    
.. activecode:: Image_Functions
    :tour_1: "Important Lines Tour"; 1,4,7,11,15,18: timg2-line1_4_7_11_15_18; 2: timg2-line2; 5: timg2-line5; 8-9: timg2-line8-9; 12-13: timg2-line12-13; 16: timg2-line16; 19-20: timg2-line19-20;
    :nocodelens:

    # UTILIZA LA LIBRERIA DE IMÁGENES 
    from image import *
    
    # CREA UNA IMAGEN DESDE UN ARCHIVO
    img = Image("arch.jpg")

    # BUCLE QUE RECORRE TODOS LOS PIXELS
    pixels = img.getPixels()
    for p in pixels:
        
        # MODIFICA EL COLOR DEL PIXEL
        r = p.getRed()
        p.setRed(r * 0.5)
            
        # ACTUALIZA LA IMAGEN
        img.updatePixel(p)
            
    # MUESTRA EL RESULTADO
    win = ImageWin(img.getWidth(),img.getHeight())
    img.draw(win)
    
La instrucción ``for p in pixels`` de la línea 9 sirve para ir recorriendo todos los pixels de la imagen, y cambiar el valor del rojo para cada pixel. Profundizaremos sobre los bucles (ejecutar pasos repetidamente) en el capítulo siguiente.

.. mchoicemf:: 6_7_1_Image_Functions_Q1
   :answer_a: Establece el valor del componente rojo del pixel actual a la mitad del valor original.  
   :answer_b: Establece el valor del componente rojo del pixel actual al doble del valor original.
   :answer_c: Establece el valor del componente rojo del pixel actual a cinco veces el valor original.
   :answer_d: Establece el valor del componente rojo del pixel actual a 0,5.  
   :correct: a
   :feedback_a: Multiplicar por 0,5 es lo mismo que dividir por 2.  
   :feedback_b: Sería cierto si fuese r * 2, en lugar de r * 0.5
   :feedback_c: Sería cierto si fuese r * 5, en lugar de r * 0.5
   :feedback_d: Sería cierto si fuese 0.5 en lugar de r * 0.5
   
   ¿Qué hace la instrucción ``p.setRed(r * 0.5)``?


Esta capacidad para asignar nombres a funciones y a procedimientoss, y a conjuntos de nombres y procedimientos, y a cualquier otra cosa o conjunto de cosas en un ordenador, es muy potente. Permite crear **abstracciones** que facilitan el uso y la programación de los ordenadores. En un capítulo possterior hay más de todo esto.
