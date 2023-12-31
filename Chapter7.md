# Product Implementation, Validation & Deployment

En el presente capítulo, el equipo describirá todos los procesos seguidos para la implementación y desarrollo de la suite de productos que conforman el ecosistema Fitster.

## Software Configuration Management

Antes de empezar a detallar el aspecto técnico del desarrollo de las soluciones, definiremos la configuración de los entornos que tendrá cada miembro del equipo para poder implementar uniformemente los productos mencionados.

### Software Development Environment Configuration

Utilizaremos principalmente los siguientes IDEs: [Visual Studio Code](https://code.visualstudio.com/) o [WebStorm](https://www.jetbrains.com/webstorm/), cada una con la configuración debida para no generar conflictos con las carpetas ‘.idea’ y ‘.vscode’. Más adelante, utilizaremos [Visual Studio 2022](https://visualstudio.microsoft.com/) o [Rider](https://www.jetbrains.com/rider/) para la implementación de la APIs.
Para el desarrollo del frontend web, usaremos la librería web [React](https://react.dev/)
Para el desarrollo de la aplicación móvil utilizaremos el framework [Flutter](https://docs.flutter.dev/) con el lenguaje de programación [Dart](https://docs.flutter.dev/).
Para el desarrollo del backend, utilizaremos el lenguaje de C# (<https://docs.microsoft.com/en-us/dotnet/csharp/>) junto con [.NET](https://dotnet.microsoft.com/es-es/apps/aspnet) como framework.
Como herramientas SaSS, utilizaremos [GitHub](https://github.com/) como herramienta de colaboración de código. La herramienta [Figma](https://www.figma.com/) se usó para la elaboración de los diseños de interfaz visual de baja y alta fidelidad de nuestras aplicaciones[Vertabelo](https://vertabelo.com/) fue utilizado para el desarrollo del diagrama de bases de datos. [LucidChart](https://www.lucidchart.com/) para la creación de diagramas diversos.

### Source Code Management

Utilizaremos GitHub para llevar el control de nuestras versiones de desarrollo. Para tal efecto, hemos creado una organización denominada [Emertech Solutions](https://github.com/emertechupc) en la que tenemos todos los repositorios necesarios. Adjuntamos también los enlaces a cada repositorio de las respectivas soluciones Fitster:

- [Landing Page: Fitster Website](https://github.com/emertechupc/fitster_website)
- [Aplicación Web: Fitster Inventory](https://github.com/emertechupc/fitster_inventory)
- [Aplicación Móvil: Fitster](https://github.com/emertechupc/fitster_app)
- [API: Fitster Backend](https://github.com/emertechupc/fitster_backend)

### Source Code Style Guide & Conventions

Para las convenciones o estilos de programación, seguiremos convenciones básicas de camelCase y UpperCamelCase según el caso. Además, la guía de estilo de Google para programar en HTML y CSS (Google HTML/CSS Style Guide).
En cuanto a las convenciones para el control de versiones, utilizaremos conventional commits tanto para la creación de ramas (aplicando type/title) como para la creación de commits (type(optional scope): description). Como, por ejemplo:

- Rama: feat/main-component
- Commit -> feat(ui): added main componente template

Con respecto a la creación de ramas, se utilizarán feature branches siguiendo el modelo de GitFlow, con la nomenclatura mencionada previamente. Nuestra rama principal será la rama main, la cual contendrá nuestra versión de la aplicación que se encuentra en producción. Todas las feature branches y hotfixes se realizarán a esta rama.

### Software Deployment Configuration

Para el Landing page se utilizó GitHub Pages para el despliegue inmediato de dicha página.
Para la aplicación web Fitster Inventory, el despliegue se hará en Vercel.
Para nuestra RESTful API utilizaremos Azure Web App Service.

## Solution Implementation

En esta sección, detallaremos las etapas de desarrollo de software para los diversos productos de nuestra suite Fitster, separados por iteraciones o sprints bajo el marco ágil de desarrollo.

### Sprint 1

En la primera iteración, explicaremos los avances de los productos a ofrecer y la evidencia del trabajo colaborativo para alcanzar los objetivos de cada entregable.

#### Sprint Planning 1

La presenta tabla resume el planeamiento de nuestra primera iteración

<table class="tg">
<thead>
  <tr>
    <th class="tg-fymr">Sprint #</th>
    <th class="tg-0pky">Sprint 1</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr" colspan="2">Sprint Planning Background</td>
  </tr>
  <tr>
    <td class="tg-0pky">Date</td>
    <td class="tg-0pky">2023-10-16</td>
  </tr>
  <tr>
    <td class="tg-0pky">Time</td>
    <td class="tg-0pky">10:00 AM</td>
  </tr>
  <tr>
    <td class="tg-0pky">Location</td>
    <td class="tg-0pky">Virtual meeting (Lima)</td>
  </tr>
  <tr>
    <td class="tg-0pky">Prepared by</td>
    <td class="tg-0pky">Angel Omar Meneses Torres</td>
  </tr>
  <tr>
    <td class="tg-0pky">Attendees (to planning meeting)</td>
    <td class="tg-0pky">Angel Meneses<br>Franco Vasquez<br>James Hurtado<br>Jherico Solier<br>Juben Cacha<br>Kolya Castañeda</td>
  </tr>
  <tr>
    <td class="tg-0pky">Sprint 0 Review Summary</td>
    <td class="tg-0pky">Como este es el primer sprint que da inicio a la etapa de desarrolllo, <br>no hay alcances previos salvo el landing page.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Sprint 0 Retrospective Summary</td>
    <td class="tg-0pky">Los miembros del equipo están entusiasmados de empezar a desarrollar<br>las diferentes aplicaciones consideradas para el alcance.</td>
  </tr>
  <tr>
    <td class="tg-fymr" colspan="2">Sprint Goal &amp; User Stories</td>
  </tr>
  <tr>
    <td class="tg-0pky">Sprint 1 Goal</td>
    <td class="tg-0pky">Desarrollar las funcionalidades principales de la interfaz web para usuarios<br>que gestionarán su inventario de productos.<br>Desarollar las funcionalidades principales de la interfaz móvil para usuarios<br>clientes que se buscarán, se probarán prendas virtuales y las comprarán<br>Desarrollar la aplicación backend que ofrecerá y soportará las funcionalidades<br>de las aplicaciones frontend previamente descritas. </td>
  </tr>
  <tr>
    <td class="tg-0pky">Sprint 1 Velocity</td>
    <td class="tg-0pky">25</td>
  </tr>
  <tr>
    <td class="tg-0pky">Sum of Story Points</td>
    <td class="tg-0pky">25</td>
  </tr>
</tbody>
</table>

#### Sprint Backlog 1

A continuación, visualizamos las historias de usuario a desarrollar en esta iteración, así como su descomposición por tareas.

<table>
<thead>
  <tr>
    <th>Sprint #</th>
    <th colspan="7">Sprint 1</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan="2">User Story</td>
    <td colspan="6">Work-Item / Task</td>
  </tr>
  <tr>
    <td>Id</td>
    <td>Title</td>
    <td>Id</td>
    <td>Title</td>
    <td>Description</td>
    <td>Estimation (hours)</td>
    <td>Assigned To</td>
    <td>Status</td>
  </tr>
  <tr>
    <td>US10</td>
    <td>Resultados de búsqueda</td>
    <td>T01</td>
    <td>Vista resultados</td>
    <td>Implementar la pantalla móvil para visualizar<br>los resultados de la búsqueda de prendas</td>
    <td>4</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="4">US08<br>US09<br></td>
    <td rowspan="4">Búsqueda de prendas <br>mediante barra y mediante<br>filtros de búsqueda</td>
    <td>T03</td>
    <td>Vista de búsqueda</td>
    <td>Implementar la pantalla móvil para visualizar<br>los resultados de la búsqueda de prendas</td>
    <td>6</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T04</td>
    <td>Filtros categóricos de búsqueda</td>
    <td>Implementar la pantalla móvil para buscar prendas<br>mediante filtros</td>
    <td>6</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T05</td>
    <td>Consultas a productos</td>
    <td>Implementar las funcionalidades en backend para <br>buscar productos</td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T06</td>
    <td>Relaciones con categorías</td>
    <td>Relacionar los productos con sus entidades superiores<br>(marca, tipo de prenda, etc.) para soportar las búsquedas</td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="5">US11</td>
    <td rowspan="5">Información de producto</td>
    <td>T07</td>
    <td>Vista detalle de prenda</td>
    <td>Implementar la pantalla móvil para visualizar <br>el detalle de información de una prenda</td>
    <td>4</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T08</td>
    <td>Vista gestión de productos</td>
    <td>Implementar la interfaz web para gestionar el inventario <br>de productos</td>
    <td>6</td>
    <td>Jherico &amp; Kolya</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T09</td>
    <td>Vista gestión detalla de producto</td>
    <td>Implementar la interfaz web para gestionar la información<br>de los productos (añadir, editar)<br></td>
    <td>6</td>
    <td>Jherico &amp; Kolya</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T10</td>
    <td>Endpoint de producto</td>
    <td>Implementar el endpoint para soportar acciones de <br>obtención de los productos</td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T11</td>
    <td>Endpoint de detalle de producto</td>
    <td>Implementar el endpoint para soportar acciones de <br>obtención de detalles de los productos</td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="3">US04</td>
    <td rowspan="3">Items al carrito</td>
    <td>T12</td>
    <td>Vista carrito de compras</td>
    <td>Implementar la pantalla móvil para que el cliente gestione<br>su carrito de compras</td>
    <td>6</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T13</td>
    <td>Endpoint carrito de compras</td>
    <td>Implementar las funcionalidades backend para gestionar<br>el carrito de compras<br></td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T14</td>
    <td>Endpoint artículo del carrito</td>
    <td>Implementar las funcionalidades backend para la gestión <br>de artículos en el carrito de compras</td>
    <td>8</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="4">US05</td>
    <td rowspan="4">Generación de orden de <br>compra</td>
    <td>T15</td>
    <td>Vista confirmacion de orden</td>
    <td>Implementar la pantalla móvil para que el cliente gestione <br>la información relacionada a su orden</td>
    <td>6</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T16</td>
    <td>Vista historial de ordenes</td>
    <td>Implementar la pantalla móvil para que el cliente vea su <br>historial de ordenes</td>
    <td>2</td>
    <td>Franco &amp; Juben</td>
    <td>WIP</td>
  </tr>
  <tr>
    <td>T17</td>
    <td>Vista gráficos e insights</td>
    <td>Implementar la interfaz web para que el gestor de inventario<br>visualice datos e información relevante en gráficos sobre el <br>progreso de sus ordenes y productos</td>
    <td>6</td>
    <td>Jherico &amp; Kolya</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T18</td>
    <td>Endpoint orders</td>
    <td>Implementar las funcionalidades backend para la gestión <br>de órdenes en las aplicaciones</td>
    <td>6</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="2">US06</td>
    <td rowspan="2">Lista de favoritos</td>
    <td>T19</td>
    <td>Vista lista de favoritos</td>
    <td>Implementar la pantalla móvil para que el cliente gestione <br>sus prendas y artículos favoritos</td>
    <td>4</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T20</td>
    <td>Endpoint lista de favoritos</td>
    <td>Implementar las funcionalidades del backend para la gestión<br>de listas de favoritos y sus elementos</td>
    <td>6</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="2">US02</td>
    <td rowspan="2">Creación de cuenta</td>
    <td>T21</td>
    <td>Vista registro</td>
    <td>Implementar la pantalla móvil para que los usuarios se registren</td>
    <td>2</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T22</td>
    <td>Endpoint users</td>
    <td>Implementar las funcionalidades que soporten la creación de <br>usuarios </td>
    <td>2</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="3">US03</td>
    <td rowspan="3">Inicio de sesión</td>
    <td>T23</td>
    <td>Vista inicio de sesión</td>
    <td>Implementar la pantalla móvil para que los usuarios inicien<br>sesión en la aplicación</td>
    <td>2</td>
    <td>Franco &amp; Juben</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T24</td>
    <td>Funcionalidades auth</td>
    <td>Implementar las funcionalidades del backend que soporten el <br>inicio de sesión y el manejo de tokens para autenticar usuarios</td>
    <td>4</td>
    <td>James &amp; Angel</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>T25</td>
    <td>Vista login web</td>
    <td>Implementar la interfaz web para que los gestores de inventario<br>inicien sesión en su respectiva aplicación como admins</td>
    <td>4</td>
    <td>Jherico &amp; Kolya</td>
    <td>Done</td>
  </tr>
</tbody>
</table>

#### Development Evidence for Sprint

En esta sección, evidenciamos los principales a manera de commits en los respectivos repositorios de desarrollo de nuestra solución. Evidentemente, todo el proceso completo de desarrollo puede visualizarse en los repositorios previamente referenciados.

<table>
<thead>
  <tr>
    <th>Repository</th>
    <th>Branch</th>
    <th>Commit id</th>
    <th>Commit message</th>
    <th>Commit message body</th>
    <th>Committed on</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">fitster_inventory</td>
    <td rowspan="2">feat/jherico</td>
    <td>b197305</td>
    <td>feat</td>
    <td>frontend first base version</td>
    <td>20/10/2023</td>
  </tr>
  <tr>
    <td>7f18ef4</td>
    <td>fix</td>
    <td>change home and add product card</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td rowspan="10">fitster_app</td>
    <td rowspan="10">develop</td>
    <td>9541e3a</td>
    <td>feat</td>
    <td>add navigation bar</td>
    <td>20/10/2023</td>
  </tr>
  <tr>
    <td>f1f734d</td>
    <td>feat</td>
    <td>implementation of settings view</td>
    <td>20/10/2023</td>
  </tr>
  <tr>
    <td>f940ccf</td>
    <td>feat</td>
    <td>implementation of dark mode</td>
    <td>20/10/2023</td>
  </tr>
  <tr>
    <td>85c5325</td>
    <td>feat</td>
    <td>add icon button in appbar</td>
    <td>23/10/2023</td>
  </tr>
  <tr>
    <td>79405a3</td>
    <td>feat</td>
    <td>redesign home page &amp; provider implementation</td>
    <td>23/10/2023</td>
  </tr>
  <tr>
    <td>7d69f82</td>
    <td>feat</td>
    <td>configure navigation</td>
    <td>26/10/2023</td>
  </tr>
  <tr>
    <td>3fa27e1</td>
    <td>feat</td>
    <td>sign up view implementation</td>
    <td>26/10/2023</td>
  </tr>
  <tr>
    <td>603b542</td>
    <td>feat</td>
    <td>welcome view implementation</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>02189a8</td>
    <td>feat</td>
    <td>order view implementation</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>ddf9e83</td>
    <td>feat</td>
    <td>shopping cart view implementation</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td rowspan="19">fitster_backend</td>
    <td rowspan="9">feat/product-detail-v1</td>
    <td>d99a12a</td>
    <td>feat(products)</td>
    <td>add products domain model</td>
    <td>21/10/2023</td>
  </tr>
  <tr>
    <td>bfdce1f</td>
    <td>feat(products)</td>
    <td>add category domain model</td>
    <td>21/10/2023</td>
  </tr>
  <tr>
    <td>11ab3a3</td>
    <td>feat(products)</td>
    <td>add type domain model</td>
    <td>21/10/2023</td>
  </tr>
  <tr>
    <td>feab390</td>
    <td>feat(products)</td>
    <td>add DAPO for incoming and outgoing resources</td>
    <td>21/10/2023</td>
  </tr>
  <tr>
    <td>60cde34</td>
    <td>chore</td>
    <td>implement base repository and unit of work</td>
    <td>22/10/2023</td>
  </tr>
  <tr>
    <td>59274a0</td>
    <td>feat(products)</td>
    <td>implement service layer for products</td>
    <td>22/10/2023</td>
  </tr>
  <tr>
    <td>c10263d</td>
    <td>chore(security)</td>
    <td>add JWT validation and error middleware</td>
    <td>22/10/2023</td>
  </tr>
  <tr>
    <td>2cac718</td>
    <td>feat(users)</td>
    <td>implement services layer for users</td>
    <td>23/10/2023</td>
  </tr>
  <tr>
    <td>ee7c4ce</td>
    <td>feat</td>
    <td>implement service layer for product detail</td>
    <td>24/10/2023</td>
  </tr>
  <tr>
    <td rowspan="3">feat/shopping-cart</td>
    <td>f10dfd5</td>
    <td>feat</td>
    <td>add models for shopping domain</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>a7caa22</td>
    <td>feat</td>
    <td>implement service layer for shopping cart and items</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>40cb10e</td>
    <td>feat</td>
    <td>implement controller layer for shopping cart and items</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td rowspan="3">feat/orders</td>
    <td>ef31c08</td>
    <td>feat</td>
    <td>add order and order items models</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>a3f0e5e</td>
    <td>feat</td>
    <td>implement methods in service layer</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>80b0899</td>
    <td>feat</td>
    <td>implement controller layer for orders</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td rowspan="3">feat/wishlist</td>
    <td>030f755</td>
    <td>feat</td>
    <td>add wishlist and item models</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>c3e7612</td>
    <td>feat</td>
    <td>implement service layer for wishlists</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>b791e5c</td>
    <td>feat</td>
    <td>implement controller for wishlist item</td>
    <td>27/10/2023</td>
  </tr>
  <tr>
    <td>develop</td>
    <td></td>
    <td>feat</td>
    <td>add deployment config</td>
    <td>27/10/2023</td>
  </tr>
</tbody>
</table>

#### Execution Evidence for Sprint Review

Presentamos las capturas que evidencian la ejecución de las aplicaciones desarrolladas para este entregable:

![Sección principal del Landing Page](/assets/landing-1.png)
![Sección 'About' del Landing Page](/assets/landing-2.png)
![Sección 'Pricing' del Landing Page](/assets/landing-3.png)
![Sección 'Partners' & 'Contact' del Landing Page](/assets/landing-4.png)

Para continuar con el flujo, si presionamos el call-to-action en el landing page, nos dirigimos a la aplicación web en la que los usuarios vendedores pueden gestionar el inventario de sus productos: Fister Inventory.

![Vista 'Sign in' de Fitster Inventory](/assets/inventory-1.png)
![Vista 'Home' de Fitster Inventory](/assets/inventory-2.png)
![Vista 'Inventory' de Fitster Inventory](/assets/inventory-3.png)
![Vista 'Resources' de Fitster Inventory](/assets/inventory-4.png)
![Vista 'Contact' de Fitster Inventory](/assets/inventory-5.png)

Finalmente, mostramos las capturas de nuestra aplicación móvil: Fitster.

![Vista 'Sign up' de Fitster](/assets/mobile-1.jpg)
![Vista 'Sign in' de Fitster](/assets/mobile-2.jpg)
![Vista 'Home' de Fitster](/assets/mobile-3.jpg)
![Vista 'Search' de Fitster](/assets/mobile-4.jpg)
![Vista 'Search Results' de Fitster](/assets/mobile-5.jpg)
![Vista 'Product Detail' de Fitster](/assets/mobile-6.jpg)
![Vista 'Wishlist' de Fitster](/assets/mobile-7.jpg)
![Vista 'Shopping Cart' de Fitster](/assets/mobile-8.jpg)
![Vista 'Order' de Fitster](/assets/mobile-9.jpg)
![Vista 'Profile' de Fitster](/assets/mobile-10.jpg)

#### Services Documentation Evidence for Sprint Review

A continuación, mostramos la documentación de servicios disponibles en nuestro API que soportan las funcionalidades en nuestra interfaz móvil como web. La documentación fue realizada con [Swagger](https://swagger.io/). Adjuntamos las presentes capturas en las que puede visualizarse todos los endpoints disponibles y las acciones CRUD realizables para cada entidad considerada en el alcance de nuestra solución.

![Primera captura de documentación con Swagger](/assets/services-1.png)
![Segunda captura de documentación con Swagger](/assets/services-2.png)
![Tercera captura de documentación con Swagger](/assets/services-3.png)
![Cuarta captura de documentación con Swagger](/assets/services-4.png)
![Quinta captura de documentación con Swagger](/assets/services-5.png)

Asimismo, en la parte inferior se pueden visualizar todos los esquemas para realizar solicitudes correctamente y recibir recursos.

![Captura de esquemas de recursos y requests](/assets/services-schemas.png)

Toda esta documentación de servicios está disponible y es interactiva para las pruebas desde [Swagger UI](https://fitsterupcapi.azurewebsites.net/swagger/index.html).

#### Software Deployment Evidence for Sprint Review

Nuestro Landing Page está desplegado utiizando [GitHub Pages](https://pages.github.com/), herramienta que permite desplegar proyectos directamente desde un repositorio de GitHub. Está disponible en el presente [enlace](https://emertechupc.github.io/fitster_website/).

Nuestra aplicación web Fitster Inventory está desplegada en [Vercel](https://emertechupc.github.io/fitster_website/). Disponible en el presente [enlace](https://frontend-example-flitster.vercel.app).

Nuestra aplicación móvil Fitster está desplegada localmente para el realizar las pruebas y validaciones necesarias. Para futuras iteraciones se generará y compartirá el APK que podría ser subido a Play Store.

Nuestra API Fitster Backend y base de datos está desplegadas en [Azure Web App Services](https://azure.microsoft.com/en-us/products/app-service/web) y [Azure SQL Database](https://azure.microsoft.com/es-es/products/azure-sql/database) respectivamente. El backend está disponible en el siguiente [enlace](https://fitsterupcapi.azurewebsites.net/swagger/index.html).  

#### Team Collaboration Insights during Sprint

Adjuntamos las evidencias de desarrollo y colaboración según las tareas asignadas y responsabilidad de cada miembro para implementar las aplicaciones.

![GitHub Insights para el Landing Page](/assets/insights-1-landing.png)
![GitHub Insights para Fitster Inventory](/assets/insights-1-web.png)
![GitHub Insights para Fitster Mobile App](/assets/insights-1-mobile.png)
![GitHub Insights para Fitster Backend](/assets/insights-1-backend.png)

### Sprint 2

En la primera iteración, explicaremos los avances de los productos a ofrecer y la evidencia del trabajo colaborativo para alcanzar los objetivos de cada entregable.

#### Sprint Planning 2

La presenta tabla resume el planeamiento de nuestra segunda iteración

<table class="tg">
 <thead>
  <tr style="height: 22.2px;">
   <th class="tg-fymr" style="height: 22.2px;">Sprint #</th>
   <th class="tg-0pky" style="height: 22.2px;">Sprint 2</th>
  </tr>
 </thead>
 <tbody>
  <tr style="height: 22px;">
   <td class="tg-fymr" style="height: 22px;" colspan="2">Sprint Planning Background</td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Date</td>
   <td class="tg-0pky" style="height: 22px;">2023-11-15</td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Time</td>
   <td class="tg-0pky" style="height: 22px;">10:00 AM</td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Location</td>
   <td class="tg-0pky" style="height: 22px;">Virtual meeting (Lima)</td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Prepared by</td>
   <td class="tg-0pky" style="height: 22px;">Angel Omar Meneses Torres</td>
  </tr>
  <tr style="height: 122px;">
   <td class="tg-0pky" style="height: 122px;">Attendees (to planning meeting)</td>
   <td class="tg-0pky" style="height: 122px;">Angel Meneses<br />Franco Vasquez<br />James Hurtado<br />Jherico Solier<br />Juben Cacha<br />Kolya Casta&ntilde;eda</td>
  </tr>
  <tr style="height: 42px;">
   <td class="tg-0pky" style="height: 42px;">Sprint 1 Review Summary</td>
   <td class="tg-0pky" style="height: 42px;">Previamente, logramos desarrollar por completo los siguientes productos:<br />- Landing Page<br />- Web Application: Fitster Inventory<br />- API: Fitster Backend<br />- Mobile Application: Fitster (80%)</td>
  </tr>
  <tr style="height: 42px;">
   <td class="tg-0pky" style="height: 42px;">Sprint 1 Retrospective Summary</td>
   <td class="tg-0pky" style="height: 42px;">
    <p>Los miembros del equipo est&aacute;n&nbsp;comprometidos con los objetivos del proyecto.</p>
    <p>Se lograron objetivos importantes, de tal forma que para este segundo y &uacute;ltimo <br />sprint, se enfocar&aacute;n los esfuerzos en consolidar la tecnolog&iacute;a emergente y&nbsp;<br />mejorar ciertos aspectos de las aplicaciones</p>
   </td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-fymr" style="height: 22px;" colspan="2">Sprint Goal &amp; User Stories</td>
  </tr>
  <tr style="height: 122px;">
   <td class="tg-0pky" style="height: 122px;">Sprint 2 Goal</td>
   <td class="tg-0pky" style="height: 122px;">
    <p>Implementar la tecnolog&iacute;a emergente: realidad virtual y realidad aumentada</p>
    <p>Mejorar las vistas ya existentes de las aplicaciones Fitster</p>
   </td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Sprint 2 Velocity</td>
   <td class="tg-0pky" style="height: 22px;">20</td>
  </tr>
  <tr style="height: 22px;">
   <td class="tg-0pky" style="height: 22px;">Sum of Story Points</td>
   <td class="tg-0pky" style="height: 22px;">8</td>
  </tr>
 </tbody>
</table>

#### Sprint Backlog 2

A continuación, visualizamos las historias de usuario a desarrollar en esta segunda iteración, así como su descomposición por tareas.

<table>
<thead>
  <tr>
    <th>Sprint #</th>
    <th colspan="7">Sprint 2</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan="2">User Story</td>
    <td colspan="6">Work-Item / Task</td>
  </tr>
  <tr>
    <td>Id</td>
    <td>Title</td>
    <td>Id</td>
    <td>Title</td>
    <td>Description</td>
    <td>Estimation (hours)</td>
    <td>Assigned to</td>
    <td>Status</td>
  </tr>
  <tr>
    <td rowspan="5">US01</td>
    <td rowspan="5">Realidad aumentada para observar productos</td>
    <td>TS26</td>
    <td>Investigación</td>
    <td>Investigar acerca de las principales herramientas para implementar AR en Flutter</td>
    <td>6</td>
    <td>Team</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>TS27</td>
    <td>Selección</td>
    <td>Seleccionar los plugins y bibliotecas a utilizar para integrar AR en nuestra aplicación</td>
    <td>2</td>
    <td>Team</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>TS28</td>
    <td>Búsqueda de modelos</td>
    <td>Buscar modelos de prendas 3D gratuitos en línea para validar la implementación</td>
    <td>4</td>
    <td>Team</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>TS29</td>
    <td>Implementación</td>
    <td>Implementar las funcionalidades para poder mostrar los modelos 3D en pantalla del móvil a través de la cámara</td>
    <td>8</td>
    <td>Team</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>TS30</td>
    <td>Pruebas</td>
    <td>Probar las funcionalidades y ajustar los errores encontrados para consolidar la implementación</td>
    <td>6</td>
    <td>Team</td>
    <td>Done</td>
  </tr>
</tbody>
</table>

#### Development Evidence for Sprint

En esta sección, evidenciamos los principales a manera de commits en los respectivos repositorios de desarrollo de nuestra solución. Evidentemente, todo el proceso completo de desarrollo puede visualizarse en los repositorios previamente referenciados.

![Vista de búsqueda de prendas](/assets/search-view.jpg)
![Vista del Shopping Cart](/assets/shopping-cart.jpg)
![Vista del realidad aumentada en el detalle de prenda](/assets/ar-1.jpg)
![Vista del realidad aumentada en en la cámara](/assets/ar-2.jpg)

<table>
<thead>
  <tr>
    <th>Repository</th>
    <th>Branch</th>
    <th>Commit id</th>
    <th>Commit message</th>
    <th>Commit body message</th>
    <th>Committed on</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>fitster_website</td>
    <td>feat/videos</td>
    <td>8dd0514</td>
    <td>feat</td>
    <td>added videos to its section</td>
    <td>20/11/2023</td>
  </tr>
  <tr>
    <td rowspan="3">fitster_app</td>
    <td rowspan="3">develop</td>
    <td>19fffe0</td>
    <td>feat</td>
    <td>add images for search view</td>
    <td>21/11/2023</td>
  </tr>
  <tr>
    <td>cad468d</td>
    <td>feat</td>
    <td>add function with ar camera</td>
    <td>21/11/2023</td>
  </tr>
  <tr>
    <td>734c474</td>
    <td>feat</td>
    <td>add shopping cart</td>
    <td>21/11/2023</td>
  </tr>
</tbody>
</table>

#### Execution Evidence for Sprint Review

#### Services Documentation Evidence for Sprint Review

A continuación, mostramos la documentación de servicios disponibles en nuestro API que soportan las funcionalidades en nuestra interfaz móvil como web. La documentación fue realizada con [Swagger](https://swagger.io/). Adjuntamos las presentes capturas en las que puede visualizarse todos los endpoints disponibles y las acciones CRUD realizables para cada entidad considerada en el alcance de nuestra solución.

![Primera captura de documentación con Swagger](/assets/services-1.png)
![Segunda captura de documentación con Swagger](/assets/services-2.png)
![Tercera captura de documentación con Swagger](/assets/services-3.png)
![Cuarta captura de documentación con Swagger](/assets/services-4.png)
![Quinta captura de documentación con Swagger](/assets/services-5.png)

Asimismo, en la parte inferior se pueden visualizar todos los esquemas para realizar solicitudes correctamente y recibir recursos.

![Captura de esquemas de recursos y requests](/assets/services-schemas.png)

Toda esta documentación de servicios está disponible y es interactiva para las pruebas desde [Swagger UI](https://fitsterupcapi.azurewebsites.net/swagger/index.html).

#### Software Deployment Evidence for Sprint Review

Nuestro Landing Page está desplegado utiizando [GitHub Pages](https://pages.github.com/), herramienta que permite desplegar proyectos directamente desde un repositorio de GitHub. Está disponible en el presente [enlace](https://emertechupc.github.io/fitster_website/).

Nuestra aplicación web Fitster Inventory está desplegada en [Vercel](https://emertechupc.github.io/fitster_website/). Disponible en el presente [enlace](https://frontend-example-flitster.vercel.app).

Nuestra aplicación móvil Fitster está desplegada localmente para el realizar las pruebas y validaciones necesarias.

Nuestra API Fitster Backend y base de datos está desplegadas en [Azure Web App Services](https://azure.microsoft.com/en-us/products/app-service/web) y [Azure SQL Database](https://azure.microsoft.com/es-es/products/azure-sql/database) respectivamente. El backend está disponible en el siguiente [enlace](https://fitsterupcapi.azurewebsites.net/swagger/index.html).  

#### Team Collaboration Insights during Sprint

Adjuntamos las evidencias de desarrollo y colaboración según las tareas asignadas y responsabilidad de cada miembro para implementar las aplicaciones.

![GitHub Insights para el Landing Page](/assets/insights-1-landing.png)
![GitHub Insights para Fitster Inventory](/assets/insights-1-web.png)
![GitHub Insights para Fitster Mobile App](/assets/insights-1-mobile.png)
![GitHub Insights para Fitster Backend](/assets/insights-1-backend.png)

### Evaluaciones según heurísticas

Evaluamos nuestra aplicación móvil según heurísticas de usabilidad y arquitectura de información, identificando los siguientes problemas:

| # | Problema                                                                                              | Escala de severidad | Heurística/Principio violado(a)                    |
|---|-------------------------------------------------------------------------------------------------------|---------------------|----------------------------------------------------|
| 1 | Sección de características de la prenda no muestra reseñas de usuarios                                | 3                   | Information Architecture - ¿Es controlable?        |
| 2 | Cambio de idioma                                                                                      | 2                   | Usabilidad - ¿Es fácil de usar y entender?         |
| 3 | Incluye una opción de colocar filtros personalizados, mas no barra de búsqueda                        | 3                   | Information Architecture - ¿Es fácil de encontrar? |
| 4 | Sección de características de la prenda no muestra prendas similares que podrían interesar al usuario | 2                   | Information Architecture - ¿Es fácil de encontrar? |

#### Descripción de problemas

**Sección de características de la prenda no muestra reseñas de usuarios**
*Severidad:* 3
*Heurística violada:* Information Architecture - ¿Es controlable?
*Problema:* La sección de características de las prendas en el probador virtual no muestra reseñas de usuarios, lo que dificulta a los usuarios obtener información adicional y opiniones sobre la prenda antes de tomar una decisión de compra.
*Recomendación:* Agregar una funcionalidad que permita a los usuarios ver y leer reseñas de otros usuarios sobre las prendas en la sección de características del probador virtual.

**Cambio de idioma**
*Severidad:* 2
*Heurística violada:* Usabilidad - ¿Es fácil de usar y entender?
*Problema:* El probador virtual de ropa no ofrece una opción clara y accesible para cambiar el idioma, lo que dificulta a los usuarios que no hablan el idioma predeterminado comprender y utilizar la aplicación de manera efectiva.
*Recomendación:* Agregar una funcionalidad para cambiar el idioma en el probador virtual, permitiendo a los usuarios seleccionar su idioma preferido de manera fácil y accesible.

**Incluye una opción de colocar filtros personalizados, mas no barra de búsqueda**
*Severidad:* 3
*Heurística violada:* Information Architecture - ¿Es fácil de encontrar?
*Problema:* El probador virtual incluye una barra de búsqueda para encontrar prendas específicas, pero no brinda la opción de colocar filtros personalizados, lo que limita la capacidad de los usuarios para refinar y encontrar rápidamente las prendas que se ajusten a sus preferencias y necesidades.
*Recomendación:* Agregar la opción de colocar filtros personalizados en el probador virtual, donde el usuario pueda definir precio, marca, color, entre otros. De esa manera, permitirá a los usuarios refinar su búsqueda y encontrar prendas de acuerdo a sus preferencias específicas.

**Sección de características de la prenda no muestra prendas similares que podrían interesar al usuario**
*Severidad:* 2
*Heurística violada:* Information Architecture - ¿Es fácil de encontrar?
*Problema:* En la sección de características de la prenda en el probador virtual, no se muestran prendas similares que podrían interesar al usuario, lo que limita su capacidad para descubrir y explorar más opciones relacionadas.
*Recomendación:* Agregar una sección de "Productos relacionados" en la sección de características de la prenda en el probador virtual, que muestre prendas similares o complementarias que podrían interesar al usuario.

## Video About-the-Product

Adjuntamos el video publicitario de nuestra aplicación móvil [Fitster subido a Youtube](https://youtu.be/vPKuGytEvik).

## Video About-the-Team

Adjuntamos el video publicitario de nuestra aplicación móvil [Team opinion subido a Youtube](https://youtu.be/XHj1OZKBQLQ).
