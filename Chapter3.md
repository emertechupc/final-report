# Requirements Specification

## To-Be Scenario Mapping

Nos brinda una visión de la experiencia futura de usuario y es un gran artefacto para poner frente a frente a las a las partes interesadas. En el caso del usuario cliente notamos que un punto importante es el tener la capacidad de probarse por medio de su dispositivo móvil las prendas que sean de su agrado.

![To-Be Scenario Map - Usuario Cliente](assets/Tobe-1.png "To-Be Scenario Map - Usuario Cliente")

En el caso de las tiendas comerciales vemos que la capacidad de ofrecer el servicio adicional con el cual los clientes pueden probarse cualquier prenda representan un punto importante para resolver los problemas que se presentaban en el As-is Scenario Map.

![To-Be Scenario Map - Tienda Comercial](assets/Tobe-2.png "To-Be Scenario Map - Tienda Comercial")

## User Stories

A continuación, mostramos las historias de usuario que consideramos más importantes.

#### Epics

<table>
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
    <th>Número de User Stories asociados</th>
  </tr>
  <tr>
    <td>EP01</td>
    <td>Almacenamiento de preferencias</td>
    <td>Como cliente, quiero poseer una cuenta propia para guardar mis configuraciones.</td>
    <td>2</td>
  </tr>
  <tr>
    <td>EP02</td>
    <td>Funcionalidades de probador</td>
    <td>Como cliente, quiero contar con las funcionalidades de un probador de prendas para probarme ropa de manera virtual.</td>
    <td>5</td>
  </tr>
  <tr>
    <td>EP03</td>
    <td>Asociación con tiendas</td>
    <td>Como dueño de una tienda, quiero asociar mi negocio con el probador virtual para que mis clientes puedan acceder y comprar mis productos desde esta interfaz.</td>
    <td>1</td>
  </tr>
</table>

#### User Stories

<table>
  <tr>
    <th>User Story ID</th>
    <th>Título</th>
    <th>Descripción</th>
    <th>Scenarios & Acceptance Criteria</th>
    <th>Epic ID</th>
  </tr>
  <tr>
    <td>US01</td>
    <td>Realidad aumentada para observar productos</td>
    <td>Como cliente, quiero que mediante realidad aumentada pueda observar una representación de un producto, para poder conocerlo de mejor manera</td>
    <td>SC01: Ingreso al probador y selecciono un producto para el uso de realidad aumentada <br><br> AC01 <br> <strong>Dado que</strong> me encuentro en el apartado de realidad aumentada. <br> <strong>Cuando</strong> elija el producto a mostrar <br> <strong>Y</strong> le otorgue permiso al uso de realidad aumentada <br> <strong>Entonces</strong> la aplicación utilizará la cámara del equipo y mostrará el producto</td>
    <td>EP02</td>
  </tr>
  <tr>
    <td>US02</td>
    <td>Creación de cuenta con el proveedor de la tienda</td>
    <td>Como cliente, quiero poder crear una cuenta para guardar mis datos, preferencias y obtener mejores recomendaciones en el futuro</td>
    <td>SC02: El cliente está en el probador e inicia la creación de su cuenta <br><br> AC02 <br> <strong>Dado que</strong> me encuentro en el apartado de creación de cuenta <br> <strong>Cuando</strong> selecciono la opción para registrarme <br> <strong>Y</strong> asocio mi cuenta de la tienda en la que estoy <br> <strong>Entonces</strong> mi cuenta se creará <br> <strong>Y</strong> mis datos serán almacenados</td>
    <td>EP02</td>
  </tr>
  <tr>
    <td>US03</td>
    <td>Lectura de código QR para inicio de sesión</td>
    <td>Como cliente quiero leer el código QR que se encuentra en la pantalla del probador para obtener recomendaciones personalizadas a mis gustos</td>
    <td>SC03: El cliente entra al probador y encuentra el código QR en la pantalla <br><br> AC03 <br> <strong>Dado que</strong> encuentro el código QR en la pantalla <br> <strong>Cuando</strong> abra la aplicación de la tienda y escanee el código <br> <strong>Entonces</strong> el probador cargará mi perfil de recomendaciones e información personal <br> <strong>Y</strong> podré obtener recomendaciones personalizadas</td>
    <td>EP02</td>
  </tr>
  <tr>
    <td>US04</td>
    <td>Generación de orden de compra</td>
    <td>Como cliente quiero generar una orden de compra para poder pagar la prenda que he decidido que me llevaré</td>
    <td>SC04: El cliente tiene la prenda en el probador <br><br> AC04 <br> <strong>Dado que</strong> tengo la prenda que me quiero llevar conmigo <br> <strong>Cuando</strong> seleccione comprar prenda <br> <strong>Entonces</strong> se me permitirá realizar el pago de la prenda en la caja o a través de un POS integrado <br><br> SC05: El cliente no tiene la prenda en el probador <br><br> AC05 <br> <strong>Dado que</strong> no tengo la prenda que me quiero llevar conmigo <br> <strong>Cuando</strong> seleccione comprar prenda <br> <strong>Entonces</strong> se me permitirá ir a caja para recoger mi orden y realizar el pago respectivo</td>
    <td>EP03</td>
  </tr>
  <tr>
    <td>US05</td>
    <td>Agregar productos a la lista de favoritos</td>
    <td>Como cliente, quiero agregar productos a una lista de favoritos, para organizar mejor los productos que son de mi interés y mejorar las recomendaciones</td>
    <td>SC06: El cliente agrega un producto a su lista de favoritos <br><br> AC06 <br> <strong>Dado que</strong> estoy viendo un producto <br> <strong>Cuando</strong> selecciono la opción para agregarlo a mis favoritos <br> <strong>Entonces</strong> el sistema agregará el producto a mi lista de favoritos <br> <strong>Y</strong> mi algoritmo de recomendaciones mejorará</td>
    <td>EP01</td>
  </tr>
  <tr>
    <td>US06</td>
    <td>Selección de diferentes modelos o colores de prenda</td>
    <td>Como cliente, quiero personalizar el modelo o colores de la prenda que me probaré virtualmente para ampliar mis opciones de compra</td>
    <td>SC07: El cliente personaliza el modelo de prenda <br><br> AC07 <br> <strong>Dado que</strong> estoy viendo un producto con múltiples modelos <br> <strong>Cuando</strong> selecciono alguna otra opción de modelo <br> <strong>Entonces</strong> el sistema me mostrará la prenda virtualmente con realidad aumentada</td>
    <td>EP01</td>
  </tr>
  <tr>
    <td>US07</td>
    <td>Búsqueda de un artículo</td>
    <td>Como cliente, quiero buscar un producto en particular en una barra de búsqueda para obtener resultados de prendas de vestir que quiera probarme</td>
    <td>SC08: El cliente escribe en la barra de búsqueda <br><br> AC08: <br> <strong>Dado que</strong> quiero encontrar un tipo de prenda específica <br> <strong>Cuando</strong> escriba en la barra de búsqueda con la pantalla táctil <br> <strong>Y</strong> aplique los filtros que necesite <br> <strong>Entonces</strong> el sistema me mostrará las prendas que coincidan</td>
    <td>EP02</td>
  </tr>
  <tr>
    <td>US08</td>
    <td>Solicitud de asistencia a un trabajador</td>
    <td>Como cliente, quiero que un trabajador de la tienda me traiga una prenda seleccionada para probármela físicamente</td>
    <td>SC07: El cliente encontró una prenda que quiere probarse físicamente después de probársela virtualmente <br><br> AC09 <br> <strong>Dado que</strong> encontré una prenda que quiero probarme físicamente <br> <strong>Cuando</strong> solicite que un encargado me traiga la prenda física al probador <br> <strong>Entonces</strong> se comunicará a un encargado para que recoja la prenda <br> <strong>Y</strong> podré recibir la prenda para probármela físicamente</td>
    <td>EP02</td>
  </tr>
</table>

## Impact Mapping

En la presente sección se presenta el Impact Mapping de nuestro modelo de negocio digital, el cual fue elaborado con la herramienta UXPressia. Para su elaboración se realizó previamente las fichas para los User Persona de nuestros segmentos objetivos.

Como se puede observar en el artefacto se han incluido los Bussiness Goals. Asimismo, hemos incluido los Actors que en este caso serían nuestros User Personas analizados previamente. Por un lado, en la columna Impact hemos incluido los enunciados de cómo deseamos que los User Persona cambien o se comporten. También se responde a la pregunta “¿Qué tendría él/ella que hacer para ayudar a que se logre la meta?”. Por otro lado, en la columna Deliverables se incluye los elementos que respondan la pregunta “¿Qué puedo hacer como negocio digital para provocar esos Impacts?”. Por último, en la columna User Stories se incluye la descripción de los User Stories empleando el formato “**Como**... **quiero**... **para**...”, el cual permite obtener los features que nos ayudarán a producir los Deliverables identificados.

![Impact Map](assets/impact-map.png "Impact Map")

## Product Backlog

En esta sección se incluirán los User Stories con su respectiva estimación y priorización.

<table>
  <tr>
    <th># Orden</th>
    <th>User Story ID</th>
    <th>Título</th>
    <th>Descripción</th>
    <th>Story Points (1/2/3/5/8)</th>
  </tr>
  <tr>
    <td>1</td>
    <td>US01</td>
    <td>Realidad aumentada para observar productos</td>
    <td>Como cliente, quiero que mediante realidad aumentada pueda observar una representación de un producto, para poder conocerlo de mejor manera</td>
    <td>8</td>
  </tr>
  <tr>
    <td>2</td>
    <td>US06</td>
    <td>Selección de diferentes modelos o colores de prenda</td>
    <td>Como cliente, quiero personalizar el modelo o colores de la prenda que me probaré virtualmente para ampliar mis opciones de compra</td>
    <td>2</td>
  </tr>
  <tr>
    <td>3</td>
    <td>US07</td>
    <td>Búsqueda de un artículo</td>
    <td>Como cliente, quiero buscar un producto en particular en una barra de búsqueda para obtener resultados de prendas de vestir que quiera probarme</td>
    <td>3</td>
  </tr>
  <tr>
    <td>4</td>
    <td>US08</td>
    <td>Solicitud de asistencia a un trabajador</td>
    <td>Como cliente, quiero que un trabajador de la tienda me traiga una prenda seleccionada para probármela físicamente</td>
    <td>8</td>
  </tr>
  <tr>
    <td>5</td>
    <td>US05</td>
    <td>Agregar productos a la lista de favoritos</td>
    <td>Como cliente, quiero agregar productos a una lista de favoritos, para organizar mejor los productos que son de mi interés y mejorar las recomendaciones</td>
    <td>1</td>
  </tr>
  <tr>
    <td>6</td>
    <td>US04</td>
    <td>Generación de orden de compra</td>
    <td>Como cliente quiero generar una orden de compra para poder pagar la prenda que he decidido que me llevaré</td>
    <td>5</td>
  </tr>
  <tr>
    <td>7</td>
    <td>US02</td>
    <td>Creación de cuenta con el proveedor de la tienda</td>
    <td>Como cliente, quiero poder crear una cuenta para guardar mis datos, preferencias y obtener mejores recomendaciones en el futuro</td>
    <td>5</td>
  </tr>
  <tr>
    <td>8</td>
    <td>US03</td>
    <td>Lectura de código QR para inicio de sesión</td>
    <td>Como cliente quiero leer el código QR que se encuentra en la pantalla del probador para obtener recomendaciones personalizadas a mis gustos</td>
    <td>3</td>
  </tr>
</table>
