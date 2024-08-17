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

Agosto del 2024

---
# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de la modificación |
| - | - | - | - |
| 1.00 | 15/08/2024 | Alejo Cardenas, Luis Angel | |
| 1.10 | 20/08/2024 | Espejo Macuri, Paolo Andre |  |
| 1.20 | 21/08/2024 | Gonzales Carrión, Jorge Enrique| |
| 1.30 | 21/08/2024 | Rios Jaimes, Jhonel Enrique | |
| 1.40 | 01/09/2024 | Sebastian Tasayco, Javier Martin | |


---
# Project Report Collaboration Insights

TB1: Se han desarrollado las actividades correspondientes para la entrega TB1 en el siguiente repositorio de Github dentro de la organización del equipo:
Link de repositorio Github: (https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource)

Para la elaboración del informe se realizaron actividades tales como: 
- Redactar y graficar en formato Markdown los puntos designados al integrante y posteriormente realizar commits para que el avance se guarde. 
- Elaborar los artefactos en las herramientas indicadas y posteriormente obtener el enlace de imagen mediante "Issues" dentro del repositorio del informe
- Se realizaron reuniones para coordinar el avance de los puntos del informe, además comunicar los avances del Sprint 1 correspondiente a la Landing Page
- Se realizaron branches dentro del repositorio del informe para separar el README.md principal en capitulos.

(imagen de commit)


---
# Contenido 
## Tabla de contenidos


## [Capítulo I: Introducción](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md)
- [1.1. Startup Profile](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#11-startup-profile)
  - [1.1.1. Descripción de la Startup](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#111-descripci%C3%B3n-de-la-startup)
  - [1.1.2. Perfiles de integrantes del equipo](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#112-perfiles-de-integrantes-del-equipo)
- [1.2. Solution Profile](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#12-solution-profile)
  - [1.2.1 Antecedentes y problemática](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#121-antecedentes-y-problem%C3%A1tica)
  - [1.2.2 Lean UX Process](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#122-lean-ux-process)
    - [1.2.2.1. Lean UX Problem Statements](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#1221-lean-ux-problem-statements)
    - [1.2.2.2. Lean UX Assumptions](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#1222-lean-ux-assumptions)
    - [1.2.2.3. Lean UX Hypothesis Statements](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#1223-lean-ux-hypothesis-statements)
    - [1.2.2.4. Lean UX Canvas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#1224-lean-ux-canvas)
- [1.3. Segmentos objetivo](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20I:%20Introducci%C3%B3n.md#13-segmentos-objetivo)

## [Capítulo II: Requirements Elicitation & Analysis](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md)
- [2.1. Competidores](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#21-competidores)
  - [2.1.1. Análisis competitivo](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#211-an%C3%A1lisis-competitivo)
  - [2.1.2. Estrategias y tácticas frente a competidores](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#212-estrategias-y-t%C3%A1cticas-frente-a-competidores)
- [2.2. Entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#22-entrevistas)
  - [2.2.1. Diseño de entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#221-dise%C3%B1o-de-entrevistas)
  - [2.2.2. Registro de entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#222-registro-de-entrevistas)
  - [2.2.3. Análisis de entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#223-an%C3%A1lisis-de-entrevistas)
- [2.3. Needfinding](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#23-needfinding)
  - [2.3.1. User Personas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#231-user-personas)
  - [2.3.2. User Task Matrix](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#232-user-task-matrix)
  - [2.3.3. User Journey Mapping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#233-user-journey-mapping)
  - [2.3.4. Empathy Mapping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#234-empathy-mapping)
  - [2.3.5. As-is Scenario Mapping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20II:%20Requirements%20Elicitation%20%26%20Analysis.md#235-as-is-scenario-mapping)

## [Capítulo III: Requirements Specification](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20III:%20Requirements%20Specification.md)
- [3.1. To-Be Scenario Mapping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20III:%20Requirements%20Specification.md#31-to-be-scenario-mapping)
- [3.2. User Stories](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20III:%20Requirements%20Specification.md#32-user-stories)
- [3.3. Impact Mapping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20III:%20Requirements%20Specification.md#33-impact-mapping)
- [3.4. Product Backlog](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20III:%20Requirements%20Specification.md#34-product-backlog)

## [Capítulo IV: Product Design](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md)
- [4.1. Style Guidelines](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#41-style-guidelines)
  - [4.1.1. General Style Guidelines](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#411-general-style-guidelines)
  - [4.1.2. Web Style Guidelines](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#412-web-style-guidelines)
- [4.2. Information Architecture](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#42-information-architecture)
  - [4.2.1. Organization Systems](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#421-organization-systems)
  - [4.2.2. Labeling Systems](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#422-labeling-systems)
  - [4.2.3. SEO Tags and Meta Tags](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#423-seo-tags-and-meta-tags)
  - [4.2.4. Searching Systems](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#424-searching-systems)
  - [4.2.5. Navigation Systems](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#425-navigation-systems)
- [4.3. Landing Page UI Design](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#43-landing-page-ui-design)
  - [4.3.1. Landing Page Wireframe](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#431-landing-page-wireframe)
  - [4.3.2. Landing Page Mock-up](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#432-landing-page-mock-up)
- [4.4. Web Applications UX/UI Design](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#44-web-applications-uxui-design)
  - [4.4.1. Web Applications Wireframes](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#441-web-applications-wireframes)
  - [4.4.2. Web Applications Wireflow Diagrams](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#442-web-applications-wireflow-diagrams)
  - [4.4.3. Web Applications Mock-ups](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#442-web-applications-mock-ups)
  - [4.4.4. Web Applications User Flow Diagrams](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#443-web-applications-user-flow-diagrams)
- [4.5. Web Applications Prototyping](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#45-web-applications-prototyping)
- [4.6. Domain-Driven Software Architecture](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#46-domain-driven-software-architecture)
  - [4.6.1. Software Architecture Context Diagram](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#461-software-architecture-context-diagram)
  - [4.6.2. Software Architecture Container Diagrams](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#462-software-architecture-container-diagrams)
  - [4.6.3. Software Architecture Components Diagrams](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#463-software-architecture-components-diagrams)
- [4.7. Software Object-Oriented Design](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#47-software-object-oriented-design)
  - [4.7.1. Class Diagrams](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#471-class-diagrams)
  - [4.7.2. Class Dictionary](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#472-class-dictionary)
- [4.8. Database Design](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#48-database-design)
  - [4.8.1. Database Diagram](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20IV:%20Product%20Design.md#481-database-diagram)

## [Capítulo V: Product Implementation, Validation & Deployment](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md)
- [5.1. Software Configuration Management](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#51-software-configuration-management)
  - [5.1.1. Software Development Environment Configuration](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#511-software-development-environment-configuration)
  - [5.1.2. Source Code Management](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#512-source-code-management)
  - [5.1.3. Source Code Style Guide & Conventions](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#513-source-code-style-guide--conventions)
  - [5.1.4. Software Deployment Configuration](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#514-software-deployment-configuration)
- [5.2. Landing Page, Services & Applications Implementation](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#52-landing-page-services--applications-implementation)
  - [5.2.1. Sprint 1](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#521-sprint-1)
    - [5.2.1.1. Sprint Planning 1](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5211-sprint-planning-1)
    - [5.2.1.2. Sprint Backlog 1](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5212-sprint-backlog-1)
    - [5.2.1.3. Development Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5213-development-evidence-for-sprint-review)
    - [5.2.1.4. Testing Suite Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5214-testing-suite-evidence-for-sprint-review)
    - [5.2.1.5. Execution Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5215-execution-evidence-for-sprint-review)
    - [5.2.1.6. Services Documentation Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5216-services-documentation-evidence-for-sprint-review)
    - [5.2.1.7. Software Deployment Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5217-software-deployment-evidence-for-sprint-review)
    - [5.2.1.8. Team Collaboration Insights during Sprint](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5218-team-collaboration-insights-during-sprint)
  - [5.2.2. Sprint 2](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#522-sprint-2)
    - [5.2.2.1. Sprint Planning 2](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5221-sprint-planning-2)
    - [5.2.2.2. Sprint Backlog 2](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5222-sprint-backlog-2)
    - [5.2.2.3. Development Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5223-development-evidence-for-sprint-review)
    - [5.2.2.4. Testing Suite Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5224-testing-suite-evidence-for-sprint-review)
    - [5.2.2.5. Execution Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5225-execution-evidence-for-sprint-review)
    - [5.2.2.6. Services Documentation Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5226-services-documentation-evidence-for-sprint-review)
    - [5.2.2.7. Software Deployment Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5227-software-deployment-evidence-for-sprint-review)
    - [5.2.2.8. Team Collaboration Insights during Sprint](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5228-team-collaboration-insights-during-sprint)
  - [5.2.3. Sprint 3](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#523-sprint-3)
    - [5.2.3.1. Sprint Planning 3](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5231-sprint-planning-3)
    - [5.2.3.2. Sprint Backlog 3](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5232-sprint-backlog-3)
    - [5.2.3.3. Development Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5233-development-evidence-for-sprint-review)
    - [5.2.3.4. Testing Suite Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5234-testing-suite-evidence-for-sprint-review)
    - [5.2.3.5. Execution Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5235-execution-evidence-for-sprint-review)
    - [5.2.3.6. Services Documentation Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5236-services-documentation-evidence-for-sprint-review)
    - [5.2.3.7. Software Deployment Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5237-software-deployment-evidence-for-sprint-review)
    - [5.2.3.8. Team Collaboration Insights during Sprint](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5238-team-collaboration-insights-during-sprint)
  - [5.2.4. Sprint 4](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#524-sprint-4)
    - [5.2.4.1. Sprint Planning 4](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5241-sprint-planning-4)
    - [5.2.4.2. Sprint Backlog 4](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5242-sprint-backlog-4)
    - [5.2.4.3. Development Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5243-development-evidence-for-sprint-review)
    - [5.2.4.4. Testing Suite Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5244-testing-suite-evidence-for-sprint-review)
    - [5.2.4.5. Execution Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5245-execution-evidence-for-sprint-review)
    - [5.2.4.6. Services Documentation Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5246-services-documentation-evidence-for-sprint-review)
    - [5.2.4.7. Software Deployment Evidence for Sprint Review](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5247-software-deployment-evidence-for-sprint-review)
    - [5.2.4.8. Team Collaboration Insights during Sprint](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#5248-team-collaboration-insights-during-sprint)
- [5.3. Validation Interviews](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#53-validation-interviews)
    - [5.3.1. Diseño de Entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#531-dise%C3%B1o-de-entrevistas)
    - [5.3.2. Registro de Entrevistas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#532-registro-de-entrevistas)
    - [5.3.3. Evaluaciones según heurísticas](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#533-evaluaciones-seg%C3%BAn-her%C3%ADsticas)
- [5.4. Video About-the-Product](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/chapter-5/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#54-video-about-the-product)


## [Conclusiones](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#conclusiones)

## [Referencias](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#referencias)

## [Anexos](https://github.com/upc-pre-202302-GreatMinds-SW51/Informe-Final_OpenSource/blob/develop/Cap%C3%ADtulo%20V:%20Product%20Implementation%2C%20Validation%20%26%20Deployment.md#anexos)

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
| Trabaja en equipo para proporcionar liderazgo en forma conjunta. |  |  |
| Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos. |  |  |
