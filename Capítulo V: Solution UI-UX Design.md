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




### 5.2.4 Searching Systems



### 5.2.5 Navigation Systems

## 5.3 Landing Page UI Design
### 5.3.1 Landing Page Wireframe
### 5.3.2 Landing Page Mock-up

## 5.4 Applications UI/UX Design
### 5.4.1 Applications Wireframes
### 5.4.2 Applications Wireflow Diagrams
### 5.4.3 Applications Mock-ups
### 5.4.4 Applications User Flow Diagrams
### 5.4.5 Applications Prototyping

## 5.5 Appilcations Prototyping

