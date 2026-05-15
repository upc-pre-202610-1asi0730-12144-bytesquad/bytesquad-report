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

A continuación todas las estadisticas que nos proporciona Github, en su apartado de Insights, sobre la colaboración del equipo durante el Sprint 1:

<img src="../assets/evidence-insights.png" alt="bounded" width="500"/>

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.
## 5.4. Video About-the-Product.