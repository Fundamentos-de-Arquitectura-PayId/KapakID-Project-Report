<div align="center">

<img src="assets/report/portada/img-da8629b888.png" alt="Logo de la Universidad Peruana de Ciencias Aplicadas" width="110" />

<p><strong>Universidad Peruana de Ciencias Aplicadas</strong></p>
<p>Carrera de Ingeniería de Software</p>
<p><strong>1ASI0657 — Fundamentos de Arquitectura de Software</strong></p>
<p><strong>Sección / NRC: 15987</strong></p>
<p><strong>Trabajo Final</strong></p>
<h1>PayID</h1>
<p><strong>Docente:</strong> Wilder Aurelio Vega Calero</p>
<p><strong>Equipo:</strong> PayID</p>

<table align="center">
  <thead><tr><th>Código</th><th>Apellidos y nombres</th></tr></thead>
  <tbody>
    <tr><td>U20231C069</td><td>Mora Blas, Diego Alonzo</td></tr>
    <tr><td>U202319440</td><td>Mallqui Vilca, Dhilsen Armil</td></tr>
    <tr><td>U20221c576</td><td>Taquiri Calderón, Jhunior Giussepe</td></tr>
    <tr><td>U202319415</td><td>Tasayco Osorio, Raul Hiroshi</td></tr>
  </tbody>
</table>

<p><strong>Ciclo académico 2026-20</strong></p>
<p>Noviembre 2026</p>

</div>

## Registro de versiones del informe

<table align="center" width="95%">
  <thead>
    <tr><th>Versión</th><th>Fecha</th><th>Autor</th><th>Descripción de modificación</th></tr>
  </thead>
  <tbody>
    <tr><td align="center">1.0</td><td align="center">13/09/2026</td><td align="center">Equipo PayID</td><td>Informe inicial, registros de entrevistas y diagramas C4 de contexto, contenedores y componentes.</td></tr>
    <tr><td align="center">2.0</td><td align="center">Pendiente</td><td align="center">Mallqui Vilca, Dhilsen Armil</td><td>ADD Iteration 1: backlog arquitectónico, objetivo, conceptos de diseño e instanciación de elementos.</td></tr>
    <tr><td align="center">3.0</td><td align="center">22/11/2026</td><td align="center">Taquiri Calderón, Jhunior Giussepe</td><td>Actualización de Student Outcome, evidencias de sprints, despliegue, anexos y referencias del informe.</td></tr>
    <tr><td align="center">3.1</td><td align="center">22/11/2026</td><td align="center">Consolidación editorial</td><td>Reorganización de la estructura y conservación de los avances reportados por el equipo.</td></tr>
    <tr><td align="center">3.2</td><td align="center">22/11/2026</td><td align="center">Consolidación editorial</td><td>Portada centrada, registro de versiones simplificado, sección GitFlow e índice completo en el README raíz; Student Outcome y capítulos quedaron en archivos separados.</td></tr>
  </tbody>
</table>

## Project Report Collaboration Insights

Commits de los integrantes en este repositorio (historial de Git al 22/11/2026):

<table align="center" width="85%">
  <thead>
    <tr><th>Integrante</th><th>Usuario / autor de Git</th><th>Commits en este repositorio</th></tr>
  </thead>
  <tbody>
    <tr><td align="center">Mallqui Vilca, Dhilsen Armil</td><td align="center">DhilsenDevs (Dhilsen18)</td><td align="center">7 (05/09/2026)</td></tr>
    <tr><td align="center">Tasayco Osorio, Raul Hiroshi</td><td align="center">Dexter</td><td align="center">2 (12/09/2026)</td></tr>
    <tr><td align="center">Taquiri Calderón, Jhunior Giussepe</td><td align="center">GiussepeTC0410</td><td align="center">Versión 3.0 del informe (22/11/2026)</td></tr>
    <tr><td align="center">Mora Blas, Diego Alonzo</td><td align="center">—</td><td align="center">0</td></tr>
  </tbody>
</table>

El registro completo de commits de los integrantes en todos los repositorios está en el [Anexo F](capitulos/anexos/README.md#anexo-f-registro-completo-de-commits-de-los-integrantes).

## Repositorios del proyecto

<table align="center" width="65%">
  <thead>
    <tr><th>Repositorio</th><th>Contenido</th></tr>
  </thead>
  <tbody>
    <tr><td><a href="https://github.com/Fundamentos-de-Arquitectura-PayId/PayID-Landing-Page">PayID-Landing-Page</a></td><td>Landing page</td></tr>
    <tr><td><a href="https://github.com/Fundamentos-de-Arquitectura-PayId/PayID-Frontend-Web-Application">PayID-Frontend-Web-Application</a></td><td>Aplicación web (Vue)</td></tr>
    <tr><td><a href="https://github.com/Fundamentos-de-Arquitectura-PayId/PayID-Mobile-App">PayID-Mobile-App</a></td><td>Aplicación móvil (Flutter)</td></tr>
    <tr><td>PayID-Backend (privado)</td><td>Backend ASP.NET Core</td></tr>
    <tr><td><a href="https://github.com/Fundamentos-de-Arquitectura-PayId/StructurizrCodePayID">StructurizrCodePayID</a></td><td>Diagramas C4</td></tr>
  </tbody>
</table>

### Ramas del proyecto (GitFlow)

Se sigue el flujo de GitFlow en los repositorios del informe y del backend:

- `main`: versión estable del proyecto.
- `develop`: integración de cambios antes de incorporarlos a `main`.
- `feature/chapter-1`, `feature/chapter-2` y `feature/chapter-3`: trabajo por capítulos.
- `feature/final-report-v3`: consolidación de la versión del informe.

La aplicación web, la landing page y la app móvil trabajan principalmente desde `main`; por eso, GitFlow está aplicado de forma parcial en el conjunto del proyecto.

---

## Contenido

- [Student Outcome: ABET–EAC, SO3](capitulos/student-outcome/README.md#student-outcome)
### [Capítulo I: Introducción](capitulos/capitulo-i/README.md#chapter-1)
- [1.1 Startup Profile](capitulos/capitulo-i/README.md#11-startup-profile)
    - [1.1.1 Descripción de la Startup](capitulos/capitulo-i/README.md#111-descripción-de-la-startup)
    - [1.1.2 Perfiles de integrantes del equipo](capitulos/capitulo-i/README.md#112-perfiles-de-integrantes-del-equipo)
- [1.2 Solution Profile](capitulos/capitulo-i/README.md#12-solution-profile)
    - [1.2.1 Nombre de producto](capitulos/capitulo-i/README.md#121-nombre-de-producto)
    - [1.2.2 Antecedentes y Problemática](capitulos/capitulo-i/README.md#122-antecedentes-y-problemática)
    - [1.2.3 Lean UX Process](capitulos/capitulo-i/README.md#123-lean-ux-process)
      - [1.2.3.1 Problem Statements](capitulos/capitulo-i/README.md#1231-lean-ux-problem-statements)
      - [1.2.3.2 Assumptions](capitulos/capitulo-i/README.md#1232-lean-ux-assumptions)
      - [1.2.3.3 Hypothesis Statements](capitulos/capitulo-i/README.md#1233-lean-ux-hypothesis-statements)
      - [1.2.3.4 Lean UX Canvas](capitulos/capitulo-i/README.md#1234-lean-ux-canvas)
- [1.3 Segmentos objetivo](capitulos/capitulo-i/README.md#13-segmentos-objetivo)
### [Capítulo II: Requirements & Analysis](capitulos/capitulo-ii/README.md#chapter-2)
- [2.1 Competidores](capitulos/capitulo-ii/README.md#21-competidores)
    - [2.1.1 Análisis competitivo](capitulos/capitulo-ii/README.md#211-análisis-competitivo-comparativa)
    - [2.1.2 Estrategias y tácticas frente a competidores](capitulos/capitulo-ii/README.md#212-estrategias-y-tácticas-frente-a-competidores)
- [2.2 Entrevistas](capitulos/capitulo-ii/README.md#22-entrevistas)
    - [2.2.1 Diseño de entrevistas](capitulos/capitulo-ii/README.md#221-diseño-de-entrevistas)
      - [Preguntas para el segmento 1](capitulos/capitulo-ii/README.md#preguntas-para-el-segmento-1-estudiantes-universitarios)
      - [Preguntas para el segmento 2](capitulos/capitulo-ii/README.md#preguntas-para-el-segmento-2-padres-madres-o-tutores)
    - [2.2.2 Registro de entrevistas](capitulos/capitulo-ii/README.md#222-registro-de-entrevistas)
    - [2.2.3 Análisis de entrevistas](capitulos/capitulo-ii/README.md#223-análisis-de-entrevistas)
- [2.3 Needfinding](capitulos/capitulo-ii/README.md#23-needfinding)
    - [2.3.1 User Personas](capitulos/capitulo-ii/README.md#231-user-personas)
    - [2.3.2 User Task Matrix](capitulos/capitulo-ii/README.md#232-user-task-matrix)
    - [2.3.3 Empathy Maps](capitulos/capitulo-ii/README.md#233-empathy-maps)
    - [2.3.4 As-Is Scenario Mapping](capitulos/capitulo-ii/README.md#234-as-is-scenario-mapping)
    - [2.3.5 Big Picture EventStorming](capitulos/capitulo-ii/README.md#235-big-picture-eventstorming)
    - [2.3.6 Ubiquitous Language](capitulos/capitulo-ii/README.md#236-ubiquitous-language)
### [Capítulo III: Requirements Specification](capitulos/capitulo-iii/README.md#chapter-3)
- [3.1 To-Be Scenario Mapping](capitulos/capitulo-iii/README.md#chapter-3-tobe)
- [3.2 User Stories](capitulos/capitulo-iii/README.md#chapter-3-user-stories)
- [3.3 Impact Map](capitulos/capitulo-iii/README.md#chapter-3-impact-map)
- [3.4 Product Backlog](capitulos/capitulo-iii/README.md#chapter-3-product-backlog)
### [Capítulo IV: Product Architecture Design](capitulos/capitulo-iv/README.md#chapter-4)
- [4.1 Design Concepts, ViewPoints & ER Diagrams](capitulos/capitulo-iv/README.md#41-design-concepts-viewpoints--er-diagrams)
    - [4.1.1 Principles Statements](capitulos/capitulo-iv/README.md#411-principles-statements)
    - [4.1.2 Approaches Statements](capitulos/capitulo-iv/README.md#412-approaches-statements)
    - [4.1.3 Context Diagram](capitulos/capitulo-iv/README.md#413-context-diagram)
    - [4.1.4 Approach Driven ViewPoints Diagrams](capitulos/capitulo-iv/README.md#414-approach-driven-viewpoints-diagrams)
      - [Diagramas UML](capitulos/capitulo-iv/README.md#diagramas-uml)
      - [Vista de procesos](capitulos/capitulo-iv/README.md#vista-de-procesos)
    - [4.1.5 Database Diagram](capitulos/capitulo-iv/README.md#415-relational--non-relational-database-diagram)
    - [4.1.6 Design Patterns](capitulos/capitulo-iv/README.md#416-design-patterns)
    - [4.1.7 Tactics](capitulos/capitulo-iv/README.md#417-tactics)
- [4.2 Architectural Drivers](capitulos/capitulo-iv/README.md#42-architectural-drivers)
    - [4.2.1 Design Purpose](capitulos/capitulo-iv/README.md#421-design-purpose)
    - [4.2.2 Primary Functionality](capitulos/capitulo-iv/README.md#422-primary-functionality-primary-user-stories)
    - [4.2.3 Quality Attribute Scenarios](capitulos/capitulo-iv/README.md#423-quality-attribute-scenarios)
    - [4.2.4 Constraints](capitulos/capitulo-iv/README.md#424-constraints)
    - [4.2.5 Architectural Concerns](capitulos/capitulo-iv/README.md#425-architectural-concerns)
- [4.3 ADD Iterations](capitulos/capitulo-iv/README.md#43-add-iterations)
    - [4.3.1 Iteration 1: Global System Structure](capitulos/capitulo-iv/README.md#431-iteration-1-global-system-structure)
      - [4.3.1.1 Architectural Design Backlog](capitulos/capitulo-iv/README.md#add1-backlog)
      - [4.3.1.2 Establish Iteration Goal by Selecting Drivers](capitulos/capitulo-iv/README.md#add1-goal)
      - [4.3.1.3 Choose One or More Elements of the System to Refine](capitulos/capitulo-iv/README.md#add1-refine)
      - [4.3.1.4 Choose One or More Design Concepts That Satisfy the Selected Drivers](capitulos/capitulo-iv/README.md#add1-concepts)
      - [4.3.1.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces](capitulos/capitulo-iv/README.md#add1-elements)
      - [4.3.1.6 Sketch Views (C4 & UML) and Record Design Decisions](capitulos/capitulo-iv/README.md#add1-views)
      - [4.3.1.7 Analysis of Current Design and Review Iteration Goal (Kanban Board)](capitulos/capitulo-iv/README.md#add1-review)
    - [4.3.2 Iteration 2: Identity and Documents](capitulos/capitulo-iv/README.md#432-iteration-2-validación-de-identidad-y-gestión-de-documentos-digitales)
      - [4.3.2.1 Architectural Design Backlog](capitulos/capitulo-iv/README.md#add2-backlog)
      - [4.3.2.2 Establish Iteration Goal by Selecting Drivers](capitulos/capitulo-iv/README.md#add2-goal)
      - [4.3.2.3 Choose One or More Elements of the System to Refine](capitulos/capitulo-iv/README.md#add2-refine)
      - [4.3.2.4 Choose One or More Design Concepts That Satisfy the Selected Drivers](capitulos/capitulo-iv/README.md#add2-concepts)
      - [4.3.2.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces](capitulos/capitulo-iv/README.md#add2-elements)
      - [4.3.2.6 Sketch Views (C4 & UML) and Record Design Decisions](capitulos/capitulo-iv/README.md#add2-views)
      - [4.3.2.7 Analysis of Current Design and Review Iteration Goal (Kanban Board)](capitulos/capitulo-iv/README.md#add2-review)
    - [4.3.3 Iteration 3: Payments and Wallet](capitulos/capitulo-iv/README.md#433-iteration-3-pagos-recargas-y-billetera-digital)
      - [4.3.3.1 Architectural Design Backlog](capitulos/capitulo-iv/README.md#add3-backlog)
      - [4.3.3.2 Establish Iteration Goal by Selecting Drivers](capitulos/capitulo-iv/README.md#add3-goal)
      - [4.3.3.3 Choose One or More Elements of the System to Refine](capitulos/capitulo-iv/README.md#add3-refine)
      - [4.3.3.4 Choose One or More Design Concepts That Satisfy the Selected Drivers](capitulos/capitulo-iv/README.md#add3-concepts)
      - [4.3.3.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces](capitulos/capitulo-iv/README.md#add3-elements)
      - [4.3.3.6 Sketch Views (C4 & UML) and Record Design Decisions](capitulos/capitulo-iv/README.md#add3-views)
      - [4.3.3.7 Analysis of Current Design and Review Iteration Goal (Kanban Board)](capitulos/capitulo-iv/README.md#add3-review)
    - [4.3.4 Iteration 4: Security](capitulos/capitulo-iv/README.md#434-iteration-4-seguridad-autenticación-y-protección-de-datos)
      - [4.3.4.1 Architectural Design Backlog](capitulos/capitulo-iv/README.md#add4-backlog)
      - [4.3.4.2 Establish Iteration Goal by Selecting Drivers](capitulos/capitulo-iv/README.md#add4-goal)
      - [4.3.4.3 Choose One or More Elements of the System to Refine](capitulos/capitulo-iv/README.md#add4-refine)
      - [4.3.4.4 Choose One or More Design Concepts That Satisfy the Selected Drivers](capitulos/capitulo-iv/README.md#add4-concepts)
      - [4.3.4.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces](capitulos/capitulo-iv/README.md#add4-elements)
      - [4.3.4.6 Sketch Views (C4 & UML) and Record Design Decisions](capitulos/capitulo-iv/README.md#add4-views)
      - [4.3.4.7 Analysis of Current Design and Review Iteration Goal (Kanban Board)](capitulos/capitulo-iv/README.md#add4-review)
    - [4.3.5 Iteration 5: Notifications](capitulos/capitulo-iv/README.md#435-iteration-5-notificaciones-alertas-y-seguimiento-de-trámites)
      - [4.3.5.1 Architectural Design Backlog](capitulos/capitulo-iv/README.md#add5-backlog)
      - [4.3.5.2 Establish Iteration Goal by Selecting Drivers](capitulos/capitulo-iv/README.md#add5-goal)
      - [4.3.5.3 Choose One or More Elements of the System to Refine](capitulos/capitulo-iv/README.md#add5-refine)
      - [4.3.5.4 Choose One or More Design Concepts That Satisfy the Selected Drivers](capitulos/capitulo-iv/README.md#add5-concepts)
      - [4.3.5.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces](capitulos/capitulo-iv/README.md#add5-elements)
      - [4.3.5.6 Sketch Views (C4 & UML) and Record Design Decisions](capitulos/capitulo-iv/README.md#add5-views)
      - [4.3.5.7 Analysis of Current Design and Review Iteration Goal (Kanban Board)](capitulos/capitulo-iv/README.md#add5-review)
### [Capítulo V: Product Implementation, Validation & Deployment](capitulos/capitulo-v/README.md#chapter-5)
- [5.1 Testing Suites & General Patterns](capitulos/capitulo-v/README.md#chapter-5-testing)
    - [5.1.1 Backend Application Core Testing Suite](capitulos/capitulo-v/README.md#511-backend-application-core-testing-suite)
    - [5.1.2 Pattern Based Backend Applications](capitulos/capitulo-v/README.md#512-pattern-based-backend-applications)
    - [5.1.3 Pattern Based Custom Software Library](capitulos/capitulo-v/README.md#513-pattern-based-custom-software-library)
    - [5.1.4 Framework Pattern Driven Refactoring Report](capitulos/capitulo-v/README.md#514-framework-pattern-driven-refactoring-report)
- [5.2 Software Configuration Management](capitulos/capitulo-v/README.md#chapter-5-configuration)
    - [5.2.1 Software Development Environment](capitulos/capitulo-v/README.md#521-software-development-environment-configuration)
    - [5.2.2 Source Code Management](capitulos/capitulo-v/README.md#522-source-code-management)
    - [5.2.3 Style Guide](capitulos/capitulo-v/README.md#523-source-code-style-guide--conventions)
    - [5.2.4 Deployment Configuration](capitulos/capitulo-v/README.md#524-software-deployment-configuration)
      - [5.2.4.1 Container Packaging and Deployment Evidence](capitulos/capitulo-v/README.md#5241-container-packaging-and-deployment-evidence)
    - [5.2.5 Backend Code Structure](capitulos/capitulo-v/README.md#525-backend-code-structure-and-conventions)
- [5.3 Microservices Implementation](capitulos/capitulo-v/README.md#chapter-5-sprints)
    - [5.3.1 Sprint 1](capitulos/capitulo-v/README.md#531-sprint-1)
      - [5.3.1.1 Sprint Backlog 1](capitulos/capitulo-v/README.md#sprint1-backlog)
      - [5.3.1.2 Development Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint1-development)
      - [5.3.1.3 Testing Suite Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint1-testing)
      - [5.3.1.4 Execution Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint1-execution)
      - [5.3.1.5 Microservices Documentation Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint1-api-docs)
      - [5.3.1.6 Software Deployment Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint1-deployment)
      - [5.3.1.7 Team Collaboration Insights during Sprint](capitulos/capitulo-v/README.md#sprint1-collaboration)
      - [5.3.1.8 Kanban Board](capitulos/capitulo-v/README.md#sprint1-kanban)
    - [5.3.2 Sprint 2](capitulos/capitulo-v/README.md#532-sprint-2)
      - [5.3.2.1 Sprint Backlog 2](capitulos/capitulo-v/README.md#sprint2-backlog)
      - [5.3.2.2 Development Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint2-development)
      - [5.3.2.3 Testing Suite Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint2-testing)
      - [5.3.2.4 Execution Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint2-execution)
      - [5.3.2.5 Microservices Documentation Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint2-api-docs)
      - [5.3.2.6 Software Deployment Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint2-deployment)
      - [5.3.2.7 Team Collaboration Insights during Sprint](capitulos/capitulo-v/README.md#sprint2-collaboration)
      - [5.3.2.8 Kanban Board](capitulos/capitulo-v/README.md#sprint2-kanban)
    - [5.3.3 Sprint 3](capitulos/capitulo-v/README.md#533-sprint-3)
      - [5.3.3.1 Sprint Backlog 3](capitulos/capitulo-v/README.md#sprint3-backlog)
      - [5.3.3.2 Development Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint3-development)
      - [5.3.3.3 Testing Suite Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint3-testing)
      - [5.3.3.4 Execution Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint3-execution)
      - [5.3.3.5 Microservices Documentation Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint3-api-docs)
      - [5.3.3.6 Software Deployment Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint3-deployment)
      - [5.3.3.7 Team Collaboration Insights during Sprint](capitulos/capitulo-v/README.md#sprint3-collaboration)
      - [5.3.3.8 Kanban Board](capitulos/capitulo-v/README.md#sprint3-kanban)
    - [5.3.4 Sprint 4](capitulos/capitulo-v/README.md#534-sprint-4)
      - [5.3.4.1 Sprint Backlog 4](capitulos/capitulo-v/README.md#sprint4-backlog)
      - [5.3.4.2 Development Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint4-development)
      - [5.3.4.3 Testing Suite Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint4-testing)
      - [5.3.4.4 Execution Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint4-execution)
      - [5.3.4.5 Microservices Documentation Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint4-api-docs)
      - [5.3.4.6 Software Deployment Evidence for Sprint Review](capitulos/capitulo-v/README.md#sprint4-deployment)
      - [5.3.4.7 Team Collaboration Insights during Sprint](capitulos/capitulo-v/README.md#sprint4-collaboration)
      - [5.3.4.8 Kanban Board](capitulos/capitulo-v/README.md#sprint4-kanban)
- [5.4 Microservices Deployment](capitulos/capitulo-v/README.md#chapter-5-cloud)
    - [Cloud Architecture Diagram](capitulos/capitulo-v/README.md#541-cloud-architecture-diagram)
    - [Cloud Architecture Deployment](capitulos/capitulo-v/README.md#542-cloud-architecture-deployment)
### [Conclusiones (pendiente de incorporar)](capitulos/conclusiones/README.md#conclusiones)

- [Conclusiones y recomendaciones](capitulos/conclusiones/README.md#conclusiones-y-recomendaciones)
- [Video About-The-Team](capitulos/conclusiones/README.md#video-about-the-team)

### [Bibliografía](capitulos/referencias/README.md#referencias)

- [Referencias bibliográficas](capitulos/referencias/README.md#referencias)

### [Anexos](capitulos/anexos/README.md#anexos)

- [Anexos](capitulos/anexos/README.md#anexos)
  - [Anexo B: Performance Reports](capitulos/anexos/README.md#anexo-b-final-individual-member-performance-report)
  - [Anexo C: Matriz de rúbricas](capitulos/anexos/README.md#anexo-c-matriz-de-cumplimiento-de-rúbricas)
  - [Anexo D: Cronograma](capitulos/anexos/README.md#anexo-d-cronograma-de-entregables)
  - [Anexo E: Términos y condiciones](capitulos/anexos/README.md#anexo-e-términos-y-condiciones-de-servicio)
  - [Anexo F: Registro de commits](capitulos/anexos/README.md#anexo-f-registro-completo-de-commits-de-los-integrantes)

### [Links](capitulos/links/README.md#links)

- [Links del proyecto](capitulos/links/README.md#links)

### Sección complementaria

- [Uso de herramientas de IA](capitulos/uso-ia/README.md#uso-de-herramientas-de-ia)
