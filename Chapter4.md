# Strategic-Level Software Design

## Strategic-Level Attribute Driven Design

En esta sección, realizaremos el proceso de Attribute-Driven Design para abordar nuestra solución centrada en productos y tecnologías de Digital Transformation. Comenzaremos con una introducción seguida de un detallado análisis de los elementos y exploraremos el proceso de diseño, Inputs, Architectural Drivers, Design Decisions, Quality Attribute Scenarios and Initial High-Level Solution Architecture Views.

### Design Purpose

El propósito fundamental del proceso de diseño de nuestra solución es abordar de manera efectiva la problemática que enfrentan tanto las tiendas por departamento como los consumidores. Buscamos transformar la experiencia de compra, proporcionando a nuestros clientes la capacidad de explorar, probar y verificar la disponibilidad de prendas de vestir de manera virtual, a través de realidad aumentada. Se tiene como objetivo satisfacer las necesidades de los segmentos objetivo al ofrecer una experiencia de compra más personalizada e impulsar el crecimiento y la eficiencia en el negocio de las tiendas por departamento.

### Attribute-Driven Design Inputs

#### Primary Funcionality (Primary User Stories)

| Epic / User Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| EP02 | Funcionalidades de probador | Como cliente, quiero contar con las funcionalidades de un probador de prendas para probarme ropa de manera virtual. | - | - |
| EP03 | Asociación con tiendas | Como dueño de una tienda, quiero asociar mi negocio con el probador virtual para que mis clientes puedan acceder y comprar mis productos desde esta interfaz. | - | - |
| US01 | Realidad aumentada para observar productos | Como cliente, quiero que mediante realidad aumentada pueda observar una representación de un producto, para poder conocerlo de mejor manera. | AC01 DADO que me encuentro en el apartado de realidad aumentada, CUANDO elija el producto a mostrar Y le otorgue permiso al uso de realidad aumentada, ENTONCES la aplicación utilizará la cámara del equipo y mostrará el producto | EP02 |
| US03 | Lectura de código QR para inicio de sesión | Como cliente quiero leer el código QR que se encuentra en la pantalla del probador para obtener recomendaciones personalizadas a mis gustos. | AC03: DADO que encuentro el código QR en la pantalla CUANDO abra la aplicación de la tienda y escanee el código, ENTONCES el probador cargará mi perfil de recomendaciones e información personal Y podré obtener recomendaciones personalizadas | EP02 |
| US04 | Generación de orden de compra | Como cliente quiero generar una orden de compra para poder pagar la prenda que he decido que me llevaré. | AC04 DADO que tengo la prenda que me quiero llevar conmigo CUANDO seleccione comprar prenda, ENTONCES se me permitirá realizar el pago de la prenda en la caja o a través de un POS integrado | EP03 |

#### Quality attribute scenarios

En esta sección, presentaremos la especificación inicial de los Quality Attribute Scenarios que desempeñarán un papel fundamental en la configuración de la arquitectura de nuestra solución. En la siguiente tabla, detallaremos estos Quality Attribute Scenarios para dar forma a nuestra visión arquitectónica.

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Fiabilidad | Cliente final | Búsqueda de prendas después de una falla de conexión a Internet | Sistema de probador virtual | Conexión inestable o intermitente | El sistema continúa operando de manera adecuada, proporcionando funcionalidades esenciales incluso con una conexión intermitente | El 95% de las operaciones fueron exitosas durante la falla de conexión |

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Fiabilidad | Cliente final | El usuario reinicia el sistema después de un fallo de hardware |  Sistema de probador virtual  | Sistema en estado de reinicio por fallo | El sistema inicia correctamente y recupera el estado previo, permitiendo al usuario continuar con sus actividades | El tiempo de inicio es menor a 3 minutos y el porcentaje de éxito en la recuperación es del 99% |

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Usabilidad | Nuevo cliente final | El usuario visualiza la página de inicio del probador virtual por primera vez |  Página de inicio del probador virtual  | Página principal del probador virtual | El usuario encuentra información clara y concisa que le indica que el software es un probador virtual de prendas de vestir | El porcentaje de nuevos usuarios que identifican claramente el próposito del software es de 90% |

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Usabilidad | Cliente final | El usuario selecciona una prenda y la visualiza en el probador virtual | Vista detallada de la prenda | Sistema de probador virtual | El usuario puede operar y controlar las funciones del probador virtual para visualizar la prenda con facilidad | El tiempo promedio para que un usuario seleccione y visualice una prenda es menor a 2 minutos |

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Eficiencia de desempeño | Cliente final | El usuario selecciona una prenda para visualizar en el probador virtual | Vista detallada de la prenda | Tienda con conexión a Internet de alta velocidad | El sistema carga y visualiza la prenda en el probador virtual | El tiempo promedio de carga de prendas en el probador virtual es menor a 2 segundos |

| Atributo   | Fuente     | Estímulo   | Artefacto  | Entorno    | Respuesta  | Medida     |
|------------|------------|------------|------------|------------|------------|------------|
| Eficiencia de desempeño | Cliente final | El usuario selecciona múltiples prendas para visualizar y comparar en el probador virtual | Vista detallada de la prenda | Tienda con conexión a Internet de alta velocidad | El sistema carga y visualiza prendas simultáneamente en el probador virtual sin pérdida de rendimiento | El número máximo de prendas que pueden ser visualizadas simultáneamente sin pérdida de rendimiento es de 10 |

#### Constraints

| Technical Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| ------------------ | ------ | ----------- | ----------------------- | ------------------------- |
| TS01 | Integración con Sistemas de Tiendas por departamento | La integración con los sistemas de tiendas existentes puede estar limitada por la compatibilidad y los recursos disponibles en las tiendas. | DADO que se inicie el proceso de integración con una tienda por departamento, CUANDO se establezca la comunicación y se compartan datos entre el software y la tienda, ENTONCES se debe confirmar que la integración se ha realizado con éxito, lo que se reflejará en la capacidad del software para acceder y utilizar los datos de esa tienda de manera efectiva. | EP03 |
| TS02 | Limitación de Recursos de Hardware | Las capacidades de hardware disponibles en los probadores convencionales pueden limitar la ejecución de características de realidad aumentada y procesamiento. | DADO que el software se esté ejecutando en el probador virtual con dispositivos de cierta antiguedad, CUANDO se realice una acción que requiera el uso intensivo de recursos ENTONCES el software debe responder de manera eficiente y sin retrasos significativos para proporcionar una experiencia fluida al usuario. | EP02 |
| TS03 | Disponibilidad de Conexión a Internet | La disponibilidda de una conexión a internet confiable puede ser una limitación en algunos probadores. | DADO que el software esté operando en condiciones de baja conectividad, CUANDO se realice una acción que requiera acceso a datos o recursos en línea, ENTONCES el software debe mantener su funcionalidad y rendimiento de manera óptima, asegurando que los usuarios puedan seguir utilizando las funcionalidades críticas incluso en condiciones de baja conectividad sin interrupciones significativas. | EP01, EP03 |
| TS04 | Compatibilidad con Dispositivos Móviles | El software de probador virtual debe ser compatible con una variedad de dispositivos móviles para brindar una experiencia óptima. | DADO que se ejecute el software en una variedad de dispositivos móviles, CUANDO el usuario inicie el software en un dispositivo específico, ENTONCES el software debe ser capaz de funcionar de manera compatible y sin problemas en dispositivos que ejecuten sistemas operativos tanto iOS como Android. | EP02 |

### Architectural Drivers Backlog

A continuación, se establecen el conjunto de Architectural Drivers como parte del proceso iterativo en el proceso de Quality Attribute Workshop. Se incluyen los Functional Drivers seleccionados, los Quality Attribute Drivers seleccionados y todos los Constraints.

| Driver ID | Título de Driver | Descripción | Importancia para Stakeholders (High, Medium, Low) | Impacto en Architecture Technical Complexity (High, Medium, Low) |
|-----------|------------------|-------------|-----------------------------------------------|-----------------------------|
|           |                  |             |                                               |                             |                                        |
|           |                  |             |                                               |                             |                                        |
|           |                  |             |                                               |                             |                                        |

### Architectural Design Decisions

A continuación, se detalla la explicación del proceso siguiendo los Stages del Quality Attribute Workshop, resumiendo para cada iteración, cuáles fueron los Drivers considerados, las tácticas y patrones que se evaluaron y los criterios para llegar sus decisiones de diseño.

| Driver ID | Título de Driver | Pattern 1               |
|-----------|------------------|------------------------|
|           |                  | Pro          | Con          |
|           |                  |              |              |
|           |                  |              |              |

### Quality Attribute Scenario Refinements

En la siguiente sección se especifican la relación de escenarios priorizados para atributos de calidad.

## Strategic-Level Domain-Driven Design

### EventStorming

El equipo colaboró efectivamente para explorar y definir las principales ideas que conforman el proceso de creación del EventStorming. Primero, nos organizamos para recapitular los principales procesos que ocurren dentro de nuestro sistema, es así que fuimos realizando un tablero con la herramienta Jamboard de Google para organizar nuestras ideas a modo de boceto sobre cómo funcionarían los flujos de un cliente usando nuestra plataforma:

![EventStorming](/assets/event-storming-1.png)

En esta primera captura de evidencia, podemos visualizar como planteamos una idea preliminar sobre el uso de nuestra solución. Evidenciamos el flujo objetivo que buscamos nuestros usuarios sigan cuando usen nuestro sistema. Por eso, puede verse como las flechas dirigen de izquierda a derecha la serie de pasos generales y externos que se realizan, mientras que la zona delimitada son todos los elementos que rodearían y compondrían nuestra solución IoT.

![EventStorming](/assets/event-storming-2.png)

Luego, en una primera versión de nuestro EventStorming, escribimos en post-its la serie de eventos y comandos que se desencadenan usando nuestra plataforma. En este primer acercamiento planteamos las ideas de arriba hacia abajo, donde los eventos que están en la parte superior desencadenan los que están debajo, y así sucesivamente. Gracias a esta técnica pudimos descubrir la serie de procesos y flujos que abarcaría y seguiría un usuario usando nuestro sistema.
En adelante, transcribimos esas ideas generales a un tablero en Lucidchart, agrupamos los eventos y comandos definidos, según afinidad, cercanía o relación, en grandes congregados delimitados como bounded contexts. De esta manera, pudimos concretar el proceso de Event Storming satisfactoriamente, obteniendo este diagrama final como resultado:

![EventStorming](/assets/event-storming-3.png)

### Candidate Context Discovery

En esta sección, identificamos mediante la técnica de **start-with-value** los contextos candidatos al profundo análisis de su funcionamiento. Esto debido a que representan la lógica principal o modelo de negocio. Estos bounded context son los dos que conforman nuestro sistema. Ambos son lo suficientemente autoexplicativos según los eventos que los componen, además definen de manera precisa cada etapa del proceso que buscamos los clientes sigan al usar nuestro sistema.

![Candidate Context Discovery](/assets/candidate-context-discovery-1.png)

![Candidate Context Discovery](/assets/candidate-context-discovery-2.png)

### Domain Message Flows Modeling

En este apartado, evidenciamos el correcto flujo de procesos ocurridos durante el uso de nuestro sistema, la interconexión e interacción entre los bounded contexts planteados y los elementos que los conforman para cumplir con el escenario ideal planteado:

![Domain Message Flows Modeling](/assets/domain-message-flows-modeling.png)

### Bounded Context Canvases

De igual manera que en las secciones previas, diseñamos los canvases de los dos bounded contexts definidos. En estos, describimos a profundidad el contenido establecido en el Event Storming.

![Bounded Context Canvases](/assets/bounded-context-canvases-1.png)

![Bounded Context Canvases](/assets/bounded-context-canvases-2.png)

### Context Mapping

![Context Mapping](/assets/context-mapping.png)

Según la interacción entre los bounded context y los sistemas externos que participan en nuestro contexto, presentamos este diagrama de mapa de contexto bajo los siguientes fundamentos: proponemos un patrón de colaboración entre el sistema externo y el bounded context de Clothing Search, específicamente el patrón Customer-Supplier, debido a que el bounded context mencionado consumirá la información del sistema externo mediante su REST API para obtener información de las prendas y demás artículos de vestir que la tienda tenga en inventario. Asimismo, cabe recalcar que ambos existen independientemente y su única interacción existe por y para fines del modelo de negocio.

Por otro lado, proponemos un patrón de cooperación entre Clothing Search y Clothing Try On, específicamente el patrón Partnertship, ya que ambos bounded context intercambian información y coordinan para lograr un fin determinado: obtener la información de determinada prenda de vestir para que el usuario pueda probársela. Esta labor conjunta favorece el logro de la funcionalidad principal de nuestro negocio.

## Software Architecture

### Software Architecture System Landscape Diagram

En este diagrama, exploramos las reglas de negocio en el más alto nivel, dando un vistazo a cómo impactan las diversas restricciones de nuestro modelo y su influencia en la toma de decisiones arquitectónica a nivel de software.
![Software Architecture System Landscape Diagram](/assets/sa-system-landscape-diagram.png)

### Software Architecture Context Level Diagrams

Introduciéndonos al modelo C4, este primer diagrama de contexto nos ayuda a visualizar y entender cómo nuestro Sistema interactúa con los principales agentes externos involucrados en el negocio, ya sean usuarios o sistemas de terceros.

![Software Architecture Context Level Diagram](/assets/sa-context-level-diagram.png)

### Software Architecture Container Level Diagrams

Si nos adentramos un nivel más, este diagrama de contenedores nos da un vistazo acercado y enfocado a lo que contiene nuestro Sistema o solución de software. Aquí es donde visualizamos por primera vez la aparición de nuestros bounded context y denotamos cómo interactúan entre sí.

![Software Architecture Container Level Diagram](/assets/sa-container-level-diagram.png)

### Software Architecture Deployment Diagrams

Este diagrama nos muestra y ayuda a entender la ejecución de arquitectura del Sistema y conocer qué entornos de ejecución usaremos, tomando en cuenta las tecnologías a la vanguardia hoy por hoy y las mejores decisiones arquitectónicas respecto a la solución.

![Software Architecture Deployment Diagram](/assets/sa-deployment-diagram.png)
