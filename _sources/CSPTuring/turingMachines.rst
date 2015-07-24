..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

..  shortname:: Chapter2: What can Computers Do?
..  description:: Describes what a computer can do.

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-2-2-


M�quinas de Turing
==================================

..	index::
	single: Turing, Alan
	single: Turing Machine

El concepto de ordenador se utiliz� por primera vez en 1936, alrededor de doce a�os antes de que se construyera el primer ordenador electr�nico. `Alan Turing <http://es.wikipedia.org/wiki/Alan_Turing>`_, un brillante matem�tico, intentaba hallar la respuesta a una pregunta con la que los matem�ticos se peleaban a principios del siglo veinte, "�Cu�les son los l�mites de la matem�tica? �Qu� se puede computar por medio de las matem�ticas, y qu� hechos cient�ficos no se pueden calcular?" Turing ide� un dispositivo (una `M�quina de Turing <https://es.wikipedia.org/wiki/M%C3%A1quina_de_Turing>`_) que respond�a a esa questi�n: "Todo lo que se puede calcular matem�ticamente se puede tambi�n programar en una m�quina de Turing". 

.. figure:: Figures/Alan_Turing_photo.jpg
    :width: 200px
    :align: center
    :alt: A Photo of Alan Turing 
    :figclass: align-center
        
    Imagen 2: Foto de Alan Turing
    
.. mchoicemf:: 2_2_1_Turing_Q1
		   :answer_a: Corr�a durante m�s de sesenta kil�metros para asistir a las reuniones en Londres.
		   :answer_b: Propuso el Test de Turing para determinar si un ordenador era inteligente.   
		   :answer_c: Trabaj� en la Segunda Guerra Mundial para descifrar la m�quina Enigma.   
		   :answer_d: Fue al colegio en Oxford, Inglaterra. 
		   :correct: d
		   :feedback_a: Es cierto. Fue un gran corredor, incluso intent� participar en una Olimpiada.
		   :feedback_b: Es verdad. Dijo que si un ordenador pod�a hacerse pasar por persona, significaba que era inteligente.  
		   :feedback_c: Verdadero.  Winston Churchill dijo que Alan Turing hizo la mejor contribuci�n de una sola persona para ganar la Segunda Guerra Mundial.   
		   :feedback_d: Esto es falso.  Estudi� en el King's College de Cambridge y en la Universidad de Princeton.

		   Consulta el siguiente enlace para conocer mejor a  `Alan Turing <http://es.wikipedia.org/wiki/Alan_Turing>`_.  �Cu�l de las siguientes afirmaciones sore �l es **falsa**?


Los ordenadores de nuestro tiempo no funcionan como una M�quina de Turing, pero son equivalentes desde el punto de vista matem�tico. "Cualquier cosa que se puede calcular puede ser tambi�n programada en un ordenador electr�nico moderno". **TODOS** los ordenadores, desde los que se emplean en el microondas hasta los super-ordenadores que predicen el tiempo, todos tienen las mismas habilidades. Haz clic en el siguiente enlace para aprender m�s sobre `c�mo funcionan las M�quinas de Turin <http://maquinaturing.blogspot.com.es/p/funcionamiento-de-la-maquina-turing.html>`_

.. figure:: Figures/turing_machine.gif
    :width: 300px
    :align: center
    :alt: A Turing Machine 
    :figclass: align-center
        
    Imagen 3: Representaci�n de una M�quina de Turing

El alcance de esta afirmaci�n es muy amplio. Significa, por ejemplo, que es **posible** ejecutar cualquier programa en cualquier ordenador, aunque probablemente tengas que programar un mot�n para hacer que funcione. Pero esto no quiere decir que *todos* los problemas se tengan que resolver usando un ordenador.Una de las cosas m�s importantes que Turing prob� era que **algunos problemas no pod�an resolverse utilizando un ordenador, y nunca ser� posible hacerlo**.

La M�quina de Turing no sab�a realmente nada sobre n�meros, lo cu�l es sorprendente para un dispositivo capaz de hacer cualquier operaci�n matem�tica. En su lugar, simplemente hac�a marcas en una cinta de papel, y despu�s las *contaba* para hacer los c�lculos. En realidad, los ordenadores electr�nicos son bastante tontos. S�lo *cuentan* utilizando patrones de voltajes a trav�s de un cable (por ejemplo, "apagado, encendido, apagado, apagado" es la representaci�n del n�mero *4* en sistema binario). Pero nosotros, las personas, no queremos tener que utilizar patrones como este, as� que hemos programado dentro de los ordenadores las operaciones matem�ticas fundamentales.

..	index::
	single: abstraction
	
Cuando utilizas un ordenador ya dispones de todas las habilidades y funciones que otros han programado. Tu ordenador ya sabe c�mo manejar los n�meros y las operaciones matem�ticas, y tambi�n otras muchas cosas. Pero sin embargo, por debajo, en el nivel m�s b�sico, incluso los super-ordenadores m�s grandes, caros y potentes no pueden resolver los problemas mejor de lo que lo hace una M�quina de Turing. **Todos los ordenadores son ex�ctamente iguales respecto a lo que pueden hacer**. 

.. mchoicemf:: 2_2_2_Computers_Q1
		   :answer_a: Hab�a mujeres computadoras.
		   :answer_b: Puedes fabricar un ordenador con piezas de construcci�n para ni�os.     
		   :answer_c: Los ordenadores pueden resolver cualquier problema.   
		   :answer_d: Los ordenadores usan secuencias de voltajes en un cable para representar n�meros 
		   :correct: c
		   :feedback_a: Verdadero. Busca m�s informaci�n en las computadoras de Harvard.  
		   :feedback_b: Es cierto. Algunos estudiantes del MIT lo hicieron en 1980.   
		   :feedback_c: Falso. Turing afirm� que hay problemas que un ordenador no puede resolver.  
		   :feedback_d: Verdadero. Los ordenadores representan n�meros por medio patrones de encendido y apagado en un cable.  

		   �Cu�l de las siguientes afirmaciones sobre los ordenadores es *falsa*?
	
..	index::
	single: programming language
	pair: programming; languages
	
Un **lenguaje de programaci�n** (Como *Java* o *Python*), que es el lenguaje que te permite darle instrucciones a un ordenador, puede hacer lo mismo que una m�quina de Turing (ni m�s ni menos). Una herramienta de programaci�n como `Alice <http://www.alice.org>`_ o `Scratch <http://scratch.mit.edu>`_ puede hacer *la mayor�a* de las cosas que hace una m�quina de Turing, pero no todo. **Con Python puedes programar cualquiera de las cosas que puede hacer una m�quina de Turing**.




