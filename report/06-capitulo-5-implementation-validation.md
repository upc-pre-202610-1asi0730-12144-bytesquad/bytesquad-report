## Capítulo V: Product Implementation, Validation & Deployment

### 5.1. Software Configuration Management

En la siguiente sección, detallaremos las herramientas, convenciones, referencias y configuraciones empleadas a lo largo del desarrollo de la plataforma FitNode Analytics. Estas decisiones establecen las bases para mantener la consistencia técnica durante todo el ciclo de vida del proyecto.

#### 5.1.1. Software Development Environment Configuration

En este apartado, se detallan las herramientas, plataformas y lenguajes utilizados por el equipo para el desarrollo técnico y operativo del proyecto. Los productos se clasifican en las siguientes categorías:

1. Project Management
2. Product UX/UI Design & Architecture
3. Software Development
4. Software Deployment

**1. Project Management:**
* **WhatsApp y Discord:** Canales principales para la comunicación síncrona, coordinación de reuniones diarias (Daily Stand-ups) y resolución de bloqueos técnicos.

**2. Product UX/UI Design & Architecture:**
* **Miro:** Plataforma de pizarra colaborativa empleada para la creación de los Scenario Maps (As-is y To-be) y flujos de procesos iniciales.
* **PlantUML (PUML):** Herramienta de modelado bajo el enfoque *Diagram-as-Code*, utilizada para estructurar la arquitectura del sistema mediante el modelo C4 y diagramas de clases UML.
* **Figma:** Software de diseño colaborativo utilizado para la elaboración de wireframes y prototipos interactivos de alta fidelidad para la Landing Page y la aplicación.
* **UXPressia:** Herramienta especializada para el diseño y documentación de los Customer Journey Maps y Personas, garantizando un enfoque centrado en el usuario.
* * **Trello:** Herramienta de gestión visual basada en tableros Kanban. Se utiliza para organizar el Product Backlog, planificar los Sprints y realizar el seguimiento detallado de las tareas del equipo.


**3. Software Development:**
* **JetBrains WebStorm:** Entorno de desarrollo integrado (IDE) utilizado para la codificación de la Landing Page y el Frontend de la aplicación web.
* **GitHub:** Plataforma central para el control de versiones distribuido y la gestión colaborativa del código fuente.
* **HTML:** Lenguaje de marcado utilizado para definir la estructura semántica y el contenido de la Landing Page.
* **CSS:** Hojas de estilo aplicadas para la maquetación responsiva (Flexbox/Grid), el diseño visual y las animaciones de la interfaz.
* **JavaScript:** Lenguaje de programación nativo utilizado para implementar la lógica de internacionalización (traducción de idiomas) y la interactividad del lado del cliente.
* **Vue.js:** Framework progresivo de JavaScript seleccionado para la construcción de la Frontend Web Application.
* **ASP.NET Core (C#):** Framework utilizado para el desarrollo de la API RESTful y la gestión de la lógica de negocio en el Backend.

**4. Software Deployment:**
* **GitHub Pages:** Servicio utilizado para el alojamiento gratuito y despliegue público de la Landing Page estática.

#### 5.1.2. Source Code Management

Para la gestión del código fuente, se utiliza GitHub como plataforma central de control de versiones y colaboración. Se han establecido repositorios independientes para asegurar la modularidad del proyecto.

**Organización en GitHub:** `https://github.com/SpotTrack`
* **Repositorio del Informe:** `https://github.com/SpotTrack/SpotTrack-report`
* **Repositorio de la Landing Page:** `https://github.com/SpotTrack/SpotTrack-website`
* **Repositorio del Frontend:** `https://github.com/SpotTrack/SpotTrack-webapp`
* **Repositorio del Backend:** `https://github.com/SpotTrack/SpotTrack-platform`

**Ramificación: GitFlow**

Se ha adoptado el modelo **GitFlow** para gestionar el flujo de trabajo, utilizando ramas efímeras que permiten un desarrollo paralelo y organizado. Las ramas base son:

* **`main`:** Rama de producción. Contiene exclusivamente código estable y versiones finales desplegadas.
* **`develop`:** Rama de integración. Aquí se consolidan todas las nuevas funcionalidades antes de pasar a la rama principal.
* **Feature Branches:** Ramas temporales creadas para el desarrollo de tareas específicas. Siguen la nomenclatura `feature/task-name` y se eliminan tras ser integradas en `develop`.

**Ejemplo de Ramas Feature para la Landing Page:**
* **`feature/landing-structure`:** Maquetación base del HTML semántico y configuración inicial de estilos CSS.
* **`feature/internationalization`:** Implementación de la lógica JavaScript para el cambio dinámico de idioma (i18n).
* **`feature/pricing-animations`:** Desarrollo de la sección de precios, incluyendo el resaltado del plan ideal y animaciones `@keyframes`.
* **`feature/login-integration`:** Creación del módulo de inicio de sesión (`login.html`) y su vinculación con el header.
* **`feature/form-validation`:** Implementación de validaciones de negocio en el formulario de contacto mediante JavaScript.

**Estilo de commits: Conventional Commits**

Para mantener un historial de cambios legible y estandarizado, el equipo sigue la convención **Conventional Commits**. Cada mensaje de commit debe comenzar con un prefijo que categorice el cambio:

* **`feat`:** Introducción de una nueva funcionalidad.
* **`fix`:** Corrección de un error o fallo.
* **`docs`:** Modificaciones exclusivas en la documentación o el informe.
* **`style`:** Cambios de formato, punto y coma, espacios, etc. (no afectan la lógica).
* **`refactor`:** Reestructuración de código que no añade funciones ni corrige errores.
* **`chore`:** Actualización de tareas de compilación, configuraciones de herramientas o dependencias.

#### 5.1.3. Source Code Style Guide & Conventions

En esta sección se definen las reglas básicas de escritura de código que el equipo sigue para mantener el proyecto ordenado y fácil de leer.

**Principios generales**
* **Idioma estándar:** Todo el código fuente y los comentarios técnicos se escriben en inglés.
* **Legibilidad:** Se utilizan nombres claros y descriptivos para variables y funciones, evitando abreviaturas confusas.
* **Organización:** Se separa estrictamente la estructura visual, los estilos y la lógica de programación.

**HTML**
* Los archivos terminan en `.html`.
* Se utilizan etiquetas semánticas como `<header>`, `<section>`, `<nav>` y `<footer>` para estructurar la página de forma lógica.
* Se incluye el atributo `alt` en las imágenes para mejorar la accesibilidad.
* Todos los atributos utilizan comillas dobles (`"`).

**CSS**
* Los archivos terminan en `.css`.
* Los selectores y las clases se nombran en minúsculas y separados por guiones medios (ejemplo: `.pricing-card`, `.btn-primary`).
* Se agrupan los estilos relacionados (por módulos) y se separan con comentarios para facilitar su búsqueda.
* Se define una paleta de colores base utilizando variables globales en el `:root` para mantener la consistencia en todo el diseño.

**JavaScript**
* Los archivos terminan en `.js`.
* Las variables y funciones se escriben usando el formato `camelCase` (ejemplo: `changeLanguage`, `currentLang`).
* Se evita por completo el uso de `var`. Se prioriza `const` para valores fijos y `let` para valores que van a cambiar.

**Vue.js (Frontend Web Application)**
* Los componentes deben nombrarse utilizando `PascalCase` (ejemplo: `MachineCard.vue`).
* Se seguirán las reglas básicas recomendadas por la guía oficial (**Vue Style Guide**) para mantener el orden en el código.

**C# y ASP.NET Core (Backend)**
* Las clases y métodos se nombran utilizando `PascalCase` (ejemplo: `MaintenanceController`).
* Todas las interfaces deben comenzar con la letra "I" mayúscula (ejemplo: `ITelemetryService`).
* Se respetarán las convenciones estándar de codificación de Microsoft para C#.

#### 5.1.4. Software Deployment Configuration

En esta sección se describe la configuración necesaria para desplegar cada uno de los componentes del proyecto: Landing Page, Frontend Web Application y RESTful Web Services. El objetivo es garantizar que el código fuente almacenado en nuestros repositorios de GitHub se integre y publique de manera funcional, segura y accesible para los usuarios finales.

**Despliegue de Landing Page**

La Landing Page promocional de SpotTrack fue desarrollada utilizando HTML5, CSS3 y Vanilla JavaScript. Para su publicación, se optó por **GitHub Pages**, un servicio de hosting nativo, seguro y optimizado para sitios web estáticos.

**Pasos de despliegue ejecutados:**

* Se creó el repositorio `SpotTrack-website` dentro de la organización de GitHub del equipo.
* Se integró el código fuente (HTML, CSS, JS) y los recursos multimedia (imágenes, iconos) mediante comandos Git.
* Desde los ajustes del repositorio (Settings > Pages), se habilitó el despliegue automático apuntando a la raíz (`/`) de la rama `main`.
* GitHub Actions procesó la solicitud y publicó el sitio web asignándole un certificado SSL gratuito y una URL pública.

* **Repositorio:** `https://github.com/SpotTrack/SpotTrack-website`
* **URL desplegada:** `https://spottrack.github.io/SpotTrack-website/`


### 5.2. Landing Page, Services & Applications Implementation
En esta sección se explica y evidencia el proceso de implementación, pruebas, documentación y despliegue del Landing Page, Web Services y Frontend Web Applications.

#### 5.2.1. Sprint 1

##### 5.2.1.1. Sprint Planning 1

| Sprint 1 | Sprint 1                                                                                                                                                           |
| :--- |:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning Background** |                                                                                                                                                                    |
| Date | 18-04-2026                                                                                                                                                         |
| Time | 20:45                                                                                                                                                              |
| Location | Via Discord                                                                                                                                                        |
| Prepared By | Gamero Miranda, Lui Mathias                                                                                                                                        |
| Attendees (to planning meeting) | Cataño Zarate Jesus Miguel, Gallardo Morales Carla Alejandra, Fernández Linares Alvaro Sebastian, Gamero Miranda Lui Mathias, Espinoza Orrego Valentino Andre      |
| Sprint 1 Review Summary | Durante este sprint se asignaron las responsabilidades individuales y se discutieron los requerimientos técnicos y visuales para el desarrollo de la Landing Page. |
| Sprint 1 Retrospective Summary | El equipo concluyó que el flujo de trabajo fue efectivo, logrando un código funcional y un despliegue exitoso de la Landing Page sin bloqueos mayores.             |
| **Sprint Goal & User Stories** |                                                                                                                                                                    |
| Sprint 1 Goal | Desarrollar y desplegar la Landing Page estática del proyecto, aplicando HTML, CSS y Vanilla JS para presentar la propuesta de valor de SpotTrack.                 |
| Sprint 1 Velocity | 42                                                                                                                                                                 |
| Sum of Story Points | 42                                                                                                                                                                 |

##### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member (Last Name, First Name) | GitHub Username | Requirements & Analysis | Landing Page Development | Configuration & Deployment |
| :---: | :---: |:-----------------------:|:------------------------:|:--------------------------:|
| Cataño Zarate, Jesus Miguel | jcus1510  |            C            |            C             |             C              |
| Espinoza Orrego, Valentino Andre | valentinoespinoza13  |            L            |            C             |             C              |
| Fernández Linares, Alvaro Sebastian | ORION-tech-c  |            C            |            C             |             C              |
| Gamero Miranda, Lui Mathias | lug07m  |            C            |            L             |             C              |
| Gallardo Morales, Carla Alejandra | Carlsss28 |            C            |            C             |             L              |

##### 5.2.1.3. Sprint Backlog 1

En esta sección se detallan las tareas asignadas para el Sprint 1 y el link del tablero de trello.

**Link del tablero:** https://trello.com/b/6LoJKkoI/sprint-backlog

| User Story ID | Id | Description | Estimation (hours) | Assigned to | Status (To-do / InProcess / To-Review / Done) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| US-01 | S-01 | Diseñar la estructura HTML5 con semantic tags para la sección principal (Hero Section). | 4h | Gamero Miranda, Lui Mathias | Done |
| US-01 | S-02 | Implementar la lógica Vanilla JS para el cambio de idioma (i18n) en el navbar y botones. | 2h | Gamero Miranda, Lui Mathias | Done |
| US-01 | S-03 | Ajustar el estilo CSS usando Flexbox para destacar el CTA y adaptarlo a móviles. | 3h | Fernández Linares, Alvaro | Done |
| US-02 | S-04 | Diseñar la estructura de tarjetas HTML para la sección "About Us" y "Experiences". | 3h | Gamero Miranda, Lui Mathias | Done |
| US-02 | S-05 | Redactar diccionarios JS (EN/ES) explicando los beneficios B2B y B2C del producto. | 2h | Espinoza Orrego, Valentino | Done |
| US-02 | S-06 | Aplicar estilos corporativos utilizando las variables CSS globales (`:root`). | 3h | Fernández Linares, Alvaro | Done |
| US-03 | S-07 | Maquetar el componente CSS Grid para mostrar las características (Features) de IoT. | 4h | Gallardo Morales, Carla | Done |
| US-03 | S-08 | Añadir transiciones CSS (`hover` state) y manipular el DOM para la navegación. | 4h | Fernández Linares, Alvaro | Done |
| US-03 | S-09 | Integrar íconos vectoriales de FontAwesome dentro de las grillas de información. | 3h | Gamero Miranda, Lui Mathias | Done |
| US-04 | S-10 | Diseñar la estructura HTML de la sección de suscripciones (Planes Basic, Mid y Platinum). | 4h | Gamero Miranda, Lui Mathias | Done |
| US-04 | S-11 | Estilizar con animaciones `@keyframes` el plan "Mid" para resaltarlo como opción popular. | 2h | Fernández Linares, Alvaro | Done |
| US-05 | S-12 | Implementar la estructura del formulario B2B en el archivo principal y en `login.html`. | 3h | Gamero Miranda, Lui Mathias | Done |
| US-05 | S-13 | Añadir manipulación de eventos en JS (`preventDefault`) para el envío de formularios. | 3h | Gallardo Morales, Carla | Done |
| US-05 | S-14 | Verificar la subida de los commits a GitHub y asegurar la integridad de ramas GitFlow. | 2h | Cataño Zarate, Jesus | Done |

#### 5.2.1.4. Development Evidence for Sprint Review

| Repository        | Branch  | Commit Id                              | Commit Message                | Commit Message Body          | Commit on (Date) |
|-------------------|---------|----------------------------------------|-------------------------------|------------------------------|------------------|
| SpotTrack-website | develop |cd7207c544f9ec13272766754d752cdc7ba9a871|feat:add-landing-1             |feat:add-landing-1            | 26/042026        |
| SpotTrack-website | develop |ce6d742d7e1f835abc6ce1e5489513f11a057640|docs: update del main en el landingpage |docs: update del main en el landingpage | 26/042026        |
| SpotTrack-website | develop |614e9f04f22d42fd1852086b91e8c4574a1fbe21|added-some-sections-to-index   |added-some-sections-to-index  | 26/042026        |
| SpotTrack-website | develop |e69be6fe7671b3e2e832f7f230ffe8a58dee1eca|feature:add footer and contact |feature:add footer and contact| 26/042026        |
| SpotTrack-website | develop |f34a15c79dd45c8f97c8bd460e58be220d23fe4b|landing:add login              |landing:add login             | 26/042026        |




| Repository       | Branch  | Commit Id                                | Commit Message                                                      | Commit Message Body                                                   | Committed on (Date) |
|------------------|----------|------------------------------------------|---------------------------------------------------------------------|------------------------------------------------------------------------|---------------------|
| spottrack-webapp | develop  |                                          | docs:analytics section added                                        | docs:analytics section added                                          | 2026-05-14 |
| spottrack-webapp | develop  | 54e1fb69ab26386f1d811d3311e5252c6258073f | Merge pull request #12 from SpotTrack/feature/maintenance-section   | docs: maintenance section added                                       | 2026-05-14 |
| spottrack-webapp | develop  | b85561c985b4ece85457bf62e362e0fb398e9cb1 | Merge pull request #14 from SpotTrack/feature/configuration         | add feature/configuration                                             | 2026-05-14 |
| spottrack-webapp | develop  | c77f3b370222b4324be01c45b29a071e389fc52c | add feature/configuration                                           | add feature/configuration                                             | 2026-05-14 |
| spottrack-webapp | develop  | 1144f26cb339b4aff1d1bd89126e7d54df66de41 | docs: maintenance section added                                     | docs: maintenance section added                                       | 2026-05-14 |
| spottrack-webapp | develop  | dc2ab8560a6b4cde84196a355dd04c287ebb46ba | Merge pull request #10 from SpotTrack/feature/client-home-view      | feat: add-client-home                                                 | 2026-05-14 |
| spottrack-webapp | develop  | 325d312445e74d15b19e753b4427b2a8f84340fc | Merge pull request #11 from SpotTrack/feature/profiles              | add feature/profiles                                                  | 2026-05-14 |
| spottrack-webapp | develop  | 1aafc318356a05a906e69f275c27b55128d01316 | add feature/profiles                                                | add feature/profiles                                                  | 2026-05-14 |
| spottrack-webapp | develop  | 521931e4dca607548ad93fb7f23eece976b4c2a5 | Merge pull request #9 from SpotTrack/feature/iot-section            | docs: iot section added                                               | 2026-05-14 |
| spottrack-webapp | develop  | a2788e5f9c5dd1fa9ffd0e9637ead421c5273a4b | docs: iot section added                                             | docs: iot section added                                               | 2026-05-14 |
| spottrack-webapp | develop  | 7b7e32b1268e894c73bbd2b7ba9ec8b80d0ea5ee | Merge pull request #8 from SpotTrack/feature/alert                  | add feature/alerts                                                    | 2026-05-14 |
| spottrack-webapp | develop  | 95c5a755a5f62bdb39dcacf45357e55807c5c6fd | add feature/alerts                                                  | add feature/alerts                                                    | 2026-05-14 |
| spottrack-webapp | develop  | 6dcabecc9c6a92aa728a906d29a03edc60c73d0b | feat: add-client-home                                               | feat: add-client-home                                                 | 2026-05-14 |
| spottrack-webapp | develop  | 3bdbb9857f2fb2f0f3447de3c955081f1abe1632 | Merge pull request #7 from SpotTrack/feature/more-sections          | Feature/more sections                                                 | 2026-05-14 |
| spottrack-webapp | develop  | 949a5e1a5b4788e757619b2cfacce86eaceec965 | new section map merge corebounded context with reservation          | new section map merge corebounded context with reservation            | 2026-05-14 |
| spottrack-webapp | develop  | 63a698c060d745015c7535cb7286132bcc46f722 | new section reservation trying to attach like a core bounded context| new section reservation trying to attach like a core bounded context  | 2026-05-14 |
| spottrack-webapp | develop  | e7222b61c8af24eb05337e9e413eb2a130537766 | routines section propertly working                                  | routines section propertly working                                    | 2026-05-14 |
| spottrack-webapp | develop  | 38a368a2d5912034b23e4a72a09e192a5552482b | Merge pull request #6 from SpotTrack/feature/add-auth               | feat:add-auth                                                         | 2026-05-14 |
| spottrack-webapp | develop  | 997f18d91df91d13546552b06bc793257aca5e52 | feat:add-auth                                                       | feat:add-auth                                                         | 2026-05-14 |
| spottrack-webapp | develop  | 29fc2a1725ee5373997d41775339140a0b11092b | Merge pull request #4 from SpotTrack/feature/add-dashboard          | feat:add-dashboard                                                    | 2026-05-14 |
| spottrack-webapp | develop  | aba5fe314604be92b2540c178140b8014271a090 | feat:add-dashboard                                                  | feat:add-dashboard                                                    | 2026-05-14 |
| spottrack-webapp | develop  | ca81506115fdf1c7fdc1b55ad44cbaf59635dbbf | Merge pull request #3 from SpotTrack/feature/add-app-functions      | feat:add-app-functions                                                | 2026-05-14 |
| spottrack-webapp | develop  | 91134babc32aaffefd03462df6a0cb54956712a1 | feat:add-app-functions                                              | feat:add-app-functions                                                | 2026-05-14 |
| spottrack-webapp | develop  | 08007a915d7d8755f223d897fc21317b35a0b7ed | Merge pull request #2 from SpotTrack/feature/initialfiles           | initial files                                                         | 2026-05-14 |
| spottrack-webapp | develop  | de9b00651a8528fd3c4872bf7e2db2af6f712165 | initial files                                                       | initial files                                                         | 2026-05-14 |
| spottrack-webapp | develop  | 3f919b629f81d00225b8e15aabea5909221dee1e | Initial commit                                                      | Initial commit                                                        | 2026-04-08 |



| Repository         | Branch  | Commit Id                                | Commit Message                                                              | Commit Message Body                                             | Committed on (Date) |
|--------------------|----------|------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|---------------------|
| spottrack-platform | develop  | 2abbd801f9850abe110ad5c00381004527bddf0a | Add or update the Azure App Service build and deployment workflow config    | Add or update the Azure App Service build and deployment workflow config | 2026-05-14 |
| spottrack-platform | develop  | 6b64d79a3da2bdbb7f07630cd71aa4f708ad5a42 | Merge pull request #3 from SpotTrack/develop                                | Develop                                                         | 2026-05-14 |
| spottrack-platform | develop  | 1d0f6cd5b0ddfb6b186466a24239fa87c2356fe6 | Merge pull request #2 from SpotTrack/fix/remove-unnecessary-files           | Delete .idea directory                                          | 2026-05-14 |
| spottrack-platform | develop  | 499433598782db8affb69b097dca9c6126ecfe8d | Delete .idea directory                                                      | Delete .idea directory                                          | 2026-05-14 |
| spottrack-platform | develop  | 8f75d9cb66eeb66a466d9fc95e99eda6db24b49c | Merge pull request #1 from SpotTrack/feature/mockapi                        | initial changes to mockapi base                                | 2026-05-14 |
| spottrack-platform | develop  | f805fa1b4cb596b48a5dfe3de54d6315be5a3ddd | initial changes to mockapi base                                             | initial changes to mockapi base                                | 2026-05-14 |
| spottrack-platform | develop  | 81f28b4055001d75d2a7dda1c50ee9db70108efa | Initial commit                                                              | Initial commit                                                  | 2026-04-08 |
##### 5.2.1.5. Execution Evidence for Sprint Review

En esta entrega, el equipo de desarrolladores de SpotTrack ha completado con éxito la implementación y el lanzamiento de la página de la Landing Page. Esta página presenta diferentes secciones que brindan información detallada sobre nuestro producto.

<img src="../assets/landing/landing1.png" alt="bounded" width="500"/>
<img src="../assets/landing/landing2.png" alt="bounded" width="500"/>
<img src="../assets/landing/landing3.png" alt="bounded" width="500"/>
<img src="../assets/landing/landing4.png" alt="bounded" width="500"/>
<img src="../assets/landing/landing5.png" alt="bounded" width="500"/>
<img src="../assets/landing/landing6.png" alt="bounded" width="500"/>

##### 5.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1, se llevó a cabo la publicación de la Landing Page de SpotTrack empleando GitHub Pages como servicio de hosting. A continuación, se detallan las acciones realizadas para lograr su despliegue exitoso.

Se creó el repositorio denominado SpotTrack-website dentro de la organización upc-pre-202610-1asi0730-12144-SpotTrack en GitHub.

El desarrollo de la Landing Page se realizó en la rama develop, siguiendo el modelo de trabajo GitFlow.

Se verificó el despliegue exitoso accediendo a la URL pública: https://spottrack.github.io/SpotTrack-website/ 

##### 5.2.1.7. Software Deployment Evidence for Sprint Review

Se desplegó la landing page usando el servicio de GitHub Pages. Se configuró para utilizar la rama main como base del proyecto a desplegar.

<img src="../assets/landing/landing1.png" alt="bounded" width="500"/>

URL de Landing Page Desplegada: https://spottrack.github.io/SpotTrack-website/ 

##### 5.2.1.8. Team Collaboration Insights during Sprint

A continuación todas las estadisticas que nos proporciona Github, en su apartado de Insights, sobre la colaboración del equipo el reporte.

<img src="../assets/evidence-insights.png" alt="bounded" width="500"/>



#### 5.2.2. Sprint 2

##### 5.2.2.1 Sprint Planning 2

El presente apartado detalla los acuerdos y objetivos definidos durante el Sprint Planning Meeting de nuestra segunda iteración. Para este Sprint, el equipo se enfocó en dos frentes de trabajo simultáneos: (1) la corrección y completitud de todos los artefactos pendientes del Sprint 1, incluyendo el despliegue completo de la Landing Page; y (2) el inicio del desarrollo frontend de la Web Application principal (Vue.js), empleando una Fake API (JSON Server) como capa de datos simulada para desacoplar el desarrollo frontend del backend real, cuya implementación se reserva para el Sprint 3.

| Aspect | Details |
| :--- | :--- |
| **Sprint #** | Sprint 2 |
| **Date** | 2026-05-08 |
| **Time** | 10:00 AM |
| **Location** | Reunión Virtual (Discord / Microsoft Teams) |
| **Prepared By** | Gallardo, Carla |
| **Attendees (to planning meeting)** | Gamero, Lui / Gallardo, Carla / Cataño Zarate, Jesus Miguel / Espinoza Orrego, Valentino Andre / Fernández Linares, Alvaro Sebastian |
| **Sprint n – 1 Review Summary** | Sprint 1 entregó los artefactos fundacionales de Lean UX, DDD, diseño UX/UI en Figma y el inicio de la Landing Page (Hero Section y Header). Sin embargo, quedaron pendientes el despliegue, las secciones de módulos, precios y contacto de la Landing Page, así como diversas secciones de documentación del informe. |
| **Sprint n – 1 Retrospective Summary** | El equipo identificó que la carga de trabajo de documentación y diseño subestimó el tiempo necesario. Para este Sprint 2 se priorizará paralelizar la corrección de Sprint 1 con el inicio del desarrollo de la Web App, asignando responsables claros por cada frente. |
| **Sprint Goal** | Nuestro enfoque es completar todos los artefactos pendientes del Sprint 1 (correcciones de documentación y Landing Page completa) e iniciar el desarrollo frontend de la Web Application de SpotTrack consumiendo una Fake API, implementando las vistas de autenticación, mapa de calor, gestión de activos, alertas de mantenimiento y sugerencias de rutinas. Esto se confirmará cuando la Landing Page esté desplegada y funcional con todas sus secciones, y las vistas frontend de las User Stories priorizadas estén implementadas y navegables en el entorno de desarrollo local. |
| **Sprint n Velocity** | 58 Story Points |
| **Sum of Story Points** | 58 |

##### 5.2.2.2 Aspect Leaders and Collaborators

Para este Sprint 2, el equipo adoptó una estructura dual de trabajo: un subequipo dedicado a las correcciones del Sprint 1 (documentación + Landing Page) y otro enfocado en el desarrollo frontend de la Web Application. Esta división permite avanzar en paralelo sin bloqueos entre tareas de distinta naturaleza.

| Team Member (Last Name, First Name) | GitHub Username | Aspect 1: Sprint 1 Corrections Leader (L) / Collaborator (C) | Aspect 2: Vue App Setup & Auth Leader (L) / Collaborator (C) | Aspect 3: Client App Frontend (Heatmap & Routines) Leader (L) / Collaborator (C) | Aspect 4: Admin Dashboard Frontend Leader (L) / Collaborator (C) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Gallardo, Carla | cgallardo | Corrections (C) | Vue App Setup (L) | Client App (C) | Admin Dashboard (C) |
| Gamero, Lui | lgamero | Corrections (C) | Fake API Config (L) | Client App (C) | Admin Dashboard (C) |
| Cataño Zarate, Jesus Miguel | jcuz1510 | Landing Page Completion (L) | Vue App Setup (C) | Client App (C) | Admin Dashboard (C) |
| Espinoza Orrego, Valentino Andre | valentinoespinoza13 | Corrections (C) | Vue App Setup (C) | Client App (C) | Admin Dashboard (L) |
| Fernández Linares, Alvaro Sebastian | ORION-tech-c | Corrections (L) | Vue App Setup (C) | Client App (L) | Admin Dashboard (C) |

#### 5.2.2.3 Sprint Backlog

> **Nota:** Las filas con prefijo `CORR-` y `SETUP-` son **storyless** — no corresponden a ninguna User Story y no tienen Story Points asignados, pero son obligatorias para subsanar deficiencias del Sprint anterior y preparar el entorno de desarrollo.

| Id | Title | Task Id | Task Title | Description | Estimation (Hours) | Assigned To | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| - | Corrección Sprint 1 | CORR-01 | Completar sección "The Solution" en Landing Page | Maquetar las seis tarjetas de soluciones del sistema (US-03 pendiente) con HTML/CSS responsivo. | 4 hrs | Cataño | Done |
| - | Corrección Sprint 1 | CORR-02 | Completar Pricing Table en Landing Page | Implementar la tabla comparativa de planes SaaS Basic/Mid/Platinum con CTAs (US-04 pendiente). | 4 hrs | Cataño | Done |
| - | Corrección Sprint 1 | CORR-03 | Completar formulario de Contacto en Landing Page | Codificar el formulario de contacto con validaciones JavaScript (US-05 pendiente). | 4 hrs | Espinoza | Done |
| - | Corrección Sprint 1 | CORR-04 | Completar Navbar y Footer de Landing Page | Implementar la barra de navegación sticky con anchor links y el footer con enlaces institucionales (US-06 pendiente). | 4 hrs | Fernández | Done |
| - | Corrección Sprint 1 | CORR-05 | Despliegue de Landing Page en producción | Configurar y publicar la Landing Page en GitHub Pages (T08 pendiente). Documentar el enlace de producción. | 4 hrs | Gallardo | Done |
| - | Corrección Sprint 1 | CORR-06 | Completar Diagrama ERD y Diagrama de Clases | Finalizar y subir el ERD y el Diagrama de Clases UML al repositorio (T04 pendiente). Actualizar referencias en el informe. | 4 hrs | Gamero / Cataño | Done |
| - | Corrección Sprint 1 | CORR-07 | Completar evidencias del Sprint 1 en el informe | Añadir capturas de pantalla de la Landing Page, commits reales y métricas de GitHub Insights en Development Evidence, Execution Evidence y Team Collaboration Insights. | 4 hrs | Espinoza / Fernández | Done |
| - | Corrección Sprint 1 | CORR-08 | Completar Big Picture Event Storming (Capítulo II) | Elaborar y añadir el Big Picture Event Storming al Capítulo II (sección actualmente vacía). | 4 hrs | Gamero | Done |
| - | Corrección Sprint 1 | CORR-09 | Completar sección Software Deployment Configuration (Capítulo V) | Redactar la descripción del entorno de despliegue, pipelines CI/CD y hosting utilizados. | 4 hrs | Gallardo | Done |
| - | Corrección Sprint 1 | CORR-10 | Completar Project Report Collaboration Insights (Capítulo 0) | Añadir la descripción de la colaboración del equipo en el desarrollo del informe con evidencia de GitHub. | 4 hrs | Espinoza | Done |
| - | Corrección Sprint 1 | CORR-11 | Agregar Student Outcome de Cataño Zárate (Capítulo 0) | Añadir las entradas de "Comunica oralmente" y "Comunica por escrito" para Jesús Miguel Cataño Zárate, actualmente ausentes de la tabla. | 4 hrs | Cataño | Done |
| - | Corrección Sprint 1 | CORR-12 | Estandarizar análisis de entrevistas 4 y 5 | Añadir el campo "Resumen" completo a las entrevistas de Joan Steffano Quispe (Entrevistado 4) y Fabián Suárez (Entrevistado 5), siguiendo el mismo formato de las entrevistas 1–3. | 4 hrs | Fernández | Done |
| - | Corrección Sprint 1 | CORR-13 | Subir fotos faltantes de integrantes del equipo | Agregar al repositorio las imágenes `foto-valentino.jpeg`, `foto-lui.png` y `foto-jesus-c.png`, referenciadas en el Capítulo I pero ausentes en la carpeta assets. | 4 hrs | Gallardo / Cataño | Done |
| - | Corrección Sprint 1 | CORR-14 | Corregir inconsistencia de tech stack (ASP.NET vs Spring Boot) | En el Sprint 1 Backlog, la tarea T05 menciona "ASP.NET Core" como backend, pero el tech stack oficial declara Spring Boot. Corregir la descripción de T05 en el informe. | 4 hrs | Gallardo | Done |
| - | Corrección Sprint 1 | CORR-15 | Corregir nombre de marca en análisis competitivo | La tabla de análisis competitivo usa "SpotTrack" (nombre antiguo) en lugar de "SpotTrack". Actualizar todas las instancias en el Capítulo II. | 4 hrs | Espinoza | Done |
| - | Setup Web App | SETUP-01 | Crear proyecto Vue con estructura por Bounded Contexts | Inicializar el proyecto Vue (`npm create vue@latest spottrack-app`), configurar la estructura de carpetas por bounded context: `auth/`, `heatmap/`, `admin/`, `maintenance/`, `equipment/`, `routines/`, `shared/`, `analytics/`. | 4 hrs | Gallardo | Done |
| - | Setup Web App | SETUP-02 | Configurar JSON Server como Fake API | Instalar y configurar `json-server` con un `db.json` que contenga datos seed para: `users`, `equipments`, `IoT`, `alerts`, `tickets`, `reservations`, `routines/alternatives`, `analytics`. Exponer en `localhost:3000`. | 4 hrs | Gamero | Done |
| - | Setup Web App | SETUP-03 | Documentar Sprint 2 Planning, Backlog y evidencias en el informe | Redactar las secciones de Sprint Planning 2, Aspect Leaders y Sprint Backlog en el Capítulo V. Al finalizar el sprint, completar Development Evidence, Execution Evidence y Team Collaboration Insights. | 4 hrs | Espinoza | Done |
| US26 | Gestión de activos físicos y altas | T01 | Implement equipment registration form | Build the UI form to register new equipment linked to an IoT sensor | 6 | Carla | Done |
| US26 | Gestión de activos físicos y altas | T02 | Implement equipment decommission flow | Add decommission action and confirmation dialog | 4 | Carla | Done |
| US21 | Monitoreo de estado de hardware Edge IoT | T03 | Build IoT node health dashboard view | Display connected/disconnected status per sensor node | 5 | Carla | Done |
| US21 | Monitoreo de estado de hardware Edge IoT | T04 | Implement reconnection status sync | Handle state sync when a node reconnects | 4 | Carla | Done |
| TS12 | Registrar evento de telemetría IoT API | T05 | Implement POST /api/v1/telemetry endpoint | Receive and process IoT sensor state events | 5 | Carla | Done |
| TS12 | Registrar evento de telemetría IoT API | T06 | Validate telemetry payload and auth | Return 400 on malformed or unauthorized payloads | 4 | Carla | Done |
| TS13 | Listar historial de uso general API | T07 | Implement GET /api/v1/telemetry endpoint | Return usage history array filtered by date range | 4 | Carla | Done |
| US08 | Gestión de preferencias y perfil | T08 | Build profile edit view | Allow user to update personal data and language preference | 4 | Jesús | Done |
| US08 | Gestión de preferencias y perfil | T09 | Implement language toggle i18n | Wire language selector to i18n service | 4 | Jesús | Done |
| US12 | Notificaciones push de disponibilidad | T10 | Build availability bell subscription UI | Allow client to subscribe to machine availability alert | 4 | Jesús | Done |
| US12 | Notificaciones push de disponibilidad | T11 | Display push notification on machine release | Show notification when subscribed machine becomes free | 4 | Jesús | Done |
| US13 | Sistema de recompensas Crowdsourcing | T12 | Build manual status report UI | Allow client to report machine status manually | 5 | Jesús | Done |
| US13 | Sistema de recompensas Crowdsourcing | T13 | Display reward points in profile | Show accumulated points after validated report | 4 | Jesús | Done |
| US24 | Notificación de restablecimiento a usuarios | T14 | Show restoration notification to clients | Notify clients when a repaired machine is back online | 4 | Lui | Done |
| US09 | Visualización del mapa de calor en vivo | T15 | Build interactive heatmap component | Render machine availability map with green/red indicators | 8 | Carla | Done |
| US09 | Visualización del mapa de calor en vivo | T16 | Implement real-time status update via polling | Auto-update machine icons without page reload | 6 | Carla | Done |
| US10 | Filtrado del inventario por tipo de máquina | T17 | Implement filter tags component | Add Fuerza/Cardio filter tags to heatmap | 4 | Carla | Done |
| US10 | Filtrado del inventario por tipo de máquina | T18 | Implement clear filters action | Restore full inventory on filter clear | 4 | Carla | Done |
| US11 | Cambio de sucursal para revisión de aforo | T19 | Implement branch selector component | Allow user to switch branches and reload heatmap | 4 | Carla | Done |
| US11 | Cambio de sucursal para revisión de aforo | T20 | Block premium branch for basic plan users | Show upgrade suggestion when branch access is denied | 4 | Carla | Done |
| US14 | Motor de sugerencia de rutinas alternativas | T21 | Build alternative routine suggestion view | Show alternative exercises when selected machine is occupied | 6 | Álvaro | Done |
| US14 | Motor de sugerencia de rutinas alternativas | T22 | Handle no-alternatives scenario | Suggest bodyweight exercises when gym is at full capacity | 4 | Álvaro | Done |
| US15 | Filtrado de alternativas por grupo muscular | T23 | Filter suggestions by target muscle group | Discard exercises from other muscle groups in suggestions | 4 | Álvaro | Done |
| US15 | Filtrado de alternativas por grupo muscular | T24 | Exclude machines with open tickets from suggestions | Filter out equipment in maintenance from suggestions | 4 | Álvaro | Done |
| US16 | Sistema de reserva exprés en horas pico | T25 | Build express reservation button and timer UI | Show yellow status and countdown on reservation | 5 | Álvaro | Done |
| US16 | Sistema de reserva exprés en horas pico | T26 | Implement reservation expiry release flow | Return machine to free state when timer runs out | 4 | Álvaro | Done |
| US25 | Calendario inteligente de bloqueos | T27 | Build smart schedule view with peak-hour warnings | Show warning when client selects high-demand slot | 5 | Álvaro | Done |
| US25 | Calendario inteligente de bloqueos | T28 | Implement valley-hour suggestion on conflict | Suggest off-peak alternative when peak slot is selected | 4 | Álvaro | Done |
| TS18 | Crear reserva exprés API | T29 | Implement POST /api/v1/reservations endpoint | Execute logical machine block during high demand | 5 | Lui | Done |
| TS19 | Cancelar reserva exprés API | T30 | Implement PUT /api/v1/reservations/{id}/cancel endpoint | Release machine block on timer expiry or user abort | 4 | Lui | Done |
| TS20 | Obtener sugerencias de rutinas API | T31 | Implement GET /api/v1/routines/alternatives endpoint | Run replacement algorithm by muscle group and availability | 5 | Lui | Done |
| TS20 | Obtener sugerencias de rutinas API | T32 | Handle bodyweight fallback in suggestions | Return bodyweight alternatives when no machines are free | 4 | Lui | Done |
| TS14 | Obtener picos de afluencia por día API | T33 | Implement GET /api/v1/analytics/peak-hours endpoint | Identify hourly blocks exceeding 90% capacity | 5 | Lui | Done |
| TS15 | Exportar reporte gerencial API | T34 | Implement GET /api/v1/analytics/export/pdf endpoint | Generate binary PDF stream of monthly usage report | 5 | Lui | Done |
| TS16 | Registrar estado manual de máquina API | T35 | Implement POST /api/v1/machines/{id}/manual-reports endpoint | Save crowdsourcing report to validation queue | 4 | Lui | Done |
| TS17 | Sumar puntos de recompensa API | T36 | Implement PUT /api/v1/users/{id}/points endpoint | Increment points when manual report matches IoT reading | 4 | Lui | Done |
| TS21 | Crear ticket de mantenimiento API | T37 | Implement POST /api/v1/tickets endpoint | Register incident and set machine to In Maintenance | 4 | Lui | Done |
| TS22 | Listar tickets activos/históricos API | T38 | Implement GET /api/v1/tickets endpoint | Return filtered ticket backlog by branch or status | 4 | Lui | Done |
| TS23 | Resolver ticket técnico API | T39 | Implement PUT /api/v1/tickets/{id}/resolve endpoint | Close ticket and return machine to free status | 4 | Lui | Done |
| TS24 | Generar alerta predictiva API | T40 | Implement POST /api/v1/alerts endpoint | Auto-generate alert when usage exceeds safe threshold | 5 | Lui | Done |
| TS25 | Programar bloqueo de mantenimiento API | T41 | Implement POST /api/v1/maintenance-blocks endpoint | Validate maintenance schedule against peak-hour conflicts | 5 | Lui | Done |
| TS26 | Calcular impacto financiero API | T42 | Implement GET /api/v1/analytics/financial-impact endpoint | Convert downtime hours to monetary loss estimate | 5 | Lui | Done |
| TS27 | Simular ROI API | T43 | Implement POST /api/v1/analytics/roi-projection endpoint | Run ROI simulation based on stress telemetry | 5 | Lui | Done |
| TS05 | Crear nueva máquina API | T44 | Implement POST /api/v1/machines endpoint | Register new equipment linked to IoT sensor | 4 | Lui | Done |
| TS06 | Listar máquinas por sede API | T45 | Implement GET /api/v1/machines endpoint | Return full inventory filtered by branchId | 4 | Lui | Done |
| TS07 | Mostrar máquina por Id API | T46 | Implement GET /api/v1/machines/{id} endpoint | Return detailed physical and logical machine data | 4 | Lui | Done |
| TS08 | Actualizar/Reubicar máquina API | T47 | Implement PUT /api/v1/machines/{id} endpoint | Allow branch reassignment or attribute update | 4 | Lui | Done |
| TS09 | Dar de baja máquina API | T48 | Implement DELETE /api/v1/machines/{id} endpoint | Apply soft-delete and unlink IoT sensor | 4 | Lui | Done |
| TS10 | Registrar repuesto en inventario API | T49 | Implement POST /api/v1/inventory endpoint | Add new spare part to maintenance stock | 4 | Lui | Done |
| TS11 | Actualizar stock de repuesto API | T50 | Implement PUT /api/v1/inventory/{id}/stock endpoint | Discount materials when a ticket is resolved | 4 | Lui | Done |
| US17 | Acumulación automática de horas de uso | T51 | Build equipment usage hours chart | Display cumulative usage minutes per machine | 5 | Valentino | Done |
| US17 | Acumulación automática de horas de uso | T52 | Implement date range filter on usage chart | Recalculate totals based on selected period | 4 | Valentino | Done |
| US18 | Identificación de equipos subutilizados | T53 | Build underutilized equipment table | Highlight machines below usage threshold | 4 | Valentino | Done |
| US18 | Identificación de equipos subutilizados | T54 | Implement CSV export for underutilized list | Download underutilized equipment data as CSV | 4 | Valentino | Done |
| US19 | Visualización de picos de estrés del local | T55 | Build peak stress hours chart | Mark red hourly blocks exceeding 90% capacity | 5 | Valentino | Done |
| US19 | Visualización de picos de estrés del local | T56 | Implement intersemanal comparison overlay | Superimpose two trend lines for weekly comparison | 4 | Valentino | Done |
| US20 | Exportación de analíticas de uso | T57 | Build PDF export button on dashboard | Trigger formatted PDF download from analytics view | 4 | Valentino | Done |
| US20 | Exportación de analíticas de uso | T58 | Handle export delay with email fallback notice | Show deferred notice when server is under load | 4 | Valentino | Done |
| US22 | Alerta predictiva de mantenimiento | T59 | Build maintenance alert banner component | Display predictive alert when threshold is exceeded | 5 | Lui | Done |
| US22 | Alerta predictiva de mantenimiento | T60 | Implement manual threshold configuration UI | Allow manager to set safe hours limit per machine | 4 | Lui | Done |
| US23 | Despacho automatizado de tickets técnicos | T61 | Build assign-to-support action on alert | Convert alert to ticket and notify technician | 4 | Lui | Done |
| US23 | Despacho automatizado de tickets técnicos | T62 | Update machine status to In Maintenance on ticket creation | Reflect maintenance state on public heatmap | 4 | Lui | Done |
| US27 | Estadísticas de reubicación multisede | T63 | Build cross-branch utilization stats view | Show demand comparison between branches | 6 | Valentino | Done |
| US27 | Estadísticas de reubicación multisede | T64 | Display relocation recommendation card | Show transfer suggestion when demand imbalance is detected | 4 | Valentino | Done |
| US28 | Gestión automatizada de stock de repuestos | T65 | Build spare parts inventory table | Show current stock per part with restock alert indicator | 4 | Lui | Done |
| US28 | Gestión automatizada de stock de repuestos | T66 | Implement restock alert notification display | Show alert when part reaches minimum stock level | 4 | Lui | Done |
| US29 | Calculadora de impacto financiero | T67 | Build financial impact module view | Display estimated monetary loss per machine downtime | 5 | Valentino | Done |
| US29 | Calculadora de impacto financiero | T68 | Show monthly inefficiency cost chart | Render total hidden cost from equipment inactivity | 4 | Valentino | Done |
| US30 | Analítica predictiva de compras e inversión | T69 | Build ROI projection simulation view | Allow manager to input acquisition cost and see ROI estimate | 5 | Valentino | Done |
| US30 | Analítica predictiva de compras e inversión | T70 | Display purchase recommendation on saturation | Show buy suggestion when machine consistently exceeds max capacity | 4 | Valentino | Done |

Trello board: https://trello.com/invite/b/69fc21c2d05be44be499c75d/ATTI944e7a75fa88bba093494745abbec4eb6F6DB156/spottrack-tb1

![](../assets/trello-evidence.png)

Si bien es cierto se solicitó el desarrollo de un Trello board, nuestro equipo principalmente decidió utilizar la plataforma de Jira para la asignación de tareas.
![](../assets/jira-evidence.png)

#### 5.2.2.4. Development Evidence for Sprint Review

Frontend Web Applications Commits:

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | d3a30e2 | Merge pull request #40 from SpotTrack-1ASI0729-2610-11881/fix/mantainance | fix: fix base infrastructure not being used | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/mantainance | 94bb1f9 | fix: fix base infrastructure not being used | - | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 424a52d | Merge pull request #39 from SpotTrack-1ASI0729-2610-11881/feature/client-booking | added booking section | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-booking | 3a88e65 | added booking section | - | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | d16b42b | Merge pull request #38 from SpotTrack-1ASI0729-2610-11881/feature/analytics | chore: analytics context structured | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/analytics | 0f0df28 | chore: analytics context structured | - | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 9e5e94a | Merge pull request #37 from SpotTrack-1ASI0729-2610-11881/feature/client-map | add map view | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-map | 4f093fa | add map view | - | 2026-05-10 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | e02b3e6 | Merge pull request #36 from SpotTrack-1ASI0729-2610-11881/feature/analytics | feat(analytics): add analytics section | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/analytics | d224048 | feat(analytics): add analytics section | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 139bca7 | Merge pull request #35 from SpotTrack-1ASI0729-2610-11881/feature/client-map | separe bottombar from layout | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-map | 9ac8232 | separe bottombar from layout | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 660ba4f | Merge pull request #34 from SpotTrack-1ASI0729-2610-11881/feature/mantainance | feat(mantainance): add mantainace section | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/mantainance | c9a42db | feat(mantainance): add mantainace section | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 50ad787 | Merge pull request #33 from SpotTrack-1ASI0729-2610-11881/fast-hotfix | fixerrors | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fast-hotfix | dd10791 | fixerrors | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 8bbb3e4 | Merge pull request #32 from SpotTrack-1ASI0729-2610-11881/feature/client-app | Feature/client app | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-app | 448b08e | Merge branch 'develop' into feature/client-app | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-app | 9f45f61 | add new properties client&admin | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-app | f3e9dc1 | Views adjusted also added proper preview components | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/client-app | 87e85ff | added-switch-button-between-client&admin | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 4522b29 | Merge pull request #31 from SpotTrack-1ASI0729-2610-11881/feature/login | fix: build fix | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/login | 0053e96 | fix: build fix | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 7b32797 | Merge pull request #30 from SpotTrack-1ASI0729-2610-11881/feature/login | feat: add login screen | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/login | 68cc54e | feat: add login screen | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 183bc13 | Merge pull request #29 from SpotTrack-1ASI0729-2610-11881/feature/iot-monitoring | fix: translation in iot monitoring section didnt work | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/iot-monitoring | 10c6cd0 | fix: translation in iot monitoring section didnt work | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | ae98bd6 | Merge pull request #28 from SpotTrack-1ASI0729-2610-11881/feature/iot-monitoring-2 | feat: IoT monitoring latest version | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/iot-monitoring-2 | 96a0b95 | feat: IoT monitoring latest version | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 76b164c | Merge pull request #27 from SpotTrack-1ASI0729-2610-11881/feature/configuration | Add configuration section | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/configuration | 414aa67 | Add configuration section | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | main | 2c1aa9b | Revert "Merge pull request #18 from SpotTrack-1ASI0729-2610-11881/US-24" | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 1c35ac9 | Merge pull request #25 from SpotTrack-1ASI0729-2610-11881/fix/endpoint-equipment | fix: equipents endopoint hardcoded | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/endpoint-equipment | f2e5559 | fix: equipents endopoint hardcoded | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 2695fe5 | Merge pull request #24 from SpotTrack-1ASI0729-2610-11881/fix/endpoints | fix: register new equipment route renamed | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/endpoints | 9e5b897 | fix: register new equipment route renamed | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | cb357fc | Merge pull request #23 from SpotTrack-1ASI0729-2610-11881/fix/endpoints | fix: equipents route fixed | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/endpoints | 6172264 | fix: equipents route fixed | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | cc80283 | Merge pull request #22 from SpotTrack-1ASI0729-2610-11881/fix/endpoints | fix: rename equipent routes | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/endpoints | ed95636 | fix: rename equipent routes | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 050fb54 | ci: add Azure Static Web Apps workflow file | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 83e0b66 | Merge pull request #21 from SpotTrack-1ASI0729-2610-11881/chore/production | chore: add production api | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | chore/production | 4f820da | chore: add production api | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 760fe04 | Merge pull request #20 from SpotTrack-1ASI0729-2610-11881/chore/production | chore: add dist folder | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | chore/production | b852edf | chore: add dist folder | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 65c1a21 | Merge pull request #19 from SpotTrack-1ASI0729-2610-11881/chore/dist | chore: configure rewrite rule for SPA | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | chore/dist | 75b24fd | chore: configure rewrite rule for SPA | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | dbd63df | Merge pull request #18 from SpotTrack-1ASI0729-2610-11881/US-24 | Add initial configurations components | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | US-24 | 82b1833 | Add initial configurations components | - | 2026-05-08 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 1ed2967 | Merge pull request #17 from SpotTrack-1ASI0729-2610-11881/feature/iot-monitoring | feat: add monitoring section initial version | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/iot-monitoring | a23eba3 | feat: add monitoring section initial version | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | b8a8cf5 | Merge pull request #16 from SpotTrack-1ASI0729-2610-11881/fix/equipment | Fix/equipment | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/equipment | 1dd31ba | fix: fix equipment.entity structure | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | fix/equipment | 91555b7 | feat: add IoT entity | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 985f74c | Merge pull request #15 from SpotTrack-1ASI0729-2610-11881/feature/sidebar | feat: add configuration to sidebar | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/sidebar | 456b712 | feat: add configuration to sidebar | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 84d2e87 | Merge pull request #14 from SpotTrack-1ASI0729-2610-11881/feature/sidebar | feat: add dashboard to the sidebar | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/sidebar | bc619c3 | feat: add dashboard to the sidebar | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | c9f20a0 | Merge pull request #13 from SpotTrack-1ASI0729-2610-11881/feature/sidebar | feat(sidebar): add sidebar | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/sidebar | a3d59a5 | feat(sidebar): add sidebar | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | cd26e26 | Merge pull request #12 from SpotTrack-1ASI0729-2610-11881/feature/equipment | feat(equipment): add register equipment and equipment section | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | 95f0342 | feat(equipment): add register equipment and equipment section | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | d43d059 | Merge pull request #11 from SpotTrack-1ASI0729-2610-11881/feature/equipment | Feature/equipment | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | ac98a93 | feat: working json server methods for equipment feature | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | 6f70b17 | feat: add equipment store | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | e1c2a86 | Merge pull request #10 from SpotTrack-1ASI0729-2610-11881/feature/equipment | feat: add partially working us-26 with json server set up | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | eabed49 | feat: add partially working us-26 with json server set up | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 9fefd90 | Merge pull request #9 from SpotTrack-1ASI0729-2610-11881/feature/equipment | Feature/equipment | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | 8ace1b1 | feat: add presentation layer for equipment related user stories | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | c9fe227 | feat: finished equipment APIs, assemblers and reponses | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/equipment | f5e6b9e | feat: add equipment infrastructure | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | cd8c1a0 | Merge pull request #8 from SpotTrack-1ASI0729-2610-11881/chore/json-local-server | feat: structure equipment infrastructure | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | chore/json-local-server | bcd9596 | feat: structure equipment infrastructure | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | cbda4b1 | Merge pull request #7 from SpotTrack-1ASI0729-2610-11881/chore/json-local-server | chore: setup db.json | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | chore/json-local-server | 6164e8c | chore: setup db.json | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 4caee1e | Merge pull request #6 from SpotTrack-1ASI0729-2610-11881/feature/generic-infrastructure | chore: add routing | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | d2fdd81 | chore: add routing | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | 13dc0d4 | chore: add routing | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | df621bc | Merge pull request #5 from SpotTrack-1ASI0729-2610-11881/feature/generic-infrastructure | Feature/generic infrastructure | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | ec0489d | feat: add equipment bounded context presentation and i18n | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | b1d97c7 | docs: add class diagrams frontend | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 67fc548 | Merge pull request #4 from SpotTrack-1ASI0729-2610-11881/feature/generic-infrastructure | feat: add base apis, responses, entities and assembler | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | 03697f5 | feat: add base apis, responses, entities and assembler | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | f385091 | Merge pull request #3 from SpotTrack-1ASI0729-2610-11881/feature/generic-infrastructure | feat: setup shared bounded context | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/generic-infrastructure | c6345ac | feat: setup shared bounded context | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 7c2c65d | Merge pull request #2 from SpotTrack-1ASI0729-2610-11881/feature/US-26 | chore: add equipment bounded context | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/US-26 | 8102bfa | chore: add equipment bounded context | - | 2026-05-04 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | develop | 29dcac5 | Merge pull request #1 from SpotTrack-1ASI0729-2610-11881/feature/class-diagrams | docs: add class diagrams | 2026-04-24 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/class-diagrams | 1308f7a | docs: add class diagrams | - | 2026-04-24 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | feature/init-testing | 66d1157 | feat: add initial vue testing program | - | 2026-04-15 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | main | 5fd40ea | chore: initial commit | - | 2026-04-14 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | main | 39f083c | chore:second commit | - | 2026-04-06 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | main | ec1c353 | chore:initial commit | - | 2026-04-06 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Frontend-Web-Applications | main | fd32baf | Initial commit | - | 2026-04-06 |

Landing Page Commits

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | f6eba3a | Merge pull request #17 from SpotTrack-1ASI0729-2610-11881/feature/contact-email | feat:add-email-sender | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-email | df0057d | feat:add-email-sender | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | ba302d6 | Merge pull request #16 from SpotTrack-1ASI0729-2610-11881/fix/contact-section-i18n | fixed:i18n contanct and footer | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | fix/contact-section-i18n | cdb34bc | fixed:i18n contanct and footer | - | 2026-05-09 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 62a2b97 | Merge pull request #15 from SpotTrack-1ASI0729-2610-11881/fix/contact-section | fixed: add-vuetify-components | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 9380f51 | Merge pull request #13 from SpotTrack-1ASI0729-2610-11881/landing/hotfix-features | landing-fix | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | landing/hotfix-features | 7564abb | landing-fix | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-section | a95b603 | Merge branch 'develop' into feature/contact-section | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-section | 248395f | fixed: add-vuetify-components | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 009da6e | Merge pull request #11 from SpotTrack-1ASI0729-2610-11881/feature/footer-section | feat:add-footer-section | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/footer-section | 914917c | Merge branch 'develop' into feature/footer-section | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/footer-section | 04fb8c8 | feat:add-footer-section | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | db87823 | Merge pull request #10 from SpotTrack-1ASI0729-2610-11881/landing/features-section | Landing/features section | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | landing/features-section | ae25905 | landing-feature-implementation-v2 | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | landing/features-section | de4178a | landing-feature-implementation | - | 2026-05-07 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | d98b24a | Merge pull request #9 from SpotTrack-1ASI0729-2610-11881/feature/contact-section | Feature/contact section | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-section | 212b557 | feat:source correction | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-section | f083ae0 | Merge branch 'feature/contact-section' into feature/contact-section | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/contact-section | c5e629f | feat:add-contact | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 11cb386 | Merge pull request #8 from SpotTrack-1ASI0729-2610-11881/chore/github-pages | fix: github pages only showed readme.md | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | chore/github-pages | 742612a | fix: github pages only showed readme.md | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 8c34fe6 | Merge pull request #7 from SpotTrack-1ASI0729-2610-11881/chore/github-pages | Chore/GitHub pages | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | chore/github-pages | 1fb2b77 | fix: switch deployment branch | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | chore/github-pages | 1831ca2 | chore: add github pages | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | b414365 | Merge pull request #6 from SpotTrack-1ASI0729-2610-11881/fix/stripe | fix: add environments and services | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | fix/stripe | 7c2a041 | fix: add environments and services | - | 2026-05-05 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | cf91d30 | Merge pull request #5 from SpotTrack-1ASI0729-2610-11881/feature/hero-header | fix: fix login button height | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/hero-header | f3804cb | fix: fix login button height | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/hero-header | d3b9348 | fix: fix login button height | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 6357640 | Merge pull request #4 from SpotTrack-1ASI0729-2610-11881/feature/hero-header | fix: hero section completed | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/hero-header | cb21759 | fix: hero section completed | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | ae2957c | Merge pull request #3 from SpotTrack-1ASI0729-2610-11881/feature/niubiz | feat(stripe): add stripe payments | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/niubiz | 1aa12f4 | feat(stripe): add stripe payments | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | db9a16c | Merge pull request #2 from SpotTrack-1ASI0729-2610-11881/feature/pricing | fix: fix pricing cards organization | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/pricing | b996a8a | fix: fix pricing cards organization | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 8b00971 | Merge pull request #1 from SpotTrack-1ASI0729-2610-11881/feature/pricing | Feature/pricing | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/pricing | d732028 | feat(pricing): add pricing section | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/pricing | 76e113d | feat(en-es): add diciontarios for en and es | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/pricing | 0138b31 | feat(i18n): add language switcher component | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | feature/pricing | 68b1da4 | chore: add translate service | - | 2026-05-03 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | e480ef9 | feat(hero-section): add background animations | - | 2026-04-19 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | ed84ec5 | feat: add header | - | 2026-04-19 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | develop | 6a2919f | chore: project-setup | - | 2026-04-18 |
| SpotTrack-1ASI0729-2610-11881/SpotTrack-Landing-Page | main | 3871093 | Initial commit | - | 2026-04-18 |

#### 5.2.2.5. Execution Evidence for Sprint Review

Se logró desplegar una primera versión de la aplicación web, se reailzaron correcciones en los diagramas C4, diagramas de clase, diagramas de base de datos, calidad de imágenes de figma. Finalmente, se desplegó el landing page completamente funcional con call-to-action.

Execution evidence video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202413214_upc_edu_pe/IQBQX52QrrC0Q5BvU9mkmvuKAdN-F57suH5kYTvjIZEDCQA?e=cdBXo1&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

Para este Sprint, se ha implementado y desplegado con éxito un Mock API utilizando JSON-Server, alojado en Azure App Service. Este servicio proporciona un backend funcional para el proyecto SpotTrack, permitiendo la persistencia de datos y la integración con el frontend. Se configuró un flujo de CI/CD mediante GitHub Actions, integrando el perfil de publicación de Azure como un secreto de organización. La API está configurada con un prefijo /api/v1 y soporta operaciones CRUD completas, facilitando el desarrollo paralelo de las funcionalidades de monitoreo de equipos y gestión de dispositivos IoT.

##### 5.2.2.7. Relación de Endpoints Documentados

| Endpoint | Acción | Verbo HTTP | Sintaxis de Llamada      | Ejemplo de Response | Explicación |
|---|---|---|--------------------------|---|---|
| `/gyms` | Listar / Crear | `GET`, `POST` | `/api/v1/gyms`           | `{ "id": 1, "name": "FitNode Central", "subscription_tier": "Premium", "created_at": "2026-05-01T10:00:00Z" }` | Gestión de la entidad principal del gimnasio. |
| `/branches` | Listar / Crear | `GET`, `POST` | `/api/v1/branches`               | `{ "id": 1, "gym_id": 1, "name": "Main Branch", "address": "123 Main Street", "city": "Lima" }` | Información de sedes físicas. |
| `/zones` | Listar / Crear | `GET`, `POST` | `/api/v1/zones`                 | `{ "id": 1, "branch_id": 1, "name": "Cardio Zone", "capacity_limit": 20 }` | Áreas específicas dentro de una sede (ej. Cardio). |
| `/users` | Listar / Crear | `GET`, `POST` | `/api/v1/users`                 | `{ "id": 1, "gym_id": 1, "name": "Admin User", "email": "admin@fitnode.com", "role": "ADMIN" }` | Gestión de acceso y perfiles de usuario. |
| `/equipments` | Listar / Crear | `GET`, `POST` | `/api/v1/equipments`             | `{ "id": 1, "zone_id": 1, "name": "Treadmill", "brand": "Life Fitness", "model": "T5 Track", "status": "OPERATIONAL" }` | Inventario de máquinas de entrenamiento. |
| `/iot_devices` | Listar / Crear | `GET`, `POST` | `/api/v1/iot_devices`           | `{ "id": 1, "equipment_id": 1, "mac_address": "AA:BB:CC:DD:01", "status": "ACTIVE" }` | Dispositivos de monitoreo vinculados a equipos. |
| `/sensor_data` | Listar / Crear | `GET`, `POST` | `/api/v1/sensor_data`           | `{ "id": 1, "device_id": 1, "timestamp": "2026-05-04T09:00:00Z", "occupancy_detected": true, "vibration_index": 0.75 }` | Captura de telemetría y detección de ocupación. |
| `/usage_sessions` | Listar / Crear | `GET`, `POST` | `/api/v1/usage_sessions`        | `{ "id": 1, "equipment_id": 1, "start_time": "2026-05-04T08:00:00Z", "end_time": "2026-05-04T08:30:00Z", "calories_burned_est": 250.5 }` | Historial de uso de máquinas por sesión. |
| `/equipment_usage_stats` | Listar / Crear | `GET`, `POST` | `/api/v1/equipment_usage_stats` | `{ "id": 1, "equipment_id": 1, "total_usage_hours": 120.5, "usage_count_daily": 8, "estimated_wear_level": 0.35 }` | Estadísticas acumuladas y nivel de desgaste. |
| `/maintenance_tickets` | Listar / Crear | `GET`, `POST` | `/api/v1/maintenance_tickets`   | `{ "id": 1, "equipment_id": 2, "status": "OPEN", "priority": "HIGH", "type": "CORRECTIVE" }` | Registro de fallos y tickets de reparación. |
| `/maintenance_logs` | Listar / Crear | `GET`, `POST` | `/api/v1/maintenance_logs`      | `{ "id": 1, "ticket_id": 1, "action_description": "Replaced internal belt", "cost": 150.0 }` | Bitácora de acciones realizadas en mantenimientos. |
| `/maintenance_schedules` | Listar / Crear | `GET`, `POST` | `/api/v1/maintenance_schedules` | `{ "id": 1, "equipment_id": 1, "scheduled_date": "2026-06-01", "task_type": "LUBRICATION" }` | Planificación de mantenimientos preventivos. |
| `/spare_parts` | Listar / Crear | `GET`, `POST` | `/api/v1/spare_parts`           | `{ "id": 1, "gym_id": 1, "part_name": "Treadmill Belt", "stock_quantity": 5, "unit_cost": 80.0 }` | Inventario de repuestos para equipos. |
| `/alerts` | Listar / Crear | `GET`, `POST` | `/alerts`                | `{ "id": 1, "equipment_id": 4, "severity": "CRITICAL", "message": "Equipment out of order", "is_resolved": false }` | Notificaciones de estado crítico de equipos. |
| `/notifications` | Listar / Crear | `GET`, `POST` | `/api/v1/notifications`         | `{ "id": 1, "user_id": 1, "title": "Critical Alert", "content": "Lat Pulldown Machine is out of order", "is_read": false }` | Mensajes enviados a usuarios finales. |


##### 5.2.2.8. Evidencias de Interacción con la Documentación

###### 5.2.2.8.1 Disponibilidad del Servicio
Validación del endpoint /api/v1/health que confirma el estado "ok" del servidor en Azure.
![captura-disponibilidad-servicio.png](../assets/captura-disponibilidad-servicio.png)

###### 5.2.2.8.2. Interacción con Recurso Equipments
Visualización de los datos de equipos obtenidos directamente desde el App Service de Azure.
![captura-equipments-db.png](../assets/captura-equipments-db.png)

##### 5.2.2.9. Repositorio y Trazabilidad de Documentación

Para asegurar la transparencia y el seguimiento de los cambios, se detallan los enlaces a los repositorios de la organización.

URL Repositorio Mock API: https://github.com/SpotTrack-1ASI0729-2610-11881/SpotTrack-Mock-Api

URL Repositorio Frontend: https://witty-tree-0f4a0570f.7.azurestaticapps.net/

URL Repositorio Landing Page: https://spottrack.github.io/spottrack-website/


#### 5.2.2.10. Software Deployment Evidence for Sprint Review

Como parte de la tarea **CORR-05**, la Landing Page de SpotTrack fue desplegada exitosamente en **GitHub Pages** durante este Sprint 2. El proceso se automatizó mediante el workflow de GitHub Actions definido en `.github/workflows/deploy.yml`, el cual se activa con cada `push` a la rama `main` del repositorio `SpotTrack-Landing-Page`, asegurando despliegues continuos sin fricción.

| Producto | Entorno | URL de Producción |
| :--- | :--- | :--- |
| SpotTrack Landing Page | GitHub Pages (producción) | https://spottrack.github.io/spottrack-website/ |

La siguiente figura muestra la Landing Page de SpotTrack correctamente desplegada y funcional en el entorno de producción de GitHub Pages:

![Vista de la Landing Page de SpotTrack desplegada y funcional en GitHub Pages](../assets/landing-page-deployment-evidence/lading-page-screenshot.png)


Por parte de la aplicación web (Vue SPA), se utilizó un static web app de Azure para realizar el despliegue. Para ello, simplemente se configura la organización, repositorio y rama deseada en donde se va desplegar la aplicación, esto se vincula a un Github Actions. La activación de este último sucede en cada push a develop.

![](../assets/azure-evidence.png)
![](../assets/github-actions-webapp.png)

Webapp URL: https://purple-tree-092d40a10.7.azurestaticapps.net/

#### 5.2.2.11. Team Collaboration Insights during Sprint

A continuación todas las estadisticas que nos proporciona Github, en su apartado de Insights, sobre la colaboración del equipo en los repositorios de webbapp y website:

<img src="../assets/evidence-insights-webapp.png" alt="bounded" width="500"/>

<img src="../assets/evidence-insights-website.png" alt="bounded" width="500"/>

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.
## 5.4. Video About-the-Product.