
# 4.1. Strategic-Level Domain-Driven Design
## 4.1.1. EventStorming

Para la sección de Event Storming el equipo de desarrollo tuvo una reunión donde expusimos ideas acerca de las funcionalidades y caracteristicas a implementar en el proyecto. En el transcurso de la reunión, se lograron plantar varias ideas para la plataforma, adempas de las primeras versiones para los bounded context.

En esta etapa, se identificaron los eventos clave que representan las acciones significativas dentro de la solución IoT. La herramienta utilizada fue Miro.

![image](https://github.com/user-attachments/assets/5b71e5bb-3dfc-4ee1-a5c5-7784fb9ed31e)

**Step 2: Timelines**

Durante esta fase, los eventos identificados fueron agrupados en subgrupos liderados por un evento en general que encapsula la función principal del grupo. Estos grupos incluyen happy paths, que representan los caminos deseados o exitoso, y los unhappy paths, que muestran los posibles problemas o situaciones no deseadas que pudieran surgir. Esto ayudó a darle una estructura a los eventos de manera coherente y a comprender mejor las diferentes secuencias dentro del sistema.

![image](https://github.com/user-attachments/assets/a73985fe-fa74-4e70-93be-e4a7032fcf66)

**Step 3: Paint Points**

En este proceso, se identificaron paint points o puntos problemáticos, que son áreas donde los usuarios pueden experimentar dificultados o fricciones en su interacción con la aplicación. Estos puntos son cruciales para mejorar la experiencia del usuario y optimizar el diseño del sistema

![image](https://github.com/user-attachments/assets/9e683320-cf1a-4e5b-bf52-546938b22481)

**Step 4: Pivotal points**

Se señalaron los pivotal points o puntos clave, que son eventos críticos que marcan hitos improtantes en el flujo de la plataforma. Estos eventos tienden a ser significativos en el comportamiento del sistema o en la experiencia del usuario

![image](https://github.com/user-attachments/assets/4e9ddb98-1b05-4c27-bde1-9f5fdc17efc9)

**Step 5: Commands**

Cada evento se asoció a un comando en específico que lo desencadena y un actor que lo realiza. Esto ayudó a tener un mejor reconocimiento de cómo interactúan los diferentes usuarios con el sistema.

![image](https://github.com/user-attachments/assets/2bd72e32-cfd6-476b-99cb-eab1a6ed341b)

**Step 6: Policies**

Durante esta etapa, se identifican las politicas relevantes para cada contexto del sistema. Estas politica spueden incluir restricciones de negocio, reglas de validación, etc.

![image](https://github.com/user-attachments/assets/04d1a968-fb42-4fbb-9ca3-f7dee6049165)

**Step 7: Read Models**

Durante esta fase, se diseñan y desarrollan lso modelos de lectura para cada contexto de sistema, asegurando que proporcionen la información necesaria de manera eficiente y coherente.

![image](https://github.com/user-attachments/assets/ff16301c-fdb0-47bc-888e-299c017daf4f)

**Step 8: External Systems** 

Durante esta etapa, se identifican los sistemas externos relevantes para la plataforma y se establecen las interfaces necesarias para integrarlos de manera efectiva.

 ![image](https://github.com/user-attachments/assets/a1c3ffdd-f757-4aa1-8974-11cac30ac3bc)

**Step 9: Aggregates**

Durante esta etapa, se definen aggregates para cad contexto del sistema, asegurando que representen ocrrectamente las transacciones y operaciones coherentes dentro del sistema.

![image](https://github.com/user-attachments/assets/c8da11d9-476d-47ca-9f7b-ce20fc79a4e5)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

### 4.1.1.1 Candidate Context Discovery

A continuación, elegimos utilizar la técnica de start-with-value ya que el equipo de desarrollo decidió empezar por el valor de la aplicación (core), esto es importante para tener una mejor visión del producto.

- **Identificación de Valores del Negocio** : Analizamos los valores clave del negocio, como la experiencia del usuario al planificar y monitorear un cultivo, la compra de productos y la eficiencia en la gestión de usuarios.

- **Identificación de Funcionalidades clave** : Identificar las funcionalidades esenciales de la aplicación, como la autenticación y registro de usuarios (IAM), el monitoreo y planificación de cultivos (Management) y las funcionalidades relacionadas a la compra y calificaciones (Shopping), que contribuyen directamente a la entre de los valores empresariales.

Candidate para Bounded Context: IAM
![image](https://github.com/user-attachments/assets/8d7f084c-4395-40f7-9973-3033746a6b83)

Candidate para Bounded Context: Management
![image](https://github.com/user-attachments/assets/2eca0689-d2ae-49b5-9d8e-0b28da5df317)

Candidate para Bounded Context: Shopping
![image](https://github.com/user-attachments/assets/79aba723-b8ea-4412-8a12-2bdee20c0272)

Vista completa:
![Event Storming - Copy of Step 10_ Bounded Contexts](https://github.com/user-attachments/assets/c6b71474-bc4d-423c-a750-378ad516e789)



### 4.1.1.2 Domain Message Flows Modeling
**Usuario**
Scenario: El usuario desea iniciar sesión
![image](https://github.com/user-attachments/assets/c3b7edd2-10e6-4a3d-9477-a312e1e5f9bd)

**Agricultor**
Scenario: Agricultor desea crear un cultivo
![image](https://github.com/user-attachments/assets/aff750cc-ce25-4d8e-a4c7-09ac9b94b9f9)

**Comerciante**
Scenario: Comerciante desea comprar un cultivo
![image](https://github.com/user-attachments/assets/7533142b-6314-4f14-8302-cd6a376d46d8)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

### 4.1.1.3 Bounded Context Canvases

IAM:
![image](https://github.com/user-attachments/assets/f3c625c1-2a38-4091-a9da-718c705b2004)

Management:
![image](https://github.com/user-attachments/assets/78049c49-0e06-4443-bff3-5ce7a71c4140)

Shopping: 
![image](https://github.com/user-attachments/assets/3af24e41-68bf-4e32-a92b-7c23cf036600)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

## 4.1.2. Context Mapping



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

![IOT drazxcxzczxcwio](https://github.com/user-attachments/assets/c431c249-f2df-4c5c-9a76-0fc7dfe62b1a)



### 4.1.3.3. Software Architecture Deployment Diagrams

![IOT drawzxczxcio](https://github.com/user-attachments/assets/2d9fdec2-2887-4e55-ae57-26b1f3bf8e44)




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
