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
| 1.00 | 15/08/2024 | Alejo Cardenas, Luis Angel | Elaboraciónd de Lean Ux Process, Diseño, analisis y registro de entrevistas  |
| 1.10 | 20/08/2024 | Espejo Macuri, Paolo Andre | Registro de entrevistas y diseño de entrevistas, bounded contexts tactical-level domain driven design |
| 1.20 | 21/08/2024 | Gonzales Carrión, Jorge Enrique| Creación de carátula, indice del informe, todos los puntos del capitulo 4, Registro de entrevistas y diseño de entrevistas, realizar el desarrollo del proceso Lean Ux|
| 1.30 | 21/08/2024 | Rios Jaimes, Jhonel Enrique | Desarrollo de User Journey Mapping y registro de entrevista |
| 1.40 | 01/09/2024 | Sebastian Tasayco, Javier Martin | Diseño, analisis y registro de entrevistas |


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




---
# Contenido 
## Tabla de contenidos


## [Capítulo I: Introducción](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#cap%C3%ADtulo-i-introducci%C3%B3n)
- [1.1. Startup Profile](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#11-startup-profile)
  - [1.1.1. Descripción de la Startup](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#111-descripci%C3%B3n-de-la-startup)
  - [1.1.2. Perfiles de integrantes del equipo](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#112-perfiles-de-integrantes-del-equipo)
- [1.2. Solution Profile](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#12-solution-profile)
  - [1.2.1 Antecedentes y problemática](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#121-antecedentes-y-problem%C3%A1tica)
  - [1.2.2 Lean UX Process](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#122-lean-ux-process)
    - [1.2.2.1. Lean UX Problem Statements](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#1221-lean-ux-problem-statements)
    - [1.2.2.2. Lean UX Assumptions](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#1221-lean-ux-problem-statements)
    - [1.2.2.3. Lean UX Hypothesis Statements](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#1221-lean-ux-problem-statements)
    - [1.2.2.4. Lean UX Canvas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#1224-lean-ux-canvas)
- [1.3. Segmentos objetivo](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20I%3A%20Introducci%C3%B3n.md#13-segmentos-objetivo)

## [Capítulo II: Requirements Elicitation & Analysis](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#cap%C3%ADtulo-ii-requirements-elicitation--analysis)
- [2.1. Competidores](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#21-competidores)
  - [2.1.1. Análisis competitivo](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#211-an%C3%A1lisis-competitivo)
  - [2.1.2. Estrategias y tácticas frente a competidores](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#212-estrategias-y-t%C3%A1cticas-frente-a-competidores)
- [2.2. Entrevistas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#22-entrevistas)
  - [2.2.1. Diseño de entrevistas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#221-dise%C3%B1o-de-entrevistas)
  - [2.2.2. Registro de entrevistas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#222-registro-de-entrevistas)
  - [2.2.3. Análisis de entrevistas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#223-an%C3%A1lisis-de-entrevistas)
- [2.3. Needfinding](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#23-needfinding)
  - [2.3.1. User Personas](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#231-user-personas)
  - [2.3.2. User Task Matrix](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#232-user-task-matrix)
  - [2.3.3. User Journey Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#233-user-journey-mapping)
  - [2.3.4. Empathy Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#234-empathy-mapping)
  - [2.3.5. As-is Scenario Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#235-as-is-scenario-mapping)
- [2.4. Ubiquitous Language](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20II%3A%20Requirements%20Elicitation%20%26%20Analysis.md#24-ubiquitous-language)

## [Capítulo III: Requirements Specification](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20III%3A%20Requirements%20Specification.md)
- [3.1. To-Be Scenario Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20III%3A%20Requirements%20Specification.md#31-to-be-scenario-mapping)
- [3.2. User Stories](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20III%3A%20Requirements%20Specification.md#32-user-stories)
- [3.3. Impact Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20III%3A%20Requirements%20Specification.md#33-impact-mapping)
- [3.4. Product Backlog](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20III%3A%20Requirements%20Specification.md#34-product-backlog)


## [Capítulo IV: Solution Software Design](#)
- [4.1. Strategic-Level Domain-Driven Design](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
- [4.1.1. EventStorming](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.1.1. Candidate Context Discovery](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.1.2. Domain Message Flows Modeling](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.1.3. Bounded Context Canvases](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
- [4.1.2. Context Mapping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
- [4.1.3. Software Architecture](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.3.1. Software Architecture System Landscape Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.3.2. Software Architecture Context Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.3.3. Software Architecture Container Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
  - [4.1.3.4. Software Architecture Deployment Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
- [4.2. Tactical-Level Domain-Driven Design](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#41-strategic-level-domain-driven-design)
- [4.2.1. Bounded Context: IAM](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#421-bounded-context-iam)
  - [4.2.1.1. Domain Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4211-domain-layer)
  - [4.2.1.2. Interface Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4212-interface-layer)
  - [4.2.1.3. Application Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4213-application-layer)
  - [4.2.1.4. Infrastructure Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4214-infrastructure-layer)
  - [4.2.1.6. Bounded Context Software Architecture Component Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4216-bounded-context-software-architecture-component-level-diagrams)
  - [4.2.1.7. Bounded Context Software Architecture Code Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4217-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.1.7.1. Bounded Context Domain Layer Class Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42171-bounded-context-domain-layer-class-diagrams)
    - [4.2.1.7.2. Bounded Context Database Design Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42172-bounded-context-database-design-diagram)
- [4.2.2. Bounded Context: Shopping](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#422-bounded-context-shopping)
  - [4.2.2.1. Domain Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4221-domain-layer)
  - [4.2.2.2. Interface Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4222-interface-layer)
  - [4.2.2.3. Application Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4223-application-layer)
  - [4.2.2.4. Infrastructure Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4224-infrastructure-layer)
  - [4.2.2.6. Bounded Context Software Architecture Component Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4226-bounded-context-software-architecture-component-level-diagrams)
  - [4.2.2.7. Bounded Context Software Architecture Code Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4227-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.2.7.1. Bounded Context Domain Layer Class Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42271-bounded-context-domain-layer-class-diagrams)
    - [4.2.2.7.2. Bounded Context Database Design Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42272-bounded-context-database-design-diagram)
- [4.2.3. Bounded Context: Crop Registration](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#423-bounded-context-crop-registration)
  - [4.2.3.1. Domain Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4231-domain-layer)
  - [4.2.3.2. Interface Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4232-interface-layer)
  - [4.2.3.3. Application Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4233-application-layer)
  - [4.2.3.4. Infrastructure Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4234-infrastructure-layer)
  - [4.2.3.6. Bounded Context Software Architecture Component Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4236-bounded-context-software-architecture-component-level-diagrams)
  - [4.2.3.7. Bounded Context Software Architecture Code Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4237-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.3.7.1. Bounded Context Domain Layer Class Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42371-bounded-context-domain-layer-class-diagrams)
    - [4.2.3.7.2. Bounded Context Database Design Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42372-bounded-context-database-design-diagram)
- [4.2.4. Bounded Context: Planification](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#424-bounded-context-planification)
  - [4.2.4.1. Domain Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4241-domain-layer)
  - [4.2.4.2. Interface Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4242-interface-layer)
  - [4.2.4.3. Application Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4243-application-layer)
  - [4.2.4.4. Infrastructure Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4244-infrastructure-layer)
  - [4.2.4.6. Bounded Context Software Architecture Component Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4246-bounded-context-software-architecture-component-level-diagrams)
  - [4.2.4.7. Bounded Context Software Architecture Code Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4247-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.4.7.1. Bounded Context Domain Layer Class Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42471-bounded-context-domain-layer-class-diagrams)
    - [4.2.4.7.2. Bounded Context Database Design Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42472-bounded-context-database-design-diagram)
- [4.2.5. Bounded Context: Monitoring](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#425-bounded-context-monitoring)
  - [4.2.5.1. Domain Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4251-domain-layer)
  - [4.2.5.2. Interface Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4252-interface-layer)
  - [4.2.5.3. Application Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4253-application-layer)
  - [4.2.5.4. Infrastructure Layer](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4254-infrastructure-layer)
  - [4.2.5.6. Bounded Context Software Architecture Component Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4256-bounded-context-software-architecture-component-level-diagrams)
  - [4.2.5.7. Bounded Context Software Architecture Code Level Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#4257-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.5.7.1. Bounded Context Domain Layer Class Diagrams](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42571-bounded-context-domain-layer-class-diagrams)
    - [4.2.5.7.2. Bounded Context Database Design Diagram](https://github.com/upc-202402-GreatMinds-SW74-Ayni-IoT/Informe-Final_IoT/blob/main/Cap%C3%ADtulo%20IV%3A%20Solution%20Software%20Design.md#42572-bounded-context-database-design-diagram)


## [Conclusiones]

## [Referencias]

## [Anexos]

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
| Trabaja en equipo para proporcionar liderazgo en forma conjunta. | Alejo Cardenas - TB1: Lideró el proceso de Lean UX y coordinó el diseño. <br> Luis Angel - TB1: Participó en la asignación de tareas y el registro de entrevistas. <br> Paolo Espejo: Contribuyó al diseño de entrevistas y al diseño táctico de bounded contexts en domain-driven design. <br> Jorge Gonzales: Lideró la creación de secciones clave del informe y el desarrollo de Lean UX. <br> Jhonel Rios: Participó en la creación de User Journey Mapping. <br> Sebastian Tasayco: Colaboró en el diseño, análisis y registro de entrevistas. | Se hizo un buen trabajo en equipo para liderar el desarrollo de los puntos que se requerian dentro del informe |
| Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos. | Alejo Cardenas - TB1: Estableció metas para el proceso de Lean UX y planificó tareas de diseño. <br> Luis Angel - TB1: Ayudó a cumplir con los objetivos de análisis y entrevistas. <br> Paolo Espejo: Estableció el plan para el registro de entrevistas y desarrolló el diseño táctico del domain-driven design. <br> Jorge Gonzales: Definió objetivos para el desarrollo de Lean UX y supervisó la creación de documentos estructurales del informe. <br> Jhonel Rios: Planificó y cumplió tareas de User Journey Mapping. <br> Sebastian Tasayco: Aseguró el cumplimiento de los objetivos de diseño y registro. | En esta primera entrega, se estableció un ambiente de colaboración y participación para establecer las metas, tareas y la inspección de cumplimiento de objetivos |
