
# 4.1. Strategic-Level Domain-Driven Design
## 4.1.1. EventStorming

Para la sección de Event Storming el equipo de desarrollo tuvo una reunión donde expusimos ideas acerca de las funcionalidades y caracteristicas a implementar en el proyecto. En el transcurso de la reunión, se lograron plantar varias ideas para la plataforma, adempas de las primeras versiones para los bounded context.

En esta etapa, se identificaron los eventos clave que representan las acciones significativas dentro de la solución IoT. La herramienta utilizada fue Miro.

![image](https://github.com/user-attachments/assets/f748594b-ad17-4f26-bb28-c271d86d68de)


**Step 2: Timelines**

Durante esta fase, los eventos identificados fueron agrupados en subgrupos liderados por un evento en general que encapsula la función principal del grupo. Estos grupos incluyen happy paths, que representan los caminos deseados o exitoso, y los unhappy paths, que muestran los posibles problemas o situaciones no deseadas que pudieran surgir. Esto ayudó a darle una estructura a los eventos de manera coherente y a comprender mejor las diferentes secuencias dentro del sistema.

![image](https://github.com/user-attachments/assets/06bcb0b0-dfec-495c-8ae7-f3736d412e5d)


**Step 3: Paint Points**

En este proceso, se identificaron paint points o puntos problemáticos, que son áreas donde los usuarios pueden experimentar dificultados o fricciones en su interacción con la aplicación. Estos puntos son cruciales para mejorar la experiencia del usuario y optimizar el diseño del sistema

![image](https://github.com/user-attachments/assets/9e683320-cf1a-4e5b-bf52-546938b22481)

**Step 4: Pivotal points**

Se señalaron los pivotal points o puntos clave, que son eventos críticos que marcan hitos improtantes en el flujo de la plataforma. Estos eventos tienden a ser significativos en el comportamiento del sistema o en la experiencia del usuario

![image](https://github.com/user-attachments/assets/fee46607-61c6-4efd-8409-d5f40907061d)


**Step 5: Commands**

Cada evento se asoció a un comando en específico que lo desencadena y un actor que lo realiza. Esto ayudó a tener un mejor reconocimiento de cómo interactúan los diferentes usuarios con el sistema.

![Event Storming - Copy of Step 5_ Commands](https://github.com/user-attachments/assets/9073d36f-350e-4f86-9eec-a0b098013af7)


**Step 6: Policies**

Durante esta etapa, se identifican las politicas relevantes para cada contexto del sistema. Estas politica spueden incluir restricciones de negocio, reglas de validación, etc.

![image](https://github.com/user-attachments/assets/1885247a-ee37-48b3-bd6b-d82a7a8742ca)


**Step 7: Read Models**

Durante esta fase, se diseñan y desarrollan lso modelos de lectura para cada contexto de sistema, asegurando que proporcionen la información necesaria de manera eficiente y coherente.

![image](https://github.com/user-attachments/assets/c7e5747e-7bf7-4c3d-a44e-2af2880b2675)


**Step 8: External Systems** 

Durante esta etapa, se identifican los sistemas externos relevantes para la plataforma y se establecen las interfaces necesarias para integrarlos de manera efectiva.

 ![image](https://github.com/user-attachments/assets/a1c3ffdd-f757-4aa1-8974-11cac30ac3bc)

**Step 9: Aggregates**

Durante esta etapa, se definen aggregates para cad contexto del sistema, asegurando que representen ocrrectamente las transacciones y operaciones coherentes dentro del sistema.

![Event Storming - Copy of Step 9; Aggregates](https://github.com/user-attachments/assets/278ba06f-b5f7-4059-93d8-7356e54165fa)


Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

### 4.1.1.1 Candidate Context Discovery

A continuación, elegimos utilizar la técnica de start-with-value ya que el equipo de desarrollo decidió empezar por el valor de la aplicación (core), esto es importante para tener una mejor visión del producto.

- **Identificación de Valores del Negocio** : Analizamos los valores clave del negocio, como la experiencia del usuario al planificar y monitorear un cultivo, la compra de productos y la eficiencia en la gestión de usuarios.

- **Identificación de Funcionalidades clave** : Identificar las funcionalidades esenciales de la aplicación, el monitoreo de cultivos con sensores y actuadores (Monitoring), planificación de cultivos (Planification) y 
 registro de nuevos cultivos (Crop Register) que contribuyen directamente a la entre de los valores empresariales.

Candidate para Bounded Context: IAM

![image](https://github.com/user-attachments/assets/61f21441-6d10-4bd4-aa29-5d5b3f754267)


Candidate para Bounded Context: Monitoring

![image](https://github.com/user-attachments/assets/b8891ce5-86e1-4940-897a-d47a3d8991dd)



Candidate para Bounded Context: Shopping

![image](https://github.com/user-attachments/assets/41776ae9-5f3c-417b-9c52-2b9a9c75e5af)



Candidate para Bounded Context: Planification

![image](https://github.com/user-attachments/assets/160156bf-ad75-421b-a5b2-2a99aa1c92a9)


Candidate para Bounded Context: Crop registration

![image](https://github.com/user-attachments/assets/a4483053-af9e-43b3-99f1-2644ed05a945)


Vista completa:
![Event Storming - Copy of Step 10_ Bounded Contexts (1)](https://github.com/user-attachments/assets/c097c48f-d683-4eef-bb09-747871a5ffd2)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 


### 4.1.1.2 Domain Message Flows Modeling
**Usuario**
Scenario: El usuario desea iniciar sesión
![image](https://github.com/user-attachments/assets/c3b7edd2-10e6-4a3d-9477-a312e1e5f9bd)

**Agricultor**
Scenario: Agricultor desea crear un cultivo
![image](https://github.com/user-attachments/assets/bfb1c762-d1a9-4f44-9656-68eb8c5be836)


**Comerciante**
Scenario: Comerciante desea comprar un cultivo
![image](https://github.com/user-attachments/assets/7533142b-6314-4f14-8302-cd6a376d46d8)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

### 4.1.1.3 Bounded Context Canvases

IAM:

![image](https://github.com/user-attachments/assets/f3c625c1-2a38-4091-a9da-718c705b2004)

Crop Registration:

![image](https://github.com/user-attachments/assets/74b2d39c-fdb2-4113-8b3c-1ed1418a9850)



Planification:

![image](https://github.com/user-attachments/assets/595a98dc-25ad-496b-81b3-0a33c834b936)


Monitoring:

![image](https://github.com/user-attachments/assets/20b0128e-4088-4897-9508-9d4cf728638f)


Shopping: 

![image](https://github.com/user-attachments/assets/3af24e41-68bf-4e32-a92b-7c23cf036600)



Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

## 4.1.2. Context Mapping

Después de realizar el EventStorming se identificó 5 bounded context: IAM, Shopping, Monitoring, Planification y Crop Registration. Se ha decidido usar los siguientes patrones:

**Relación 1: IAM ↔ Shopping**
Patrón: Customer/Supplier
Explicación: El contexto de Shopping actúa como un Customer que consume los servicios de autenticación y autorización del contexto IAM (Session Management), que es el Supplier. Shopping se adapta a la API de IAM para validar las sesiones de los usuarios.

**Relación 2: Crop Registration ↔ IAM**
Patrón: Customer/Supplier
Explicación: El contexto de registro de cultivos depende de la información del usuario pasada en base al rol escogido en IAM context.

**Relación 3: Crop Registration ↔ Planification**
Patrón: Anticurroption Layer
Explicación: Ambos contextos necesitan pasarse información y no comprometerse entre ellos, dado que una planificación debe ser ligada al cultivo

**Relación 4: Planification ↔ Monitoring**
Patrón: Anticurroption Layer
Explicación: El contexto de monitoring debe utilizar la información de las planificaciones dentro de su contexto respectivo.

**Relación 5: Monitoring ↔  Shoppoing Context**
Patrón: Customer/Supplier
Explicación: El contexto de monitoring debe brindarle la infomración de los sensores al momento de elegir el cultivo en su compra.

![IOT drawio (11)](https://github.com/user-attachments/assets/8cf4ad6e-cf46-42eb-86b0-c937ad440de1)



## 4.1.3. Software Architecture

A continuación, se muestra los diagramas C4 donde se expone la arquitectura de la aplicación creada.

### 4.1.3.1. Software Architecture System Landscape Diagram

Nuestra startup cuenta con un sistema de software Ayni(aplicación web y móvil) y cuenta con un sistema que maneja dispositivos IoT.

![IOT drawiso](https://github.com/user-attachments/assets/b202f2fe-2cdd-4dd2-a030-aaf39619870c)


### 4.1.3.2. Software Architecture Context Level Diagrams

En la siguiente imagen se aprecia 2 usuarios que interactúan con el sistema, "Farmer" y "Merchant" son el segmetno objetivo. Además existe una dependencia a un sistema externo, EmailJS.

![IOT drazxcio](https://github.com/user-attachments/assets/80dbd09a-c3ed-4cd3-8694-8e22b1ee2c7e)



### 4.1.3.2. Software Architecture Container Level Diagrams

En la siguiente imagen se visualizan los contenedores, los cuales sirven para dividr el sistema de la aplicación.

![IOT drawio (13)](https://github.com/user-attachments/assets/c9f8325f-9eb8-425b-a72b-fbf498e2571a)




### 4.1.3.3. Software Architecture Deployment Diagrams

![IOT drawio (12134)](https://github.com/user-attachments/assets/69aefb03-1d12-459d-8400-1aabe9797b46)


# 4.2. Tactical-Level Domain-Driven Design
## 4.2.1. Bounded Context: IAM
### 4.2.1.1. Domain Layer

<table>
    <tr>
        <td colspan="4" align="center">Aggregate</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>User</td>
        <td>Entity/Aggregate</td>
        <td colspan="2">Representación de los usuarios del segmento objetivo</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>id</td>
        <td>Long</td>
        <td>Private</td>
        <td>Identificador unico</td>
    </tr>
    <tr>
        <td>userName</td>
        <td>String</td>
        <td>Private</td>
        <td>Nombre de usuario</td>
    </tr>
     <tr>
        <td>email</td>
        <td>String</td>
        <td>Private</td>
        <td>Correo electronico</td>
    </tr>
     <tr>
        <td>password</td>
        <td>String</td>
        <td>Private</td>
        <td>Contraseña del usuario</td>
    </tr>
     <tr>
        <td>role</td>
        <td>String</td>
        <td>Private</td>
        <td>rol del usuario</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>getUsername</td>
        <td>username</td>
        <td>Public</td>
        <td>Obtención de nombre de usuario</td>
    </tr>
    <tr>
        <td>getEmail</td>
        <td>email</td>
        <td>Public</td>
        <td>Obtención de correo electrónico</td>
    </tr>
    <tr>
        <td>getPassword</td>
        <td>password</td>
        <td>Public</td>
        <td>Obtención de contraseña</td>
    </tr>
     <tr>
        <td>getRoles</td>
        <td>srtRoles</td>
        <td>Public</td>
        <td>Obtención del rol del usuario</td>
    </tr>
</table>

### 4.2.1.2. Interface Layer

<table>
    <tr>
        <td colspan="4" align="center">Controller</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>AuthController</td>
        <td>Controller</td>
        <td colspan="2">Controlador para autenticación</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>authService</td>
        <td>AuthService</td>
        <td>Private</td>
        <td>Servicio de autenticación</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>authenticateUser</td>
        <td>authenticatedResource</td>
        <td>Public</td>
        <td>Metodo para autenticar usuario</td>
    </tr>
    <tr>
        <td>registerUser</td>
        <td>signInResource</td>
        <td>Public</td>
        <td>Metodo de registro de usuario</td>
    </tr>
</table>

<table>
    <tr>
        <td colspan="4" align="center">Controller</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>UsersController</td>
        <td>Controller</td>
        <td colspan="2">Controlador para usuarios</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>userQueryService</td>
        <td>UserQueryService</td>
        <td>Private</td>
        <td>Servicio de registro de usuario</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>getAllUsers</td>
        <td>usersResource</td>
        <td>Public</td>
        <td>Metodo para obtener todos los usuarios/td>
    </tr>
    <tr>
        <td>getUserById</td>
        <td>userResource</td>
        <td>Public</td>
        <td>Metodo para obtener un usuario por id</td>
    </tr>
</table>


### 4.2.1.3. Application Layer

<table>
    <tr>
        <td colspan="4" align="center">Service</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>UserCommandService</td>
        <td>Service</td>
        <td colspan="2">Servicio con reglas de negocio para usuario</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>UserRepository</td>
        <td>Long</td>
        <td>private</td>
        <td>Repositorio de usuario</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>existByUsername</td>
        <td>user</td>
        <td>Public</td>
        <td>Metodo para validar usuario por nombre de usuario</td>
    </tr>
    <tr>
        <td>findByUsername</td>
        <td>user</td>
        <td>Public</td>
        <td>Metodo para obtener usuario por nombre de usuario</td>
    </tr>
</table>


### 4.2.1.4. Infrastructure Layer


<table>
    <tr>
        <td colspan="4" align="center">Repository</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>UserRepository</td>
        <td>Repository</td>
        <td colspan="2">Repositorio que guarda la información de los usuario</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>existsByUsername</td>
        <td>user</td>
        <td>Public</td>
        <td>Metodo para validar usuario por nombre de usuario</td>
    </tr>
    <tr>
        <td>findByUsername</td>
        <td>user</td>
        <td>Public</td>
        <td>Metodo para buscar usuario por nombre de usuario</td>
    </tr>
</table>



### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams

![structurizr-85725-Componente (1)](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/285030967-60a9a7b9-f81b-42f7-9082-7b85c6f66481.png)


### 4.2.1.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.1.7.1. Bounded Context Domain Layer Class Diagrams

![image](https://github.com/user-attachments/assets/756ee8f2-a2c0-4d8b-95d1-69b36efe7740)


#### 4.2.1.7.2. Bounded Context Database Design Diagram

![image](https://github.com/user-attachments/assets/71c76fb2-c063-42d8-a7be-0c6cd55fa1a3)


## 4.2.2. Bounded Context: Shopping
### 4.2.2.1. Domain Layer

<table>
    <tr>
        <td colspan="4" align="center">Aggregate</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>Order</td>
        <td>Entity/Aggregate</td>
        <td colspan="2">Representación de una orden para la compra</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>id</td>
        <td>Long</td>
        <td>Private</td>
        <td>Identificador unico</td>
    </tr>
    <tr>
        <td>orderedBy</td>
        <td>Long</td>
        <td>Private</td>
        <td>Ordenado por</td>
    </tr>
     <tr>
        <td>acceptedBy</td>
        <td>Long</td>
        <td>Private</td>
        <td>Aceptado por</td>
    </tr>
     <tr>
        <td>description</td>
        <td>String</td>
        <td>Private</td>
        <td>descripcion de la orden</td>
    </tr>
     <tr>
        <td>quantity</td>
        <td>Long</td>
        <td>Private</td>
        <td>cantidad de la orden</td>
    </tr>
        <tr>
        <td>OrderDate</td>
        <td>Date</td>
        <td>Private</td>
        <td>Estado de la orden</td>
    </tr>
    </tr>
        <tr>
        <td>totalPrice</td>
        <td>Double</td>
        <td>Private</td>
        <td>Precio total de la orden</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>updateDate</td>
        <td>orderedDate</td>
        <td>Public</td>
        <td>Actualización de fecha de la orden</td>
    </tr>
    <tr>
        <td>update</td>
        <td>orderedDate</td>
        <td>Public</td>
        <td>Actualizar la orden</td>
    </tr>
    <tr>
        <td>end</td>
        <td>status.Finalized</td>
        <td>Public</td>
        <td>Estado finalizados</td>
    </tr>
     <tr>
        <td>qualify</td>
        <td>status.Quialified</td>
        <td>Public</td>
        <td>Estado de calificado</td>
    </tr>
     <tr>
        <td>isPending</td>
        <td>orderStatus.pending</td>
        <td>Public</td>
        <td>Obtención del rol del usuario</td>
    </tr>
         <tr>
        <td>isQualified</td>
        <td>orderStatus.qualified</td>
        <td>Public</td>
        <td>Obtención del rol del usuario</td>
    </tr>
         <tr>
        <td>isFinalized</td>
        <td>orderStatus.finalizated</td>
        <td>Public</td>
        <td>Obtención del rol del usuario</td>
    </tr>
    </tr>
         <tr>
        <td>getStatus</td>
        <td>status</td>
        <td>Public</td>
        <td>Obtención de estado</td>
    </tr>
</table>

### 4.2.2.2. Interface Layer

<table>
    <tr>
        <td colspan="4" align="center">Controller</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>OrderController</td>
        <td>Controller</td>
        <td colspan="2">Controlador para ordenes</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>OrderQueryService</td>
        <td>orderQueryService</td>
        <td>Private</td>
        <td>Servicio de cola de ordenes</td>
    </tr>
        <tr>
        <td>OrderCommandService</td>
        <td>orderCommandService</td>
        <td>Private</td>
        <td>Servicio de comandos de ordenes</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>createOrder</td>
        <td>Order Resource</td>
        <td>Public</td>
        <td>Metodo para crear una orden</td>
    </tr>
</table>



### 4.2.2.3. Application Layer

<table>
    <tr>
        <td colspan="4" align="center">Service</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>OrderCommandService</td>
        <td>Service</td>
        <td colspan="2">Servicio con reglas de negocio para la orden</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Atributos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de dato</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>OrderRepository</td>
        <td>orderRepository</td>
        <td>private</td>
        <td>Repositorio de orden</td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td>existById</td>
        <td>order</td>
        <td>Public</td>
        <td>Metodo para validar orden por nombre de orden</td>
    </tr>
    <tr>
        <td>findById</td>
        <td>order</td>
        <td>Public</td>
        <td>Metodo para obtener orden por nombre de orden</td>
    </tr>
</table>


### 4.2.2.4. Infrastructure Layer


<table>
    <tr>
        <td colspan="4" align="center">Repository</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Categoria</td>
        <td colspan="2">Propósito</td>
    </tr>
    <tr>
        <td>OrderRepository</td>
        <td>Repository</td>
        <td colspan="2">Repository </td>
    </tr>
    <tr>
        <td colspan="4" align="center">Métodos</td>
    </tr>
    <tr>
        <td>Nombre</td>
        <td>Tipo de retorno</td>
        <td>Visibilidad</td>
        <td>Descripción</td>
    </tr>
    <tr>
        <td> findOrderBySaleIdAndId</td>
        <td>order</td>
        <td>Public</td>
        <td>Metodo para obtener una orden por sale Id</td>
    </tr>
</table>



### 4.2.2.6. Bounded Context Software Architecture Component Level Diagrams

![image](https://github.com/user-attachments/assets/874b41be-d048-4820-910a-8fc1f2a4530d)

### 4.2.2.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.2.7.1. Bounded Context Domain Layer Class Diagrams

![image](https://github.com/user-attachments/assets/6697ed43-5f31-4bc9-a241-d779fffc8477)


#### 4.2.2.7.2. Bounded Context Database Design Diagram

![image](https://github.com/user-attachments/assets/91d47e55-640d-4e7c-b129-439d5349f3af)

## 4.2.3. Bounded Context: Crop Registration
### 4.2.3.1. Domain Layer

<table> <tr> <td colspan="4" align="center">Aggregate</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>Product</td> <td>Entity/Aggregate</td> <td colspan="2">Representación de un producto agrícola</td> </tr> <tr> <td colspan="4" align="center">Atributos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>id</td> <td>Long</td> <td>Private</td> <td>Identificador único</td> </tr> <tr> <td>name</td> <td>String</td> <td>Private</td> <td>Nombre del producto</td> </tr> <tr> <td>description</td> <td>String</td> <td>Private</td> <td>Descripción del producto</td> </tr> <tr> <td>recommendedCultivationDistance</td> <td>String</td> <td>Private</td> <td>Distancia de cultivo recomendada</td> </tr> <tr> <td>recommendedCultivationDepth</td> <td>String</td> <td>Private</td> <td>Profundidad de cultivo recomendada</td> </tr> <tr> <td>recommendedGrowingClimate</td> <td>String</td> <td>Private</td> <td>Clima de crecimiento recomendado</td> </tr> <tr> <td>recommendedSoilType</td> <td>String</td> <td>Private</td> <td>Tipo de suelo recomendado</td> </tr> <tr> <td>recommendedGrowingSeason</td> <td>String</td> <td>Private</td> <td>Temporada de crecimiento recomendada</td> </tr> <tr> <td>imageUrl</td> <td>String</td> <td>Private</td> <td>URL de la imagen del producto</td> </tr> <tr> <td>userId</td> <td>Long</td> <td>Private</td> <td>Identificador del usuario que creó el producto</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>getId</td> <td>Long</td> <td>Public</td> <td>Obtiene el identificador del producto</td> </tr> <tr> <td>getName</td> <td>String</td> <td>Public</td> <td>Obtiene el nombre del producto</td> </tr> <tr> <td>getDescription</td> <td>String</td> <td>Public</td> <td>Obtiene la descripción del producto</td> </tr> <tr> <td>getRecommendedCultivationDistance</td> <td>String</td> <td>Public</td> <td>Obtiene la distancia de cultivo recomendada</td> </tr> <tr> <td>getRecommendedCultivationDepth</td> <td>String</td> <td>Public</td> <td>Obtiene la profundidad de cultivo recomendada</td> </tr> <tr> <td>getRecommendedGrowingClimate</td> <td>String</td> <td>Public</td> <td>Obtiene el clima de crecimiento recomendado</td> </tr> <tr> <td>getRecommendedSoilType</td> <td>String</td> <td>Public</td> <td>Obtiene el tipo de suelo recomendado</td> </tr> <tr> <td>getRecommendedGrowingSeason</td> <td>String</td> <td>Public</td> <td>Obtiene la temporada de crecimiento recomendada</td> </tr> <tr> <td>getImageUrl</td> <td>String</td> <td>Public</td> <td>Obtiene la URL de la imagen del producto</td> </tr> <tr> <td>getUserId</td> <td>Long</td> <td>Public</td> <td>Obtiene el identificador del usuario que creó el producto</td> </tr> </table>

### 4.2.3.2. Interface Layer

<table> 
  <tr> <td colspan="4" align="center">Controller</td> </tr> 
  <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> 
  <tr> <td>ProductController</td> <td>Controller</td> <td colspan="2">Controlador para productos</td> </tr> 
  <tr> <td colspan="4" align="center">Atributos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>ProductQueryService</td> <td>productQueryService</td> <td>Private</td> <td>Servicio de consultas de productos</td> </tr> 
  <tr> <td>ProductCommandService</td> <td>productCommandService</td> <td>Private</td> <td>Servicio de comandos de productos</td> </tr> 
  <tr> <td colspan="4" align="center">Métodos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>createProduct</td> <td>ProductResource</td> <td>Public</td> <td>Método para crear un producto</td> </tr> 
  <tr> <td>getAllProducts</td> <td>List&lt;ProductResource&gt;</td> <td>Public</td> <td>Método para obtener todos los productos</td> </tr> 
  <tr> <td>getProductById</td> <td>ProductResource</td> <td>Public</td> <td>Método para obtener un producto por ID</td> </tr> 
</table>

### 4.2.3.3. Application Layer

<table> <tr> <td colspan="4" align="center">Service</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>ProductCommandService</td> <td>Service</td> <td colspan="2">Servicio con lógica de negocio para productos</td> </tr> <tr> <td colspan="4" align="center">Atributos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>ProductRepository</td> <td>productRepository</td> <td>Private</td> <td>Repositorio de productos</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>handleCreateProduct</td> <td>Long</td> <td>Public</td> <td>Método para manejar la creación de un producto</td> </tr> <tr> <td>handleGetProductById</td> <td>Optional&lt;Product&gt;</td> <td>Public</td> <td>Método para manejar la consulta de un producto por su ID</td> </tr> <tr> <td>handleGetAllProducts</td> <td>List&lt;Product&gt;</td> <td>Public</td> <td>Método para manejar la consulta de todos los productos</td> </tr> </table>

### 4.2.3.4. Infrastructure Layer

<table> <tr> <td colspan="4" align="center">Repository</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>ProductRepository</td> <td>Repository</td> <td colspan="2">Repositorio para la persistencia de productos</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>findById</td> <td>Optional&lt;Product&gt;</td> <td>Public</td> <td>Método para encontrar un producto por su ID</td> </tr> <tr> <td>findAll</td> <td>List&lt;Product&gt;</td> <td>Public</td> <td>Método para obtener todos los productos</td> </tr> </table>

### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams

![image](https://github.com/user-attachments/assets/36aa4fad-8889-4eee-a0ec-1e560d7e333a)


### 4.2.3.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.3.7.1. Bounded Context Domain Layer Class Diagrams

![image](https://github.com/user-attachments/assets/025a1cfd-5749-45e9-8963-bb1f222b7955)



#### 4.2.3.7.2. Bounded Context Database Design Diagram

![image](https://github.com/user-attachments/assets/3710915f-2038-4d1a-9d92-c41a2864497a)


## 4.2.4. Bounded Context: Planification
### 4.2.4.1. Domain Layer

<table> <tr> <td colspan="4" align="center"><strong>Aggregate</strong></td> </tr> 
  <tr> <td><strong>Nombre</strong></td> <td><strong>Categoría</strong></td> <td colspan="2"><strong>Propósito</strong></td> </tr> 
  <tr> <td>Crop</td> <td>Entity/Aggregate</td> <td colspan="2">Representación de un cultivo agrícola</td> </tr> 
  <tr> <td colspan="4" align="center"><strong>Atributos</strong></td> </tr> 
  <tr> <td><strong>Nombre</strong></td> <td><strong>Tipo de dato</strong></td> <td><strong>Visibilidad</strong></td> <td><strong>Descripción</strong></td> </tr> 
  <tr> <td>id</td> <td>Long</td> <td>Private</td> <td>Identificador único del cultivo</td> </tr> 
  <tr> <td>name</td> <td>String</td> <td>Private</td> <td>Nombre del cultivo</td> </tr> 
  <tr> <td>pickUpWeed</td> <td>Boolean</td> <td>Private</td> <td>Indica si el deshierbe está activo</td> </tr> 
  <tr> <td>fertilizeCrop</td> <td>Boolean</td> <td>Private</td> <td>Indica si la fertilización del cultivo está activa</td> </tr> 
  <tr> <td>oxygenateCrop</td> <td>Boolean</td> <td>Private</td> <td>Indica si la oxigenación del cultivo está activa</td> </tr> 
  <tr> <td>makeCropLine</td> <td>Boolean</td> <td>Private</td> <td>Indica si se deben hacer líneas en el cultivo</td> </tr> 
  <tr> <td>makeCropHole</td> <td>Boolean</td> <td>Private</td> <td>Indica si se deben hacer hoyos en el cultivo</td> </tr> 
  <tr> <td>wateringDays</td> <td>Long</td> <td>Private</td> <td>Número de días de riego</td> </tr> 
  <tr> <td>pestCleanupDays</td> <td>Long</td> <td>Private</td> <td>Número de días de limpieza de plagas</td> </tr> 
  <tr> <td>product</td> <td>Product (Entity)</td> <td>Private</td> <td>Producto asociado al cultivo</td> </tr> 
  <tr> <td>userId</td> <td>Long</td> <td>Private</td> <td>Identificador del usuario responsable</td> </tr> 
  <tr> <td colspan="4" align="center"><strong>Métodos</strong></td> </tr> 
  <tr> <td><strong>Nombre</strong></td> <td><strong>Tipo de retorno</strong></td> <td><strong>Visibilidad</strong></td> <td><strong>Descripción</strong></td> </tr> 
  <tr> <td>updateInformation</td> <td>Crop</td> <td>Public</td> <td>Actualiza la información del cultivo</td> </tr> 
  <tr> <td>isPickUpWeedActive</td> <td>boolean</td> <td>Public</td> <td>Verifica si el deshierbe está activo</td> </tr> 
  <tr> <td>isFertilizeCropActive</td> <td>boolean</td> <td>Public</td> <td>Verifica si la fertilización del cultivo está activa</td> </tr> 
  <tr> <td>isOxygenateCropActive</td> <td>boolean</td> <td>Public</td> <td>Verifica si la oxigenación del cultivo está activa</td> </tr> 
  <tr> <td>isMakeCropLineActive</td> <td>boolean</td> <td>Public</td> <td>Verifica si se deben hacer líneas en el cultivo</td> </tr> 
  <tr> <td>isMakeCropHoleActive</td> <td>boolean</td> <td>Public</td> <td>Verifica si se deben hacer hoyos en el cultivo</td> </tr> 
  <tr> <td>getId</td> <td>Long</td> <td>Public</td> <td>Obtiene el identificador único del cultivo</td> </tr> 
  <tr> <td>getName</td> <td>String</td> <td>Public</td> <td>Obtiene el nombre del cultivo</td> </tr> 
  <tr> <td>getPickUpWeed</td> <td>Boolean</td> <td>Public</td> <td>Obtiene el estado del deshierbe</td> </tr> 
  <tr> <td>getFertilizeCrop</td> <td>Boolean</td> <td>Public</td> <td>Obtiene el estado de la fertilización del cultivo</td> </tr> 
  <tr> <td>getOxygenateCrop</td> <td>Boolean</td> <td>Public</td> <td>Obtiene el estado de la oxigenación del cultivo</td> </tr> 
  <tr> <td>getMakeCropLine</td> <td>Boolean</td> <td>Public</td> <td>Obtiene el estado de la creación de líneas en el cultivo</td> </tr> 
  <tr> <td>getMakeCropHole</td> <td>Boolean</td> <td>Public</td> <td>Obtiene el estado de la creación de hoyos en el cultivo</td> </tr> 
  <tr> <td>getWateringDays</td> <td>Long</td> <td>Public</td> <td>Obtiene el número de días de riego</td> </tr> 
  <tr> <td>getPestCleanupDays</td> <td>Long</td> <td>Public</td> <td>Obtiene el número de días de limpieza de plagas</td> </tr> 
  <tr> <td>getProduct</td> <td>Product</td> <td>Public</td> <td>Obtiene el producto asociado al cultivo</td> </tr> 
  <tr> <td>getUserId</td> <td>Long</td> <td>Public</td> <td>Obtiene el identificador del usuario responsable</td> </tr> 
</table>

### 4.2.4.2. Interface Layer

<table> 
  <tr> <td colspan="4" align="center">Controller</td> </tr> 
  <tr> <td>Nombre</td> <td>Categoría</td> <td colspan="2">Propósito</td> </tr> 
  <tr> <td>CropController</td> <td>Controller</td> <td colspan="2">Controlador para manejar solicitudes relacionadas con cultivos</td> </tr> 
  <tr> <td colspan="4" align="center">Atributos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>CropQueryService</td> <td>CropQueryService</td> <td>Private</td> <td>Servicio para consultas de cultivos</td> </tr> 
  <tr> <td>CropCommandService</td> <td>CropCommandService</td> <td>Private</td> <td>Servicio para comandos de cultivos</td> </tr> 
  <tr> <td colspan="4" align="center">Métodos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>createCrop</td> <td>Crop Resource</td> <td>Public</td> <td>Método para crear un nuevo cultivo</td> </tr> 
  <tr> <td>getAllCrops</td> <td>List(Crop Resource)</td> <td>Public</td> <td>Método para obtener todos los cultivos</td> </tr> 
  <tr> <td>getCropById</td> <td>Crop Resource</td> <td>Public</td> <td>Método para obtener un cultivo en especifico</td> </tr> 
</table>

### 4.2.4.3. Application Layer

<table> 
  <tr> <td colspan="4" align="center">Service</td> </tr> 
  <tr> <td>Nombre</td> <td>Categoría</td> <td colspan="2">Propósito</td> </tr> 
  <tr> <td>CropCommandService</td> <td>Service</td> <td colspan="2">Servicio que contiene las reglas de negocio para los cultivos</td> </tr> 
  <tr> <td colspan="4" align="center">Atributos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>CropRepository</td> <td>CropRepository</td> <td>Private</td> <td>Repositorio de cultivos</td> </tr> 
  <tr> <td colspan="4" align="center">Métodos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>getAllCrops</td> <td>List(Crop)</td> <td>Public</td> <td>Obtinene todos los cultivos</td> </tr> 
  <tr> <td>getCropById</td> <td>Crop</td> <td>Public</td> <td>Obtinene un cultivo especifico</td> </tr> 
  <tr> <td>getCropsByProductId</td> <td>List(Crop)</td> <td>Public</td> <td>Busca todos los cultivo que le pertenecen a un producto</td> </tr> 
  <tr> <td>getCropByProductId</td> <td>Crop</td> <td>Public</td> <td>Busca un cultivo por la id el producto</td> </tr> 
  <tr> <td>createCrop</td> <td>Crop</td> <td>Public</td> <td>Crea un cultivo</td> </tr> 
</table>

### 4.2.4.4. Infrastructure Layer

<table> <tr> <td colspan="4" align="center">Repository</td> </tr> 
  <tr> <td>Nombre</td> <td>Categoría</td> <td colspan="2">Propósito</td> </tr> 
  <tr> <td>CropRepository</td> <td>Repository</td> <td colspan="2">Repositorio para manejar la persistencia de cultivos</td> </tr> 
  <tr> <td colspan="4" align="center">Métodos</td> </tr> 
  <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> 
  <tr> <td>findCropByProductIdAndId</td> <td>Crop</td> <td>Public</td> <td>Encuentra un cultivo por su ID y el ID del producto asociado</td> </tr> 
  <tr> <td>findAllByProductId</td> <td>List(Crop)</td> <td>Public</td> <td>Retorna todos los cultivos asociados a un producto específico</td> </tr> 
    </table>

### 4.2.4.6. Bounded Context Software Architecture Component Level Diagrams

![image](https://github.com/user-attachments/assets/38bdd8af-3f7a-403c-9883-d780c5212818)

### 4.2.4.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.4.7.1. Bounded Context Domain Layer Class Diagrams

![image](https://github.com/user-attachments/assets/087a48ca-458e-48dd-98be-a4a7f338692a)


#### 4.2.4.7.2. Bounded Context Database Design Diagram

![image](https://github.com/user-attachments/assets/99e675a2-b960-4221-b757-b7ed9ca75d04)



## 4.2.5. Bounded Context: Monitoring
### 4.2.5.1. Domain Layer

<table> <tr> <td colspan="4" align="center">Aggregate</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>Sensor</td> <td>Entity/Aggregate</td> <td colspan="2">Representación de un sensor IoT para monitorear datos del terreno.</td> </tr> <tr> <td>Actuator</td> <td>Entity/Aggregate</td> <td colspan="2">Representación de un actuador IoT para realizar acciones automáticas en base a los datos monitoreados.</td> </tr> <tr> <td colspan="4" align="center">Atributos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>id</td> <td>Long</td> <td>Private</td> <td>Identificador único del sensor o actuador.</td> </tr> <tr> <td>dataValue</td> <td>String</td> <td>Private</td> <td>Valor de datos medido por el sensor (ej. temperatura).</td> </tr> <tr> <td>timestamp</td> <td>String</td> <td>Private</td> <td>Fecha y hora de la medición realizada por el sensor.</td> </tr> <tr> <td>status</td> <td>String</td> <td>Private</td> <td>Estado del actuador (ej. activado/desactivado).</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>CollectDailyData</td> <td>SensorData</td> <td>Public</td> <td>Recolectar datos diarios de los sensores.</td> </tr> <tr> <td>ActivateActuator</td> <td>void</td> <td>Public</td> <td>Activar un actuador basado en condiciones del terreno.</td> </tr> <tr> <td>DeactivateActuator</td> <td>void</td> <td>Public</td> <td>Desactivar un actuador.</td> </tr> </table>

### 4.2.5.2. Interface Layer

<table> <tr> <td colspan="4" align="center">Controller</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>MonitoringController</td> <td>Controller</td> <td colspan="2">Controlador para la gestión de sensores y actuadores IoT.</td> </tr> <tr> <td colspan="4" align="center">Atributos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>SensorQueryService</td> <td>sensorQueryService</td> <td>Private</td> <td>Servicio de consulta de sensores.</td> </tr> <tr> <td>ActuatorCommandService</td> <td>actuatorCommandService</td> <td>Private</td> <td>Servicio de comandos para actuadores.</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>getDailySensorData</td> <td>List<SensorData></td> <td>Public</td> <td>Obtener datos diarios de sensores.</td> </tr> <tr> <td>activateActuator</td> <td>void</td> <td>Public</td> <td>Activar un actuador basado en los datos recolectados.</td> </tr> <tr> <td>deactivateActuator</td> <td>void</td> <td>Public</td> <td>Desactivar un actuador.</td> </tr> </table>

### 4.2.5.3. Application Layer

<table> <tr> <td colspan="4" align="center">Service</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>SensorQueryService</td> <td>Service</td> <td colspan="2">Servicio para consultas de datos de sensores.</td> </tr> <tr> <td>ActuatorCommandService</td> <td>Service</td> <td colspan="2">Servicio para ejecutar comandos de actuadores.</td> </tr> <tr> <td colspan="4" align="center">Atributos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de dato</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>SensorRepository</td> <td>sensorRepository</td> <td>Private</td> <td>Repositorio de datos de sensores.</td> </tr> <tr> <td>ActuatorRepository</td> <td>actuatorRepository</td> <td>Private</td> <td>Repositorio de actuadores.</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>existById</td> <td>Boolean</td> <td>Public</td> <td>Método para validar la existencia de un sensor o actuador por ID.</td> </tr> <tr> <td>findById</td> <td>Sensor/Actuator</td> <td>Public</td> <td>Método para obtener un sensor o actuador por ID.</td> </tr> </table>

### 4.2.5.4. Infrastructure Layer

<table> <tr> <td colspan="4" align="center">Repository</td> </tr> <tr> <td>Nombre</td> <td>Categoria</td> <td colspan="2">Propósito</td> </tr> <tr> <td>SensorRepository</td> <td>Repository</td> <td colspan="2">Repositorio de sensores.</td> </tr> <tr> <td>ActuatorRepository</td> <td>Repository</td> <td colspan="2">Repositorio de actuadores.</td> </tr> <tr> <td colspan="4" align="center">Métodos</td> </tr> <tr> <td>Nombre</td> <td>Tipo de retorno</td> <td>Visibilidad</td> <td>Descripción</td> </tr> <tr> <td>findSensorById</td> <td>Sensor</td> <td>Public</td> <td>Método para obtener un sensor por su ID.</td> </tr> <tr> <td>findActuatorById</td> <td>Actuator</td> <td>Public</td> <td>Método para obtener un actuador por su ID.</td> </tr> </table>

### 4.2.5.6. Bounded Context Software Architecture Component Level Diagrams

![image](https://github.com/user-attachments/assets/e655c3e7-3fe7-438e-bc13-02e73f03df8c)

### 4.2.5.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.5.7.1. Bounded Context Domain Layer Class Diagrams

![image](https://github.com/user-attachments/assets/0c6f98c0-8bbb-41c1-ac54-4ddcfa8d8d25)

#### 4.2.5.7.2. Bounded Context Database Design Diagram

![image](https://github.com/user-attachments/assets/305633b9-6f93-4cf5-8711-8950ff5ddf92)

