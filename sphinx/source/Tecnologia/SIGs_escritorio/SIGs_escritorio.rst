.. _sigs_escritorio:

**********************************************************
Herramientas de escritorio
**********************************************************

Las herramientas de escritorio son la forma más *típica* en la que se presentan los Sistemas de Información Geográfica, y que ofrecen elementos para realizar las tareas básicas de un proyecto SIG. En este capítulo veremos sus características principales y los distintos tipos de ellas que pueden encontrarse, detallando la utilidad de cada una.


Introducción
=====================================================

El concepto clásico de un SIG es el de una aplicación completa en la cual se implementan herramientas para llevar a cabo las tareas básicas del trabajo con datos geográficos: creación o edición, manejo y análisis. Con esta filosofía fueron desarrollados los primeros programas SIG, especialmente para el tratamiento y análisis de datos geográficos y, posteriormente, para dotar a estos de mayor versatilidad, incorporando otras funciones adicionales que facilitaran el trabajo con esos mismos datos. Se tienen así las herramientas de escritorio, que son aquellas que más se asemejan a la concepción original de los SIG.

A pesar de que existen, como vimos en el capítulo anterior, otras clases de aplicaciones SIG, los SIG de escritorio siguen manteniendo su posición como aplicaciones fundamentales, y hablar genéricamente de un SIG implica por lo general  hacerlo de una aplicación de escritorio antes que de otros tipos de aplicaciones. Por otra parte, las herramientas de escritorio son soluciones en general completas que cubren la totalidad de necesidades que se presentan en el desarrollo de proyectos SIG, y por ello constituyen las herramientas primordiales para llevar estos a cabo.

Funciones básicas
=====================================================

Podemos dividir las funciones básicas de un SIG de escritorio en cinco bloques: entrada y salida de datos, visualización, edición, análisis y generación de cartografía. Una aplicación de escritorio habitual presenta todas estas capacidades en cierta medida, aunque no necesariamente con el mismo nivel de implementación.

Entrada y salida de datos
--------------------------------------------------------------

Ya sabemos que los datos son una parte imprescindible de un SIG, y sin ellos no puede desarrollarse actividad con una aplicación SIG. Por esta razón, todas estas aplicaciones deben obligatoriamente implementar capacidades para leer datos y, opcionalmente, para guardarlos. Esta ultima es necesaria en el caso en que el SIG pueda generar nuevos datos geográficos (nuevas capas), pero no en aquellas aplicaciones sin capacidades de análisis o edición, donde su empleo no ha de crear nuevos datos.

Pese a ser de tal importancia, la implementación de las capacidades de entrada y salida es muy variable en unos u otros SIG. Una razón por la que esto sucede es el gran número de formatos de fichero distintos, la cual no favorece la interoperabilidad, como ya vimos en el capítulo :ref:`Fuentes_datos`. Así, cada SIG es capaz de abrir unos u otros formatos de archivo, y mientras que algunos tratan a todos ellos por igual, ciertas aplicaciones trabajan en un formato propio con carácter nativo, y son capaces de incorporar datos en otros formatos a través de extensiones o funciones de conversión entre estos y el formato particular del programa.

La existencia de librerías y componentes de acceso a datos en los que las aplicaciones SIG de escritorio pueden apoyarse mejora la conectividad entre estas y aporta cierta homogeneidad en este aspecto.

Otra diferencia importante en la gestión de los datos es la capacidad de conexión a bases de datos o servicios remotos como los que veremos en el capítulo :ref:`Servidores_y_clientes_remotos` [#fn2]_. Así, algunas aplicaciones tienen únicamente capacidades de abrir archivos, pero no de acceder a servicios remotos, mientras que otras pueden acceder a todo tipo de orígenes de datos. Las aplicaciones que acceden a servicios remotos entran dentro de la denominación de *clientes*. Los clientes Web que veremos en el capítulo :ref:`Servidores_y_clientes_remotos` se conocen como clientes *ligeros*, mientras que las aplicaciones SIG de escritorio con estas capacidades se denominan clientes *pesados*, haciendo referencia a su mayor volumen y el mayor número de funcionalidades que contienen. La funcionalidad que ofrecen en relación al acceso a datos remotos es similar en ambos casos, y la trataremos en el citado capítulo :ref:`Servidores_y_clientes_remotos` con detalle.

En general, las capacidades de acceso a servicios remotos están en función del enfoque de la aplicación, y aquellas fuertemente enfocadas al análisis no suelen presentar tales funcionalidades, mientras que aquellas más orientadas a la visualización o las herramientas globales más completas sí que las incorporan.

.. _funcion_sig_visualizacion:

Visualización
--------------------------------------------------------------


La visualización es una función fundamental dentro de los SIG y del trabajo con cartografía en general. En este libro, por ejemplo, existe una parte completa dedicada a esta materia, pues su conocimiento resulta fundamental para poder aprovechar plenamente la información contenida en el dato geográfico.

Aunque existen SIG que no incorporan capacidades de visualización o estas no son muy avanzadas, la gran mayoría de las herramientas de escritorio incluyen un gran número de elementos para representar los datos geográficos con los que se trabaja. En ocasiones, interesa únicamente crear una representación de los datos, pero incluso cuando el trabajo con una herramienta SIG está enfocado a la realización de un análisis, la visualización y exploración visual de los datos de partida es un paso previo.

En general, la forma de operar con los elementos de visualización es muy similar entre soluciones SIG distintas y, a diferencia de lo que sucede con la implementación de otras funcionalidades, el manejo es prácticamente igual. Esto sucede no solo ya en las herramientas de escritorio que tratamos en este capítulo, sino también en las que veremos en el dedicado a las aplicaciones Web, las cuales incorporan también capacidades de visualización del mismo tipo. En ambos casos, las herramientas fundamentales presentan una estructura similar y unos conceptos base muy parecidos.

Esta estructura se compone fundamentalmente de un lienzo sobre el que se sitúan las distintas capas de información geográfica, y que el usuario va conformando añadiendo nuevas capas y editando la forma en la que estas se representan. Las capas se sitúan en un orden dado dentro del lienzo, lo que permite establecer una jerarquía de representación y así lograr el aspecto deseado.

Junto a este lienzo existen herramientas de navegación que permiten ampliar o reducir la escala, o bien modificar el encuadre (Figura :num:`#figherramientasnavegacion`). Asimismo, se presentan todas las funciones que permiten obtener las distintas formas de representación que veremos en la parte :ref:`Visualizacion`, tales como el ajuste de colores o el establecimiento de etiquetas en función de los valores asociados a las distintas entidades, entre otros.

.. _figherramientasnavegacion:

.. figure:: Herramientas_navegacion.*
	:width: 650px
	:align: center

	Herramientas de navegación fundamentales en el entorno gráfico de un SIG de escritorio. a) alejamiento (*zoom out*), b) acercamiento (*zoom in*), c) desplazamiento (*pan*)


 


Estas capacidades convierte a los datos geográficos en un elemento activo, pues, a diferencia de un mapa clásico donde no pueden modificarse sus características, en un SIG el usuario puede de forma rápida y sencilla elegir *qué* ve y *cómo* lo ve.

Como parece lógico pensar, la visualización ha evolucionado mucho desde los primeros SIG, y ha ido progresivamente adquiriendo nuevas capacidades, muchas de las cuales solo son posibles con los modernos componentes gráficos de los ordenadores actuales. Así, además de ofrecer mayores posibilidades de personalización, el uso del SIG como herramienta de representación permite obtener resultados novedosos que añaden nuevas formas de explorar los datos geográficos y trabajar con ellos.

En el caso más habitual, la representación de una capa en un lienzo de un SIG es bidimensional, de la misma forma que se representa en un mapa impreso, lo cual se debe tanto a la mayor facilidad de implementación de este tipo de representaciones como a la mayor exigencia que otro tipo de representaciones presentan en lo referente al equipo (*hardware*). 

No obstante, la presencia de visores tridimensionales está experimentando un gran crecimiento en los últimos años, y se van integrando paulatinamente dentro de los SIG para ofrecer una nueva forma de representación. Esta clase de capacidades gráficas, inalcanzables en términos de rendimiento para un equipo común hace unos años, son hoy día perfectamente utilizables en un ordenador de consumo habitual, y aportan una nueva forma de trabajar con los datos geográficos.

Las funcionalidades de representación 3D aún no se integran completamente dentro del entorno de un SIG de escritorio completo, ya que se conciben por lo general como un elemento puramente visual y enfocado a la representación como tal, mientras que un lienzo 2D cumple su función tradicional de marco de trabajo sobre el que se desarrollan las restantes tareas del SIG como el análisis o la propia gestión de datos. Aun así, conforme las vistas tridimensionales se van convirtiendo en elementos habituales, los restantes componentes del SIG se van coordinando con ellas para darles a su vez la capacidad de servir como entornos de trabajo versátiles.

La presencia de una dimensión adicional hace que las herramientas de navegación sean más complejas en el caso tridimensional, existiendo ajustes relativos a la perspectiva, a los ángulos de visión o a la exageración del relieve, entre otros parámetros. Como puede verse más adelante en la figura :num:`#figgearth`, las herramientas de control de navegación de un visor 3D (situadas en este caso en la parte superior derecha de la figura) , son sensiblemente más complejas que las herramientas base del caso 2D, presentadas en la figura :num:`#figherramientasnavegacion`.

Esta mayor complejidad hace asimismo que puedan existir diversas formas en las que las capacidades de visualización 3D se presentan en un SIG. Las representaciones tridimensionales pueden ser simples representaciones en relieve de una capa (Figura :num:`#figtiposvistas3d` a), o pueden incluir verdaderos elementos en tres dimensiones (Figura :num:`#figtiposvistas_3d` b). En el primer caso, la capa no contiene datos de elevación (puede ser por ejemplo una capa de usos de suelo), y la representación tridimensional se realiza basándose en la información de una capa adicional de elevaciones (que denominábamos de 2,5D por no poder representar todo tipo de formas en el espacio). La capa plana se representa en espacio *deformada* para ajustarse al relieve existente en la zona que representa.

En el caso de una representación tridimensional real, los objetos poseen información sobre su forma tridimensional, y junto con las coordenadas que delimitan su geometría plana (las geometrías básicas que conocemos: punto, línea y polígono), existen valores adicionales en el eje vertical. De este modo, pueden representarse entidades tales como edificios, o una ruta tridimensional que represente la trayectoria de un avión. Asimismo, y como puede verse en la figura, pueden añadirse elementos adicionales que aprovechan las capacidades de representación 3D, así como etiquetas o incluso elementos interactivos que también actúan en 3D (por ejemplo, para la selección de entidades).


.. _figtiposvistas3d:

.. figure:: Tipos_vistas_3D.*
	:width: 750px
	:align: center

	Distintas formas de representación 3D de capas de datos geográficos


 


Es importante recalcar que la visualización de una capa dentro de un SIG es independiente de la información que dicha capa contiene o la forma en que esta se almacena. El dato geográfico y su representación van por separado, y el dato en sí no define la representación, sino que únicamente sirve como apoyo para esta. Esto es particularmente cierto para el caso de capas vectoriales, así como para capas ráster que contengan un valor de tipo no gráfico, es decir, aquellas que no sean imágenes.

Una imagen tendrá el mismo aspecto en todos los SIG en los que se utilice, puesto que la información relativa a su representación se contiene, al menos en cierta medida, en la propia imagen. Los valores de la imagen representan una intensidad de luz y, si las bandas corresponden a la zona del visible, existe asimismo una información de colores. Otras imágenes pueden proceder del escaneo de un mapa o una fotografía impresa, y en ese caso recogen también los colores de cada píxel. 

Aun en el caso de imágenes con más de tres bandas, en las que no existe una correspondencia directa entre los valores y la representación (tal como vimos, por ejemplo, en la creación de representaciones en falso color en el apartado :ref:`Visualizacion_imagenes`), puede existir una representación *por defecto* tomando, por ejemplo, las tres primeras bandas, y sigue siendo probable que estas imágenes también se vean de igual modo en uno u otro SIG (aunque luego ello no implica que dicha representación no pueda ajustarse a conveniencia en todos los casos).

En el caso de capas vectoriales o una capa ráster tal como un MDE, no existe ningún tipo de información acerca de la representación acompañando al dato espacial en sí. Los datos necesitan de un esquema de asignación que los convierta en elementos visuales (colores, texturas, etc.), pero este esquema es ajeno al dato en sí. 

La labor del SIG relativa a la visualización consiste en *interpretar* los datos y convertirlos en representaciones, y para ello se basa en esquemas definidos por el usuario. Estos esquemas pueden ser almacenados de forma que en sucesivos usos de una capa de datos, esta se represente de una misma forma. No obstante, abrir la capa con una aplicación SIG distinta implicará en general perder las características definidas para su representación ya que, si bien los formatos de datos son relativamente interoperables, no así los formatos en que se almacenan los criterios de representación de esos datos.

Estándares para el almacenamiento de estilos como SLD(*Styled Layer Descriptor*), que veremos en detalle en el apartado :ref:`SLD`, tienen como objeto solventar este problema. 

Análisis
--------------------------------------------------------------

Si hubiéramos de ordenar cronológicamente las distintas funcionalidades que un SIG de escritorio presenta, probablemente el análisis fuera una de las primeras. Por encima de otras capacidades, los ordenadores han sido y son principalmente herramientas de cálculo capaces de realizar operaciones y computar resultados, y este ha sido uno de los usos fundamentales relativos al manejo de datos geográficos. Otros usos, tales como la visualización, pese a ser prácticamente imprescindibles hoy en día, estaban muy limitados en los primeros SIG. No ocurría así en el ámbito del análisis ya que, aunque con capacidades como es lógico menores que las actuales, los ordenadores ofrecían una potencia de calculo que los convertía en herramientas de análisis tan interesantes como en la actualidad.

La tendencia actual en los SIG es considerar las capacidades de análisis como herramientas modulares que se ejecutan sobre una plataforma base, la cual comprende las capacidades de visualización y entrada y salida de datos. Todas estas capacidades de análisis son independientes entre sí, aunque pueden coordinarse y emplearse en conjunto para alcanzar un resultado concreto. De otro modo, cada una de las formulaciones o algoritmos que vimos en los capítulos de la parte :ref:`Procesos` aparece dentro del SIG como una herramienta individual que opera sobre una serie de capas y genera un resultado dado, tomando en muchas ocasiones esas capas de entre aquellas que se están representando en el SIG, e incorporando asimismo a dicha representación las nuevas capas generadas.

Las herramientas de análisis pueden aparecer igualmente como programas independientes, y el SIG de escritorio ser una herramienta aglutinadora que centraliza estas, facilitando su uso y la gestión de los datos implicados en los procesos de análisis.

Cuando las herramientas de análisis utilizan directamente la base del SIG donde se encuentran las capacidades de visualización y manejo de datos, puede existir cierto grado de interactividad. Las operaciones de consulta, por ejemplo, las cuales vimos en el capítulo :ref:`Consultas`, son en general de este tipo, ya que el usuario puede actuar sobre el lienzo para hacer una selección de modo gráfico. Más aún, esa selección puede condicionar los posteriores análisis sobre la capa cuyas entidades se seleccionan, ya que los procesos que operen sobre ella pueden restringir su alcance a aquellas entidades seleccionadas.

En caso de no existir este tipo de interacción entre elementos de análisis y elementos de visualización y exploración de datos, los procesos de análisis suelen constituir utilidades autocontenidas que simplemente toman una serie de datos de entrada, realizan un proceso en el que el usuario no interviene, y finalmente generan un resultado con carácter definitivo. Este resultado podrá ser posteriormente visualizado o utilizado como entrada para un nuevo análisis.

A modo de ejemplo, podemos analizar el caso particular del cálculo de una ruta que conecte una serie de puntos a través de una red (los fundamentos de este análisis los vimos en el apartado :ref:`Analisis_redes`). 

Una de las formas de implementar este análisis es aquella que requiere del usuario la introducción de la información necesaria (una capa de lineas con la red viaria y otra de puntos con los puntos de inicio, paso, y llegada correspondientemente ordenados) como parámetros que el proceso toma y en función a los cuales se genera una nueva capa. El proceso es una tarea perfectamente definida, con unas entradas y una salidas, y tras la selección de unas capas de entrada se genera un nuevo resultado en forma de otra capa. Este proceso puede implementarse de forma aislada del SIG, aunque coordinada con él para lograr mejores resultados y una utilización más sencilla.

Otra forma con un enfoque distinto sería presentando un proceso interactivo en el cual se introduce como único parámetro inicial la red viaria. Posteriormente, el usuario puede operar sobre el lienzo en el que esta se encuentra representada para ir definiendo y editando la lista de puntos de paso. El cálculo se va efectuando cuando se produce algún cambio en la misma y debe aplicarse de nuevo el algoritmo pertinente para adaptar el resultado ---la ruta óptima--- a ese cambio.

Este tipo de formulaciones interactivas son más intuitivas y agradables de usar, pero en realidad menos productivas de cara a un trabajo dentro de un proyecto SIG. Aparecen por ello en aquellas funciones que tienen una mayor componente visual o, especialmente, en las que representan un análisis puntual que se realiza de forma común como algo individual. Estos son los análisis que se implementan en las aplicaciones que veremos más adelante como parte del grupo de SIG enfocados a la exploración visual de datos geográficos, que además de esta proveen alguna serie de utilidades de análisis, pocas en general, sin que estas estén concebidas para un trabajo completo en un proyecto SIG de cualquier índole, sino más bien para un uso ocasional.

En un proyecto SIG de cierto tamaño, lo más común es que la fase de análisis, a la que seguirá una fase también compleja de preparación e interpretación de resultados, y previa a la cual se ha debido llevar a cabo la preparación de los datos de partida, comprenda no uno sino muchos análisis distintos. Estos análisis, a su vez, no son independientes, sino que están relacionados entre sí y lo más habitual es que definan como tales un flujo de trabajo que comienza en los datos de partida y desemboca en los resultados finales a través de una serie de procesos. 

Por su naturaleza, tanto los datos espaciales como los procesos en los que estos intervienen se prestan a formar parte de estos flujos de trabajo más o menos complejos, y es por ello que en los SIG actuales una funcionalidad básica es la creación de tareas complejas que permiten simplificar todo un proceso de muchas etapas en una única que las engloba a todas. La forma anteriormente comentada en que aparecen las formulaciones dentro de un SIG, de forma atomizada y modular, facilita la creación de estos *modelos* a partir de procesos simples.

Para entender esta idea, podemos ver un ejemplo aplicado. La extracción de una red de drenaje en formato vectorial a partir de un MDE requiere una serie de procesos, a saber (para repasar los fundamentos de cada uno de estos procesos y comprender mejor la operación global, puede consultarse el capítulo :ref:`Geomorfometria`, donde se describieron en su momento, así como la sección :ref:`Vectorizacion_lineas`):

* Eliminación de depresiones del MDE.
* Cálculo de una capa de área acumulada a partir del MDE corregido
* Extracción de capa ráster con la red de drenaje a partir de la capa anterior y un valor umbral
* Vectorización de la capa resultante del paso anterior


Lo anterior podría simplificarse si se agruparan en una sola operación todos los procesos anteriores, de forma que tomando dos datos de entrada (un MDE y un umbral), se realizara todo el proceso de forma continua. Las capacidades de creación de modelos que implementan los SIG de escritorio (en particular, los más enfocados al análisis) permiten crear nuevos procesos compuestos utilizando entornos gráficos intuitivos, y estos procesos pasan a formar parte del conjunto de ellos de que dispone el SIG, permitiendo que cada usuario *resuma* en procesos unitarios una serie de operaciones que, de otro modo, deberían realizarse de forma individual con el coste operacional que ello implica.

Una vez que se ha creado un proceso compuesto, este puede aplicarse sobre nuevos datos de entrada, reduciéndose así el tiempo y la complejidad con que nuevos parámetros de entrada pueden ser procesados según el esquema de trabajo definido en dicho proceso.

Debe pensarse que el proceso presentado como ejemplo es muy sencillo y únicamente implica cuatro operaciones encadenadas de forma lineal. Un proceso de análisis habitual puede contener muchas más operaciones individuales, y estas disponerse de forma más compleja, con dependencia de distinta índole entre sus resultados. La imagen :num:`#figprocesocomplejo` muestra el aspecto de uno de tales procesos implementado en un software (ArcGIS, véase sección :ref:`Softprivativo`) con capacidad de de creación de modelos. El proceso representado en la figura :num:`#figesquemamontecarlo` también es un ejemplo de otro tipo de análisis que puede adaptarse ventajosamente en este tipo de herramientas de modelización.

.. _figprocesocomplejo:

.. figure:: Proceso_complejo.*
	:width: 650px
	:align: center

	Esquema de un proceso complejo creado a partir de operaciones simples de análisis con datos SIG.


 


Edición
--------------------------------------------------------------

Los datos geográficos con los que trabajamos en un SIG no son una realidad estática. La información contenida en una capa es susceptible de ser modificada o corregida, y las funciones que permiten estas tareas son importantes para dotar al SIG de versatilidad. Sin ellas, los datos espaciales pierden gran parte de su utilidad dentro de un SIG, ya que se limitan las posibilidades de trabajo sobre estos. Las funcionalidades de edición son, por tanto, básicas en una herramienta de escritorio.

Las operaciones de edición pueden emplearse, por ejemplo, para la actualización de cartografía. Como vimos en el capítulo :ref:`Fuentes_datos`, una de las ventajas de los datos digitales frente a los analógicos es la mayor facilidad de actualización. Así, si una entidad en una capa vectorial (por ejemplo, una parcela catastral) modifica su geometría, no es necesario rehacer todo un mapa, sino simplemente editar ese elemento. A lo largo del desarrollo de un proyecto SIG, es muy probable que sea necesario editar de un modo u otro algún dato espacial, bien sea para corregirlo, ampliarlo, mejorarlo o sencillamente adaptarlo a las necesidades del propio proyecto.

Además de la modificación de una capa ya existente, las herramientas de edición de un SIG de escritorio se emplean igualmente para la creación de capas nuevas, que pueden crearse a partir de la digitalización de imágenes como vimos en el capítulo :ref:`Fuentes_datos`, o bien en base a cualquier otra capa de la que dispongamos.

Aunque las tareas de edición más habituales son las relacionadas con la edición de geometrías, no es esta la única edición que puede realizarse dentro de un SIG. Podemos distinguir las siguientes formas de edición:


* Edición de geometrías de una capa vectorial
* Edición de atributos de una capa vectorial
* Edición de valores de una capa ráster


Las herramientas destinadas a la edición de entidades geométricas heredan sus características de los programas de diseño asistido por ordenador (CAD), cuya funcionalidad principal es precisamente la edición de elementos gráficos. Estas incluyen la adición o eliminación de nuevas geometrías, la modificación de ellas editando sus puntos (recordemos que toda entidad vectorial se reduce a un conjunto de puntos en última instancia), así como otras operaciones geométricas básicas. En la sección :ref:`Digitalizacion_manual` vimos algunas de ellas a la hora de tratar la calidad de la digitalización en pantalla.

Otras funciones de edición que encontramos son las que permiten simplificar algunas tareas, tales como la división de un polígono. La figura  :num:`#figdivisionpoligono` muestra cómo un polígono puede dividirse en dos simplemente trazando una línea divisoria.  Otras funcionalidades similares incluyen la eliminación automática de polígonos espúreos (véase :ref:`poligonos_espureos`), o el ajuste automático entre entidades.

.. _figdivisionpoligono:

.. figure:: Division_poligono.*
	:width: 650px
	:align: center

	División automática de un polígono en dos nuevas entidades a partir de una línea. Funcionalidades de este tipo aparecen en los SIG para facilitar las tareas de edición.

En general, el número de funcionalidades es sensiblemente menor que en el caso de los programas CAD, ya que gran parte de ellas no tiene aplicación directa en el caso de trabajar con datos geográficos. No obstante, también aparecen herramientas adicionales, como sucede en el caso de que se registre información topológica, lo cual ha de considerarse por igual en el proceso de edición. Así, herramientas como la mostrada en la figura :num:`#figdivisionpoligono` han de tener en cuenta la existencia de una estructura topológica y un modelo de representación particular en el SIG, y no operarán igual en todas las aplicaciones, ya que, como sabemos, no todas presentan las mismas capacidades en este terreno.

Junto con las propias geometrías que pueden editarse según lo anterior, toda capa vectorial tiene asociado un conjunto de atributos, y estos deben poder editarse también desde el SIG. De hecho, la adición de una nueva geometría a una capa vectorial no está completa hasta que no se añaden igualmente sus atributos.

La edición de toda la información alfanumérica relacionada con las distintas entidades se realiza en un SIG a través de elementos tomados del ámbito de las bases de datos, siendo esto en general válido tanto en lo referente a las interfaces como en el propio acceso a datos. Las operaciones de edición de atributos abarcan tanto la modificación de valores sencillos como la de la propia estructura del conjunto de atributos (adición o eliminación de columnas ---campos--- en la tabla correspondiente). Por supuesto, la edición de atributos y de geometrías esta íntimamente relacionada.

Por último, la edición de capas ráster es mucho menos frecuente, y una gran mayoría de SIG no permiten la modificación directa de los valores de las celdas. Las operaciones del álgebra de mapas permiten modificar los valores de una capa y obtener nuevas capas con esos valores modificados, pero editar directamente un valor de celda del mismo modo que se editan el valor de un atributo o la posición de un punto de una capa vectorial no es una funcionalidad tan habitual.

Este tipo de capacidades, no obstante, pueden ser de gran utilidad, especialmente en SIG orientados al manejo principal de capas ráster, donde sustituyen en cierta medida a las funcionalidades de edición vectorial equivalentes.


.. _generacioncartografia:

Generación de cartografía
--------------------------------------------------------------


A pesar de que la representación de las distintas capas de datos espaciales en un lienzo es suficientemente potente a efectos de explorar visualmente la información que estas contienen, la mayoría de los SIG incorporan capacidades de creación de cartografía impresa, generando un documento cartográfico que posteriormente puede imprimirse y emplearse como un mapa clásico. Las razones para la existencia de tales funcionalidades son muchas, pero la principal sigue siendo la necesidad general que aún existe de apoyarse en esa clase de documentos cartográficos para poder incorporarlos a proyectos o estudios como parte de anexos cartográficos.

Aunque la representación dentro de un SIG ofrece posibilidades mayores (cambio de escala, ajuste de los parámetros de visualización, etc.), disponer de una copia *estática* de cada bloque de información con el que se trabaja en un SIG es una necesidad ineludible. Más que una capacidad necesaria para la presentación adecuada de la información cartográfica, la generación de cartografía impresa es en muchos casos la principal razón para el uso de un SIG. Mientras que las capacidades de análisis o edición son en ocasiones poco o nada utilizadas, las de generación de cartografía son un elemento fundamental, y muchos usuarios la consideran erróneamente como la funcionalidad primordial de un SIG.

Llegado a este punto del libro, y tras todo lo que hemos visto, queda claro, no obstante, que un SIG es ante todo una herramienta de gestión y análisis de datos espaciales, y que las capacidades enfocadas a la producción cartográfica deben verse como una ayuda ---de vital importancia, eso sí--- para la presentación final de todo el trabajo que se lleva a cabo en él.

Fundamentalmente, estas capacidades permiten la composición de documentos cartográficos de acuerdo con un diseño dado, y la impresión directa de estas en algún periférico tal como una impresora común o un *plotter* de gran formato. En la elaboración de dicho diseño, pueden emplearse todos los elementos que habitualmente podemos encontrar en un mapa: el propio mapa en sí (la representación de la información geográfica), leyenda, título, escala, etc. Con estos elementos, se crea una versión autocontenida de la información geográfica, que puede ya emplearse de modo independiente del SIG.

Las funciones de diseño que se implementan por regla general en un SIG son similares a las que pueden encontrarse en un software de maquetación genérico, permitiendo la composición gráfica del documento general y el ajuste de los distintos elementos que lo forman. Funciones más avanzadas no están presentes de modo habitual, principalmente debido a las características muy concretas y bien definidas del tipo de documento con el que se trabaja, lo cual hace posible esta simplificación.

Aunque, como se ha dicho, muchos usuarios, bien por desconocimiento o falta de formación en la herramienta, consideran que la capacidad principal de un SIG es *hacer mapas*, lo cierto es que, incluso en aquellas aplicaciones más completas y avanzadas, la potencia en la producción cartográfica es muchas veces insuficiente para producir cartografía profesional. Pueden obtenerse resultados de gran calidad y sin duda de suma utilidad, pero lo más habitual es no encontrar en un SIG las capacidades que se necesitan, no ya únicamente desde el punto de vista del cartógrafo, sino desde la perspectiva del diseño. 

La creación de un mapa no es solo una tarea técnica, sino asimismo una labor artística, existiendo unas necesidades en función del enfoque que prime. Como herramienta de trabajo, un SIG es un elemento técnico, y las consideraciones artísticas, aunque pueden en cierta forma aplicarse con las herramientas que este implementa, resultan más sencillas de tratar si se dispone de aplicaciones más específicas en ese sentido.  

Por ello, lograr un mapa de apariencia realmente profesional requiere unas herramientas de diseño avanzado, a la par que un conjunto de utilidades suficiente como para poder aplicar a la creación del mapa todos los conceptos sobre representación que veremos en la parte :ref:`Visualizacion`, no encontrándose estas en ocasiones en su totalidad dentro de un SIG. La utilización del SIG como aplicación base y el uso posterior de programas de diseño es la solución adecuada para la obtención de cartografía profesional, aunque lógicamente requiere unos mayores conocimientos y una especialización más allá de la propia práctica cartográfica.

No obstante, para el usuario técnico de SIG (el usuario al que está dirigido este libro), las herramientas de diseño cartográfico que la mayoría de aplicaciones implementan son más que suficientes, y permiten lograr resultados altamente satisfactorios.

Una de las funciones más interesantes de generación cartográfica en un SIG es la automatización del proceso y la simplificación de la producción de grandes volúmenes de cartografía. Por una parte, todas las herramientas de escritorio capaces de producir cartografía son a su vez capaces de *reutilizar* diseños, de tal modo que si un conjunto de mapas tienen unas características comunes (por ejemplo, una misma disposición de sus elementos), no es necesario elaborar todos ellos desde cero.

Esto permite, por ejemplo, crear una serie de mapas de una misma zona conteniendo cada uno de ellos información sobre distintas variables. A partir de un conjunto de capas, se elabora el diseño de un mapa y este se alimenta de dichas capas, creando mapas independientes que reflejan estas por separado o en distintas combinaciones. Esto simplifica notablemente el proceso, ya que el diseño ha de realizarse una única vez, al tiempo que se garantiza la uniformidad de los distintos resultados.

Otra aplicación en esta linea es la generación de una serie de mapas que cubren en su conjunto una amplia extensión, fragmentando esta en unidades. La gestión de los encuadres para cada una de esas unidades, o la creación de un mapa guía en cada caso que localice la hoja concreta dentro de la extensión global del conjunto, ambas pueden automatizarse junto con las restantes operaciones de diseño. De este modo, la producción de toda una serie cartográfica se simplifica en gran medida, siendo el SIG una herramienta que supone un gran avance en términos de productividad en este tipo de tareas.

La figura :num:`#figseriemapas` muestra un ejemplo de lo anterior.

.. _figseriemapas:

.. figure:: Serie_mapas.*
	:width: 650px
	:align: center

	La automatización de las tareas de creación cartográfica permite simplificar la producción de grandes volúmenes de cartografía, como por ejemplo al dividir un área geográfica en una serie dada de mapas.


 


Estas posibilidades surgen de la separación existente en un SIG entre los datos espaciales y el diseño del documento cartográfico que los contiene, del mismo modo que ya vimos existe entre datos y parámetros de representación a la hora de visualizar los primeros.

Tipos de herramientas de escritorio
=====================================================

No todas las aplicaciones de escritorio presentan las anteriores funcionalidades de igual modo. Es frecuente que ciertos Sistemas de Información Geográfica tengan una fuerte componente de análisis, pero que otras de las funciones principales, como por ejemplo la edición, no se presenten tan desarrolladas. 

Un caso particular es el de aquellos SIG de escritorio que centran la gran mayoría de sus capacidades en el terreno de la visualización, permitiendo un uso de los datos geográficos similar al que corresponde a un mapa clásico, donde el trabajo con este se basa fundamentalmente en el análisis visual. 

Comenzaremos por estos últimos para dar un breve repaso a los principales tipos de aplicaciones de escritorio en función de sus capacidades.

.. _visoresyexploradores:

Visores y exploradores
--------------------------------------------------------------


Las aplicaciones SIG de escritorio cuya función principal es la visualización se conocen generalmente como *visores* o *exploradores*, y en la actualidad representan una fracción importante del conjunto total de herramientas SIG de escritorio. 

En ocasiones, se trata de aplicaciones en el sentido habitual, las cuales presentan capacidades reducidas de análisis y edición, y cuyo objetivo no es otro que el permitir la visualización de cartografía, sin incorporar las restantes posibilidades del SIG. En otros casos, son versiones simplificadas de soluciones SIG de escritorio más complejas, desarrolladas como alternativas más asequibles (en términos de dificultad de manejo y aprendizaje, y también a veces en términos de coste).

Una forma también habitual en la que se presentan los exploradores son como herramientas de apoyo a unos datos espaciales particulares. Para entender este tipo de enfoque, debe pensarse que un mapa clásico puede visualizarse de igual modo con independencia del uso que se le pretenda dar y de la experiencia y formación de quien lo usa. Con un conjunto de datos espaciales en forma de una o varias capas, no sucede lo mismo, ya que estos datos no son un elemento *visual* de por sí. Es necesario utilizar un SIG para poder visualizarlos.

Un usuario experimentado no encontrará problemas en manejar un SIG de escritorio complejo, pero un usuario con poca experiencia que lo único que desee sea *ver* la cartografía y explorarla visualmente (del mismo modo que un excursionista casual puede querer emplear un mapa topográfico) encontrará el entorno de ese SIG demasiado complejo y con elementos que, en su mayoría, no le son necesarios. Con la disponibilidad creciente de cartografía y la popularización de las tecnologías SIG, este tipo de usuarios ha crecido notablemente, y las aplicaciones adaptadas a sus necesidades han ido apareciendo y popularizándose igualmente de forma progresiva.

Así, existen visores que ocupan un papel secundario como parte de un producto compuesto que incluye al propio programa y a los datos en sí. Ejemplos muy claros y muy populares son aplicaciones como Google Earth (ver página \pageref{GoogleEarth} y figura :num:`#figgearth`), que permite que cada usuario incorpore su propia información para visualizar esta, pero cuyo mayor interés es el acceso a una enorme base de datos de imágenes de satélite con cobertura global. De esta forma, la aplicación puede utilizarse para explorar una área deseada, sin necesidad de disponer junto con ella de datos para dicha zona, puesto que por defecto la aplicación accede a una base de datos de imágenes que van indisolublemente unidos a ella.

.. _figgearth:

.. figure:: gearth.*
	:width: 650px
	:align: center

	Aspecto de un globo o visor tridimensional (GoogleEarth).


El usuario puede también añadir sus propias capas y usar estos visualizadores de la misma manera que emplea las capacidades de visualización de un SIG de escritorio más rico en funcionalidades, pero parte del interés de la aplicación no está solo en sus capacidades, sino en los datos que tiene vinculados y que permiten emplear estas.

En otros casos, un organismo o empresa puede generar un conjunto de capas bien a partir de algún tipo de análisis o de cualquier otra metodología, y opta por distribuir estas acompañadas de un visor que permita un primer acceso a los datos. Todas esas capas podrán ser empleadas dentro de un SIG que soporte los formatos de archivo en el que estas se hayan almacenado, pero aquellos usuarios que no dispongan de un SIG podrán igualmente efectuar consultas básicas y explorar la cartografía haciendo uso del visor incorporado.

En líneas generales podemos enumerar las siguientes características de los visores:


* Interfaz simple en la que tienen un peso mayoritario las herramientas de navegación.
* Capacidades de lectura de datos, pero no de escritura.
* Reducidas o nulas capacidades de edición y análisis.
* Enfocadas a usuarios no especializados.


Encontramos dos grupos básicos de visores, en función de qué tipo de visualización principal incorporan: planos y tridimensionales (globos). Mientras que una aplicación SIG de escritorio completa puede presentar los dos tipos de representación, y sobre ambas implementar las restantes funcionalidades tales como la edición o el análisis (aunque, como ya dijimos, en mayor proporción sobre las vistas bidimensionales), los visores habitualmente reducen sus capacidades de representación a una de estas variantes.

Los visores bidimensionales, aunque sin alcanzar el enfoque especializado de una aplicación completa, se orientan más al usuario con cierto conocimiento del ámbito SIG, mientras que la tendencia en los tridimensionales es a ofrecer herramientas de acceso a datos geográficos con una apariencia atractiva. Ello, no obstante, no implica que estos visores carezcan de utilidad en el ámbito científico, siendo igualmente herramientas válidas para todo tipo de investigación o trabajo que incorpore cierta componente geográfica. De hecho, la popularización de este tipo de visores ha supuesto un gran acercamiento de los datos geográficos y las capacidades SIG a toda una amplia comunidad de usuarios, incluyendo los del mundo científico, permitiéndoles realizar sus trabajos de forma más adecuada. Esto es especialmente cierto con aquellos visores que se hallan vinculados a bases de datos particulares, como ya se ha comentado, ya que permiten explotar los datos de dichas bases y proporcionar a todo usuario un sustrato de información geográfica sobre la que trabajar.


Soluciones de escritorio completas
--------------------------------------------------------------

La aplicación SIG más habitual, y la que constituye la herramienta básica para el desarrollo de un proyecto SIG, es aquella que reúne en un único producto todas las funciones básicas que hemos visto en este capítulo. Con las lógicas diferencias en cuanto al grado de funcionalidad de estas según el enfoque de la aplicación, una aplicación SIG de escritorio completa debe permitir la lectura de los datos, la creación y modificación de estos con sus capacidades de edición, su visualización, la realización de análisis con ellos y la generación de resultados cartográficos ya sea a partir de los datos originales o de datos generados en los procesos de análisis. Con todas estas capacidades, una herramienta SIG de escritorio constituye una solución completa para todo tipo de proyectos SIG, y puede dar respuesta a todas las necesidades que en ellos se presentan.

Como ya vimos en el capítulo introductorio de esta parte, y también en el capítulo :ref:`Bases_datos` dedicado a las bases de datos, la forma de abordar la implementación de las distintas capacidades ha ido variando a medida que se iban desarrollando los SIG. En la actualidad, encontramos tanto SIG de escritorio que implementan en una sola aplicación central todas las funcionalidades base, como grupos de aplicaciones muy interrelacionadas que implementan por separado cada una de dichas funcionalidades. Tanto en uno como en otro caso, existen elementos sobre los que las distintas herramientas del SIG se apoyan, especialmente en lo relativo al acceso a datos. %Veremos más sobre ellos en el capítulo :ref:`Otros_tecnologia` dentro de esta misma parte.

Pese a que incorporan toda la gama de funcionalidades base, las soluciones de escritorio completas no cubren las necesidades de todo usuario de SIG. La convergencia a la que tienen este tipo de aplicaciones, comentada en el capítulo introductorio de esta parte del libro, no ha sido, como ya entonces se mencionó, completamente lograda en la actualidad. El problema no es ya un problema de integración de tecnologías, sino una dificultad relativa a la gran amplitud de la ciencia de los SIG. Resulta imposible reunir en una sola herramienta todas las capacidades que un SIG de escritorio puede incluir, y es por ello que todas las soluciones de escritorio presentan algún tipo de especialización, dando prioridad a algún área respecto a las restantes.

Una división que perdura, aunque en mucho menor medida que en los primeros SIG, es la existente entre SIG ráster y SIG vectoriales, especialmente en lo relativo al análisis. Un usuario que trabaje con datos espaciales como los correspondientes, por ejemplo, a información catastral, utilizará para su labor un SIG de escritorio distinto al que usara alguien cuyo trabajo implique mayoritariamente la realización de análisis del terreno o la creación de modelos geográficos, a pesar de que ambas soluciones probablemente incorporen capacidades tanto en el ámbito ráster como en el vectorial. El alcance de estas, no obstante, será distinto en cada caso.

Incluso en caso de presentar una orientación principalmente hacia los datos de tipo ráster, existen también enfoques distintos dependiendo principalmente del tipo información que se vaya a manejar. Una división fundamental es la existente entre aquellas aplicaciones destinadas al manejo de imágenes y aquellas cuyo elemento principal de trabajo son las capas ráster con otro tipo de valores, tales como MDE o capas similares.

Las imágenes, especialmente si se trata de imágenes de satélite, van a constar de una serie de bandas cuyo número puede ser muy elevado, lo que requiere unas herramientas particulares para su manejo. Asimismo, gran parte de las funciones que vimos en el capítulo :ref:`Procesado_imagenes` tales como las relativas a la corrección de imágenes, no tienen aplicación para otro tipo de capas (no tiene sentido aplicar una corrección geométrica a un MDE o una capa de pendientes, ya que estos datos necesariamente provienen de fuentes ya conveniente corregidas), por lo que en cierto modo pueden considerarse especificas de este campo, el de las imágenes, si bien es cierto que se trata de un campo de gran amplitud.

Por el contrario, capas como el propio MDE u otras similares solo contienen una única banda, y el tipo de operaciones que se desarrollan sobre ellos es bien distinto. Con objeto de simplificar estas operaciones, la estructura de estas aplicaciones ha de enfocarse hacia alguna de estas variantes, dándole prioridad sobre la otra. Por ello, las herramientas de escritorio que se orientan al trabajo con imágenes incorporan en general pocas o nulas herramientas en áreas como el análisis del terreno, mientras que aquellas que sí tratan estos análisis no incluyen salvo las funciones más simples para el manejo de imágenes (realces, ajuste de contraste, etc.), pero no las más específicas.

En realidad, una aplicación de escritorio global que cubriera todas estas funcionalidades no sería práctica desde el punto de vista de su uso, pues sería excesivamente compleja. Es poco probable, igualmente, que un mismo usuario requiera un entorno profesional productivo en todas ellas, y más habitual sin embargo que centre su trabajo en un área concreta.

Resumen
=====================================================

Las herramientas de escritorio son la forma más clásica de los SIG. Entendemos como tales a aquellas herramientas ciertamente complejas que permiten llevar a cabo las tareas básicas de un SIG en sentido tradicional, como son el manejo de datos espaciales y el trabajo con los mismos. 

Podemos distinguir cuatro funcionalidades básicas que aparecen representadas en mayor o menor medida en un SIG de escritorio: visualización, edición, análisis y generación de cartografía.

En función del grado de desarrollo e implementación en que las anteriores funcionalidades se encuentren en un SIG de escritorio, distinguimos distintas formas de estas herramientas. La división más genérica es aquella que distingue las herramientas pensadas para un trabajo completo en todas las distintas fases de un proyecto SIG de aquellas orientadas a la representación y exploración visual de los datos geográficos. Estas últimas representan un enfoque más reciente, y en la actualidad están contribuyendo de manera muy notable a la expansión de las tecnologías SIG fuera del ámbito más especializado.

.. rubric:: Footnotes

.. [#fn2] Básicamente, estos servicios van a permitir acceder a datos geográficos que no están en nuestro ordenador, del mismo modo que accedemos a textos o imágenes a través de un navegador Web