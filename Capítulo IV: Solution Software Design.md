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

**Candidate para Bounded Context: IAM**

Este contexto está encargado de manejar el ciclo de vida de los usuarios en la plataforma, desde el registro hasta la validación de credenciales y el acceso a la plataforma, de acuerdo con su rol, ya sea agricultor o comerciante. Se cubren dos políticas clave: Política de Registro y Registro de Roles y Política de Autenticación.

Posibles responsabilidades del Bounded Context:
- Gestionar el registro y autenticación de usuarios.
- Definir y aplicar políticas de roles para asegurarse de que cada usuario tenga las capacidades correctas dentro del sistema.
- Proveer un sistema de validación de credenciales utilizando estándares de seguridad como JWT.
- Facilitar el acceso a la plataforma basado en los roles asignados al usuario al registrarse.

![image](https://github.com/user-attachments/assets/61f21441-6d10-4bd4-aa29-5d5b3f754267)


**Candidate para Bounded Context: Monitoring**
Este contexto se enfoca en permitir a los comerciantes realizar transacciones dentro de la plataforma, específicamente la compra y venta de cultivos. Está centrado en garantizar que los procesos comerciales fluyan de manera eficiente entre los comerciantes y agricultores.

Posibles responsabilidades del Bounded Context:
- Gestionar la publicación de cultivos en venta y asegurar que sean visibles para otros usuarios de acuerdo a las políticas definidas.
- Administrar la compra y calificación de cultivos, asegurando la satisfacción del usuario y la validez de las transacciones.
- Enviar notificaciones automáticas a través de servicios de mensajería para mantener a los usuarios informados sobre sus cultivos, compras y calificaciones.
- Aplicar las políticas comerciales que rigen las interacciones entre comerciantes y agricultores.

![image](https://github.com/user-attachments/assets/b8891ce5-86e1-4940-897a-d47a3d8991dd)


**Candidate para Bounded Context: Shopping**

Este contexto se centra en las operaciones que permiten a los comerciantes interactuar con los cultivos que publican los agricultores, asegurando que los procesos de compra, venta y calificación de los cultivos se realicen de manera efectiva.

Responsabilidades del Bounded Context:
- Publicación y gestión de la lista de cultivos en venta.
- Facilitar el proceso de compra de cultivos asegurando la seguridad y fiabilidad de la transacción.
- Gestionar las calificaciones de los productos comprados, incentivando la transparencia y confianza en la plataforma.
- Notificaciones automáticas a través de servicios como EmailJS para informar a los agricultores sobre las actividades comerciales que afectan a sus productos.

![image](https://github.com/user-attachments/assets/41776ae9-5f3c-417b-9c52-2b9a9c75e5af)



**Candidate para Bounded Context: Planification**

Este contexto se centra en las operaciones que permiten a los agricultores planificar y gestionar sus cultivos, asegurando que los procesos de creación y edición de los planes de cultivo se realicen de manera efectiva.

Responsabilidades del Bounded Context:

- Permitir la creación de nuevos planes de cultivo por parte de los agricultores.
- Facilitar la edición de los planes de cultivo ya existentes, asegurando que los detalles puedan ser actualizados de forma eficiente.
- Validar la información ingresada para asegurar que los planes de cultivo estén completos y listos para su ejecución.
- Informar a los agricultores sobre el éxito o los posibles problemas en la creación y edición de los planes mediante mensajes claros y acciones correctivas, si es necesario.



![image](https://github.com/user-attachments/assets/160156bf-ad75-421b-a5b2-2a99aa1c92a9)


**Candidate para Bounded Context: Crop registration**
Este contexto se centra en las operaciones que permiten a los agricultores registrar nuevos cultivos en el sistema, asegurando que los cultivos se agreguen correctamente a la lista de cultivos disponibles.

Responsabilidades del Bounded Context:

- Permitir a los agricultores registrar nuevos cultivos en la plataforma.
- Almacenar los datos de los cultivos registrados de manera eficiente y confiable.
- Añadir el nuevo cultivo a la lista de cultivos disponibles para su posterior gestión.
- Ofrecer la opción de vincular el cultivo registrado con un plan de cultivo para su seguimiento y planificación.

![image](https://github.com/user-attachments/assets/a4483053-af9e-43b3-99f1-2644ed05a945)


Vista completa:
![Event Storming - Copy of Step 10_ Bounded Contexts (1)](https://github.com/user-attachments/assets/c097c48f-d683-4eef-bb09-747871a5ffd2)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 


### 4.1.1.2 Domain Message Flows Modeling
**Usuario**
Scenario: El usuario desea iniciar sesión

Explicación del proceso:

- **Identificación de Actores:** Se comienza por identificar al usuario como el principal actor en este flujo de inicio de sesión. El sistema de autenticación (IAM) también es un actor clave que interactúa con los datos del usuario.


**Definición de los eventos y mensajes clave:**

- Ingreso de datos: El usuario ingresa sus credenciales (ID, email, password, role) en el sistema.
- Envío de datos: Una vez ingresados, los datos se envían al sistema para su procesamiento.
- Autenticación y validación de datos: Los datos son enviados al servicio de autenticación IAM, que valida la información (username y password).
- Confirmación de autenticación: Tras la validación, IAM devuelve los datos autenticados si el proceso es exitoso.

**Visualización del flujo:**
- Se representa el flujo de mensajes entre el usuario, la aplicación web o móvil y el sistema IAM.
- Cada paso en el proceso de inicio de sesión está acompañado de los datos clave involucrados en cada interacción.

Explicación del escenario:

El diagrama modela el proceso de inicio de sesión en una aplicación web o móvil, describiendo las interacciones y mensajes que se intercambian entre los distintos componentes del sistema.

- El usuario ingresa sus credenciales: Esto incluye el nombre de usuario, correo electrónico, contraseña y rol.

- Los datos son enviados al sistema de inicio de sesión: El sistema procesa los datos ingresados y los envía al servicio de autenticación IAM.

- Autenticación de los datos: El servicio IAM recibe las credenciales y las valida. Si la información es correcta, se autentican los datos.

- Validación y retorno de información autenticada: Una vez validados los datos, el sistema de autenticación devuelve una respuesta que indica si el usuario fue autenticado correctamente. Estos datos autenticados contienen la información relevante (ID, username, password y rol) que permite al usuario acceder a la aplicación.

![image](https://github.com/user-attachments/assets/c3b7edd2-10e6-4a3d-9477-a312e1e5f9bd)

**Agricultor**
Scenario: Agricultor desea crear un cultivo

Explicación del proceso:

**Actor Principal (Agricultor):**

- El agricultor es quien interactúa con la aplicación web/móvil. El actor es representado en el diagrama como el punto de inicio del proceso.

**Acción Inicial (Crear Cultivo):**

- El agricultor inicia el proceso seleccionando la opción "Crear cultivo" en la interfaz de la aplicación. Esta acción es la primera interacción que desencadena el flujo de mensajes.
- El agricultor puede visualizar un formulario para ingresar los detalles del cultivo.
Llenado de Datos del Cultivo:

**El agricultor proporciona los datos requeridos para el registro de su cultivo.** 
Estos pueden incluir:

- Nombre del cultivo.
- Información sobre pesticidas o fertilizantes utilizados.
- Días de riego, entre otros datos necesarios para la administración del cultivo.
- Este paso se refleja en el segundo bloque del diagrama (2. Llenar datos del cultivo).

**Proceso Interno en la Aplicación (Crop Registration):**

- Una vez que los datos son ingresados, la aplicación web/móvil se comunica con un sistema de backend (representado por "Crop registration"). Este sistema valida y procesa la información proporcionada por el agricultor.
- En esta etapa, se registra el cultivo en la base de datos, verificando que toda la información sea correcta.

**Confirmación (Cultivo Creado):**

- La aplicación confirma al agricultor que el cultivo ha sido creado con éxito, proporcionando un mensaje o actualización visual (Paso 3. Cultivos creados). El sistema puede devolver una lista de cultivos registrados, que el agricultor podrá revisar o actualizar en el futuro.

**Listar Cultivos Registrados:**

- El agricultor finalmente puede visualizar el cultivo recién registrado en la Página de lista de cultivos. Este es el último paso en el proceso donde el agricultor ve el resultado de la operación iniciada.

![image](https://github.com/user-attachments/assets/bfb1c762-d1a9-4f44-9656-68eb8c5be836)


**Comerciante**
Scenario: Comerciante desea comprar un cultivo

Explicación de proceso:
El comerciante es el usuario que inicia el proceso. Su objetivo es comprar un cultivo disponible en la plataforma.

- **Buscar cultivos en venta:**
El comerciante utiliza la aplicación web o móvil para buscar cultivos disponibles para la compra. El sistema le devuelve una lista de cultivos (identificados por id, products, merchantId).

- **Elegir cultivo:**
El comerciante selecciona uno de los cultivos listados. Este paso podría involucrar mostrar información detallada sobre el cultivo seleccionado, como precios y características.

- **Pagar el cultivo:**
Tras seleccionar un cultivo, el comerciante procede a realizar el pago. La aplicación toma los detalles del cultivo seleccionado y los datos del comerciante para procesar la compra.

- **Enviar datos del pago:**
Los datos del cultivo y del comerciante se envían a un servicio externo de pago, representado en el diagrama como "Shopping". Esta interacción representa la comunicación entre la aplicación y un sistema externo encargado de procesar la transacción.

- **Confirmación de pago realizado:**
El sistema de pago confirma que la transacción ha sido completada exitosamente y notifica tanto al sistema como al comerciante. El diagrama lo representa como el evento "Pago realizado".

- **Confirmación visual del pago:**
Finalmente, el comerciante recibe una confirmación en la aplicación, donde puede ver los detalles de la transacción completada (id, date, image_url, unit_price, name). Esta es una confirmación visual dentro de la plataforma que asegura al comerciante que el proceso se completó correctamente.


![image](https://github.com/user-attachments/assets/7533142b-6314-4f14-8302-cd6a376d46d8)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 

### 4.1.1.3 Bounded Context Canvases

En esta sección, se detallan los criterios considerados en cada Bounded Context Canvases, herramienta que sirve para diseñar y documentar un solo bounded context, el proceso de diseño de cada uno se basó en la importancia que tiene para la solución IOT.

**Crop Registration:**

Explicación de diseño:

El diseño del bounded context se fundamenta en las interacciones esenciales para el agricultor. La funcionalidad central se centra en permitir el registro de cultivos y su posterior monitoreo, lo cual es un proceso fundamental para la plataforma Ayni. Las decisiones de diseño están alineadas con mantener este proceso eficiente y asegurarse de que los datos críticos se gestionen correctamente.

La implementación como custom build asegura que el contexto esté profundamente adaptado a las necesidades específicas del negocio agrícola, mientras que el rol de compliance enforcer garantiza que los usuarios cumplan con las reglas definidas para la gestión de cultivos.

1. **Propósito (Purpose)**:
   El objetivo principal del contexto es la **funcionalidad de registro y edición de cultivos** y sus detalles, proporcionando a los agricultores la capacidad de crear y mantener información sobre sus cultivos dentro de la plataforma.

2. **Clasificación Estratégica (Strategic Classification)**:
   - **Dominio:** El contexto es parte del dominio **Core** ya que el registro de cultivos es esencial para el modelo de negocio de la plataforma agrícola.
   - **Modelo de Negocio:** Actúa como un **compliance enforcer** ya que asegura que los cultivos cumplan con las políticas y regulaciones internas.
   - **Evolución:** La solución se clasifica como **custom build**, lo que significa que ha sido diseñada específicamente para ajustarse a los requisitos del negocio, personalizando el proceso de registro de cultivos.

3. **Roles del Dominio (Domain Roles)**:
   El tipo de rol que este contexto juega es **Execution Context**, donde los usuarios interactúan directamente con el sistema para completar sus tareas de registro y edición de cultivos.

4. **Comunicación Entrante (Inbound Communication)**:
   - El principal colaborador es el **agricultor**, quien interactúa con el sistema enviando solicitudes para registrar nuevos cultivos o modificar los existentes.
   - Mensajes clave incluyen: 
     - **Crop register request**
     - **Post crop**
     - **Form sent**

5. **Comunicación Saliente (Outbound Communication)**:
   - El sistema responde confirmando las acciones tomadas por el agricultor con mensajes como:
     - **Crop confirmed**
     - **Details confirmed**
     - Además de mensajes que permiten visualizar los cultivos registrados: **Show crop** y **Show details**.
   - Esta información es enviada al **Frontend**, lo que facilita la interacción con el usuario final.

6. **Lenguaje Ubicuo (Ubiquitous Language)**:
   - Definición clara de los términos dentro del dominio:
     - **Crop:** Objeto que se crea cuando el usuario registra un cultivo.
     - **Product Details:** Son los detalles del cultivo cuando se publica una venta.
     - **Crop Details:** Son los detalles específicos del cultivo como tipo de planta, tiempo de vida, etc.

7. **Decisiones de Negocio (Business Decisions)**:
   - Algunas de las reglas claves de negocio incluyen:
     - Un usuario con un ID único puede ver solo sus propios cultivos.
     - Solo el usuario agricultor puede crear, ver y editar cultivos.

8. **Suposiciones (Assumptions)**:
   - Los usuarios agricultores deben crear un cultivo para luego hacer una planificación.
   - Los usuarios pueden publicar productos en venta siempre y cuando tengan una planificación.
   - Los usuarios pueden crear varios cultivos.

9. **Métricas de Verificación (Verification Metrics)**:
   - El principal criterio de éxito es la **cantidad de cultivos creados en la plataforma**, que servirá para medir el uso y efectividad del sistema.


![image](https://github.com/user-attachments/assets/c1605e83-dc86-437a-9b94-ace570e8d4af)

---

**Planification:**

El diseño del bounded context se enfoca en ofrecer una solución personalizada para la planificación agrícola. Al ser parte del dominio Core, el éxito del negocio depende directamente de la capacidad de los agricultores para planificar sus cultivos. La personalización (custom build) de esta solución permite una adaptación a las necesidades agrícolas, y el sistema asegura el cumplimiento de las reglas establecidas. La interacción con el frontend facilita una experiencia fluida para los agricultores al gestionar sus planes.

1. **Propósito (Purpose)**:
   El contexto está diseñado para manejar la **funcionalidad de planificación de cultivos**, permitiendo a los agricultores crear planes detallados relacionados con el manejo de sus cultivos, estableciendo acciones y plazos para optimizar la producción.

2. **Clasificación Estratégica (Strategic Classification)**:
   - **Dominio:** El contexto es parte del dominio **Core** ya que la planificación es crucial para el éxito de la gestión de cultivos.
   - **Modelo de Negocio:** Funciona como un **compliance enforcer** asegurando que los planes de cultivo cumplan con los estándares establecidos.
   - **Evolución:** Clasificado como **custom build** porque la planificación de cultivos está adaptada a las necesidades específicas del negocio agrícola.
  
3. **Roles del Dominio (Domain Roles)**:
   El contexto actúa bajo el rol de **Execution Context**, donde los agricultores interactúan directamente con el sistema para establecer y gestionar planes para sus cultivos.

4. **Comunicación Entrante (Inbound Communication)**:
   - El principal colaborador es el **agricultor**, quien envía solicitudes para crear o editar planes de cultivo.
   - Los mensajes clave son:
     - **Planification request**
     - **Post plans**
     - **Form sent**

5. **Comunicación Saliente (Outbound Communication)**:
   - El sistema responde confirmando la creación o modificación de planes con mensajes como:
     - **Plan confirmed**
     - **Crop confirmed**
     - También se incluye la visualización de los planes: **Show plan**
   - Esta información es enviada al **Frontend**, donde los usuarios pueden ver y gestionar sus planes de cultivo.

6. **Lenguaje Ubicuo (Ubiquitous Language)**:
   - Se define un lenguaje claro dentro del dominio:
     - **Planification:** Es el proceso de planificación relacionada a los cultivos.
     - **Schedule:** Rango de días en los que se realizarán las acciones relacionadas con los cultivos.

7. **Decisiones de Negocio (Business Decisions)**:
   - Algunas reglas de negocio importantes son:
     - Solo el usuario agricultor puede crear planificaciones para sus cultivos.
     - Solo se puede hacer un plan con un cultivo existente.

8. **Suposiciones (Assumptions)**:
   - Los planes admiten distintos detalles del cultivo.
   - Los planes deben ser la base de funcionamiento de los sensores y actuadores en la plataforma.

9. **Métricas de Verificación (Verification Metrics)**:
   - El éxito del contexto se medirá por la **cantidad de planes realizados en la plataforma**, asegurando que los usuarios están utilizando la funcionalidad de planificación de manera efectiva.

![image](https://github.com/user-attachments/assets/595a98dc-25ad-496b-81b3-0a33c834b936)

---

**Monitoring:**

El diseño del bounded context de Monitoring se enfoca en el seguimiento continuo y en tiempo real de los cultivos, asegurando que el agricultor pueda reaccionar rápidamente a cualquier cambio en las condiciones del cultivo. Al ser parte del dominio Core, su rol es vital en la gestión agrícola. El sistema facilita la integración con sensores y actuadores, mientras que el Frontend provee al agricultor con información crítica y fácil de interpretar para tomar decisiones en el momento adecuado.

1. **Propósito (Purpose)**:
   El contexto está diseñado para manejar la **funcionalidad de control, planificación y registro de cultivos**, permitiendo monitorear y registrar información de los cultivos a través de sensores y actuadores.

2. **Clasificación Estratégica (Strategic Classification)**:
   - **Dominio:** Este contexto pertenece al dominio **Core**, ya que el monitoreo en tiempo real es crucial para la efectividad del sistema de gestión de cultivos.
   - **Modelo de Negocio:** Funciona como un **compliance enforcer**, garantizando que las acciones de monitoreo y control se realicen siguiendo los procedimientos predefinidos.
   - **Evolución:** Es clasificado como **custom build** debido a la necesidad de personalización según las características y requisitos de los cultivos en diferentes situaciones.

3. **Roles del Dominio (Domain Roles)**:
   Este contexto actúa en el rol de **Execution Context**, donde se ejecuta el monitoreo constante y se reportan los estados de los sensores y actuadores al sistema y al usuario.

4. **Comunicación Entrante (Inbound Communication)**:
   - El **agricultor** es el colaborador clave que solicita información del dashboard.
   - Los mensajes principales son:
     - **Watch dashboard request**
     - **Get information from sensors**
     - **Form sent**

5. **Comunicación Saliente (Outbound Communication)**:
   - El sistema responde enviando la información monitoreada a través de mensajes como:
     - **Information obtained**
     - **New dashboard confirmed**
     - Además de la visualización de la información en el dashboard con **Show Dashboard**.
   - Estos datos se presentan en el **Frontend** para facilitar la interpretación y acción por parte del usuario.

6. **Lenguaje Ubicuo (Ubiquitous Language)**:
   - **Sensor:** Dispositivo que monitorea y controla diferentes aspectos del negocio, en este caso los terrenos de cultivo.
   - **Actuator:** Dispositivo encargado de ejecutar tareas con base en condiciones establecidas.
   - **Base plan:** Los sensores y actuadores trabajan según el plan creado previamente por el agricultor.

7. **Decisiones de Negocio (Business Decisions)**:
   - Reglas importantes dentro de este contexto incluyen:
     - Solo el usuario agricultor puede crear cultivos y planificaciones.
     - Los sensores y actuadores responden a las acciones predeterminadas del plan.

8. **Suposiciones (Assumptions)**:
   - Los sensores deben estar conectados a un dispositivo central que enviará la información a la plataforma.
   - Los sensores y actuadores serán codificados en una **Edge API IoT** para facilitar la integración con la plataforma.

9. **Métricas de Verificación (Verification Metrics)**:
   - El éxito del sistema se medirá por la **cantidad de notificaciones de sensores recibidas**, asegurando que los datos son monitoreados correctamente y reportados al agricultor a través del dashboard.


![image](https://github.com/user-attachments/assets/0f9bb4f0-5a3d-47a1-b81f-53b5cc6896c7)

---

**Shopping:**

ElBounded Context Canvas presentado se enfoca en el contexto de un sistema de "compra y venta de cultivos", donde se analizan distintos aspectos clave para el diseño del dominio.

1. **Propósito (Purpose)**:
   El contexto está diseñado para manejar la **funcionalidad de compra y venta de cultivos**, cubriendo las necesidades de ambos segmentos: vendedores y compradores de cultivos.

2. **Clasificación Estratégica (Strategic Classification)**:
   - **Dominio:** Este contexto pertenece al dominio **Core**, ya que la compra y venta de cultivos es una parte esencial del negocio.
   - **Modelo de Negocio:** Funciona como un **compliance enforcer**, garantizando que las transacciones de compra y venta se realicen conforme a las normativas del negocio.
   - **Evolución:** Se clasifica como **custom build**, debido a la necesidad de personalizar el sistema según las necesidades específicas de los usuarios en el mercado de cultivos.

3. **Roles del Dominio (Domain Roles)**:
   Este contexto actúa en el rol de **Execution Context**, manejando la ejecución de las transacciones de compra y venta de cultivos entre los usuarios, tanto vendedores como compradores.

4. **Comunicación Entrante (Inbound Communication)**:
   - El **comerciante** es el colaborador clave que interactúa con el sistema.
   - Los mensajes principales que envía son:
     - **Pay attendance**: Confirmación de pago.
     - **Post sales**: Publicación de ventas.
     - **Form sent**: Formulario enviado.
     - **Rate attendance**: Valoración de asistencia.
     - **Post rate**: Publicación de calificación.

5. **Comunicación Saliente (Outbound Communication)**:
   - El sistema responde enviando mensajes tanto al colaborador clave como al **Frontend**. Algunos mensajes clave son:
     - **Rate confirmed**: Confirmación de la valoración.
     - **Payment confirmed**: Confirmación del pago.
     - **Show confirmation**: Mostrar confirmación al usuario.
     - **Show rates**: Mostrar las calificaciones de los productos o ventas.

6. **Lenguaje Ubicuo (Ubiquitous Language)**:
   - **Producto:** Cultivo que se ofrece para la venta.
   - **Ventas:** La transacción de venta vinculada al producto.
   - **Orden:** La orden finalizada asociada a una venta concreta.

7. **Decisiones de Negocio (Business Decisions)**:
   - Reglas importantes dentro de este contexto incluyen:
     - Un usuario puede tener varias ventas publicadas.
     - Cada venta está vinculada a un producto específico.
     - Cada orden corresponde a una transacción finalizada.

8. **Suposiciones (Assumptions)**:
   - Los usuarios son libres de elegir qué productos comprar.
   - Deben realizar un pago a través de una pasarela para concretar la compra.
   - Los cultivos que se muestran deben ser publicados primero por los agricultores.

9. **Métricas de Verificación (Verification Metrics)**:
   - Cantidad de usuarios que realizan una venta al día.
   - Cantidad de usuarios que publican cultivos a la venta diariamente.


![image](https://github.com/user-attachments/assets/3af24e41-68bf-4e32-a92b-7c23cf036600)

---

**IAM:**

1. **Propósito (Purpose)**:
   Este contexto está diseñado para manejar la **autenticación de usuarios** según su tipo de cuenta. Los usuarios pueden crear un perfil, registrarse en la plataforma y autenticarse.

2. **Clasificación Estratégica (Strategic Classification)**:
   - **Dominio:** Este contexto pertenece al dominio **Generic**, ya que la autenticación de usuarios es una funcionalidad estándar en muchas plataformas.
   - **Modelo de Negocio:** Funciona como un **compliance enforcer**, asegurando que el proceso de autenticación y registro de usuarios siga las normativas y procedimientos definidos.
   - **Evolución:** Se clasifica como **Commodity**, ya que es una funcionalidad comúnmente implementada en plataformas y no requiere un desarrollo altamente personalizado.

3. **Roles del Dominio (Domain Roles)**:
   Este contexto actúa como un **Execution Context**, donde se maneja la validación de las credenciales de los usuarios y la creación de cuentas.

4. **Comunicación Entrante (Inbound Communication)**:
   - El colaborador clave es el **Usuario**, quien interactúa con el sistema enviando los siguientes mensajes:
     - **Log In**: Inicio de sesión mediante credenciales.
     - **Sign In**: Registro de usuario.
     - **Post Account Info**: Envío de la información de la cuenta.
     - **Form Sent**: Formulario enviado con los datos del usuario.

5. **Comunicación Saliente (Outbound Communication)**:
   - El sistema responde enviando mensajes al **Frontend** y a otros colaboradores como el **IAM**:
     - **User validation**: Validación del usuario.
     - **Get credentials info**: Obtención de las credenciales del usuario.
     - **Account created**: Confirmación de la creación de la cuenta.
     - **Account logged**: Confirmación del inicio de sesión.
     - **Data saved**: Datos guardados exitosamente.

6. **Lenguaje Ubicuo (Ubiquitous Language)**:
   - **Log In:** El proceso de ingresar credenciales (correo electrónico y contraseña) para acceder al sistema.
   - **Sign Up:** El proceso de registrar una nueva cuenta, incluyendo la creación de credenciales.
   - **Account:** El perfil o cuenta de un usuario, que contiene su información personal.
   - **Validation:** Proceso de verificación de las credenciales para asegurar que sean correctas.

7. **Decisiones de Negocio (Business Decisions)**:
   - Las reglas importantes dentro de este contexto incluyen:
     - Cada cuenta debe estar vinculada a un único usuario.
     - Los datos de la cuenta se deben guardar correctamente para permitir la autenticación futura.

8. **Suposiciones (Assumptions)**:
   - Lo primero que debe hacer el usuario para utilizar la plataforma es iniciar sesión (Log In) o registrarse (Sign Up).
   - La plataforma debe almacenar los datos del usuario y la autenticación se realiza mediante correo electrónico y contraseña.

9. **Métricas de Verificación (Verification Metrics)**:
   - Cantidad de usuarios que ingresan a la app diariamente.

![image](https://github.com/user-attachments/assets/f3c625c1-2a38-4091-a9da-718c705b2004)

Link de Miro: https://miro.com/welcomeonboard/YkswaDJnVWNVWVpaZlQ0cXQ2Y3FUR0hTTlBmMW1BUWNUTzBRa0tqTG1kOXlEaGRvbFJ5UmpuTmNzdWk1VE4xNHwzMDc0NDU3MzU3NDk3MzU0NjE5fDI=?share_link_id=387833456347 



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

![image](https://github.com/user-attachments/assets/a7e1193e-88b7-4311-b5d3-bc6fffb9026b)


### 4.1.3.2. Software Architecture Context Level Diagrams

En la siguiente imagen se aprecia 2 usuarios que interactúan con el sistema, "Farmer" y "Merchant" son el segmetno objetivo. Además existe una dependencia a un sistema externo, EmailJS.

![image](https://github.com/user-attachments/assets/c1950481-9795-4402-b339-bf2ed0c58f69)



### 4.1.3.2. Software Architecture Container Level Diagrams


El diagrama de contexto muestra un sistema de monitoreo y compra/venta de cultivos llamado Ayni, donde interactúan dos tipos de usuarios: Merchant (comerciante) y Farmer (agricultor). El Merchant puede realizar compras de cultivos de calidad, mientras que el Farmer se encarga de gestionar y mejorar sus cultivos.

El Farmer utiliza diferentes interfaces para interactuar con el sistema, tales como una Landing Page (hecha en HTML/CSS), una Aplicación Móvil (con Flutter/Dart) y una Aplicación Web. Estas interfaces le permiten crear, monitorear y publicar cultivos. El Merchant accede principalmente a través de una Web App (Java y Spring MVC) y una Aplicación de Página Única (con JavaScript y Angular), que le permiten visualizar cultivos y realizar compras.

El sistema se soporta en varias capas de infraestructura tecnológica. Hay una Aplicación Web API (con SpringBoot Java) que actúa como intermediaria entre las aplicaciones de usuario y otras capas del sistema. Esta aplicación maneja llamadas API que son procesadas por una Aplicación de Edge API (también en SpringBoot), que a su vez se comunica con una base de datos MySQL. También existe una Aplicación IoT embebida (en C++) que procesa información desde dispositivos IoT y la envía al resto del sistema.

Adicionalmente, el sistema se conecta a servicios externos como Email JS (para mensajería) y Niubiz (para pasarela de pago).

En resumen, el diagrama representa un sistema distribuido que integra diferentes interfaces y tecnologías para monitorear y comercializar cultivos, con soporte para pagos y notificaciones.

![image](https://github.com/user-attachments/assets/751fc70f-c1b5-4a7d-ab07-083875a1b004)




### 4.1.3.3. Software Architecture Deployment Diagrams

El diagrama describe el despliegue de un sistema distribuido, que incluye diferentes aplicaciones front-end, back-end y bases de datos, organizadas según sus nodos de despliegue. Los componentes principales son:

Aplicación Móvil (Flutter/Dart): Se despliega en el dispositivo móvil del cliente (ya sea iOS o Android). La aplicación hace llamadas API (JSON/HTTP) para interactuar con el backend.

Aplicación de Página Única (JavaScript/Angular): Ejecutada en el navegador web del cliente (Chrome, Firefox, Safari, Edge), también realiza llamadas API (JSON/HTTP) para conectarse con el sistema.

Aplicación Web (Java y Spring MVC): Desplegada en Netlify, sirve a los clientes a través del navegador, entregando contenido web.

Aplicación Web API (SpringBoot Java): Desplegada en Zeabur, actúa como intermediario entre las aplicaciones de cliente (móvil y web) y la base de datos. Esta aplicación realiza lecturas y escrituras a la base de datos mediante protocolos SQL/TCP.

Aplicación Embebida IoT (C++): Desplegada en Cloud Azure, procesa y envía información relevante al sistema a través de las API.

Aplicación Edge API (SpringBoot): También desplegada en Cloud Azure, esta aplicación recibe información de la aplicación IoT y la envía a la base de datos mediante llamadas SQL.

Bases de Datos MySQL: Existen dos bases de datos principales. Una es la base de datos central que maneja la Web API, y la otra es una base de datos para la Edge API. Ambas están desplegadas en Railway y usan MySQL para almacenar y recuperar datos mediante conexiones SQL.

Este diagrama ilustra la arquitectura distribuida del sistema, donde diferentes componentes están desplegados en nodos en la nube (Netlify, Zeabur, Azure, Railway) y se comunican entre sí utilizando APIs y protocolos SQL, manteniendo la interoperabilidad entre las aplicaciones cliente y las bases de datos backend.

![image](https://github.com/user-attachments/assets/1e05d0a9-5a3b-4016-b43f-ec71a56d6e66)




# 4.2. Tactical-Level Domain-Driven Design
## 4.2.1. Bounded Context: IAM
### 4.2.1.1. Domain Layer

La capa de dominio es el núcleo de la aplicación, donde residen las reglas de negocio y los modelos esenciales que definen la lógica del sistema. En este caso, el Aggregate "User" representa la entidad principal que define a los usuarios del sistema, incluidas sus propiedades y métodos. Esta capa se asegura de que los conceptos empresariales y sus interacciones estén correctamente modelados y encapsulados. 

Propósito: Modelar las entidades del negocio, incluyendo atributos y comportamientos necesarios para representar de forma fiel los conceptos de la aplicación, como usuarios, productos, transacciones, etc.

| **Aggregate**: `User`                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa el agregado raíz "Usuario", que contiene los datos de la cuenta y su rol. Se mapea a la tabla `users` en la base de datos.|

| **Atributo**                      | **Tipo**                | **Descripción**                                                   |
|-----------------------------------|-------------------------|-------------------------------------------------------------------|
| `id`                              | `Long`                  | Identificador único del usuario (autogenerado).                   |
| `username`                        | `Username` (Value Object) | Nombre de usuario (Valor embebido).                               |
| `email`                           | `EmailAddress` (Value Object) | Dirección de correo electrónico (Valor embebido).                  |
| `password`                        | `Password` (Value Object) | Contraseña del usuario (Valor embebido).                          |
| `role`                            | `Role` (Value Object)   | Rol del usuario (Valor embebido).                                 |
| `createdAt`                       | `Date`                  | Fecha de creación del usuario (no modificable).                   |
| `updatedAt`                       | `Date`                  | Fecha de la última actualización del usuario.                     |

| **Método**                        | **Descripción**                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------|
| `getId()`                         | Retorna el `id` del usuario.                                                                      |
| `getUsername()`                   | Retorna el `username` del usuario (valor embebido).                                                |
| `getEmail()`                      | Retorna el `email` del usuario (valor embebido).                                                   |
| `getPassword()`                   | Retorna el `password` del usuario (valor embebido).                                                |
| `getRoles()`                      | Retorna los `roles` asociados al usuario (actualmente solo uno).                                   |

| **Value Object**: `EmailAddress`                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa una dirección de correo electrónico válida como un objeto de valor embebido.                   |

| **Atributo**                     | **Tipo**                | **Descripción**                                                   |
|----------------------------------|-------------------------|-------------------------------------------------------------------|
| `email`                          | `String`                | Dirección de correo electrónico validada (no en blanco, máximo 50 caracteres, formato válido de correo). |

| **Método**                       | **Descripción**                                                                                   |
|----------------------------------|---------------------------------------------------------------------------------------------------|
| `EmailAddress(String email)`     | Constructor que recibe un correo electrónico y lo valida según las restricciones.                  |
| `EmailAddress()`                 | Constructor por defecto que inicializa con `null`.                                                 |
| `email()`                        | Retorna la dirección de correo electrónico encapsulada en este Value Object.                       |

| **Value Object**: `Password`                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa una contraseña válida como un objeto de valor embebido, encapsulando y validando su longitud.  |

| **Atributo**                     | **Tipo**                | **Descripción**                                                   |
|----------------------------------|-------------------------|-------------------------------------------------------------------|
| `password`                       | `String`                | Contraseña del usuario (no en blanco, máximo 120 caracteres).      |

| **Método**                       | **Descripción**                                                                                   |
|----------------------------------|---------------------------------------------------------------------------------------------------|
| `Password(String password)`      | Constructor que recibe una contraseña y la valida según las restricciones.                        |
| `Password()`                     | Constructor por defecto que inicializa con `null`.                                                 |
| `password()`                     | Retorna la contraseña encapsulada en este Value Object.                                            |

| **Value Object**: `Role`                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa el rol de un usuario como un objeto de valor embebido, encapsulando un rol específico.         |

| **Atributo**                     | **Tipo**                | **Descripción**                                                   |
|----------------------------------|-------------------------|-------------------------------------------------------------------|
| `role`                           | `ERole`                 | Rol del usuario, puede ser `ROLE_FARMER` o `ROLE_MERCHANT`.        |

| **Método**                       | **Descripción**                                                                                   |
|----------------------------------|---------------------------------------------------------------------------------------------------|
| `Role(String role)`              | Constructor que recibe un string y asigna un rol basado en el valor (`farmer` o `merchant`).       |
| `Role()`                         | Constructor por defecto que no asigna ningún rol.                                                  |
| `getRole()`                      | Retorna el valor del rol encapsulado.                                                             |


### 4.2.1.2. Interface Layer

Esta capa actúa como un punto de entrada para la interacción entre los usuarios del sistema y los servicios que se ofrecen. Los controladores (Controllers) son los componentes clave de esta capa, que gestionan las solicitudes entrantes y devuelven las respuestas adecuadas. En este caso, los controladores de autenticación y de usuarios gestionan el flujo de autenticación y el acceso a los recursos de usuario.

Propósito: Exponer los endpoints (APIs) para que los usuarios o sistemas interactúen con la lógica del negocio. Esta capa no contiene lógica de negocio, sino que se centra en orquestar las llamadas a servicios o a la capa de dominio.

| **Controlador**: `AuthController`                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que maneja los endpoints relacionados con la autenticación de usuarios.                  |

| **Método**              | **Ruta**                  | **Descripción**                                                                                                                                                      |
|-------------------------|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `authenticateUser`      | `POST /api/v1/auth/signin` | Maneja la autenticación de usuarios. Toma un objeto `SignInResource` del cuerpo de la solicitud, lo convierte en un comando, y llama al servicio de comandos para autenticar al usuario. Si la autenticación es exitosa, devuelve un recurso de usuario autenticado. Si falla, retorna un error 404. |
| `registerUser`          | `POST /api/v1/auth/signup` | Maneja el registro de nuevos usuarios. Recibe un objeto `SignUpResource`, lo convierte en un comando, y llama al servicio de comandos para registrar al usuario. Si el registro es exitoso, recupera los datos del usuario y devuelve un recurso de usuario. Si hay un error, retorna un error 400.      |

| **Dependencias**                            | **Descripción**                                                                                  |
|---------------------------------------------|--------------------------------------------------------------------------------------------------|
| `UserQueryService`                          | Servicio encargado de manejar las consultas relacionadas con usuarios.                          |
| `UserCommandService`                        | Servicio encargado de manejar los comandos relacionados con la creación y autenticación de usuarios. |
| `SignInCommandFromResourceAssembler`       | Utilidad para convertir el recurso de inicio de sesión en un comando.                          |
| `SignUpCommandFromResourceAssembler`       | Utilidad para convertir el recurso de registro en un comando.                                   |
| `AuthenticatedUserResourceFromEntityAssembler` | Utilidad para convertir el usuario autenticado en un recurso.                                  |
| `UserResourceFromEntityAssembler`          | Utilidad para convertir el usuario registrado en un recurso.                                     |

| **Controlador**: `UsersController`                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que maneja los endpoints relacionados con la gestión de usuarios.                        |

| **Método**                | **Ruta**                           | **Descripción**                                                                                                                                                  |
|---------------------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `getAllUsers`            | `GET /api/v1/users`                | Maneja la solicitud para obtener todos los usuarios. Llama al servicio de consultas, obtiene la lista de usuarios y la convierte en recursos para la respuesta. Devuelve una lista de recursos de usuarios. |
| `getUserById`            | `GET /api/v1/users/{userId}`      | Maneja la solicitud para obtener un usuario específico por su ID. Llama al servicio de consultas con el ID proporcionado. Si el usuario existe, lo convierte en un recurso y lo devuelve; si no, retorna un error 404. |

| **Dependencias**                            | **Descripción**                                                                                  |
|---------------------------------------------|--------------------------------------------------------------------------------------------------|
| `UserQueryService`                          | Servicio encargado de manejar las consultas relacionadas con usuarios.                          |
| `GetAllUsersQuery`                          | Consulta que se utiliza para obtener todos los usuarios.                                        |
| `GetUserByIdQuery`                          | Consulta que se utiliza para obtener un usuario específico por su ID.                          |
| `UserResourceFromEntityAssembler`           | Utilidad para convertir las entidades de usuario en recursos que se envían en la respuesta.     |


### 4.2.1.3. Application Layer

La capa de aplicación es responsable de coordinar las operaciones de negocio y ejecutar la lógica que controla el flujo de datos entre las capas de infraestructura y dominio. En esta capa residen los servicios que gestionan tanto los comandos como las consultas relacionadas con los usuarios, encapsulando las reglas de negocio en torno a estos procesos.

Propósito: Proveer los servicios que implementan la lógica de negocio aplicada, orquestando las interacciones entre el repositorio (capa de infraestructura) y las entidades del dominio. Aquí se realizan las validaciones de negocio y otras operaciones complejas antes de interactuar con la capa de dominio o infraestructura.

| **Servicio**: `UserCommandServiceImpl`                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio de comandos para la gestión de usuarios, incluyendo registro e inicio de sesión.  |

| **Método**                | **Descripción**                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handle(SignUpCommand)`   | Maneja el comando de registro de un nuevo usuario. Verifica la unicidad del nombre de usuario y del correo electrónico. Si todo es válido, crea un nuevo usuario y lo guarda en el repositorio, devolviendo su ID. |
| `handle(SignInCommand)`   | Maneja el comando de inicio de sesión. Busca al usuario por nombre de usuario. Verifica que el usuario existe y que la contraseña coincide. Si es válido, genera un token de autenticación y lo devuelve junto con el usuario. |

| **Dependencias**                            | **Descripción**                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `UserRepository`                            | Repositorio que maneja las operaciones de persistencia relacionadas con usuarios.                                    |
| `HashingService`                            | Servicio encargado de codificar y verificar contraseñas de usuarios.                                                |
| `TokenService`                              | Servicio que genera tokens de autenticación para usuarios.                                                           |
| `User`                                      | Agregado que representa al usuario en el sistema.                                                                   |
| `SignUpCommand`                            | Comando que encapsula la información necesaria para registrar un nuevo usuario.                                     |
| `SignInCommand`                            | Comando que encapsula la información necesaria para iniciar sesión con un usuario.                                  |

| **Servicio**: `UserQueryServiceImpl`                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio de consultas para la gestión de usuarios, permitiendo obtener información sobre usuarios registrados.  |

| **Método**                  | **Descripción**                                                                                                       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `handle(GetUserByUsernameQuery)` | Maneja el comando para obtener un usuario por su nombre de usuario. Devuelve un `Optional<User>` que puede estar vacío si no se encuentra el usuario. |
| `handle(GetUserByIdQuery)`       | Maneja el comando para obtener un usuario por su ID. Devuelve un `Optional<User>` que puede estar vacío si no se encuentra el usuario. |
| `handle(GetAllUsersQuery)`       | Maneja el comando para obtener todos los usuarios registrados en el sistema. Devuelve una lista de objetos `User`.  |

| **Dependencias**                          | **Descripción**                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `UserRepository`                          | Repositorio que maneja las operaciones de persistencia relacionadas con usuarios.                                      |
| `User`                                    | Agregado que representa al usuario en el sistema.                                                                     |
| `GetUserByUsernameQuery`                 | Consulta que encapsula la información necesaria para buscar un usuario por su nombre de usuario.                      |
| `GetUserByIdQuery`                       | Consulta que encapsula la información necesaria para buscar un usuario por su ID.                                     |
| `GetAllUsersQuery`                       | Consulta que encapsula la información necesaria para obtener todos los usuarios registrados.                          |


### 4.2.1.4. Infrastructure Layer

La capa de infraestructura se encarga de la interacción con fuentes externas de datos, como bases de datos, APIs de terceros, o cualquier recurso que esté fuera del ámbito de la lógica de negocio del sistema. En este caso, el UserRepository es el responsable de la persistencia de los datos del usuario, proporcionando métodos para validar la existencia de un usuario y buscar usuarios en la base de datos.

Propósito: Implementar la lógica de acceso a datos y garantizar que el sistema pueda interactuar con fuentes externas de forma eficiente. Esta capa contiene los repositorios que manejan la persistencia de las entidades del dominio.

| **Repositorio**: `UserRepository`                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Repositorio que maneja las operaciones de persistencia relacionadas con los usuarios en la base de datos.  |

| **Método**                               | **Descripción**                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `findByUsername(Username username)`      | Busca un usuario en la base de datos utilizando su nombre de usuario. Devuelve un `Optional<User>`.                |
| `findById(Long id)`                     | Busca un usuario en la base de datos utilizando su ID. Devuelve un `Optional<User>`.                              |
| `findAll()`                             | Devuelve una lista de todos los usuarios almacenados en la base de datos.                                         |
| `existsByUsername(Username username)`    | Verifica si un usuario con el nombre de usuario especificado ya existe en la base de datos. Devuelve un `boolean`. |
| `existsByEmail(EmailAddress email)`      | Verifica si un usuario con el correo electrónico especificado ya existe en la base de datos. Devuelve un `boolean`. |

| **Dependencias**                          | **Descripción**                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `User`                                    | Clase que representa al usuario en el sistema.                                                                      |
| `Username`                                | Valor de objeto que encapsula el nombre de usuario.                                                                 |
| `EmailAddress`                            | Valor de objeto que encapsula la dirección de correo electrónico del usuario.                                        |


### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams

El diagrama representa una arquitectura monolítica de una aplicación API llamada "Ayni". La aplicación está dividida en componentes que interactúan entre sí: una SPA que realiza llamadas API a controladores para gestionar autenticación y obtener datos de usuarios. Los controladores, como el Auth Controller y Users Controller, delegan las operaciones de comandos y consultas a servicios como UserCommandService y UserQueryService, que interactúan con el UserRepository. El repositorio gestiona el acceso a la base de datos MySQL, encargada de almacenar los datos de los usuarios.

![structurizr-85725-Componente (1)](https://github-production-user-asset-6210df.s3.amazonaws.com/104078975/285030967-60a9a7b9-f81b-42f7-9082-7b85c6f66481.png)


### 4.2.1.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.1.7.1. Bounded Context Domain Layer Class Diagrams

En el diagrama de clases perteneciente al bounded context IAM, se tiene como aggregate a User, el cual se conforma por atributos básicos como id (de tipo Long), email, password y username (de tipo String). Este agregado proporciona métodos como getUsername(), getEmail() y getPassword() para acceder a esos datos.

El agregado User se relaciona con dos interfaces: UserQueryService y UserCommandService. Estas interfaces abstraen las operaciones relacionadas con la consulta y los comandos sobre los usuarios. UserQueryService encapsula las consultas relacionadas con los usuarios, como la obtención de datos del usuario sin modificarlos. Por otro lado, UserCommandService está destinado a ejecutar acciones que modifican el estado del agregado, como actualizaciones o creación de usuarios.

![image](https://github.com/user-attachments/assets/f44e6f3b-e721-4b04-8a7b-e388ac9e3d23)



#### 4.2.1.7.2. Bounded Context Database Design Diagram


El diagrama de base de datos muestra dos tablas principales en el bounded context "Iam" (Identity and Access Management): users y roles, relacionadas por una clave foránea. La tabla users contiene campos como id (clave primaria), email, password, username (todos de tipo varchar(50)), y role_id (tipo bigint), que es una clave foránea que referencia la tabla roles. La tabla roles tiene los campos id (clave primaria) y name (de tipo varchar(30)) para definir diferentes roles de usuario. Esta estructura sugiere un sistema de autenticación y autorización donde cada usuario tiene un rol específico que determina sus permisos dentro del sistema.

![image](https://github.com/user-attachments/assets/71c76fb2-c063-42d8-a7be-0c6cd55fa1a3)


## 4.2.2. Bounded Context: Shopping
### 4.2.2.1. Domain Layer

Descripción: El Domain Layer es donde se define la lógica de negocio principal, encapsulando las reglas de negocio más importantes del sistema. Este nivel contiene las entidades y los agregados que representan objetos de dominio reales, y en este caso, la entidad principal es Order. Los agregados en esta capa permiten gestionar la consistencia y las operaciones de estas entidades.

Justificación: La entidad Order representa las órdenes de compra en el sistema. Contiene atributos como el identificador único, el cliente que ordena, el encargado que la acepta, descripción, cantidad, fecha de la orden, y el precio total. Los métodos como updateDate, end, y qualify proporcionan las operaciones esenciales para manejar el ciclo de vida de una orden, permitiendo actualizaciones de estado y la gestión del flujo de trabajo de las órdenes, como si están pendientes, calificadas o finalizadas.

| **Aggregate**: `Order`                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa la raíz del agregado de una orden en el sistema de compras, mapeando la tabla "orders".        |

| **Atributo**                     | **Tipo**                | **Descripción**                                                   |
|----------------------------------|-------------------------|-------------------------------------------------------------------|
| `id`                             | `Long`                  | Identificador único de la orden.                                  |
| `sale`                           | `Sale`                  | Relación con la entidad `Sale` a la que pertenece la orden.       |
| `orderedBy`                      | `Long`                  | ID del usuario que realizó la orden.                              |
| `acceptedBy`                     | `Long`                  | ID del usuario que aceptó la orden.                               |
| `description`                    | `String`                | Descripción detallada de la orden.                                |
| `quantity`                       | `Long`                  | Cantidad de productos solicitados en la orden.                    |
| `status`                         | `OrderStatus`           | Estado de la orden, utilizando un objeto de valor `OrderStatus`.  |
| `orderedDate`                    | `Date`                  | Fecha en la que se realizó la orden.                              |
| `totalPrice`                     | `Double`                | Precio total de la orden.                                         |
| `paymentMethod`                  | `String`                | Método de pago utilizado en la orden.                             |

| **Método**                       | **Descripción**                                                                             |
|----------------------------------|---------------------------------------------------------------------------------------------|
| `Order(...)`                     | Constructor que inicializa una nueva orden con los valores de sus atributos.                |
| `updateDate(Date currentDate)`    | Actualiza la fecha de la orden a la proporcionada.                                         |
| `update(Order request)`          | Actualiza los atributos de la orden (descripción, cantidad, precio total, método de pago).  |
| `end()`                          | Cambia el estado de la orden a `FINALIZED`.                                                 |
| `qualify()`                      | Cambia el estado de la orden a `QUALIFIED`.                                                 |
| `isPending()`                    | Verifica si la orden está en estado `PENDING`.                                              |
| `isQualified()`                  | Verifica si la orden está en estado `QUALIFIED`.                                            |
| `isFinalized()`                  | Verifica si la orden está en estado `FINALIZED`.                                            |
| `getStatus()`                    | Retorna el estado actual de la orden como un string en minúsculas.                          |

| **Aggregate**: `Rate`                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa la raíz del agregado de una calificación (rate) en el sistema de compras, mapeando la tabla "rates". |

| **Atributo**                     | **Tipo**                | **Descripción**                                                   |
|----------------------------------|-------------------------|-------------------------------------------------------------------|
| `id`                             | `Long`                  | Identificador único de la calificación.                           |
| `rate`                           | `Long`                  | Valor de la calificación asignada por un usuario.                 |
| `date`                           | `String`                | Fecha en la que se asignó la calificación.                        |
| `product`                        | `Sale`                  | Relación con la entidad `Sale` que está siendo calificada.        |
| `userId`                         | `Long`                  | Identificador del usuario que asignó la calificación.             |

| **Método**                       | **Descripción**                                                                             |
|----------------------------------|---------------------------------------------------------------------------------------------|
| `Rate(Long rate, String date, Sale product, Long userId)` | Constructor que inicializa un nuevo "Rate" con sus atributos.      |
| `updateRate(Long rate)`          | Actualiza el valor de la calificación.                                                      |

| **Entidad**: `Sale`                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa la entidad de una venta, mapeando la estructura de la tabla "sales" en la base de datos.       |

| **Atributo**                | **Tipo**           | **Descripción**                                                             |
|-----------------------------|--------------------|-----------------------------------------------------------------------------|
| `id`                        | `Long`             | Identificador único de la venta.                                            |
| `name`                      | `String`           | Nombre del producto o servicio en venta.                                    |
| `description`               | `String`           | Descripción detallada del producto o servicio.                              |
| `unitPrice`                 | `Double`           | Precio unitario del producto o servicio.                                    |
| `quantity`                  | `Long`             | Cantidad disponible del producto para la venta.                             |
| `imageUrl`                  | `String`           | URL de la imagen representativa del producto.                               |
| `userId`                    | `Long`             | Identificador del usuario que está ofreciendo el producto o servicio.       |

| **Método**                  | **Descripción**                                                                                  |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| `Sale(String name, String description, Double unitPrice, Long quantity, String imageUrl, Long userId)` | Constructor que inicializa una nueva instancia de la entidad `Sale`. |

### 4.2.2.2. Interface Layer

Descripción: El Interface Layer o capa de interfaz define cómo los usuarios o sistemas externos interactúan con el sistema. Aquí, los controladores reciben y gestionan las solicitudes HTTP, enviando la información adecuada a los servicios de aplicación.

Justificación: El OrderController maneja las solicitudes relacionadas con las órdenes de compra, como la creación de nuevas órdenes mediante el método createOrder. Este controlador se apoya en los servicios OrderQueryService y OrderCommandService para consultar y ejecutar acciones sobre las órdenes, respetando las reglas de negocio definidas en el sistema. Este layer actúa como la entrada principal para interactuar con las órdenes, canalizando solicitudes a la capa de aplicación.

| **Controlador**: `OrderController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con los pedidos. Define los endpoints para la API.   |

| **Método**                              | **Descripción**                                                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `createOrder(CreateOrderResource resource)`    | Crea un nuevo pedido y devuelve el recurso del pedido creado con su ID.                                         |
| `finalizeOrder(Long orderId)`          | Finaliza un pedido existente basado en su ID y devuelve el ID del pedido finalizado.                            |
| `qualifyOrder(Long orderId)`           | Califica un pedido existente basado en su ID y devuelve el ID del pedido calificado.                             |
| `getAllOrders()`                        | Recupera una lista de todos los pedidos registrados y los devuelve como recursos.                                |
| `getOrderById(Long orderId)`           | Recupera un pedido específico por su ID y devuelve el recurso correspondiente.                                    |
| `updateOrder(Long orderId, UpdateOrderResource resource)` | Actualiza un pedido existente y devuelve el recurso del pedido actualizado.                                         |
| `deleteOrder(Long orderId)`            | Elimina un pedido basado en su ID y devuelve una respuesta sin contenido.                                         |

| **Dependencias**                          | **Descripción**                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `OrderQueryService`                       | Servicio para manejar las consultas relacionadas con los pedidos.                                                   |
| `OrderCommandService`                     | Servicio para manejar las órdenes relacionadas con las operaciones de comando de pedidos.                           |
| `CreateOrderCommandFromResourceAssembler` | Ensamblador para convertir un recurso de creación de pedido en un comando.                                          |
| `OrderResourceFromEntityAssembler`       | Ensamblador para convertir una entidad de pedido en un recurso para la API.                                         |
| `CreateOrderResource`                     | Recurso que representa la solicitud para crear un pedido.                                                           |
| `OrderResource`                           | Recurso que representa la respuesta de un pedido en la API.                                                         |
| `UpdateOrderResource`                     | Recurso que representa la solicitud para actualizar un pedido.                                                      |

| **Controlador**: `RateController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con las tarifas. Define los endpoints para la API.   |

| **Método**                              | **Descripción**                                                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `createRate(CreateRateResource resource)`    | Crea una nueva tarifa y devuelve el recurso de la tarifa creada con su ID.                                       |
| `getAllRates()`                        | Recupera una lista de todas las tarifas registradas y las devuelve como recursos.                                |
| `getRateById(Long rateId)`           | Recupera una tarifa específica por su ID y devuelve el recurso correspondiente.                                    |

| **Dependencias**                          | **Descripción**                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `RateQueryService`                       | Servicio para manejar las consultas relacionadas con las tarifas.                                                   |
| `RateCommandService`                     | Servicio para manejar las órdenes relacionadas con las operaciones de comando de tarifas.                           |
| `CreateRateCommandFromResourceAssembler` | Ensamblador para convertir un recurso de creación de tarifa en un comando.                                          |
| `RateResourceFromEntityAssembler`       | Ensamblador para convertir una entidad de tarifa en un recurso para la API.                                         |
| `CreateRateResource`                     | Recurso que representa la solicitud para crear una tarifa.                                                           |
| `RateResource`                           | Recurso que representa la respuesta de una tarifa en la API.                                                         |

| **Controlador**: `SaleController`                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con las ventas. Define los endpoints para la API.     |

| **Método**                             | **Descripción**                                                                                                    |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `createSale(CreateSaleResource resource)` | Crea una nueva venta y devuelve el recurso de la venta creada con su ID.                                        |
| `getAllSales(String name)`            | Recupera una lista de todas las ventas registradas, con opción de filtrar por nombre.                           |
| `getSaleById(Long saleId)`            | Recupera una venta específica por su ID y devuelve el recurso correspondiente.                                   |

| **Dependencias**                         | **Descripción**                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `SaleQueryService`                      | Servicio para manejar las consultas relacionadas con las ventas.                                                  |
| `SaleCommandService`                    | Servicio para manejar las órdenes relacionadas con las operaciones de comando de ventas.                          |
| `CreateSaleCommandFromResourceAssembler`| Ensamblador para convertir un recurso de creación de venta en un comando.                                         |
| `SaleResourceFromEntityAssembler`      | Ensamblador para convertir una entidad de venta en un recurso para la API.                                        |
| `CreateSaleResource`                    | Recurso que representa la solicitud para crear una venta.                                                          |
| `SaleResource`                          | Recurso que representa la respuesta de una venta en la API.                                                       |

| **Controlador**: `SaleOrdersController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con los pedidos de una venta.                           |

| **Método**                                   | **Descripción**                                                                                                    |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `getOrderBySaleIdAndOrderId(Long saleId, Long orderId)` | Recupera un pedido específico asociado a una venta utilizando los IDs de la venta y del pedido. Devuelve el recurso correspondiente. |

| **Dependencias**                              | **Descripción**                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `OrderQueryService`                          | Servicio para manejar las consultas relacionadas con los pedidos.                                                  |
| `GetOrderBySaleIdQuery`                     | Consulta utilizada para obtener un pedido basado en el ID de la venta y el ID del pedido.                          |
| `OrderResource`                              | Recurso que representa la respuesta de un pedido en la API.                                                       |
| `OrderResourceFromEntityAssembler`          | Ensamblador para convertir una entidad de pedido en un recurso para la API.                                        |



### 4.2.2.3. Application Layer

Descripción: El Application Layer orquesta las operaciones que deben ejecutarse para cumplir con las necesidades del usuario, coordinando diferentes servicios y repositorios del sistema. Contiene la lógica específica de las acciones que no necesariamente forman parte del dominio principal pero son esenciales para el funcionamiento.

Justificación: En este contexto, los servicios OrderCommandService y OrderQueryService gestionan las reglas de negocio relacionadas con las órdenes. Se encargan de ejecutar comandos y consultas sobre las órdenes, como validar si una orden existe (existById) o recuperar una orden por su identificador (findById). Esta capa se comunica con el OrderRepository, asegurando que la lógica de negocio esté correctamente aplicada y se cumplan las reglas de integridad.

| **Controlador**: `OrderController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con los pedidos. Define los endpoints para la API.   |

| **Método**                              | **Descripción**                                                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `createOrder(CreateOrderResource resource)`    | Crea un nuevo pedido y devuelve el recurso del pedido creado con su ID.                                         |
| `finalizeOrder(Long orderId)`          | Finaliza un pedido existente basado en su ID y devuelve el ID del pedido finalizado.                            |
| `qualifyOrder(Long orderId)`           | Califica un pedido existente basado en su ID y devuelve el ID del pedido calificado.                             |
| `getAllOrders()`                        | Recupera una lista de todos los pedidos registrados y los devuelve como recursos.                                |
| `getOrderById(Long orderId)`           | Recupera un pedido específico por su ID y devuelve el recurso correspondiente.                                    |
| `updateOrder(Long orderId, UpdateOrderResource resource)` | Actualiza un pedido existente y devuelve el recurso del pedido actualizado.                                         |
| `deleteOrder(Long orderId)`            | Elimina un pedido basado en su ID y devuelve una respuesta sin contenido.                                         |

| **Dependencias**                          | **Descripción**                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `OrderQueryService`                       | Servicio para manejar las consultas relacionadas con los pedidos.                                                   |
| `OrderCommandService`                     | Servicio para manejar las órdenes relacionadas con las operaciones de comando de pedidos.                           |
| `CreateOrderCommandFromResourceAssembler` | Ensamblador para convertir un recurso de creación de pedido en un comando.                                          |
| `OrderResourceFromEntityAssembler`       | Ensamblador para convertir una entidad de pedido en un recurso para la API.                                         |
| `CreateOrderResource`                     | Recurso que representa la solicitud para crear un pedido.                                                           |
| `OrderResource`                           | Recurso que representa la respuesta de un pedido en la API.                                                         |
| `UpdateOrderResource`                     | Recurso que representa la solicitud para actualizar un pedido.                                                      |

| **Controlador**: `RateController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con las tarifas. Define los endpoints para la API.   |

| **Método**                              | **Descripción**                                                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `createRate(CreateRateResource resource)`    | Crea una nueva tarifa y devuelve el recurso de la tarifa creada con su ID.                                       |
| `getAllRates()`                        | Recupera una lista de todas las tarifas registradas y las devuelve como recursos.                                |
| `getRateById(Long rateId)`           | Recupera una tarifa específica por su ID y devuelve el recurso correspondiente.                                    |

| **Dependencias**                          | **Descripción**                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `RateQueryService`                       | Servicio para manejar las consultas relacionadas con las tarifas.                                                   |
| `RateCommandService`                     | Servicio para manejar las órdenes relacionadas con las operaciones de comando de tarifas.                           |
| `CreateRateCommandFromResourceAssembler` | Ensamblador para convertir un recurso de creación de tarifa en un comando.                                          |
| `RateResourceFromEntityAssembler`       | Ensamblador para convertir una entidad de tarifa en un recurso para la API.                                         |
| `CreateRateResource`                     | Recurso que representa la solicitud para crear una tarifa.                                                           |
| `RateResource`                           | Recurso que representa la respuesta de una tarifa en la API.                                                         |

| **Controlador**: `SaleController`                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con las ventas. Define los endpoints para la API.     |

| **Método**                             | **Descripción**                                                                                                    |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `createSale(CreateSaleResource resource)` | Crea una nueva venta y devuelve el recurso de la venta creada con su ID.                                        |
| `getAllSales(String name)`            | Recupera una lista de todas las ventas registradas, con opción de filtrar por nombre.                           |
| `getSaleById(Long saleId)`            | Recupera una venta específica por su ID y devuelve el recurso correspondiente.                                   |

| **Dependencias**                         | **Descripción**                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `SaleQueryService`                      | Servicio para manejar las consultas relacionadas con las ventas.                                                  |
| `SaleCommandService`                    | Servicio para manejar las órdenes relacionadas con las operaciones de comando de ventas.                          |
| `CreateSaleCommandFromResourceAssembler`| Ensamblador para convertir un recurso de creación de venta en un comando.                                         |
| `SaleResourceFromEntityAssembler`      | Ensamblador para convertir una entidad de venta en un recurso para la API.                                        |
| `CreateSaleResource`                    | Recurso que representa la solicitud para crear una venta.                                                          |
| `SaleResource`                          | Recurso que representa la respuesta de una venta en la API.                                                       |

| **Controlador**: `SaleOrdersController`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que gestiona las operaciones relacionadas con los pedidos de una venta.                           |

| **Método**                                   | **Descripción**                                                                                                    |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `getOrderBySaleIdAndOrderId(Long saleId, Long orderId)` | Recupera un pedido específico asociado a una venta utilizando los IDs de la venta y del pedido. Devuelve el recurso correspondiente. |

| **Dependencias**                              | **Descripción**                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `OrderQueryService`                          | Servicio para manejar las consultas relacionadas con los pedidos.                                                  |
| `GetOrderBySaleIdQuery`                     | Consulta utilizada para obtener un pedido basado en el ID de la venta y el ID del pedido.                          |
| `OrderResource`                              | Recurso que representa la respuesta de un pedido en la API.                                                       |
| `OrderResourceFromEntityAssembler`          | Ensamblador para convertir una entidad de pedido en un recurso para la API.                                        |

### 4.2.2.3. Application Layer

| **Servicio**: `OrderCommandServiceImpl`                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `OrderCommandService`, encargada de manejar la creación y actualización de pedidos.  |

| **Método**                                    | **Descripción**                                                                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(CreateOrderCommand command)`         | Maneja la creación de un nuevo pedido. Valida la venta asociada y guarda el pedido en el repositorio.                        |
| `handle(FinalizeOrderCommand command)`      | Maneja la finalización de un pedido existente. Marca el pedido como finalizado y lo guarda en el repositorio.                 |
| `handle(QualifyOrderCommand command)`       | Maneja la calificación de un pedido existente. Actualiza el estado del pedido y lo guarda en el repositorio.                  |
| `deleteOrder(Long orderId)`                  | Elimina un pedido existente por ID. Lanza una excepción si el pedido no se encuentra en el repositorio.                      |
| `updateOrder(Long orderId, UpdateOrderResource request)` | Actualiza un pedido existente si su estado es "pendiente". Lanza una excepción si el pedido no se encuentra o no está en estado "pendiente". |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `OrderRepository`                           | Repositorio para manejar la persistencia de los pedidos.                                                                     |
| `SaleQueryService`                          | Servicio para manejar las consultas relacionadas con las ventas, utilizado para validar ventas al crear o actualizar pedidos. |
| `CreateOrderCommand`                        | Comando que encapsula los datos necesarios para crear un nuevo pedido.                                                      |
| `FinalizeOrderCommand`                      | Comando que encapsula los datos necesarios para finalizar un pedido.                                                        |
| `QualifyOrderCommand`                       | Comando que encapsula los datos necesarios para calificar un pedido.                                                        |
| `UpdateOrderResource`                       | Recurso que encapsula los datos necesarios para actualizar un pedido.                                                       |
| `Order`                                     | Entidad que representa un pedido en el dominio.                                                                              |

| **Servicio**: `OrderQueryServiceImpl`                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `OrderQueryService`, encargada de manejar las consultas relacionadas con los pedidos.  |

| **Método**                                   | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(GetOrderByIdQuery query)`          | Maneja la consulta para obtener un pedido por su ID. Devuelve un `Optional<Order>` que contiene el pedido si se encuentra.     |
| `handle(GetAllOrdersQuery query)`          | Maneja la consulta para obtener todos los pedidos. Devuelve una lista de todos los pedidos.                                    |
| `handle(GetOrderBySaleIdQuery query)`      | Maneja la consulta para obtener un pedido específico asociado a una venta por sus IDs. Devuelve un `Optional<Order>` que contiene el pedido si se encuentra. |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `OrderRepository`                           | Repositorio para manejar la persistencia y consulta de pedidos.                                                              |
| `GetOrderByIdQuery`                        | Consulta que encapsula el ID del pedido que se desea obtener.                                                                |
| `GetAllOrdersQuery`                        | Consulta que no requiere parámetros y busca obtener todos los pedidos.                                                       |
| `GetOrderBySaleIdQuery`                    | Consulta que encapsula el ID de la venta y el ID del pedido para buscar un pedido específico.                                 |

| **Servicio**: `RateCommandServiceImpl`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `RateCommandService`, encargada de manejar la creación de valoraciones.       |

| **Método**                                   | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(CreateRateCommand command)`          | Maneja la creación de una nueva valoración. Busca la venta asociada al producto mediante su ID y guarda la nueva valoración en el repositorio. Devuelve el ID de la valoración creada. |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `RateRepository`                           | Repositorio para manejar la persistencia y consulta de valoraciones.                                                          |
| `SaleQueryService`                         | Servicio utilizado para obtener información sobre ventas, necesario para asociar una valoración a una venta específica.       |
| `CreateRateCommand`                        | Comando que encapsula los datos necesarios para crear una nueva valoración, como la tasa, la fecha, y el ID del usuario.     |
| `GetSaleByIdQuery`                        | Consulta que encapsula el ID del producto para buscar la venta asociada.                                                      |

| **Servicio**: `RateQueryServiceImpl`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `RateQueryService`, encargada de manejar las consultas relacionadas con las valoraciones.       |

| **Método**                                   | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(GetAllRatesQuery query)`            | Maneja la consulta para obtener todas las valoraciones. Retorna una lista de todas las valoraciones almacenadas en el repositorio. |
| `handle(GetRateByIdQuery query)`            | Maneja la consulta para obtener una valoración específica mediante su ID. Retorna un `Optional<Rate>` que puede contener la valoración si existe. |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `RateRepository`                           | Repositorio para manejar la persistencia y consulta de valoraciones.                                                          |
| `GetAllRatesQuery`                        | Consulta que se utiliza para obtener todas las valoraciones.                                                                  |
| `GetRateByIdQuery`                        | Consulta que encapsula el ID de la valoración que se desea recuperar.                                                         |

| **Servicio**: `SaleCommandServiceImpl`                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `SaleCommandService`, encargada de manejar la creación de ventas.                        |

| **Método**                                   | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(CreateSaleCommand command)`         | Maneja el comando para crear una nueva venta. Crea una instancia de `Sale` utilizando los parámetros del comando y la guarda en el repositorio. Retorna el ID de la venta creada. |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `SaleRepository`                           | Repositorio para manejar la persistencia y consulta de ventas.                                                          |
| `CreateSaleCommand`                        | Comando que encapsula los parámetros necesarios para crear una nueva venta, como nombre, descripción, precio unitario, cantidad, URL de imagen y ID de usuario. |

| **Servicio**: `SaleQueryServiceImpl`                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación de la interfaz `SaleQueryService`, encargada de manejar las consultas relacionadas con ventas.              |

| **Método**                                   | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `handle(GetAllSalesQuery query)`            | Maneja el comando para obtener todas las ventas. Retorna una lista de todas las instancias de `Sale` almacenadas en el repositorio. |
| `handle(GetSaleByIdQuery query)`            | Maneja el comando para obtener una venta específica por su ID. Retorna un `Optional<Sale>` que puede contener la venta buscada. |

| **Dependencias**                             | **Descripción**                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `SaleRepository`                           | Repositorio para manejar la persistencia y consulta de ventas.                                                          |
| `GetAllSalesQuery`                         | Comando que encapsula la solicitud para obtener todas las ventas.                                                        |
| `GetSaleByIdQuery`                         | Comando que encapsula la solicitud para obtener una venta específica por su ID.                                          |


### 4.2.2.4. Infrastructure Layer

Descripción: El Infrastructure Layer se encarga de proporcionar acceso a la base de datos, servicios externos y otros detalles técnicos que no forman parte de la lógica de negocio. Actúa como la implementación real de la persistencia y otras preocupaciones técnicas.

Justificación: El OrderRepository es el repositorio responsable de la persistencia de las órdenes. Métodos como findOrderBySaleIdAndId permiten interactuar directamente con la base de datos para obtener órdenes por el identificador de la venta y el identificador de la orden. Este layer asegura que los datos se almacenen y recuperen correctamente desde la infraestructura subyacente, separando las preocupaciones técnicas de las reglas de negocio.

| **Repositorio**: `OrderRepository`                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Repositorio de acceso a datos para la entidad `Order`, utilizando JPA para realizar operaciones de persistencia. |

| **Método**                                          | **Descripción**                                                                                                  |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `findOrderBySaleIdAndId(Long saleId, Long orderId)` | Busca una orden específica asociada a una venta dada, utilizando el ID de la venta y el ID de la orden. Retorna un `Optional<Order>` que puede contener la orden buscada o estar vacío si no se encuentra. |




### 4.2.2.6. Bounded Context Software Architecture Component Level Diagrams

Este nuevo diagrama muestra una arquitectura monolítica ampliada de la aplicación API "Ayni". La Single Page Application (SPA) realiza llamadas API a varios controladores, como el Rate Controller, Sale Controller, Order Controller, y SalesOrders Controller, los cuales gestionan las operaciones de productos, ventas, pedidos y sus relaciones. Cada controlador delega las funciones de consultas y comandos a sus respectivos servicios, como RateQueryService, SaleCommandService, y OrderQueryService, que interactúan con repositorios dedicados (como RateRepository, SaleRepository, y OrderRepository) para acceder y gestionar los datos almacenados en una base de datos MySQL. Esta arquitectura asegura una separación clara de responsabilidades dentro del monolito, facilitando la gestión de datos y operaciones.

![image](https://github.com/user-attachments/assets/874b41be-d048-4820-910a-8fc1f2a4530d)

### 4.2.2.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.2.7.1. Bounded Context Domain Layer Class Diagrams

el diagrama UML presenta la estructura de un sistema de gestión de órdenes y ventas, mostrando clases como "Order" con atributos y métodos específicos, relacionadas con clases como "OrderStatus", "PaymentMethod", y "Sale". Incluye interfaces para servicios de comandos y consultas, sugiriendo una arquitectura orientada a servicios para operaciones CRUD. las relaciones y asociaciones en el diagrama reflejan principios de orientación a objetos como encapsulación, herencia y polimorfismo.

![imagen](https://github.com/user-attachments/assets/9b5224a5-c4bc-48b6-aad7-8fc669b46506)




#### 4.2.2.7.2. Bounded Context Database Design Diagram


El diagrama de la base de datos para el bounded context "Shopping" muestra las tablas clave relacionadas con el procesamiento de órdenes de compra. La tabla principal es orders, que almacena información sobre los pedidos, incluyendo el método de pago, fecha de la orden, ID de la venta, cantidad, precio total, usuario que realizó la orden y el estado del pedido. La tabla order_statuses define los diferentes estados que una orden puede tener. La tabla sales almacena detalles de los productos en venta, como el nombre, descripción, precio unitario e imagen. También está vinculada a los usuarios que los venden mediante el campo user_id. Las relaciones entre tablas como payments especifican los métodos de pago utilizados en las órdenes, y la tabla rates contiene las calificaciones de los productos vendidos, asociadas a la tabla sales. Las conexiones entre las tablas están definidas por claves foráneas que aseguran la integridad de los datos, permitiendo la gestión eficiente de las órdenes, productos, pagos y calificaciones en el contexto de compras.

![image](https://github.com/user-attachments/assets/91d47e55-640d-4e7c-b129-439d5349f3af)

## 4.2.3. Bounded Context: Crop Registration

### 4.2.3.1. Domain Layer

El Domain Layer es el corazón del diseño de un sistema basado en DDD (Domain-Driven Design). En el contexto de Crop Registration, este capa contiene la lógica del dominio y modela los conceptos centrales del sistema, en este caso, los productos agrícolas. El agregado principal es la entidad Product, que representa un producto agrícola y contiene atributos como nombre, descripción, tipo de suelo recomendado, distancia y profundidad de cultivo, y más.

Justificación: Este nivel se encarga de encapsular las reglas de negocio y los invariantes asociados a los productos agrícolas, asegurando que cualquier operación relacionada con los productos cumpla con las reglas del negocio. Los métodos públicos proporcionan acceso a los atributos del producto de una manera controlada, lo que evita inconsistencias y errores en la manipulación de los datos. El Domain Layer define el modelo de dominio sin involucrarse en detalles de implementación o infraestructura.

| **Entidad**: `Product`                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa un producto agrícola y su información relacionada.                                              |

| **Atributo**                      | **Tipo**       | **Descripción**                                                   |
|-----------------------------------|----------------|-------------------------------------------------------------------|
| `id`                              | `Long`         | Identificador único del producto (autogenerado).                  |
| `name`                            | `String`       | Nombre del producto.                                              |
| `description`                     | `String`       | Descripción del producto.                                         |
| `recommendedCultivationDistance`  | `String`       | Distancia de cultivo recomendada.                                 |
| `recommendedCultivationDepth`     | `String`       | Profundidad de cultivo recomendada.                               |
| `recommendedGrowingClimate`       | `String`       | Clima de crecimiento recomendado.                                 |
| `recommendedSoilType`             | `String`       | Tipo de suelo recomendado.                                        |
| `recommendedGrowingSeason`        | `String`       | Temporada de crecimiento recomendada.                             |
| `imageUrl`                        | `String`       | URL de la imagen del producto.                                    |
| `userId`                          | `Long`         | ID del usuario que creó o gestiona el producto.                   |

| **Método**                        | **Descripción**                                                       |
|-----------------------------------|-----------------------------------------------------------------------|
| `getId()`                         | Retorna el `id` del producto.                                         |
| `getName()`                       | Retorna el `name` del producto.                                       |
| `getDescription()`                | Retorna la `description` del producto.                                |
| `getRecommendedCultivationDistance()` | Retorna la distancia de cultivo recomendada (`recommendedCultivationDistance`). |
| `getRecommendedCultivationDepth()`| Retorna la profundidad de cultivo recomendada (`recommendedCultivationDepth`). |
| `getRecommendedGrowingClimate()`  | Retorna el clima de crecimiento recomendado (`recommendedGrowingClimate`). |
| `getRecommendedSoilType()`        | Retorna el tipo de suelo recomendado (`recommendedSoilType`).          |
| `getRecommendedGrowingSeason()`   | Retorna la temporada de crecimiento recomendada (`recommendedGrowingSeason`). |
| `getImageUrl()`                   | Retorna la URL de la imagen del producto (`imageUrl`).                |
| `getUserId()`                     | Retorna el ID del usuario (`userId`).                                 |


### 4.2.3.2. Interface Layer

El Interface Layer contiene los Controladores que permiten la interacción entre el sistema y los usuarios o sistemas externos. Aquí se encuentran métodos como createProduct, getAllProducts, y getProductById, que se encargan de gestionar las solicitudes HTTP relacionadas con los productos agrícolas.

Justificación: Este layer actúa como un mediador entre el mundo exterior (usuarios, APIs externas, etc.) y la aplicación, traduce las solicitudes entrantes en comandos que el sistema entiende y devuelve respuestas comprensibles para los usuarios o sistemas. Los servicios de comandos y consultas (ProductCommandService y ProductQueryService) están inyectados como dependencias, permitiendo que los controladores deleguen la lógica de negocio a servicios especializados.

| **Controlador**: `ProductController`                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador para la gestión de productos. Define los endpoints para manejar las solicitudes y respuestas relacionadas con los productos. |

| **Método**                                          | **Descripción**                                                                                               |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `createProduct(CreateProductResource resource)`      | Maneja la creación de un nuevo producto. Toma un recurso de creación de producto, convierte a un comando y llama al servicio de comando. Retorna el recurso del producto creado. |
| `getAllProducts(String name)`                        | Maneja la recuperación de todos los productos. Si se proporciona un nombre como parámetro, filtra la lista de productos por nombre antes de devolverla. |
| `getProductById(Long productId)`                    | Maneja la recuperación de un producto por su ID. Si el producto no se encuentra, retorna un estado 404 Not Found. De lo contrario, retorna el recurso del producto. |

| **Controlador**: `ProductCropsController`                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador para manejar los cultivos asociados a un producto. Define los endpoints para manejar las solicitudes y respuestas relacionadas con los cultivos de un producto específico. |

| **Método**                                          | **Descripción**                                                                                               |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `getAllCropsByProductId(Long productId)`           | Maneja la recuperación de todos los cultivos asociados a un producto específico dado su ID. Retorna una lista de recursos de cultivos. |
| `getCropByProductIdAndCropId(Long productId, Long cropId)` | Maneja la recuperación de un cultivo específico dado su ID y el ID del producto. Si el cultivo no se encuentra, retorna un estado 404 Not Found; de lo contrario, retorna el recurso del cultivo. |


### 4.2.3.3. Application Layer

El Application Layer es el nivel donde se definen los servicios de aplicación que gestionan la orquestación de las reglas de negocio. Aquí, se encuentran servicios como ProductCommandService y ProductQueryService, que implementan la lógica relacionada con la creación, modificación y consulta de productos.

Justificación: Esta capa actúa como intermediaria entre el Domain Layer y la Interface Layer. Al centralizar las reglas de negocio en los servicios, el sistema mantiene la lógica separada de los controladores y el dominio, lo que facilita su reutilización y prueba. Además, esta capa no almacena datos directamente, sino que interactúa con el repositorio para obtener o persistir información.

| **Servicio**: `ProductCommandServiceImpl`                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio `ProductCommandService` que maneja la creación de productos en la aplicación.              |

| **Método**                                         | **Descripción**                                                                                               |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `handle(CreateProductCommand command)`             | Maneja la creación de un nuevo producto. Toma un comando que contiene la información del producto y lo persiste en la base de datos. Retorna el ID del producto creado. |

| **Servicio**: `ProductQueryServiceImpl`                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio `ProductQueryService` que maneja la recuperación de productos de la aplicación.           |

| **Método**                                         | **Descripción**                                                                                               |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `handle(GetProductByIdQuery query)`                | Maneja la consulta para recuperar un producto por su ID. Devuelve un `Optional<Product>` que contiene el producto si se encuentra, o está vacío si no. |
| `handle(GetAllProductsQuery query)`                | Maneja la consulta para recuperar todos los productos. Retorna una lista de productos disponibles en la base de datos. |


### 4.2.3.4. Infrastructure Layer

El Infrastructure Layer maneja los detalles de la persistencia de los datos. Aquí se define el ProductRepository, que se encarga de interactuar con la base de datos para realizar operaciones CRUD sobre los productos. Métodos como findById y findAll permiten al sistema recuperar productos de la base de datos.

Justificación: Este layer permite desacoplar la lógica de acceso a datos del dominio y la aplicación, siguiendo el principio de separación de preocupaciones. La infraestructura está diseñada para ser fácilmente intercambiable o adaptable (por ejemplo, cambiar una base de datos sin modificar la lógica de negocio). Además, encapsula detalles técnicos como el mapeo de objetos a tablas en una base de datos relacional.

| **Repositorio**: `ProductRepository`                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Repositorio que maneja la persistencia de la entidad `Product` en la base de datos utilizando JPA.                     |

| **Método**                     | **Descripción**                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `findAll()`                   | Recupera todos los productos de la base de datos. Devuelve una lista de objetos `Product`.                          |
| `findById(Long id)`           | Recupera un producto por su ID. Devuelve un `Optional<Product>` que contiene el producto si se encuentra, o está vacío si no. |


### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams

Este diagrama muestra una arquitectura de componente para la gestión de productos en una aplicación monolítica. En la parte superior, la Single-Page Application (SPA) es el punto de acceso de los usuarios y está construida con tecnologías como JavaScript y Angular. Esta SPA realiza llamadas API (como JSON/HTTP) al Products Controller, que está implementado como un controlador MVC de Spring.

El Products Controller gestiona las solicitudes relacionadas con la creación y consulta de productos. Para operaciones de comando, como agregar productos, el controlador utiliza el ProductCommandService, que encapsula la lógica relacionada con los comandos para productos. Para las consultas de datos, se apoya en el ProductQueryService, que facilita la recuperación de datos de productos.

Ambos servicios, el ProductCommandService y el ProductQueryService, interactúan con el ProductRepository, que abstrae los detalles de interacción con la base de datos. Finalmente, el ProductRepository lee y escribe datos en una base de datos MySQL. Esta estructura sigue el patrón de separación de responsabilidades, asegurando que los controladores gestionen la lógica de presentación, mientras que los servicios manejan la lógica de negocio y los repositorios interactúan con la base de datos.

![image](https://github.com/user-attachments/assets/36aa4fad-8889-4eee-a0ec-1e560d7e333a)


### 4.2.3.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.3.7.1. Bounded Context Domain Layer Class Diagrams

el diagrama UML muestra una entidad "Product" con atributos como "id", "name", "description" y varios consejos de cultivo, además de una "imageUrl". dos interfaces, "ProductCommandService" y "ProductQueryService", están relacionadas con esta entidad, indicando una posible implementación de servicios de comandos y consultas, típicos de un patrón CQRS. las flechas sugieren que estas interfaces manejan operaciones relacionadas con objetos "Product".


![imagen](https://github.com/user-attachments/assets/67a04124-f087-4e91-8588-deb30209bc4d)




#### 4.2.3.7.2. Bounded Context Database Design Diagram


El diagrama de la tabla products representa los productos disponibles en el contexto de un sistema agrícola. Cada producto tiene un ID único como clave primaria, y atributos que incluyen el nombre y una descripción detallada. Además, contiene varias recomendaciones específicas para el cultivo del producto, como la distancia de cultivo, profundidad de cultivo, clima adecuado para el crecimiento, tipo de suelo recomendado, y la temporada de cultivo ideal. También se incluye un campo para la URL de la imagen del producto y un campo de clave foránea (user_id) que relaciona al producto con el usuario que lo ha registrado. Estos atributos permiten gestionar no solo la información básica de los productos, sino también recomendaciones detalladas para su cultivo óptimo.

![image](https://github.com/user-attachments/assets/3710915f-2038-4d1a-9d92-c41a2864497a)


## 4.2.4. Bounded Context: Planification
### 4.2.4.1. Domain Layer

El Domain Layer en este contexto se encarga de definir las entidades fundamentales que representan el dominio agrícola, específicamente la entidad "Crop". Este agregado captura las propiedades esenciales de un cultivo, como su nombre, estado de deshierbe, fertilización, oxigenación, y otras características propias de la gestión agrícola. También define la relación de un cultivo con otros elementos del sistema, como el producto asociado y el usuario responsable.

Justificación:
El uso de un Domain Layer permite encapsular la lógica de negocio y las reglas específicas del dominio en torno a la gestión de cultivos. Al centralizar estos aspectos en el agregado "Crop", se asegura una consistencia en la manipulación de datos y operaciones relacionadas a los cultivos. Este enfoque también facilita la escalabilidad del sistema, ya que permite agregar nuevas propiedades o métodos a la entidad sin afectar otros niveles del sistema.

| **Aggregate**: `Crop`                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa el agregado raíz "Cultivo" y su información relacionada. Se mapea a la tabla `crops` en la base de datos.|

| **Atributo**                      | **Tipo**       | **Descripción**                                                   |
|-----------------------------------|----------------|-------------------------------------------------------------------|
| `id`                              | `Long`         | Identificador único del cultivo (autogenerado).                   |
| `name`                            | `String`       | Nombre del cultivo.                                               |
| `pickUpWeed`                      | `Boolean`      | Indica si se realiza el deshierbe en el cultivo.                  |
| `fertilizeCrop`                   | `Boolean`      | Indica si se fertiliza el cultivo.                                |
| `oxygenateCrop`                   | `Boolean`      | Indica si se oxigena el cultivo.                                  |
| `makeCropLine`                    | `Boolean`      | Indica si se trazan líneas en el cultivo.                         |
| `makeCropHole`                    | `Boolean`      | Indica si se hacen agujeros en el cultivo.                        |
| `wateringDays`                    | `Long`         | Días entre riegos del cultivo.                                    |
| `pestCleanupDays`                 | `Long`         | Días entre limpiezas de plagas.                                   |
| `product`                         | `Product`      | El producto asociado con el cultivo (entidad `Product`).          |
| `userId`                          | `Long`         | ID del usuario que gestiona el cultivo.                           |

| **Método**                        | **Descripción**                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------|
| `getId()`                         | Retorna el `id` del cultivo.                                                                      |
| `getName()`                       | Retorna el `name` del cultivo.                                                                    |
| `getPickUpWeed()`                 | Retorna si el deshierbe está activo (`pickUpWeed`).                                               |
| `getFertilizeCrop()`              | Retorna si la fertilización está activa (`fertilizeCrop`).                                        |
| `getOxygenateCrop()`              | Retorna si la oxigenación está activa (`oxygenateCrop`).                                          |
| `getMakeCropLine()`               | Retorna si el trazado de líneas está activo (`makeCropLine`).                                     |
| `getMakeCropHole()`               | Retorna si la perforación de agujeros está activa (`makeCropHole`).                               |
| `getWateringDays()`               | Retorna los días entre riegos (`wateringDays`).                                                   |
| `getPestCleanupDays()`            | Retorna los días entre limpiezas de plagas (`pestCleanupDays`).                                   |
| `getProduct()`                    | Retorna el `product` asociado al cultivo.                                                         |
| `getUserId()`                     | Retorna el ID del usuario (`userId`).                                                             |
| `updateInformation()`             | Actualiza la información del cultivo con nuevos valores.                                          |
| `isPickUpWeedActive()`            | Verifica si el deshierbe está activo.                                                             |
| `isFertilizeCropActive()`         | Verifica si la fertilización está activa.                                                         |
| `isOxygenateCropActive()`         | Verifica si la oxigenación está activa.                                                           |
| `isMakeCropLineActive()`          | Verifica si el trazado de líneas está activo.                                                     |
| `isMakeCropHoleActive()`          | Verifica si la perforación de agujeros está activa.                                               |

### 4.2.4.2. Interface Layer

El Interface Layer expone las operaciones que el sistema permite realizar con los cultivos mediante el controlador "CropController". Este controlador actúa como intermediario entre la capa de aplicación y el cliente, permitiendo crear, consultar, y actualizar la información de los cultivos. Se apoya en los servicios de consultas y comandos para ejecutar las operaciones necesarias.

Justificación:
El Interface Layer es crucial para mantener una separación clara entre las capas de la aplicación y el cliente. Al usar un controlador dedicado, se asegura que todas las interacciones con los cultivos pasen por un punto central, lo que permite validar datos, aplicar reglas de seguridad, y simplificar el flujo de datos entre las diferentes capas del sistema. Además, desacopla la lógica de presentación de la lógica de negocio, promoviendo una arquitectura más limpia y fácil de mantener.

| **Controlador**: `CropController`                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador que maneja las operaciones relacionadas con cultivos. Define los endpoints para la gestión de cultivos. |

| **Método**                                    | **Descripción**                                                                                                        |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `createCrop(CreateCropResource resource)`    | Maneja la creación de un nuevo cultivo. Recibe un comando de creación, lo procesa y devuelve el recurso del cultivo creado. |
| `getAllCrops(String name)`                   | Maneja la recuperación de todos los cultivos. Devuelve una lista de recursos de cultivo. Permite filtrar por nombre.        |
| `getCropById(Long cropId)`                   | Maneja la recuperación de un cultivo específico por su ID. Devuelve el recurso del cultivo correspondiente o un 404 si no se encuentra. |


### 4.2.4.3. Application Layer

El Application Layer implementa la lógica de negocio relacionada con los cultivos mediante dos servicios clave: el CropCommandService y el CropQueryService. Estos servicios manejan las operaciones de comandos, como la creación de cultivos, y las consultas, como la obtención de todos los cultivos o la búsqueda de cultivos específicos por su ID o por el ID del producto asociado.

Justificación:
Este enfoque permite separar claramente las operaciones de comando y consulta, facilitando el mantenimiento y la expansión del sistema. La lógica de negocio es gestionada en este nivel, lo que permite aplicar reglas y restricciones de manera centralizada antes de realizar cambios en el dominio. Esto garantiza que las acciones relacionadas con los cultivos sean coherentes con las reglas de negocio y, al mismo tiempo, asegura que las consultas de información sean eficientes y directas.

| **Servicio**: `CropCommandServiceImpl`                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio que maneja la creación de cultivos. Utiliza un repositorio para persistir los cultivos y un servicio de consulta para verificar la existencia del producto asociado. |

| **Método**                                   | **Descripción**                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `handle(CreateCropCommand command)`         | Maneja la creación de un nuevo cultivo. Verifica la existencia del producto asociado y guarda el cultivo en el repositorio.  |

| **Servicio**: `CropQueryServiceImpl`                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Implementación del servicio que maneja las consultas relacionadas con los cultivos. Utiliza un repositorio para acceder a los datos de los cultivos. |

| **Método**                                   | **Descripción**                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `handle(GetAllCropsQuery query)`            | Maneja la consulta para obtener todos los cultivos. Devuelve una lista de todos los cultivos almacenados en el repositorio.  |
| `handle(GetCropByIdQuery query)`            | Maneja la consulta para obtener un cultivo por su ID. Devuelve un `Optional<Crop>` que contiene el cultivo, si existe.      |
| `handle(GetAllCropsByProductIdQuery query)`| Maneja la consulta para obtener todos los cultivos asociados a un producto específico. Devuelve una lista de cultivos.      |
| `handle(GetCropByProductIdQuery query)`     | Maneja la consulta para obtener un cultivo específico asociado a un producto dado. Devuelve un `Optional<Crop>` si existe. |

### 4.2.4.4. Infrastructure Layer

El Infrastructure Layer maneja la persistencia de los datos del dominio, en este caso, de los cultivos. El CropRepository es responsable de interactuar con la base de datos y proveer métodos para buscar, guardar y actualizar los cultivos, ya sea individualmente o en conjunto, mediante su ID o el ID del producto asociado.

Justificación:
Esta capa es esencial para desacoplar la lógica de negocio de los detalles de persistencia. Al utilizar un repositorio, se abstraen las interacciones directas con la base de datos, lo que facilita cambiar la implementación de la persistencia sin afectar las capas superiores. Además, permite centralizar el acceso a los datos, asegurando que todas las operaciones que modifiquen o consulten cultivos lo hagan de manera consistente y controlada.

| **Repositorio**: `CropRepository`                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Interfaz que extiende `JpaRepository` para manejar la persistencia de los cultivos. Proporciona métodos para acceder a los cultivos en la base de datos. |

| **Método**                                        | **Descripción**                                                                                                          |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `findCropByProductIdAndId(Long productId, Long cropId)` | Busca un cultivo específico por su ID y el ID del producto al que está asociado. Devuelve un `Optional<Crop>` que contiene el cultivo, si existe. |
| `findAllByProductId(Long productId)`            | Devuelve una lista de todos los cultivos que están asociados a un producto específico, utilizando el ID del producto.    |


### 4.2.4.6. Bounded Context Software Architecture Component Level Diagrams

Este diagrama muestra la arquitectura de un sistema monolítico donde una Single-Page Application (SPA), implementada con JavaScript y Angular, interactúa a través de llamadas API con una Web API Application construida con Spring. La SPA realiza peticiones HTTP a dos controladores: el Crops Controller, que permite a los usuarios añadir cultivos, y el ProductCrops Controller, que gestiona la interacción entre productos y cultivos. Ambos controladores utilizan servicios: el CropCommandService para operaciones relacionadas con la creación y modificación de cultivos, y el CropQueryService para la recuperación de datos. Estos servicios, a su vez, interactúan con el CropRepository, un componente que abstrae los detalles de interacción con la base de datos MySQL, usando JPA para lectura y escritura de información.

![image](https://github.com/user-attachments/assets/38bdd8af-3f7a-403c-9883-d780c5212818)

### 4.2.4.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.4.7.1. Bounded Context Domain Layer Class Diagrams

el diagrama contiene una clase 'Crop' que detalla características y cuidados del cultivo junto con operaciones para su gestión y estado. existen dos interfaces, 'CropQueryService' y 'CropCommandService', para las consultas y comandos del cultivo. las relaciones no están indicadas con flechas pero su disposición implica una conexión.

![image](https://github.com/user-attachments/assets/1c62f486-68fd-4e19-9cc3-1ba3646343c1)



#### 4.2.4.7.2. Bounded Context Database Design Diagram


El diagrama de la tabla crops describe las tareas y parámetros relacionados con el cultivo de productos agrícolas. Cada cultivo tiene un ID único como clave primaria y un nombre descriptivo. Además, incluye campos booleanos que indican si es necesario realizar tareas como recoger maleza (pick_up_weed), fertilizar el cultivo (fertilize_crop), oxigenar el cultivo (oxygenate_crop), hacer líneas de cultivo (make_crop_line), y hacer agujeros para el cultivo (make_crop_hole). También se especifican campos numéricos que indican la cantidad de días de riego (watering_days) y de días para limpieza de plagas (pest_cleanup_days). Finalmente, la tabla está vinculada a la tabla products a través de la clave foránea product_id, lo que relaciona las actividades de cultivo con un producto específico. Esto permite la gestión detallada de las operaciones necesarias para el cuidado de distintos tipos de cultivos.

![image](https://github.com/user-attachments/assets/99e675a2-b960-4221-b757-b7ed9ca75d04)



## 4.2.5. Bounded Context: Monitoring
### 4.2.5.1. Domain Layer

En el Domain Layer del contexto de monitoreo, los agregados principales son el "Sensor" y el "Actuator". Estos representan los componentes clave del sistema de monitoreo IoT, donde los sensores recolectan datos en tiempo real del terreno (como la temperatura o humedad), y los actuadores responden de manera automática a las condiciones monitoreadas, como activarse para regar o ajustar la ventilación.

Justificación:
Este enfoque permite encapsular las responsabilidades de cada dispositivo en un solo agregado. Al definir claramente qué información y comportamientos están asociados a cada entidad, se garantiza la coherencia y la integridad en la recolección de datos y en las respuestas automatizadas. Los atributos clave, como id, dataValue y timestamp en los sensores, y status en los actuadores, ayudan a gestionar eficientemente los estados y las mediciones críticas para las decisiones automatizadas.

| **Aggregate**: `Sensor`                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa un sensor IoT para monitorear datos del terreno.    |

| **Atributos**                                | **Tipo de dato** | **Visibilidad** | **Descripción**                                                                                           |
|----------------------------------------------|------------------|-----------------|-----------------------------------------------------------------------------------------------------------|
| `id`                                         | `Long`           | `Private`       | Identificador único del sensor o actuador.                                                                 |
| `dataValue`                                  | `String`         | `Private`       | Valor de datos medido por el sensor (ej. temperatura).                                                     |
| `timestamp`                                  | `String`         | `Private`       | Fecha y hora de la medición realizada por el sensor.                                                       |

| **Métodos**                                  | **Tipo de retorno** | **Visibilidad** | **Descripción**                                                                                           |
|----------------------------------------------|---------------------|-----------------|-----------------------------------------------------------------------------------------------------------|
| `CollectDailyData()`                         | `SensorData`         | `Public`        | Recolecta datos diarios de los sensores.                                                                  |


| **Aggregate**: `Actuator`                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|
| **Descripción**: Representa un actuador IoT para realizar acciones automáticas. |

| **Atributos**                                | **Tipo de dato** | **Visibilidad** | **Descripción**                                                                                           |
|----------------------------------------------|------------------|-----------------|-----------------------------------------------------------------------------------------------------------|
| `id`                                         | `Long`           | `Private`       | Identificador único del sensor o actuador.                                                                 |
| `status`                                     | `String`         | `Private`       | Estado del actuador (ej. activado/desactivado).                                                            |

| **Métodos**                                  | **Tipo de retorno** | **Visibilidad** | **Descripción**                                                                                           |
|----------------------------------------------|---------------------|-----------------|-----------------------------------------------------------------------------------------------------------|
| `ActivateActuator()`                         | `void`               | `Public`        | Activa un actuador basado en las condiciones del terreno.                                                  |
| `DeactivateActuator()`                       | `void`               | `Public`        | Desactiva un actuador.                                                                                     |

### 4.2.5.2. Interface Layer

El Interface Layer incluye el "MonitoringController", que expone las operaciones para gestionar tanto los sensores como los actuadores. Este controlador permite obtener los datos diarios de los sensores y activar o desactivar los actuadores en base a las condiciones del terreno.

Justificación:
El Interface Layer es esencial para proporcionar un punto de entrada claro para la gestión de dispositivos IoT. Con un controlador dedicado, se logra desacoplar la lógica de presentación de la lógica de negocio, manteniendo la simplicidad y claridad en la interacción entre la interfaz del usuario y el sistema. Esto garantiza que la recolección de datos y la activación de los actuadores ocurran de manera controlada y eficiente.

| **Controller** `MonitoringController`                                                                                             |
|------------------------------------------------------------------------------------------------------------|
| **Descripción**: Controlador para la gestión de sensores y actuadores IoT.                                   |

| **Atributos**                              | **Tipo de dato**           | **Visibilidad** | **Descripción**                                 |
|--------------------------------------------|----------------------------|-----------------|-------------------------------------------------|
| `SensorQueryService`                      | `sensorQueryService`      | `Private`       | Servicio de consulta de sensores.                |
| `ActuatorCommandService`                  | `actuatorCommandService`  | `Private`       | Servicio de comandos para actuadores.            |

| **Métodos**                                | **Tipo de retorno**       | **Visibilidad** | **Descripción**                                 |
|--------------------------------------------|----------------------------|-----------------|-------------------------------------------------|
| `getDailySensorData()`                     | `List<SensorData>`        | `Public`        | Obtiene datos diarios de sensores.               |
| `activateActuator()`                       | `void`                     | `Public`        | Activa un actuador basado en los datos recolectados. |
| `deactivateActuator()`                     | `void`                     | `Public`        | Desactiva un actuador.                           |

### 4.2.5.3. Application Layer

En el Application Layer, el "SensorQueryService" y el "ActuatorCommandService" manejan la lógica de negocio relacionada con los sensores y actuadores. El servicio de consultas se encarga de obtener los datos de los sensores, mientras que el servicio de comandos gestiona la activación o desactivación de los actuadores en función de los datos del terreno.

Justificación:
Esta capa asegura que todas las interacciones con los sensores y actuadores sigan las reglas de negocio definidas. Separar las consultas y comandos en servicios especializados permite mantener el código limpio y modular. También facilita la ampliación futura del sistema para incluir nuevas reglas o tipos de datos sin alterar la estructura básica.

| **Service** `SensorQueryService`                                                                                             |
|--------------------------------------------------------------------------------------------------------|
| **Descripción**: Servicio para consultas de datos de sensores.                                           |

| **Atributos**                           | **Tipo de dato**           | **Visibilidad** | **Descripción**                                 |
|-----------------------------------------|----------------------------|-----------------|-------------------------------------------------|
| `SensorRepository`                     | `sensorRepository`        | `Private`       | Repositorio de datos de sensores.                |

| **Métodos**                             | **Tipo de retorno**       | **Visibilidad** | **Descripción**                                 |
|-----------------------------------------|----------------------------|-----------------|-------------------------------------------------|
| `existById`                            | `Boolean`                 | `Public`        | Método para validar la existencia de un sensor por ID. |
| `findById`                             | `Sensor`                  | `Public`        | Método para obtener un sensor por ID.           |

### 4.2.5.4. Infrastructure Layer

El Infrastructure Layer gestiona la persistencia de los datos. Los repositorios de sensores y actuadores son responsables de interactuar con la base de datos para obtener y almacenar la información crítica relacionada con estos dispositivos. Métodos como findSensorById y findActuatorById permiten recuperar la información correspondiente a un dispositivo en particular.

Justificación:
El uso de repositorios permite centralizar el acceso a los datos, desacoplando la lógica de negocio de la infraestructura de persistencia. Esto facilita cambios en la implementación de la base de datos sin afectar otras capas del sistema, y garantiza que los datos se gestionen de manera coherente y eficiente, manteniendo la fiabilidad del sistema IoT.

| **Repository** `SensorRepository`                                                                                         |
|--------------------------------------------------------------------------------------------------------|
| **Descripción**: Repositorio de sensores.                                                                |

| **Métodos**                                | **Tipo de retorno**     | **Visibilidad** | **Descripción**                                 |
|---------------------------------------------|--------------------------|-----------------|-------------------------------------------------|
| `findSensorById`                          | `Sensor`                 | `Public`        | Método para obtener un sensor por su ID.       |

---

| **Repository** `ActuatorRepository`                                                                                          |
|--------------------------------------------------------------------------------------------------------|
| **Descripción**: Repositorio de actuadores.                                                              |

| **Métodos**                                | **Tipo de retorno**     | **Visibilidad** | **Descripción**                                 |
|---------------------------------------------|--------------------------|-----------------|-------------------------------------------------|
| `findActuatorById`                        | `Actuator`               | `Public`        | Método para obtener un actuador por su ID.     |

### 4.2.5.6. Bounded Context Software Architecture Component Level Diagrams

Este diagrama de componentes representa un sistema monolítico que gestiona datos de sensores y actuadores, donde una Single-Page Application (SPA), implementada con JavaScript y Angular, interactúa con una Web API Application a través de llamadas HTTP. La SPA realiza peticiones al Sensors Controller para obtener datos de los sensores, y al Actuators Controller para acceder a las funcionalidades de los actuadores. El Sensors Controller utiliza el SensorQueryService para encapsular la lógica de recuperación de datos, que a su vez se comunica con el SensorRepository, encargado de abstraer la interacción con la base de datos. De manera similar, el Actuators Controller utiliza el ActuatorCommandService para encapsular la lógica de control de actuadores, y este se comunica con el ActuatorRepository para la interacción con la base de datos. Ambos repositorios emplean JPA para realizar operaciones de lectura y escritura en la base de datos MySQL.

![image](https://github.com/user-attachments/assets/e655c3e7-3fe7-438e-bc13-02e73f03df8c)

### 4.2.5.7. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.5.7.1. Bounded Context Domain Layer Class Diagrams

El diagrama de clases representa el bounded context "Monitoring" y muestra dos agregados principales: Sensor y Actuator, cada uno con su respectiva interfaz de servicio. El agregado Sensor tiene atributos como id: Long, dataValue: String, y timestamp: String, y está asociado con la interfaz SensorQueryService que probablemente proporciona operaciones de consulta sobre los sensores. El agregado Actuator tiene atributos como id: Long y status: String, y está vinculado a la interfaz ActuatorCommandService, sugiriendo que este servicio maneja comandos para el control de actuadores. Los dos agregados están conectados mediante una relación de composición, indicando que juntos forman un sistema de monitoreo que integra sensores y actuadores.

![image](https://github.com/user-attachments/assets/c5e870d5-1047-4da0-96b0-507f709bf5dc)


#### 4.2.5.7.2. Bounded Context Database Design Diagram

El diagrama de base de datos representa el contexto limitado (bounded context) de "Monitoring", compuesto por dos tablas principales: sensors y actuators. La tabla sensors contiene los atributos id (clave primaria), data_value (valor de datos registrado, de tipo varchar), timestamp (de tipo booleano, probablemente para indicar si es válido), y crop_id (clave foránea que posiblemente hace referencia a un cultivo específico). La tabla actuators está relacionada con sensors a través de sensor_id (clave foránea), y sus atributos incluyen id (clave primaria), status (estado actual del actuador, de tipo varchar) y sensor_id. Esta estructura sugiere un sistema de monitoreo donde los sensores capturan datos asociados a cultivos y los actuadores reaccionan en función de esos datos.

![image](https://github.com/user-attachments/assets/305633b9-6f93-4cf5-8711-8950ff5ddf92)

