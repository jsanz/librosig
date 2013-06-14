.. _Ecologia:

**********************************************************
Ecología
**********************************************************



Los SIG son herramientas básicas para biólogos y otros profesionales que analizan las comunidades animales o vegetales, o cualquier otro elemento del medio natural. Tratándose de elementos vivos y dinámicos, presentan casos de uso interesantes para demostrar las capacidades de los SIG de cara al estudio de su evolución y desarrollo a lo largo del tiempo.

En este capítulo detallaremos algunas formulaciones particulares que estas disciplinas aportan a los SIG, y el uso que de ellas se hace en las situaciones y aplicaciones más habituales .


Introducción
=====================================================

Los SIG son herramientas básicas en la actualidad dentro del campo de la ecología, algo que no debería resultar extraño teniendo en cuenta la importancia de la información geográfica en este ámbito. Del mismo modo que la cartografía ha sido una parte fundamental para el estudio del medio natural y de las comunidades animales y vegetales, con la aparición de los SIG estas tareas han pasado a adoptar todas las funcionalidades de estos, al tiempo que las han aprovechado para desarrollar nuevas formas de explotar la información geográfica.

El uso que se hace de los SIG en el campo de la ecología es en buena parte analítico, tratando de extraer información a partir de los datos de que se dispone, ya sean estos acerca del medio, de una especie dada o de una comunidad natural de cualquier tipo. Este volumen de datos es, no obstante, grande en muchos casos, y el uso de SIG permite una gestión adecuada y, muy especialmente, una presentación óptima de estos. Mientras que el análisis es una labor más técnica, la ecología genera productos de interés para un público menos especializado, y mostrar a este los resultados de esos análisis o bien los datos de partida directamente a través de cartografía es una solución idónea en la que los SIG se demuestran de gran ayuda. 

Veremos en este capítulo dos bloques de conocimiento significativos dentro del uso que se le da a los SIG en el terreno de la ecología. Por una parte, la arquitectura del paisaje, un tipo de análisis en el que fundamentalmente se estudian las formas y patrones espaciales de los distintos elementos que forman un entorno natural o paisaje. Es decir, un análisis de cómo está compuesto espacialmente ese paisaje. Por otra, veremos los denominados *modelos predictivos*, que conforman un análisis estadístico más centrado en la componente temática de la información geográfica. Al aplicarlos en un contexto espacial, nos van a permitir la elaboración de cartografía de potencialidad, útil como veremos para diversas tareas.


Ecología del paisaje
=====================================================


En ecología se entiende por paisaje a un entorno natural dado, con unas características concretas fruto de la interacción de múltiples factores como el clima, la presencia humana, las comunidades animales y vegetales, o el relieve, entre otros. No se trata, por tanto, del concepto estético de paisaje como lo entendemos en su acepción habitual, sino un concepto geográfico y ecológico que hace referencia a cómo todos esos elementos que actúan sobre una porción de terreno definen sus características.



El resultado de todas esas acciones es un conjunto heterogéneo de unidades que ponen de manifiesto la forma distinta en que sobre las distintas partes del paisaje actúan los elementos que le dan forma. No es difícil ver que esta heterogeneidad es una heterogeneidad espacial, y que las fuerzas que la originan también tienen un carácter espacial igual, por lo que su estudio y análisis es susceptible de aprovecharse en gran medida de las capacidades de un SIG.

El estudio del paisaje definido según lo anterior conforma la denominada *ecología del paisaje*, una disciplina que analiza tanto la estructura como el funcionamiento del paisaje como entidad. SIG y ecología del paisaje van íntimamente unidas desde los inicios de ambas disciplinas, y del conjunto de técnicas que se utilizan para el estudio del paisaje, una buena parte han sido desarrolladas sobre la base del SIG como herramienta a emplear para su aplicación.

Según  :cite:p:`Forman1983Bioscience`, la ecología del paisaje es el *estudio de las interacciones entre los aspectos temporales y espaciales del paisaje y sus componentes de flora, fauna y culturales*. Este estudio se puede entender como suma de tres tipos distintos de análisis:



* Análisis de las propiedades espaciales de las unidades del paisaje y sus relaciones espaciales. Estas unidades forman *manchas* sobre el conjunto total del paisaje, y la forma en que estas se distribuyen sobre el terreno condiciona muchos aspectos del paisaje cuyo estudio es altamente relevante, así como las características espaciales de cada una, tales como su forma o el área que ocupan.
* Análisis de la interacción entre las unidades. Cada unidad no es un elemento estanco, y se producen flujos entre ellas que también son de interés para su caracterización y la del paisaje como entidad global.
* Análisis de la dinámica temporal del paisaje. Es decir, de la evolución de ese conjunto de unidades a lo largo del tiempo y los cambios que se producen en su estructura.


De cara a su estudio en un SIG, el primer punto de los anteriores es el que tiene mayores posibilidades de aprovechar las capacidades de este, puesto que se trata de un análisis netamente espacial. Los otros dos, no obstante, también pueden llevarse a cabo en un SIG. Aunque no los veremos aquí y nos centraremos en el estudio de las relaciones espaciales, en el apartado :ref:`Cambio_usos_suelo` detallaremos los modelos de cambio de usos del suelo, cuyos fundamentos son aplicables de igual modo para estudiar el cambio en las unidades del paisaje. Estos modelos, de hecho, constituyen herramientas para el estudio del paisaje, ya que el uso de suelo es un factor más de la caracterización de las unidades paisajísticas.

El análisis de las relaciones espaciales entre las unidades del paisaje persigue obtener una caracterización cuantitativa de este, y lleva esto a cabo analizando diferentes propiedades espaciales de las unidades por separado, así como de cada una junto a las circundantes, y a nivel global de todo el paisaje. Esto permite obtener resultados que pueden relacionarse con cada una de las funciones que las unidades de paisaje cumplen, y dar una caracterización de este a distintas escalas. Por su propia naturaleza, el estudio del paisaje es un ámbito en el que el concepto de escala de análisis es vital para que los resultados tengan sentido.

Toda la información que se maneja en el estudio espacial de las unidades del paisaje es de tipo categórico, ya que no nos interesan (al menos con carácter fundamental) las características de esas unidades, sino saber qué unidades hay y los límites de cada una. Aunque la información categórica resulta en general más conveniente manejarla en forma vectorial (como polígonos en este caso), el carácter analítico de las tareas que se van a desarrollar hace que el modelo ráster sea más idóneo desde ese punto de vista. Asimismo, las capas categóricas a emplear se obtienen frecuentemente mediante técnicas de clasificación a partir de imágenes, con lo que originalmente se crean como capas ráster. Por todo esto, la aplicación de las formulaciones que seguidamente veremos puede encontrarse tanto sobre una base ráster como sobre una base vectorial, siendo ambas alternativas posibles.

En esencia, y de un modo muy simplista, podemos decir que la labor que vamos a realizar con un SIG para el estudio del paisaje consiste en el análisis de los patrones que aparecen en un mapa con información categórica, y la definición de las características de cada unidad y de cada categoría de las presentes. Este análisis puede enfocarse desde dos concepciones teóricas distintas:


* La Biogeografía de Islas  :cite:p:`MacArthur1967Princeton`. Considera cada unidad como una isla, en el sentido de que en su interior puede darse algún tipo de proceso ecológico, mientras que en las áreas que la rodean el terreno es *hostil* para este. Este modelo supone por tanto una concepción dicotómica del paisaje al analizar una unidad o una clase dada. Esto permite un análisis sencillo, centrado en las características propias de cada una de esas unidades (las islas) frente al fondo formado por el resto de estas (el *mar*). No obstante, es un enfoque que implica una simplificación excesiva, y que no tiene en cuenta la interacción entre las unidades ni las características del fondo.
* El modelo del mosaico paisajístico. Se considera el paisaje como un conjunto de unidades interconectadas y se tiene en cuenta la heterogeneidad de estas. En lugar de enfocar el estudio sobre las unidades en sí, lo hace sobre un proceso dado y sobre cómo este tiene lugar para un paisaje con una configuración y unas propiedades dadas. Es un modelo más real que el anterior, ya que la respuesta de los organismos sobre un tipo de unidad de paisaje no es en realidad únicamente de dos tipos posibles (isla o mar), sino que pueden existir términos intermedios.


El número de parámetros que se han definido para el análisis cuantitativo del paisaje (conocidos como *métricas* del paisaje) es muy elevado, y veremos a continuación solo algunos. El lector interesado en profundizar en el tema puede consultar  :cite:p:`fragstatsMetrics`. Para una definición completa de todas estas métricas, la referencia a consultar es  :cite:p:`fragstatsMetricsDefinition`.

Las métricas del paisaje pueden clasificarse según dos criterios: la escala a la que se aplican y el tipo de propiedades que describen. Según la escala encontramos tres tipos:


* Metricas de unidad (*Patch metrics*). Analizan las unidades del paisaje de forma independiente del resto.
* Métricas de clase. Analizan las manchas que corresponden a una misma clase, es decir, un conjunto de polígonos disjuntos con las mismas características.
* Métricas del paisaje. Analizan el paisaje en su totalidad, como un conjunto de manchas que teselan el espacio.


Las métricas de unidad o de clase pueden integrarse para dar información global del paisaje mediante el uso de estadísticos tales como la media, la media ponderada, la desviación típica o el rango del conjunto de manchas o clases, según corresponda. 

En referencia a las propiedades que describen, los siguientes son los grupos principales:


* Métricas de composición. Se aplican tan solo para el paisaje globalmente y reflejan la forma en que las distintas clases están representadas en este.
* Métricas de configuración. Se aplican a los distintos niveles de escala y recogen la configuración espacial de las distintas unidades. 


Veremos algunos de los principales representantes de estos dos grupos a continuación. 

Métricas de composición
--------------------------------------------------------------

Las métricas de composición estudian la variedad y la abundancia de las distintas clases dentro del paisaje. Algunas de las principales métricas de este tipo son las siguientes:


* Abundancia. La abundancia es uno de los parámetros más sencillos de calcular, pero que más información aporta acerca del paisaje. Simplemente se expresa como el porcentaje de área que cada clase supone en el total del paisaje.
* Riqueza. La riqueza indica el número total de clases distintas que el paisaje contiene. Pese a ser también un parámetro de gran simpleza, su significado es muy importante para la caracterización del paisaje. Por ejemplo, y puesto que muchos organismos se asocian con un tipo concreto de clase (un hábitat particular definido por esta), puede asumirse que una mayor riqueza en términos de estas clases supone a su vez una mayor riqueza en lo que a especies respecta. 

 La riqueza tiene una relación directa con la escala, ya que áreas mayores presentan mayor heterogeneidad, lo que se traduce en mayor riqueza. Comparar la riqueza de paisajes de diferente tamaño puede ser, por tanto, problemático.

 Su propia simplicidad es también el principal punto débil de está métrica, ya que un paisaje compuesto por 3 clases distintas representadas cada una por un 33\% de la superficie no es igual que un paisaje en el que una de ellas ocupara un 98\% y las restantes un 1\% cada una. Aunque los valores de riqueza sean los mismos, la estructura de las comunidades animales y vegetales será muy distintas en ambos casos, por lo que la información a este respecto que puede inferirse debe considerarse en conjunto con otras métricas que aporten información adicional, tales como las detalladas a continuación.
	
* Equitatividad. La equitatividad es el concepto contrario a la dominancia. En un paisaje existe equitatividad cuando todas las clases se encuentran representadas de igual modo. Por el contrario, si una de ellas ocupa un área mayor que las restantes (como en el caso citado anteriormente), existe dominancia de esta. Existen varios índices que miden la equitatividad, entre los que destacan los dos siguientes:

	* Índice de equitatividad de Shannon. Se calcula según la expresión
	
	 .. math::

	 	E = -\frac{\sum_{i=1}^{s}{P_i\ln{P_i}}}{\ln{s}}

    siendo :math:`s` el número total de clases presentes y :math:`P_i` la proporción ocupada por la clase i--esima en el paisaje.
	
	* Índice de equitatividad de Simpson. Según la expresión
	
	 .. math::

	 	E = \frac{1-\sum_{i=1}^{n}{P_i^2}}{1 - \frac{1}{n}}

	donde :math:`n` es el número total de clases.

 En ambos casos, la dominancia puede calcularse como :math:`1 - E`.
	
 Ambos índices varían de 0 a 1.
	

* Diversidad. La diversidad tiene relación con la equitatividad y la riqueza, y se calcula en función de estas variables de diversas formas, según sea la importancia asignada a cada una de ellas. Algunas de las fórmulas más comunes son las siguientes:
	

	* Índice de diversidad de Shannon. El más usado, responde a la expresión
	
	 .. math::

	 	H = -\sum_{i=1}^{s}{P_i\ln{P_i}}


	* Índice de diversidad de Simpson. Calculado según la siguiente expresión:
		
	 .. math::

	 	D = 1-\sum_{i=1}^{n}{P_i^2}




Puede verse que los índices de diversidad corresponden al numerador de los de equitatividad presentados anteriormente. El denominador es el valor de la diversidad máxima.



Métricas de configuración
--------------------------------------------------------------

Las métricas de configuración son más abundantes que las de composición, a la vez que más variadas. Las siguientes son algunas de las características que pueden cuantificarse mediante este tipo de métricas.


* Tamaño. El parámetro más básico, empleado a su vez como parte de otras métricas. Pueden calcularse estadísticos del tamaño de unidad para todo el paisaje o bien para una clase dada. También puede emplearse como densidad, expresando el número de distintas unidades por unidad de área.

* Complejidad de forma. Existen muchas métricas en este grupo, la mayoría de las cuales intentan describir la complejidad de la forma geométrica de la unidad. En muchos casos esto se lleva a cabo mediante relaciones perímetro/área, y comparando estas con las correspondientes a una figura geométrica regular (circulo o cuadrado generalmente) de la misma área. Aunque la forma de la unidad puede relacionarse con el comportamiento de ciertas especies animales y vegetales (actividad, migración, colonización de la unidad, etc.), la principal implicación de estos parámetros es en relación con el efecto de borde (recuérdese lo visto en :ref:`EfectoBorde`). La dimensión fractal de la unidad es también un parámetro empleado con frecuencia. Otras métricas más elaboradas pueden calcularse igualmente, aunque la interpretación de su significado en términos ecológicos no es tan clara.

* Bordes. Además de la relación directa que guarda con las métricas de complejidad de forma, el efecto de borde puede medirse directamente con otras métricas. La más simple de todas ellas es la mera longitud total de los bordes, es decir, de los perímetros de las distintas unidades, ya sea de forma individual o agrupadas por clases o paisaje total. También puede expresarse como densidad, en longitud de borde por unidad de de área.

* Área central. Estas métricas tratan de cuantificar el área de la unidad libre de efecto de borde. Para ello, se elimina un área dada situada a una distancia del borde menor que un umbral establecido, y se cuantifica el área restante. Estas métricas integran la complejidad de la forma, el área y los efectos de borde en un único valor descriptivo. Se entiende que esta área central es la que es de interés para el estudio de ciertos procesos o el comportamiento de una comunidad concreta.

* Aislamiento/proximidad. Las métricas de esta clase cuantifican la tendencia de las unidades de una misma clase a aparecer en el paisaje cercanas entre sí o bien separadas. Una forma de llevar esto a cabo es mediante el cálculo de la distancia al vecino más cercano, es decir, a la mancha de paisaje de la misma clase que se encuentra a una distancia menor. Estas distancias para cada unidad de una clase pueden promediarse, ya sea asignando peso a cada una en función del área correspondiente a la unidad en cuestión, o bien considerando el mismo peso para todas.

 Como es lógico pensar, este cálculo de las distancias entre unidades no se lleva a cabo de la misma manera si trabajamos con datos ráster o vectoriales, y las formulaciones difieren notablemente. Conservan, no obstante, la misma base teórica, y la interpretación de los resultados es idéntica.

* Conectividad. La conectividad cuantifica el grado en que el paisaje impide o facilita el flujo entre las distintas unidades. La pérdida de conectividad es una de las razones más importantes para la pérdida de hábitat. Si el hábitat se fragmenta y no existe conexión entre las distintas comunidades de una especie, esto puede llevar a un menor número de individuos en cada unidad de las habitadas por dicha especie, y en última instancia incluso causar su extinción.
	
 Para estudiar la conectividad, es fundamental definir qué condiciones han de cumplir dos unidades de una clase dada para considerarse como conectadas, lo cual depende del proceso que pretendamos estudiar, así como del resto de unidades. Se ha de trabajar con una *conectividad funcional* entre unidades. La distancia es un parámetro fundamental a considerar, sin duda, aunque no el único. Una distancia insalvable para un pequeño reptil puede no constituir un problema para un ave o para la dispersión de las semillas de un árbol. Asimismo, para una especie que habite en un hábitat boscoso, cruzar una determinada distancia de pasto puede ser perfectamente viable, mientras que una distancia menor ocupada por agua puede constituir una barrera insalvable que no permite que exista conectividad.
	
 El conjunto de unidades y sus conexiones funcionales constituye una red que puede analizarse con algunas de las ideas que ya conocemos a este respecto, así como definirse con parámetros derivados de la teoría de grafos (Figura :num:`#figconectividad`).
	
.. _figconectividad:

.. figure:: Conectividad.*
	:width: 650px

	Para el análisis de conectividad, el conjunto de unidades de una clase se convierten en una red que define la conectividad funcional entre ellas.





* Contraste. El contraste cuantifica la diferencia relativa entre cada unidad y las contiguas. Una zona de bosque rodeada de una zona de pasto no constituye el mismo tipo de paisaje que esa misma zona rodeada de áreas urbanas o de agua. Una forma de calcular métricas de contraste es aplicar las ideas de las métricas de borde, pero asignando pesos a estos en función de la diferencia que exista entre las dos unidades que cada borde delimita.

* Contagio. El contagio expresa la tendencia de las unidades de una clase a formar grupos compactos, o bien a estar dispersas a los largo del paisaje.


*Software*
--------------------------------------------------------------

Sin duda alguna, el software más extendido para el análisis del paisaje es FRAGSTATS  :cite:p:`referenciaFragstats`, referencia en su campo y del que derivan la mayor parte de parámetros que acabamos de ver. Existen otras aplicaciones que toman elementos de FRAGSTATS e implementan parte de las métricas que este calcula (muchas de ellas son sumamente sencillas y su implementación no es costosa), y algunos SIG incluyen funcionalidades de análisis basadas en esas ideas. No obstante, es habitual encontrar componentes en algunos de los SIG más habituales que permiten usar FRAGSTATS directamente desde esos SIG.

Como aplicación, FRAGSTATS no es un SIG, aunque dispone de capacidades para leer capas de entrada tanto ráster como vectoriales en formatos que también pueden leerse en buena parte de los SIG de escritorio más populares. La interfaz es sencilla de emplear, pero no existen elementos como los que encontramos en uno de esos SIG para el manejo de capas. La figura :num:`#figfragstats` muestra la interfaz de ajuste de parámetros de FRAGSTATS como aplicación independiente.

.. _figfragstats:

.. figure:: Fragstats.*
	:width: 650px

	Interfaz de FRAGSTATS





Las soluciones que enlazan FRAGSTAT con algún SIG permiten que pueda ejecutarse el programa directamente desde el SIG, alimentándolo con las capas abiertas en este en un momento dado, y completando esta información con los parámetros que se requieran para la ejecución, introducidos en interfaces diseñadas a tal efecto.

Los resultados generados por FRAGSTATS son en su gran mayoría en forma de tablas, y es habitual que, una vez el programa ha terminado su trabajo, el SIG a través de su componente de enlace tome esas tablas y las introduzca en él de la manera más conveniente, o al menos facilite desde su interfaz la consulta de estas.

Esta integración dentro de un SIG permite combinar las métricas del paisaje con algunas de las posibilidades adicionales que ofrece un SIG. De especial relevancia resultan las capacidades de modelización, ya que puede modelizarse la evolución del paisaje y caracterizar cada una de las etapas mediante las correspondientes métricas. Veremos en el apartado :ref:`Cambio_usos_suelo` algo más acerca de este tipo de modelización.

Algunas aplicaciones más particulares para el análisis del paisaje se centran en determinados aspectos de la caracterización de este. Por ejemplo, *Conefor Sensinode*  :cite:p:`Saura2009EMS` es una aplicación para el análisis de la conectividad basada en un uso avanzado de elementos de la teoría de grafos, así como para el estudio de la disponibilidad de hábitats.

.. _Modelos_predictivos:

Modelización de hábitats. Modelos predictivos
=====================================================



Uno de los análisis más interesantes en el campo de la ecología, y en el que los SIG aportan mayores posibilidades, es la modelización de hábitats. Este tipo de análisis pretende establecer qué tipo de condiciones son las más adecuadas para una determinada especie animal o vegetal, y con ello poder establecer en qué zonas puede estar presente dicha especie y estimar la probabilidad de encontrarla en ellas teniendo en consideración las condiciones allí presentes. 


Este tipo de información puede ser utilizada para predecir la presencia o ausencia de individuos de la especie en unas zonas de interés, para analizar si resulta viable la introducción de una especie en una concreta, o incluso para tratar de analizar la distribución pasada de una especie y la evolución que desde entonces ha sufrido dicha distribución.

Es fácil ver que existen similitudes entre el estudio del paisaje y la modelización de hábitats, ya que el paisaje condiciona que una especie pueda o no ocupar una determinada zona, y el éxito con que esto sucede, como de hecho hemos mencionado en el apartado anterior de este capítulo. No obstante, el tipo de modelización que tratamos ahora es muy distinto en su enfoque y metodología, y veremos que se trata de técnicas distintas con un objetivo también diferente en lo que a los resultados buscados respecta.

En general, los modelos de hábitat que vamos a ver toman una serie de variables que se supone tiene influencia en el comportamiento de la especie, estudian los valores de esas variables en los puntos donde se sabe con certeza que la variable está presente, y posteriormente intentan en base a esos datos valorar la idoneidad de una serie de zonas para acoger igualmente a dicha especie. Además de usar información sobre la presencia de una especie en una determinada localización, pueden emplearse datos de ausencia para indicar aquellos lugares en que la especie no aparezca. No obstante, y mientras que una zona de presencia se puede caracterizar sin ninguna duda como tal, la ausencia puede deberse a que, simplemente, no se ha observado, o bien a algún hecho particular ajeno a las variables que se consideran para el análisis. Crear registros de ausencia es, en general, una labor difícil  :cite:p:`Jarvis2005ME`.

El resultado de esta modelización es una cartografía de distribución potencial de la especie estudiada, que nos dice la probabilidad de que esa especie esté presente en los distintos puntos de un área analizada, a partir de los datos conocidos para unos emplazamientos concretos (aquellos definidos como puntos de presencia o ausencia, y empleados como entrada del modelo). Estos modelos se conocen como *modelos predictivos* o también *modelos de idoneidad*.

Formalmente, el modelo es una función de probabilidad :math:`P(i)`, según

.. math::

	P(i) = f(x_1,x_2,x_3,\ldots,x_n)




donde :math:`f` es la función que asigna la probabilidad de aparición de la especie en función de una serie de :math:`n` variables, y :math:`x_1,x_2,\ldots,x_n` son los valores de esas variables.

Puesto sobre el contexto de un conjunto de capas con tales variables (puesto que han de cubrir el espacio estudiado, estas serán de tipo ráster preferentemente), el modelo predictivo nos proporciona esa cartografía de distribución antes mencionada, sin más que aplicarlo sobre todas las celdas de las capas de entrada. La presencia del SIG ha contribuido decisivamente al desarrollo de este tipo de modelos, y el avance que se ha dado en las herramientas SIG ha favorecido la aparición de nuevas metodologías para la creación de cartografía de tipo predictivo.

Si estudiamos la forma de proceder de este tipo de análisis, es claro que guarda una gran similitud con los procedimientos estadísticos que vimos en el apartado :ref:`Clasificacion`, donde tratamos los métodos de clasificación supervisada. Partiendo de un conocimiento acerca de unas localizaciones particulares (en este caso son puntos de presencia/ausencia, entonces eran áreas de entrenamiento), se trata de clasificar las restantes dentro de un marco geográfico. La clasificación en este caso sería en dos únicas clases (hay presencia o no de la especie), aunque, puesto que usamos la función de probabilidad, se asemejaría más al tipo de clasificación que denominábamos *débil*, el cual nos ofrece valores en función de los cuales podemos posteriormente discriminar y establecer si la presencia de la especie puede asumirse o no.

Las similitudes entre la aplicación de modelos predictivos y técnicas de clasificación supervisada no es solo aparente, sino que sus fundamentos son en gran medida los mismos y emplean herramientas de análisis comunes. No obstante, un modelo predictivo tiene sus propias características y un objetivo más acotado que el de la clasificación genérica, por lo que existen algunas diferencias y soluciones particulares, que serán las que veamos en esta sección. Por ejemplo, el uso de variables cualitativas no es tan habitual en los algoritmos de clasificación (las metodologías que fueron explicadas en su momento solo trabajan con variables cuantitativas), mientras que en los modelos predictivos se contempla en algunos de ellos el uso de todo tipo de variables. En general, estos modelos están, como parece lógico, adaptados al hecho particular que modelizan.

A la hora de su operativa dentro de un SIG, usaremos un conjunto de capas ráster y una capa vectorial de puntos que debe contener un campo que especifique si el punto es de presencia o ausencia. Las capas con las variables independientes pueden ser de todo tipo, y vendrán condicionadas a las entradas que el modelo requiera. Algunos modelos trabajan con capas cualesquiera y las estudian todas por igual como condicionantes del comportamiento de la especie. Otros exigen una cierta serie de capas concretas, ya que no emplean estas directamente como variables para los análisis correspondientes, sino otras intermedias que son calculadas a partir de ellas.

Lógicamente, el uso de unas u otras variables esta condicionado a la escala del estudio a realizar. Un modelo de distribución para una extensión grande de territorio puede asumir que el clima es el factor principal a considerar. Para un estudio local, sin embargo, el clima sigue teniendo importancia, pero otras circunstancias han de considerarse igualmente, en especial el relieve  :cite:p:`Guisan2000EM`.

Algunos modelos de uso frecuente
--------------------------------------------------------------

Un modelo sencillo es el denominado BIOCLIM  :cite:p:`BIOCLIM`, que parte de una serie de parámetros climatológicos, asumiendo por tanto que el clima es el único factor que condiciona el comportamiento de la especie. Estos parámetros, no obstante, son utilizados para el cálculo de otras variables biológicamente  más significativas, y es sobre estas sobre las que se opera. La técnica de clasificación de BIOCLIM es en realidad un método de paralelepípedos como el que vimos en :ref:`Paralelepipedos`, ya que calcula el hipercubo delimitado por un umbral :math:`x`, de tal forma que la dimensión de ese hipercubo en cada eje es el rango de los valores de la variable correspondiente a dicho eje, recortado en un tanto por ciento :math:`x`. Un valor habitual del umbral es 5\%, de tal modo que la dimension de cada eje se sitúe entre los valores del 5\% y el 95\% del rango para la variable correspondiente.


Se trata de un modelo simple, que sin embargo tiene muchas desventajas debido a las condiciones que asume y a que no permite el uso de variables distintas de las climatológicas.

Algo más elaborado, aunque también dentro de la misma familia (ambos modelos solo requieren datos de ausencia), es el modelo DOMAIN, basado en la denominada *distancia de Grover*. Esta tiene la forma

.. math::

	G_{AB} = \frac{1}{n}\sum_{k=1}^n{\frac{|A_k-B_k|}{\mathrm{rango}(k)}}


donde :math:`n` es el número total de variables, :math:`A_k` el valor de la variable :math:`k` en el punto de presencia :math:`A`, :math:`B_k` el valor de la variable :math:`k` en la celda :math:`B` y :math:`\mathrm{rango}(k)` el rango de la variable :math:`k` en los puntos de presencia. La media de distancias de Grover entre una celda y todos los puntos de presencia nos da una idea de la diferencia entre estos últimos y la celda en cuestión. Como estadístico de similitud puede emplearse el valor :math:`1-G`.

Algunos modelos más complejos soportan el uso de datos de ausencia. Entre estos encontramos el modelo Maxent  :cite:p:`Phillips2006EM`, que crea él mismo puntos de pseudo-ausencia. Este modelo se basa en el principio estadístico de máxima entropía. Otro modelo habitual es GARP (*Genetic Algorithm for Rule set Production*), basado en algoritmos genéticos y con un funcionamiento mucho más complejo.  Los árboles de clasificación y regresión (*classification and regression trees*, CART) :cite:p:`Breiman1984WB` son otra técnica estadística que puede aplicarse para desarrollar modelos predictivos. Su uso en un SIG es, sin embargo, complejo  :cite:p:`Felicisimo2005Dehesa`, por lo que tienen menos valor a la hora de crear cartografía de distribución potencial.

Citar, por último, el uso de regresión logística múltiple como una alternativa habitual para plantear este tipo de modelos. La probabilidad en este caso viene dada por una fórmula del tipo

.. math::

	P(i) =  \frac{1}{1+e^{b_0 + x_1b_1+x_2b_2+\ldots+x_nb_n}}


donde :math:`x_1\ldots x_n` son los valores de las variables y  :math:`b_1 \ldots b_n` son constantes.

Para saber más sobre estos y otros modelos, puede consultarse  :cite:p:`GarciaMateo2008phd`.


Validación
--------------------------------------------------------------

La cartografía obtenida mediante la aplicación de los anteriores modelos debe validarse del mismo modo que sucedía en el caso de la clasificación. También en este caso se necesita información complementaria que no haya sido empleada para el modelo, tal como un segundo conjunto de puntos de presencia y ausencia sobre el que contrastar la bondad de los resultados generados.

Las técnicas a emplear son también similares a lo que vimos entonces para la clasificación, comparando aquello que se conoce en los puntos de ese segundo conjunto (si son ausencias o presencias) con lo que el modelo predice. Cruzando estas informaciones se pueden elaborar estadísticos que ayuden a valorar si el resultado que hemos obtenido es válido. Es decir, a valorar la consistencia del modelo.

El índice Kappa que ya conocemos es un estadístico empleado habitualmente, y se aplica de la misma forma que vimos. Otra forma frecuente de comprobar la bondad del modelo es mediante la denominada *curva ROC* (*Receiver Operating Characteristic*). Esta curva presenta en el eje de ordenadas valores de *sensibilidad*, y en el de abscisas valores de 1-*especificidad*. Estas variables se calculan según

.. math::

	\mathrm{sensibilidad} = \frac{VP}{VP+FP}\nonumber \\
	\mathrm{especificidad} = \frac{FN}{VN+FN}

siendo :math:`VP` los verdaderos positivos, :math:`FP` los falsos positivos,  :math:`VN` los verdaderos negativos y :math:`FN` los falsos negativos.

Para un umbral :math:`x` que define el punto de separación entre las zonas viables y no viables en función de los valores resultantes, se calculan los anteriores parámetros, obteniendo un punto de la curva. Variando el umbral entre 0 y 1 (los valores mínimo y máximo que pueden aparecer en la capa de distribución potencial, ya que como hemos visto esta expresa una probabilidad), se obtienen los distintos valores con que construir la curva ROC.
 
El aspecto típico de una curva ROC puede verse en la figura :num:`#figroc`.

El área bajo la curva así definida sirve como estadístico de comprobación, y sus valores están comprendidos entre 0,5 y 1. Un valor de 0,5 equivale a un modelo que clasificara al azar, mientras que 1 indica un ajuste perfecto del modelo.

.. _figroc:

.. figure:: CurvaROC.*
	:width: 650px

	Curva ROC.





*Software*
--------------------------------------------------------------

En lo que al *software* respecta, los modelos anteriores, así como otros que no se han citado, presentan soluciones muy variadas. Algunos de ellos, como BIOCLIM, se encuentran implementados en SIG y también como aplicaciones independientes. En este segundo caso, su uso es más sencillo y no requiere saber utilizar un SIG, aunque en la práctica esto sí que resulta necesario, ya que las capas de entrada han de crearse y prepararse, y el SIG es la herramienta para ello. La funcionalidad SIG que estas aplicaciones incorporan es tan solo la relativa a la lectura y escritura de los datos, debiendo recurrirse a una aplicación SIG para cualquier otro tipo de tareas. Estas incluyen no solo los pasos previos a la ejecución del modelo, sino también los posteriores, ya que la capa resultante no puede usarse en el programa, que se limita a producirla

La forma de introducir las capas es variable, usándose en algunos casos formatos SIG habituales, aunque en otros existen formas menos estandarizadas de aportar datos de entrada, en particular en lo referente a los puntos de ausencia/presencia, que incluso pueden tener que introducirse manualmente.

Algunas metodologías, como por ejemplo la regresión logística múltiple, no requieren para su aplicación más capacidades que las funciones del álgebra de mapas que ya conocemos, y es sencillo incorporarlas en un SIG. Otras, por el contrario, necesitan elementos más complejos. Esto suele suceder con los modelos más específicos, los cuales suelen tener algún tipo de *software* asociado que es el que se utiliza para aplicarlos. Maxent dispone de una aplicación del mismo nombre  :cite:p:`webMaxent`, y GARP Desktop  :cite:p:`webGARPDesktop` es una aplicación que permite aplicar el modelo GARP, desarrollada por los creadores mismos de este. Un SIG sencillo enfocado a este tipo de análisis, y que incorpora modelos como BIOCLIM o DOMAIN, es Diva--GIS :cite:p:`webDivaGIS`. Las referencias anteriores llevan a paginas Web de donde pueden descargarse los programas.

La figura :num:`#figcapturamodelospredictivos` muestra capturas de pantalla de dos de los programas anteriores.

.. _figcapturamodelospredictivos:

.. figure:: CapturaModelosPredictivos.*
	:width: 650px

	Ventanas de introducción de datos de dos *software* para aplicación de modelos predictivos: Maxent(derecha) y GARP Desktop (izquierda). Como puede verse, estos programas no incluyen capacidades de manejo de capas de la forma habitual en la que estas se presentan en un SIG de escritorio.






Otros usos de los modelos predictivos
--------------------------------------------------------------

Los modelos predictivos tienen uno de sus principales campo de aplicación dentro del campo de la ecología, donde, como acabamos de ver, ayudan a descubrir dónde podemos encontrar una especie determinada y lo adecuado que resulta un determinado emplazamiento para esa especie en función de las características que definen a este. Algunos modelos trabajan con capas de entrada fijas, de tal modo que los factores que se consideran relevantes para definir la idoneidad de un punto concreto ya están definidos. La aplicabilidad de estos modelos en otros ámbitos distintos es pequeña, ya que en un contexto diferente lo más probable es que las variables de influencia no sean las mismas. Los modelos que, sin embargo, pueden operar con cualquier capa de entrada y simplemente efectúan análisis estadísticos sobre ellas sin interpretar su significado, sí que pueden emplearse para tareas fuera del campo de la ecología.

Hay muchas otras situaciones en las que, conociendo dónde se da un determinado fenómeno, es interesante localizar otras zonas que resulten adecuadas para que ese mismo fenómeno también se produzca. A la hora de *buscar* esas zonas, disponer de cartografía de potencialidad como la que producen los modelos que hemos estudiado puede ahorrar tiempo y dinero, ya que puede concentrar esa búsqueda en las zonas de mayor probabilidad supone optimizar el esfuerzo. Por esta razón, el uso de modelos predictivos lo encontramos también en otros ámbitos y con unos planteamientos muy similares a lo expuesto para el caso de la ecología. Aunque esos ámbitos no están dentro de la temática de este capítulo, es de interés revisar algunos de ellos en lo que a la aplicación de modelos predictivos respecta, para tener una visión más amplia de la utilidad de estos.

Una de las disciplinas que se apoya en este tipo de modelos con más intensidad es la arqueología, dentro de la cual constituyen un campo de gran desarrollo recientemente, y en la que la principal labor del SIG en muchos casos es precisamente esta. La popularización de este tipo de modelos, unida a la facilidad con la que gracias a los SIG pueden aplicarse sobre juegos de datos antes difíciles de manejar por su volumen, ha supuesto un cambio en el campo de la arqueología, incorporando una herramienta ventajosa para el trabajo del arqueólogo, tanto el teórico como el desarrollado en campo.

Pueden distinguirse dos áreas distintas de aprovechamiento de los modelos predictivos dentro de la arqueología: la gestión del patrimonio arqueológico y la investigación  :cite:p:`Leusen2002`. En ambas, no obstante, la forma de operar es la misma, y aunque el objetivo perseguido sea distinto, tanto los modelos aplicados como la manera en que se aplican es la misma.

En lo que a la gestión del patrimonio respecta, una de las labores del arqueólogo es la búsqueda de nuevo patrimonio, desarrollada a través de yacimientos que han de localizarse en función de unos determinados factores. Conociendo variables del medio, así como la localización de otros yacimientos o de elementos que puedan relacionarse con la presencia o no de restos arqueológicos, un modelo predictivo ayudar a acotar las zonas candidatas donde cabe esperar nuevos hallazgos.

En el caso del arqueólogo que desarrolla un trabajo más científico, un modelo predictivo puede ayudarle a inferir nueva información a partir de la que ya tiene. Conociendo el emplazamiento de los yacimientos ya encontrados, puede establecer las zonas en las que es factible la presencia de nuevos restos, con lo que parcialmente obtiene la información que esos nuevos yacimientos aportarían, en particular la información de su localización. Esto puede utilizarse para conocer más acerca de la cultura a la que corresponden los yacimientos, analizando su distribución, que se conoce tanto en base a los yacimientos encontrados como a los lugares probables donde también existan.

Aunque común, este tipo de análisis no cuenta con el favor de todos los arqueólogos. Algunos argumentan que se trata de un análisis inductivo en lugar de uno deductivo, es decir, que el hallazgo de nuevos yacimientos no se fundamenta en la comprensión del hecho que los origina, sino simplemente como resultado de un análisis estadístico.

Puede encontrarse más acerca de modelos predictivos en arqueología en  :cite:p:`Leusen2002`.

Por último, otro uso de los modelos predictivos es en la planificación territorial, para la selección de emplazamientos óptimos. Ya vimos algo en este sentido en el capítulo :ref:`Estadistica_avanzada`, al presentar las formas de combinar capas en modelos multicriterio. El uso de modelos como los vistos en este apartado también es una opción para aplicar una serie de factores a la elección de una localización. La cartografía que se obtiene, del mismo modo que nos informa de la idoneidad de las distintas zonas para el crecimiento de una especie, también lo puede hacer para la idoneidad de estas a la hora de establecer algún tipo de infraestructura. Al igual que en el caso de la arqueología, los factores implicados van a ser distintos, pero la metodología en la que se sustenta el análisis es la misma.

En el capítulo :ref:`Gestion_ambiental` veremos más acerca de otro tipo de modelos de localización óptima, que pueden a su vez combinarse con estos.


Resumen
=====================================================

Dos son las tareas que hemos visto en este capítulo en las cuales el uso de SIG aporta interesantes elementos dentro del ámbito de la ecología: el análisis del paisaje y la modelización de hábitats mediante modelos predictivos.

En la primera de estas áreas, los SIG se emplean para el análisis espacial de las distintas unidades que componen el paisaje, ya sea individualmente, para el conjunto de las unidades de una misma clase o para la totalidad de dicho paisaje. Además de los parámetros (denominados *métricas*) que cuantifican la forma y otras características geométricas de cada unidad, existen otros que miden la conectividad, el aislamiento entre unidades de una misma clase o el contraste entre unidades contiguas. En conjunto, sirven para cuantificar la heterogeneidad del paisaje, y sus valores pueden emplearse para explicar el funcionamiento de este.

Por su parte, la modelización de hábitats se basa en la aplicación de modelos que, conociendo una serie de variables del medio y un conjunto de puntos en los que aparece (o no) una determinada especie, pueden calcular la idoneidad de las distintas zonas de un territorio para la presencia de dicha especie, prediciendo así la probabilidad de que tales zonas se encuentren, o hayan podido encontrarse, habitadas por la especie en cuestión. Este tipo de modelos tienen una base estadística y son empleados no solo en el terreno de la ecología, sino en otras áreas de conocimiento muy distintas, como sucede por ejemplo con la arqueología.
