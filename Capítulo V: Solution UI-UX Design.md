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

Link de Figma: https://www.figma.com/design/hvG1ZF2UKWOEpW9kons6b1/Landing-Page?node-id=0-1&t=yWIQX0TXDIKOqSn0-1

## 5.4 Applications UI/UX Design
### 5.4.1 Applications Wireframes

**Web Application**

**Pantallas relacionadas al inicio de sesión y registro de usuario**

![image](https://github.com/user-attachments/assets/6d2041c9-f06e-4fbb-9fce-a5204806d6b1)


**Pantallas relacionadas a la gestión de los cultivos del agricultor**

![image](https://github.com/user-attachments/assets/1f054f21-8a04-46c1-9d40-b420c17f3135)


**Pantallas relacionadas a la gestión de solicitudes de compra del agricultor**

![image](https://github.com/user-attachments/assets/0fd1c04a-0c64-4dd7-b199-9cf5edeeee6b)


**Pantallas relacionadas al proceso de compra del comerciante**

![image](https://github.com/user-attachments/assets/34d3df8e-dd05-40c5-8f27-8efa27e06cd7)


**Pantallas relacionadas al proceso de calificar un producto por parte del comerciante**

![image](https://github.com/user-attachments/assets/92238f77-9567-4ec5-8d69-ca0c147e5e15)


---

**Mobile Application**

**Pantallas relacionadas al inicio de sesión y registro de usuario**

![image](https://github.com/user-attachments/assets/e18c50d4-23cb-4ba6-9a65-fa1e0239be65)

**Pantallas relacionadas a la gestión de cultivos del agricultor**

![image](https://github.com/user-attachments/assets/d17f5991-4037-4d16-9ca3-1fe82c93b867)

**Pantallas relacionadas al proceso de compras del comerciante**

![image](https://github.com/user-attachments/assets/53951723-27c7-4764-9c4b-9cfdc362546c)

**Pantalals relacionadas al estado de la orden de un cultivo**

![image](https://github.com/user-attachments/assets/e8092df0-a4a8-4b1e-a122-bef1a7902fa4)

**Pantallas relacionadas al proceso de calificar un producto por parte del comerciante**

![image](https://github.com/user-attachments/assets/7f5094bc-4d88-4e90-aad8-6baaf2b981fb)

Link de Figma: https://www.figma.com/design/ihUX0q6TZToajfIfLt5h82/Wireframes-App.-Moviles?node-id=0-1&t=o66KQhhg5VyRkx9e-1

### 5.4.2 Applications Wireflow Diagrams

En esta sección, se presentan los wireflows de la aplicación web y móvil guiándose de las historias de usuario en la herramienta LucidChart.

Link de Lucidchar: (https://lucid.app/lucidchart/aa72d3cf-f994-4a82-9ad8-044f3b9fc331/edit?viewport_loc=676%2C-2242%2C15341%2C7356%2C0_0&invitationId=inv_0da86b32-9131-4d2a-9317-1d95207a50e7)

**Web App**

Usar Goal: Como usuario, quiero poder registrarme en la aplicación para acceder a las funcionalidades disponibles.

Task Flow:

- Primero se observará la pantalla de inicio de sesión, en esta se puede o iniciar o registrarse
- Si accede a registrarse, se mostrará la pantalla de registro. Puede regresar a iniciar sesión o continuar
- Finalmente, se accede a la pantalla de selección de roles si es que se registra, para que acceda a la aplicación.

![image](https://github.com/user-attachments/assets/6bf9e278-b55a-48bc-974c-f10a1d82ea5e)

---

User Goal: Como agricultor (Maria Gracia), quiero ingresar los datos correspondientes para la planificación de las actividades agrícolas.

Task Flow:

- Primero se está en la pantalla de “Mis productos”
- Si presiona el botón de “Añadir nuevo producto”, se mostrará la pantalla para rellenar los datos del cultivo
- Luego, se mostrará un dashboard para la planificación de cultivo, donde se irá introduciendo pasos para la planificación
- Finalmente, se mostrará el calendario de la planificación donde el usuario podrá introducir eventos

![image](https://github.com/user-attachments/assets/fe8480a0-5196-4b3c-8444-c550245cfcd8)

---

User Goal: Como usuario tipo agricultor (Maria Gracia), deseo ver los pedidos que tengo de manera rápida y fácil en una pantalla

Task Flow:

- Primero el usuario tiene que estar en la sección del header “Mis pedidos”
- Luego, se mostrará la pantalla de pedidos con las listas de los pedidos pendientes
- Al seleccionar un pedido, el productor puede darle al botón de aceptar o rechazar pedido

![image](https://github.com/user-attachments/assets/9efcab4f-3255-4ae5-b97f-26cd5b01175f)

---

User Goal: Como usuario de la aplicación Ayni deseo encontrar los productos de manera rápida para no perder tiempo

Task Flow:

- Primero el usuario debe encotnrarse en una de las paginas de inicio o en secciones con paginación
- Luego, el usuario deberá escribir lo que desea en el input y luego darle click al icono de la lupa, en caso de paginación escoger la pagina deseada.

![image](https://github.com/user-attachments/assets/baefe68f-f238-48fe-81a3-d1ae016f8e61)

---

User Goal: Como comercializador (Carlos Martinez) quiero observar los productos disponibles para poder realizar los pedidos

Task Flow:

- Primero el usuario tiene que estar en la sección “Buscar Productos”
- Luego se mostrará la pantalla con los productos disponibles y una descripción

![image](https://github.com/user-attachments/assets/792a0f1d-9b25-48c7-9014-eef8924d9235)

---

Usar Goal: Como comercializador (Carlos Martinez), quiero poder realizar los pedidos de productos agrícolas para poder realizar las entregas

Task Flow:

- Primero el usuario debe estar en la pantalla de buscar productos
- Luego debe seleccionar el producto que desee comprar
- Se debe dar click en comprar y aparecerá la pantalla de dashboard donde debe completar datos para la compra

![image](https://github.com/user-attachments/assets/4656cc1a-c928-4a4a-9e8a-6c1fb171f071)

---

User Goal: Como comercializador (Carlos Martinez), quiero poder observar el estado de los pedidos y entregas para poder sentirme más tranquilo

Task Flow:

- Primero el usuario debe estar en la pestaña de “Mis compras”
- Seleccionar un producto y luego se le mostrará el estado de su compra e información
- Si hace click en el botón “Ver estado” podrá ver detalladamente el estado actual del producto

![image](https://github.com/user-attachments/assets/cceeabd4-705d-4ed8-b086-20db14374ac1)

---

User Goal: Como comercializador (Carlos Martinez), quiero acceder a las calificaciones y reseñas dejadas por los agricultores para saber sobre la valoración de mis servicios

Task Flow:

- Primero el usuario debe estar en la sección “Calificaciones”
- En la siguiente pantalla se mostrará información de los productos que compró y una calificación en estrellas

![image](https://github.com/user-attachments/assets/571cf5f6-aa1a-47d1-8531-4d188c1ee082)

---

**Mobile App**

User Goal: Como comercializador (Carlos Martinez) quiero observar los productos disponibles para poder realizar los pedidos

Task Flow:

- Primero el usuario tiene que estar en la sección “Buscar Productos”
- Luego se mostrará la pantalla con los productos disponibles y una descripción

![image](https://github.com/user-attachments/assets/b2913e71-56bd-42b7-95b6-2330a43cd214)


---

Usar Goal: Como comercializador (Carlos Martinez), quiero poder realizar los pedidos de productos agrícolas para poder realizar las entregas

Task Flow:

- Primero el usuario debe estar en la pantalla de buscar productos
- Luego debe seleccionar el producto que desee comprar
- Se debe dar click en comprar y aparecerá la pantalla del detalle para una orden
- Luego se añade un medio de pago y se confirma la compra

![image](https://github.com/user-attachments/assets/8fc2f305-04d7-4c9e-a5e4-52ed84babfb5)

---

User Goal: Como comercializador (Carlos Martinez), quiero poder observar el estado de los pedidos y entregas para poder sentirme más tranquilo

Task Flow:

- Primero el usuario debe estar en la pestaña de “Mis compras”
- Seleccionar un producto y luego se le mostrará el estado de su compra e información
- Si hace click en el botón “Ver estado” podrá ver detalladamente el estado actual del producto
- Si desea cancelar el producto le saldrá un aviso de confirmación

![image](https://github.com/user-attachments/assets/b762188b-74b8-4f0d-a90e-73b72fe8d0a2)



### 5.4.3 Applications Mock-ups

**Web Application**

**Pantallas relacionadas al inicio de sesión y registro de usuario**

![image](https://github.com/user-attachments/assets/8ae3e093-fe59-4af9-93ff-f03df738f190)


**Pantallas relacionadas a la gestión de los cultivos del agricultor**

![image](https://github.com/user-attachments/assets/af1c60fb-26ed-4d91-8811-6164f18691e3)


**Pantallas relacionadas a la gestión de solicitudes de compra del agricultor**

![image](https://github.com/user-attachments/assets/1c807d38-1b3c-4331-a56a-74734a0d8d98)


**Pantallas relacionadas al proceso de compra del comerciante**

![image](https://github.com/user-attachments/assets/3915590c-a8f1-445e-9b3a-752d7524b8b8)


**Pantallas relacionadas al proceso de calificar un producto por parte del comerciante**

![image](https://github.com/user-attachments/assets/7b9e0c31-6b9f-40f7-b2b9-b62527f94bc7)


---

**Mobile Application**

**Pantallas relacionadas al inicio de sesión y membresias**

![image](https://github.com/user-attachments/assets/d664eba5-2098-4138-8c53-296b9a332f7c)

**Pantallas relacionadas a la exploración de productos (Comerciantes)**

![image](https://github.com/user-attachments/assets/b66abc90-c3bc-4633-87ef-269331ced0fa)

**Pantallas de proceso de compra de un cultivo**

![image](https://github.com/user-attachments/assets/5f71c6ee-a249-4cf3-bdea-109b87a92902)

**Pantalla de calificación de una orden**

![image](https://github.com/user-attachments/assets/e7f16f33-5e3f-4703-bbec-5e579749402f)

**Pantalla de estado de una orden**

![image](https://github.com/user-attachments/assets/af19b50e-cb40-4e12-8cae-728dc0683bc9)

**Pantalla de registro de un cultivo por parte de agricultor**

![image](https://github.com/user-attachments/assets/c6e294f4-5c14-43e2-9557-3445b271f961)

**Pantalla de monitoreo de cultivos**

![image](https://github.com/user-attachments/assets/5456509a-5563-4334-8ad5-9db153be6a30)

**Pantalla de registro de plan de cultivo**

![image](https://github.com/user-attachments/assets/d58cef82-3f3c-469e-8029-47cf78148330)

**Pantalla de publicación de cultivo en venta**

![image](https://github.com/user-attachments/assets/402dc456-bd52-4d06-9ec3-eb6a2dc37ee7)

Link de Figma: https://www.figma.com/design/ihUX0q6TZToajfIfLt5h82/Wireframes-App.-Moviles?node-id=0-1&t=o66KQhhg5VyRkx9e-1

### 5.4.4 Applications User Flow Diagrams

**Web App**

User Goal: Observar el estado de los pedidos realizados

Task Flow:

- Primero el usuario debe estar en la pestaña de “Mis compras”
- Seleccionar un producto y luego se le mostrará el estado de su compra e información
- Si hace click en el botón “Ver estado” podrá ver detalladamente el estado actual del producto
- Si el usuario lo desea puede cancelar su compra (Unhappy Path)

![image](https://github.com/user-attachments/assets/d0bad33e-4583-400b-8d9c-7c92f9934f85)

Usar Goal: Realizar pedidos de productos agrícolas

---

Task Flow:

- Primero el usuario debe estar en la pantalla de buscar productos
- Luego debe seleccionar el producto que desee comprar
- Se debe dar click en comprar y aparecerá la pantalla de dashboard donde debe completar datos para la compra
- Si el usuario lo desea puede cancelar la compra con el botón "Cancelar compra" (Unhappy Path)

![image](https://github.com/user-attachments/assets/7e0680f6-9a58-4a67-889f-5caf938605d1)

---

User Goal: Visualizar los pedidos existentes

Task Flow:

- Primero el usuario tiene que estar en la sección del header “Mis pedidos”
- Luego, se mostrará la pantalla de pedidos con las listas de los pedidos pendientes
- Al seleccionar un pedido, el productor puede darle al botón de aceptar (Happy Path) o rechazar pedido (Unhappy Path)

![image](https://github.com/user-attachments/assets/654c5896-9411-418c-b37a-b1ba2a8101fe)

---

User Goal: Añadir cultivos y realizar plan de cultivo de este mismo

Task Flow:

- Primero se está en la pantalla de “Mis productos”
- Si presiona el botón de “Añadir nuevo producto”, se mostrará la pantalla para rellenar los datos del cultivo
- Luego, se mostrará un dashboard para la planificación de cultivo, donde se irá introduciendo pasos para la planificación
- Finalmente, se mostrará el calendario de la planificación donde el usuario podrá introducir eventos
- Si el usuario quiere eliminar el cultivo, le debe dar al botón "Elminar cultivo" (Unhappy Path)

![image](https://github.com/user-attachments/assets/882ac091-f77f-415f-9fbc-54a604e6fb01)

---

**Mobile App**

User Goal: Visualizar los datos de los sensores para el monitoreo de cultivo

Task Flow:
- Primero al seleccionar un cultivo existente
- Al dar en el boton de "Cultivar"
- Se le mostrará los detalels del plan de cultivo acabo
- Luego, se le muestra un dashboard de la información de los sensores
- Si el usuario desea un resumen de la información de los sensores, al dar click al boton next será redirigido a esa pantalla
- Si el usuario desea terminar con el cultivo, le da al botón Back y se le lleva a la pantalla de inicio  (Unhappy path)

![image](https://github.com/user-attachments/assets/5ef50c70-ea69-405a-8069-98346ec27143)

---

User Goal: Añadir cultivos y realizar plan de cultivo de este mismo

Task Flow:

- Primero se está en la pantalla de “Mis productos”
- Se le muestran los cultivos disponibles para añadir un plan de cultivo
- Luego, se mostrará un formulario para la planificación de cultivo, donde se irá introduciendo pasos para la planificación
- Si el usuario quiere eliminar el cultivo, le debe dar al botón "Elminar cultivo" (Unhappy Path)

![image](https://github.com/user-attachments/assets/7c62c22e-656e-419a-b572-eae7064eb5b6)

---

User Goal: Visualizar los pedidos existentes

Task Flow:

- Primero el usuario tiene que estar en la sección del header “Mis pedidos”
- Luego, se mostrará la pantalla de pedidos con las listas de los pedidos pendientes
- Al seleccionar un pedido, el productor puede darle al botón de aceptar (Happy Path) o rechazar pedido (Unhappy Path)

![image](https://github.com/user-attachments/assets/61217a16-6eed-41c6-860b-c4ecba25c5f1)

---

User Goal: Visualizar los pedidos existentes

Task Flow:

- Primero el usuario tiene que estar en la sección del header “Mis pedidos”
- Luego, se mostrará la pantalla de pedidos con las listas de los pedidos pendientes
- Al seleccionar un pedido, el productor puede darle al botón de aceptar (Happy Path) o rechazar pedido (Unhappy Path)

![image](https://github.com/user-attachments/assets/2ad22083-73e4-489a-9a18-d26e044f6ca8)

---

User Goal: Observar el estado de los pedidos realizados

Task Flow:

- Primero el usuario debe estar en la pestaña de “Mis compras”
- Seleccionar un producto y luego se le mostrará el estado de su compra e información
- Si hace click en el botón “Ver estado” podrá ver detalladamente el estado actual del producto
- Si el usuario lo desea puede cancelar su compra (Unhappy Path)

![image](https://github.com/user-attachments/assets/f076b3b0-1493-4d6e-9a6b-c81ae75d3425)



### 5.4.5 Applications Prototyping

## 5.5 Appilcations Prototyping
En esta sección, se puede acceder al prototipo en la herramienta Figma. Asismismo se pueden evidenciar los principios de arquitectura de información, esto hace que la aplicación se vea lo más eficiente posible.

Principio de elección: Procuramos que la aplicación web Y MOVIL posea una cantidad de secciones a todo momento, por lo que se cuenta con la barra superior e inferior siempre en la aplicación con 4 secciones, los cuales podrá acceder a las funcionalidades rapidamente desde cualquier pantalla.

Principio de divulgación: La información presentada se separa por partes, de tal manera que el usuario encuentre lo que desee. Esto se evidencia en los detalles al seleccionar un cultivo.

![image](https://github.com/user-attachments/assets/6c3aed2b-58d2-45ee-8e8d-257dd61aea3d)


Link de video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202118468_upc_edu_pe/EbqyE9CXfb5Ehf9tzTvo2SABleoGIMDoOvpgHuxEPFCQ8w?e=RPmzQt&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D


**Web App:**
![image](https://github.com/user-attachments/assets/df0845c9-6c2e-46ab-85a6-33ee65fa4c6a)

**Mobile App:**
![image](https://github.com/user-attachments/assets/4c858d5f-d29d-499d-a117-fae2fd030ff6)

