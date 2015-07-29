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
	:prefix: csp-3-6-

.. highlight:: java
   :linenothreshold: 4

La velocidad del ketchup
========================

Vamos a calcular el tiempo que tardaría el ketchup en rebosar de una mesa. Imaginemos para ello que tenemos una mesa normal, de 1,5 metros de largo, y que comenzamos a derramar sobre ella una cantidad suficiente de ketchup. ¿Cuánto tiempo tardaría el ketchup en alcanzar el otro lado de la mesa y caer al suelo? Para simplificar, vamos a ignorar la física avanzada y el ángulo de la mesa, y comenzaremos considerando que la velocidad media a la que se desplaza el ketchup es de 0,045 kilómetros por hora.   

.. figure:: Figures/ketchup.jpg
    :width: 200px
    :align: center
    :alt: A picture of ketchup dripping from a bottle
    :figclass: align-center

    Imagen 2: Velocidad de una gota de ketchup

.. codelens:: Ketchup_Speed

   velKPH = .045            # Velocidad del ketchup en Km/hora
   CPK = 100000.0           # Centímetros en 1 kilómetro  
   velCPH = velKPH * CPK    # Velocidad ketchup en cm\hora  
   MPH = 60                 # Minutos en 1 hora 
   velCPM = velCPH / MPH    # Velocidad ketchup en cm\minuto
   print("Velocidad del ketchup en centrímetros por minuto:")
   print(velCPM)
   print("Minutos para recorrer los 150 cm. de mesa:")
   print(150 / velCPM)

   
A continuación veamos un nuevo tipo de problema. A la izquierda se muestra el código del programa separado en bloques desordenados. Para resolverlo tienes que arrastrar los bloques a la parte derecha y colocarlos en el orden correcto. Observa por favor el siguiente vídeo par ver una demostración.
   
**Haz clic en el icono de reproducir para ver el vídeo.**
   
.. video:: parsons
   :controls:
   :thumb: ../_static/MixedUpCodeVideoThumb.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/MixedUpCode.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/MixedUpCode.webm

.. parsonsprob:: 3_6_1_Ketchup_Speed

   El programa siguiente calcula la velocidad del ketchup en centímetros por <i>segundo</i>. Arrastra los bloques desde la izquierda y colócalos a la derecha en el orden correcto. Pulsa el botón <i>Check Me</i> para comprobar si lo has hecho correctamente.</p>
   -----
   velKPH = .045
   CPK= 100000.0
   velCPH = velKPH * CPK    
   =====
   MPH = 60  #mins por hora
   velCPM = velCPH / MPH    
   =====
   SPM = 60  #segs. por minuto
   velCPS = velCPM / SPM
   =====
   print("Velocidad en cm. por segundo:")
   print(velCPS)



