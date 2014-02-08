.. _metadatos:

**********************************************************
Metadatos
**********************************************************

Blake, Landon; Olaya, Víctor


Los metadatos son aquellos datos que describen los datos espaciales y los servicios disponibles en una IDE. Los metadatos son uno de los puntos de entrada a la información geográfica contenida en una IDE ya que permiten a un actor sin ningún conocimiento de esta consultar qué puede ofrecer. En este capítulo describiremos en detalle qué son los metadatos, su utilidad, y cómo crearlos y emplearlos.


Introducción
=====================================================

Los datos contienen la información geográfica, y es esta la que empleamos en un SIG para realizar las distintas operaciones que ya hemos visto en anteriores capítulos de este libro. No obstante, esos datos pueden resultar insuficientes, ya que el proceso de interpretación mediante el que extraemos la información a partir de estos puede requerir conocer alguna otra serie de elementos.

Por ejemplo, si tenemos las coordenadas de un punto disponemos de un dato, pero para interpretarlo correctamente necesitamos conocer, entre otras cosas, el sistema de coordenadas en que vienen expresadas esas coordenadas. El dato con el que trabajamos (las coordenadas), requiere unos datos adicionales (por ejemplo, el código EPSG del sistema de referencia empleado) para cobrar verdadero sentido.

Surge así el concepto de *metadatos*. Literalmente, los metadatos son *datos acerca de los datos* y su misión es *explicar* el significado de los datos. Es decir, ayudan a los usuarios de los datos a entender mejor el significado que estos tienen y la información que guardan. Los metadatos son un documento adicional que acompaña a los datos, y que permite una mejor gestión y una utilización más precisa de ellos.

Trabajando en el entorno de un SIG, los datos con los que trabajamos son de tipo espacial, y como ya estudiamos en su momento (véase el apartado :ref:`ComponenteInformacionGeografica`), existe una componente espacial y una temática. Los metadatos pueden referirse a ambas componentes, ya que es necesario documentar todas ellas, y podemos encontrar metadatos referidos a una capa de forma global, a su componente espacial o a su componente temática.

Un ejemplo de metadato global de una capa puede ser el nombre de su autor o la fecha en la que ese dato ha sido creado. El sistema de referencia en el que se expresan las coordenadas de cada entidad recogida es un tipo de metadato relativo a la componente espacial. Y en lo referente a la componente temática, los metadatos pueden recoger las unidades en las que se recoge una variable asociada a cada entidad, o bien almacenar cualquier otro valor que permita una mejor interpretación de esa variable.

En una definición más formal, los metadatos son archivos de información que recogen las características básicas de algún dato o recurso. Representan el quién, qué, cuándo, dónde, cómo y por qué de ese recurso. Los metadatos geoespaciales se emplean para documentar recursos geográficos digitales tales como una base de datos espacial, un SIG o una imagen de satélite. Un registro de metadatos incluye elementos básicos tales como el título o nombre del recurso, elementos geográficos como la extensión que cubre el dato o el sistema de coordenadas empleado, así como elementos relativos a la base de datos asociada tales como la definición de cada uno de sus campos o el dominio en que se encuentran los valores de estos  :cite:p:`webFGDC`.

El concepto de metadato no es algo nuevo y exclusivo de los datos digitales, ya que un mapa impreso también contiene metadatos en cierta forma. Una leyenda o un texto en un margen del mapa con información sobre la fecha en que se ha creado son también metadatos. En el caso de los datos geográficos digitales, los metadatos no forman parte del dato directamente sino que son independientes de este. Ello permitirá realizar operaciones separadamente con los metadatos, tales como búsquedas, que abren nuevas posibilidades y dan un gran valor a estos.

La utilidad de los metadatos
=====================================================

Dependiendo del tipo de dato con el que trabajemos y las operaciones que deseemos realizar con ellos, los metadatos correspondientes serán más o menos necesarios, pudiendo ser prácticamente irrelevantes o bien completamente imprescindibles. Por ejemplo, si se trabaja con una única capa y gran parte de la información que esta contiene no va a emplearse para la realización de operaciones, los metadatos son menos necesarios que si se da un uso más intenso a los datos. 

En algunos casos, incluso si carecemos de metadatos, resulta posible interpretar correctamente los datos, como sucede si trabajamos con un MDE y valores de elevación en metros. Es fácil saber que los valores de elevación se encuentran en esas unidades aplicando cierta lógica, y procesarlos correspondientemente aunque no exista un dato explicito que así nos los indique. 

En otras circunstancias, los metadatos son necesarios, pues contienen información que no puede inferirse directamente desde los propios datos. Si varias capas están en sistemas de coordenadas distintos y deseamos aplicar las transformaciones correspondientes para unificarlos en uno único y procesarlas de manera conjunta, estas transformaciones no se pueden llevar a cabo si no conocemos el sistema de origen del que partimos en cada capa. En este supuesto, el trabajo con los datos viene condicionado a que existan los metadatos correspondientes.

Los metadatos son, por tanto, sumamente importantes en el trabajo con SIG y, como veremos en breve, cobran una importancia mayor todavía cuando no nos encontramos en el contexto de un uso aislado de los datos, sino cuando nos situamos en un entorno de un gran volumen de datos y numerosos usuarios. 

Dos de las funciones principales de los metadatos son garantizar el uso correcto y adecuado de los datos y facilitar su gestión, localización y consulta.

Garantizar el uso correcto de los datos
--------------------------------------------------------------

Uno de los beneficios más importantes que proporcionan los metadatos es asegurar que los datos espaciales son empleados de forma adecuada. Los datos espaciales, como muchos otros datos, son creados habitualmente para un determinado objetivo, y este objetivo no ha de ser necesariamente evidente o contenerse como tal en los datos mismos. Cuando se emplean esos datos para un objetivo distinto a aquel para el que fueron diseñados, pueden surgir problemas debido a que se está realizando un proceso para el que los datos con los que se trabaja presentan carencias. A continuación veremos algunos ejemplos para ilustrar algunas situaciones en las que puede producirse un uso indebido de los datos, las cuales podrían corregirse o evitarse mediante el empleo de los correspondientes metadatos.


* Ejemplo 1: Un organismo crea un juego de datos con los ejes de las principales vías de una ciudad. Estos datos se emplean para labores de mantenimiento, de tal modo que faciliten la localización de las señales viales en la realización de inventarios. El juego de datos no contiene informacion sobre direcciones ni tampoco almacena la topología de la red. Posteriormente, una compañía especializada en reparto adquiere estos datos para el cálculo de rutas óptimas desde sus almacenes hasta las direcciones de destino de sus clientes.

* Ejemplo 2: Un organismo crea un juego de datos con los elementos de la red de alcantarillado tales como alcantarillas, tuberías, bombas, etc. Durante años, esta capa no se actualiza. Años después de la creación de esos datos, ese mismo organismo desarrolla un proyecto relativo a la calidad de las aguas y el control de la contaminación y utiliza ese juego de datos.

* Ejemplo 3: Una compañía mantiene un registro de los limites aproximados de las parcelas catastrales de una zona. El juego de datos, no obstante, no muestra las posibles discrepancias que pueden existir en esos límites, tales como solapes o huecos. Una inmobiliaria emplea ese juego de datos para asesorar a sus clientes y mostrarles la localización y límites de las parcelas a los compradores potenciales.


En los tres casos, nos encontramos con un usuario de un juego de datos que, por desconocer las características de este, realiza un uso indebido. 

En el primer caso, la compañía de reparto no podrá operar con esos datos, ya que no contienen la información que necesitan. Conocer de antemano las limitaciones de los datos antes de adquirirlos o plantear cualquier operación con ellos ahorra tiempo y dinero.

En el segundo caso, la información contenida en el juego de datos está desfasada. Si los metadatos contienen la fecha en la que los datos fueron creados, esta puede emplearse para juzgar la validez de estos últimos en función de su antigüedad.

Por último, en el tercer caso la compañía inmobiliaria trabaja con unos datos que no tienen la precisión requerida. Si existieran metadatos y estos dejaran claro que los límites de parcelas son aproximados, se conocería con exactitud las limitaciones de los datos y no se les daría un uso indebido.

Estos tres ejemplos ponen de manifiesto la necesidad que existe de conocer acerca de los datos más que lo que ellos mismos contienen, en particular todo lo relativo a los fines para los que estos se han creado. Esto permite conocer lo que se puede esperar de los datos y no emplearlos en situaciones indebidas.

Los creadores de datos deben procurar acompañar estos de metadatos precisos y suficientes, y los usuarios deben consultar estos antes de utilizar dichos datos. De este modo, se puede garantizar que un dato no es empleado de forma errónea y que los resultados que se obtendrán tendrán validez.

Vimos en el capítulo :ref:`Calidad_datos` cómo la calidad se define como el conjunto de propiedades y de características de un producto o servicio que le confieren su aptitud para satisfacer unas necesidades explícitas e implícitas. Los metadatos documentan esas características y las de todas aquellas necesidades a las que pueden responder los datos, y de este modo documentan la propia calidad del dato. Como ya se dijo entonces, los metadatos son un elemento muy importante en relación con la calidad de los datos espaciales

Facilitar la gestión los datos
--------------------------------------------------------------

Las funciones anteriores ponen de manifiesto la utilidad e importancia de los metadatos en un contexto reducido en el que un individuo o un pequeño grupo trabaja con ciertos datos. La importancia de los metadatos se hace patente incluso cuando se dispone de un único dato (una sola capa), pues es en el momento de utilizar este cuando se consultan los metadatos y se emplea la información que contienen para poder conocer la precisión de los datos, su referencia espacial, u otros elementos que permitan que ese uso sea más correcto.

En esta situación, se dispone ya de los datos y de los metadatos, y estos últimos nos permiten conocer más acerca de los primeros. No obstante, en el panorama tecnológico actual un usuario no dispone de todos los datos que necesita, sino que puede acceder a ellos en la medida en que le sea necesario, del mismo modo que no guardamos en nuestro ordenador enciclopedias y libros, pero podemos acceder a ellos a través de Internet. Las tecnologías que vimos en el capítulo :ref:`Servidores_y_clientes_remotos` dedicado a servidores y clientes nos permiten acceder a una enorme cantidad de datos espaciales, y los metadatos juegan un papel clave en la gestión de estos.

En el contexto de las Infraestructuras de Datos Espaciales es donde los metadatos cobran una importancia mayor si cabe, ya que informan de las características de los datos a los restantes actores de la IDE. Los metadatos constituyen un *resumen* de las características principales de los datos, y pueden ser empleados para labores de búsqueda y localización de datos de un tipo dado. De este modo, compartir los datos es más sencillo, y la difusión de estos se realiza de una forma más fluida. Es decir, la IDE alcanza mejor sus objetivos cuando los datos que contiene se encuentran correctamente documentados mediante buenos metadatos. Los catálogos que veíamos como parte integrante de la IDE necesitan los metadatos para funcionar, ya que responden a las peticiones del usuario del catálogo en función de la información que los metadatos contienen.

En el escenario actual, esta funcionalidad de los datos es preponderante sobre las restantes, y es por ello que tratamos los metadatos dentro de este libro en esta parte dedicada al factor organizativo, ya que son ante todo un elemento básico para la organización de los datos dentro del sistema SIG.

Algunas características de los datos solo se contienen en los metadatos, como por ejemplo el sistema de coordenadas empleado o la descripción detallada de los distintos campos de la componente temática. Otros, por el contrario, pueden obtenerse a partir de los propios datos, como por ejemplo el área que cubre una capa. Aunque este tipo de valores sea posible obtenerlos procesando los datos en sí, añadirlos a los metadatos abre nuevas posibilidades en el marco de la gestión, permitiendo un manejo más dinámico.

En general, los metadatos son mucho menos voluminosos que los datos a los que acompañan. Si en una IDE buscamos datos para una zona dada, es mucho más sencillo consultar los metadatos que consultar los datos como tales. Mientras que la primera operación puede realizarse de forma rápida, la segunda demanda unos cálculos mucho mayores, que con los grandes volúmenes que son habituales en una IDE puede hacer esa búsqueda virtualmente irrealizable. Es decir, que los metadatos facilitan y agilizan la localización de los datos cuando estos se buscan por criterios geográficos. Añadiendo a los metadatos elementos como la extensión del área cubierta por los datos, este tipo de búsquedas se efectúan de forma más ágil y efectiva.

Cuando la búsqueda se realiza por otros criterios distintos, los metadatos son el elemento clave para poder realizar esta búsqueda. Si queremos localizar la capa más actual con un tipo de información dada, necesitamos conocer *qué* información contiene cada capa y *cuándo* se ha creado, para aplicar sobre esos datos los criterios de búsqueda correspondientes. Sin los metadatos, estas operaciones no son posibles.

En su conjunto, los metadatos sirven para catalogar los datos y por tanto son básicos dentro de las IDE para hacer más fluida la transferencia de datos en ella.

Facilitando la localización de datos adecuados para una determinada tarea se obtienen además beneficios colaterales. Haciendo más sencillo el acceso a los datos se pueden evitar esfuerzos redundantes tales como la creación o modificación de datos cuando existen dentro de la IDE otros que pueden servir para responder a una necesidad concreta. El uso de metadatos permite así ahorro de tiempo y dinero y un mejor aprovechamiento de los datos.

Características de los metadatos
=====================================================

Los metadatos pueden ser tan variados en sus características como los propios datos a los que acompañan. Los enfoques para la creación de metadatos son muy diversos y ello da lugar a metadatos muy diferentes.

Algunas de las características que resulta de interés tratar son las siguientes:


* Contenido de los metadatos. ¿Qué información contienen?
* Granularidad de los metadatos. ¿A qué elementos particulares hace referencia esa información?
* Forma de almacenamiento de los metadatos. ¿Cómo se guardan?


Contenido de los metadatos
--------------------------------------------------------------

Los valores que pueden incorporarse a los metadatos son muy abundantes, tantos como tipos distintos de información se considere necesario registrar respecto a un dato geográfico particular.

Las características de los metadatos asociados a los datos dependerán directamente de estos y de algunos factores como los siguientes:


* El tipo de dato y en particular, el modelo de representación empleado. Los datos vectoriales tendrán asociados unos metadatos distintos que los correspondientes a datos ráster.

* El formato en que se almacenan los datos. El tipo de fichero o base de datos condiciona la información que puede almacenarse (vimos esto en detalle en la sección :ref:`Formatos_archivo`), y por tanto condiciona los metadatos. 

* La organización, entidad o individuo responsable de la creación de los datos y el uso que se pretende dar a estos. Puesto que, como hemos dicho, los datos se crean para un objetivo definido, este objetivo y los intereses de quien ha creado los datos definirán el tipo y cantidad de información que se recoja en los metadatos. Datos pensados para un catálogo público tendrán asociados metadatos distintos que datos privados con acceso restringido, del mismo modo que datos pensados para un uso muy concreto presentarán unos metadatos diferentes a los que acompañarán a unos datos de uso más genérico.

* Elemento al que se asocian los metadatos. Como veremos en el siguiente apartado, podemos asociar metadatos a un juego de capas, una capa o una entidad aislada dentro de una capa. Esto implica diferencias en el contenido de los metadatos, pues esos elementos tienen características de distinta naturaleza.

* El estándar empleado para crear los metadatos. En el capítulo :ref:`Estandares` veremos los estándares que existen para los metadatos geográficos y la forma que estos tienen, la cual define directamente su contenido.     


 
Algunos de los elementos comunes que se incorporan a los metadatos geográficos son los siguientes:


* Información de identificación. Este tipo de información permite identificar de forma única un dato geográfico y distinguirlo de otros. Esta información ayuda a catalogar los datos, e incluye el nombre, palabras claves, una descripción básica o la ya mencionada extensión geográfica de los datos.

* Información sobre la calidad de los datos. La información sobre la calidad de los datos puede incluir, entre otros elementos, aquellos relativos a la completitud de estos, los procesos que se han empleado en su creación y mantenimiento, o las operaciones de validación y verificación a las que se han sometido.

 En relación con los procesos empleados, es importante reseñar que muchos de los algoritmos que vimos en la parte :ref:`Procesos` toman algún tipo de dato geográfico como entrada y generan algún otro nuevo. Es decir, toman una o varias capas y generan nuevas capas como resultado. Para documentar la calidad de los datos resultantes se debe documentar en los metadatos la procedencia completa de estos, indicando las metodologías empleadas para su creación y todos los metadatos propios de las capas de entrada.

 Un ejemplo de esto puede ser el proceso de cálculo de una capa de pendientes a partir de un MDE. Este MDE tendrá a su vez unos metadatos asociados (entre ellos algunos relativos a su calidad), y la bondad y calidad de la capa de pendientes está ligada directamente a la del MDE. Por tanto, en los metadatos debe hacerse referencia a ese MDE o bien a las características de este.

 Si el MDE no se ha adquirido directamente, sino que se ha elaborado haciendo uso de otros procesos tales como interpolación a partir de curvas de nivel, se ha de añadir también a los metadatos la información correspondiente a esos procesos, especificando por ejemplo el método de interpolación usado, los parámetros de ajuste de este o incluso el software mediante el que se ha aplicado.

 Con esto, puede *rastrearse* el origen de los datos y se dispone de una base sobre la que evaluar la calidad de estos en función de dicho origen. Tenemos así el concepto de *linaje* de los datos. Esta idea es similar a la de *trazabilidad* empleada en otros sectores como, por ejemplo, el alimentario.

* Información sobre la representación del dato espacial. Se incluyen en este grupo la precisión y exactitud de los datos, la escala de trabajo o la resolución en el caso de capas ráster. Este tipo de metadatos están también íntimamente ligados con la calidad de los datos.

* Información sobre la componente no espacial. Información relacionada con los atributos que acompañan a las capas vectoriales, o bien relativas a las variables que se recogen en capas ráster. Esto incluye explicaciones sobre el significado de los nombres de cada uno de los atributos, el rango de valores válidos para cada uno de ellos o los métodos empleados para recoger estos datos.

* Información sobre la distribución. Esta información sirve para definir el acceso a los datos y las posibilidades de distribución de estos, especificando quiénes pueden acceder a ellos y quiénes no, o en qué condiciones pueden hacerlo. También puede recoger elementos como la fecha en que fueron publicados los datos o bien cuándo fueron puestos a disposición del público, de tal forma que se disponga de toda la información referente a su presencia en el marco de una IDE o una red.

De entre estos, algunos son considerados como fundamentales y se incluyen de forma genérica, mientras que otros pueden o no incorporarse. Al definir una especificación de metadatos, se pueden establecer niveles de prioridad, estableciéndose un grupo de propiedades básicas que han de documentarse siempre y otro con propiedades de carácter opcional.


Granularidad de los metadatos
--------------------------------------------------------------

Habitualmente, los metadatos están asociados a un conjunto de datos al completo. Este conjunto de datos que sirve como unidad a la hora de crear metadatos coincide en general con la idea de capa en un SIG. Es decir, cada capa tiene asociado un bloque de metadatos.

Esto no quiere decir, no obstante, que no puedan registrarse metadatos a un nivel distinto. Dependiendo del tipo de datos con los que se trabaje, puede resultar de interés o incluso necesario asociar metadatos a unidades distintas.

Algunos metadatos como el sistema de coordenadas serán compartidos por todos los elementos de una capa, y por tanto es lógico en su caso emplear la capa como unidad básica en lo que a metadatos se refiere. Otro metadatos, sin embargo, hacen referencia a elementos particulares dentro de la capa.	

Este tipo de metadatos aparecen especialmente cuando a lo largo del ciclo de vida de los datos se introducen modificaciones en estos, editándolos o añadiendo nuevas entidades. Si bien en el origen el creador de los datos es una única entidad, otras entidades pueden alterar esos datos y deberán actualizar correspondientemente los metadatos. Registrando como autores de los datos a ambas entidades se recoge más información al respecto, pero esta puede no ser suficiente. Sabemos que los datos fueron creados por una entidad A y posteriormente modificados por una entidad B, pero si tomamos un elemento dado no podemos saber si esta corresponde al trabajo original de A o a la modificación realizada por B.

De modo similar, podemos incorporar a los metadatos las dos fechas de creación y edición de los datos, así como parámetros relativos a la calidad de los datos o las metodologías empleadas para recogerlos en ambos instantes. Sin embargo, no podemos saber en qué fecha fue incorporado un elemento concreto o la calidad de los datos que definen ese elemento en particular.

En estas circunstancias, resulta más conveniente optar por metadatos más granulares, de forma que puedan recogerse particularizados para las distintas entidades de la capa.

Por ejemplo, algunos de los datos que pueden resultar de interés a escala de elemento (en el caso de una capa vectorial, hablamos de una geometría y sus atributos asociados) son los siguientes:


* Quién ha creado ese elemento.
* Quién ha modificado ese elemento.
* Cuándo fue creado originalmente.
* Cuándo ha sido modificado por ultima vez.
* Cuántas veces ha sido modificado.
* Una descripción del objeto real que este elemento representa.


Podemos encontrar el caso opuesto, en el que varias capas comparten los mismos metadatos, y por tanto estos pueden asociarse a escala de toda una familia de datos. Ese es el caso cuando se tiene un conjunto de capas generadas por una misma entidad y para un mismo fin, las cuales cubren una amplia zona geográfica y debido a ello se encuentran divididas horizontalmente. Estas circunstancias se dan de forma habitual en series de datos de carácter nacional o autonómico, y conforman una de las situaciones en las que el registro de metadatos puede hacerse para toda la serie en su conjunto, al menos para algunos de esos metadatos.

.. _figgranularidadmetadatos:

.. figure:: Granularidad_metadatos.*
	:width: 650px
	:align: center

	Granularidad de los metadatos. Los metadatos pueden hacer referencia a elementos a distinta escala.

Los metadatos pueden así registrarse a una escala distinta a la de la capa como unidad de datos, aunque esta sigue siendo la referencia más habitual a la hora de crear metadatos (Figura :num:`#figgranularidadmetadatos`).

Forma de almacenamiento de los metadatos
--------------------------------------------------------------

Si para los propios datos geográficos encontramos muy diversas alternativas a la hora de almacenarlos, la situación no es distinta a la hora de almacenar los metadatos. Las dos alternativas principales son el uso de ficheros independientes o el almacenamiento en bases de datos  :cite:p:`metadataPrimer`.

Elegir entre uno u otro enfoque depende del conjunto de datos de trabajo, su volumen total, el uso principal que se le da o la granularidad de los datos según vimos en el apartado anterior.  :cite:p:`webFGDC` recomienda el uso de bases de datos cuando los datos estén sujetos a frecuentes modificaciones o si existe una parte de los metadatos que es común a varios grupos de datos. Este es el caso que vimos en el apartado anterior al mencionar los metadatos correspondiente a toda una serie de datos.

Utilizando una base de datos, resulta más sencillo actualizar los datos, especialmente si puede haber varios usuarios que realicen esas actualizaciones. Como veremos más adelante, existen servicios relacionados con la información geográfica que van a permitir a varios usuarios modificar un mismo juego de datos base. Las modificaciones que estos usuarios hagan han de reflejarse en los metadatos, y para ello es necesario contar con una tecnología que permita un acceso concurrente similar para los metadatos. Las bases de datos proveen esas capacidades, y son por tanto adecuadas para el almacenamiento de metadatos en ese contexto.

Si, por el contrario, los datos no van a ser usados de esa forma, no es probable que deban modificarse con frecuencia y apenas contienen elementos comunes, una forma más simple de almacenarlos es utilizando ficheros independientes, generalmente ficheros de texto plano que son más sencillos de producir y además pueden leerse con un simple editor de texto.

Creación de metadatos
=====================================================

La creación de los metadatos no es tarea de un único grupo de profesionales ni se lleva a cabo en un único momento dentro del ciclo de vida de los datos. Por el contrario, distintas entidades o grupos pueden crear o editar los metadatos, y pueden hacerlo a lo largo de todo el tiempo de existencia de dichos datos. 

Los metadatos puede crearse en el mismo origen de los datos, recogiendo la información al mismo tiempo que se producen los datos en sí. Esta creación puede derivar de la digitalización de mapas impresos o de la medición directa de valores, entre otros procesos. Las organizaciones que se encargan de crear datos son responsables en este caso de crear los metadatos que los acompañan.

Las entidades responsable de distribuir datos geográficos y ponerlos a disposición de los distintos usuarios pueden igualmente crear metadatos en caso de que estos no existan. Estas entidades no producen datos, pero recogen datos de sus creadores y han de prepararlos para ofrecer un mejor servicio. Los metadatos aportan un valor añadido a los datos y facilitan la gestión de datos que estas organizaciones han de realizar.

Por último, los mismos usuarios y beneficiarios de los datos pueden crear metadatos o ampliar los ya existentes. Si estos usuarios modifican los datos, esas modificaciones deben recogerse en los metadatos. Aún así, incluso si no se producen modificaciones, puede resultar de interés añadir nueva información en los metadatos, particularmente aquella que estos no contengan pero que pueda tener valor para los objetivos que se persiguen usando esos datos. Igualmente, dejar de usar los datos por alguna razón tal como el hecho de que se encuentren desactualizados es una información que los mismos usuarios pueden incorporar a los metadatos, informando así a futuros usuarios de la falta de validez de esos datos.


En resumen, los metadatos pueden ser creados o modificados en los siguientes puntos dentro de la vida de los datos:


* Cuando se crean los datos.
* Cuando se organizan o catalogan los datos.
* Cuando se modifican o editan los datos.
* Cuando se archivan o descatalogan los datos.


En circunstancias ideales, todo dato debería tener asociados unos metadatos, y estos últimos deberían crearse siempre que se creen dichos datos y actualizarse siempre que estos se modifiquen. La realidad, sin embargo, es que una gran parte de los datos geográficos que existen no tiene metadatos asociados, o bien estos no son lo suficientemente detallados.

Una razón importante para ello es la falta de concienciación que existen por parte tanto de creadores de datos como de usuarios respecto a la importancia de los metadatos. Mientras que para un usuario aislado o un pequeño grupo de técnicos SIG puede no resultar importante generar metadatos a la hora de crear algún dato geográfico, cuando nos encontramos con organizaciones más grandes e infraestructuras de datos mayores los metadatos se hacen imprescindibles. El usuario aislado prefiere generalmente no dedicar tiempo (la creación de metadatos no es en absoluto sencilla y es una tarea que consume tiempo) a crear unos metadatos que no percibe como importantes para su trabajo con los datos. 

Si en lugar de datos geográficos habláramos de libros, una persona normal no cataloga los libros que tiene en su casa y recopila información acerca de cada uno de ellos, almacenándola en una base de datos. En una gran biblioteca, sin embargo, esta labor es imprescindible, pues de otro modo resulta imposible gestionar tanto el gran fondo bibliográfico del que se dispone como el amplio número de lectores y usuarios.

En realidad, incluso en el nivel más local, las ventajas de la creación de metadatos son grandes, especialmente si consideramos que un dato creado y utilizado en un entorno local puede más adelante pasar a formar parte de una infraestructura de datos de mayor envergadura. 

La creación de metadatos no tiene que ser necesariamente una labor propia del técnico o equipo de técnicos que crean los datos en sí, del mismo modo que el escritor de un libro no es el encargado de catalogar este. Tanto usuarios como creadores de datos geográficos deben poseer unos conocimientos básicos en relación a los metadatos, pero existen expertos en metadatos a quien la creación de estos debe corresponder en última instancia.

Los usuarios deben saber consultar e interpretar los metadatos, y ser conscientes de la importancia de estos y el papel que juegan en una buena parte de las operaciones que pueden desarrollarse con los datos. Los creadores, por su parte, deben ser capaces de elaborar no los metadatos en sí directamente, pero sí la información necesaria acerca de los datos que debe incluirse en los metadatos, y transmitirla de forma correcta a los profesionales encargados de crear esos metadatos.

Herramientas para crear metadatos
--------------------------------------------------------------

Existe un amplio conjunto de herramientas que facilitan la labor de creación de metadatos. Entre ellas podemos distinguir las siguientes  :cite:p:`metadataPrimer`.


* Editores de texto. Los metadatos pueden almacenarse en un fichero de texto plano, y por tanto pueden editarse con cualquier programa que permita la creación y edición de tales ficheros. Lo habitual en este caso es disponer de un fichero plantilla que contenga los distintos campos que se han de registrar para cada conjunto de datos geográficos, y la creación del metadato consiste simplemente en apoyarse en esa plantilla y a continuación de cada nombre de campo añadir el valor correspondiente.

* Formularios. A partir de una definición de campos como la anterior, se pueden desarrollar herramientas más elaboradas que presenten una interfaz gráfica con distintas cajas de texto o listas desplegables. Estas aplicaciones, además de ser más agradables para el usuario, permiten incorporar elementos de validación en el proceso, evitando que en algún campo se introduzcan valores incorrectos o avisando al usuario en caso de que un campo presente un valor sospechoso.Del mismo modo, se puede establecer qué campos son obligatorios y cuáles opcionales, y avisar en caso de que un metadato no contenga valores para todos sus campos obligatorios.

* Utilidades. Existen aplicaciones que no se emplean directamente para introducir los valores de los metadatos, pero que pueden intervenir en el proceso. Entre ellas están aquellas que chequean y validan los metadatos o las que lo preprocesan dándole un formato adecuado según unas reglas establecidas de antemano.

* Herramientas de creación automática de metadatos. Algunos de los valores que se incorporan a los metadatos pueden extraerse de los propios datos. Por ello, el proceso de creación de metadatos puede automatizarse en cierta medida, y existen aplicaciones específicamente diseñada para realizar esa tarea. 

 Las aplicaciones de creación automática de metadatos pueden, por ejemplo, analizar un archivo con una capa vectorial y crear un archivo adjunto de metadatos en el que se incluya la extensión de la capa, el tipo de geometrías que tiene o los campos de su tabla de atributos, indicando además el tipo de valor en cada uno de ellos.

 Además de estos metadatos extraídos directamente del dato geográfico, las herramientas que automatizan este proceso pueden añadir información común introducida manualmente en una única ocasión, y que se repite de forma automática en todos los datos creados. Así, por ejemplo, si una de estas herramientas automáticas se emplea en un organismo, puede establecer como creador de cada nuevo dato a esa entidad, sin necesidad de que la persona encargada de crear dicho dato deba añadir esa información manualmente cada vez que genere algo nuevo.

 El uso de herramientas automáticas no se limita al momento de creación de los datos, sino que también pueden emplearse durante la actualización de estos. Si se actualiza un dato empleando un SIG, este puede estar conectado con la aplicación de creación automática de metadatos y lanzar esta para que vuelva a analizar ese dato y actualizar los metadatos inmediatamente. Quizás sea necesario añadir información manualmente, pero una buena parte de esta habrá sido creada de forma automática, facilitando el proceso y haciéndolo más rápido.

 La importancia de este tipo de aplicaciones es grande si se tiene en cuenta que, como se ha dicho, una de las razones principales de la carencia de metadatos es la cantidad de tiempo que se requiere para elaborarlos.



Algunos ejemplos
=====================================================

La mejor forma de entender el contenido de los metadatos es ver algunos sencillos ejemplos reales. Puesto que estos datos son generalmente voluminosos (siempre que tengan el detalle necesario para ser realmente útiles), en lugar de reproducirlos aquí, puedes consultarlos en las direcciones Web  :cite:p:`ejemploMetadatos` y  :cite:p:`ejemploMetadatos2`, cada una de las cuales tiene un ejemplo concreto.

En ellas pueden verse verse los metadatos con un formato de página Web sencilla compuesta de una lista de apartados y campos, así como su valores correspondientes. A la hora de utilizar la información que estos metadatos contienen desde una aplicación tal como un servidor Web, es necesario no obstante recogerlos en un formato que dicha aplicación pueda entender y procesar utilizando un esquema dado y una semántica bien definida. Es decir, que el *software* que trabaja con metadatos no lo hace a través de documentos como los de esas páginas Web, cuyo formato tiene como único fin mostrarlos de forma legible para una persona. En el capítulo :ref:`Estandares` veremos algunos estándares relacionados con metadatos que definen formas estandarizadas de recoger estos para facilitar el trabajo de las aplicaciones los utilizan.

Si se comparan los campos y apartados que aparecen en ambas páginas, puede verse que no coinciden completamente. Eso es debido a que esos metadatos han sido generados por distintos organismos, que no utilizan una única metodología. En el mencionado capítulo :ref:`Estandares` veremos también que esas formas estandarizadas no solo lo son en lo referente al formato, sino también a los contenidos, con objeto de homogeneizar los metadatos generados por organizaciones distintas, proporcionándoles unos criterios comunes a seguir.


Resumen
=====================================================

Para que los datos sean verdaderamente útiles es necesario acompañarlos de otros datos adicionales que los describan y aporten información suplementaria acerca de ellos. Estos datos adicionales son los metadatos, y recogen información tanto de la componente espacial como de la componente temática del dato geográfico.

La importancia de los metadatos se hace patente en la gestión de la calidad de los datos, o a la hora de utilizarlos como base para procesos, pues es necesario conocer todos los detalles relativos a los datos con los que se trabaja. Sin embargo, es dentro de las IDE donde los metadatos abren gran número de nuevas posibilidades y se demuestran como una pieza imprescindible, ya que permiten que las operaciones de descubrimiento y consulta de los datos se efectúen de forma eficaz.

Los metadatos pueden asociarse con los datos geográficos en niveles de detalle diversos, desde una única entidad hasta una colección de varias capas. Esto permite trabajar con ellos en distintas granularidades. El contenido de los metadatos es también variable, y depende de esa granularidad, así como de otros parámetros, como por ejemplo el tipo de datos, ya que la información adicional que puede recogerse sobre una capa vectorial no es la misma que la correspondiente a una capa ráster.

Algunas de las secciones más importantes que encontramos en los metadatos son la identificación del dato, los valores relativos a su calidad o los relacionados con su distribución, entre otros.

