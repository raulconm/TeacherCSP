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
	:prefix: csp-7-1-
	
.. highlight:: java
   :linenothreshold: 4

	
Repetir pasos
=====================================

..	index:
	single: variable
	single: index variable
	single: definite loop
	pair: statements; for

*Objetivos de aprendizaje:*

- Utilizar un bucle ``for`` para que el código se ejecute varias veces
- Utilizar ``range`` para crear una lista de números

Es habitual que haya que repetir pasos dentro de un proceso. Si estás preparando un bizcocho es muy posible que la receta indique que se añada un ingrediente y se mezcle cincuenta veces, o hasta que la masa sea uniforme. Puedes mezclar la masa esas cincuenta veces, pero ¿y si tuvieras que mezclarla mil veces? Seguramente necesitarías una máquina que lo hiciera. 

.. figure:: Figures/stirCake.jpg
    :height: 250px
    :align: center
    :alt: a cake mix that must be stirred
    :figclass: align-center

    Figura 1: Ingredientes de un bizcocho que hay que mezclar
    
..	index::
	single: bucle
	single: iteración

Los ordenadores nunca se cansan. Pueden repetir el mismo paso hasta el infinito sin mostrar signos de fatiga. Pueden ejecutar un programa ssin parar mientras tengan electricidad. Entonces, tiene que existir una manera de decirle al ordenador que haga las cosas una y otra vez. Los ordenadores saben cómo repetir pasos en un programa, y la forma en que lo hacen se llama habitualmente **bucle** o **iteración**. ¿Alguna vez se te ha pegado una canción y la has tenido sonando en la cabeza, repitiéndose todo el rato, como en un **bucle**?




