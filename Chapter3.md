# Requirements Specification

## To-Be Scenario Mapping

![To-Be Scenario Map - Usuario Cliente](assets/Tobe-1.png "To-Be Scenario Map - Usuario Cliente")

![To-Be Scenario Map - Tienda Comercial](assets/Tobe-2.png "To-Be Scenario Map - Tienda Comercial")

## User Stories

A continuación, mostramos las historias de usuario que consideramos más importantes.

#### Epics

|Epic ID|Título|Descripción|Número de User Stories asociados|
|:----:|:----:|:----:|:----:|
|EP01|Almacenamiento de preferencias|Como cliente, quiero poseer una cuenta propia para guardar mis configuraciones.|2|
|EP02|Funcionalidades de probador|Como cliente, quiero contar con las funcionalidades de un probador de prendas para probarme ropa de manera virtual.|5|
|EP03|Asociación con tiendas|Como dueño de una tienda, quiero asociar mi negocio con el probador virtual para que mis clientes puedan acceder y comprar mis productos desde esta interfaz.|1|

#### User Stories

| User Story ID | Título | Descripción | Scenarios & Acceptance Criteria | Epic ID |
|:--:|:--:|:--:|:--|:--:|
|US01|Realidad aumentada para observar productos|Como cliente, quiero que mediante realidad aumentada pueda observar una representación de un producto, para poder conocerlo de mejor manera|SC01: Ingreso al probador y selecciono un producto para el uso de realidad aumentada <br><br> AC01 <br> **Dado que** me encuentro en el apartado de realidad aumentada. <br> **Cuando** elija el producto a mostrar <br> **Y** le otorgue permiso al uso de realidad aumentada <br> **Entonces** la aplicación utilizará la cámara del equipo y mostrará el producto |EP02|
|US02|Creación de cuenta con el proveedor de la tienda|Como cliente, quiero poder crear una cuenta para guardar mis datos, preferencias y obtener mejores recomendaciones en el futuro|SC02: El cliente está en el probador e inicia la creación de su cuenta <br><br> AC02 <br> **Dado que** me encuentro en el apartado de creación de cuenta <br> **Cuando** selecciono la opción para registrarme <br> **Y** asocio mi cuenta de la tienda en la que estoy <br> **Entonces** mi cuenta se creará <br> **Y** mis datos serán almacenados|EP02|
|US03|Lectura de código QR para inicio de sesión|Como cliente quiero leer el código QR que se encuentra en la pantalla del probador para obtener recomendaciones personalizadas a mis gustos|SC03: El cliente entra al probador y encuentra el código QR en la pantalla <br><br> AC03 <br> **Dado que** encuentro el código QR en la pantalla <br> **Cuando** abra la aplicación de la tienda y escanee el código <br> **Entonces** el probador cargará mi perfil de recomendaciones e información personal <br> **Y** podré obtener recomendaciones personalizadas|EP02|
|US04|Generación de orden de compra|Como cliente quiero generar una orden de compra para poder pagar la prenda que he decido que me llevaré|SC04: El cliente tiene la prenda en el probador <br><br> AC04 <br> **Dado que** tengo la prenda que me quiero llevar conmigo <br> **Cuando** seleccione comprar prenda <br> **Entonces** se me permitirá realizar el pago de la prenda en la caja o a través de un POS integrado <br><br> SC05: El cliente no tiene la prenda en el probador <br><br> AC05 <br> **Dado que** no tengo la prenda que me quiero llevar conmigo <br> **Cuando** seleccione comprar prenda <br> **Entonces** se me permitirá ir a caja para recoger mi orden y realizar el pago respectivo|EP03|
|US05|Agregar productos a la lista de favoritos|Como cliente, quiero agregar productos a una lista de favoritos, para organizar mejor los productos que son de mi interés y mejorar las recomendaciones|SC06: El cliente agrega un producto a su lista de favoritos <br><br> AC06 <br> **Dado que** estoy viendo un producto <br> **Cuando** selecciono la opción para agregarlo a mis favoritos <br> **Entonces** el sistema agregará el producto a mi lista de favoritos <br> **Y** mi algoritmo de recomendaciones mejorará|EP01|
|US06|Selección de diferentes modelos o colores de prenda|Como cliente, quiero personalizar el modelo o colores de la prenda que me probaré virtualmente para ampliar mis opciones de compra|SC07: El cliente personaliza el modelo de prenda <br><br> AC07 <br> **Dado que** estoy viendo un producto con múltiples modelos <br> **Cuando** selecciono alguna otra opción de modelo <br> **Entonces** el sistema me mostrará la prenda virtualmente con realidad aumentada|EP01|
|US07|Búsqueda de un artículo|Como cliente, quiero buscar un producto en particular en una barra de búsqueda para obtener resultados de prendas de vestir que quiera probarme|SC08: El cliente escribe en la barra de búsqueda <br><br> AC08: <br> **Dado que** quiero encontrar un tipo de prenda específica <br> **Cuando** escriba en la barra de búsqueda con la pantalla táctil <br> **Y** aplique los filtros que necesite <br> **Entonces** el sistema me mostrará las prendas que coincidan|EP02|
|US08|Solicitud de asistencia a un trabajador|Como cliente, quiero que un trabajador de la tienda me traiga una prenda seleccionada para probármela físicamente|SC07: El cliente encontró una prenda que quiere probarse físicamente después de probársela virtualmente <br><br> AC09 <br> **Dado que** encontré una prenda que quiero probarme físicamente <br> **Cuando** solicite que un encargado me traiga la prenda física al probador <br> **Entonces** se comunicará a un encargado para que recoja la prenda <br> **Y** podré recibir la prenda para probármela físicamente|EP02|