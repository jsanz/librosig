.. _introduccion_factor_organizativo:

**********************************************************
Introducción. ¿Cómo se organiza un SIG?
**********************************************************



Trabajar con un SIG requiere una correcta organización a todos los niveles. Ahora que conocemos qué podemos hacer con un SIG, es el momento de ver cómo debemos plantearnos ese trabajo de forma óptima, dejando los aspectos técnicos y centrándonos en aspectos funcionales, organizativos y humanos, todos ellos igual de importantes que los anteriores ya vistos.

En este capítulo se presentan las ideas fundamentales relativas a la organización de un SIG, su implantación y uso. Estas ideas serán básicas para entender posteriormente los restantes capítulos de esta parte, en los que se desarrollan por separado algunos conceptos relacionados y de gran importancia en la escena actual de los SIG.


Introducción
=====================================================

Como sistema complejo, un SIG requiere una organización eficiente que permita la correcta interacción de todos sus elementos y a todos los niveles. Esta organización es tanto más necesaria cuanto más volumen adquiere el sistema SIG, pues la propia complejidad de este puede conllevar la perdida de eficiencia y un uso en el que no se aprovechan plenamente las capacidades que el SIG ofrece como herramienta para el trabajo con datos geográficos. Una organización ineficiente es con frecuencia el cuello de botella más importante con el que un sistema SIG se encuentra y, paradójicamente, un aspecto con frecuencia olvidado.

Los niveles de complejidad y volumen que encontramos actualmente en el ámbito de los SIG son muy superiores a los que existían hace apenas unos años, y requieren un enfoque distinto para poder lograr que todas las piezas del SIG funcionen de forma armoniosa y sincronizada, sin problemas derivados de una mala sincronización o de un incorrecto dimensionamiento del sistema. De hecho, el cambio que veíamos en el capítulo :ref:`Introduccion_fundamentos` en la definición del propio SIG, en el que se pasaba de una combinación de *hardware* y *software* para manejo de datos localizados espacialmente a un sistema complejo con más componentes, viene en gran medida desencadenado por la creciente consideración de la organización como un factor vital para el buen funcionamiento del SIG. Esa organización a la que originalmente no se le concedía la relevancia actual debido a que las circunstancias eran distintas, se ha demostrado en el contexto presente como un elemento clave para la gestión del SIG, y sin duda alguna un elemento al que ha de prestarse atención en cualquier utilización de un SIG más allá del ámbito meramente personal.

Implantar un SIG (es decir, establecer un entorno SIG susceptible de ser empleado productivamente) es una labor compleja. No basta con conseguir un *software* SIG, instalarlo en un ordenador, conseguir un conjunto de datos y ponerse a trabajar para dar respuestas a un problema dado en el que se requiera algún tipo de análisis geográfico. Ni siquiera en el supuesto de un contexto individual de trabajo ---la expresión mínima que podemos encontrar, y por tanto la más sencilla de gestionar--- la implantación resulta tan sencilla, ya que deben considerarse algunos aspectos antes de llevar a cabo cualquier acción. En este capítulo, vamos a ver cuáles son los puntos más importantes en los que debemos recalar a la hora de implantar un SIG, de forma que garanticemos el buen funcionamiento de este y establezcamos las condiciones adecuadas para poder trabajar con dicho SIG de forma óptima.

Las ideas de este capítulo son de interés no solo para los encargados de implantar como tal el SIG y ponerlo en funcionamiento dentro de un determinado entorno, sino para todo aquel usuario o persona implicada de algún modo en ese entorno. De un modo u otro, resulta interesante conocer las reglas que regulan el funcionamiento del sistema si se es en cierta medida parte de él. Más aún, el trabajo con un SIG no solo incluye la utilización directa de este, sino también un cierto planeamiento de ese trabajo y una serie de tomas de decisiones previas. Estas consideraciones, que aparecen en la realización de cualquier proyecto con independencia de su índole, afectan también a los Sistemas de Información Geográfica, y será en este aspecto en el que profundizaremos a lo largo de este capítulo.

La importancia de la organización
=====================================================

Hemos citado ya la importancia de la organización dentro de un SIG, justificando así brevemente la conveniencia de estudiar la mejor forma posible de llevar esta a cabo. Veamos con más detalle el porqué de dicha importancia y las consecuencias directas que una adecuada implantación de un SIG tiene en el funcionamiento de este y, especialmente, en su eficacia, rendimiento y en la calidad del trabajo realizado con él. Las siguientes son las dos principales de ellas:


* Mejor relación entre elementos del sistema. El sistema no lo componen únicamente un conjunto de elementos, sino también una serie de relaciones dentro del sistema. Si estas relaciones son fluidas y existe una sinergia entre las funciones que cada parte cumple en el todo del sistema, el funcionamiento de este último sera mejor. 
 En el sistema representado por un SIG, algunos elementos como los datos son utilizados por todos los restantes. El diseño de este elemento debe tener en cuenta esa circunstancia para que no existan problemas al interactuar con otras partes del SIG, como pueden ser las personas o el *hardware* y *software* empleado. El *hardware* debe dimensionarse para tener capacidad suficiente a la hora de manejar los volúmenes de datos con los que se trabaja, y el *software* debe ser capaz de poder acceder a los datos en el formato en que estos se encuentren almacenados. Por su parte, los datos deben ser los adecuados para satisfacer las necesidades de los usuarios que forman parte del sistema, para que estos, a través de los procesos de análisis y otras operaciones disponibles, obtengan resultados de interés de una forma óptima. Consideraciones similares pueden realizarse si se consideran elementos distintos del sistema SIG y su interrelación particular.
* Mejor relación entre representantes de un mismo elemento del sistema. Los elementos del sistema son a su vez conjuntos de otros elementos. La parte humana de un SIG no es una única persona, del mismo modo que el *software* puede no ser una única aplicación, sino varias de ellas para realizar distintas tareas sobre la información geográfica. A medida que avanzamos en el desarrollo de los SIG, encontramos escenarios más complejos en los que se multiplica la magnitud de los distintos factores implicados (más gente, más datos, más potencia en el *hardware* empleado...), requiriéndose a su vez una organización interna de esos mismos factores.

A la hora de planificar la implantación de un SIG, debemos tratar de homogeneizar internamente cada uno de sus elementos, o al menos de incorporar mecanismos que garanticen una correcta comunicación y coordinación a todos los niveles. Esto puede implicar, por ejemplo, aplicar estrategias de trabajo coordinado para organizar el factor humano, o emplear esquemas comunes para el almacenamiento de datos. Si cada uno de los datos con que trabajamos presenta una estructura distinta, encontraremos el mismo problema que si las distintas personas que van a trabajar en nuestro entorno SIG hablan distintos idiomas y son incapaces de comunicarse. En esta situación, puede resultar complejo y poco eficiente (o incluso ser por completo imposible) emplear varios grupos de datos de forma conjunta, restando así capacidades y eficiencia al sistema. 


Logrando lo anterior, el sistema SIG ofrece mejor funcionamiento, justificando así plenamente el esfuerzo desarrollado para su correcta implementación y organización, esfuerzo que, por otra parte, en ocasiones es notable y no debe menospreciarse.

Organizando los distintos elementos de un SIG
=====================================================

Ahora que ya sabemos por qué es importante una adecuada organización de un SIG, veamos algunas ideas básicas sobre la forma de lograr esta. Para ello, y puesto que la organización es un concepto íntimamente ligado a la estructura del SIG como sistema, veremos por separado cómo plantear esa organización para los principales elementos de este, los cuales ya conocemos bien de capítulos anteriores. Descubriremos así que la implantación de un SIG es mucho más que simplemente elegir una aplicación y utilizarla, y que una implantación que no cubra todos los aspectos fundamentales que a continuación detallaremos es muy probable que presente problemas y falle a la hora de ofrecer respuestas a las necesidades a las que un SIG correctamente planificado puede responder.

Datos
--------------------------------------------------------------

Ya sabemos que sin datos no podemos trabajar en un SIG, por lo que la implantación de este implica necesariamente la implantación de un conjunto de datos a partir de los cuales poder efectuar las operaciones propias del SIG. Esto conlleva el diseño y creación de una base de datos contra la que posteriormente trabajarán las distintas aplicaciones, bien sea para leer esos datos, modificarlos, o añadir nuevos datos.

A la hora de planificar el diseño y creación de la base de datos, se deben considerar todas las actividades que a lo largo de su vida van a desarrollarse sobre ella. En función de esto, se establecen las distintas etapas a seguir, que en una primera aproximación pueden ser las siguientes:


* Recopilación de datos. Los datos a incluir en nuestro SIG pueden obtenerse de procedencias muy diversas, ya sea adquiriéndolos de proveedores privados, de organismos oficiales o de cualquier otra entidad que disponga de los datos que van a ser necesarios. La elaboración de una lista de datos necesarios ha de realizarse considerando los futuros análisis que tendrán lugar sobre ellos, con objeto de saber qué datos hemos de obtener (es decir, qué variables del medio van a ser necesarias), pero también algunas características más detalladas de esos datos. Por ejemplo, si los usuarios de nuestro SIG van a hacer estudios a distintas escalas, es de interés contar con un mismo dato en esas escalas de trabajo, para así facilitar el manejo de datos y optimizar las operaciones.

 Si los datos que pueden obtenerse por las vías habituales no son suficientes, será necesario, siempre que ello sea viable dentro del contexto de la implantación, elaborar aquellos que no hayan podido obtenerse. La creación de estos datos debe encaminarse a obtener un producto acorde con el resto de datos de que disponemos, para que puedan integrarse de la forma más sencilla posible y disminuyan el trabajo a realizar.

 En ocasiones, la creación de nuevos datos no implica obligatoriamente el desarrollo de trabajo de campo o la aplicación de técnicas como las que vimos en el capítulo :ref:`Fuentes_datos` (por ejemplo, la digitalización). Puede ser interesante elaborar nuevas capas de datos a partir de las ya disponibles, mediante procesos de análisis u operaciones como las que hemos visto en la parte :ref:`Procesos` de este libro. Aunque estos procesos pueden ser llevados a cabo por los usuarios en el momento de necesitar un determinado dato, crear previamente ese dato y ofrecerlo junto a los demás puede ser interesante por varias razones. 

 En primer lugar, si son varios los usuarios que en un momento concreto van a necesitar ese dato, evitaremos la repetición innecesaria del proceso, con la consiguiente ganancia de tiempo. En segundo lugar, un usuario puede no estar capacitado o no disponer de la experiencia necesaria para crear correctamente ese dato, especialmente si el proceso a seguir es complejo o proclive a la aparición de errores. El hecho de que un usuario necesite un dato no implica que conozca la forma de elaborarlo a partir de otros datos primarios.

* Preparación de los datos. Obtener los datos es solo la mitad del trabajo. Si creamos nuestra base de datos con los datos que hemos adquirido tal y como han sido suministrados, es probable que el trabajo posterior sea difícil y complejo. Salvo que todos los datos provengan de un único proveedor, vamos a tener datos con una gran heterogeneidad, la cual no favorece en absoluto el trabajo fluido con ellos. Incluso si todos los datos tienen un origen común, es necesario prepararlos para el uso particular que esperamos se realice en nuestro SIG, teniendo en cuenta aspectos que no han sido considerados por el proveedor. 
 Los siguientes son algunos de los apartados a los que debe prestarse atención para la preparación de datos:

	* Extensión geográfica. Algunos datos pueden cubrir una región mucho mayor que la que se espera vaya a ser necesaria en el desarrollo de proyectos dentro de nuestro SIG. En tal caso, *recortar* la extensión disminuye el volumen de datos y facilita su manejo.
	* Formato. El formato debe ser el adecuado para que las aplicaciones puedan leer los datos, lo cual no siempre sucede. Cada proveedor de datos suele tener unas pautas a la hora de distribuir sus datos, y esto puede no coincidir con las capacidades de lectura de datos del *software* que vamos a utilizar. En tal caso, es necesaria una conversión de formato para que los usuarios no encuentren dificultades en ese sentido.
	* Modelo de datos. La forma en que esta recogida la información geográfica define en gran medida lo que podemos hacer con ella una vez la incorporemos al SIG, como vimos en el capítulo :ref:`Tipos_datos`. Si, por ejemplo, sabemos que una gran parte del trabajo en nuestro SIG va a implicar el análisis de Modelos Digitales de Elevaciones, este se lleva a cabo mayoritariamente sobre capas ráster, tal y como explicamos en el capítulo :ref:`Geomorfometria`. Si disponemos de una capa de elevaciones recogida como un conjunto de curvas de nivel (es decir, una capa vectorial), resulta conveniente transformar esta y que exista en el conjunto de datos del SIG un MDE ráster, mucho más acorde con lo que los usuarios van a requerir.
	* Sistema de coordenadas. Si los datos tienen distintos sistemas de coordenadas, será necesario transformarlos a un sistema común, preferentemente a aquel que vaya a ser utilizado con más frecuencia para la generación de resultados.

En resumen, el objetivo principal que debemos perseguir al configurar el conjunto de datos que van a formar parte de un SIG es lograr que la utilización de estos sea lo más sencilla y fluida posible. Un conjunto de datos rico y variado, bien estructurado y cuyo empleo no dé lugar a problemas o haga aparecer necesidades adicionales, simplificará más tarde el trabajo con el SIG y será una garantía del éxito de su implementación.

Personas
--------------------------------------------------------------

Si a lo largo de este libro hemos mencionado en repetidas ocasiones que los datos son el elemento imprescindible del sistema SIG, a la hora de implementar y organizar este son las personas quienes juegan el papel principal. El desarrollo del sistema SIG debe realizarse a partir de los usuarios, ya que la influencia que tienen en los restantes elementos es muy superior a la de estos otros. Los usuarios son quienes operan directamente con las aplicaciones y quienes además han de tomar decisiones a lo largo de un proyecto SIG, por lo que es necesario escuchar sus necesidades y sus opiniones antes de implantar un SIG, con el fin de proporcionarles el mejor entorno posible.

Las consideraciones acerca de los restantes elementos, tales como datos o *software*, deben matizarse *escuchando* lo que los usuarios pueden decir al respecto. El éxito en la implantación de un SIG pasa por tener en cuenta de forma conjunta los requerimientos del mayor número de usuarios posible, considerando incluso el perfil de futuros usuarios que puedan incorporarse más adelante.

Resulta erróneo, por ejemplo, adquirir un determinado *software* basándose exclusivamente en las propias características de este, y sin consultar a los futuros usuarios si poseen alguna experiencia previa con él o con otro similar. No siempre la mejor herramienta desde el punto de vista técnico garantiza unos mejores resultados al usarla, ya que existen otros factores que afectan a la productividad y la calidad de los trabajos que se desarrollen posteriormente sobre esa herramienta. 

Una sencilla encuesta a los usuarios es una herramienta muy valiosa para aportar información en este sentido y decantar la elección de la herramienta en uno u otro sentido. Igualmente, nos permitirá saber algo más sobre el nivel medio de los usuarios, sus preferencias o el tipo de trabajo que desarrollan mayoritariamente.

Se admite generalmente que el éxito en la implantación de un SIG pasa por un modelo de implantación que dé preponderancia a los usuarios como factores a considerar. No obstante, este enfoque no es siempre sencillo y no siempre está exento de riesgos. Definir las necesidades de los usuarios es uno de los aspectos vitales para la implementación de un SIG, pero también uno de los más difíciles  :cite:p:`Campbell1992IJGIS`. En ocasiones, por ejemplo, el usuario no necesariamente sabe qué es lo que necesita o qué le conviene. Un problema muy habitual en el mundo del SIG es el desconocimiento por parte de los usuarios de las verdaderas capacidades que el SIG tiene y puede ofrecerles. Estos usuarios son capaces de utilizar un SIG, pero el aprovechamiento que hacen de este no es óptimo, ya que ignoran una gran parte de su potencia. El hecho de que las aplicaciones SIG sean complejas y dispongan de funcionalidades numerosas contribuye a este hecho.

En este sentido, es importante considerar el papel de los usuarios también con posterioridad a la implantación del SIG, es decir, una vez que se ha tomado una decisión acerca de otros elementos como *software* o datos, y estos ya se encuentran operativos. En lo que al *software* respecta, esto incluye el desarrollo de acciones tales como seminarios o presentaciones, que divulguen las capacidades del SIG entre los usuarios y les hagan conscientes de lo que pueden lograr con este.

Otro de los aspectos importantes en el elemento formado por los usuarios son las relaciones entre estos. Citábamos como una de las ventajas de una buena organización el hecho de que existe un mejor conexión no solo entre los distintos elementos del SIG, sino también en cada uno de dichos elementos, entre sus distintos representantes. Esto es especialmente relevante en el caso de los usuarios, ya que la comunicación fluida entre ellos puede evitar muchos problemas y aumentar sensiblemente la productividad y la calidad del trabajo. Los usuarios con mayor experiencia pueden solucionar problemas a usuarios menos experimentados, aconsejarles en el desarrollo de su trabajo o instruirles en las capacidades del *software*. La creación de comunidades de usuarios activas es una buena señal de una implantación exitosa de un SIG, y estas comunidades pueden incluso trascender el ámbito de una implantación particular de un SIG, extendiéndose hasta cubrir a todos los usuarios de una determinada aplicación, o a todos los involucrados en un área de conocimiento dada en la que se utilice un SIG.


Por último, es importante para definir las necesidades de los usuarios saber clasificar a estos y conocer su papel en el SIG. Un usuario puede tener funciones muy distintas, ya que consideramos como tal a toda persona involucrada en el sistema SIG, no exclusivamente a aquellas que directamente realizan el trabajo más típico tal como el análisis de datos y la obtención de cartografía a partir de ese análisis. Para ver esto, podemos acudir a un ejemplo sencillo.

Volvamos al caso presentado en el primer capítulo de este libro, relativo a la gestión de una masa forestal, y analicemos qué tipos de usuarios podemos encontrar y el papel que cada uno de ellos desarrolla en el SIG.

En un extremo encontramos a las personas encargadas de la toma de decisiones, tales como los gestores y miembros de la administración responsable de la masa forestal. Estas personas no han de tener necesariamente unos amplios conocimientos de SIG, sino tan solo ser capaces de entender los resultados que se generan con este. En función de ellos, tomarán decisiones aplicando su experiencia al respecto, que en este área sí que debe ser elevada. En una posición similar encontramos a los operarios encargados del trabajo de campo y agentes forestales que trabajan directamente sobre la masa, y que, en términos del SIG, realizan fundamentalmente una labor de recogida de datos. Deben conocer bien el entorno forestal y las técnicas de muestreo y toma de datos, pero no es un requisito imprescindible que cuenten con experiencia en SIG. Si la recogida se realiza empleando alguna tecnología a tal efecto, o incluso algún tipo de SIG sobre una plataforma móvil, deberán tener nociones básicas de manejo, pero eso no constituye un conocimiento amplio de los SIG y sus capacidades.

En el extremo contrario a los anteriores encontramos a aquellos usuarios que se encargan de las cuestiones más técnicas del SIG y de corte más informático. Entre ellos están los administradores de las bases de datos, los programadores o los técnicos encargados de la digitalización de cartografía. Estos deben tener un amplio conocimiento del *software* que usan, pero no es necesario que sean expertos en el ámbito de aplicación en el que se encuentran. Así, los técnicos que digitalicen cartografía deben tener suficientes conocimientos cartográficos y de manejo de la herramienta, pero pueden desarrollar su trabajo sin conocer en profundidad aquello que están digitalizando (por ejemplo, parcelas de inventario o unidades de gestión del monte).

Entre estos dos extremos encontramos un diverso abanico de usuarios que emplearán de un modo u otro el SIG, y que aplicarán en distinta medida sus pocos o muchos conocimientos del ámbito de la gestión forestal, estando especializados de forma distinta en ambos campos. Podemos ver cómo todos estos tipos de usuarios se caracterizan, pues, atendiendo principalmente a sus capacidades dentro de dos ámbitos distintos: el de los SIG y el ámbito propio de aplicación de este (en este caso, el de la gestión forestal). En función de esto,  :cite:p:`Eason1994Belhaven` define cuatro bloques principales de usuarios:


* Técnicos informáticos. Con alta especialización en SIG pero escasa en el ámbito de aplicación.
* Profesionales ocasionales. Gestores y usuarios finales, con conocimientos limitados de SIG y alta especialización en el ámbito concreto de aplicación.
* Público. Los clientes del servicio que ofrece la organización en que se implanta un SIG, los cuales normalmente no presentan una gran especialización en ninguno de los dos bloques mencionados.
* Especialistas en la aplicación. Expertos que conocen con detalle el SIG y también el campo de aplicación de este. Se incluyen aquí los analistas SIG y los cartógrafos, para cuyo trabajo se requiere un alto conocimiento de todos los elementos implicados.


Un resumen distinto de estas ideas acerca de los usuarios de un SIG lo encontrarás en la tabla siguiente, donde puedes ver una definición de las principales labores que estos desempeñan y los perfiles correspondientes a estas.

==================================  ======================================================  =======================================================
Actor                                Tareas                                                 Actores específicos
==================================  ======================================================  =======================================================
Proveedores de datos                Generan nuevos datos espaciales.                        Grupos de investigación dentro de la institución.  
                                    Son los dueños de los datos del sistema.                Otras entidades interesadas en el mismo espacio.
                                    Proveen información espacial. 
Administradores de datos            Mantenimiento y estandarización de datos espaciales.    Especialistas en SIG y programación.
                                    Mantenimiento de los procesos que aseguran eficiencia 
                                    y estandarización para manejar y entregar datos.
Usuarios de datos                   Acceso y recombinación de datos espaciales.             Profesionales en GIS y geografía. 
                                    Generación de nueva información geográfica.             Analistas de información espacial. 
                                    y de bases de datos.                                    Planificadores
                                    Adición de conocimientos, hechos, interpretaciones 
                                    y análisis al sistema.
Clientes y usuarios de datos        Uso de la información y de los datos geográficos        De diversa naturaleza, interesados en los fenómenos 
fuera de la institución.            generados a partir del SIG institucional.               espaciales.
==================================  ======================================================  =======================================================

Con todo lo anterior, tenemos ya un marco en el que trabajar a la hora de implantar un SIG, tratando de no dejar fuera de este a ningún grupo de usuarios y adaptándolo a las distintas formas de utilizarlo que estos presentan.

Software
--------------------------------------------------------------

Puede pensarse en un principio que el software es el único factor a tener en cuenta al realizar la implantación de un SIG, pues es la cara visible de ese GIS de cara al usuario y al trabajo que este realiza. Sabemos ya, sin embargo, que esa visión simplificada en la que la elección de un *software* es la única decisión relevante a tomar es errónea, pero incluso en ese caso, el problema al que nos enfrentaríamos no sería sencillo. El mercado está lleno de aplicaciones SIG de muy diversas características que no hacen precisamente fácil elegir la más adecuada a nuestras necesidades concretas. Más aún, lo más probable es que ninguna de esas aplicaciones, pese a la amplia variedad existente, pueda cubrir dichas necesidades, y nos veamos obligados a combinar varias de ellas. Si el entorno de trabajo hacia el que enfocamos la implantación de nuestro SIG es amplio, la gama de necesidades que vamos a encontrar resultará más extensa, siendo todavía más complejo elegir el *software* que necesitamos.

Conocer con detalle el panorama actual del mercado de aplicaciones SIG es complejo, pero tener una visión global de sus principales representantes puede ser sencillo y muy útil no solo para elegir una aplicación concreta, sino también para saber qué podemos esperar al tratar de escoger una herramienta. El del SIG es un escenario cambiante donde aparecen muchas novedades continuamente, y donde los enfoques cambian a veces de forma notable. 

Aun conociendo qué aplicaciones SIG existen en el mercado y sus características, la elección de una que responda a nuestras exigencias puede no ser posible. En ocasiones, no existiendo una alternativa satisfactoria, puede ser necesario desarrollar elementos adicionales a medida de las necesidades existentes, e incluso, en un caso más extremo, el desarrollo completo de una aplicación SIG. Como vimos en el capítulo :ref:`Introduccion_tecnologia`, los SIG en la actualidad se conciben como elementos base muy extensibles, siendo sencillo extenderlos desarrollando únicamente las capacidades que necesitamos, y haciendo uso de forma transparente de todas las funcionalidades que ya contienen. 

En lo que respecta a la procedencia del software, encontramos una situación parecida a la existente con los datos. Adquirir software es la solución más inmediata y generalmente asequible, aunque en circunstancias particulares es necesario producir el software necesario que responda a unos requisitos más específicos. El desarrollo de este *software* puede contratarse como un servicio externo, o bien dentro del organismo de trabajo en el que nos encontremos :cite:p:`Grinshaw1994Longman`.

En caso de optar por simplemente utilizar un producto existente en el mercado,  :cite:p:`Heywood1998Longman` cita algunas cuestiones que deben plantearse antes de elegir un software SIG, entre las que figuran las siguientes:


* ¿Qué funcionalidades tiene?
* ¿Cumplen esas funcionalidades los requerimientos de mi organismo/equipo de trabajo?
* ¿Necesito realmente todas esas funciones?
* ¿Dispone de un entorno amigable?
* ¿Dispone de funcionalidades adicionales para usuarios avanzados?
* ¿Puede intercambiar datos con otras aplicaciones usadas en mi organismo/equipo de trabajo?
* ¿Qué documentación existe?
* ¿Es posible obtener formación?
* ¿Cuánto cuesta?
* ¿Puede esperarse que el fabricante siga desarrollando y apoyando este *software*?
* ¿Qué sistema operativo necesita para ejecutarse?


Como ya se ha mencionado, estas cuestiones deben relativizarse en función de otros criterios tratados en este mismo apartado. Los usuarios del *software* condicionan, por ejemplo, lo que entendemos por *entorno amigable*, ya que usuarios expertos pueden encontrar muy amigable una linea de comandos, mientras que otros menos familiarizados con este tipo de interfaces pueden ser incapaces de trabajar con ella. En este caso, es incluso probable que el usuario experto sea mucho más productivo en esa interfaz de linea de comandos que en otra distinta, con lo cual cabe reflexionar acerca de este apartado y tener claro que un mismo *software* puede ser interpretado de formas distintas según las circunstancias.

Asimismo, si consideramos la posibilidad de desarrollo de elementos adicionales mencionada anteriormente, es importante tener en cuenta un aspecto que analizaremos igualmente en el citado apéndice :ref:`Panorama_actual`, y que es el relativo a la forma de licenciamiento del *software*, bien sea como *software* libre o bien como *software* privativo. Esto condicionará en gran medida las posibilidades de modificación y extensión que la aplicación base escogida nos ofrezca, y por tanto también la idoneidad de una u otra decisión al respecto.

Hardware
--------------------------------------------------------------

Sin dejar de ser relevante, el *hardware* plantea menos problemas que otros elementos a la hora de implementar un SIG. Pese a ser un elemento fundamental, las actuales capacidades de los ordenadores y el cada vez menor coste de la tecnología han hecho más sencilla la elección de equipos adecuados dentro de un presupuesto dado. 

El *hardware* es, además, el elemento en el que las particularidades del SIG tienen menos influencia, al menos en lo que a los ordenadores como tales respecta. Los requisitos de un SIG en este aspecto no son muy distintos de lo que cabe esperar en muchas otras aplicaciones de distinta índole hoy en día. 

Estudios como  :cite:p:`Anon1996GISWORLD` muestran que las características de los equipos empleados para el trabajo con SIG dentro de un organismo o grupo de trabajo dependen principalmente del tamaño de la comunidad de usuarios. Es decir, que por encima de otras consideraciones tales como qué hacen esos usuarios o cómo lo hacen, el factor más relevante es *cuántos* usuarios existen. Esto parece lógico si se piensa que un mayor número de usuarios va a implicar una mayor cantidad de datos y muy posiblemente unas mayores necesidades de proceso, circunstancias que favorecen el empleo de estaciones de trabajo de mayor potencia, en lugar	de o junto a los habituales ordenadores personales.

La parte más específica dentro de un SIG en lo referente a *hardware* la encontramos en los periféricos. Como ya vimos en el capítulo :ref:`Fuentes_datos`, algunas tareas tales como la creación de datos requieren equipos especiales como por ejemplo tabletas digitalizadoras. Mientras que un puesto de trabajo para un usuario que realice un trabajo de análisis de datos es sencillo de instalar y requiere, en términos de *hardware*, poco más que un equipo estándar, una estación fotogramétrica digital tienen unos requisitos más específicos. En casos particulares como este, la oferta suele ser mucho más reducida y, con frecuencia, los proveedores de *software* y *hardware* son el mismo y no ofrecen ambos productos por separado, sino formando parte de paquetes ya definidos.

Otro aspecto particular del hardware SIG aparece en la generación de salidas. La creación de mapas impresos, generalmente de gran tamaño, exige el empleo de medios de impresión de gran formato, menos comunes y con un coste mayor que el de impresoras y *plotters* comunes.

Distintos niveles de organización. Organización de un proyecto SIG
=============================================================================

Cuando hablamos de organización de un SIG, entendemos que este concepto se aplica, como venimos viendo, a los elementos que componen el sistema, tratando de mejorar la labor de cada uno de ellos y las relaciones con los restantes. Esto afecta al SIG como sistema complejo, desde el momento de su implantación (es decir, desde que se crea y se pone en uso dentro de un contexto dado), y durante una serie de trabajos o acciones desarrolladas a lo largo de su vida. Esta organización se desarrolla sobre el total de lo que vamos a encontrar en el SIG durante esa vida, es decir, teniendo en cuenta toda la gente que va a operar con el SIG o todos los datos que es posible que se almacenen, entre otras consideraciones. Se debe pensar, igualmente, en todos los distintos proyectos que van a llevarse a cabo, cada uno de los cuales planteará unas necesidades específicas y condicionará así el diseño global del SIG.

No obstante, existe también una necesidad organizativa que afecta a cada uno de esos proyectos, y que guarda gran importancia si deseamos concluir estos de forma exitosa. Los proyectos SIG no son distintos de otro tipo de proyectos tales como el desarrollo de un *software*, la construcción de un edificio o la creación de una empresa, y necesitan un análisis previo, unos planteamientos de partida y una serie de procedimientos estructurados para ir completando con garantías las distintas etapas del proyecto. En el caso de un proyecto SIG, estas etapas vienen caracterizadas por el empleo de información geográfica y el planteamiento de un problema también con una componente geográfica, a resolver mediante una serie de procesos de análisis y operaciones tales como las que hemos ido viendo en capítulos anteriores.

La ingeniería de proyectos provee un nutrido conjunto de técnicas para la elaboración de estos, las cuales son de aplicación en los más diversos contextos, incluido el de los SIG. Herramientas como el análisis DAFO para la realización de estudios de idoneidad, o los diagramas de Gantt para controlar el desarrollo del proyecto a lo largo del tiempo, son solo algunas de las más populares para cubrir las necesidades de planificación de un proyecto de características cualesquiera. No es el objetivo de este texto el detallar estas metodologías, que quedan todas ellas fuera de su alcance temático. El lector interesado puede encontrar una interesante introducción a la gestión de proyectos en  :cite:p:`Jaque2007Proyectos`.

Es de interés, no obstante, mencionar la multidisciplinaridad  de los proyectos SIG como una característica básica a la que debe prestarse atención. Los distintos tipos de usuarios que vamos a encontrar dentro de un proyecto SIG conforman un panorama muy variado, con unas funciones que, en ocasiones, y especialmente en proyectos de menores dimensiones, no se reparten adecuadamente, recayendo algunas de ellas en usuarios no especializados. Aislar adecuadamente las responsabilidades y conocimientos necesarios para jugar cada papel dentro de un proyecto SIG es importante de cara a lograr que todas las partes de ese proyecto se completan de manera óptima. 

Resumen
=====================================================

Implantar un SIG es una tarea compleja de la que depende posteriormente el éxito de dicho SIG. Organizar y coordinar adecuadamente todos los elementos de un SIG es una labor básica para llevar a cabo una correcta implantación. Hemos visto en este capítulo cómo considerar cada uno de esos elementos tanto por sí mismos como en relación con los restantes, y de qué forma plantearse lo que cada uno de ellos representa antes de tomar decisiones de cara a la implantación de SIG. Entre ellos, los usuarios suponen el elemento de mayor importancia, alrededor del cual debe centrarse el proceso de implantación.

Es necesario igualmente organizar los proyectos SIG y tener en cuenta las particularidades de estos como proyectos, para así poder aplicar las técnicas habituales de gestión de proyectos de forma más específica. La característica particulares que define a un proyecto SIG en comparación con otro tipo de proyectos es su alta multidisciplinaridad.

