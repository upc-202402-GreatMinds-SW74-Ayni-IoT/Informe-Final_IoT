
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
## 4.2.X. Bounded Context
### 4.2.X.1. Domain Layer
### 4.2.X.2. Interface Layer
### 4.2.X.3. Application Layer
### 4.2.X.4. Infrastructure Layer
### 4.2.X.6. Bounded Context Software Architecture Component Level Diagrams
### 4.2.X.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.X.7.1. Bounded Context Domain Layer Class Diagrams
#### 4.2.X.7.2. Bounded Context Database Design Diagram
