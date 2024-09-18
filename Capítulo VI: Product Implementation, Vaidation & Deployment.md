

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

Repositorio de pruebas de aceptación:

Repositorio frontend: https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/AyniFrontend

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

(imagen network)

El lenguaje de diseño de Landing Page y Web Applications estará basado en Material Design. Como biblioteca de componentes de UI se utilizará Angular Material.

Para el desarrollo de Web Services, se realizará bajo RESTful API architectural style y se hará uso de Spring Boot Framework, utilizando Java como lenguaje de Programación.

Para el desarrollo de Mobile App, se hará uso de Flutter/Dart como lenguaje y se utilizará el mismo Web Service anteriormente mencionado.


### 6.1.4 Software Deployment Configuration

Para el despliegue del Landing Page se utilizará Netlify, para el despliegue automático y gracias a su integración con GitHub se irá actualizando con cada commit realizado y para el Frontend de la aplicación se usará Netlify.

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
| Sprint 1 Goal| El objetivo del presente Sprint es en desarrollar la Landing Page y Web App usando los wireframes y mockups diseñados previamente |
| Sprint 1 - Velocity | El equipo puede aceptar 20 Story Points|
| Sprint 1 - Story Points | La suma de los Story Points de los User Sotires que se atenderá es 18|



### 6.2.1.2 Sprint Backlog 1

<table><tr><th valign="top">Sprint 1</th><th colspan="7" valign="top">Implementar landing page y primera versión de fronend</th></tr>
<tr><td colspan="2" valign="top">User Story</td><td colspan="6" valign="top">Work-Item / Task</td></tr>
<tr><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Id</td><td valign="top">Title</td><td valign="top">Description</td><td valign="top">Estimation (Hours)</td><td valign="top">Assigned To</td><td valign="top"><p>Status </p><p>(To-do / </p><p>InProcess / </p><p>To Review / </p><p>Done)</p></td></tr>
<tr><td rowspan="2" valign="top">HU-11</td><td rowspan="2" valign="top">Visualización de características de la aplicación web o móvil web en Landing Page</td><td valign="top">11.1</td><td valign="top">Implementar vistas con estilos</td><td valign="top">Realizar las secciones de funcionalidades y beneficios</td><td valign="top">4</td><td valign="top">Jorge Gonzales</td><td valign="top">Done</td></tr>
<tr><td valign="top">11.2</td><td valign="top">Implementar sección responsive </td><td valign="top">Realizar las secciones con proporciones repsonsive</td><td valign="top">4</td><td valign="top">Jorge Gonzales</td><td valign="top">Done</td></tr>

<tr><td rowspan="1" valign="top">HU-12</td><td rowspan="1" valign="top">Landing Page responsive</td><td valign="top">12.1</td><td valign="top">Implementar vistas responsive</td><td valign="top">Realizar los estilos de las secciones responsive</td><td valign="top">4</td><td valign="top">Paolo Espejo</td><td valign="top">Done</td></tr>


<tr><td rowspan="1" valign="top">HU-13</td><td rowspan="1" valign="top">Botón Call to Action</td><td valign="top">13.1</td><td valign="top">Implementar sección Hero con botón call to action</td><td valign="top">Realizar la sección hero con el botón call to action para redirigar a la aplicación</td><td valign="top">4</td><td valign="top">Luis Alejo</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-16</td><td valign="top">Sección principal ("Home")</td><td valign="top">16.1</td><td valign="top">Implementar sección Home </td><td valign="top">Realizar la vista y cards dentro de la sección Home en Web App </td><td valign="top">2</td><td valign="top">Jhonel Rios</td><td valign="top">Done</td></tr>

<tr><td valign="top">HU-04</td><td valign="top">Ver detalles del terreno de cultivo y de las fases de cosecha de los cultivos</td><td valign="top">04.1</td><td valign="top">Implementar vistas de registro y detalles de cultivo de la app web</td><td valign="top">Implementar componentes de paginación y barras de búsquedas en las secciones de la app web</td><td valign="top">4</td><td valign="top">Javier Sebastían</td><td valign="top">Done</td></tr>
<
</table>

### 6.2.1.3 Development Evidence for Sprint Review
### 6.2.1.4 Testing Suite Evidence for Sprint Review
### 6.2.1.5 Execution Evidence for Sprint Review
### 6.2.1.6 Services Documentation Evidence for Sprint Review
### 6.2.1.7 Software Deployment Evidence for Sprint Review
### 6.2.1.8 Team Collaboration Insights during Sprint
