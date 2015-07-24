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


Máquinas de Turing
==================================

..	index::
	single: Turing, Alan
	single: Turing Machine

El concepto de ordenador se utilizó por primera vez en 1936, alrededor de doce años antes de que se construyera el primer ordenador electrónico. `Alan Turing <http://es.wikipedia.org/wiki/Alan_Turing>`_, un brillante matemático, intentaba hallar la respuesta a una pregunta con la que los matemáticos se peleaban a principios del siglo veinte, "¿Cuáles son los límites de la matemática? ¿Qué se puede computar por medio de las matemáticas, y qué hechos científicos no se pueden calcular?" Turing ideó un dispositivo (una `Máquina de Turing <https://es.wikipedia.org/wiki/M%C3%A1quina_de_Turing>`_) que respondía a esa questión: "Todo lo que se puede calcular matemáticamente se puede también programar en una máquina de Turing". 

.. figure:: Figures/Alan_Turing_photo.jpg
    :width: 200px
    :align: center
    :alt: A Photo of Alan Turing 
    :figclass: align-center
        
    Imagen 2: Foto de Alan Turing
    
.. mchoicemf:: 2_2_1_Turing_Q1
		   :answer_a: Corría durante más de sesenta kilómetros para asistir a las reuniones en Londres.
		   :answer_b: Propuso el Test de Turing para determinar si un ordenador era inteligente.   
		   :answer_c: Trabajó en la Segunda Guerra Mundial para descifrar la máquina Enigma.   
		   :answer_d: Fue al colegio en Oxford, Inglaterra. 
		   :correct: d
		   :feedback_a: Es cierto. Fue un gran corredor, incluso intentó participar en una Olimpiada.
		   :feedback_b: Es verdad. Dijo que si un ordenador podía hacerse pasar por persona, significaba que era inteligente.  
		   :feedback_c: Verdadero.  Winston Churchill dijo que Alan Turing hizo la mejor contribución de una sola persona para ganar la Segunda Guerra Mundial.   
		   :feedback_d: Esto es falso.  Estudió en el King's College de Cambridge y en la Universidad de Princeton.

		   Consulta el siguiente enlace para conocer mejor a  `Alan Turing <http://es.wikipedia.org/wiki/Alan_Turing>`_.  ¿Cuál de las siguientes afirmaciones sore él es **falsa**?


Los ordenadores de nuestro tiempo no funcionan como una Máquina de Turing, pero son equivalentes desde el punto de vista matemático. "Cualquier cosa que se puede calcular puede ser también programada en un ordenador electrónico moderno". **TODOS** los ordenadores, desde los que se emplean en el microondas hasta los super-ordenadores que predicen el tiempo, todos tienen las mismas habilidades. Haz clic en el siguiente enlace para aprender más sobre `cómo funcionan las Máquinas de Turin <http://maquinaturing.blogspot.com.es/p/funcionamiento-de-la-maquina-turing.html>`_

.. figure:: Figures/turing_machine.gif
    :width: 300px
    :align: center
    :alt: A Turing Machine 
    :figclass: align-center
        
    Imagen 3: Representación de una Máquina de Turing

El alcance de esta afirmación es muy amplio. Significa, por ejemplo, que es **posible** ejecutar cualquier programa en cualquier ordenador, aunque probablemente tengas que programar un motón para hacer que funcione. Pero esto no quiere decir que *todos* los problemas se tengan que resolver usando un ordenador.Una de las cosas más importantes que Turing probó era que **algunos problemas no podían resolverse utilizando un ordenador, y nunca será posible hacerlo**.

La Máquina de Turing no sabía realmente nada sobre números, lo cuál es sorprendente para un dispositivo capaz de hacer cualquier operación matemática. En su lugar, simplemente hacía marcas en una cinta de papel, y después las *contaba* para hacer los cálculos. En realidad, los ordenadores electrónicos son bastante tontos. Sólo *cuentan* utilizando patrones de voltajes a través de un cable (por ejemplo, "apagado, encendido, apagado, apagado" es la representación del número *4* en sistema binario). Pero nosotros, las personas, no queremos tener que utilizar patrones como este, así que hemos programado dentro de los ordenadores las operaciones matemáticas fundamentales.

..	index::
	single: abstraction
	
Cuando utilizas un ordenador ya dispones de todas las habilidades y funciones que otros han programado. Tu ordenador ya sabe cómo manejar los números y las operaciones matemáticas, y también otras muchas cosas. Pero sin embargo, por debajo, en el nivel más básico, incluso los super-ordenadores más grandes, caros y potentes no pueden resolver los problemas mejor de lo que lo hace una Máquina de Turing. **Todos los ordenadores son exáctamente iguales respecto a lo que pueden hacer**. 

.. mchoicemf:: 2_2_2_Computers_Q1
		   :answer_a: Había mujeres computadoras.
		   :answer_b: Puedes fabricar un ordenador con piezas de construcción para niños.     
		   :answer_c: Los ordenadores pueden resolver cualquier problema.   
		   :answer_d: Los ordenadores usan secuencias de voltajes en un cable para representar números 
		   :correct: c
		   :feedback_a: Verdadero. Busca más información en las computadoras de Harvard.  
		   :feedback_b: Es cierto. Algunos estudiantes del MIT lo hicieron en 1980.   
		   :feedback_c: Falso. Turing afirmó que hay problemas que un ordenador no puede resolver.  
		   :feedback_d: Verdadero. Los ordenadores representan números por medio patrones de encendido y apagado en un cable.  

		   ¿Cuál de las siguientes afirmaciones sobre los ordenadores es *falsa*?
	
..	index::
	single: programming language
	pair: programming; languages
	
Un **lenguaje de programación** (Como *Java* o *Python*), que es el lenguaje que te permite darle instrucciones a un ordenador, puede hacer lo mismo que una máquina de Turing (ni más ni menos). Una herramienta de programación como `Alice <http://www.alice.org>`_ o `Scratch <http://scratch.mit.edu>`_ puede hacer *la mayoría* de las cosas que hace una máquina de Turing, pero no todo. **Con Python puedes programar cualquiera de las cosas que puede hacer una máquina de Turing**.




