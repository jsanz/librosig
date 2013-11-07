.. _conceptos_basicos_visualizacion:

**********************************************************
Conceptos básicos de visualización y representación
**********************************************************

Puesto que tratamos la visualización de la información geográfica, resulta necesario conocer algunas de las ideas fundamentales acerca del lenguaje visual para usar este adecuadamente. Con estas, sabremos cómo hacer mejores representaciones visuales para transmitir una información dada, aprovechando las propiedades de los elementos del lenguaje de un modo óptimo. Los conceptos que se detallan en este capítulo pueden aplicarse a cualquier tipo de representación visual, por lo que podremos posteriormente trasladarlos al contexto de la cartografía.


Introducción
=====================================================

Cuando visualizamos cualquier tipo de información geográfica, ya sea a través de un mapa clásico o de algún elemento gráfico en la pantalla de un ordenador, estamos utilizando un lenguaje visual para transmitirla. Del mismo modo que al hablar empleamos un lenguaje oral y al escribir un lenguaje escrito, siempre que plasmemos la información geográfica en una serie de elementos visuales estaremos empleando este lenguaje visual.

Existen muchas similitudes entre el lenguaje visual y el lenguaje que utilizamos cada día para comunicarnos, comunes todas ellas a cualquier forma de lenguaje. Por una parte, disponemos de una serie de elementos básicos que podemos usar, que son como las palabras con las que formamos frases y expresamos ideas. Estas se combinan de acuerdo con unas normas y siguiendo esquemas definidos que conocen tanto el creador del mensaje como el receptor, y sin los cuales no seria posible establecer la comunicación. Por otra, el conocimiento y manejo adecuado de todos estos elementos define nuestra capacidad de emplear el lenguaje y expresar correctamente aquello que queremos transmitir.

Al igual que en el lenguaje hablado, y por su carácter simbólico, el lenguaje visual implica la existencia de unas limitaciones. Es decir, no podemos expresar todo aquello que tratamos de representar, y un mapa nunca puede contener y transmitir fielmente toda la realidad de una zona o de un fenómeno espacial dado. Sin embargo, un correcto uso del lenguaje permite comunicar gran cantidad de información y hacer de este una herramienta de gran utilidad, más allá de sus limitaciones, o incluso aprovechando estas para su propio beneficio.

El estudio de los signos de un lenguaje constituye lo que se conoce como *semiología*. En el caso de los elementos del lenguaje visual, encontramos una *semiología gráfica*, tal y como la definió el cartógrafo francés Jacques Bertin, pionero en este campo  :cite:p:`Bertin1987Pompidou`. Esta semiología trata los signos del lenguaje visual y la gramática de estos, definiendo una lingüística visual que nos ayuda a comprender cómo una representación gráfica dada cumple su propósito de transmitir la información en base a la cual se crea.

Detallando las ideas de Bertin, en este capítulo veremos algunos aspectos fundamentales acerca del lenguaje visual que nos permitirán conocer sus propiedades y la forma en que sus elementos pueden emplearse de forma efectiva para la comunicación. Aplicando estos al caso particular de representar y visualizar información cartográfica, expandiremos este en el próximo capítulo para obtener un lenguaje cartográfico, fundamental para la creación de mapas.


Las variables visuales
=====================================================

Cada lenguaje tiene sus propiedades particulares y permite expresar unas u otras ideas de distintas maneras. Por ejemplo, podemos plasmar la música en una partitura, utilizando un lenguaje de signos musicales. Este lenguaje musical\footnote{Entiéndase que hablamos aquí de ese lenguaje de signos sobre un papel y no del lenguaje musical relativo a una forma de expresión a través del ritmo, el tono, etc.} permite recoger y transmitir una canción a través de una partitura, expresando mediante un conjunto de símbolos las distintas notas que la componen, su duración o los elementos expresivos que deben incorporarse en la interpretación de esta. Un músico que conozca este lenguaje puede interpretar una pieza gracias a que la música le llega a través de esos símbolos, siendo la partitura el medio de comunicación entre el interprete y el compositor o quien haya transcrito dicha pieza. 

Aunque dos personas conozcan a la perfección el lenguaje musical, no podrán, sin embargo, transmitirse mediante sus símbolos y sus reglas algo como una formula matemática o un poema. El lenguaje matemático o el lenguaje oral son los adecuados para transmitir este tipo de mensajes, pero no el lenguaje musical, que tiene limitaciones en ese sentido.

Puesto que nuestro objetivo a lo largo de los capítulos de esta parte del libro es ser capaces de crear mapas y otros elementos visuales que transmitan la información geográfica, debemos estudiar qué clase de información vamos a transmitir y, sobre todo, qué nos permite transmitir el lenguaje visual. Del mismo modo que sabemos que los símbolos de nuestro lenguaje musical (pentagrama, figuras, etc.) no son capaces de transmitir una formula matemática, debemos ver si los elementos del lenguaje visual van a ser capaces de, por ejemplo, transmitir el patrón de distribución de un fenómeno en el espacio, las diferencias entre dos zonas distintas o la relación entre los valores de una variable en dos puntos. Además, debemos ver cómo emplearlos para que esa información se transmita de la mejor manera posible, ya que existen diversas propiedades de los elementos visuales que podemos emplear, siendo más adecuadas unas u otras según sea la circunstancia.

Estas propiedades conforman lo que se conoce como *variables visuales*, y se aplican a los elementos básicos de la representación, que son aquellos objetos geométricos de que se compone esta. Las variables visuales permiten diferenciar unos de otros y asignarles unas ciertas características, susceptibles a su vez de ser interpretadas junto al propio significado que el objeto pueda tener. Dados dos elementos, estos pueden diferenciarse por las siguientes variables (Figura:num:`#figvariablesvisuales`).


* Posición
* Tamaño
* Forma
* Textura
* Color
* Orientación


.. _figvariablesvisuales:

.. figure:: VariablesVisuales.*
	:width: 650px
	:align: center

	Ejemplo de uso de las distintas variables visuales. De izquierda a derecha: posición, forma, tamaño, tono, valor, textura, y orientación


Todas ellas constituyen las variables visuales, que estudiaremos seguidamente en detalle. El color, como explicaremos, se divide en dos variables visuales independientes: valor y tono.

Las variables visuales se aplican de forma distinta en función del tipo de elemento que queramos simbolizar, por lo que detallaremos su uso para las tres clases de símbolos que podemos incorporar en un mapa: puntuales, lineales y de superficie.

Posición
--------------------------------------------------------------

La posición constituye un caso particular de variable visual a la hora de emplearla en la creación de cartografía, ya que viene fuertemente condicionada por el hecho de que todo aquello que representamos tiene una posición en el espacio y, por tanto, ha de tener una posición concreta en el mapa. Mientras que en cualquier otro tipo de gráfico la posición puede modificarse a voluntad para transmitir algún tipo de información, tal y como haremos con las restantes variables visuales, en el caso de un mapa la posición ya está asociada a una información que ha de transmitir: la información sobre la posición real en el espacio geográfico de aquel objeto que se simboliza.

Aunque el cartógrafo puede en determinadas ocasiones variar la posición de algunos elementos (por ejemplo, para mejorar la legibilidad del mapa), siempre está supeditado a la corrección cartográfica, y no posee libertad para alterar esta de cualquier modo. Por ello, el uso de la posición como variable visual está muy restringido en el caso de un mapa, y no se emplea. Su escasa aplicación en ese sentido queda patente en el hecho de que en algunos textos no se menciona junto a las restantes variables visuales, detallándose por separado como un elemento distinto.


Forma
--------------------------------------------------------------

La forma viene definida por el perímetro exterior del objeto. Esto no implica que únicamente se pueda aplicar la forma a símbolos de superficie, ni tampoco que se debe tratar de un perímetro cerrado como el de una forma poligonal.

La forma se aplica fundamentalmente a los símbolos puntuales, situando un símbolo de una forma dada sobre las coordenadas exactas del punto a representar. Su aplicación a símbolos lineales es difícil y no se da, mientras que en el caso de aplicarse sobre símbolos de superficie requiere la alteración de los polígonos representados (por ejemplo, que tracen los límites de países), dando lugar a una representación imprecisa, al menos en lo que al contorno del polígono respecta. Esto se produce únicamente en el caso de los denominados *cartogramas*, un tipo particular de mapas que veremos en el próximo capítulo.

Tamaño
--------------------------------------------------------------

El tamaño se refiere a la dimensión del símbolo. Para el caso de símbolos puntuales, puede aplicarse sin más que hacer más grande o pequeño el símbolo en sí. En el caso de líneas, el grosor de estas constituye la forma de aplicar la variable tamaño. Al igual que sucedía con la forma, en las superficies va a implicar la modificación de estas, por lo que se emplea únicamente en los cartogramas. Otra forma de aplicar el tamaño a los símbolos superficiales es hacerlo sobre la textura con la que estos se rellenan, usando un único patrón con diferentes tamaños en sus tramas (Figura :num:`#figtamanotexturas`).


.. _figtamanotexturas:

.. figure:: Texturas.*
	:width: 550px
	:align: center

	Uso del tamaño en símbolos de superficie mediante texturas.



El tamaño condiciona la percepción de otras variables visuales, especialmente cuando se trata de tamaños pequeños. Un punto muy pequeño o una línea demasiado fina no van a permitir la aplicación de, por ejemplo, el tono o el valor, o al menos no del mismo modo que con un tamaño mayor, ya que la percepción de estas variables será más difícil.


Color
--------------------------------------------------------------

La variable color es la más importante de todas las variables visuales, y la que a su vez requiere un grado mayor de detalle en su exposición, debido a la que complejidad que presenta y a las posibilidades que ofrece\footnote{Si estas leyendo una copia impresa de este libro, es posible adquirir esta tanto en versión a color como en versión en blanco y negro. En caso de usar esta última, no vas a poder apreciar correctamente algunas de las imágenes de este capítulo, por lo que te recomiendo acudir a la versión digital del libro (recuerda, este es un libro libre y puedes obtener esa versión de forma gratuita en el página Web del libro), al menos para este capítulo, o, mejor aún, para toda esta parte dedicada a la visualización. Otros capítulos en otras partes del libro también presentan figuras en color, pero pueden ser interpretadas igualmente en blanco y negro. En las de este, no obstante, el uso del color es más relevante y será mejor utilizar una versión con figuras a todo color, ya sea impresa o digital.}.

Existen muchas formas de representar y crear un color, a través de los denominados *espacios de color*. De cara a su uso como variable visual en el contexto de este capítulo, resulta de especial interés el uso del espacio de color HSV, en el cual un color se define mediante un espacio de coordenadas cilíndrico, según lo mostrado en la figura :num:`#fighsv`.  

.. _fighsv:

.. figure:: HSV.*
	:width: 450px
	:align: center

	Espacio de color HSV explicando el significado de las componentes tono, valor y saturación (adaptado de Wikipedia).


Tres son las componentes de un color, las cuales establecen sus coordenadas en el cilindro: tono, valor y saturación.

El tono es lo que en el lenguaje común denominaríamos color, es decir el nombre del color, por ejemplo verde, rojo o amarillo. Está relacionado con la longitud de onda de la luz, y distintas longitudes de onda producen un efecto perceptivo distinto, haciendo que distingamos así los diferentes colores. En el cilindro del espacio de color, el tono viene marcado por el ángulo del vector definido por la posición del color y el eje central, sobre el plano perpendicular a dicho eje.

El tono puede verse alterado por los tonos del entorno, especialmente en símbolos de pequeño tamaño. Aunque es una variable para la que la percepción humana tiene gran sensibilidad, en los símbolos pequeños puede ser difícil de identificar y pueden producirse una falsa percepción si comparten espacio con otras más grandes de un tono distinto. Por ejemplo, al trazar una linea con un grosor fino que atraviesa una serie de polígonos de distintos colores, el tono de esta se percibirá como distinto en cada uno de esos polígonos por el efecto que sus colores causan como colores de fondo.

Por su parte, el valor indica la claridad del color. Un tono azul puede ser más claro o más oscuro sin dejar de ser azul. Esa variación que se produce es una variación del valor del color. En el caso de usar una tinta de un color dado, la mezcla de esta con una pintura blanca produce una disminución del valor, aclarándose progresivamente según añadimos más de esta última en la mezcla. A la hora de imprimir se hace uso de tramas más o menos densas para modificar el valor, sin modificar así la tinta. Según el espacio en blanco que se deja entre los puntos de tinta impresos, se consigue la apariencia de un color de mayor o menor valor. El valor se define en el cilindro de coordenadas como la altura del color sobre el eje central.

La capacidad de diferenciar dos símbolos con valor distinto varía en función del tipo de símbolo. Así, es mayor en el caso de símbolos de superficie, mientras que en el caso de símbolos puntuales y lineales está relacionada con el tamaño. Si el punto es muy pequeño o la línea muy delgada, es más difícil apreciar el valor y, por tanto, comparar este con otro o extraer la información que mediante esa variable visual se intenta transmitir.

La saturación, por último, expresa la pureza relativa del color. Depende del número de distintas longitudes de onda que aparecen en un color dado. A medida que disminuye la saturación, el color va pareciendo más grisáceo, y el número de longitudes de onda es mayor. En el cilindro del espacio de color queda definido por la distancia del color al eje central.

En lo que al color como variable visual respecta, cada una de estas componentes de un color son a su vez variables visuales, y como tales pueden emplearse para simbolizar los distintos elementos de un mapa. En la práctica, el tono y el valor son utilizadas muy frecuentemente, pero la saturación tiene una utilidad muy limitada, por lo que es muy infrecuente su uso. En lo sucesivo, por tanto, trataremos el color no como una única variable visual sino como dos distintas: valor y tono.

Si tienes un programa de dibujo o de edición de imágenes, puedes experimentar construyendo colores según sus componentes, usando el habitual selector de colores. Si no, prueba en la siguiente dirección Web, donde encontrarás un selector de colores *on--line*: \url{http://www.dgx.cz/tools/colormixer/stripe.php?hsv=space\%20color}.

La figura :num:`#figselectorcolores` muestra el aspecto de un selector de colores, en el que puede verse cómo estos pueden definirse mediante sus componentes tono (H), saturación (S) y luminosidad (L). Aunque no es exactamente el mismo concepto, la luminosidad cumple el papel del valor en este contexto, y este modelo (HSL en lugar de HSV) es el que encontramos con carácter habitual en las herramientas de este tipo para definir un color.

.. _figselectorcolores:

.. figure:: SelectorColores.*
	:width: 550px
	:align: center

	Selector de colores mediante sus componentes tono (H), saturación (S) y luminosidad (L). La componente de la parte inferior es la denominada *alpha*, que indica la transparencia del color.



Textura
--------------------------------------------------------------

La textura hace referencia al relleno de un símbolo mediante algún patrón. Empleando patrones distintos se produce una diferenciación en los símbolos correspondientes. 

En el caso de los símbolos puntuales, la textura requiere que estos tengan un tamaño suficiente para que pueda apreciarse el patrón que constituye cada una de las texturas. Este tamaño mínimo requerido es mayor que en el caso de emplear el tono o el valor.

En el caso de líneas, entendemos como textura el uso de guiones y espacios en blanco que dan lugar a un patrón de discontinuidad, como se muestra en la figura :num:`#figtexturas`.  No obstante, esta discontinuidad es una desventaja a la hora de representar un elemento lineal, ya que implica que una parte de él no va a representarse. Dependiendo del significado de aquello que representemos, el uso de texturas en elementos lineales puede no ser lo más recomendable a la hora de crear un mapa. Puede emplearse otro tipo de texturas para formar líneas, *rellenando* estas si tienen un grosor considerable, pero su uso no se recomienda.

Las texturas se aprovechan plenamente sobre los símbolos de superficie, ya que la mayor dimensión de estos permite una percepción completa y una interpretación mucho más sencilla, al igual que ocurría en el caso del valor.

.. _figtexturas:

.. figure:: Texturas_lineas.*
	:width: 650px
	:align: center

	Aplicación de la variable visual textura a los símbolos lineales.



Orientación
--------------------------------------------------------------

La última variable visual es la orientación. Se aplica sobre los símbolos puntuales, siempre que estos no presenten simetrías que impidan percibir correctamente la orientación. Por ejemplo, para el caso del círculo, resulta obvio que no tiene sentido aplicar la orientación como variable visual. Los símbolos compuestos por formas geométricas son adecuados para emplear la orientación, mientras que los símbolos pictóricos no responden de igual forma y producen en la representación sensación de desequilibrio. Se recomienda, por tanto, emplear esta variable únicamente con los primeros.

Puede aplicarse también sobre los símbolos de superficie a través de la textura, variando la orientación de esta. Sobre las líneas, no obstante, su aplicación no es posible. Puede emplearse en caso de líneas con textura, pero esto requiere un ancho excesivo para una correcta percepción.

Las propiedades de las variables visuales
=====================================================

Las variables que acabamos de ver son ahora nuestras herramientas que emplearemos para simbolizar la información geográfica y sabemos ya cómo aplicarlas. Lo que no hemos visto aún es qué capacidades tienen y qué podemos simbolizar mediante ellas, y este es realmente el aspecto clave sobre el que deberemos decidir posteriormente cuando nos dispongamos a crear un mapa, para así seleccionar la variable visual más adecuada en función de aquello que queramos representar.

Se distinguen 4 propiedades básicas que una variable visual puede presentar:


* Asociativa. Una variable visual presenta la propiedad asociativa si al ser aplicada no aumenta ni disminuye la visibilidad de un elemento. Es decir, cuando en función de esa variable visual no puede asignársele más o menos importancia a este.
* Selectiva. La propiedad selectiva la presentan aquellas variables visuales que, al ser aplicadas, generan distintas categorías de símbolos.
* Ordenada. Cuando una variable visual puede emplearse para representar un orden, se dice que presenta la propiedad ordenada.
* Cuantitativa. Cuando, además del orden, una variable puede mostrar cantidades o proporciones, entonces se dice que posee la propiedad cuantitativa.


El orden en que se han presentado estas propiedades no es casual, ya que están ordenadas dando lugar a lo que Bertin denomina *niveles de organización*. La propiedad asociativa se sitúa en el nivel más bajo, mientras que la cuantitativa ocupa el más alto. El nivel de organización de las variables visuales tiene importancia a la hora de combinar varias de ellas en un símbolo, como veremos más adelante. Asimismo, y como detallaremos en el capítulo siguiente, el nivel de organización define qué tipo de información podemos transmitir con una variable visual.

Para ver más exactamente el significado de estas propiedades, estudiemos con detalle la figura :num:`#figpropiedadesvariablesvisuales`, que muestra diferentes representaciones de un conjunto de símbolos (en este caso, símbolos puntuales) en los que en cada caso se ha utilizado únicamente una variable visual.

.. _figpropiedadesvariablesvisuales:

.. figure:: PropiedadesVariablesVisuales.*
	:width: 650px
	:align: center

	Representación de un conjunto de símbolos aplicando de forma individual las distintas variables visuales.


Comenzando con la propiedad asociativa, vemos que a excepción del tamaño y el tono, las demás variables visuales no hacen que los elementos presenten una preponderancia en la imagen. No existen una orientación que podamos definir como más importante, ni tampoco un color. Lo mismo sucede con la textura, la forma y la posición. Podemos emplear una u otra forma, o una u otra textura, y con ello no conseguiremos llamar más la atención sobre un elemento en cuestión. 

Con el tamaño, sin embargo, resulta claro que mayor tamaño implica un papel destacado dentro de la información que transmite el mapa. De igual modo, un mayor valor (un color más oscuro) da sensación de mayor definición, y centra la atención de observador sobre el elemento de un modo muy superior a como lo hace un valor bajo.

Respecto a la propiedad selectiva, diremos que una variable visual la presenta si de un vistazo podemos rápidamente seleccionar los elementos que pertenecen a un determinado grupo, identificados estos mediante dicha variable visual. El caso más claro de propiedad selectiva lo presenta el tono. Podemos rápidamente quedarnos solo con los elementos amarillos o con los rojos. Aunque no de un modo tan claro, todas las restantes variables presentan igualmente esta propiedad, a excepción de la forma. La forma no permite que los elementos se agrupen de modo espontáneo en familias, y su validez en este sentido está muy ligada a la complejidad de dicha forma.

La propiedad ordenada la presentan aquellas variables que permiten establecer un orden. Tan solo posición, textura, tamaño y valor la presentan, mientras que las demás carecen de ella. Por ejemplo, en la imagen correspondiente a la variable visual tono no podemos decir cuáles de los elementos situaríamos al principio y cuáles al final de una escala dada definida por esos tonos. Con el valor, sin embargo, sí que podemos, ya que esta escala iría de los tonos más claros a los más oscuros, y visualmente podemos sin dificultad distinguir los distintos niveles y ordenarlos.

Por último, la propiedad cuantitativa la presentan aquellas variables visuales que permiten estimar proporciones o cantidades de forma visual. Esta propiedad es exclusiva del tamaño y de la posición, mientras que las demás no la presentan. Podemos visualmente estimar una distancia en comparación con otra y decir que es, por ejemplo, el doble de esta. También podemos ver que los círculos grandes en la figura correspondiente son aproximadamente el doble que los pequeños. 

El valor, que ya sabemos que presenta la propiedad ordenada, podría pensarse que también presenta la propiedad cuantitativa, pero no sucede así. Es difícil e impreciso afirmar que un color es el doble de oscuro que otro, y lo más que podemos hacer es situarlo entre dos valores distintos (de ahí que posea la propiedad ordenada), pero no deducir una cifra que exprese una cantidad o proporción. Las restantes variables visuales resulta claro que no poseen esta propiedad.

En la tabla siguiente se muestra un resumen de todo lo anterior.

=================  ===================== ==================== ====================  ==================== ====================  ====================  ==================== 
Propiedad          Posición              Tamaño               Forma                   Valor              Tono                  Textura               Orientación
=================  ===================== ==================== ====================  ==================== ====================  ====================  ====================
Asociativa         :math:`\diamondsuit`  ---                  :math:`\diamondsuit`  ---                  :math:`\diamondsuit`  :math:`\diamondsuit`  :math:`\diamondsuit` 
Selectiva          :math:`\diamondsuit`  :math:`\diamondsuit` ---                   :math:`\diamondsuit` :math:`\diamondsuit`  :math:`\diamondsuit`  :math:`\diamondsuit` 
Ordenada           :math:`\diamondsuit`  :math:`\diamondsuit` ---                   :math:`\diamondsuit` ---                   ---                   --- 
Cuantitativa       :math:`\diamondsuit`  :math:`\diamondsuit` ---                   ---                  ---                   ---                   --- 
=================  ===================== ==================== ====================  ==================== ====================  ====================  ====================

Aunque las ideas de Bertin conforman una sólida base teórica de reconocido valor, lo cierto es que debe permitirse cierta laxitud en la aplicación de estas, y no considerar que existe una dicotomía estricta en el caso de las propiedades antes presentadas. Hay muchos factores y circunstancias que pueden alterar la forma en que estas propiedades se presentan, y alterar la intensidad con que aparecen en unas u otras variables visuales. Por ejemplo, aunque el tono no presenta, según la propuesta original de Bertin, la propiedad ordenada, sí que puede emplearse para representar un orden en determinadas circunstancias. Si estamos simbolizando unos valores de temperatura, podemos establecer una transición de colores entre el rojo y el azul, que serán fácilmente identificados y ordenados por el observador del mapa, ya que el primero de estos colores se asocia habitualmente al calor y el segundo al frío. En este contexto particular, el tono sí presenta la propiedad ordenada. En los capítulos :ref:`Algebra_de_mapas` o :ref:`Creacion_capas_raster` verás muchos ejemplos de representaciones en que se usan gradaciones de tono para simbolizar variables de tipo cuantitativo, ya sean razones o proporciones. Estas guardan, no obstante, cierta lógica, de tal modo que puede entenderse adecuadamente su significado. Como veremos en el próximo capítulo, esto también tiene relación con el tipo de mapa, de tal modo que ciertos tipos de mapas permiten por sus propias características el uso del tono para este tipo de variables.

Junto a lo anterior, algunos autores (véase  :cite:p:`MacEachren2004Guilidford`) expanden el número de variables visuales y se han desarrollado revisiones a las propiedades enunciadas por Bertin basadas en estudios prácticos, que demuestran cómo pueden existir variaciones sobre la relación entre estas y las distintas variables visuales (por ejemplo,  :cite:p:`TreiSman1988PR`).

Uso combinado de las variables visuales
=====================================================

Para explicar cada una de las variables visuales, hemos visto diversos ejemplos en los que utilizábamos cada una de ellas por separado y de forma única. Sin embargo, las variables visuales pueden combinarse y, si se hace de la manera correcta, esto reforzará la capacidad que estas tienen para transmitir una información dada. La imagen :num:`#figcombinacionvariablesvisuales` muestra algunos ejemplos de combinación de variables visuales que nos servirán para detallar la forma adecuada de usas varias de ellas simultáneamente.

.. _figcombinacionvariablesvisuales:

.. figure:: CombinacionVariablesVisuales.*
	:width: 750px
	:align: center

	Combinación de variables visuales.


El primero de los ejemplos propuestos muestra el uso combinado de las variables tamaño y forma para símbolos puntuales. Estos símbolos representan la profundidad del suelo medida en determinados emplazamientos, estando relacionado un mayor tamaño del símbolo  con una profundidad mayor. Asimismo, se ha asociado un símbolo triangular a los valores más bajos, un símbolo circular a los intermedios y uno cuadrado a los más altos. Aunque se emplean dos variables visuales distintas, el resultado no es, sin embargo, mejor que en caso de emplear uno solo de ellos (en este caso, debería emplearse el tamaño, ya que la forma no presenta la propiedad cuantitativa necesaria para representar cantidades). Lejos de producirse una sinergia entre el efecto de ambas variables, el resultado es similar al uso exclusivo del tamaño en cuanto a su capacidad de transmitir la información, o incluso peor, ya que la forma puede dificultar la estimación visual del tamaño, al ser más complicado comparar la dimensión de objetos de distinta forma.

Pese a que no es clara la ventaja de aplicar conjuntamente las variables forma y tamaño, esta puede emplearse para representar cantidades, por lo que podemos decir que mantiene la propiedad cuantitativa que posee el tamaño. En general, al combinar dos variables visuales el resultado presentara las propiedades de aquella que tenga un mayor nivel organizativo. Puesto que la propiedad cuantitativa representa el nivel organizativo superior, en este caso se mantiene en la combinación.

Aún así, hay mejores formas de combinar las variables visuales para que esta combinación enfatice en mayor grado la información que se pretende transmitir, como por ejemplo la mostrada en el segundo ejemplo. Este ejemplo combina el tamaño y el valor, variables ambas que no poseen la propiedad asociativa. Es decir, poseen su complementaria, que podríamos denominar *disociativa*, y que, recordemos, es la propiedad que, al aplicarse sobre un símbolo, hace que este gane importancia visual. El resultado presenta un carácter todavía más disociativo, en cuanto que los símbolos que representan una cantidad elevada, al ser no solo grandes, sino estar pintados en color oscuro, llaman aún más nuestra atención que si empleáramos una única de las variables visuales utilizadas.

Como regla en este sentido, podemos decir que, cuando se combinan variables visuales que poseen una determinada propiedad, en el resultado esta propiedad queda reforzada con respecto a las variables individuales.

El tercer ejemplo nos muestra que combinar variables visuales con una misma propiedad no garantiza necesariamente que se vaya a producir una sinergia entre ellas, sino que, por el contrario, pueden anularse. Las variables empleadas en este caso son las mismas, valor y tamaño, pero se ha asociado el color claro a los valores mayores y el oscuro a los menores, de tal modo que los símbolos de mayor tamaño son más claros que los pequeños. Esto atenúa el efecto disociativo del tamaño, de forma que la representación es más difícil de interpretar y su información no se transmite de modo tan inmediato y directo.

En resumen, podemos sintetizar lo anterior diciendo que, a la hora de combinar variables visuales, deben tenerse en cuenta las propiedades de estas del mismo modo que cuando se emplean de forma individual. Las propiedades a reforzar serán aquellas que convengan más al tipo de información representado, y deben presentarlas todas las variables a combinar para que el efecto conjunto sea más acusado.


La percepción visual
=====================================================

La percepción engloba toda la serie de procesos que convierten un fenómeno físico en una información acerca de nuestro entorno, a través de la estimulación de unos órganos perceptivos. La percepción tiene una fase física, una fisiológica (la estimulación en sí) y una psicológica (la interpretación del estímulo). En el caso de la percepción visual, este fenómeno físico es de tipo energético (la luz), y los órganos correspondientes son los ojos. 

El estudio de la percepción es un fenómeno complejo que no entraremos a detallar, pero en el que resulta de interés profundizar para conocer algo más acerca de cómo la información que plasmamos en un mapa (que es un elemento visual) acaba convertida en una información en la mente del observador de ese mapa. Entender este proceso, al menos someramente, nos permitirá mejorar la eficacia de la percepción, de forma que tengamos una mayor garantía de que la información que transmitimos sea recibida e interpretada correctamente.

Dos son los aspectos que detallaremos en esta sección: las constancias perceptivas y las ayudas a la percepción. En otras palabras, hasta qué punto podemos modificar los elementos visuales o su entorno sin que dejen de transmitir su información y sean confundidos sus características, y cómo podemos facilitar que se perciban exactamente como pretendemos.

Las constancias y contrastes perceptivos
--------------------------------------------------------------

Entendemos por constancias perceptivas a las propiedades de los objetos cuya percepción no varía aunque se produzcan modificaciones. Podemos ver algunos ejemplos para algunas de las variables visuales que conocemos.

Dado un objeto redondo tal como una rueda, si lo miramos en una dirección perpendicular aparecerá efectivamente como una forma circular perfecta. Sin embargo, si la miramos desde otro ángulo, veremos una forma elíptica, pero ello no nos lleva a pensar que la rueda en sí no sea ya redonda. Nuestra percepción de esa rueda es la misma, y podemos apreciar de igual modo su tamaño o su forma. Alterar el ángulo de visión no altera el objeto y la percepción que tenemos de él.

Del mismo modo, un elemento pintado de un color claro se identifica como tal aunque la luz sea tenue, y un elemento oscuro lo seguimos percibiendo como oscuro aunque estemos en unas condiciones de iluminación fuerte. Nuestro cerebro es capaz de interpretar simultáneamente el objeto y el contexto, y de este modo extraer las características de ese objeto, que no varían.

Estos dos ejemplos muestran la constancia perceptiva de la forma y el valor, y podemos buscar otros similares para otras variables visuales.

No todas las variables visuales tienen una constancia perceptiva como la anterior. Todos conocemos múltiples ejemplos de ilusiones ópticas en las que algo no parece lo que realmente es, y esa percepción errónea viene normalmente motivada por las condiciones en las que percibimos el objeto, por ejemplo debido al entorno particular en el que este se encuentra junto a otros objetos. La figura :num:`#figzollner` muestra un ejemplo clásico de ilusión óptica, conocida como *ilusión de Zollner*. Las lineas largas diagonales son paralelas, pero no aparentan serlo, debido al efecto causado por las líneas más cortas. En este caso, no existe una constancia perceptiva de la variable visual orientación.

Cuando la percepción de un elemento cambia aunque el estimulo no lo haga, en lugar de una constancia perceptiva hablamos de un *contraste perceptivo*. Los contrastes perceptivos son importantes, ya que pueden inducir una interpretación errónea de la información que pretendemos transmitir, al producirse una percepción equivocada.


.. _figzollner:

.. figure:: Zollner_illusion.*
	:width: 400px
	:align: center

	Ilusión de Zollner que demuestra el contraste perceptivo de la orientación.



Las siguientes son algunas de las ideas más importantes a tener en cuenta a este respecto a la hora de crear un mapa:


* El tamaño es la variable visual que más afectada se ve, y el tamaño aparente de un objeto puede variar notablemente si se encuentra rodeado de otros de un tamaño distinto. La figura :num:`#figcontrastetamano` muestra un ejemplo de esto. A la hora de emplear simbología de elementos puntuales en un mapa (por ejemplo, en un mapa de símbolos graduados, como veremos en el apartado :ref:`MapasSimbolosGraduados`), esto debe tenerse en cuenta, ya que pueden presentarse situaciones como la de la figura.	
* El valor se ve igualmente alterado al situar alrededor elementos de distinto valor. Si el número de distintos valores es pequeño, es más difícil que aparezca este contraste perceptivo. A medida que se aumenta el número de estos, es más probable que aparezca en mayor o menor medida.
* El tono se ve alterado por la presencia de otros tonos distintos. En un mapa, veremos este efecto al enfrentar el color de un elemento sobre el color del fondo. Por ejemplo, si una línea que representa a una carretera y cruza una serie de polígonos de distinto tono, puede parecer que el tono de la línea varia aunque en realidad sea constante.
* Tonos complementarios puestos juntos pueden crear sensación de vibración en la frontera que los separa.


.. _figcontrastetamano:

.. figure:: ContrasteTamano.*
	:width: 550px
	:align: center

	Contraste perceptivo del tamaño. Ambos circulos grises tienen el mismo tamaño, pero el de la izquierda aparenta ser mayor.


 
.. _ayudaspercepcion:

Ayudas a la percepción
--------------------------------------------------------------


Con lo que hemos visto anteriormente, queda claro que podemos alterar la forma en que se perciben las variables visuales que caracterizan a un elemento visual. Podemos usar este hecho para nuestro beneficio, de tal modo que el diseño de un mapa incorpore elementos que hagan más patente la información que este contiene, facilitando la correcta percepción del mapa en su conjunto.

Un factor clave en este sentido es la adecuado separación entre el fondo y la figura. Aquello que queremos que resulte visible con carácter principal (en el caso de un mapa, sus distintos elementos) debe separarse de aquello que constituye el fondo de la imagen, y debe atraer la atención del observador de manera prioritaria. En caso de no ser así, puede resultar difícil *descubrir* la información que el mapa transmite, al quedar esta al mismo nivel que la de otros elementos de menor importancia. El ejemplo clásico de la figura :num:`#figcuporfaces` ilustra este hecho. Puesto que no existe una diferenciación clara entre el fondo y la figura, no es obvio saber si la imagen pretende representar una copa o dos caras.

.. _figcuporfaces:

.. figure:: Cup_or_faces_paradox.*
	:width: 400px
	:align: center

	Sin un adecuado contraste entre fondo y figura la imagen presenta ambigüedad.


En un mapa, y como veremos en el próximo capítulo, encontramos dos tipos de cartografía: una con carácter de base que define un contexto geográfico, y una temática que constituye la información principal que se transmite con el mapa. Puesto que esta segunda es la fundamental y de mayor importancia, y la primera se incluye tan solo como apoyo de esta, es importante asegurarse de que esa cartografía base no interfiere y se mantiene en un segundo plano, constituyéndose como fondo y dejando que sea la información temática la que actúe como figura. Para ello podemos emplear las distintas variables visuales aplicadas a la cartografía base, de modo que su importancia relativa no sea mayor que la de los elementos principales de la parte temática.

Otro aspecto a considerar es la adecuada jerarquización entre los elementos del mapa. La división entre fondo y figura ya constituye en sí una jerarquización, pero no es suficiente si conviven varios tipos de elementos en el mapa. Dentro de la parte temática es necesario estructurar estos visualmente para que quede clara su importancia y se vea sin dificultad que existe una división entre ellos.

Esta jerarquía debe aportar una *profundidad* a la información, de forma que existan niveles en esta y se perciba que algunos elementos están por encima de otros. Como veremos en el capítulo :ref:`Visualizacion_SIG`, la forma de ordenar las distintas capas en un SIG ya establece un orden, aunque este no es en sí suficiente, y deben utilizarse las variables visuales para enfatizar o no unas o otras capas y la información que contienen.

Algunas técnicas básicas para esto son las que permiten que exista algún factor diferencial en la información más relevante. Si las propiedades de los elementos destacados difieren notablemente de las del fondo, esto centra la atención sobre ellas y garantiza que no se confundan con este. Emplear unas características más homogéneas para el fondo permite que la diferenciación de la figura sea más patente. En otras palabras, el contraste, aplicado este a todas las variables visuales, es una de las claves para lograr una adecuada transmisión de la información al emplear una representación visual.

El contraste se aplica no solo a las variable visuales, sino en general a las características de la representación. Por ejemplo, el nivel de detalle es una propiedad susceptible de ser utilizada para enfatizar algo. Así, y en el caso particular del documento cartográfico, el lector de un mapa espera que el detalle sea mayor en la cartografía temática que en la de base, ya que esta última es simplemente un elemento complementario de ayuda. Un mayor detalle sobre ciertos elementos llamará más la atención en contrate con un fondo menos detallado, y esto puede utilizarse para enfocar la atención sobre lo más relevante. Ofrecer menos detalle en la cartografía de base no es un inconveniente si esto ayuda a un mejor entendimiento de los elementos principales del mapa.

Como ejemplo de lo anterior, la figura :num:`#figjerarquiamapa` muestra un ejemplo de como una correcta jerarquización es fundamental para crear mapas de calidad.

.. _figjerarquiamapa:

.. figure:: JerarquiaMapa.*
	:width: 750px
	:align: center

	Mapa con jerarquía incorrecta (a) y mapa adecuadamente jerarquizado (b).


 


Por último, un aspecto clave para la claridad de un mapa es el relativo al poder separador. Este define la capacidad de un individuo para distinguir objetos muy pequeños y separar objetos cercanos. Además de depender del propio individuo, está condicionado por una serie de factores. 

Se admite en líneas generales que el límite de separación entre dos objetos para el ojo humano es de 0,2mm. Si existe una distancia menor entre ellos, en condiciones normales no será posible distinguir uno de otro. 

Existe también un límite para poder reconocer objetos aislados, aunque este depende del tipo de objeto. Los siguientes son algunos de los aplicados usualmente:


* 0,2mm de diametro para el caso de un punto.
* 0,5mm de grosor para el caso de una línea negra.
* 0,4mm de lado para el caso de un cuadrado negro.
* 0,6mm de lado para un cuadrado sin relleno.


Existe asimismo un umbral de diferenciación, que define el tamaño mínimo de dos objetos para que puedan ser percibidos como distintos. Este umbral también depende de las caracteristicas de los objetos, como por ejemplo la forma (si las formas son muy distintas será más fácil distinguirlos que si son muy similares). 

El poder separador no depende únicamente de variables de tipo espacial, sino que también está en relación con otras variables visuales. Por ejemplo, una línea negra sobre fondo blanco puede distinguirse aunque sea fina, pero en caso de ser amarilla sobre ese mismo fondo, será necesario un grosor mayor.

Como parece lógico, estos conceptos deben usarse para no incorporar a un mapa elementos que estén más allá del umbral de separación del lector del mapa, ya que en este caso no podrá extraer la información que se ha incorporado en este al crearlo.



Resumen
=====================================================

Para transmitir correctamente cualquier tipo de información mediante el lenguaje visual, es necesario conocer sus elementos y saber emplearlos de modo adecuado. La semiología gráfica se encarga del estudio de los símbolos del lenguaje visual, y en este capítulo hemos visto algunas de sus ideas principales.

De especial relevancia resultan las denominadas *variables visuales*, las cuales empleamos para la caracterización de símbolos. Existen seis variables visuales: posición, forma, tamaño, color, textura y orientación. El color a su vez se puede dividir en tres: tono, valor y saturación. De estas tres, solo las dos primeras, tono y valor, tienen aplicación práctica en el ámbito cartográfico.

Las variables visuales presentan distintas propiedades, que definen a su vez los *niveles de organización*. De menor a mayor organización, estas propiedades son las siguientes: asociativa, selectiva, ordenada, cuantitativa. Las propiedades de una variable visual condicionan el tipo de información que puede transmitirse haciendo uso de ella. Cuando se combinan varias variables visuales que poseen una misma propiedad, esta propiedad se presenta con mayor fuerza en el resultado.

Podemos ayudar a que la percepción de la información que transmitimos con un elemento visual sea mejor, atendiendo a aspectos como el contraste entre el fondo y la figura, así como estableciendo una correcta jerarquización entre los distintos elementos. Igualmente, debemos prestar atención a los contrastes perceptivos, para evitar que estos aparezcan y se produzca una percepción incorrecta.


