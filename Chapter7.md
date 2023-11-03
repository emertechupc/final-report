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

#### Development Evidence for Sprint Review

#### Testing Suite Evidence for Sprint Review

#### Execution Evidence for Sprint Review

#### Services Documentation Evidence for Sprint Review

#### Software Deployment Evidence for Sprint Review

#### Team Collaboration Insights during Sprint

## Validation Interviews

### Diseño de Entrevistas

### Registro de Entrevistas

### Evaluaciones según heurísticas

## Video About-the-Product
