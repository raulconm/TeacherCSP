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

.. 	qnum::
	:start: 1
	:prefix: csp-4-1-

Asignar un nombre a una cadena
===================================

..	index::
	single: assignment
	pair: strings; assignment

*Objetivos de aprendizaje:*

- Crear una variable para almacenar un texto (una cadena)
- Sumar (unir o concatenar) cadenas para crear nuevas cadenas 
- Convertir un número en una cadena para concatenarla con otra
- Usar la notación de puntos para invocar funciones sobre los objetos
- Demostrar que las cadenas son inmutables (no cambian) 

Los ordenadores pueden representar *cualquier cosa* utilizando nombres. En el capítulo anterior vimos que podíamos darle un nombre a números (declarar una variable con un nombre y ocuparla con un número) y hacer después cálculos usando los nombres que le habíamos dado a esos números. También podemos nombrar cadenas y hacer cálculos entre ellas refiriéndonos a ellas por sus nombres. ¿Qué significa hacer un cálculo con una cadena? Bueno, en Python podemos utilizar el símbolo ``+`` para concatenar cadenas, como se muestra a continuación. 

.. activecode:: String_Assign
   :tour_1: "Line-by-line Tour"; 1: sa1-line1; 2: sa1-line2; 3: sa1-line3; 4: sa1-line4; 
   
   nombre = "Jorge"
   apellido = "Herranz"
   nombreCompleto = nombre + " " + apellido
   print(nombreCompleto)
   
.. note::
   Los espacios en blanco no se agregan automáticamente cuando sumamos dos cadenas. Si quieres que aparezca un espacio entre ellas tienes que indicarlo explíciamente añadiendo una cadena que contenga un único espacio en blanco ``" "`` como aparece arriba.
   
Concatenar cadenas de  caracteres y números
--------------------------------------------

Puedes imprimir tanto cadenas como números, y puedes concatenar cadenas por medio del ``+``, pero si intentas concatenar una cadena con un número te dará un error. El ordenador almacena en su memoria la cadena ``"5"`` y el número ``5`` de forma distinta, así que para concatenar el número ``5`` con una cadena es necesario convertir primero el número en cadena. Para convertir un número a cadena se emplea la función ``str(num)``.

.. activecode:: String_Convert
   :tour_1: "Line-by-line Tour"; 1: sa3-line1; 2: sa3-line2; 3: sa3-line3; 4: sa3-line4; 
   
   Juan = 5
   print("Juan")
   print(Juan)
   print("Juan" + " es " + str(Juan))
   
.. note::
   Observa que el ordenador hace algo diferente cuando imprime la cadena ``"Juan"`` que cuando imprime el valor de la variable ``Juan``. Imprimir la cadena ``"Juan"`` significa que imprime exactamente los caracteres incluidos en esa cadena. Recuerda que las cadenas están delimitadas por comillas simples o dobles, y que cuando se imprimen se muestran exactamente los caracteres que forman parte de la cadena. Cuando imprimes una variable se mostrará el *valor* de dicha variable. 
   
Podemos ahora mejorar el ejemplo del coste del viaje que hicimos antes, imprimiendo todo con una sola instrucción ``print``.

.. activecode:: Trip_Calculator2
   :tour_1: "Line by line tour"; 1: trp-line1; 2: trp-line2; 3: trp-line3; 4: trp-line4; 5: trp-line5; 6: trp2-line6;

   distancia = 948.1
   kpl = 16
   litros = distancia / kpl
   costePorLitro = 1.22
   costeDelViaje = litros * costePorLitro
   print("Coste del viaje de Malaga a Santander: "+str(costeDelViaje) + " euros")
   print(costeDelViaje)
  
Las cadenas son objetos
------------------------------------
   
..	index::
	single: dot-notation
	pair: programming; dot-notation

En Python las cadenas son objetos. Esto significa que puedes utilizar el conjunto de funciones que existen en Python para manipular cadenas. Puedes utilizar la **notación de puntos** para invocar las funciones que permiten manejar cadenas, como ``cadena.lower()``. La función ``lower()`` nos devolverá una cadena con todos los caracteres de la cadena original en minúsculas. La función ``capitalize()`` pondrá en mayúscula la primera letra de la cadena original.  

.. activecode:: String_Methods2
   :tour_1: "Line-by-line Tour"; 1: str2-line1; 2: str2-line2; 3: str2-line3; 4: str2-line4; 5: str2-line5;
   :nocodelens:
   
   frase = "ESTO ES UNA PRUEBA"
   mejor = frase.lower()
   print(mejor)
   mejorTodavia = mejor.capitalize() + "."
   print(mejorTodavia)
   

Las cadenas son inmutables
---------------------------

..	index::
	pair: string; immutable

Aunque podemos manipular una cadena para crear otra a partir de la primera, la cadena original es **inmutable**, no cambia. Fíjate que después de ejecutar el siguiente código, la cadena contenida en la variable ``frase`` no ha cambiado.    

.. activecode:: String_Immutable
   :tour_1: "Line-by-line Tour"; 1: str2-line1; 2: str2-line2; 3: str2-line3; 4: str2-line4; 5: str2-line5; 6: str2-line6;
   
   frase = "ESTO ES UNA PRUEBA"
   mejor = frase.lower()
   print(mejor)
   mejorTodavia = mejor.capitalize() + "."
   print(mejorTodavia)
   print(frase)
   
Aunque las cadenas no se pueden modificar, sí es posible  alterar el valor de una variable. De esta forma puedes indicarle al ordenador que olvide la cadena original y que establezca una nueva cadena como valor de la variable. 

.. activecode:: String_Reassign
   :tour_1: "Line-by-line Tour"; 1: sa2-line1; 2: sa2-line3; 3: sa2-line2; 4: sa2-line3;
   
   frase = "ESTO ES UNA PRUEBA"
   print(frase)
   frase = "Hola"
   print(frase)
   
.. mchoicemf:: 4_1_1_s1
   :answer_a: xyz
   :answer_b: xyxyz
   :answer_c: xy xy z
   :answer_d: xy z
   :answer_e: z
   :correct: b
   :feedback_a: s1 será igual a "xy" y otro "xy" y con una z al final.
   :feedback_b: s1 contiene el valor original, además de sí mismo, y una "z"
   :feedback_c: En una concatenación no se añaden los espacios.
   :feedback_d: En una concatenación no se añaden los espacios, y se debería agregar un "xy" adicional al principio.
   :feedback_e: s1 se definió inicialmente como "xy", así que la frase final será "xyxyz"

   ¿Cuál será el valor de la cadena s1 una vez ejecutado el siguiente fragmento de código?
   
   ::

     s1 = "xy"
     s2 = s1
     s1 = s1 + s2 + "z"
     
.. mchoicemf:: 4_1_2_s2
   :answer_a: Hey
   :answer_b: hey
   :answer_c: HEY
   :correct: c
   :feedback_a: Sería correcto si hubiésemos preguntado cuál es el valor de s3. ¿Cuál es el valor de s1?
   :feedback_b: Sería correcto si hubiésemos preguntado cuál es el valor de s2 después de ejecutar el código. ¿Cuál es el valor de s1?
   :feedback_c: Las cadenas son inmutables, lo que significa que no cambian. Cualquier función que modifica una cadena devuelve una nueva cadena.  Así pues s1 no cambia nunca, a menos que explícitamente le asignemos como valor una cadena diferentes.

   ¿Cuál es el valor de s1 después de ejecutar el siguiente código?
   
   :: 

     s1 = "HEY"
     s2 = s1.lower()
     s3 = s2.capitalize()


