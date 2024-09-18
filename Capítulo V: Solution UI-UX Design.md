# Capítulo V: Solution UI/UX Design

## 5.1 Style Guidelines
### 5.1.1 General Style Guidelines

Mediante la solución IoT Ayni se busca que los usuarios gocen de una interfaz que transmite formalidad, profesionalismo y la serenidad que transmiten los paisajes de campos de cultivo de Perú. Por ello, el equipo tomó la decisión de emplear recursos visuales que capten la atención de los segmentos objetivos y que sean fáciles de identificar. Como estrategia se utilizaron colores pasivos, con temperaturas frías (verde y azul) junto con fuentes tipográficas con diferentes tamaños y espaciados ligeramente amplios, con el propósito de generar placer visual y lograr que el texto sea más visible. Cabe destacar que no se emplearán texturas, pues se busca mantener un aspecto minimalista.

**Brand Overview**

La solución IOT Ayni, surge a partir de la necesidad de mejorar la calidad de los productos de cultivo a través de mejorar los procesos y el flujo de ganancias de los productos y de los comerciantes respectivamente. A partir de esto, se propuso desarrollar una solución completa incluyendo IOT que facilitará la planificación de cultivos, entre otras funciones con el fin de atender las necesidades previamente mencionadas.


**Brand Name**

El nombre de la solución IOT es Ayni. Este nombre nació de la lengua quechua para referirse al trabajo común y a la reciprocidad, que es lo que se desea para los clientes, nosotros les damos una solución IOT eficiente para ayudar a sus rutinas de cultivo y ellos nos dan el reconocimiento por facilitarles la tarea. Por otro lado, el logo de Ayni representa la esperanza y la vida a través de una hoja verde.

![Ayni Logo](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/ceb29e85-3c65-4758-85e6-feae0881ad60)

**Colores**

Colores primarios: El color primario empleado para el diseño del producto y para el logotipo es una escala de colores similares a la celeste aguamarina, el cual es una mezcla entre azul y verde que transmite balance, armonía, seguridad y novedad. Estas características permiten elaborar una interfaz no intrusiva, donde el fondo pasa desapercibido y como consecuencia, indirectamente otorga mayor prioridad al texto.

![Colores primarios](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/4a45a2af-990a-44f4-b4f8-7db5d0fc5133)

Colores secundarios: Como color secundario se seleccionó una escala de verdes, los cuales transmiten sentimientos tales como armonía, serenidad, sensación de crecimiento y están arraigados a conceptos como prestigio y bonanza económica, lo cual encaja a la perfección con el enfoque que buscamos potenciar de los agricultores.

![Colores secundarios](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/4e048e5c-9a84-459d-9965-e4891e8f2e3b)

Colores adicionales: Como colores adicionales se seleccionaron blanco, negro y dos tonalidades diferentes de rojo. Estos serán empleados dentro de la tipografía, botones y mensajes de la aplicación. El blanco también será empleado para algunos fondos que requieran que la visibilidad del texto resalte con mayor ímpetu.

![Adicionales](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/f7790537-54c7-4226-92bc-11323d7cf5b0)

**Tipografia:**

El equipo seleccionó la fuente de letra Archivo, un estilo tradicional y fácil de leer. La separación del interletraje es de 0,15 px, el interlineado es de 0,5 px y el tamaño de la fuente varía dependiendo de la finalidad de uso, por ejemplo, para los títulos se opta por un tamaño de 56 px, y para el texto redactado por el usuario 27 px. 

![Tipografia](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/2e9abaf9-db14-4c7f-b000-2a60df98a8c6)

Tono de comunicación y lenguaje aplicado
El tipo de lenguaje a emplear será serio y formal junto con entusiasmo y serenidad. Dado que se agregarán mejoras y pasos que captarán la atención del usuario. Asimismo, se agregaron elementos para perfeccionar la interfaz y diseño final para los clientes.


### 5.1.2 Web, Mobile and IoT Style Guidelines

Con respecto a la página web, está diseñada para mostrarse en el dispositivo que se esté usando, ya sea desde una computadora o dispositivo móvil (responsive), el sitio web estará disponible en ambas plataformas para proporcionar una mejor experiencia de usuario. Además, el patrón de diseño web usado es Flat Design, para que el usuario tenga una alta comprensión y una fácil interacción al momento de estar en la interfaz. 

Se utilizará el patrón Z:

![image](https://github.com/user-attachments/assets/0b4b3e9c-c055-4da0-b4b9-c4da4d384186)

Asimismo, se tienen contemplados los siguientes puntos relacionados a responsive web interfaces:

- Grid System: Generalmente un sistema de 12 columnas para permitir que la interfaz se adapte a diferentes tamaños de pantalla.
- Breakpoints: Definir puntos de quiebre (breakpoints) para adaptarse a pantallas pequeñas (móviles), medianas (tabletas) y grandes (escritorios). Ejemplos comunes son 320px, 768px y 1200px.
- Escalado en tipografía: Asegurarse de que el texto sea legible tanto en pantallas grandes como pequeñas. Por ejemplo, un tamaño mínimo de 16px para móviles.
- Consistencia en la paleta de colores: Usar una paleta de colores uniforme con variaciones para estados interactivos (hover, focus, active).
- Botones y Links: Tienen que ser lo suficientemente grandes para interactuar en pantallas táctiles (mínimo 44px de altura).
- Iconografía: Uso de iconos universales y reconocibles para navegación y acciones.

Con respecto a las interfaces de la aplicación móvil, se contemplan los siguientes puntos:

- Single Column: Ideal para aplicaciones de lectura de contenido (blogs, redes sociales), formularios simples, y listas de artículos o productos.
- Bottom Navigation: La barra de navegación principal se coloca en la parte inferior de la pantalla, donde es más fácil de alcanzar con el pulgar, especialmente en dispositivos móviles más grandes.
- Overlays: Utiliza capas superpuestas para mostrar información adicional sin cambiar de pantalla. Por ejemplo, ventanas emergentes que muestran más detalles o permiten realizar acciones rápidas.
- Floating Action Button: Un botón flotante que suele ubicarse en la esquina inferior derecha y proporciona acceso a la acción principal de la aplicación.

No se contemplan diseños de interfaz para la IoT embedded app debido a que la solución IOT no lo implica.


## 5.2 Information Architecture

En la presente sección, se establecerá la estructura de la solución IOT según cada segmento objetivo. Del mismo modo, los distintos elementos que se emplearán en la navegación dentro de las aplicaciones.

### 5.2.1 Organization Systems

En el presente punto se indicará los grupos de información en los cuales se aplicarán los tipos de estructuración visual, además, se indicará para qué segmento objetivo está diseñado y que tipo de categorización se utilizará.

**Segmento: Productores que desean mejorar su producción**

Jerárquica:

Lista de productos: los productores podrán visualizar sus productos que se mostrarán de manera ordenada mediante una lista. Con ello, los exportadores podrán ver los productos que tienen los productores

Lista de planificación de cultivo: Los productores luego de escoger un producto, se le mostrará sus planes de cultivo y asimismo empezar uno nuevo si no hay existente

Secuencial:

Atención de pedidos: 

En esta sección el productor puede atender los pedidos que realicen los exportadores de manera secuencial. Para ello, se deberá seguir ciertos pasos como la elección de aceptar el pedido o no, negociación de precio, selección de fecha, hora y lugar para la venta y la selección de método de pago.

Matricial:

Planes de cultivo: En este apartado el usuario visualizará y agregará las acciones que debe realizar en ciertos días propios de cada cultivo. Para ello, se presentarán varios items de registro.

**Segmento: Exportadores o comerciantes que desean vender productos de calidad**

Jerárquica:

Búsqueda de productos: El comerciante será capaz de buscar productos asimismo revisar el reporte de calidad y cantidad del cultivo donde fue extraído.

Calificación del servicio: El comerciante será capaz de realizar calificación en base a la producción que se pactó en la venta con el productor.


Secuencial:

Pedido de productos: En esta sección, se necesitaran realizar ciertos pasos como selección del producto, revisión de informe de cultivo, añadir propuesta de precio, añadir fecha, hora y lugar para el pedido. Este proceso es obligatorio para la elección de atender un pedido por parte del productor e indispensable para realizar una venta.

Algunas de las funcionalidades ofrecidas van dirigidas a ambos segmentos objetivos, estas son:

Jerarquica:

Landing Page: En esta sección se presentará a los visitantes del sitio web estático y toda la información acerca del producto solución. Esta información se mostrará categorizada por secciones y organizada en base a su relevancia. Algunas de las secciones a presentar son:

Matricial: Menú de opciones: Tanto productores como exportadores contarán con un menú de opciones que le permita acceder a cada una de las funciones de Ayni. Estas se presentaron en una lista sin ningún orden en especifico, solo variara de acuerdo con el segmento al que pertenezca el usuario

### 5.2.2 Labeling Systems

A continuación, el equipo mostrará el sistema de etiquetado que otorgará una descripción breve y clara de la información brindada por la Landing Page.

Los encabezados serán los siguientes:

- Inicio/Home: Sección preseleccionada por defecto que brindara una frase representativa y el logo de la aplicación, además brindara una idea principal del objetivo de esta.

- Sobre nosotros/About Us: Sección donde el cliente obtiene información acerca del equipo de desarrollo, será capaz de visualizar nuestra misión, visión, quienes somos y qué hacemos.

- Services/Funcionalidades: Sección dividida para cada segmento objetivo donde se mostrará las funcionalidades que otorga la aplicación para ellos.

- Contactanos/Contact Us: Sección donde se muestran nuestros canales de comunicación.

A continuación, el equipo mostrará el sistema de etiquetado que otorgará una descripción breve y clara de las funcionalidades brindadas por la aplicación web

Los encabezados son los siguientes:

Para productores:

Inicio/Home: En esta página preseleccionada por defecto que presentará los productos que tiene en cultivo además de mostrar las fechas con actividades provenientes de los planes de cultivo. Finalmente, saldrá publicidad de proveedores de insumos.

Mis Productos/My Products: Página que muestra los productos existentes que están en proceso de cultivo. Además, si no hay productos existentes estará presente un botón para agregar uno.

Mis Pedidos / My Orders: Página donde el usuario podrá ver y atender los pedidos que realicen los exportadores o comerciantes.

Para comerciantes:

Inicio/Home: Página preseleccionada por defecto que presentará el número de productos que se compró o publicidad, además de mostrar los pedidos que se acordaron recientemente.

Search Products / Buscar productos: Página donde el comerciante podrá buscar los productos que desea vender, además se hará el contacto con el productor y acordar el precio.

Rate Products / Calificar productos: Página donde el comerciante podrá calificar los productos que compró a los productores. Esta calificación será en base a números.

### 5.2.3 SEO Tags and Meta Tags

En esta sección, se presentarán las etiquetas que identificarán y diferenciarán al sitio web de los demás en internet. Gracias a ellos, se podrá encontrar a Ayni en los diversos buscadores.

Para el sitio web estático:

Tittle: Ayni

Description: Ayni - GreatMinds Oficial Landing Page

Keywords: harvest management, sell crops, harvest suppliers

Authors: GreatMinds team

Para la aplicación web:

Tittle: Ayni

Description: Ayni - GreatMinds Oficial Web Page

Keywords: harvest management, sell crops, harvest suppliers, crop planning,

Authors: GreatMinds team

Para la aplicación móvil:

Tittle: Ayni

Description: Ayni - GreatMinds Oficial Mobile App

Keywords: harvest management, sell crops, harvest suppliers, crop planning,

Authors: GreatMinds team


### 5.2.4 Searching Systems

En esta sección se presentarán los sistemas de búsqueda que se implementarán en la aplicación web. móvil y landing page. Al hacer uso de esos sistemas, los usuarios podrán encontrar la información que requieran.

En el sitio web estático, los usuarios podrán utilizar la barra de navegación para buscar la información acerca del producto solución, paralelas funcionalidades se hará uso interactivo de un botón donde se alternará entre “Para productores” y “Para comerciantes”

En la aplicación web y móvil:

Segmento: Productores que desean mejorar la calidad de sus productos

Mis productos: Esta sección le permitirá al productor realizar el seguimiento de sus cultivos. En esta sección luego el productor podrá realizar un plan de cultivo en la siguiente página luego de seleccionar el producto en “Mis productos”. En esta sección se podrá usar un buscador que contará con la función de filtro para los productos asimismo con la sección de planes de cultivo, donde se podrá realizar búsquedas de planes de cultivo predeterminado o hacer uno personalizado. Posteriormente, los resultados de esta búsqueda mostrarán una lista de lo deseado.

Mis pedidos: Esta sección le permitirá al usuario atender los pedidos que los comerciantes realicen, es de elección del productor atenderlos o no. Se mostrarán los pedidos en una lista según orden de origen predeterminadamente, pero estarán filtros para visualizar los pedidos según meses o días.

Segmento: Exportadores o comerciantes que desean mejorar la calidad de sus ventas

Búsqueda de productos: Esta sección es una de las más importantes para el flujo principal de la aplicación debido a ello, contará con un sistema de búsqueda mediante una barra para que los comerciantes busquen el producto en específico. En esta sección también se podrá acordar la venta, introducir un precio, fecha, hora y lugar. Posteriormente, se realiza la venta.

### 5.2.5 Navigation Systems

A continuación, el equipo mostrará los sistemas de navegación con los que contará Ayni para permitir a los usuarios navegar de manera rápida y segura a cualquier bloque de información.

En el Landing Page, se cuenta con encabezados que representan a las diversas secciones que estarán presentes. Estas estarán ubicadas en la parte superior de la página como menú horizontal siempre presente a la hora de bajar y subir con el ratón. Para que el usuario no tenga que realizar una traslación de manera manual por toda la página para llegar a una sección, se podrá usar estos encabezados para ubicarse inmediatamente en el sector que se desee. Obviamente, el visitante tiene que haber leído el título del encabezado para asegurarse de que se ubicará en la zona adecuada. Gracias a esto, se genera una traslación fácil e intuitiva.

En el caso de la aplicación web, se presenta un proceso similar para el menú principal, se utilizarán diversas opciones que presenta para trasladarse a otra página del sitio web. Estas opciones variarán de acuerdo al segmento objetivo al que pertenezca el usuario. Del mismo modo, se utilizan listados para los grupos de elementos, Dentro de estas listas podrán aplicar filtros que permitan a los usuarios navegar entre esas opciones

En el caso de la aplicación móvil, la navegación tendrá como caracteristica un scroll limitado, mostrando carruseles de los productos en loa sección Home, por otro lado, la navegación será asistida con un bottom navigation bar, que verían entre opciones según el tipo de usuario.

## 5.3 Landing Page UI Design

En esta sección se mostrará el desarrollo visual del Landing Page. Para ello, se usuará la herramienta de diseño web Figma, debido a sus funciones y plugins que nos permite desarrollar el prototipo sin dificultades. Asimismo se evidenciará el uso de los Style Guidelines e Information architecture.

### 5.3.1 Landing Page Wireframe

![wireframe landing2](https://user-images.githubusercontent.com/104078975/265294361-ba30a39c-91f2-4854-aae4-14e8560d2aa4.png) 

![wireframe landing1](https://user-images.githubusercontent.com/104078975/265294362-cf7b8b7d-a3c6-4886-a961-17ebea4f9f2f.png)

Link: https://www.figma.com/design/hvG1ZF2UKWOEpW9kons6b1/Landing-Page?node-id=0-1&t=yWIQX0TXDIKOqSn0-1

### 5.3.2 Landing Page Mock-up

Trabajando con los wireframes anteriormente mostrados, luego se aplicó los Style Guidelines para el uso de los colores. Como se aprecia, estos tienen un contraste llamativo en cada sección de la landing page.

![image](https://github.com/user-attachments/assets/b1d63659-6428-4324-acec-ff58e0398c3c)
![image](https://github.com/user-attachments/assets/d5ec52e7-3c6d-4a1a-9815-8e99e0445cf7)
![image](https://github.com/user-attachments/assets/c6b228a0-a7a3-4772-bed4-5b824dad6a0d)

Finalmente, este es un vistazo general a los mockups y wireframes:

![image](https://github.com/user-attachments/assets/695e511e-9000-48b8-b4bf-fe9b5f89d64e)

Link: Link: https://www.figma.com/design/hvG1ZF2UKWOEpW9kons6b1/Landing-Page?node-id=0-1&t=yWIQX0TXDIKOqSn0-1

## 5.4 Applications UI/UX Design
### 5.4.1 Applications Wireframes
### 5.4.2 Applications Wireflow Diagrams
### 5.4.3 Applications Mock-ups
### 5.4.4 Applications User Flow Diagrams
### 5.4.5 Applications Prototyping

## 5.5 Appilcations Prototyping

