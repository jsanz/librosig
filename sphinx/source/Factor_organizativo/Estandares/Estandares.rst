.. _estandares:

**********************************************************
Estándares
**********************************************************

Olaya, Víctor; Turton, Ian


Dentro de una IDE, debe ser posible acceder a los datos desde distintos puntos y hacerlo de forma simple y eficaz. Para maximizar el valor de la IDE y hacerla más útil para todos sus actores, es imprescindible que el acceso a los datos geográficos no presente problemas. Para ello, es importante definir de forma adecuada cómo se establece la comunicación entre clientes y servidores, de forma que estos primeros no solo puedan obtener los propios datos geográficos de estos últimos, sino también realizar consultas o conocer qué otras funcionalidades se encuentran disponibles.

En otras palabras, resulta necesario definir una *lingua franca* para que todas las comunicaciones se produzcan de forma fluida. Esto obliga a establecer una cierta normalización y crear elementos estandarizados que sean conocidos e implementados por los distintos actores de la IDE, y hacerlo para cada uno de los servicios ofrecidos, así como para los propios datos.

En este capítulo veremos con detalle la importancia de los estándares y el papel exacto que juegan en una IDE, y describiremos una buena parte de los que actualmente existen.

Puesto que estos estándares están relacionados con las tecnologías cliente--servidor y las IDE, los capítulos correspondientes a estos elementos (capítulos :ref:`Servidores_y_clientes_remotos` y :ref:`IDEs` respectivamente) son un requisito necesario para comprender mejor el contenido de este capítulo.


Introducción
=====================================================

En el capítulo :ref:`Servidores_y_clientes_remotos` vimos los elementos tecnológicos que permiten ofrecer a través de una red de servicios relacionados con la información geográfica. Estos servicios eran muy diversos, y ofrecían posibilidades que iban desde obtener un dato en sí hasta la realización de consultas sobre el conjunto de operaciones que un servicio dado puede ofrecer. En todos ellos aparecen un cliente y un servidor, los cuales se comunican para realizar una tarea concreta.

Este modelo de cliente--servidor en términos tecnológicos no es muy diferente de la idea de un cliente y un proveedor de servicios en la vida real. Una persona (el cliente) que quiera adquirir un producto de un distribuidor (el servidor) debe igualmente comunicarse con él para preguntarle si dispone del producto deseado, realizar una petición de este y después recibirlo cuando el distribuidor se lo envíe. En una IDE, un usuario puede consultar el catálogo para localizar un dato concreto y después acceder a él remotamente mediante, por ejemplo, un cliente Web. Ambos esquemas de funcionamiento son muy semejantes.

Imaginemos ahora la situación en la que una persona en España desea adquirir un producto electrónico de un proveedor chino. En primer lugar, es probable que tenga dificultades para entender el catálogo de productos, pues este describirá cada uno de ellos en chino. Si consigue localizarlo y desea adquirirlo, es igualmente probable que encuentre dificultades para comunicárselo al proveedor, ya que seguirá existiendo la misma barrera lingüística. Y si finalmente recibe el producto, puede tener dificultades al utilizarlo, ya que este puede funcionar a un voltaje distinto al de la red eléctrica española o bien estar preparado para un tipo de enchufe distinto. 

Este pequeño ejemplo nos hace ver que en la relación cliente--servidor pueden surgir problemas derivados de la falta de elementos comunes entre ambos actores. Si todos los elementos que toman parte en el establecimiento de esa relación comercial estuvieran normalizados y fueran únicos, un comprador de cualquier parte del mundo podría de forma inmediata comprar un dispositivo a cualquier vendedor de otro país comunicándose en un único idioma, y tener después la garantía de poder usarlo sin problemas.

En el ámbito de la información geográfica la situación es similar a la anterior. Hay muchos formatos distintos para almacenarla y muchas formas distintas de transmitirla, y ello dificulta el trabajo en el marco de una IDE. Igual que los clientes españoles no hablan el mismo idioma que los vendedores chinos, no todos los clientes SIG hablan el mismo idioma que todos los servidores, y dos cualesquiera de ellos no han de *entenderse* necesariamente.

De hecho, históricamente los distintos fabricantes de clientes definían por sí mismos la forma en que sus programas se comunicaban, que no coincidía con la del resto de fabricantes. Un cliente de un fabricante dado no podría acceder a los servicios de un servidor creado por un fabricante distinto. Este paradigma, característico del software privativo, es un problema en el marco de una IDE, pues dificulta el acceso a los datos.

En circunstancias ideales, en el marco de la IDE debe existir una total *interoperabilidad* con independencia de los formatos y las aplicaciones empleadas, pudiendo interactuar entre sí los distintos clientes y servidores. Los estándares son el elemento que va a permitir esa interoperabilidad, definiendo el marco común que clientes y servidores emplearán para entenderse. En un contexto altamente heterogéneo tanto en datos como en herramientas, lograr esto no resulta una tarea sencilla :cite:p:`Lemmenes2006IEEE`, y los estándares son los encargados de aportar homogeneidad tecnológica y favorecer todo el trabajo a desarrollar dentro de una IDE. 

Estándares abiertos e interoperabilidad
=====================================================

La interoperabilidad implica que podemos sustituir unos elementos del sistema en el que se incluyen los clientes y servidores por otros distintos, teniendo la seguridad de que van a interaccionar entre ellos sin dificultades. Las funcionalidades que un cliente o servidor nos ofrece pueden ser distintas a las de otro, pero independientemente de su origen (independientemente del fabricante), si esos elementos implementan un estándar dado, siempre podrán interactuar con todos aquellos que también lo implementen.

La clave, por tanto, está en los estándares, y en particular en que estos sean estándares *abiertos*. Un estándar es un documento o práctica que busca armonizar los aspectos técnicos de un producto o servicio. 

Un estándar se considera como tal cuando es empleado por un grupo o comunidad, que lo acepta para la definición de las características de ese producto o servicio en su seno. Si únicamente es el uso del estándar el que lo ratifica como tal, se denomina estándar *de facto*. El formato *shapefile* para capas vectoriales, por ejemplo, es uno de estos estándares, ya que está ampliamente difundido y existe tal cantidad de datos en este formato que todas las aplicaciones deben implementarlo para tener valor práctico.

Existen estándares que se convierten en normas o estándares *de iure*, cuando estos son promovidos por algún organismo oficial de normalización o su uso se impone con carácter legal. 

Un estándar *abierto* es aquel cuya definición se encuentra disponible y todo aquel que lo desee puede conocerla y emplearla para el desarrollo de la actividad relacionada con ese estándar. En nuestro campo de trabajo, eso quiere decir que cualquier desarrollador que desee crear un nuevo cliente o servidor para datos SIG puede acceder al estándar y desarrollar en base a este.

Los principios fundamentales de los estándares abiertos son los siguientes  :cite:p:`perensEstandares`:


* Disponibilidad. Los estándares abiertos están disponibles para todos el mundo para su lectura y uso en cualquier implementación.
* Máxima posibilidad de elección para los usuarios finales. Los estándares abiertos crean un mercado competitivo y justo, y no bloquean a los usuarios en el entorno de un vendedor particular. Desde el punto de quienes venden la tecnología SIG, esto no es tan ventajoso, ya que permite la aparición de competidores que antes no podían existir. Si un fabricante basa sus productos en un estándar cerrado definido por él mismo, otros no pueden elaborar soluciones que trabajen con esos productos, ya que no conocen el estándar empleado. 
 Asimismo, el fabricante puede cambiar el estándar utilizado por, por ejemplo, su producto de servidor, y obligar a los consumidores y a todo aquel que quiera utilizar un servicio basado en ese servidor a que actualicen también los clientes, pues los anteriores ya no podrán comunicarse con el nuevo servidor. Utilizando estándares abiertos, la competencia entre fabricantes ha de basarse puramente en las capacidades que ofrecen, con lo que los consumidores ganan en calidad de los productos y en posibilidades de elección.
* Gratuidad. Implementar un estándar es gratuito, sin necesidad de pagar, como en el caso de una patente. Los organismos que generan los estándares pueden cobrar una cierta cantidad por acceder a la definición de los estándares, con objeto de financiar así la labor que desarrollan, y también pueden cobrar por emitir certificados de que un determinado producto o servicio se ha desarrollado de acuerdo con el estándar.
* Discriminación. Los estándares abiertos y las organizaciones que los desarrollan no favorecen de ningún modo a uno u otro implementador sobre los restantes.
* Extensión o creación de subconjuntos de un estándar. Los estándares abiertos pueden ser extendidos o bien presentados como subconjuntos del estándar original.
* Prácticas predatorias. Los estándares abiertos pueden tener licencias que requieran a todo aquel que desarrolle una extensión de dicho estándar la publicación de información acerca de esa extensión, y el establecimiento de una licencia dada para todos aquellos que creen, distribuyan y vendan *software* compatible con ella. Un estándar abierto no puede prohibir de otro modo el desarrollo de extensiones.


Para tener una noción de lo que en la práctica realmente significa el uso de estándares abiertos en el campo de los SIG y las IDE, podemos ver la figura :num:`#figesquemanointeroperable`, donde se representa el esquema de una arquitectura no interoperable. Es decir, una arquitectura que no se basa en este tipo de estándares.

.. _figesquemanointeroperable:

.. figure:: Esquema_no_interoperable.*
	:width: 650px
	:align: center

	Esquema de una arquitectura no interoperable.


 


Los datos que se encuentran en cada base de datos son accesibles únicamente a través de un único cliente, que es aquel correspondiente al servidor que ofrece servicios basados en esos datos. Los restantes datos quedan fuera del alcance de ese cliente, ya que no es capaz de acceder a ellos. Las diferentes soluciones cliente--servidor crean en esta situación un conjunto de islas tecnológicas, cada una completamente independiente y sin posibilidad alguna de interactuar con las restantes.

Entre los principales inconvenientes de una arquitectura no interoperable como la representada podemos citar los siguientes:


* Desperdicio de recursos. Cada servicio debe gestionar sus propio conjunto de datos, lo cual requiere abundantes recursos y no es sencillo, además de implicar un elevado coste.
* Necesidad de conocer múltiples clientes. Si para acceder a cada servicio necesitamos su cliente particular, acceder al conjunto de servicios ofrecidos por esos servidores requiere por parte de los usuarios aprender a utilizar tantos clientes como servidores existan.
* Imposibilidad de combinar datos}. Dos datos a los que pueda accederse a través de dos servidores distintos no podrán utilizarse simultáneamente en un único cliente, ya que este no podrá comunicarse con ambos servidores. Un análisis que requiera distintos tipos de datos no podrá realizarse si todos ellos no se ofrecen a través de un mismo servidor.
* Imposibilidad de combinar funcionalidades. Los datos ofrecidos por un servidor pueden usarse para el desarrollo de muchas tareas. Estas tareas requieren que las correspondientes herramientas estén disponibles en los clientes, y estos se diferencian notablemente, de la misma forma que lo hacen también los SIG de escritorio entre sí. Si acceder a los datos a través de un servidor solo se puede hacer empleando un cliente concreto, no existe la posibilidad de aprovechar las funcionalidades de otro cliente sobre esos mismos datos, y el usuario ve así limitadas sus posibilidades de trabajo.


En contraste con lo anterior, tenemos una situación de plena interoperabilidad basada en estándares abiertos como la representada en el esquema de la figura :num:`#figesquemainteroperable`.

.. _figesquemainteroperable:

.. figure:: Esquema_interoperable.*
	:width: 650px
	:align: center

	Esquema de una arquitectura interoperable.


 


En este caso, existe un servidor que es el que gestiona y ofrece los servicios para cada base de datos, pero a él pueden acceder todos los clientes, ya que por el hecho de estar basados en estándares abiertos es posible una comunicación plena entre dos cualesquiera de ellos.

En esta situación, un usuario puede emplear su cliente favorito (siempre que este implemente los estándares pertinentes) para acceder a muchos servicios distintos, o bien puede utilizar varios clientes para acceder a unos mismos datos, eligiendo en cada momento el que más le convenga según sus necesidades. Las posibilidades de trabajo se multiplican cuando la arquitectura del sistema se fundamenta en estándares abiertos.

Las ventajas no son solo para los usuarios, sino también para los desarrolladores. A la hora de crear un cliente, no es necesario comprobar que este se comunica bien con todos los servidores y funciona correctamente, sino simplemente seguir las especificaciones del estándar. Todo aquel servidor que las implemente funcionará sin dificultades, ya que el estándar garantiza la buena comunicación y la interoperabilidad.

Entidades creadoras de estándares
=====================================================

Crear un estándar no es una labor sencilla. Se han de recoger las principales necesidades y armonizar todas ellas en una especificación única, de modo que clientes y servidores que implementen ese estándar sean de la mayor utilidad posible para todos los usuarios.

Existen organizaciones dedicadas a redactar las especificaciones correspondientes a estándares que cubran los distintos servicios, así como a promoverlas y mejorarlas. Los estándares más habituales en el campo de la información geográfica son elaborados por tres organizaciones: el Open Geospatial Consortium (OGC), ISO y W3C.

Open Geospatial Consortium (OGC)
--------------------------------------------------------------

El Open Geospatial Consortium  :cite:p:`webOGC` es una organización internacional y voluntaria dedicada a la elaboración de estándares. En el OGC participan más de 350 organizaciones miembro, incluyendo entre ellas a los principales fabricantes del sector, agencias nacionales, grupos de investigación u organizaciones sin ánimo de lucro, entre otros. Estas organizaciones miembro colaboran para alcanzar consensos y desarrollar e implementar estándares en el ámbito de los contenidos geoespaciales.

Algunos de los estándares OGC más relevantes, los cuales veremos a lo largo de este capítulo, son los siguientes:


* WMS. Para obtener imágenes de mapas.
* WCS. Para obtener y consultar coberturas.
* WFS. Para obtener y editar entidades geográficas y sus atributos asociados.
* WPS. Para servicios de procesos remotos.
* GML. Para almacenamiento de información geográfica.
* CSW. Para consultas en catálogos.


Cada uno de estos estándares está descrito en una especificación, y estas están sujetas a cambios y mejoras, existiendo varias versiones en cada caso. 


ISO
--------------------------------------------------------------

ISO  :cite:p:`webISO` es una organización internacional dedicada a la elaboración de estándares no solo en el ámbito geográfico, sino en todas las áreas. ISO es responsable, por ejemplo, de estándares bien conocidos y aplicados en la industria actual, tales como los relacionados con la gestión medioambiental en empresas o los estándares de calidad.

Dentro de ISO existen diversos comités técnicos, cada uno de los cuales se encarga de definir los estándares correspondientes a un campo de trabajo. El comité ISO/TC 211 es el responsable de aquellos relacionados con la información geográfica digital.

ISO redacta Especificaciones Técnicas y Estándares Internacionales, catalogando estos con un número que los identifica. Los elaborados por ISO/TC 211 corresponde a la serie 19100.

Existe una estrecha relación entre ISO y OGC, y los estándares elaborados por ambas organizaciones son muchos de ellos muy similares o incluso idénticos. De hecho, algunos de los estándares desarrollados por el OGC, como WMS o GML, citados anteriormente y que en breve detallaremos, son también estándares ISO.

En  :cite:p:`webDocsISOTC211` puede consultarse la lista de normas ISO/TC211 aprobadas y el estado de cada uno de sus documentos de trabajo.

W3C
--------------------------------------------------------------

El Consorcio World Wide Web (W3C) es un consorcio internacional donde las organizaciones miembro, personal a tiempo completo y el público en general, trabajan conjuntamente para desarrollar estándares Web. Según su propia definición :cite:p:`webW3C`, la misión del W3C es *guiar la Web hacia su máximo potencial a través del desarrollo de protocolos y pautas que aseguren el crecimiento futuro de la Web*.

El W3C no guarda una relación directa con los SIG, pero parece lógico pensar que todo aquello que se haga en el seno de Internet debería acomodarse a las pautas establecidas por este consorcio, en especial si lo que se desea es maximizar la interoperabilidad, como ya hemos visto que resulta de interés en el ámbito SIG. Puesto que la mayoría de los estándares abiertos que vamos a ver en este capítulo se aplican sobre tecnologías que operan en la red, estos se han de fundamentar siempre que sea posible en otros existentes desarrollados por el W3C, o al menos seguir las recomendaciones de este organismo.

Visto de otro modo, el W3C persigue objetivos similares a los de las organizaciones que elaboran estándares para la información geoespacial, pero su campo de actuación es la red en términos generales.

De entre todos los elementos definidos por el W3C, resulta de especial importancia el lenguaje XML (*eXtensible Markup Language*, Lenguaje de Marcado Extensible). XML no es un lenguaje en sí, sino que permite definir la gramática de otros lenguajes. Es lo que se conoce como *metalenguaje*. De este modo, puede utilizarse para definir reglas para crear formas de expresión que permitan recoger cualquier tipo de información. Esto hace que pueda emplearse para el intercambio de información de toda clase, y como veremos es la base de la mayoría de estándares a tratar en este capítulo.

Entrar en detalles acerca de XML escapa del ámbito de este libro. No obstante, para aquellos que deseen saber más, Internet está llena de buenas referencias libres sobre XML, como por ejemplo  :cite:p:`wikibookXML`.

Estándares para representación y obtención de información geográfica
======================================================================

Entre los estándares más importantes encontramos aquellos que especifican la forma de recoger la información geográfica, así como aquellos que definen el modo en que esta se transmite.

Los siguientes estándares OGC forman parte de este grupo.

.. _simplefeatures:

Simple Features for SQL (SFS)
------------------------------

Sabemos del capítulo :ref:`Consultas` que el lenguaje SQL en su forma básica no sirve para recoger las geometrías que forman la parte espacial de una entidad, sino únicamente los datos no espaciales de esta. Sin embargo, versiones posteriores de SQL permiten la definición de tipos personalizados, y esto puede emplearse para poder incorporar estos elementos espaciales dentro del lenguaje.

El problema surge debido a que la propia flexibilidad de este mecanismo permite que los tipos se implementen de diversas formas, lo cual no favorece la interoperabilidad. Si una consulta se establece sobre unos tipos definidos de forma distinta a como lo están en la base de datos que recibe la consulta, esa consulta no podrán procesarse correctamente. Es necesario definir una forma estandarizada de definir esos tipos, y una pauta a seguir para su implementación.

OGC define la especificación *Simple Features for SQL* (SFS)  :cite:p:`webSFS` con objeto de hacer frente al problema anterior. SFS define por un lado unos tipos estandarizados para geometrías, los cuales se basan en otra especificación OGC denominada *OpenGIS Geometry Model*, que establece una forma de definir geometrías. Por otra parte, se definen una serie de operaciones SQL que operan sobre esos tipos.

Todas las geometrías que pueden definirse según este esquema son geometrías en un espacio bidimensional, y cada objeto geométrico está asociado a un sistema de referencia en el cual se define.

Existe un objeto fundamental denominado *Geometry* del que heredan los restantes en una jerarquía bien definida (Figura :num:`#figjerarquiaclasessfs`). Los métodos de este objeto son de tres tipos:


* Métodos básicos. Proveen información sobre el objeto (dimensión, tipo de geometría, sistema de referencia, etc.)
* Métodos para comprobar relaciones espaciales entre objetos geométricos (cruza a, contiene a, se intersecta con, etc.)
* Métodos que efectúan algún tipo de análisis (unión de geometrías, distancia entre geometrías, area de influencia de una geometría, etc.)


.. _figjerarquiaclasessfs:

.. figure:: Jerarquia_clases_SFS.*
	:width: 650px
	:align: center

	Esquema de clases de geometrías en *Simple Features for SQL.*


Cada uno de los objetos derivados de la clase raíz *Geometry* tiene además a su vez sus propios métodos específicos, siempre dentro de alguno de los grupos anteriores.

Con estos objetos y sus métodos se da respuesta a todas las necesidades que aparecen en la realización de consultas sobre bases de datos espaciales. La especificación SFS permite así dotar de potencia al lenguaje de consulta SQL y hacerlo de forma estandarizada para ampliar la interoperabilidad en las operaciones de consulta.

Geography Markup Language (GML)
-----------------------------------------------------

El *Geography Markup Language* (GML)  :cite:p:`webGML` es un lenguaje basado en XML, diseñado para el almacenamiento de información geográfica. Utilizando este lenguaje, resulta posible el intercambio de información geográfica de forma interoperable.

GML puede utilizarse para transmitir información a través de una red, como parte de un servicio. Este es el caso del servicio WFS que veremos más adelante, que devuelve información geográfica codificada según este lenguaje. No obstante, puede emplearse igualmente para almacenar la información con la que trabajamos de un SIG, del mismo modo que utilizamos cualquiera de los formatos de archivo que vimos en el capítulo :ref:`Fuentes_datos`. Es decir, sin que tengan que mediar servicios en ningún momento.

Algunos SIG permiten este uso, y soportan GML como un formato más de archivo. No obstante, no es una práctica común, ya que, pese a las ventajas de ser un estándar aceptado, GML es un formato de fichero de tipo texto (está basado en XML) y produce archivos de gran tamaño. Para este uso, es más habitual recurrir a algún otro formato.

GML es un lenguaje extremadamente genérico, que permite recoger tanto datos ráster como vectoriales y hacerlo con mucha flexibilidad. Permite, por ejemplo, recoger datos vectoriales sin que exista una geometría asociada, es decir, simplemente almacenando unos atributos como si se tratara de una base de datos no espacial. Esta gran flexibilidad, que es uno de los puntos fuertes de GML, es también uno de sus inconvenientes, ya que la especificación es muy compleja y difícil de implementar en su totalidad.

La versión más reciente de GML es GML3, aunque GML2 es la más extendida.

Existe un dialecto conocido como *Simple Features Protocol* que trata de solucionar el problema de la excesiva complejidad de GML3, ofreciendo las ventajas más importantes de este frente a GML2, pero sin incorporar todos sus elementos.

Web Feature Service (WFS)
-----------------------------------------------------

El servicio *Web Feature Service* WFS  :cite:p:`webWFS` está relacionado con los datos de tipo vectorial, y a través de él se sirven directamente las entidades de un dato vectorial con sus geometrías y datos alfanuméricos asociados. Desde este punto de vista, acceder a un servicio WFS es similar a acceder a una capa vectorial cualquiera o a una base de datos, ya que el SIG puede recuperar la información correspondiente (tanto la componente geográfica como la temática de cada entidad) y operar con ella.

En particular, las operaciones que permite un servicio WFS son:


* Crear una nueva entidad.
* Borrar una entidad.
* Actualizar una entidad.
* Obtener o consultar el conjunto de entidades en base a condiciones espaciales y no espaciales.


Para realizar lo anterior, un servicio WFS debe permitir las siguientes operaciones:


* ``GetCapabilities``. Esta operación devuelve los metadatos correspondientes al propio servicio WFS. Estos contienen una descripción del contenido del servicio y los parámetros que este acepta a la hora de realizar peticiones sobre él. Es decir, la respuesta a esta operación es un documento que informa acerca del servicio y de los datos disponibles a través de este. Este documento es un archivo XML que debe comunicar al cliente el tipo de entidades que sirve y las operaciones que soporta sobre estas.		
* ``DescribeFeatureType``. La respuesta a esta operación es la descripción de la estructura de las entidades que pueden servirse, indicando tipo de geometría y nombre y tipo de campos asociados a esta.
* ``GetFeature``. Como respuesta a esta operación, el servidor devuelve un conjunto de entidades. El cliente puede especificar restricciones tanto espaciales como no espaciales en los parámetros de la operación, para así limitar el conjunto de entidades obtenidas. Estas entidades son devueltas por el servidor en formato GML.
* ``Transaction``. El servidor puede realizar transacciones. Estas se componen de operaciones que modifican las entidades, tales como la creación de una nueva, o la actualización o eliminación de una ya existente.


En función de lo anterior, podemos distinguir dos tipos de servicios WFS:


* Un servicio WFS básico, que solo provee las tres primeras operaciones. Es decir, que permite consultar los datos, pero no modificarlos.
* Un servicio WFS transaccional (WFS--T) que implementa la operación de transacción y por tanto permite realizar modificaciones en las entidades.


La versión más actual de la especificación WFS es la 1.1. No obstante, la versión 1.0 es la implementada mayoritariamente en los servidores actuales. WFS 1.1 utiliza GML3 como lenguaje para la codificación de la información a servir, mientras que WFS 1.0 usa GML2.

Filter Encoding
--------------------------------------------------------------

Cuando un cliente efectúa una petición a un servidor WFS, no es necesario que obtenga de este todas las entidades de una capa. Incluso para una zona geográfica dada, el usuario puede querer obtener a través del cliente solo aquellas entidades que cumplan un criterio dado. 

Ya conocemos elementos que permiten realizar ese tipo de consultas para trabajar con un subgrupo de las entidades de una capa. En el capítulo :ref:`Consultas` vimos el lenguaje SQL, mediante el cual podían definirse consultas de esta clase.

El estándar Filter Encoding  :cite:p:`FilterEncoding` define un formato basado en XML para el almacenamiento de expresiones de filtrado según otro estándar OGC conocido como *OGC Common Catalog Query Language*. La expresión del filtro expresada según la especificación Filter Encoding puede ser validada y procesada por herramientas adicionales para convertirla en las expresiones correspondientes en otro lenguaje para consulta de bases de datos espaciales. Por ejemplo, en una clausula ``WHERE`` de SQL que emplear en una sentencia ``SELECT``.

Las expresiones que pueden recogerse empleando *Feature Encoding* pueden ser consultas con componente espacial o hacer referencia a la parte temática de la información geográfica. Es decir, que permiten recoger toda la variabilidad de las consultas espaciales que vimos en el capítulo :ref:`Consultas`

Además de emplear estas expresiones para consultar servicios WFS, pueden utilizarse igualmente para otros como los servicios de Nomenclátor (Gazetteer) que veremos más adelante, y en general en todos aquellos en los que tenga sentido especificar algún tipo de restricción a la hora de realizar una petición al servidor.

Web Coverage Service (WCS)
-----------------------------------------------------

Si el estándar WFS permite obtener de un servidor datos vectoriales en forma de entidades, el estándar *Web Coverage Service* hace lo propio con datos ráster. Este servicio está pensado para tratar con *coberturas*, es decir, representaciones de un fenómeno que varía en el espacio. Como ya vimos en su momento, las coberturas se corresponden con el modelos de campos.

Representar una cobertura puede hacerse de muchas formas distintas: capas ráster, Redes de Triángulos Irregulares (TIN) o funciones matemáticas. No obstante, por el momento el estándar WCS solo está preparado para el trabajo con mallas ráster regulares.

EL servicio WCS ofrece los datos de la capa ráster como tales, con su semántica original. Es decir, que un servicio WCS puede servir un MDE y el cliente obtiene directamente los valores de elevación en sus unidades correspondientes. %Después será el cliente el que se encargue de asignarle la representación que se desee para la capa obtenida, en función de esos valores.

De forma similar a WFS, WCS presenta tres operaciones básicas que permiten consultar al servicio por sus características o por las características de los datos de que dispone, y obtener finalmente los datos en sí.


* ``GetCapabilities``. Describe las capacidades del servicio, indicando las coberturas de que dispone.
* ``DescribeCoverage``. Describe una cobertura particular
* ``GetCoverage``. Obtiene una de las coberturas disponibles. Los parámetros de esta operación se emplean para indicar al servidor la extensión que se desea cubrir. %, del mismo modo que en el caso de WMS.


Estándares para mapas y visualización
=====================================================

De entre todos los estándares que vamos a ver en este capítulo, los más importantes por ser los más extendidos son los que sirven mapas. Entendemos por *mapa* en este contexto a una representación gráfica de una determinada información geográfica, elaborada a partir de una o más capas.

Gran parte de los sitios Web que ofrecen información geográfica lo hacen en forma de mapas, es decir, que permiten simplemente *ver* los datos geográficos, y los estándares de esta sección son los encargados de definir ese tipo de servicios.

El estándar WMS, el principal en esta categoría, está ampliamente probado e implementado en gran cantidad de software, y es el soporte fundamental para cientos de aplicaciones basadas en mapas, lo que ratifica su utilidad y validez.


Web Map Service (WMS)
--------------------------------------------------------------

El estándar *Web Map Service* (WMS)  :cite:p:`webWMS` define los elementos necesarios para un servicio de mapas.

Un servicio WMS devuelve una imagen con información geográfica, pero esta solo contiene la propia información visual para que el cliente pueda mostrarla. Es decir, si se pide a este servicio un mapa creado a partir de un MDE, la información de los píxeles no contiene la elevación de la coordenada correspondiente, sino el color asociado en función de un determinado criterio. La imagen puede contener otros elementos visuales tales como etiquetas o símbolos, en función de cómo se haga la representación en el servidor. Una vez que el cliente recibe la imagen, no puede actuar sobre esta para cambiar la forma de representación de una capa, sino simplemente representarla como es.

Se definen en este servicio tres operaciones básicas, dos de ellas obligatorias y la restante opcional, que son empleadas por los clientes para consultar los servidores. %Junto a ésto, define el conjunto de parámetros de consulta posibles y su comportamiento asociado.

Las tres operaciones fundamentales son:


* ``GetCapabilities`` (obligatoria): Al igual que en el caso de WFS y WMS, esta operación describe el servicio, informando de los mapas disponibles.

* ``GetFeatureInfo`` (opcional): Esta operación permite al cliente pedir al servidor información particular sobre algunas entidades representadas en el mapa. Si el servidor soporta esta operación, los mapas que devuelve pueden consultarse. Para ello, la consulta hecha por el cliente debe añadir ciertos parámetros adicionales como una localización (una coordenada dentro de la imagen) y el número de entidades cercanas de las que se desea obtener información.

* ``GetMap`` (obligatoria): Esta operación devuelve una imagen de un mapa con unos parámetros geoespaciales y dimensionales (tamaño de la imagen) definidos. El cliente utiliza esta función para obtener un conjunto rectangular de píxeles, los cuales conforman una imagen de un mapa correspondiente a una zona geográfica dada, o un conjunto de elementos gráficos dentro de esa zona.

La operación *GetMap* permite asimismo al cliente especificar qué capas emplear para formar la imagen a obtener, el sistema de referencia a utilizar, el área geográfica a cubrir o el formato en el que se desea recibir la imagen (de entre una serie de formato habituales soportados).

Las capas pueden especificarse como accesos a otros servicios tales como WFS.


En un servicio WMS, cuando el cliente pide un mapa al servidor, puede controlar en cierto modo la forma en que este va a representarlo (colores, estilos, etc.). El servidor ofrece una serie de opciones predeterminadas, de las cuales el cliente solo conoce su nombre, y puede elegir una de ellas. No obstante, no puede saber exactamente qué caracteriza a cada uno de esos perfiles predeterminados de representación ni tampoco puede definir los suyos propios.

Para solucionar esto y ampliar las capacidades del servicio WMS, aparece otro nuevo estándar: SLD.

.. _sld:

Standard Layer Description (SLD)
--------------------------------------------------------------



El estándar OGC *Standard Layer Description* (SLD)  :cite:p:`webSLD` define una forma de almacenar los parámetros de representación empleados para crear un mapa a partir de los datos geográficos. Este estándar permite extender las capacidades de WMS, ofreciendo al cliente la posibilidad de definir sus propias configuraciones.

SLD es un estándar complejo que permite cubrir situaciones variadas y no solo las más sencillas y habituales. Permite, por ejemplo, el ajuste de elementos tales como etiquetas o simbologías personalizadas para elementos puntuales (por ejemplo, representar cada punto de una capa de localizaciones de estaciones de autobús con un pequeño dibujo de un autobús), Para esto último se apoya en otros estándares tales como SVG  :cite:p:`webSVG`, diseñado para la representación de gráficos vectoriales.

Las simbologías recogidas en un documento SLD pueden emplearse para la representación tanto de capas ráster como vectoriales.

A la hora de definir una simbología para una capa, es necesario conocer cierta información acerca de esta. Para definir una simbología sencilla en la que todos los elementos de una capa van a ser representados de igual forma (por ejemplo, todos las líneas de una capa de ríos con un grosor dado y en color azul), esta información no es imprescindible, pero en caso de que se quiera variar ese color o ese grosor en función de un atributo, será necesario conocer qué atributos tiene la capa y de qué tipo son.

Para hacer esto, pueden emplearse las operaciones de los servicios de donde se toman los datos a representar. La operación *DescribeLayers* del servicio WFS permite conocer los tipos de entidades de una capa representada. La información sobre los atributos puede obtenerse con la operación *DescribeFeatureTypes*.

Web Mapping Context (WMC)
--------------------------------------------------------------

El estándar *Web Mapping Context* (WMC)  :cite:p:`webWMC` define un formato estandarizado para almacenar un *contexto*. Un *contexto* recoge la información necesaria para reproducir las condiciones de una determinada sesión de uso de un cliente, de tal forma que ese cliente pueda restablecerlas posteriormente. El contexto se almacena en un archivo XML.

En el contexto se almacena información sobre las capas que forman el mapa representado por el cliente y los servidores de los que estas se obtienen, la región cubierta por el mapa, así como información adicional para anotar este mapa.

Los usos que se le pueden dar a un contexto son variados, entre ellos los siguientes:


* Mediante un contexto se puede definir una configuración particular de inicio para distintos tipos de usuario del cliente.
* Un contexto puede emplearse para almacenar el estado del cliente a medida que el usuario navega y modifica elementos, pudiendo retornar a una configuración establecida anteriormente.
* El contexto puede almacenarse y después transferirse a otro cliente distinto en el que comenzar en una misma configuración.


Los contextos pueden a su vez catalogarse y descubrirse, ofreciendo así un nivel de granularidad más amplio que las capas individuales. Pueden crearse diferentes contextos predefinidos y después hacer estos accesibles para facilitar el establecimiento de una determinada configuración en un cliente.

.. _estandarescatalogos:

Estándares para metadatos, catálogos y consulta de datos
============================================================



Los metadatos y las operaciones sobre ellos tienen sus propios estándares bien definidos. 

Por una parte, existen estándares dedicados a los metadatos en sí y a la forma de almacenarlos. Estos pueden especificar parámetros relativos a los metadatos tales como los siguientes:


* Contenido de los metadatos, definiendo qué campos son obligatorios y cuáles opcionales.
* Formato de almacenamiento. En general, una descripción del formato a emplear.
* Prácticas adecuadas de creación y actualización. Se definen las pautas correctas que han de seguirse a lo largo del ciclo de vida de los datos.
* Reglas de conformidad. Reglas que permiten comprobar si un determinado metadato se encuentra conforme con el estándar.


Por otro lado, un conjunto de metadatos conforma la base para las consultas sobre un catálogo, el cual describe a su vez un conjunto de datos. Como ya vimos, el catálogo constituye una forma más sencilla y eficaz de consultar los datos, agilizando las operaciones y permitiendo el descubrimiento de datos de forma óptima, por lo que la consulta de estos metadatos también debe estar estandarizada, y debe definirse cómo los clientes deben obtener la información de los metadatos para posteriormente, a partir de dicha información, realizar el acceso a los datos correspondientes que resulten de interés.

ISO 19115 e ISO 19119
--------------------------------------------------------------

ISO 19115 e ISO 19119 son los estándares ISO para metadatos asociados a información geográfica. Definen más de 400 elementos, de los cuales los siguientes forman parte de su núcleo fundamental.


* Título
* Fecha de referencia de los datos
* Idioma
* Categoría en que encuadrar la temática de los datos
* Resumen
* Punto de contacto para los metadatos
* Fecha de los metadatos
* Organismo responsable de los datos
* Localización
* Juego de caracteres de los datos
* Resolución espacial
* Formato de distribución
* Tipo de representación espacial
* Sistema de referencia
* Recurso en línea
* Identificador del fichero de metadatos
* Nombre del estándar de metadatos
* Versión del estándar de metadatos
* Idioma de los metadatos
* Juego de caracteres de los metadatos


En España, existe el Núcleo Español de Metadatos (NEM), un subconjunto de la ISO 19115 definido por un subgrupo de trabajo de la IDEE.


Nomenclátor (Gazetteer)
-------------------------------------------------------------- 

.. _nomenclator:

Un *nomenclátor* o {gazeteer} permite la localización de fenómenos geográficos a partir de un determinado nombre. El catálogo sobre el que se basa es una colección de estos fenómenos, cada uno de ellos asociados a un identificador geográfico. Dicho identificador es una referencia espacial en forma de etiqueta o código que identifica un lugar en el mundo real  :cite:p:`iso19112`. Ejemplos de tales identificadores son los nombres de ciudades o pueblos (Burgos, Plasencia), los códigos postales (10600), los accidentes geográficos (Puerto de Navacerrada, Pico de la Miel) o las direcciones (Carretera N--V p.k.35, Calle Mayor 32), entre otros. Así, el servicio de nomenclátor permite establecer un sistema de referencia basado en identificadores geográficos.

El servicio recibe como entrada un nombre y utiliza este para localizar los fenómenos geográficos que cumplen un criterio. Este criterio puede ser variable, pudiendo exigir que el nombre coincida plenamente, que comience por él, o que lo contenga, entre otras opciones. Es habitual además que el catálogo contenga una tipología de los fenómenos recogidos (población, río, puerto, lago, etc.), de forma que esta también puede utilizarse para establecer el criterio de consulta (por ejemplo, para localizar todos los ríos que comiencen con las letra *b*).

En el terreno de los nomenclátor encontramos la Norma ISO 19115:2003 (*Geographic Information -- Spatial referencing by Geographic Identifiers*), y los *OGC Catalog Services*, que permiten estandarizar procesos de consulta como los mencionados.

Estándares para procesamiento
=====================================================

Además de servir datos, pueden servirse procesos sobre esos datos, de tal forma que existan procesos remotos a los que los clientes pueden acceder. También debe estandarizarse la forma de acceso a estos servicios y cómo los clientes efectuarán las peticiones de procesos y la transmisión o definición de los datos que han de tomarse para esos procesos.

Web Processing Service (WPS)
-----------------------------------------------------

El estándar *Web Processing Service* (WPS) de OGC está enfocado a definir el marco en el que se ha de producir el servicio de procesos remotos. WPS define una interfaz estándar que facilita la publicación de procesos y su uso posterior por parte de clientes. Se entiende por proceso en este contexto a todo aquel algoritmo, cálculo o modelo que opere sobre datos georreferenciados.

Los procesos que pueden definirse son sumamente flexibles, pudiendo tener un número cualquiera de entradas y salidas, y operar con distintos tipos de datos. Es decir, que ofrece un marco para definir cualquier tipo de proceso de análisis geográfico, tanto si este utiliza datos ráster como si utiliza datos vectoriales. Todos los procesos que hemos visto en la parte :ref:`Procesos` de este libro pueden ofrecerse como servicios remotos a través de WPS.

Los datos empleados para alimentar los procesos pueden encontrarse en el propio servidor o ser transmitidos a través de la red al igual que la propia petición de proceso por parte del cliente. Asimismo, puede relacionarse este estándar con otros que ya hemos visto, como por ejemplo WFS. Los datos necesarios para ejecutar un proceso que requiera una capa vectorial pueden obtenerse llamando a un servicio WFS, en cuyo caso debe indicarse en los parámetros del proceso los propios parámetros que corresponden a la petición a ese servicio WFS.

WPS define tres operaciones básicas, todas ellas obligatorias para todo servidor que implemente este estándar:


* ``GetCapabilities``. Al igual que en otros estándares que ya hemos visto, esta operación hace que el servidor ofrezca los metadatos referentes al servicio. En este caso, estos incluyen la definición de todos los procesos que es capaz de ejecutar el servidor. 
* ``DescribeProcess``. El servidor devuelve la definición detallada de uno de los procesos soportados, especificando número y tipo de entradas y salidas, y formatos válidos para estas.
* ``Execute``. Esta operación pide la ejecución de un proceso con unas entradas dadas, y la obtención de los resultados de este.


Relación entre estándares
=====================================================

Los estándares que hemos visto a lo largo de estás páginas guardan una lógica relación entre ellos. Dentro de un mismo ámbito, los estándares pueden guardar relación con otros similares aun habiendo sido desarrollados por entidades distintas. El objetivo de armonización tecnológica que pretenden los estándares resulta más difícil de lograr si el número de estándares para una misma tecnología es elevado, ya que los fabricantes necesitan dedicar más tiempo y recursos a implementar todos ellos, y lo normal es que opten por implementar solo algunos.

Por este motivo, las organizaciones que promueven estándares trabajan conjuntamente y suelen producir estándares muy similares. En algunos casos, como ya hemos mencionado, algunos estándares OGC son también estándares ISO, existiendo no una similitud sino una absoluta coincidencia.

Más importante es la relación que guardan entre sí estándares dedicados a áreas distintas. Las tecnologías para la gestión y transmisión de datos  incluyen diversos elementos que forman un todo interrelacionado como vimos en el capítulo :ref:`Servidores_y_clientes_remotos`. Los estándares correspondientes a esos elementos y a cada proceso particular que se desarrolla deben formar también un todo conectado y poder a su vez *entenderse* con otros estándares relacionados.

Un caso particular de esto es, por ejemplo, el de los estándares WMS, SLD y WFS. El servicio WMS ofrece un mapa, que no es sino una representación de unos datos según unos criterios dados. Esos datos pueden obtenerse de un servicio WFS y los criterios para representarlos pueden expresarse utilizando el estándar SLD. La ventaja de los estándares abiertos, máxime si estos han sido además creados por una misma organización, es la capacidad de interoperar entre ellos, de forma que WMS puede tomar datos de servicios WFS o WCS, o una consulta conforme a Filter Encoding puede aplicarse para consultar un servicio WFS y también un servicio de nomenclátor.

Otro ejemplo en esta línea es el que hemos descrito para un servicio WPS que toma datos de un servicio WFS para operar con ellos.

En su conjunto deben verse todos los estándares como una gran familia de elementos que armoniza el trabajo con la información geográfica, potenciando así el cumplimiento de los objetivos de la IDE.


Resumen
=====================================================

Los estándares abiertos son básicos en el entorno de las IDE para garantizar una correcta comunicación entre clientes y servidores, y su adopción implica una larga serie de ventajas, aumentando las posibilidades de uso de la IDE y la potencia de los datos y herramientas que se incluyen en estas.

Existen diversas organizaciones que desarrollan estos estándares, siendo OGC e ISO las más relevantes en el campo de la información geográfica, y W3C en el campo de la World Wide Web. Estás organizaciones han creado estándares que son de aplicación en diversas tareas. 

Para la codificación y almacenamiento de la información geográfica encontramos estándares a nivel conceptual como SFS, y otros para la propia codificación y creación de archivos como GML. Este último es el empleado también para la transmisión de información geográfica según el estándar WFS, definido para el trabajo con datos vectoriales. Para servir coberturas (en la especificación actual equivalentes a datos ráster regulares), encontramos el estándar WCS.

Existen igualmente estándares para mapas, como WMS, que a su vez se apoyan en los anteriores para obtener los datos a representar, y en otros como SLD para establecer los parámetros de esa representación.

Los estándares se encuentra interrelacionados entre sí y se apoyan unos en otros. El conjunto de todos ellos permite en el seno de una IDE el trabajo fluido y la interoperabilidad en todas las operaciones que se realizan.

