![UPC_logo_transparente (1)](https://github.com/JorgeGonzales15/SW51-GreatMinds-OpenSource/assets/104078975/2ff342be-dc34-415c-925e-1e7133e49abf)

Universidad Peruana de Ciencias Aplicadas

Ingeniería de Software

Ciclo 2024-02

# DESARROLLO DE SOLUCIONES IOT

Sección SW74

Profesor: Velasquez Nuñez, Angel Augusto

***INFORME DE TRABAJO FINAL - TF***

**Startup: GreatMinds**

**Producto: Ayni**

**Integrantes:**
- Alejo Cardenas, Luis Angel
- Espejo Macuri, Paolo Andre
- Gonzales Carrión, Jorge Enrique
- Rios Jaimes, Jhonel Enrique
- Sebastian Tasayco, Javier Martin

Noviembre del 2024

---
# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de la modificación |
| - | - | - | - |
| 1.00 | 15/08/2024 | Alejo Cardenas, Luis Angel | Elaboraciónd de Lean Ux Process, Diseño, analisis y registro de entrevistas  |
| 1.10 | 20/08/2024 | Espejo Macuri, Paolo Andre | Registro de entrevistas y diseño de entrevistas, bounded contexts tactical-level domain driven design |
| 1.20 | 21/08/2024 | Gonzales Carrión, Jorge Enrique| Creación de carátula, indice del informe, todos los puntos del capitulo 4, Registro de entrevistas y diseño de entrevistas, realizar el desarrollo del proceso Lean Ux|
| 1.30 | 21/08/2024 | Rios Jaimes, Jhonel Enrique | Desarrollo de User Journey Mapping y registro de entrevista |
| 1.40 | 01/09/2024 | Sebastian Tasayco, Javier Martin | Diseño, analisis y registro de entrevistas |
| 2.00 | 21/09/2024 | Espejo Macuri, Paolo Andre | Correcciones en Strategic Domain Driven Design, Elaboración de User Flows y Wireflows y Task de Sprint 1|
| 2.10 | 23/09/2024 | Rios Jaimes, Jhonel Enrique | Elaboración de primera versión de web app y mockups y correcciones de Capitulo 3 y Task de Sprint 1|
| 2.20 | 23/09/2024 | Sebastian Tasayco, Javier Martin | Correcciones de Lean Ux Problem Statement e hipotesis y task de Sprint 1 |
| 2.30 | 23/09/2024 | Alejo Cardenas, Luis Angel | Correcciones de Capitulo 2 y elaboración de mockups y wireframes de la web app  y Task de Sprint 1|
| 2.40 | 23/09/2024 | Gonzales Carrión, Jorge Enrique | Elaboración y planificación de Sprint 1 y task correspondientes, elaboración de mockups y wireframes de mobile app |
| 3.00 | 31/10/2024 | Espejo Macuri, Paolo Andre | Correcciones de entregable anterior y registro de commits de Sprint 2 |
| 3.10 | 31/10/2024 | Rios Jaimes, Jhonel Enrique | Correcciones de entregable anterior y registro de pantallas (Web App) de evidencias de desarrollo del Sprint 2 |
| 3.20 | 31/10/2024 | Sebastian Tasayco, Javier Martin | Correcciones de entregable anterior y redacción del contenido para Software Configuration Management |
| 3.30 | 31/10/2024 | Alejo Cardenas, Luis Angel | Correcciones de entregable anterior y elaboración de Sprint Planning |
| 3.40 | 31/10/2024 | onzales Carrión, Jorge Enrique | Correcciones de entregable anterior y elaboración de Sprint 2 |
| 4.00 | 19/11/2024 | Espejo Macuri, Paolo Andre | En base al matriz de responsabilidad, se encargó de realizar la documentación de historias de usuario de la aplicación embebida IoT|
| 4.10 | 19/11/2024 | Rios Jaimes, Jhonel Enrique | En base a la matriz de responsabildiad, se encargó de documentar los commits de desarrollo de la web app y el video de ejecución |
| 4.20 | 19/11/2024 | Sebastian Tasayco, Javier Martin | En base a la matriz de responsabilidad, se encargó de aplicar mejora continua y documentar los endpoints de la Edge API realizados junto con la evidencia de desarrollo |
| 4.30 | 19/11/2024 | Alejo Cardenas, Luis Angel | En base a la matriz de responsabilidad, se encargó de documentar la evidencia de desarrollo de los nuevos features de la aplicació móvil junto con los commits de la evidencia de desarrollo |
| 4.40 | 19/11/2024 | onzales Carrión, Jorge Enrique | En base a la matriz de responsabilidad, se encargó de planfiicar el Sprint 3 y documentar el Sprint Backlog 3, se encargó de documentar el desarrollo de la aplicación móvil y los logs de la evidencia de despliegue de los productos digitales |
---
# Project Report Collaboration Insights

TB1: Se han desarrollado las actividades correspondientes para la entrega TB1 en el siguiente repositorio de Github dentro de la organización del equipo:
Link de repositorio Github: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT)

Para la elaboración del informe se realizaron actividades tales como: 
- Redactar y graficar en formato Markdown los puntos designados al integrante y posteriormente realizar commits para que el avance se guarde. 
- Elaborar los artefactos en las herramientas indicadas y posteriormente obtener el enlace de imagen mediante "Issues" dentro del repositorio del informe
- Se realizaron reuniones para coordinar el avance de los puntos del informe, además comunicar las primeras versiones de arquitectura de la solución IOT
- Se realizaron branches dentro del repositorio del informe para separar el README.md principal en capitulos.
- Primera versión de Software Architecture, Strategic-Level Attribute-Driven Design, Strategic-Level Domain-Driven Design
- Lean UX Process
- Diseño y analisis de entrevistas
- Analisis de competidores
- User Stories y Product Backlog

![image](https://github.com/user-attachments/assets/4d2b9c97-0b59-41d0-9c6c-5607ff723378)
![image](https://github.com/user-attachments/assets/b934f9d7-383a-468e-b653-07ec33e7beb3)


TP: Se han desarrollado las actividades correspondientes para la entrega TP en el siguiente repositorio de Github dentro de la organización del equipo:
Link de repositorio Github: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT)

Para la elaboración del informe se realizaron actividades tales como: 
- Redactar y graficar en formato Markdown los puntos designados al integrante y posteriormente realizar commits para que el avance se guarde. 
- Elaborar los artefactos en las herramientas indicadas y posteriormente obtener el enlace de imagen mediante "Issues" dentro del repositorio del informe
- Se realizaron correcciones de los artefactos previamente evaluados
- Se desarrollaron 2 nuevos capitulos correspondientes a Solution UI Design y Product Implementation
- Se planificó y desarrollo el Sprint 1 y su alcance, landing page y primera versión de web apps

![image](https://github.com/user-attachments/assets/4e4e2db4-65a1-4161-97c5-85b08f759bac)


TB2: Se han desarrollado las actividades correspondientes para la entrega TB2 en el siguiente repositorio de Github dentro de la organización del equipo:
Link de repositorio Github: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT)

Para la elaboración del informe se realizaron actividades tales como: 
- Redactar y graficar en formato Markdown los puntos designados al integrante y posteriormente realizar commits para que el avance se guarde. 
- Elaborar los artefactos en las herramientas indicadas y posteriormente obtener el enlace de imagen mediante "Issues" dentro del repositorio del informe
- Se realizaron correcciones de los artefactos previamente evaluados
- Se desarrollaron 4 puntos nuevos relacionados a Validation Interviews y Evaluación según heuristicas
- Se desarrollaron la segunda version de Web App y Landing Page. Las primeras versiones de Mobile App, Embedded App, Edge Server y Web API fueron realizadas
- Jhonel Rios realizó la documentación de commits en sección Development Evidence del Sprint 2
- Luis Alejo realizó la redacción de la sección Configuration Management del Sprint 2
- Jorge Gonzales realizó la redacción del Sprin Planning y Sprint Backlog 2
- Javier Sebastian realizó la documentación de commits de pruebas de aceptación del Sprint 2
- Paolo Espejo realizó la documentación de Deployment Evidence y correcciones de mejora continua del Sprint 2

![imagen](https://github.com/user-attachments/assets/96a877f1-4003-4c04-b99d-7571c288549a)

TF: Se han desarrollado las actividades correspondientes para la entrega TB2 en el siguiente repositorio de Github dentro de la organización del equipo:
Link de repositorio Github: (https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT)

Para la elaboración del informe se realizaron actividades tales como: 


- Documentar los principales features realizados en el Sprint 3
- Planificar y registrar el Sprint Backlog 3 realizado por Jorge Gonzales
- Documentar los logs de los despliegues brindados por las herramientas por Jorge Gonzales
- Documentar el desarrollo de la aplicación embebida y la adición de las historias de usuario relacionadas a ello por Paolo Espejo
- Realizar la documentación de la evidencia de desarrollo y ejecución de la aplicación web para el Sprint 3 por Jhonel Rios
- Documentar lo realizado en el desarrollo del Edge API y documentar los endpoints relacionados al Sprint 3 por Javier Sebastian
- Sustentar el desarrollo de la aplicación móvil y su despliege en Firebase mediante la documentación de evidencia de desarrollo en el Sprint 3 por Luis Angel.
- Elaborar la mejora continua relacionada a artefactos previos como Architecutre Domain Driven Dessing (Domain Layer), User Stories, Referencias y 
- Redactar y graficar en formato Markdown los puntos designados al integrante y posteriormente realizar commits para que el avance se guarde. 
- Elaborar los artefactos en las herramientas indicadas y posteriormente obtener el enlace de imagen mediante "Issues" dentro del repositorio del informe

![imagen](https://github.com/user-attachments/assets/bf7b711b-9966-49cf-82f6-d9c7aad277a1)

---
# Contenido 
## Tabla de contenidos


## [Capítulo I: Introducción](#capítulo-i-introducción)
- [1.1. Startup Profile](#11-startup-profile)
  - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
  - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
- [1.2. Solution Profile](#12-solution-profile)
  - [1.2.1 Antecedentes y problemática](#121-antecedentes-y-problemática)
  - [1.2.2 Lean UX Process](#122-lean-ux-process)
    - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
    - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
    - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
    - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
- [1.3. Segmentos objetivo](#13-segmentos-objetivo)

## [Capítulo II: Requirements Elicitation & Analysis](#capítulo-ii-requirements-elicitation--analysis)
- [2.1. Competidores](#21-competidores)
  - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
  - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
- [2.2. Entrevistas](#22-entrevistas)
  - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
  - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
  - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
- [2.3. Needfinding](#23-needfinding)
  - [2.3.1. User Personas](#231-user-personas)
  - [2.3.2. User Task Matrix](#232-user-task-matrix)
  - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
  - [2.3.4. Empathy Mapping](#234-empathy-mapping)
  - [2.3.5. As-is Scenario Mapping](#235-as-is-scenario-mapping)
- [2.4. Ubiquitous Language](#24-ubiquitous-language)

## [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
- [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
- [3.2. User Stories](#32-user-stories)
- [3.3. Impact Mapping](#33-impact-mapping)
- [3.4. Product Backlog](#34-product-backlog)

## [Capítulo IV: Solution Software Design](#capítulo-iv-solution-software-design)
- [4.1. Strategic-Level Domain-Driven Design](#41-strategic-level-domain-driven-design)
  - [4.1.1. EventStorming](#411-eventstorming)
    - [4.1.1.1. Candidate Context Discovery](#4111-candidate-context-discovery)
    - [4.1.1.2. Domain Message Flows Modeling](#4112-domain-message-flows-modeling)
    - [4.1.1.3. Bounded Context Canvases](#4113-bounded-context-canvases)
  - [4.1.2. Context Mapping](#412-context-mapping)
  - [4.1.3. Software Architecture](#413-software-architecture)
    - [4.1.3.1. Software Architecture System Landscape Diagram](#4131-software-architecture-system-landscape-diagram)
    - [4.1.3.2. Software Architecture Context Level Diagrams](#4132-software-architecture-context-level-diagrams)
    - [4.1.3.3. Software Architecture Container Level Diagrams](#4133-software-architecture-container-level-diagrams)
    - [4.1.3.4. Software Architecture Deployment Diagrams](#4134-software-architecture-deployment-diagrams)
- [4.2. Tactical-Level Domain-Driven Design](#42-tactical-level-domain-driven-design)
  - [4.2.1. Bounded Context: IAM](#421-bounded-context-iam)
    - [4.2.1.1. Domain Layer](#4211-domain-layer)
    - [4.2.1.2. Interface Layer](#4212-interface-layer)
    - [4.2.1.3. Application Layer](#4213-application-layer)
    - [4.2.1.4. Infrastructure Layer](#4214-infrastructure-layer)
    - [4.2.1.6. Bounded Context Software Architecture Component Level Diagrams](#4216-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.1.7. Bounded Context Software Architecture Code Level Diagrams](#4217-bounded-context-software-architecture-code-level-diagrams)
      - [4.2.1.7.1. Bounded Context Domain Layer Class Diagrams](#42171-bounded-context-domain-layer-class-diagrams)
      - [4.2.1.7.2. Bounded Context Database Design Diagram](#42172-bounded-context-database-design-diagram)
  - [4.2.2. Bounded Context: Shopping](#422-bounded-context-shopping)
    - [4.2.2.1. Domain Layer](#4221-domain-layer)
    - [4.2.2.2. Interface Layer](#4222-interface-layer)
    - [4.2.2.3. Application Layer](#4223-application-layer)
    - [4.2.2.4. Infrastructure Layer](#4224-infrastructure-layer)
    - [4.2.2.6. Bounded Context Software Architecture Component Level Diagrams](#4226-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.2.7. Bounded Context Software Architecture Code Level Diagrams](#4227-bounded-context-software-architecture-code-level-diagrams)
  - [4.2.3. Bounded Context: Crop Registration](#423-bounded-context-crop-registration)
    - [4.2.3.1. Domain Layer](#4231-domain-layer)
    - [4.2.3.2. Interface Layer](#4232-interface-layer)
    - [4.2.3.3. Application Layer](#4233-application-layer)
    - [4.2.3.4. Infrastructure Layer](#4234-infrastructure-layer)
    - [4.2.3.6. Bounded Context Software Architecture Component Level Diagrams](#4236-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.3.7. Bounded Context Software Architecture Code Level Diagrams](#4237-bounded-context-software-architecture-code-level-diagrams)
  - [4.2.4. Bounded Context: Planification](#424-bounded-context-planification)
    - [4.2.4.1. Domain Layer](#4241-domain-layer)
    - [4.2.4.2. Interface Layer](#4242-interface-layer)
    - [4.2.4.3. Application Layer](#4243-application-layer)
    - [4.2.4.4. Infrastructure Layer](#4244-infrastructure-layer)
    - [4.2.4.6. Bounded Context Software Architecture Component Level Diagrams](#4246-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.4.7. Bounded Context Software Architecture Code Level Diagrams](#4247-bounded-context-software-architecture-code-level-diagrams)
  - [4.2.5. Bounded Context: Monitoring](#425-bounded-context-monitoring)
    - [4.2.5.1. Domain Layer](#4251-domain-layer)
    - [4.2.5.2. Interface Layer](#4252-interface-layer)
    - [4.2.5.3. Application Layer](#4253-application-layer)
    - [4.2.5.4. Infrastructure Layer](#4254-infrastructure-layer)
    - [4.2.5.6. Bounded Context Software Architecture Component Level Diagrams](#4256-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.5.7. Bounded Context Software Architecture Code Level Diagrams](#4257-bounded-context-software-architecture-code-level-diagrams)

## [Capítulo V: Solution UI/UX Design](#capítulo-v-solution-uiux-design)
- [5.1. Style Guidelines](#51-style-guidelines)
  - [5.1.1. General Style Guidelines](#511-general-style-guidelines)
  - [5.1.2. Web, Mobile and IoT Style Guidelines](#512-web-mobile-and-iot-style-guidelines)
- [5.2. Information Architecture](#52-information-architecture)
  - [5.2.1. Organization Systems](#521-organization-systems)
  - [5.2.2. Labeling Systems](#522-labeling-systems)
  - [5.2.3. SEO Tags and Meta Tags](#523-seo-tags-and-meta-tags)
  - [5.2.4. Searching Systems](#524-searching-systems)
  - [5.2.5. Navigation Systems](#525-navigation-systems)
- [5.3. Landing Page UI Design](#53-landing-page-ui-design)
  - [5.3.1. Landing Page Wireframe](#531-landing-page-wireframe)
  - [5.3.2. Landing Page Mock-up](#532-landing-page-mock-up)
- [5.4. Applications UX/UI Design](#54-applications-uxui-design)
  - [5.4.1. Applications Wireframes](#541-applications-wireframes)
  - [5.4.2. Applications Wireflow Diagrams](#542-applications-wireflow-diagrams)
  - [5.4.3. Applications Mock-ups](#543-applications-mock-ups)
  - [5.4.4. Applications User Flow Diagrams](#544-applications-user-flow-diagrams)
- [5.5. Applications Prototyping](#55-applications-prototyping)

## [Capítulo VI: Product Implementation, Validation & Deployment](#capítulo-vi-product-implementation-validation--deployment)
- [6.1. Software Configuration Management](#61-software-configuration-management)
  - [6.1.1. Software Development Environment Configuration](#611-software-development-environment-configuration)
  - [6.1.2. Source Code Management](#612-source-code-management)
  - [6.1.3. Source Code Style Guide & Conventions](#613-source-code-style-guide--conventions)
  - [6.1.4. Software Deployment Configuration](#614-software-deployment-configuration)
- [6.2. Landing Page, Services & Applications Implementation](#62-landing-page-services--applications-implementation)
  - [6.2.1. Sprint 1](#621-sprint-1)
    - [6.2.1.1. Sprint Planning 1](#6211-sprint-planning-1)
    - [6.2.1.2. Sprint Backlog 1](#6212-sprint-backlog-1)
    - [6.2.1.3. Development Evidence for Sprint Review](#6213-development-evidence-for-sprint-review)
    - [6.2.1.4. Testing Suite Evidence for Sprint Review](#6214-testing-suite-evidence-for-sprint-review)
    - [6.2.1.5. Execution Evidence for Sprint Review](#6215-execution-evidence-for-sprint-review)
    - [6.2.1.6. Services Documentation Evidence for Sprint Review](#6216-services-documentation-evidence-for-sprint-review)
    - [6.2.1.7. Software Deployment Evidence for Sprint Review](#6217-software-deployment-evidence-for-sprint-review)
    - [6.2.1.8. Team Collaboration Insights during Sprint](#6218-team-collaboration-insights-during-sprint)
  - [6.2.2. Sprint 2](#622-sprint-2)
    - [6.2.2.1. Sprint Planning 2](#6221-sprint-planning-2)
    - [6.2.2.2. Sprint Backlog 2](#6222-sprint-backlog-2)
    - [6.2.2.3. Development Evidence for Sprint Review](#6223-development-evidence-for-sprint-review)
    - [6.2.2.4. Testing Suite Evidence for Sprint Review](#6224-testing-suite-evidence-for-sprint-review)
    - [6.2.2.5. Execution Evidence for Sprint Review](#6225-execution-evidence-for-sprint-review)
    - [6.2.2.6. Services Documentation Evidence for Sprint Review](#6226-services-documentation-evidence-for-sprint-review)
    - [6.2.2.7. Software Deployment Evidence for Sprint Review](#6227-software-deployment-evidence-for-sprint-review)
    - [6.2.2.8. Team Collaboration Insights during Sprint](#6228-team-collaboration-insights-during-sprint)
  - [6.2.3. Sprint 3](#623-sprint-3)
    - [6.2.3.1. Sprint Planning 3](#6231-sprint-planning-3)
    - [6.2.3.2. Sprint Backlog 3](#6232-sprint-backlog-3)
    - [6.2.3.3. Development Evidence for Sprint Review](#6233-development-evidence-for-sprint-review)
    - [6.2.3.4. Testing Suite Evidence for Sprint Review](#6234-testing-suite-evidence-for-sprint-review)
    - [6.2.3.5. Execution Evidence for Sprint Review](#6235-execution-evidence-for-sprint-review)
    - [6.2.3.6. Services Documentation Evidence for Sprint Review](#6236-services-documentation-evidence-for-sprint-review)
    - [6.2.3.7. Software Deployment Evidence for Sprint Review](#6237-software-deployment-evidence-for-sprint-review)
    - [6.2.3.8. Team Collaboration Insights during Sprint](#6238-team-collaboration-insights-during-sprint)
- [6.3. Validation Interviews](#63-validation-interviews)
  - [6.3.1. Diseño de Entrevistas](#631-diseño-de-entrevistas)
  - [6.3.2. Registro de Entrevistas](#632-registro-de-entrevistas)
  - [6.3.3. Evaluaciones según heurísticas](#633-evaluaciones-segun-heuristicas)
- [6.4. Video About-the-Product](#64-video-about-the-product)


## [Conclusiones](#conclusiones)

## [Video About-the-Team](#video-about-the-teambout-the-Team)

## [Bibliografía](#bibliografía)

## [Anexos](#anexos)
---

# Student Outcome

El curso contribuye al cumplimiento del Student Outcome ABET:

ABET – EAC - Student Outcome 5

Criterio: La capacidad de funcionar efectivamente en un equipo cuyos miembros juntos proporcionan liderazgo, crean un entorno de colaboración e inclusivo, establecen objetivos, planifican tareas y cumplen objetivos. 

En el siguiente cuadro se describe las acciones realizadas y enunciados de 
conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro 
del ABET – EAC - Student Outcome 5.

| Criterio específico | Acciones realizadas | Conclusiones |
| - | - | - |
| Trabaja en equipo para proporcionar liderazgo en forma conjunta. | Espejo Macuri, Paolo Andre - TB1: Lideró el desarrollo de la backend de la aplicación móvil y participó en la integración de la app embebida IoT. <br> Gonzales Carrión, Jorge Enrique - TB1: Lideró la creación de la Landing Page y contribuyó en el desarrollo backend y la integración de la API de borde. <br> Alejo Cardenas, Luis Angel - TB1: Participó en el desarrollo del backend y contribuyó con la app embebida IoT y Edge API. <br> Rios Jaimes, Jhonel Enrique - TB1: Lideró el desarrollo del frontend de la aplicación web y participó en la integración con la app embebida IoT. <br> Sebastian Tasayco, Javier Martin - TB1: Contribuyó en el desarrollo de la app embebida IoT y la API de borde. <br><br> Espejo Macuri, Paolo Andre - TP: Contribuyó en la mejora continua de la backend y en la elaboración de la app móvil. <br> Gonzales Carrión, Jorge Enrique - TP: Participó en el desarrollo de la backend y lideró el diseño de la Landing Page. <br> Alejo Cardenas, Luis Angel - TP: Apoyó en el desarrollo de la backend y colaboró en la implementación de la app embebida IoT. <br> Rios Jaimes, Jhonel Enrique - TP: Contribuyó al desarrollo del frontend de la app web y al desarrollo de la app móvil. <br> Sebastian Tasayco, Javier Martin - TP: Participó en la implementación de la app embebida IoT y la API de borde. <br><br> Espejo Macuri, Paolo Andre - TB2: Realizó correcciones en la backend y documentó las funcionalidades de la app embebida IoT. <br> Rios Jaimes, Jhonel Enrique - TB2: Documentó las interfaces frontend de la Web App y colaboró en el desarrollo backend. <br> Gonzales Carrión, Jorge Enrique - TB2: Lideró la revisión de la Landing Page y la integración de la Edge API. <br> Alejo Cardenas, Luis Angel - TB2: Colaboró en la planificación y en la mejora del desarrollo backend. <br> Sebastian Tasayco, Javier Martin - TB2: Participó en la mejora de la app embebida IoT y contribuyó a la integración de la Edge API. <br><br> Espejo Macuri, Paolo Andre - TF: Documentó las historias de usuario relacionadas con la aplicación embebida IoT, asegurando claridad en los objetivos funcionales del sistema.<br>Rios Jaimes, Jhonel Enrique - TF: Documentó los commits de desarrollo de la web app y preparó el video de ejecución como evidencia, promoviendo la transparencia del trabajo realizado.<br>Sebastian Tasayco, Javier Martin - TF: Implementó mejoras continuas y documentó los endpoints de la Edge API, fortaleciendo la infraestructura de desarrollo.<br>Alejo Cardenas, Luis Angel - TF: Documentó las evidencias de los nuevos features de la aplicación móvil junto con los commits, asegurando trazabilidad y calidad del desarrollo.<br>Gonzales Carrión, Jorge Enrique - TF: Planificó el Sprint 3, documentó el Sprint Backlog y registró evidencias de desarrollo y logs del despliegue de productos digitales, consolidando el liderazgo del equipo. | TB1: Se evidenció un liderazgo compartido y una colaboración efectiva en el desarrollo de las áreas de backend, frontend y la app embebida IoT. <br> TP: El equipo demostró capacidad de organización y ejecución en el primer sprint, entregando una versión funcional de la Landing Page y la app móvil. <br> TB2: La planificación colaborativa y el liderazgo compartido facilitaron la ejecución de correcciones y mejoras, asegurando un entregable de calidad. <br> TF: El equipo demostró un alto nivel de liderazgo colaborativo, donde cada integrante asumió responsabilidades clave para fortalecer la documentación y planificación, asegurando el éxito del Sprint 3. Se destaca la capacidad de liderazgo compartido en diferentes etapas del proceso de desarrollo. |
| Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos. | Espejo Macuri, Paolo Andre - TB1: Planificó tareas de desarrollo de backend y contribuyó a la coordinación de la app embebida IoT. <br> Gonzales Carrión, Jorge Enrique - TB1: Lideró la planificación y el desarrollo de la Landing Page. <br> Alejo Cardenas, Luis Angel - TB1: Ayudó a establecer metas para el desarrollo backend y colaboró en la app embebida IoT. <br> Rios Jaimes, Jhonel Enrique - TB1: Planificó y ejecutó tareas de desarrollo frontend y contribuyó al desarrollo de la app móvil. <br> Sebastian Tasayco, Javier Martin - TB1: Aseguró la correcta ejecución de las tareas de la app embebida IoT y la API de borde. <br><br> Espejo Macuri, Paolo Andre - TP: Estableció objetivos para la mejora continua del backend y la app móvil. <br> Gonzales Carrión, Jorge Enrique - TP: Planificó el desarrollo de la backend y la Landing Page. <br> Alejo Cardenas, Luis Angel - TP: Apoyó la planificación y desarrollo backend y la implementación de la app embebida IoT. <br> Rios Jaimes, Jhonel Enrique - TP: Participó en la planificación del desarrollo de la app web y móvil. <br> Sebastian Tasayco, Javier Martin - TP: Aseguró el cumplimiento de objetivos relacionados con la app embebida IoT y la API de borde. <br><br> Espejo Macuri, Paolo Andre - TB2: Planificó y ejecutó correcciones en el backend, promoviendo un desarrollo colaborativo. <br> Rios Jaimes, Jhonel Enrique - TB2: Documentó las pantallas del frontend de la app web para asegurar trazabilidad. <br> Gonzales Carrión, Jorge Enrique - TB2: Lideró la planificación y revisión de la Edge API. <br> Alejo Cardenas, Luis Angel - TB2: Colaboró en la planificación del sprint y la mejora del backend. <br> Sebastian Tasayco, Javier Martin - TB2: Contribuyó a la integración de la app embebida IoT y la API de borde. <br><br> Espejo Macuri, Paolo Andre - TF: Lideró la documentación de historias de usuario para la aplicación embebida IoT, estableciendo metas claras para la funcionalidad del sistema.<br>Rios Jaimes, Jhonel Enrique - TF: Documentó los commits del desarrollo de la web app y preparó el video de ejecución, asegurando trazabilidad y comunicación efectiva.<br>Sebastian Tasayco, Javier Martin - TF: Implementó mejoras continuas y documentó los endpoints de la Edge API, alineando las tareas a los objetivos del sprint.<br>Alejo Cardenas, Luis Angel - TF: Documentó las evidencias del desarrollo de nuevos features para la aplicación móvil y los commits asociados, promoviendo la trazabilidad y la mejora colaborativa.<br>Gonzales Carrión, Jorge Enrique - TF: Planificó el Sprint 3, organizó el Sprint Backlog y registró los logs de despliegue, fomentando un entorno colaborativo con metas claras y bien definidas. | TB1: Se establecieron objetivos claros y se promovió un entorno inclusivo para cumplir con las metas en backend, frontend y la app embebida IoT. <br> TP: La planificación efectiva del equipo permitió cumplir con los requisitos de la app móvil y web, manteniendo el enfoque en la mejora continua. <br> TB2: La colaboración del equipo resultó en un cumplimiento exitoso de las tareas de revisión y desarrollo, contribuyendo a un avance sólido del proyecto. <br> TF: La planificación y la documentación realizadas por el equipo permitieron crear un entorno inclusivo y orientado al cumplimiento de objetivos, logrando avanzar de manera efectiva en el desarrollo de la web app, la aplicación móvil y los productos digitales embebidos. |



