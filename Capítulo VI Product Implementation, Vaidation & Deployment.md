

# Capítulo VI: Product Implementation, Vaidation & Deployment

## 6.1 Software Configuration Management
### 6.1.1 Software Development Environment Configuration

Utilizaremos principalmente como IDEs: Visual Studio Code o WebStorm, cada una con su configuración debida para no causar conflictos con carpetas personalizadas de cada IDE. Más adelante se hará uso de IntelliJ IDEA para la implementación de las Web APIs.

Como herramientas de desarrollo se hará uso de la última versión disponible de Node.js. Para el frontend, se usará el framework web Angular versión 13. El cual se instalará mediante nvm en su versión de Windows. Como framework de diseño se usará Angular Material UI. Finalmente, para el backend, se utilizará el lenguaje de programación de Java.

Como IDE de desarrollo para la aplicación móvil, se usará Visual Studio junto con un emulador y el SDK de Flutter más reciente, esto nos permite desarrollar con una amplia gamma de extensiones para facilitar la codificación y todas las opciones que brinda flutter en sus componentes.

Como herramientas SaSS, se usará GitHub como herramienta para colaboración de código. También usaremos Trello para la elaboración de los Product Backlog. Vertabelo, para la elaboración del diagrama de base de datos. Codegram, para la elaboración del diagrama de clases y LucidChart, para diagramas adicionales.

Como herramienta de desarrollo para el Embedded IOT Application se usará el simulador Wokwim, con el lenguaje de programación C++.

Para el desarrollo del landing page, se decidió con el equipo usar HTML, JS y CSS. Para llevarlo a cabo se eligieron diversas herramientas tecnológicas de las cuales el equipo ya está acostumbrado y tienen un cierto dominio. Estas herramientos son las siguientes:

Visual Studio Code: Es un editor de código gratuito, moderno y potente gracias a que cuenta con varias funciones y extensiones para trabajar con cualquier lenguaje de programación. Además es bastante conocida por todos los integrantes del equipo y debido a ello se decidió trabajar con Visual Studio Code. Para la instalación del programa, se puede conseguir desde su página web oficial: una vez descargado se puede proceder con la instalación de forma rápida y fácil.

Git y Github: Se usaron estas herramientas por la razón de que hoy en día es un estándar usar Git para el control de versiones de software y se eligió GitHub por ser la plataforma más popular y fácil de usar para crear y manejar repositorios, tener funciones para ver cambios, commits, pull request, entre otros. El enlace de descarga del instalador de GitHub Desktop es

Live Server: Finalmente, para acelerar el desarrollo del landing page, se usó esta extensión que sirve para visualizar los cambios inmediatamente después de alguna modificación en el código así se evita estar recargando la página, lo cual es un ahorro de tiempo y comodidad al desarrollar.

Discord: Aunque originalmente se diseñó como una plataforma de comunicación para gamers, Discord también se utiliza para diseñar y crear comunidades en línea y mejorar la experiencia de usuario a través de la comunicación y colaboración en grupos.

WhatsApp: WhatsApp es una aplicación de mensajería instantánea que se utiliza para la comunicación en tiempo real. Aunque no es una herramienta de gestión de proyectos, se puede usar para mantenerse en contacto con miembros del equipo y colaborar en cierta medida.

Zoom: Zoom es una plataforma de comunicación que ofrece videoconferencias y reuniones en línea. Aunque se utiliza principalmente para comunicarse y realizar reuniones virtuales, también puede ser útil para la gestión de proyectos remotos y la colaboración en tiempo real.

Requirements Management:

Miro: Miro es una plataforma de pizarra en línea que se utiliza para colaborar en la ideación, planificación y diseño de proyectos. Es especialmente útil para la colaboración visual, como la creación de mapas mentales, diagramas y prototipos.

Google Docs: Google Docs es una suite de aplicaciones de procesamiento de texto, hojas de cálculo y presentaciones en línea. Aunque no es específicamente una herramienta de gestión de requisitos, se puede utilizar para documentar y colaborar en la definición y seguimiento de requisitos de proyectos.

Product UX/UI Design:

Figma: Figma es una herramienta de diseño de interfaz de usuario (UI) y experiencia de usuario (UX) basada en la nube. Se utiliza para crear prototipos interactivos, diseños de aplicaciones y colaboración en tiempo real en proyectos de diseño.

UXPressia: UXPressia es una herramienta especializada en la creación de mapas de experiencia de usuario, perfiles de clientes y otros elementos relacionados con el diseño de UX. Ayuda a visualizar y comprender la experiencia del usuario en un producto o servicio.

LucidChart: es una herramienta para crear diagramas de clases, flujo y entre otros, de manera facil e intuitiva. Nos va a servir para hacer los user flows y el diagrama de clases para el proyecto.

Software Development:

Visual Studio Code: Visual Studio Code es un editor de código fuente altamente configurable y ampliable. Se utiliza principalmente para la codificación, depuración y desarrollo de software en varios lenguajes de programación.

Git: Git es un sistema de control de versiones distribuido. Aunque no es un programa en sí mismo, es una tecnología esencial para el desarrollo de software y se usa para rastrear cambios en el código fuente y facilitar la colaboración entre programadores.

Software Documentation:

GitHub: GitHub es una plataforma de desarrollo colaborativo que utiliza el sistema de control de versiones Git. Se utiliza para alojar, revisar y colaborar en proyectos de desarrollo de software, lo que facilita la colaboración entre desarrolladores.

Software Testing:

Lenguaje Gherkin: El lenguaje Gherkin es un lenguaje de dominio específico utilizado para escribir pruebas de aceptación en un formato legible por humanos. Se utiliza junto con herramientas de prueba de comportamiento, como Cucumber, para automatizar pruebas funcionales.

### 6.1.2 Source Code Management

Como mencionamos anteriormente, se utilizará GitHub para llevar un control de las versiones de desarrollo y poder trabajar de forma colaborativa. Para ello, se creó una organización llamada:

Repositorio de Landing Page: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Ayni_LandingPageOfficial

Repositorio de pruebas de aceptación:  https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/acceptance-test-IoT

Repositorio frontend: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniFrontend

Repositorio Edge API: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniEdgeAPI 

Repositorio Web API: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniBackend-API

Repositorio Mobile App: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/ayni_flutter_app

### 6.1.3 Source Code Style Guide & Conventions

A continuación, se darán a conocer las convenciones, formatos, estilos y entre otras propiedades de los lenguajes trabajados en la presente solución las cuales son: HTML, JavaScript/TypeScript, CSS:

HTML: Se hará uso de la guía “HTML Style Guide and Coding” de la página W3Schools, la cual menciona las convenciones y estándares de este lenguaje de etiquetas. Hemos considerado las siguientes como las más importantes:

Declarar siempre el tipo documento: Es decir, colocar siempre la etiqueta en la primera línea del código.

Utilizar el nombre de las etiquetas y sus atributos en minúscula: Por un tema de estética y orden del código para que este se vea más limpio y sea más fácil de escribir.

Cerrar todas las etiquetas: Esto evita futuros problemas o errores de sintaxis.

Siempre coloca comillas para los valores de los atributos de las etiquetas: De esta forma los valores son más fáciles de leer y se deben utilizar obligatoriamente si este contiene espacios.

Especificar siempre los atributos alt, width y height para las imágenes: Es importante en caso de que la imagen no se pueda mostrar por algún motivo y también ayuda con el tema de la accesibilidad de los usuarios.

No omitir la etiqueta ni los metadatos: Estas etiquetas son importantes para la optimización de motores de búsqueda (SEO).

CSS: Se siguió la guía “Google HTML/CSS Style Guide” donde se indican las convenciones, reglas y buenas prácticas para este lenguaje. Hemos considerado las siguientes recomendaciones como las más destacadas:

Nombre de clases: Se recomienda usar nombres generales para las clases, no deben ser específicas por la razón de que deben comportarse como padres.

Usar nombres de clase cortos: Se recomienda utilizar nombres de clase que sean cortos y descriptivos, para transmitir la idea de lo que representa de manera concisa.

Usar delimitadores de nombres de clase adecuados: Se debe de separar las palabras en los nombres de clase con solo guiones.

Evitar los selectores de ID: No se recomienda implementar este tipo de selectores, por la razón de que estos deben ser únicos en toda la página y en proyectos grandes que tengan muchos componentes es difícil de garantizar esa unicidad, es preferible usar selectores de clase.

Usar propiedades abreviadas: Es muy recomendable usar propiedades que soporten ser declarados de forma abreviada (por ejemplo, la propiedad padding, margin, border, etc.) por la razón de que reduce de forma significativa la cantidad de líneas de código, y es más legible para el programador o diseñador.

JavaScript: Se consideró importante seguir una guía de buenas prácticas para un mejor desarrollo del código, para este caso se eligió la guía de la wiki “JavaScript best practices“ del World Wide Web (W3C). Lo cual se destaca lo siguiente:

Usar nombres cortos y fáciles de leer: Es recomendable nombrar adecuadamente las variables, clases, funciones y otros elementos para que sea más sencillo de leer y comprender.

Evitar el uso de variables globales (keyword “var”): No se recomienda el uso de este tipo de variables en un proyecto, porque pueden generar muchos errores a medida que el proyecto crece y estas pueden sobrescribirse fácilmente afectando el valor y se pueden declarar otros elementos como funciones con el mismo nombre de la variable y generar errores.

Comentar y documentar lo necesario: Se recomienda comentar líneas de código que son complejos de entender a simple vista explicando o dejando mensajes para que otros programadores lo entiendan.

Usar notaciones sencillas de entender: Javascript cuenta con diversas notaciones y operadores para crear o modificar ciertas estructuras de datos como objetos, arrays, selectivas, etc.

Gherkin: Se consideró conveniente usar la guía y convenciones que se mencionan en “Gherkin Conventions for Readable Specifications” para una correcta realización de las pruebas. A continuación, se mencionan los puntos que consideramos más importantes para nuestro trabajo:

Los bloques “Give-When-Then” deben ser diferenciados: Se recomienda usar una correcta indentación de esos bloques para identificar mejor las secciones de la prueba y también añadiendo la keyword “And” para añadir otra línea en los pasos y otro bloque.

Usar tablas para los pasos: Si uno de los pasos requiere de más información es recomendable usar tablas para organizar dicha información y tenga un aspecto más ordenado.

Usar comillas simples para los parámetros: Se recomienda esta práctica para una mejor legibilidad de los parámetros en un paso y tener una sintaxis más simple.

Separar los escenarios con comentarios: Si se da el caso de tener muchos escenarios en una prueba, es usar los comentarios como separadores para que visualmente sea más organizado, fácil de leer y distinguir mejor.

En resumen, las convenciones o estilos de programación, se seguirá la guía de estilos de Google para programar en HTML (Google HTML), CSS (CSS Style Guide) y JavaScript (JS) en el caso de la landing page. En el caso de la implementación del frontend, se utilizará Angular Framework utilizando HTML5, CSS3 y JavaScript para aspectos estáticos de templates y TypeScript como lenguaje de programación.

Para el almacenamiento y control de versiones de código se utilizará GIT gestionado desde GitHub aplicando GitFlow Workflow, Conventional Commits y Semantic Versioning. Además, todos los hotfixes se realizan en ella, para así poder tener los arreglos desplegados de forma automática.

El lenguaje de diseño de Landing Page y Web Applications estará basado en Material Design. Como biblioteca de componentes de UI se utilizará Angular Material.

Para el desarrollo de Web Services, se realizará bajo RESTful API architectural style y se hará uso de Spring Boot Framework, utilizando Java como lenguaje de Programación.

Para el desarrollo de Mobile App, se hará uso de Flutter/Dart como lenguaje y se utilizará el mismo Web Service anteriormente mencionado.


### 6.1.4 Software Deployment Configuration


Para el despliegue de la web app y landing page se usó Netlify, a continuación se detallará paso a paso para este proceso

Ejecutamos el comando “ng build” en la ruta de nuestro projecto en angular, nos muestra lo siguiente:

![image](https://github.com/user-attachments/assets/04bc0a04-824c-472c-93e2-f28ee2533092)


Se genera la carpeta dist:

![image](https://github.com/user-attachments/assets/044c7e28-9ba6-418d-b38a-0b1f6d4f48b9)


Se añade el archivo “netlify.toml” para que netlify pueda entender las rutas de nuestro programa en angular con la siguiente configuración:

![image](https://github.com/user-attachments/assets/c709bea5-f479-493f-bb9b-dee374c80e7a)



Por último, vamos a netlify a la sección que nos permite desplegar nuestra aplicación manualmente para evitar errores:

![image](https://github.com/user-attachments/assets/e4ff6f55-ee48-4e0e-bbcd-ed09daf71694)


Y pasamos la carpeta que se encuentra dentro de la carpeta dist generada en nuestro proyecto. Y se obtiene el registro del despliegue dentro de Netlify

![image](https://github.com/user-attachments/assets/3a7f5aa8-86cc-4d3d-8f06-cc76a4f224c5)

---

Para el despliegue del backend y Edge API, se usó primero Railway, donde se creó un servicio para el hosting de la base de datos:

![imagen](https://github.com/user-attachments/assets/df245cf1-0ef2-4a4f-b122-cbb84dad8a6e)
![imagen](https://github.com/user-attachments/assets/c5ddeeff-788b-4642-b23c-c8b39ce726bc)

Link de base de datos: (https://railway.app/invite/vGyddg8tAkd)

Luego, se usó Zeaburn para el despliegue del backend, primero se crea un espacio de trabajo:

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/284024946-31a139f1-37cc-4f38-b28b-ab99cff2b1d0.png)

Posteriormente, se vincula con Github para realizar el deploy y este es el resultado:

![imagen](https://github.com/user-attachments/assets/7e1feb74-c6d7-4aa0-9154-b13b74870ecd)


Como se puede observar, cada vez que se haga un push a la rama master, se realiza un build nuevo para que se apliquen los cambios realizados en el proyecto.

Sin embargo, solo da 7 días de prueba para hacer deploys. Por lo tanto, se buscarán mejores alternativas

---

Para el despliegue de la aplicación móvil, se usara Firebase App Distribution, los pasos son los siguientes:

Se crea un proyecto en Firebase:

![imagen](https://github.com/user-attachments/assets/166c3724-fe14-4573-ae51-65b4221c9edf)

Se ejecuta la siguiente linea de codigo:

![imagen](https://github.com/user-attachments/assets/74c08eb8-9c3a-49cb-897c-276847db1533)

Luego se registra la app:

![imagen](https://github.com/user-attachments/assets/b47e96b6-ccf8-4044-8b3b-99052dd01781)

Se crea un grupo de testers:

![imagen](https://github.com/user-attachments/assets/bd9881ea-048c-4cbf-8818-e3abf4f07904)

Luego se realizan cambios en el main.dart:

![imagen](https://github.com/user-attachments/assets/cb3de7de-b00f-41b0-8c92-ac6fb9e1b357)

Y se obtiene la invitación.


## 6.2 Landing Page, Services & Applications Implementation

## 6.2.1 Sprint 1
### 6.2.1.1 Sprint Planning 1

| Sprint # | 1 | 
| - | - | 
| **Sprint Planning Background** | - |
| Date | 2024 - 09 - 10 |
| Time | 19:00 PM |
| Location | Virtual via Google Meet |
| Prepared By | Gonzales Carrión, Jorge Enrique |
| Attendees (to planning meeting) | Gonzales Carrión, Jorge Enrique / Espejo Macuri, Paolo Andre / Alejo Cardenas, Luis Angel / Rios Jaimes, Jhonel Enrique / Sebastian Tasayco, Javier Martin |
| Sprint 1 - Review Summary | No aplica (Es el primer Sprint) |
| Sprint 1 - Retrospective Summary  | No aplica (Es el primer Sprint) |
| **Sprint Goal & User Stories** | - |
| Sprint 1 Goal| Nuestro objetivo es brindar información pertinente en secciones acerca de la solución IoT en la landing page y visualizar, almacenar, planificar y mostrar cultivos en la aplicación web. <br> Creemos que esto genera una base sólida acerca de las funcionalidades de Ayni para los visitantes y permitir a los agricultores registrar y planificar sus cultivos. <br> Esto será confirmado cuando los visitantes se suscriban para acceder a las aplicaciones y los agricultores registren sus cultivos en la plataforma |
| Sprint 1 - Velocity | El equipo puede aceptar 28 Story Points|
| Sprint 1 - Story Points | La suma de los Story Points de los User Sotires que se atenderá es 18|



### 6.2.1.2 Sprint Backlog 1


El objetivo de este sprint es establecer una base sólida en la experiencia de usuario mediante el desarrollo de una landing page que brinde información clave sobre la aplicación y sus funcionalidades. Además, de desarrollar la primera versión de la aplicación web, donde se centrará en la visualización, monitoreo y planificación de cultivos.

Como herramienta de control para este Sprint se usó Trello con un board exclusivo para esta iteración:

![imagen](https://github.com/user-attachments/assets/dbeff7a3-afd4-4c97-9461-966e1dba4488)


Link: https://trello.com/invite/b/6711c7f10cf002d7fb8bb2da/ATTIc01f58e45484044f9c2e58d5fa2605b37DCEF44E/sprint-backlog-1-ayni



<table><tr><th valign="top">Sprint #</th><th colspan="7" valign="top">Sprint 1</th></tr>
<tr><td colspan="2" valign="top">User Story</td><td colspan="6" valign="top">Work-Item / Task</td></tr>
<tr><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Description</td><td valign="top">Estimation (Hours)</td><td valign="top">Assigned To</td><td valign="top"><p>Status </p><p>(To-do / </p><p>InProcess / </p><p>To Review / </p><p>Done)</p></td></tr>
<tr><td rowspan="2" valign="top">HU-11</td><td rowspan="2" valign="top">Sección Hero y Botón Call-to-Action</td><td valign="top">11.1</td><td valign="top">Implementar vistas con estilos</td><td valign="top">Realizar las secciones de hero y calltoaction</td><td valign="top">4</td><td valign="top">Jorge Gonzales</td><td valign="top">Done</td></tr>
<tr><td valign="top">11.2</td><td valign="top">Implementar sección responsive </td><td valign="top">Realizar las secciones con proporciones responsive</td><td valign="top">2</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>

<tr><td rowspan="1" valign="top">HU-12</td><td rowspan="1" valign="top">Landing Page responsive</td><td valign="top">12.1</td><td valign="top">Implementar vistas responsive</td><td valign="top">Realizar los estilos de las secciones responsive</td><td valign="top">4</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-13</td><td rowspan="1" valign="top">Sección de Funcionalidades y Planes</td><td valign="top">13.1</td><td valign="top">Implementar sección de funcionalidades y beneficios</td><td valign="top">Realizar la sección con los estilos e iconografía correspondiente</td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td rowspan="1" valign="top">HU-14</td><td rowspan="1" valign="top">Sección de Misión y Visión</td><td valign="top">14.1</td><td valign="top">Implementar sección de misión y visión de la landing page</td><td valign="top">Realizar la sección con los estilos e iconografía correspondiente</td><td valign="top">2</td><td valign="top">Javier Sebastian</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-16</td><td valign="top">Sección principal ("Home")</td><td valign="top">16.1</td><td valign="top">Implementar sección Home de la web app</td><td valign="top">Realizar los estilos de la sección Home para agricultores </td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-04</td><td valign="top">Ver detalles del terreno de cultivo y de las fases de cosecha de los cultivos</td><td valign="top">04.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web utilizando un JSON Placeholder</td><td valign="top">8</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-08</td><td valign="top">Planificar actividades agrícolas</td><td valign="top">08.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">4</td><td valign="top">Javier Sebastían</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-15</td><td valign="top">Sistemas de búsqueda y paginación</td><td valign="top">15.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">3</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-02</td><td valign="top">Inicio de sesión</td><td valign="top">02.1</td><td valign="top">Implementar vistas de inicio de sesión y planes en la web app</td><td valign="top">Implementar vistas y formularios de inicio de sesión (sin función)</td><td valign="top">3</td><td valign="top">Jorge gonzales</td><td valign="top">Done</td></tr>

</table>

### 6.2.1.3 Development Evidence for Sprint Review

Con respecto al alcance de desarrollo en este sprint, se logró realziar las secciones principales para landing page, tales como la sección Hero, especificación de funcionalidades y precios, acerca del equipo de desarrollo. Por otro lado, en la aplicación web se diseñó e implementó distintas secciones, tales como: Home, Crops, y la compra de productos mediante un stepper. Una de las pantallas a resaltar es el dashboard de monitoreo de cultivo. 

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| - | - | - | - | - | - |
| Ayni_LandingPageOfficial | feature/aboutus-section | 5832e79 | feat: update descriptions  | - | 25/09/2023 |
| Ayni_LandingPageOfficial  | feature/functionalities-section | c69748b | feat/added prices and functionalities  | - | 25/09/2023 |
| Ayni_LandingPageOfficial  | feature/hero-section | 457fd51 | feat: update descriptions  | - | 25/09/2023 |
| Ayni_LandingPageOfficial  | develop | 4524261 | fix: sections and cards  | - | 19/09/2023 |
| Ayni_LandingPageOfficial  | develop | 13c7bbe| Fix: update functionalities farmers  | - | 19/09/2023 |
| Ayni_LandingPageOfficial  | develop | 929a124 | feat: Hero section update  | - | 19/09/2023 |
| AyniFrontend  | feature/crop-detail | 4eb7589 | fix: signin and signup components  | - | 19/09/2023 |
| AyniFrontend  | feature/crop-detail | 13fa79a | fix: sales indentation  | - | 19/09/2023 |
| AyniFrontend  | feature/crop-detail | b79d6a8 | fix: rates component indentation | - | 19/09/2023 |
| AyniFrontend  | feature/crop-detail | 597a41e | feat: json server | - | 21/09/2023 |
| AyniFrontend  | feature/crop-detail | 02d5eab | feat: crop details component | - | 21/09/2023 |
| AyniFrontend  | feature/crop-detail | 9dd841f | feat: navigate to crop detail | - | 21/09/2023 |
| AyniFrontend  | feature/home-ui | 239aecd | fix: update fonts and cards | - | 23/09/2023 |
| AyniFrontend  | feature/plans-forms | 27abcdf | update: fix stepper for plans forms | - | 23/09/2023 |
| AyniFrontend  | feature/plans-forms | 40aacad | fix: update following steps to plan form | - | 23/09/2023 |
| AyniFrontend  | fix/code-style | c72eeb2 | fix: styles in bottom bar and rates | - | 23/09/2023 |

### 6.2.1.4 Testing Suite Evidence for Sprint Review


En esta sección, se realizaron acceptance test en .feature para cada una de las historias de usuario incluidas en este Sprint.
Las historias de usuario relacionadas a estos primeros .features son:
- HU-11	Sección Hero y Botón Call-to-Action
- HU-12	Landing Page responsive
- HU-13	Sección de Funcionalidades y Planes
- HU-14	Sección de Misión y Visión
- HU-16	Sección principal ("Home")
- HU-04	Realizar pedidos de productos
- HU-08	Planificar actividades agrícolas
- HU-15	Sistemas de búsqueda y paginación
- HU-02	Inicio de sesión

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| - | - | - | - | - | - |
| acceptance-test-IoT | test/UserStories | 70f7178 | Acceptance_test_09.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | e075329 | Acceptance_test_08.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | 7580071 | Acceptance_test_07.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | 792b52e | Acceptance_test_06.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | 3549d2d | Acceptance_test_05.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | dbf0ead | Acceptance_test_04.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | d9d7765 | Acceptance_test_03.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | 16df5ba | Acceptance_test_02.feature  | - | 25/09/2023 |
| acceptance-test-IoT | test/UserStories | 3fab5b6 | Acceptance_test_01.feature  | - | 25/09/2023 |


Link de repositorio: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/acceptance-test-IoT

### 6.2.1.5 Execution Evidence for Sprint Review

En el Sprint 1 se alcanzó a desarrollar una primera versión de las web apps y la landing page, como principales caracteristicas tenemos las vistas de Dashboard de monitoreo de cultivo, Home, PLanificación de cultivo, etc. A continuación se muestran imagenes de las vistas:

Principales vistas desarrolladas:
Landing page (sección Hero):
![image](https://github.com/user-attachments/assets/354bdd5e-7307-4f97-8aa6-c56a28fccbc1)

Landing page (sección de funcionalidades y precios):
![image](https://github.com/user-attachments/assets/5b46dd5a-8241-4fb7-beec-45af560f00ff)
![image](https://github.com/user-attachments/assets/8c0f4e25-9d4c-4bf6-bd19-c093622ac8f1)

Landing Page (sección about us)
![image](https://github.com/user-attachments/assets/bfcfcbba-f554-40b2-8298-fd7f95ba4518)


Home:
![image](https://github.com/user-attachments/assets/0447d09e-bcd3-457a-9bf8-95fae1b7ac06)

Dashboard de monitoreo de cultivo:
![image](https://github.com/user-attachments/assets/0c8e2c9a-d5ec-4ab2-98d2-f1dfa036fb80)

Vista de cultivos:
![image](https://github.com/user-attachments/assets/28ee32ec-d2b5-4e90-a6a1-5fbe6c847cfc)
![image](https://github.com/user-attachments/assets/8634a5c5-8e5e-4e1b-9913-fd05c75a1407)

Stepper de planificación de cultivo:
![image](https://github.com/user-attachments/assets/b70e9166-5753-4530-8117-914ace8233f5)

Formulario de añadir cultivo:
![image](https://github.com/user-attachments/assets/e332837b-715b-4ca9-9640-29ff73956a8f)

A continuación se muestra un video con todas las vistas mostradas:

![image](https://github.com/user-attachments/assets/b1f1202f-a32e-4984-a737-896f308d640a)

Link de video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202118468_upc_edu_pe/Eaahd6mxXbdNjQaZuE3PZrIB814G-5xhwWlgis9qpv1sWw?e=mH887A&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

### 6.2.1.6 Services Documentation Evidence for Sprint Review

Para este sprint 1, debido a que no existe la incorporación de los Web Services, se decidió usar JSON Placeholder como alternativa a consumir datos.

JSON Placeholder: https://my-json-server.typicode.com/JorgeGonzales15/ayni-jsonplaceholder-iot

| Endpoint | Detalles |
| - | - | 
| /users| En este endpoint se almacenan la información de los usuarios, tales como username, email, password, role, photo y token | 
| /products | En este endpoint se almacenan los productos que aun no son publicados a venta y tienen una planificación definida | 
| /orders  | En este endpoint se almacena las ordenes de los comerciantes, en el cual tienen un precio, que es ligado a un saleId, metodo de pago, descripción, etc. | 
| /crops  | En este endpoint almacena los cultivos creados por parte de los agricultores | 
| /rates  | En este endpoint se almacena las calificaciones y sus estados para cada orden | 
| /sales  | En este endpont se almacena los ventas de los comerciantes |

### 6.2.1.7 Software Deployment Evidence for Sprint Review


Para el despliegue de la web app y landing page se usó Netlify, a continuación se detallará paso a paso para este Sprint 1:

Ejecutamos el comando “ng build” en la ruta de nuestro projecto en angular, nos muestra lo siguiente:

![image](https://github.com/user-attachments/assets/04bc0a04-824c-472c-93e2-f28ee2533092)


Se genera la carpeta dist:

![image](https://github.com/user-attachments/assets/044c7e28-9ba6-418d-b38a-0b1f6d4f48b9)


Se añade el archivo “netlify.toml” para que netlify pueda entender las rutas de nuestro programa en angular con la siguiente configuración:

![image](https://github.com/user-attachments/assets/c709bea5-f479-493f-bb9b-dee374c80e7a)



Por último, vamos a netlify a la sección que nos permite desplegar nuestra aplicación manualmente para evitar errores:

![image](https://github.com/user-attachments/assets/e4ff6f55-ee48-4e0e-bbcd-ed09daf71694)


Y pasamos la carpeta que se encuentra dentro de la carpeta dist generada en nuestro proyecto. Y se obtiene el registro del despliegue dentro de Netlify

![image](https://github.com/user-attachments/assets/3a7f5aa8-86cc-4d3d-8f06-cc76a4f224c5)


De esta manera el avance del Sprint 1 queda desplegado.

Link de landing page: (https://ayni-landingpage-v1.netlify.app/)
Link de primera versión de frontend: (https://ayni-webapp-v1.netlify.app/)



### 6.2.1.8 Team Collaboration Insights during Sprint

En el presente sprint se implementó la landing page y una primera versión de la web application, a continuación se mostrará una tabal de las actividades de todos participantes:

| Alumno | Actividad | 
| - | - | 
| Espejo Macuri, Paolo Andre  | Desarrollo de frontend y landing page | 
| Gonzales Carrión, Jorge Enrique  | Desarrollo de frontend y landing page | 
| Alejo Cardenas, Luis Angel  |  Desarrollo de frontend y landing page | 
| Rios Jaimes, Jhonel Enrique |  Desarrollo de frontend y landing pageDesarrollo de frontend y backend | 
| Sebastian Tasayco, Javier Martin |  Desarrollo de frontend y landing page | 

Landing Page
![image](https://github.com/user-attachments/assets/d4c2f9fe-5efc-46e0-857d-052e97e8ca13)
![image](https://github.com/user-attachments/assets/8302ff21-28bd-4efb-bb04-271ab0c4591d)


Web App
![image](https://github.com/user-attachments/assets/fa251f6c-bb7c-4536-b578-f616b159f250)
![image](https://github.com/user-attachments/assets/8343536d-d3f4-47ce-aa48-6e2b82479e94)



## 6.2.2 Sprint 2
### 6.2.2.1 Sprint Planning 2

| Sprint # | 2 | 
| - | - | 
| **Sprint Planning Background** | - |
| Date | 2024 - 10 - 10 |
| Time | 19:00 PM |
| Location | Virtual via Google Meet |
| Prepared By | Gonzales Carrión, Jorge Enrique |
| Attendees (to planning meeting) | Gonzales Carrión, Jorge Enrique / Espejo Macuri, Paolo Andre / Alejo Cardenas, Luis Angel / Rios Jaimes, Jhonel Enrique / Sebastian Tasayco, Javier Martin |
| Sprint 1 - Review Summary | Se realizó la primera versión de landing page y web app, asimismo features de alta prioridad para los usuarios agricolas. |
| Sprint 1 - Retrospective Summary  | Se debe detallar la herramienta de control de gestión de proeyctos empleada en el Sprint 1 y mejorar explicaciones en las secciones Development, Testing, Execution, Documentation, Deployment |
| **Sprint Goal & User Stories** | - |
| Sprint 2 Goal| Nuestro enfoque está en permitir que los agricultores puedan registrar y planificar cultivos, además de monitorear sus cultivos utilizando datos de una aplicación embebida y en proporcionar a los comerciantes pantallas para la compra eficiente de cultivos en la aplicación móvil.<br> Creemos que esto ofrecerá una experiencia fluida de gestión de cultivos para los agricultores, brindando herramientas detalladas de planificación y monitoreo, mientras que los comerciantes podrán navegar y realizar compras de cultivos de manera sencilla dentro del sistema. <br> Esto se confirmará cuando los agricultores puedan monitorear sus cultivos a través de la aplicación embebida, y los comerciantes puedan acceder y completar la compra de cultivos mediante las pantallas implementadas, utilizando los endpoints en Ayni. |
| Sprint 2 - Velocity | El equipo puede aceptar 80 Story Points|
| Sprint 2 - Story Points | La suma de los Story Points de los User Sotires que se atenderá es 72|



### 6.2.2.2 Sprint Backlog 2

El objetivo de este Sprint es permitir que los agricultores puedan registrar y planificar cultivos, además de monitorear sus cultivos utilizando datos de una aplicación embebida y en proporcionar a los comerciantes pantallas para la compra eficiente de cultivos en la aplicación móvil.

Creemos que esto ofrecerá una experiencia fluida de gestión de cultivos para los agricultores, brindando herramientas detalladas de planificación y monitoreo, mientras que los comerciantes podrán navegar y realizar compras de cultivos de manera sencilla dentro del sistema.

Esto se confirmará cuando los agricultores puedan monitorear sus cultivos a través de la aplicación embebida, y los comerciantes puedan acceder y completar la compra de cultivos mediante las pantallas implementadas, utilizando los endpoints en Ayni.

Como herramienta de control para este Sprint se usó Trello con un board exclusivo para esta iteración:

![imagen](https://github.com/user-attachments/assets/cc649612-1584-46a8-a2ec-8a0e1111f52d)




Link: https://trello.com/invite/b/6711cea372164d45ac966845/ATTIfc89256cc30d96794e9f205a7629c5f382930C0C/sprint-backlog-2-ayni



<table><tr><th valign="top">Sprint #</th><th colspan="7" valign="top">Sprint 2</th></tr>
<tr><td colspan="2" valign="top">User Story</td><td colspan="6" valign="top">Work-Item / Task</td></tr>
<tr><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Description</td><td valign="top">Estimation (Hours)</td><td valign="top">Assigned To</td><td valign="top"><p>Status </p><p>(To-do / </p><p>InProcess / </p><p>To Review / </p><p>Done)</p></td></tr>
<tr><td rowspan="1" valign="top">HU-10</td><td rowspan="1" valign="top">Atender pedidos</td><td valign="top">10.1</td><td valign="top">Desarrollar las páginas de compra/venta para comerciantes en la app web</td><td valign="top">Realizar las vistas de ventas para comerciantes utulizando componenets de Angular Material</td><td valign="top">4</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-16</td><td rowspan="1" valign="top">Sección principal ("Home")</td><td valign="top">16.1</td><td valign="top">Desarrollar la página "Home" para los comerciante</td><td valign="top">Desarrollar las paginas con los estilos en Angular Material</td><td valign="top">4</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-05</td><td rowspan="1" valign="top"> 	Realizar pedidos de productos</td><td valign="top">5.1</td><td valign="top">Desarrollar la pagina de obtención de cultivos para los comerciantes en la app web</td><td valign="top">Realizar la pagina correspondiente mediante un stepper usando Angular Material</td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td rowspan="1" valign="top">HU-08</td><td rowspan="1" valign="top">Sección de Misión y Visión</td><td valign="top">08.2</td><td valign="top">Desarrollar paginas de planificación y lista de cultivos en la aplicación móvil</td><td valign="top">Realizar las secciones en Flutter para la aplicación móvil</td><td valign="top">2</td><td valign="top">Jorge Gonzales</td><td valign="top">Done</td></tr>

<tr><td valign="top">TS-02</td><td valign="top">Creación y obtención de cultivos</td><td valign="top">TS02.1</td><td valign="top">Desarrollar endpoints de creación y obtención de cultivos</td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">TS-03</td><td valign="top"> Desarrollar endpoints de creación y obtención de productos</td><td valign="top">TS03.1</td><td valign="top">Desarrollar endpoints de creación y obtención de productos</td><td valign="top">Implementar endpoints relacionados a los productos y su relación con las ordenes</td><td valign="top">8</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-08</td><td valign="top">Planificar actividades agrícolas</td><td valign="top">08.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">4</td><td valign="top">Javier Sebastían</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-15</td><td valign="top">Sistemas de búsqueda y paginación</td><td valign="top">15.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">3</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-02</td><td valign="top">Inicio de sesión</td><td valign="top">02.1</td><td valign="top">Implementar vistas de inicio de sesión y planes en la web app</td><td valign="top">Implementar vistas y formularios de inicio de sesión (sin función)</td><td valign="top">3</td><td valign="top">Jorge gonzales</td><td valign="top">Done</td></tr>

</table>

### 6.2.2.3 Development Evidence for Sprint Review


Con respecto al alcance del desarrollo de este Sprint, se desarrolló la primera versión de la aplicación móvil, abarcando la intefaz del agricultor y sus principales funcioanlidades como las secciones de Home, Crops y Orders. Por otro lado, tambien se realizó al primera versión de la aplicación embebida IoT, obteniendo como resultado el funcionamiento de los sensores y actuadores a utilziar en la solución IoT. Finalmente, se implementaron los principales endpoints en el API Restful Web, relacionados a la creación y obtencion de cultivos, productos y ordenes.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| - | - | - | - | - | - |
| ayni_flutter_app | feat/crops_and_products | f5a33a5 | feat: added dashboards crops and profiles  | - | 28/10/2024 |
| ayni_flutter_app | feat/crops_monitoring | f1f8c63f | feat: update functionalities about the project | - | 25/10/2024 |
| ayni_flutter_app | feat/orders_and_sales | 733bc1b | feat: added orders and sales service | - | 25/10/2024 |
| AyniBackend-API | develop | e12ce74 | feat: added orders and sales service | - | 23/10/2024 |
| AyniBackend-API | develop | 7e576cc | feat: Created Sensor Repository | - | 23/10/2024 |
| AyniBackend-API | develop | 0a9b31b | feat: Created Sensor Service and Controller | - | 23/10/2024 |
| AyniBackend-API | develop | dd0d38b | feat: Created Actuator Aggregate | - | 23/10/2024 |
| AyniBackend-API | develop | 6518a12 | feat: Created Actuator Services and Repository | - | 23/10/2024 |
| AyniBackend-API | develop | ad7fb89 | feat: Created Actuator Controller | - | 23/10/2024 |
| AyniBackend-API | develop | 002b6d1| feat: Updated Sensor model | - | 02/10/2024 |
| AyniBackend-API | develop | fd36f1b | feat: Updated Crop model | - | 02/10/2024 |
| AyniBackend-API | develop | 4e20aad | fix: Fixed bugs | - | 02/10/2024 |
| AyniWokwi | develop | 06b8c3e | feat: added wokwi sketch | - | 25/10/2024 |
| AyniWokwi | develop | e75542a | feat: Added connection with Edge API | - | 02/10/2024 |
| Ayni_LandingPage_Official | main | 177fd55 | feat: added about the team and product | - | 01/10/2024 |
| AyniEdgeApi | master | cdfd4825 | chore: Initial commit | - | 02/10/2024 |
| AyniEdgeApi | master | 1617ed1 | feat: Added AppConfig | - | 02/10/2024 |
| AyniEdgeApi | master | e364baa |feat: Updated database | - | 02/10/2024 |
| AyniEdgeApi | master | 09451aa |eat: Added connection with backend | - | 02/10/2024 |
| AyniFrontend | main | 845efdf |feat: sales integration | - | 01/10/2024 |
| AyniFrontend | main | f372353 |feat: sale detail integration | - | 01/10/2024 |
| AyniFrontend | main | 795e613 |feat: orders integration | - | 01/10/2024 |
| AyniFrontend | main | 479f191 |feat: order detail integration | - | 01/10/2024 |
| AyniFrontend | main | 43d5190 |feat: request form integration | - | 01/10/2024 |
| AyniFrontend | main | 1ca0b40 |feat: merchant user integration | - | 01/10/2024 |
| AyniFrontend | main | 2842d35 |feat: farmer user integration | - | 01/10/2024 |
| AyniFrontend | main | 3b9bf5f |feat: farmer products integration | - | 01/10/2024 |
| AyniFrontend | main | e000ab6 |feat: order integration | - | 01/10/2024 |
| AyniFrontend | main | 45d6067 |feat: crop detail integration | - | 01/10/2024 |


### 6.2.2.4 Testing Suite Evidence for Sprint Review

En esta sección, se realizaron acceptance test en .feature para cada una de las historias de usuario incluidas en este Sprint.
Las historias de usuario relacionadas a estos primeros .features son:
- HU-10 Atender pedidos
- HU-05 Realizar pedidos de productos
- TS-02 Creación y obtención de cultivos
- HU-16	Sección principal ("Home")
- TS-03 Obtención y creación para productos agrícolas
- HU-08	Planificar actividades agrícolas
- HU-15 Sistemas de búsqueda y paginación
- HU-02 Inicio de sesión


| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| - | - | - | - | - | - |
| acceptance-test-IoT | test/UserStories | 5084640 | Acceptance_test_10.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | fb40fde | Acceptance_test_11.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | 48b72cc | Acceptance_test_12.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | d604b83 | Acceptance_test_13.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | dc02648 | Acceptance_test_14.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | 64597a6 | Acceptance_test_15.feature  | - | 31/10/2024 |
| acceptance-test-IoT | test/UserStories | 50f709c | Acceptance_test_16.feature  | - | 31/10/2024 |

Link de repositorio: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/acceptance-test-IoT

### 6.2.2.5 Execution Evidence for Sprint Review

En el Sprint 2 se alcanzó a desarrollar una primera versión del Web Service (API RESTful) y la aplicación móvil, como principales caracteristicas tenemos las vistas de Dashboard de monitoreo de cultivo, Home, PLanificación de cultivo, etc. A continuación se muestran imagenes de las vistas:

Principales vistas desarrolladas y otros productos:

Mobile App:

![imagen](https://github.com/user-attachments/assets/e482bc49-f295-449e-b472-2e99e8b2b6bb)

![imagen](https://github.com/user-attachments/assets/45142eca-7ac2-48eb-a4a0-f0e8fd7c1669)

![imagen](https://github.com/user-attachments/assets/6f0a2eaa-b861-4b7d-abd5-1804bd78a272)

![imagen](https://github.com/user-attachments/assets/d9f84ab7-fb64-45fb-804f-de4788d32583)

![imagen](https://github.com/user-attachments/assets/6cd7281a-9c80-4929-8713-512b57651435)

![imagen](https://github.com/user-attachments/assets/5ed24371-a20b-471c-a599-f43b0897c639)

![imagen](https://github.com/user-attachments/assets/517f97b1-70dd-4904-b82e-26c1c11d8735)

Web App:

![imagen](https://github.com/user-attachments/assets/e308ebbf-2bf2-432d-85a0-4e2e52c862c1)

![imagen](https://github.com/user-attachments/assets/91a56652-7086-45c2-a763-aab46a07aba3)

![imagen](https://github.com/user-attachments/assets/1c81807f-65c4-4724-86d7-dd45ab1cd2da)

![imagen](https://github.com/user-attachments/assets/23999c06-2322-417b-80fc-be5f0e53f4b2)

![imagen](https://github.com/user-attachments/assets/e1c322b4-ec86-444e-9443-2fae0360b07d)

Embedded App Iot:

![imagen](https://github.com/user-attachments/assets/3deeb138-44fc-4740-b990-0827f5dac862)


A continuación se muestra un video con todas las vistas, endpoints y simulaciones:

![imagen](https://github.com/user-attachments/assets/c0955189-792a-4568-80a4-331868ec83a6)


Link: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202118468_upc_edu_pe/ERew7zrbe-BPoUqTItiUFJoBq7t4_XrFh_nPxtTgLq_Q5Q?e=LVeLc4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

### 6.2.2.6 Services Documentation Evidence for Sprint Review

En esta sección, se documentará los endpoints de Web Services, en este sprint se logró abarcar los endpoints más importantes para la aplicación. Sin embargo, todavía queda adicionar más metodos de regla de negocio. Con respecto a la documentación, se usó OpenApi para documentar la interacción de los usuarios con los controllers  El link del repositorio de WebServices: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniBackend-API) y EdgeAPI: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniEdgeAPI)


Web Api:

| Acciones | Endpoint | Detalles | Enlace | Datos de muestra |
| - | - | - | - | - |
| POST | /api/auth/signin | En este endpoint se puede iniciar sesión | http://localhost:8080/swagger-ui/index.html#/Authentication/authenticateUser | username: "Juan" <br> "password: contrasenia" |
| POST | /api/auth/signup | En este endpoint se puede crear el usuario  | http://localhost:8080/swagger-ui/index.html#/Authentication/registerUser | username: "Juan" <br> email: "Juan@gmail.com" <br> "role: farmer" <br> "password: contrasenia" |
| POST | api/v1/products  | En este endpoint se puede utilizar para registrar un producto | http://localhost:8080/swagger-ui/index.html#/Products/createProduct | "name": "Zanahoria","description": "Rica zanahora","recommendedCultivationDistance": "12","recommendedCultivationDepth": "2","recommendedGrowingClimate": "Templado","recommendedSoilType": "Arenoso","recommendedGrowingSeason": "Otoño","imageUrl": "imagen","userId": 1 |
| GET | api/v1/products  | En este endpoint se puede utilizar para obtener todos los productos | http://localhost:8080/swagger-ui/index.html#/Products/getAllProducts | - |
| GET | api/v1/products/{productId}  | En este endpoint se puede utilizar para obtener todos un producto por Id | http://localhost:8080/swagger-ui/index.html#/Products/getProductById | productId: 1 |
| GET | api/v1/products/{productId}/crops | En este endpoint se puede utilizar para obtener todos los cultivos del producto | http://localhost:8080/swagger-ui/index.html#/Products/getAllCropsByProductId | productId: 1 |
| GET | api/v1/products/{productId}/crops/{cropId} | En este endpoint se puede utilizar para obtener un cultivo en especifico de un producto en especifico | http://localhost:8080/swagger-ui/index.html#/Products/getCropByProductIdAndCropId | productId: 1, cropId: 1 |
| POST | api/v1/crops  | En este endpoint se puede utilizar para registrar un cultivo | http://localhost:8080/swagger-ui/index.html#/Crops/createCrop | "name": "Papa","pickUpWeed": true,"fertilizeCrop": true,"oxygenateCrop": false,"makeCropLine": true,"makeCropHole": true,"wateringDays": 12,"pestCleanupDays": 3,"productId": 1,"userId": 1 |
| GET | api/v1/crops  | En este endpoint se puede utilizar para obtener todos los cultivo | http://localhost:8080/swagger-ui/index.html#/Crops/getAllCrops | - |
| GET | api/v1/crops/{cropId}  | En este endpoint se puede utilizar para un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Crops/getCropById | cropId: 1 |
| POST | api/v1/orders  | En este endpoint se puede utilizar para registrar una orden | http://localhost:8080/swagger-ui/index.html#/Orders/createOrder |   "description": "Papayas muy buenas", "totalPrice": 15, "quantity": 3, "paymentMethod": "mastercard", "status": "On Package", "saleId": 1, "orderedBy": 1, "acceptedBy": 2, "orderedDate": "2023-11-02T13:16:02.798Z" |
| POST | api/v1/orders/{orderId}/qualifications  | En este endpoint se puede utilizar para cambiar el estado de una orden | http://localhost:8080/swagger-ui/index.html#/Orders/qualifyOrder | orderId: 1 |
| POST | api/v1/orders/{orderId}/finalizations | En este endpoint se puede utilizar para cambiar el estado de una orden | http://localhost:8080/swagger-ui/index.html#/Orders/finalizeOrder | orderId: 1 |
| GET | api/v1/orders  | En este endpoint se puede utilizar para obtener todas las ordenes | http://localhost:8080/swagger-ui/index.html#/Orders/getAllOrders | - |
| GET | api/v1/orders/{orderId}  | En este endpoint se puede utilizar para obtener una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/getOrderById | orderId: 1 |
| PUT | api/v1/orders{orderId}  | En este endpoint se puede actualizar una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/updateOrder | orderId: 1 |
| DELETE | api/v1/orders/{orderId}  | En este endpoint se puede eliminar una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/deleteOrder | orderId: 1 |
| POST | api/v1/sales  | En este endpoint se puede utilizar para registrar una venta | http://localhost:8080/swagger-ui/index.html#/Sales/createSale |   "name": "Venta de camote", "description": "buena venta", "unitPrice": 24, "quantity": 2, "imageUrl": "https://www.gob.mx/cms/uploads/article/main_image/20333/camote1.jpg" |
| GET | api/v1/sales  | En este endpoint se puede utilizar para obtener todas las ventas | http://localhost:8080/swagger-ui/index.html#/Sales/getAllSales | - |
| GET | api/v1/sales/{salesId}  | En este endpoint se puede utilizar para obtener una venta por Id | http://localhost:8080/swagger-ui/index.html#/Sales/getSaleById | saleId: 1 |
| GET | api/v1/sales/{salesId}/orders/{orderId}  | En este endpoint se puede utilizar para obtener una venta por Id en especifico vinculado a una orden por Id en especifico | http://localhost:8080/swagger-ui/index.html#/Sales/getOrderBySaleIdAndOrderId | saleId: 1, orderId: 1 |
| POST | api/v1/rates  | En este endpoint se puede utilizar para crear una calificación de un producto | http://localhost:8080/swagger-ui/index.html#/Rates/createRate | "rate": 5, "date": "25-09-2023","productId": 1, "userId": 1 |
| GET | api/v1/rates  | En este endpoint se puede utilizar para obtener todas las calificaciones | http://localhost:8080/swagger-ui/index.html#/Rates/getAllRates | - |
| GET | api/v1/rates/{ratesId}  | En este endpoint se puede utilizar para obtener una calificación por Id | http://localhost:8080/swagger-ui/index.html#/Rates/getRateById | rateId: 1 |
| GET | /api/v1/sensors/{sensorId} | Este endpoint se usa para obtener información de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getSensorById | sensorId: 1 |
| PUT | /api/v1/sensors/{sensorId} | Este endpoint se usa para actualizar un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/updateSensor | sensorId: 1 |
| DELETE | /api/v1/sensors/{sensorId} | Este endpoint se usa para eliminar un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/deleteSensor | sensorId: 1 |
| POST | /api/v1/sensors | Este endpoint se usa para registrar un nuevo sensor | http://localhost:8080/swagger-ui/index.html#/Sensors/createSensor | "type": "temperature", "location": "Warehouse" |
| GET | /api/sensors/{sensorId}/actuators | Este endpoint se usa para obtener todos los actuadores de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getAllActuatorsBySensorId | sensorId: 1 |
| GET | /api/sensors/{sensorId}/actuators/{actuatorId} | Este endpoint se usa para obtener un actuador específico de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getActuatorBySensorIdAndActuatorId | sensorId: 1, actuatorId: 1 |
| GET | /api/v1/actuators/{actuatorId} | Este endpoint se usa para obtener información de un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/getActuatorById | actuatorId: 1 |
| PUT | /api/v1/actuators/{actuatorId} | Este endpoint se usa para actualizar un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/updateActuator | actuatorId: 1 |
| DELETE | /api/v1/actuators/{actuatorId} | Este endpoint se usa para eliminar un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/deleteActuator | actuatorId: 1 |
| POST | /api/v1/actuators | Este endpoint se usa para registrar un nuevo actuador | http://localhost:8080/swagger-ui/index.html#/Actuators/createActuator | "type": "valve", "status": "off", "sensorId": 1 |

Edge Api:
| Acciones | Endpoint | Detalles | Enlace | Datos de muestra |
| - | - | - | - | - |
| POST | /api/v1/limitations | En este endpoint se puede utilizar para registrar las limitaciones de un cultivo | http://localhost:8080/swagger-ui/index.html#/Limitations/createLimitation | "cropId": 0, "recommendedTemperature": 0, "recommendedHumidity": 0, "recommendedOxygen": 0, "recommendedWaterlevel": 0 |
| GET | /api/v1/limitations/{id} | En este endpoint se puede utilizar para obtener las limitaciones de un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Limitations/getLimitationById | id: 0 |
| GET | /api/v1/limitations/{cropId} | En este endpoint se puede utilizar para obtener las limitaciones de un cultivo específico | http://localhost:8080/swagger-ui/index.html#/Limitations/getLimitationByCropId | cropId: 0 |
| POST | /api/v1/status | En este endpoint se puede utilizar para registrar el estado actual de un cultivo | http://localhost:8080/swagger-ui/index.html#/Status/createStatus | "cropId": 0, "temperature": 0, "humidity": 0, "oxygen": 0, "waterLevel": 0 |
| GET | /api/v1/status/{id} | En este endpoint se puede utilizar para obtener el estado de un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Status/getStatusById | id: 0 |




A continuación se mostrarán capturas de la documentación usando OpenAPI:

Backend: 
![imagen](https://github.com/user-attachments/assets/8e864981-59b5-463a-85ed-8c5a9ea7e0e1)
![imagen](https://github.com/user-attachments/assets/bac07886-c344-4f84-84a6-a19355ecdfce)
![imagen](https://github.com/user-attachments/assets/8b0198a3-51ae-450d-9212-4061cf699cf1)

Edge API:
![imagen](https://github.com/user-attachments/assets/022e8779-5131-4234-b706-50e271ed1f75)


### 6.2.2.7 Software Deployment Evidence for Sprint Review


Para el despliegue de la web app y landing page se usó Netlify, a continuación se detallará paso a paso para este Sprint 1:

Ejecutamos el comando “ng build” en la ruta de nuestro projecto en angular, nos muestra lo siguiente:

![image](https://github.com/user-attachments/assets/04bc0a04-824c-472c-93e2-f28ee2533092)


Se genera la carpeta dist:

![image](https://github.com/user-attachments/assets/044c7e28-9ba6-418d-b38a-0b1f6d4f48b9)


Se añade el archivo “netlify.toml” para que netlify pueda entender las rutas de nuestro programa en angular con la siguiente configuración:

![image](https://github.com/user-attachments/assets/c709bea5-f479-493f-bb9b-dee374c80e7a)



Por último, vamos a netlify a la sección que nos permite desplegar nuestra aplicación manualmente para evitar errores:

![image](https://github.com/user-attachments/assets/e4ff6f55-ee48-4e0e-bbcd-ed09daf71694)


Y pasamos la carpeta que se encuentra dentro de la carpeta dist generada en nuestro proyecto. Y se obtiene el registro del despliegue dentro de Netlify

![image](https://github.com/user-attachments/assets/3a7f5aa8-86cc-4d3d-8f06-cc76a4f224c5)


De esta manera el avance del Sprint 2 queda desplegado.

Link de landing page: (https://ayni-landingpage-v1.netlify.app/)
Link de primera versión de frontend: (https://ayni-webapp-v1.netlify.app/)

---

Para el despliegue del backend y Edge API, se usó primero Railway, donde se creó un servicio para el hosting de la base de datos:

![imagen](https://github.com/user-attachments/assets/df245cf1-0ef2-4a4f-b122-cbb84dad8a6e)
![imagen](https://github.com/user-attachments/assets/c5ddeeff-788b-4642-b23c-c8b39ce726bc)

Link de base de datos: (https://railway.app/invite/vGyddg8tAkd)

Luego, se usó Zeaburn para el despliegue del backend, primero se crea un espacio de trabajo:

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/284024946-31a139f1-37cc-4f38-b28b-ab99cff2b1d0.png)

Posteriormente, se vincula con Github para realizar el deploy y este es el resultado:

![imagen](https://github.com/user-attachments/assets/7e1feb74-c6d7-4aa0-9154-b13b74870ecd)


Como se puede observar, cada vez que se haga un push a la rama master, se realiza un build nuevo para que se apliquen los cambios realizados en el proyecto.

Sin embargo, solo da 7 días de prueba para hacer deploys. Por lo tanto, se buscarán mejores alternativas

El link es el siguiente: (https://ayni-v1.sfo1.zeabur.app/swagger-ui/index.html)
Edge API: (https://ayni-edge.sfo1.zeabur.app/swagger-ui/index.html)


---

Para el despliegue de la aplicación móvil, se usó Firebase App Distribution, se siguieron los siguientes pasos:

Se crea un proyecto en Firebase:

![imagen](https://github.com/user-attachments/assets/166c3724-fe14-4573-ae51-65b4221c9edf)

Se ejecuta la siguiente linea de codigo:

![imagen](https://github.com/user-attachments/assets/74c08eb8-9c3a-49cb-897c-276847db1533)

Luego se registra la app:

![imagen](https://github.com/user-attachments/assets/b47e96b6-ccf8-4044-8b3b-99052dd01781)

Se crea un grupo de testers:

![imagen](https://github.com/user-attachments/assets/bd9881ea-048c-4cbf-8818-e3abf4f07904)

Luego se realizan cambios en el main.dart:

![imagen](https://github.com/user-attachments/assets/cb3de7de-b00f-41b0-8c92-ac6fb9e1b357)

Y se obtiene la invitación: 

Link: https://appdistribution.firebase.dev/i/4eb4946b644720bd

### 6.2.2.8 Team Collaboration Insights during Sprint

En este Sprint se realizó la primera versión del backend, mobile application y Embedded Application IoT

| Alumno | Actividad | 
| - | - | 
| Espejo Macuri, Paolo Andre  | Desarrollo de backend, mobile app, embedded app IoT, Edge API, Embedded app Iot | 
| Gonzales Carrión, Jorge Enrique  | Desarrollo de backend, mobile app, Landing Page, Embedded app Iot y Edge API | 
| Alejo Cardenas, Luis Angel  |  Desarrollo de backend, mobile app, Embedded app Iot y Edge API| 
| Rios Jaimes, Jhonel Enrique |  Desarrollo de backend, mobile app, Frontend, Embedded app Iot y Edge API| 
| Sebastian Tasayco, Javier Martin |  Desarrollo de backend, mobile app, embedded app IoT y Edge API | 


Mobile App
![imagen](https://github.com/user-attachments/assets/b3813063-7905-4e87-87f4-59419c442651)


Backend
![imagen](https://github.com/user-attachments/assets/0545b25d-c6cc-4f8e-8bf9-ab485d4d399a)


Edge API:
![imagen](https://github.com/user-attachments/assets/62d4a5c8-9ebf-45fe-901f-f0cc8e2972a4)


IoT Embedded App:
![imagen](https://github.com/user-attachments/assets/561ab524-f4b6-436d-b855-7aedd8f8ede4)


Landing Page:
![imagen](https://github.com/user-attachments/assets/5d39b885-ae87-4aea-bff5-e24677212333)


Frontend:
![imagen](https://github.com/user-attachments/assets/d2c43f9f-7ce0-4bbf-bd4b-2000ec4646d1)

## 6.2.3 Sprint 3
### 6.2.3.1 Sprint Planning 3

| Sprint # | 3 | 
| - | - | 
| **Sprint Planning Background** | - |
| Date | 2024 - 10 - 10 |
| Time | 19:00 PM |
| Location | Virtual via Google Meet |
| Prepared By | Gonzales Carrión, Jorge Enrique |
| Attendees (to planning meeting) | Gonzales Carrión, Jorge Enrique / Espejo Macuri, Paolo Andre / Alejo Cardenas, Luis Angel / Rios Jaimes, Jhonel Enrique / Sebastian Tasayco, Javier Martin |
| Sprint 2 - Review Summary | Se realizó la primera versión de landing page y web app, asimismo features de alta prioridad para los usuarios agricolas. |
| Sprint 2 - Retrospective Summary  | Se debe detallar la herramienta de control de gestión de proeyctos empleada en el Sprint 1 y mejorar explicaciones en las secciones Development, Testing, Execution, Documentation, Deployment |
| **Sprint Goal & User Stories** | - |
| Sprint 3 Goal| Nuestro enfoque está en permitir que los agricultores puedan registrar y planificar cultivos, además de monitorear sus cultivos utilizando datos de una aplicación embebida y en proporcionar a los comerciantes pantallas para la compra eficiente de cultivos en la aplicación móvil.<br> Creemos que esto ofrecerá una experiencia fluida de gestión de cultivos para los agricultores, brindando herramientas detalladas de planificación y monitoreo, mientras que los comerciantes podrán navegar y realizar compras de cultivos de manera sencilla dentro del sistema. <br> Esto se confirmará cuando los agricultores puedan monitorear sus cultivos a través de la aplicación embebida, y los comerciantes puedan acceder y completar la compra de cultivos mediante las pantallas implementadas, utilizando los endpoints en Ayni. |
| Sprint 3 - Velocity | El equipo puede aceptar 80 Story Points|
| Sprint 3 - Story Points | La suma de los Story Points de los User Sotires que se atenderá es 72|



### 6.2.3.2 Sprint Backlog 3

El objetivo de este Sprint es permitir que los agricultores puedan registrar y planificar cultivos, además de monitorear sus cultivos utilizando datos de una aplicación embebida y en proporcionar a los comerciantes pantallas para la compra eficiente de cultivos en la aplicación móvil.

Creemos que esto ofrecerá una experiencia fluida de gestión de cultivos para los agricultores, brindando herramientas detalladas de planificación y monitoreo, mientras que los comerciantes podrán navegar y realizar compras de cultivos de manera sencilla dentro del sistema.

Esto se confirmará cuando los agricultores puedan monitorear sus cultivos a través de la aplicación embebida, y los comerciantes puedan acceder y completar la compra de cultivos mediante las pantallas implementadas, utilizando los endpoints en Ayni.

Como herramienta de control para este Sprint se usó Trello con un board exclusivo para esta iteración:






Link: 



<table><tr><th valign="top">Sprint #</th><th colspan="7" valign="top">Sprint 3</th></tr>
<tr><td colspan="2" valign="top">User Story</td><td colspan="6" valign="top">Work-Item / Task</td></tr>
<tr><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Description</td><td valign="top">Estimation (Hours)</td><td valign="top">Assigned To</td><td valign="top"><p>Status </p><p>(To-do / </p><p>InProcess / </p><p>To Review / </p><p>Done)</p></td></tr>
<tr><td rowspan="1" valign="top">HU-10</td><td rowspan="1" valign="top">Atender pedidos</td><td valign="top">10.1</td><td valign="top">Desarrollar las páginas de compra/venta para comerciantes en la app web</td><td valign="top">Realizar las vistas de ventas para comerciantes utulizando componenets de Angular Material</td><td valign="top">4</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-16</td><td rowspan="1" valign="top">Sección principal ("Home")</td><td valign="top">16.1</td><td valign="top">Desarrollar la página "Home" para los comerciante</td><td valign="top">Desarrollar las paginas con los estilos en Angular Material</td><td valign="top">4</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-05</td><td rowspan="1" valign="top"> 	Realizar pedidos de productos</td><td valign="top">5.1</td><td valign="top">Desarrollar la pagina de obtención de cultivos para los comerciantes en la app web</td><td valign="top">Realizar la pagina correspondiente mediante un stepper usando Angular Material</td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td rowspan="1" valign="top">HU-08</td><td rowspan="1" valign="top">Sección de Misión y Visión</td><td valign="top">08.2</td><td valign="top">Desarrollar paginas de planificación y lista de cultivos en la aplicación móvil</td><td valign="top">Realizar las secciones en Flutter para la aplicación móvil</td><td valign="top">2</td><td valign="top">Jorge Gonzales</td><td valign="top">Done</td></tr>

<tr><td valign="top">TS-02</td><td valign="top">Creación y obtención de cultivos</td><td valign="top">TS02.1</td><td valign="top">Desarrollar endpoints de creación y obtención de cultivos</td><td valign="top">2</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">TS-03</td><td valign="top"> Desarrollar endpoints de creación y obtención de productos</td><td valign="top">TS03.1</td><td valign="top">Desarrollar endpoints de creación y obtención de productos</td><td valign="top">Implementar endpoints relacionados a los productos y su relación con las ordenes</td><td valign="top">8</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-08</td><td valign="top">Planificar actividades agrícolas</td><td valign="top">08.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">4</td><td valign="top">Javier Sebastían</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-15</td><td valign="top">Sistemas de búsqueda y paginación</td><td valign="top">15.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">3</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-02</td><td valign="top">Inicio de sesión</td><td valign="top">02.1</td><td valign="top">Implementar vistas de inicio de sesión y planes en la web app</td><td valign="top">Implementar vistas y formularios de inicio de sesión (sin función)</td><td valign="top">3</td><td valign="top">Jorge gonzales</td><td valign="top">Done</td></tr>

</table>

### 6.2.3.3 Development Evidence for Sprint Review


Con respecto al alcance del desarrollo de este Sprint, se desarrolló la primera versión de la aplicación móvil, abarcando la intefaz del agricultor y sus principales funcioanlidades como las secciones de Home, Crops y Orders. Por otro lado, tambien se realizó al primera versión de la aplicación embebida IoT, obteniendo como resultado el funcionamiento de los sensores y actuadores a utilziar en la solución IoT. Finalmente, se implementaron los principales endpoints en el API Restful Web, relacionados a la creación y obtencion de cultivos, productos y ordenes.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| - | - | - | - | - | - |
| AyniFrontend | feat/dashboard | 9b3d252 | feat: dashbaord  | - | 17/11/2024 |
| AyniFrontend | feat: membership page | 9318580| feat: membership page  | - | 17/11/2024 |
| AyniFrontend | feat: membership page | b7e1b06 | feat: addedd components to fix getUser  | - | 18/11/2024 |
| AyniFrontend | feat: membership page | 9b5141c | fix: delete transatcions | - | 18/11/2024 |
| ayni_flutter_app | feat/dashboards_by_crops | 1374ef6 | feat: Sensor and SensorService  | - | 16/11/2024 |
| ayni_flutter_app | feat/dashboards_by_crops | b77e558 | fix: clean crop dashboard details screen  | - | 18/11/2024 |
| ayni_flutter_app | feat/dashboards_by_crops | 597f3c0 | feat: added and edit profile service | - | 18/11/2024 |
| ayni_flutter_app | feat/dashboards_by_crops | adfe6b7 | feat: fix sensor service  | - | 18/11/2024 |
| ayni_flutter_app | feat/dashboards_by_crops | 06c3a45 | feat: update main screen  | - | 18/11/2024 |
| ayni_flutter_app | main | f050609 | Create main.yml  | - | 01/11/2024 |
| ayni_flutter_app | main | dcda3e0 | Update main.yml  | - | 01/11/2024 |
| ayni_flutter_app | main | 236133e | fix: fixed bugs  | - | 01/11/2024 |
| AyniEdgeAPI  | master | 24344ae | update database  | - | 14/11/2024 |
| AyniEdgeAPI  | master | 61521a3 | fix: Fixed update  | - | 14/11/2024 |
| AyniEdgeAPI  | master | 1d5f071 | fix: Fixed update | - | 14/11/2024 |
| AyniEdgeAPI  | master | d7e9a9a | fix: Fixed get bugs | - | 15/11/2024 |
| AyniEdgeAPI  | master | 818d1db | update database | - | 14/11/2024 |
| AyniWokwi  | master | e75542a | feat: Added connection with Edge API | - | 02/11/2024 |
| AyniWokwi  | master | f1d1caa | feat: Updated structure | - | 15/11/2024 |
| AyniWokwi  | master | c8a6cec | feat: Split code using headers | - | 15/11/2024 |

### 6.2.3.4 Testing Suite Evidence for Sprint Review

En esta sección, se realizaron acceptance test en .feature para cada una de las historias de usuario incluidas en este Sprint.
Las historias de usuario relacionadas a estos primeros .features son:

Historias de usuario:
- HU09
- HU13
- HU14
- HU17
- TS10
- TS01
- TS09
- 
- 

| Repository            | Branch           | Commit Id | Commit Message           | Commit Message Body | Commited on (Date) |
|-----------------------|------------------|-----------|--------------------------|----------------------|--------------------|
| acceptance-test-IoT  | test/UserStories | d394ed    | Acceptance_test_17.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 543a74    | Acceptance_test_18.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | b59dab    | Acceptance_test_19.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 48a76e    | Acceptance_test_20.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 91164e    | Acceptance_test_21.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 9d7d7d    | Acceptance_test_22.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 366016    | Acceptance_test_23.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 6ac9a8    | Acceptance_test_24.feature | -                    | 16/11/2024        |
| acceptance-test-IoT  | test/UserStories | 5beed2    | Acceptance_test_25.feature | -                    | 16/11/2024        |
| AyniBackend-API | main | ecd2c89324e228939982f13c241b0876b95cddbd | test: added test to qualifated sale  | - | 18/11/2024 |
| AyniBackend-API | main | 851d556cf71935e659f4d52efc1463690028c6c9 | test: add test about finalizated product | - | 18/11/2024 |


Testing en Frontend:
A continuación se muestran pruebas realizadas en el frontend usando TestBed, proporcionado por el mismo Framework de Angular
![imagen](https://github.com/user-attachments/assets/efdc7ad0-2c87-43bf-95c3-447d815cb493)
![imagen](https://github.com/user-attachments/assets/fe2114e7-a481-4c6b-919a-397122b54a8e)

Finalmente, se hicieron pruebas automatizadas con Selenium:
![imagen](https://github.com/user-attachments/assets/b50567c8-ae44-49ab-8f7b-08f005fd1c34)


Testing Backend y Edge API:
A continuación, se muestran pruebas unitarias realizadas con J-Unit para el backend:

Esta prueba valida una orden existente y si es calificada:
![imagen](https://github.com/user-attachments/assets/3fc42917-d4a5-44e6-8f43-6c2b25dd5241)

Esta prueba valida una venta existente y si es finalizada:
![imagen](https://github.com/user-attachments/assets/618d886a-0e18-4d67-b565-ae09ef56f8f4)


Link de repositorio: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/acceptance-test-IoT

### 6.2.3.5 Execution Evidence for Sprint Review

En el Sprint 3 se alcanzó a desarrollar la ultima versión del Web Service (API RESTful) y la aplicación móvil, como principales caracteristicas tenemos las vistas de Dashboard de monitoreo de cultivo y su total funcionaldiad con los datos proporcionados por la aplicación embebida.

Principales vistas desarrolladas y otros productos:

Mobile App:
Pantalla de dashboard de información de sensores:
![imagen](https://github.com/user-attachments/assets/36bc49da-6dcf-4055-bc94-4bba808b0db5)


Web App:

Pantalla de membresias:
![imagen](https://github.com/user-attachments/assets/3e679fe0-31ad-495a-972f-57f1e17b6356)

Pantalla de login:
![imagen](https://github.com/user-attachments/assets/34591a37-be92-4bb3-96c0-68f8210ec1f3)

Dashbaord de cultivo:
![imagen](https://github.com/user-attachments/assets/e79a8f1d-a3bc-44d3-9b48-ec8678934b26)

Embedded App Iot:

![imagen](https://github.com/user-attachments/assets/f1bffc07-ab4a-4094-870f-ee119eb8b860)



A continuación se muestra un video con todas las vistas, endpoints y simulaciones:

![imagen](https://github.com/user-attachments/assets/1f80f0af-69fc-4664-ac3e-98a0d205e483)


Link: https://goo.su/8ddlB

### 6.2.3.6 Services Documentation Evidence for Sprint Review

En esta sección, se documentará los endpoints de Web Services, en este sprint se logró abarcar los endpoints más importantes para la aplicación. Sin embargo, todavía queda adicionar más metodos de regla de negocio. Con respecto a la documentación, se usó OpenApi para documentar la interacción de los usuarios con los controllers  El link del repositorio de WebServices: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniBackend-API) y EdgeAPI: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniEdgeAPI)


Web Api:

| Acciones | Endpoint | Detalles | Enlace | Datos de muestra |
| - | - | - | - | - |
| POST | /api/auth/signin | En este endpoint se puede iniciar sesión | http://localhost:8080/swagger-ui/index.html#/Authentication/authenticateUser | username: "Juan" <br> "password: contrasenia" |
| POST | /api/auth/signup | En este endpoint se puede crear el usuario  | http://localhost:8080/swagger-ui/index.html#/Authentication/registerUser | username: "Juan" <br> email: "Juan@gmail.com" <br> "role: farmer" <br> "password: contrasenia" |
| POST | api/v1/products  | En este endpoint se puede utilizar para registrar un producto | http://localhost:8080/swagger-ui/index.html#/Products/createProduct | "name": "Zanahoria","description": "Rica zanahora","recommendedCultivationDistance": "12","recommendedCultivationDepth": "2","recommendedGrowingClimate": "Templado","recommendedSoilType": "Arenoso","recommendedGrowingSeason": "Otoño","imageUrl": "imagen","userId": 1 |
| GET | api/v1/products  | En este endpoint se puede utilizar para obtener todos los productos | http://localhost:8080/swagger-ui/index.html#/Products/getAllProducts | - |
| GET | api/v1/products/{productId}  | En este endpoint se puede utilizar para obtener todos un producto por Id | http://localhost:8080/swagger-ui/index.html#/Products/getProductById | productId: 1 |
| GET | api/v1/products/{productId}/crops | En este endpoint se puede utilizar para obtener todos los cultivos del producto | http://localhost:8080/swagger-ui/index.html#/Products/getAllCropsByProductId | productId: 1 |
| GET | api/v1/products/{productId}/crops/{cropId} | En este endpoint se puede utilizar para obtener un cultivo en especifico de un producto en especifico | http://localhost:8080/swagger-ui/index.html#/Products/getCropByProductIdAndCropId | productId: 1, cropId: 1 |
| POST | api/v1/crops  | En este endpoint se puede utilizar para registrar un cultivo | http://localhost:8080/swagger-ui/index.html#/Crops/createCrop | "name": "Papa","pickUpWeed": true,"fertilizeCrop": true,"oxygenateCrop": false,"makeCropLine": true,"makeCropHole": true,"wateringDays": 12,"pestCleanupDays": 3,"productId": 1,"userId": 1 |
| GET | api/v1/crops  | En este endpoint se puede utilizar para obtener todos los cultivo | http://localhost:8080/swagger-ui/index.html#/Crops/getAllCrops | - |
| GET | api/v1/crops/{cropId}  | En este endpoint se puede utilizar para un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Crops/getCropById | cropId: 1 |
| POST | api/v1/orders  | En este endpoint se puede utilizar para registrar una orden | http://localhost:8080/swagger-ui/index.html#/Orders/createOrder |   "description": "Papayas muy buenas", "totalPrice": 15, "quantity": 3, "paymentMethod": "mastercard", "status": "On Package", "saleId": 1, "orderedBy": 1, "acceptedBy": 2, "orderedDate": "2023-11-02T13:16:02.798Z" |
| POST | api/v1/orders/{orderId}/qualifications  | En este endpoint se puede utilizar para cambiar el estado de una orden | http://localhost:8080/swagger-ui/index.html#/Orders/qualifyOrder | orderId: 1 |
| POST | api/v1/orders/{orderId}/finalizations | En este endpoint se puede utilizar para cambiar el estado de una orden | http://localhost:8080/swagger-ui/index.html#/Orders/finalizeOrder | orderId: 1 |
| GET | api/v1/orders  | En este endpoint se puede utilizar para obtener todas las ordenes | http://localhost:8080/swagger-ui/index.html#/Orders/getAllOrders | - |
| GET | api/v1/orders/{orderId}  | En este endpoint se puede utilizar para obtener una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/getOrderById | orderId: 1 |
| PUT | api/v1/orders{orderId}  | En este endpoint se puede actualizar una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/updateOrder | orderId: 1 |
| DELETE | api/v1/orders/{orderId}  | En este endpoint se puede eliminar una orden por Id | http://localhost:8080/swagger-ui/index.html#/Orders/deleteOrder | orderId: 1 |
| POST | api/v1/sales  | En este endpoint se puede utilizar para registrar una venta | http://localhost:8080/swagger-ui/index.html#/Sales/createSale |   "name": "Venta de camote", "description": "buena venta", "unitPrice": 24, "quantity": 2, "imageUrl": "https://www.gob.mx/cms/uploads/article/main_image/20333/camote1.jpg" |
| GET | api/v1/sales  | En este endpoint se puede utilizar para obtener todas las ventas | http://localhost:8080/swagger-ui/index.html#/Sales/getAllSales | - |
| GET | api/v1/sales/{salesId}  | En este endpoint se puede utilizar para obtener una venta por Id | http://localhost:8080/swagger-ui/index.html#/Sales/getSaleById | saleId: 1 |
| GET | api/v1/sales/{salesId}/orders/{orderId}  | En este endpoint se puede utilizar para obtener una venta por Id en especifico vinculado a una orden por Id en especifico | http://localhost:8080/swagger-ui/index.html#/Sales/getOrderBySaleIdAndOrderId | saleId: 1, orderId: 1 |
| POST | api/v1/rates  | En este endpoint se puede utilizar para crear una calificación de un producto | http://localhost:8080/swagger-ui/index.html#/Rates/createRate | "rate": 5, "date": "25-09-2023","productId": 1, "userId": 1 |
| GET | api/v1/rates  | En este endpoint se puede utilizar para obtener todas las calificaciones | http://localhost:8080/swagger-ui/index.html#/Rates/getAllRates | - |
| GET | api/v1/rates/{ratesId}  | En este endpoint se puede utilizar para obtener una calificación por Id | http://localhost:8080/swagger-ui/index.html#/Rates/getRateById | rateId: 1 |
| GET | /api/v1/sensors/{sensorId} | Este endpoint se usa para obtener información de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getSensorById | sensorId: 1 |
| PUT | /api/v1/sensors/{sensorId} | Este endpoint se usa para actualizar un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/updateSensor | sensorId: 1 |
| DELETE | /api/v1/sensors/{sensorId} | Este endpoint se usa para eliminar un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/deleteSensor | sensorId: 1 |
| POST | /api/v1/sensors | Este endpoint se usa para registrar un nuevo sensor | http://localhost:8080/swagger-ui/index.html#/Sensors/createSensor | "type": "temperature", "location": "Warehouse" |
| GET | /api/sensors/{sensorId}/actuators | Este endpoint se usa para obtener todos los actuadores de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getAllActuatorsBySensorId | sensorId: 1 |
| GET | /api/sensors/{sensorId}/actuators/{actuatorId} | Este endpoint se usa para obtener un actuador específico de un sensor específico | http://localhost:8080/swagger-ui/index.html#/Sensors/getActuatorBySensorIdAndActuatorId | sensorId: 1, actuatorId: 1 |
| GET | /api/v1/actuators/{actuatorId} | Este endpoint se usa para obtener información de un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/getActuatorById | actuatorId: 1 |
| PUT | /api/v1/actuators/{actuatorId} | Este endpoint se usa para actualizar un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/updateActuator | actuatorId: 1 |
| DELETE | /api/v1/actuators/{actuatorId} | Este endpoint se usa para eliminar un actuador específico | http://localhost:8080/swagger-ui/index.html#/Actuators/deleteActuator | actuatorId: 1 |
| POST | /api/v1/actuators | Este endpoint se usa para registrar un nuevo actuador | http://localhost:8080/swagger-ui/index.html#/Actuators/createActuator | "type": "valve", "status": "off", "sensorId": 1 |

Edge Api:
| Acciones | Endpoint | Detalles | Enlace | Datos de muestra |
| - | - | - | - | - |
| POST | /api/v1/limitations | En este endpoint se puede utilizar para registrar las limitaciones de un cultivo | http://localhost:8080/swagger-ui/index.html#/Limitations/createLimitation | "cropId": 0, "recommendedTemperature": 0, "recommendedHumidity": 0, "recommendedOxygen": 0, "recommendedWaterlevel": 0 |
| GET | /api/v1/limitations/{id} | En este endpoint se puede utilizar para obtener las limitaciones de un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Limitations/getLimitationById | id: 0 |
| GET | /api/v1/limitations/{cropId} | En este endpoint se puede utilizar para obtener las limitaciones de un cultivo específico | http://localhost:8080/swagger-ui/index.html#/Limitations/getLimitationByCropId | cropId: 0 |
| POST | /api/v1/status | En este endpoint se puede utilizar para registrar el estado actual de un cultivo | http://localhost:8080/swagger-ui/index.html#/Status/createStatus | "cropId": 0, "temperature": 0, "humidity": 0, "oxygen": 0, "waterLevel": 0 |
| GET | /api/v1/status/{id} | En este endpoint se puede utilizar para obtener el estado de un cultivo por Id | http://localhost:8080/swagger-ui/index.html#/Status/getStatusById | id: 0 |




A continuación se mostrarán capturas de la documentación usando OpenAPI:

Backend: 
![imagen](https://github.com/user-attachments/assets/8e864981-59b5-463a-85ed-8c5a9ea7e0e1)
![imagen](https://github.com/user-attachments/assets/bac07886-c344-4f84-84a6-a19355ecdfce)
![imagen](https://github.com/user-attachments/assets/8b0198a3-51ae-450d-9212-4061cf699cf1)

Edge API:
![imagen](https://github.com/user-attachments/assets/022e8779-5131-4234-b706-50e271ed1f75)


### 6.2.3.7 Software Deployment Evidence for Sprint Review


A continuación se muestra evidencia del despliege realizado en Netlify mediante los logs proporcionados por la herramienta:

Despliegue de Landing Page:


Despliegue de Web App:
![imagen](https://github.com/user-attachments/assets/d191d3de-13ec-4b64-91cc-6805fcf09651)


Link de landing page: (https://ayni-landingpage-v1.netlify.app/)
Link de primera versión de frontend: (https://ayni-webapp-v1.netlify.app/)

---

A continuación se muestra evidencia del despliege realizado en Zeabur mediante los logs proporcionados por la herramienta:

Despliegue de Edge API:
![imagen](https://github.com/user-attachments/assets/60dcdf1f-e1e7-459a-bad6-c5738ddc2e8e)

Despliegue de Web API:
![imagen](https://github.com/user-attachments/assets/ab1c99be-a6d1-42ca-a35a-f5a4d082f8c0)


El link es el siguiente: (https://ayni-v1.sfo1.zeabur.app/swagger-ui/index.html)
Edge API: (https://ayni-edge.sfo1.zeabur.app/swagger-ui/index.html)


---

A continuación se muestra evidencia del despliege realizado en Firebase App Distribution mediante los logs proporcionados por la herramienta:

Despliegue de app móvil:

![imagen](https://github.com/user-attachments/assets/3bb42c1b-8b0f-4c4f-b477-04bdd70f9714)

Link: https://appdistribution.firebase.google.com/testerapps/1:21261281534:android:1a093cbd3cf02aebbb1daf/releases/4m43ppte0edlg?utm_source=firebase-console

### 6.2.3.8 Team Collaboration Insights during Sprint

En este Sprint se realizó la primera versión del backend, mobile application y Embedded Application IoT

| Alumno | Actividad | 
| - | - | 
| Espejo Macuri, Paolo Andre  | Desarrollo de backend, mobile app, embedded app IoT, Edge API, Embedded app Iot | 
| Gonzales Carrión, Jorge Enrique  | Desarrollo de backend, mobile app, Landing Page, Embedded app Iot y Edge API | 
| Alejo Cardenas, Luis Angel  |  Desarrollo de backend, mobile app, Embedded app Iot y Edge API| 
| Rios Jaimes, Jhonel Enrique |  Desarrollo de backend, mobile app, Frontend, Embedded app Iot y Edge API| 
| Sebastian Tasayco, Javier Martin |  Desarrollo de backend, mobile app, embedded app IoT y Edge API | 


Mobile App
![imagen](https://github.com/user-attachments/assets/fd35b979-2f47-4300-a1b9-085a62560570)



Backend
![imagen](https://github.com/user-attachments/assets/cabee589-88ed-4ec2-aa69-e90389ecf4f8)



Edge API:
![imagen](https://github.com/user-attachments/assets/6dac96dc-b040-491c-be4f-d69cd1fa95f1)



IoT Embedded App:
![imagen](https://github.com/user-attachments/assets/1da41b01-2bd3-4ff6-91f7-15740d098121)



Landing Page:



Frontend:
![imagen](https://github.com/user-attachments/assets/c65e0171-6f23-41e5-a575-1695022d4aa1)



# 6.3 Validation Interviews

En esta sección, se registra las actividades correspondientes a las entrevistas de validación del proyecto. Estas entrevistas van dirigidas a ambos segmentos objetivos donde se evidencia la interacción con el landing page y con las aplicaciones.

## 6.3.1 Diseño de Entrevistas

**Segmento Objetivo: Productores que quieren mejorar la calidad de sus ventas**
- **Presentación del entrevistado**
  - ¿Cuál es tu nombre?
  - ¿Qué edad tienes?
  - ¿Hace cuánto se dedica a la agricultura?
- **Explicación de los alcances de la demostración**
  - Landing Page
  - Principales tareas en la aplicación móvil y web
- **Navegación a través de la aplicación web**
  
  **User Flow: Añadir cultivo y plan de cultivo**
  - El usuario ingresa a landing page
  - Busca el botón call to action
  - Se redirige a la sección de registro de usuarios y llena los campos solicitados
  - Selecciona su rol 
  - Se redirige a la sección de Home
  - Ingresa a la sección "Mis Productos"
  - Añade un cultivo
  - Crea un plan de cultivo
  - Ingresa los campos solicitados en el formulario
 
- **Preguntas principales**
  - ¿Consideras atractiva la manera en la que el producto Ayni está promocionado en la Landing Page?
  - ¿Consideras que el landing page ofrece toda la información necesaria para tener un entendimiento adecuado del funcionamento, propósito y funcionalidades ofrecidas por la apliación?
  - ¿Resulta agradable a la vista la manera en la que la información está presentada?
  - ¿Qué dispositivo utilizaste para acceder al Landing Page? ¿La página presenta  algún tipo de inconveniente de diseño que impida navegar de manera fluida?
  - Del 1 al 10 ¿Cómo calificarías el diseño de la Landing Page?
  - Con respecto a la aplicación, ¿considera que es complicado añadir un cultivo?
  - ¿Los cultivos que son añadidos contienen lo que necesitas saber sobre ellas para su correcto sembrío? ¿Qué otros apartados le gustaría visualizar?
  - ¿Qué opina acerca de la distribución de secciones?
  - ¿Cómo describiría nuestra aplicación web en pocas palabras?
  - ¿Qué características específicas desea usted que agreguemos a la aplicación web?
  - ¿Utiliza actualmente una aplicación web para administrar sus sembríos u obtener información sobre sus plantas? De ser así, ¿Qué características logra diferenciar entra esa aplicación y la nuestra?
  - ¿De todas las características evidenciadas en la aplicación web, cuál cree que debería mejorarse? ¿Por qué?
  - ¿Considera que el diseño es adecuado?



**Segmento Objetivo: Comerciantes que quieren mejorar la calidad de sus ventas**
- **Presentación del entrevistado**
  - ¿Cuál es tu nombre?
  - ¿Qué edad tienes?
  - ¿Hace cuánto se dedica a la venta de productos agrícolas?
- **Explicación de los alcances de la demostración**
  - Landing Page
  - Prinipales tareas en la aplicación móvil y web
- **Navegación a través de la aplicación web**
  
  **User Flow: Comprar un producto**
  - El usuario ingresa a landing page
  - Busca el botón call to action
  - Se redirige a la sección de registro de usuarios y llena los campos solicitados
  - Selecciona su rol 
  - Se redirige a la sección de Home
  - Ingresa a la sección "Buscar productos"
  - Selecciona un cultivo
  - Hace click en el botón "Comprar"
  - Ingresa los campos solicitados en el stepper
  - Confirma la compra
- **Preguntas principales**
  - ¿Consideras atractiva la manera en la que el producto Ayni está promocionado en la Landing Page?
  - ¿Consideras que el landing page ofrece toda la información necesaria para tener un entendimiento adecuado del funcionamento, propósito y funcionalidades ofrecidas por la apliación?
  - ¿Resulta agradable a la vista la manera en la que la información está presentada?
  - ¿Qué dispositivo utilizaste para acceder al Landing Page? ¿La página presenta  algún tipo de inconveniente de diseño que impida navegar de manera fluida?
  - Del 1 al 10 ¿Cómo calificarías el diseño de la Landing Page?
  - Con respecto a la aplicación, ¿considera que es complicado encontrar un cultivo?
  - ¿Los cultivos que son mostrados contienen lo que necesitas saber sobre ellas para incentivar su compra? ¿Qué otros apartados le gustaría visualizar?
  - ¿Qué opina acerca de la distribución de secciones?
  - ¿Cómo describiría nuestra aplicación web en pocas palabras?
  - ¿Qué características específicas desea usted que agreguemos a la aplicación web?
  - ¿Utiliza actualmente una aplicación web para administrar sus ventas u obtener información sobre los productos agrícolas? De ser así, ¿Qué características logra diferenciar entra esa aplicación y la nuestra?
  - ¿De todas las características evidenciadas en la aplicación web, cuál cree que debería mejorarse? ¿Por qué?
  - ¿Considera que el diseño es adecuado?

## 6.3.2 Registro de Entrevistas

**Segmento Objetivo: Productores que quieren mejorar la calidad de sus ventas**

Nombre y apellidos: Lissane Mareni

Edad: 19

Distrito: San Juan de Miraflores - Lima

Link: https://goo.su/Cvsf6

Inicio: 0:00

Fin: 11:00

Duración: 11:30


![imagen](https://github.com/user-attachments/assets/b656c4cb-8227-4597-9574-7d2812898b96)

Lissane nos brindó su sincera opinión acerca de la última versión de la aplicación móvil, aplicación web y la landing page. Con respecto a la landing page, destacó el diseño atractivo y eficiente de las secciones, así como el orden de estas. Sin embargo, considera que se debería dar mayor relevancia a las funcionalidades mostradas, incluyendo capturas de pantalla de la aplicación web y móvil. Pese a ello, la landing page le resultó agradable visualmente, calificándola con un 8 de 10.
En cuanto a la última versión de la aplicación web, que utilizó en el navegador Google Chrome, no encontró dificultades en la navegación del flujo para añadir un cultivo y está conforme con la distribución de las secciones en la barra de navegación. Sin embargo, sugirió mejorar el formulario de registro de cultivos, añadiendo más campos de datos relevantes. A pesar de estas observaciones, le pareció que el diseño general de la aplicación web es bueno, aunque podría ser aún mejor si se implementan las mejoras propuestas.
Por último, evaluó la última versión de la aplicación móvil, la cual utilizó en un Samsung Galaxy S22, destacando su funcionalidad y diseño general. Aunque no se mencionaron observaciones específicas en este caso, sus comentarios serán fundamentales para seguir optimizando tanto la aplicación web como la móvil y la landing page.


**Segmento Objetivo: Comerciantes que quieren mejorar la calidad de sus ventas**

Nombre y apellidos: Andre Luna

Edad: 25

Distrito: Lince - Lima

Link: https://goo.su/Cvsf6


Inicio: 11:30

Fin: 23:45

Duración: 12:25

![imagen](https://github.com/user-attachments/assets/b14b972f-e846-4973-816b-a408d5389483)


Al analizar la entrevista, Andre nos menciona que las vistas son atractivas y adecuadas para el propósito de la aplicación que se desea ofrecer. Además, le resulta muy fácil navegar en ella al ser intuitiva, y las secciones le parecen bien distribuidas. Con respecto a la información brindada acerca de las funcionalidades, considera que es adecuada. No tuvo problemas para abrir la landing page en su dispositivo móvil, calificándola con un 8 de 10.
En cuanto a la última versión de la aplicación web, que utilizó en el navegador Mozilla Firefox, nos brindó una sugerencia relacionada con la creación de un perfil propio del usuario, donde se puedan proporcionar teléfonos de contacto, lo que facilitaría aún más la comunicación con el agricultor. Además, sugirió mejorar la tipografía y el tamaño de algunos botones. Finalmente, aunque considera que la aplicación web es muy buena, cree que aún se puede mejorar añadiendo más funciones y puliendo un poco más las vistas.
Andre destacó su experiencia con la aplicación móvil, utilizada en un iPhone 14 Pro Max, resaltando su diseño moderno, intuitivo y responsivo, adaptado perfectamente a la pantalla del dispositivo. Subrayó la fluidez en la navegación y el rápido tiempo de respuesta, además de la accesibilidad de botones y textos. Sin embargo, sugirió incorporar funciones personalizadas como la configuración de perfil, optimización de notificaciones y tutoriales interactivos para nuevos usuarios, lo que mejoraría la experiencia general. A pesar de estas observaciones, calificó la app con un 9 de 10, considerándola una herramienta muy cercana a ser ideal con algunos ajustes adicionales.

Nombre y apellidos: Favio Onofre

Edad: 21

Distrito: Lince - Lima

Link: https://goo.su/Cvsf6


Inicio: 23:45

Fin: 33:13

Duración: 09:28

![imagen](https://github.com/user-attachments/assets/c1148d96-3c42-4ccc-9ff0-540c39185178)

Favio nos dedicó su tiempo para explorar la landing page y las aplicaciones web de Ayni, compartiendo su opinión sobre el diseño y funcionalidad de ambas. Le pareció que el diseño es bueno y adecuado, y destacó la claridad de la información acerca de las funcionalidades de la aplicación web presentadas en la landing page, describiéndola como agradable a la vista. Pudo acceder a la landing page desde su navegador Google Chrome sin inconvenientes, calificándola con un 8 de 10. Sin embargo, sugirió algunas mejoras, como ajustar el tamaño de los botones y reducir la cantidad de información, que considera algo excedente.
En cuanto a la aplicación web, Favio recomendó incluir información más detallada sobre los cultivos, como datos sobre el clima o la altitud, para enriquecer la experiencia del usuario. A pesar de ello, elogió la correcta distribución de las secciones y los colores utilizados, destacando que reflejan características propias de la agricultura y generan un ambiente visualmente ameno. Sus comentarios son valiosos para continuar mejorando tanto la landing page como la aplicación web.
Favio también exploró la aplicación móvil de Ayni, utilizándola en un Xiaomi Redmi Note 12, y compartió su experiencia. Destacó que la aplicación es intuitiva y funcional, con un diseño limpio que mantiene la coherencia con las otras plataformas. La navegación le resultó sencilla, permitiéndole explorar las funciones principales sin complicaciones. Sin embargo, sugirió incluir un apartado de guía rápida o tutorial interactivo para nuevos usuarios, que podría facilitar aún más el uso de la app.
Entre los aspectos positivos, resaltó el tiempo de respuesta ágil de la app y su correcta adaptación al tamaño de la pantalla del dispositivo. No obstante, recomendó optimizar algunos elementos visuales, como el tamaño y la ubicación de ciertos botones, para mejorar la experiencia de uso. En general, calificó la aplicación móvil con un 8.5 de 10, considerando que, con algunas mejoras, podría ser una herramienta aún más eficiente y atractiva para los usuarios. Su retroalimentación abarca puntos clave para seguir perfeccionando las tres plataformas de Ayni.

Nombre y apellidos: Juli Carrión

Edad: 45

Distrito: Surco - Lima

Link: https://goo.su/Cvsf6


Inicio: 33:13

Fin: 40:52

Duración: 07:39


![imagen](https://github.com/user-attachments/assets/b73a2a3c-a956-4109-bb29-0a367714f680)


Juli nos compartió su sincera opinión acerca de la landing page, la aplicación web y la aplicación móvil. Con respecto a la landing page, elogió la distribución de las secciones y la promoción del producto, destacando que ofrece la información necesaria sobre las funcionalidades. Sin embargo, recomendó reducir un poco el texto y presentar las funcionalidades de manera más específica. A pesar de ello, encontró la navegación por las secciones agradable, calificándola con un 8 de 10.
En cuanto a la aplicación web, Juli comentó que no tuvo complicaciones para encontrar y seleccionar un cultivo para comprar. Destacó la buena distribución de las secciones, ya que resumen adecuadamente las funcionalidades ofrecidas. Considera que la app está completa para sus necesidades como comerciante y no cree necesario añadir más características. Sin embargo, sugirió mejorar la sección de estado de compra, añadiendo más detalles relevantes para el usuario. En general, describió la aplicación web como muy buena, intuitiva y efectiva, con un diseño adecuado.
Sobre la aplicación móvil, que utilizó en un iPhone 13 Mini, destacó la fluidez y rapidez en su desempeño. Resaltó que el diseño es coherente con las otras plataformas, pero sugirió optimizar algunos elementos visuales, como la legibilidad de los textos en pantallas más pequeñas. En general, calificó la experiencia móvil como positiva, mencionando que facilita sus tareas como comerciante y complementa perfectamente la aplicación web y la landing page.

## 6.3.3 Evaluaciones según heurísticas

UX Heuristics & Principles Evaluation

En esta sección se realizará el reporte de Heurísticas de usabilidad que se ecnotnraron en la realización de la valdiación con posibles usuarios según su segmento.

**Usability – Inclusive Design – Information Architecture**

**CARRERA : Ingeniería de Software**

**CURSO : Desarrollo de Soluciones IOT**

**SECCIÓN : SW74**

**PROFESORES : Todos**

**AUDITOR : Equipo de desarrollo Greatminds** 

**CLIENTE(S) : Ayni** 


- **SITE o APP A EVALUAR:**

Ayni - Solución IOT de gestión y monitoreo agrícola. 

- **TAREAS A EVALUAR:**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Desktop landing page
   1. Información y descripción de la aplicación y sus funcionalidades
   2. Visualización de botón call to action y redirección a web applications
   3. Header y footer apropiado para la landing page
2. Web Applications
   1. Registro de nuevo usuario
   2. Inicio de sesión de usuario existente
   3. Botones interactivos y de uso intuitivo
   4. Creación de cultivos
   5. Navegación y orientación dentro de las secciones
   6. Proceso de compra de cultivo
   7. Visualización de cultivos
3. Mobile Application
    1. 

- **ESCALA DE SEVERIDAD:**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

|**Nivel:**|**Descripción**|
| :- | :- |
|**1**|<p>Problema superficial: puede ser fácilmente superador por el usuario ó ocurre con muy poco </p><p>frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.</p>|
|**2**|<p>Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de </p><p>superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente </p><p>reléase</p>|
|**3**|<p>Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es </p><p>importante que sean corregidos y se les debe asignar una prioridad alta.</p>|
|**4**|<p>Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de </p><p>la herramienta. Es imperativo que sea corregido antes del lanzamiento</p>|



- **TABLA RESUMEN:**

1. **Web Application**

|*#*|*Problema*|*Escala de severidad*|*Heurística/Principio violada(o)*|
| :-: | :-: | :-: | :-: |
|*1*|*El formato de diseño elegido para los botones es inconsistente*|*1*|*Usabilidad - Consistencia y estándares*|
|*2*|*Al estar en una de las secciones, resulta imposible de diferenciar entre estos debido a que la barra de navegación no indica en qué sección se encuentra el usuario*|*1*|*Usabilidad - Reconocer antes que recordar*|
|*3*|*No existe un apartado de edición de perfil*|*2*|*Usabilidad - Control de usuario y libertad*|
|*4*|*En el inicio de sesión, la card de contenido no resalta diferencia del fondo*|*1*|*Usabilidad - Diseño estético y minimalista*|
|*5*|*Inconsistencia en tamaño de tipografía*|*2*|*Usabilidad - Consistencia y estándares*|

2. **Landing page**

|*#*|*Problema*|*Escala de severidad*|*Heurística/Principio violada(o)*|
| :-: | :-: | :-: | :-: |
|*1*|*El contenido de funcionalidades no se actualiza periódicamente*|*3*|*Information Architecture - Is it credible?*|

3. **Mobile Application**


|*#*|*Problema*|*Escala de severidad*|*Heurística/Principio violada(o)*|
| :-: | :-: | :-: | :-: |
|*1*|*Al estar en una de las pantallas, resulta imposible de diferenciar entre estos debido a que la barra de navegación no indica en qué sección se encuentra el usuario*|*1*|*Usabilidad - Reconocer antes que recordar*|


- **DESCRIPCIÓN DE PROBLEMAS:**



1. **Web Application**

***PROBLEMA #1:** El formato de diseño elegido para los botones es inconsistente*

***Severidad:** 1*

*Heurística violada: Usabilidad - Consistencia y estándares*

***Problema:***
Botones en sección "Sign In y Sign Up"

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/278846713-9ed0ca37-09d7-45c7-b111-b614739c209e.png)


Botones en sección "Financial Management"

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/278846724-a145e2c6-d273-4e4e-9bfc-73b8c11b22f8.png)


*El formato de diseño elegido para los botones “Sign In” es inconsistente a comparación de todas las secciones de la aplicación web. Esto incluye el color y bordes del botón que permite identificarlos. Como consecuencia, esto puede provocar que potencialmente los usuarios se desorienten y no puedan diferenciar el texto de un botón con el cual pueden interactuar.*

***Recomendación:**
Utilizar el mismo estilo de botones para mostrar más información en todas las secciones, de manera que el usuario se familiarice mejor con la aplicación web.*

***PROBLEMA #2:** Al estar en una de las secciones, resulta imposible de diferenciar entre estos debido a que la barra de navegación no indica en qué sección se encuentra el usuario*

***Severidad:** 1*

*Heurística violada: Usabilidad - Reconocer antes que recordar*

***Problema:***

Barra de navegación:

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/277204700-cbbfa595-2a68-4619-8a4c-fa66067715cc.png)


*Dentro de las secciones que se ofrecen para ambos roles, no existe ningún indicador resaltante que permita indicar al usuario en qué sección se encuentra, potencialmente provocando que se desubique.*

***Recomendación:**
Resaltar con un cuadro de color resaltante la sección que se seleccione dentro de la barra de navegación, con la finalidad de orientar al usuario.*

***PROBLEMA #3:** No existe un apartado de edición de perfil*

***Severidad:** 2*

*Heurística violada: Usabilidad - Control de usuario y libertad*

***Problema:***

*Dentro de la barra de navegación no hay un apartado de edición de perfil, esto ocasiona que el usuario no brinde y proporcione datos quepeuden llegar a ser relevantes, como teléfono de contacto entre otros campos.*

***Recomendación:**
Implementar un boton o apartado para editar perfil de usuario.*

***PROBLEMA #4:** En el inicio de sesión, la card de contenido no resalta diferencia del fondo*

***Severidad:** 1*

*Heurística violada: Usabilidad - Diseño estético y minimalista*

***Problema:***

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/277204363-409272f0-0261-4092-bccf-3331e5c190c8.png)


*En la pantalla de login, el contenido dento de la card principal de la página, no es notable visualmente ya que no tiene un color que lo diferencie del fondo principal, por lo que el usuario puede forzar la vista y descontrarse para realizar un inicio de sesión exitoso.*

***Recomendación:**
Cambiar el color de la card contenedora de los campos de inicio de sesión*

***PROBLEMA #5:** Inconsistencia en tamaño de tipografía *

***Severidad:** 2*

*Heurística violada: Usabilidad - Consistencia y estándares*

***Problema:***

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/277205109-ba79cecd-1ba0-489c-a18e-f8eeb0a91a3a.png)

*En las pantallas de home para ambos roles, existe una incosistencia en el tamaño de la tipografía, lo que ocasiona insatisfacción visual al usuario al momento de navegar por las pantallas de home*


***Recomendación:**
Corregir la tipografía en todas las secciones de un tamaño equivalente*

---

**Landing Page**

***PROBLEMA #1:**  El contenido de funcionalidades no se actualiza periodicamente*

***Severidad:** 3*

*Heurística violada: Information Architecture - Is it credible?*

***Problema:***

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/277208099-62d39d65-9fa9-4d98-859a-cf2b655faad0.png)

*En la sección de funcionalidades, algunas de estas ya no se están implementando, por lo que el usuario puede ser confundido al querer usar esas caracteristicas*

***Recomendación:**
Corregir las funcionalidades mostradas en las listas de la sección*

---

**Mobile Application**

**PROBLEMA #1:** Al estar en una de las pantallas, resulta imposible de diferenciar entre estos debido a que la barra de navegación no indica en qué sección se encuentra el usuario

***Severidad:** 1*

*Heurística violada: Usabilidad - Reconocer antes que recordar*

***Problema:***

![imagen](https://github.com/user-attachments/assets/d6b01ccc-f7cc-403a-bcde-044098a81327)

*En la pantalla de dashboard de monitoreo de cultivo no se presenta el bottom navigation bar, lo que resulta imposible*

# 6.4 Video About-the-Product

A continuación, se mostrará el Video About the Product, donde se mostrará las carácteristicas de la Landing Page para los segmentos objetivos interesados. De igual manera, la aplicación web y móvil serán mostrada en su nueva versión del Sprint #2, abarcando muchas más funcionalidades para ser expuestas en este video. Finalmente, también incluye un testimonio de uso realizado en una entrevista de validación:

![imagen](https://github.com/user-attachments/assets/64c16a19-d96e-42b6-8667-7097a6cf4a5c)

Link: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202118468_upc_edu_pe/EQvkrqtupmNCiHPncyZHlRIBhQ_NC-3csCH_4G9RJcVbeQ?e=92sY2y&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Finalmente, se presenta el video about the product donde se muestra las caracteristicas de los productos digitales en su ultima versión del Sprint 3.

![imagen](https://github.com/user-attachments/assets/ee795d38-c32e-43ed-aff8-d0fb2a0ea251)

Link: https://goo.su/nRWtcx