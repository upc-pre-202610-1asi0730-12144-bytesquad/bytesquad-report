# Capítulo IV: Product Design
## 4.1. Style Guidelines.
Para garantizar la consistencia visual, la accesibilidad y una experiencia de usuario (UX) coherente en todas las plataformas de SpotTrack (Landing Page, Dashboard B2B y Web App B2C), se ha definido la siguiente guía de estilos. Esta guía no solo estandariza los componentes de la interfaz, sino que también alinea la identidad visual con los objetivos del negocio.
### 4.1.1. General Style Guidelines.
La legibilidad es fundamental para una plataforma que muestra datos analíticos complejos y mapas de calor en tiempo real. Se ha establecido una jerarquía tipográfica limpia y moderna:

Tipografía Primaria: Utilizada para títulos (H1, H2, H3) y elementos de gran énfasis visual. Posee un carácter geométrico y dinámico que transmite modernidad tecnológica y agilidad deportiva. (Pesos utilizados: SemiBold, Bold).

Tipografía Secundaria: Utilizada para párrafos, etiquetas de la interfaz, tablas de datos y botones. Se caracteriza por su alta legibilidad en tamaños pequeños y pantallas móviles, garantizando que el usuario pueda escanear la información rápidamente. (Pesos utilizados: Regular, Medium, SemiBold).

![Typography](../assets/styleguidelines/Typography.png)

Paleta de Colores
La selección cromática de SpotTrack está construida sobre un contraste de alto impacto que refleja innovación tecnológica y energía deportiva, utilizando los siguientes colores base:

Primary Dark / Neutral (#000000 - Negro Absoluto): Usado para fondos estructurados, modo oscuro del dashboard, textos principales y contenedores de gráficos.

Transmite autoridad, elegancia, fuerza y alta tecnología. En interfaces analíticas y de monitoreo constante (como el dashboard gerencial), el negro reduce drásticamente la fatiga visual y permite que los datos y los mapas de calor resalten de manera inmediata.

Primary Accent / Brand (#00ccb2 - Verde Azulado / Teal): Usado para los Call to Action (CTAs) principales, enlaces, indicadores de progreso y elementos interactivos primarios.

Es un color que fusiona la tranquilidad y fiabilidad tecnológica del azul con el crecimiento, salud y balance del verde. Transmite claridad, eficiencia e innovación. En el contexto del gimnasio, da una sensación de frescura y fluidez (ideal para indicar máquinas disponibles o acciones confirmadas).

Secondary Accent / Highlight (#f5bc36 - Amarillo Anaranjado / Dorado): Usado para destacar alertas preventivas, notificaciones importantes, botones secundarios de alta prioridad y estados de "Reserva" en el mapa de calor.

Representa vitalidad, energía, movimiento y el dinamismo puro del sector fitness. Capta la atención del ojo humano de inmediato, por lo que es perfecto para advertencias de mantenimiento predictivo o cuellos de botella en el aforo, comunicando precaución sin llegar a la agresividad de un rojo puro.

![Colors](../assets/styleguidelines/Colors.png)

Logo
El logotipo de SpotTrack Analytics se compone de un isotipo acompañado de un logotipo tipográfico.

Isotipo: Representa un "nodo" estilizado que simula el flujo de datos e interconexión (Edge IoT), utilizando contrastes entre el #00ccb2 y el #f5bc36 sobre fondos oscuros (#000000) para proyectar dinamismo.

Tipografía del Logo: De trazos gruesos, limpios y modernos, estableciendo una presencia sólida en el mercado B2B, denotando confianza y robustez tecnológica.

![Branding](../assets/styleguidelines/Branding.png)

### 4.1.2. Web Style Guidelines.

Para la construcción de las interfaces en código (Angular / CSS), se ha definido un sistema de diseño atómico estricto que rige la estructura y disposición de los elementos.

Grid System
El diseño se basa en un layout estructurado para mantener la alineación perfecta en resoluciones de escritorio y su correcta adaptabilidad a dispositivos móviles.

Columnas: Sistema de 12 columnas.

Ancho de Gutter: 24px.

Spacing System
Se utiliza una escala de espaciado predecible basada en múltiplos de 4 y 8 píxeles para mantener el ritmo vertical y horizontal

![Launguage and Spacing](../assets/styleguidelines/Launguage%20and%20Spacing.png)

## 4.2. Information Architecture.
### 4.2.1. Organization Systems.

Para estructurar el ecosistema de SpotTrack de forma práctica, utilizamos una categorización principal basada en la audiencia. Al final del día, toda la arquitectura de la información se rige por un modelo de **jerarquía visual (visual hierarchy)**, priorizando el contenido de mayor a menor importancia según lo que cada tipo de usuario necesita ver primero al entrar.

<div align= "center">
  <align>
    <img src="../assets/info/INFO-ADMIN.jpg" alt="wireflow" width="500"/>
  </div> <br>

**Plataforma Administrativa (Dashboard B2B)**
Su estructura jerárquica se divide de frente por módulos operativos (Inventario, Tickets, Estadísticas). Dentro de estos, los datos se categorizan por tópicos (para agrupar las máquinas según la sucursal) y de forma cronológica (para ordenar las alertas predictivas y el historial de horas de uso de más reciente a más antiguo).

<div align= "center">
  <align>
    <img src="../assets/info/INFO-CLIENT.jpg" alt="wireflow" width="500"/>
  </div> <br>

**Aplicación Móvil (Web App B2C)**
Diseñada para la inmediatez. La jerarquía visual coloca el mapa de calor en tiempo real como el componente absoluto y principal de la pantalla, subordinando opciones secundarias (como el perfil o recompensas) a menús de navegación. El catálogo de máquinas aplica una categorización directa por tópicos (ej. "Fuerza", "Cardio") para que el cliente filtre y encuentre lo que busca sin dar tantas vueltas.

<div align= "center">
  <align>
    <img src="../assets/info/INFO-LANDING-PAGE.jpg" alt="wireflow" width="500"/>
  </div> <br>

**Landing Page Comercial**
Sigue una jerarquía visual descendente (top-down) para guiar la lectura. El flujo arranca con lo más importante arriba (Hero Section con la propuesta de valor) y decanta hacia los detalles específicos más abajo (features, tabla de precios y formulario de contacto). El texto y las tarjetas están categorizados explícitamente según la audiencia, separando qué gana el dueño del gimnasio y qué gana el usuario final.
https://miro.com/app/board/uXjVHcq90QA=/?share_link_id=360970048482

### 4.2.2. Labeling Systems.

Para garantizar la simplicidad y reducir la carga cognitiva de los usuarios, se utilizará un vocabulario directo, estandarizado y libre de jerga técnica compleja. Las etiquetas representan acciones claras o agrupaciones lógicas de información.

Para el Dashboard Administrativo (B2B):

    "Resumen": En lugar de "Dashboard Principal" o "Métricas Generales". Agrupa los KPIs de alto nivel.

    "Activos": En lugar de "Inventario de Máquinas Físicas".

    "Monitoreo IoT": Agrupa el estado de la red y conexión de sensores.

    "Mantenimiento": En lugar de "Gestión de Tickets y Reparaciones". Agrupa las alertas y órdenes de trabajo.

    "Reportes": Agrupa la analítica histórica y mapas de calor estáticos.

    "Finanzas": En lugar de "Calculadora de Impacto Financiero y ROI".

Para la Aplicación Móvil (Cliente B2C):

    "Mapa en Vivo": Representa la vista de disponibilidad en tiempo real.

    "Rutinas": Agrupa las sugerencias de ejercicios alternativos.

    "Reservar": Acción directa para bloquear temporalmente un equipo.

### 4.2.3. SEO Tags and Meta Tags

Para asegurar un posicionamiento orgánico adecuado y una correcta indexación, se definen las siguientes etiquetas principales.

Landing Page (Sitio Público)

    Title: SpotTrack | Gestión Inteligente y Telemetría para Gimnasios

    Description: Optimiza la gestión de tu gimnasio con telemetría IoT. Reduce costos de mantenimiento, evita aglomeraciones y mejora la retención de tus clientes con mapas de calor en tiempo     real.

    Keywords: software para gimnasios, telemetría deportiva, mantenimiento predictivo gimnasios, sensores IoT fitness, gestión de activos deportivos, mapa de calor gimnasio, SpotTrack.

    Author: SpotTrack

Web Application (Portal de Acceso Administrativo)

    Title: SpotTrack Dashboard | Acceso Administrativo
    
    Description: Panel de control gerencial para la gestión de activos, monitoreo de hardware IoT y resolución de tickets de mantenimiento en tiempo real.
    
    Keywords: spottrack admin, login spottrack, gestión interna, dashboard gimnasios.
    
    Author: SpotTrack

### 4.2.4. Searching Systems.

Dada la alta densidad de datos (cientos de máquinas, múltiples sedes, histórico de tickets), el sistema de búsqueda es fundamental para la operatividad.

Opciones de Búsqueda y Filtros (Dashboard Administrativo):

Búsqueda Global (Barra de texto): Ubicada en el encabezado (Header). Permite búsquedas difusas ingresando el ID del equipo, nombre de la máquina o descripción de un ticket.

Filtros de Contexto (Faceted Search): * Por Sede: Dropdown global para cambiar la vista de datos entre diferentes sucursales.

Por Estado: Checkboxes rápidos para aislar máquinas (ej. Solo mostrar equipos 'En Mantenimiento' o 'Desconectados').

Por Categoría: Filtros por tipo de equipamiento (Cardio, Fuerza, Funcional).

### 4.2.5. Navigation Systems.

El sistema de navegación está diseñado para ser predecible y jerárquico, minimizando la cantidad de clics necesarios para alcanzar cualquier objetivo.

Landing Page (One-Page Scroll Navigation):

Navegación global superior fija (Sticky Top Navbar) que permite saltos rápidos (Anchor links) a las secciones clave: Inicio, Soluciones, Precios, Contacto. Incluye un Call to Action persistente ("Login") que redirige a la Web App.

Dashboard Administrativo (Desktop Web):

Navegación Estructural Permanente: Se utilizará un Sidebar (menú lateral izquierdo) persistente que contiene las etiquetas de los módulos principales (Activos, IoT, Mantenimiento, etc.). Esto permite al administrador saltar entre contextos sin perder su ubicación.

Navegación Local: Pestañas (Tabs) dentro de cada módulo para separar vistas internas (ej. dentro de "Mantenimiento", pestañas para Pendientes, En Progreso, Completados).

Aplicación Móvil (Clientes):

Bottom Navigation Bar: Barra inferior persistente con 3 o 4 íconos de acceso rápido a las funciones críticas para el usuario en movimiento (ej. Mapa, Rutinas, Perfil). Facilita el uso con una sola mano.

## 4.3. Landing Page UI Design.
### 4.3.1. Landing Page Wireframe.

- Home:

<div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landingw-nosotros.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe:**
 
El wireframe del Hero Section presenta la estructura de la primera pantalla visible de la Landing Page al cargar, sin scroll. En la versión desktop se aprecia el navbar superior con el logo "SpotTrack" en el extremo izquierdo, los ítems de navegación ("Nosotros", "Funciones", "Precios") centrados, y los controles de acceso ("Iniciar Sesión" como enlace de texto y "Demo Gratis" como botón con relleno diferenciado) en el extremo derecho. En la versión mobile el navbar se simplifica conservando únicamente el logo y los controles de acceso.
 
El cuerpo del Hero muestra el titular principal en la mayor escala tipográfica de toda la página, el subtítulo descriptivo en tipografía secundaria de menor peso, y los dos CTAs ("Comenzar Ahora →" y "Ver Demo") centrados y dispuestos en fila horizontal en desktop o en columna en mobile. En la parte inferior del viewport, una fila de cuatro métricas clave ("Reduce tiempos de espera", "Monitoreo 24/7", "Alertas automáticas", "Dashboard en tiempo real") completa el Hero antes del inicio del scroll.
 
**Principios y elementos de diseño aplicados:**
 
- **Jerarquía visual por escala tipográfica:** El titular ocupa el mayor tamaño de fuente de toda la landing, estableciendo el punto de entrada visual inmediato para el usuario. La escala desciende del título al subtítulo y de este a los CTAs, siguiendo la jerarquía H1/H2/Body del Design System.
- **Principio de énfasis en el CTA primario:** El botón "Comenzar Ahora →" adopta un relleno de gris más oscuro que "Ver Demo" (contorno sutil), estableciendo la prioridad de la acción principal sin depender del color.
- **Navbar sticky:** La barra de navegación se posiciona como elemento persistente en la parte superior, validando el sistema de Sticky Top Navbar con Anchor Links definido en el Navigation System de la Arquitectura de Información.
- **Diseño inclusivo:** Los CTAs presentan dimensiones de área de toque suficientes para interacción táctil en mobile. Las métricas clave de la parte inferior del Hero usan texto descriptivo breve, no solo íconos, garantizando la comprensión sin dependencia de elementos visuales únicos.
- **Grid system:** El layout de cuatro columnas para las métricas clave en desktop y la columna única en mobile validan el sistema de 12 columnas con gutter de 24px definido en las Web Style Guidelines, asegurando la correcta adaptabilidad responsive.


- Features:
  <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landingw-features.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del wireframe:**
 
El wireframe de la sección "Funciones" (identificada como "La Solución" en el contenido) presenta seis tarjetas de características del producto distribuidas en un layout de tres columnas por dos filas en desktop. Cada tarjeta incluye un ícono de línea en la parte superior, un título en tipografía secundaria SemiBold y un párrafo descriptivo en regular. Las seis características son: Sensores IoT Edge, Almacenamiento en la Nube, Monitoreo en Tiempo Real, Alertas de Mantenimiento, Dashboard Analítico y Seguridad JWT.
 
En mobile, las seis tarjetas se reorganizan en una sola columna, manteniendo el mismo orden de lectura de izquierda a derecha y de arriba a abajo.
 
**Principios y elementos de diseño aplicados:**
 
- **Jerarquía visual por posición:** El título de sección "La Solución" y el subtítulo "SpotTrack: Gestión inteligente todo en uno" se posicionan centrados y por encima de la cuadrícula de tarjetas, estableciendo el contexto antes de presentar el detalle, siguiendo el principio de jerarquía descendente top-down de la Landing Page.
- **Principio de consistencia de componentes:** Las seis tarjetas comparten la misma estructura (ícono → título → descripción), aplicando el Design System atómico para crear un ritmo visual predecible que facilita el escaneo rápido de la información.
- **Íconos de línea como indicadores semánticos:** Cada tarjeta utiliza un ícono de línea contextual (onda para IoT, nube para almacenamiento, gráfico para analítica, campana para alertas, escudo para seguridad) que complementa el título textual. La combinación ícono + texto aplica el principio de redundancia de canales de comunicación, no dependiendo del ícono como único indicador.
- **Arquitectura de información — Labeling System:** Los nombres de las seis características siguen el vocabulario definido en el Labeling System: directo, estandarizado y libre de jerga técnica compleja, permitiendo que tanto administradores técnicos como usuarios no especializados comprendan el valor de cada función.
- **Spacing system:** El espaciado entre tarjetas y entre el contenido interno de cada tarjeta respeta la escala de múltiplos de 8px definida en las Web Style Guidelines, manteniendo el ritmo visual de la sección.

- Pricing:
   <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landingw-pricing.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del wireframe:**
 
El wireframe de la sección "Planes y Precios" presenta tres tarjetas de suscripción dispuestas en un layout de tres columnas en desktop. La tarjeta central ("Mid – $109/mes") se distingue de las demás mediante una etiqueta "Más Popular" posicionada en la parte superior del borde y un contorno de mayor grosor, estableciendo la jerarquía visual del plan recomendado sin necesidad de color. Cada tarjeta muestra el nombre del plan, el precio mensual en el mayor tamaño tipográfico de la tarjeta, la lista de características incluidas con íconos de verificación circulares, y el botón de CTA diferenciado por plan (Demo Gratis / Comenzar Ahora → / Contactar).
 
En mobile, las tres tarjetas se apilan verticalmente con la tarjeta "Mid" posicionada en el centro del scroll, manteniendo su distinción visual mediante el borde y la etiqueta.
 
**Principios y elementos de diseño aplicados:**
 
- **Principio de énfasis y jerarquía:** La tarjeta "Mid" utiliza borde diferenciado y etiqueta superior para jerarquizar la opción recomendada sin depender del color, validando que la distinción es estructural y perceptible en escala de grises.
- **Consistencia con diferenciación controlada:** Las tres tarjetas comparten la misma estructura interna, pero se diferencian por el número de características listadas, el nivel de precio y el tipo de CTA, aplicando el principio de consistencia con variación significativa para comunicar las diferencias entre planes.
- **Diseño inclusivo — Íconos de verificación con texto:** Los checkmarks junto a cada característica acompañan al texto (no son el único indicador), garantizando que la lista sea comprensible para usuarios con daltonismo o dificultades de percepción visual.
- **Arquitectura de información:** La sección sigue la jerarquía descendente de la Landing Page: el usuario llega a esta sección después de haber comprendido el producto en el Hero y las Features, siguiendo el flujo lógico de decisión de compra establecido en el Organization System.
- **CTAs diferenciados por plan:** Los tres CTAs del wireframe tienen nombres distintos según el nivel de compromiso que implica cada plan (Demo Gratis → exploración sin compromiso; Comenzar Ahora → conversión directa; Contactar → ventas para empresa), aplicando el Labeling System orientado a la acción.

- Contact:
 <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landingw-contact.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe:**
 
El wireframe de la sección "Contacto" es la última sección de contenido de la Landing Page, accesible desde el navbar o al final del scroll. Presenta un formulario de contacto centralizado con tres campos: Nombre*, Email* y Mensaje* (textarea de mayor altura), y el botón "Enviar" de ancho completo como CTA único. Debajo del formulario, el footer muestra el copyright "© 2026 SpotTrack. Todos los derechos reservados." como cierre de la página.
 
En mobile el formulario ocupa el 90% del ancho del viewport, manteniendo los mismos campos y el mismo orden vertical.
 
**Principios y elementos de diseño aplicados:**
 
- **Minimalismo y reducción de fricción:** El formulario se compone únicamente de los tres campos estrictamente necesarios para iniciar el contacto comercial, reduciendo la barrera de entrada para el visitante y aumentando la probabilidad de conversión.
- **Etiquetas posicionadas dentro del campo (placeholder):** En el wireframe, las etiquetas orientativas ("Nombre*", "Email*", "Mensaje*") se muestran como placeholders dentro de los campos. El asterisco (*) indica obligatoriedad de forma estándar, siguiendo la convención de formularios web.
- **CTA de ancho completo:** El botón "Enviar" ocupa el ancho total del contenedor del formulario, maximizando el área de interacción y facilitando su uso táctil en mobile, cumpliendo con las directrices de accesibilidad del Design System.
- **Arquitectura de información — posición en el flujo:** La sección "Contacto" ocupa el último lugar en la jerarquía descendente de la Landing Page, recibiendo al usuario que ya procesó la propuesta de valor, las funciones y los precios, y está listo para dar el siguiente paso comercial. Esta posición es coherente con el Organization System definido.
- **Footer como cierre de identidad:** El copyright en el footer refuerza la identidad de marca y proporciona el cierre visual de la página de una sola columna, validando la estructura completa del Navigation System de One-Page Scroll.


### 4.3.2. Landing Page Mock-up.

- Home:
<div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landing-nosotros.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El Mock-up del Hero Section aplica la paleta de colores del Design System sobre la estructura validada en el wireframe. El fondo negro absoluto (`#000000`) crea el contexto de alto contraste que caracteriza la identidad visual de SpotTrack. El titular principal "Transforma la gestión de tu **gimnasio** con tecnología inteligente" resalta la palabra "gimnasio" en color teal (`#00ccb2`), el acento primario de marca, estableciendo el foco semántico del mensaje en la palabra clave del sector objetivo.
 
El CTA principal "Comenzar Ahora →" adopta el color teal (`#00ccb2`) como fondo con texto negro, siguiendo la convención de CTA primario del Design System. El CTA secundario "Ver Demo" se presenta con contorno sutil sobre fondo negro, subordinado visualmente al primario. El navbar superior presenta el logo SpotTrack con el isotipo de nodo estilizado a la izquierda, los ítems de navegación en tipografía secundaria Regular en el centro, y el botón "Iniciar Sesión" como texto y "Demo Gratis" como botón con fondo dorado (`#f5bc36`) a la derecha.
 
En la versión mobile, el navbar muestra el logo y el botón "Iniciar Sesión" con un selector de idioma (EN/ES), evidenciando la funcionalidad de internacionalización definida en US08. El texto del título se redistribuye en dos líneas con la palabra "gimnasio" en verde, manteniendo el énfasis cromático en la palabra clave. La fila de métricas clave ("Reduce tiempos de espera", "Monitoreo 24/7", "Alertas automáticas", "Dashboard en tiempo real") en la parte inferior utiliza tipografía Bold en blanco puro sobre fondo negro.
 
**Principios y elementos de diseño aplicados:**
 
- **Identidad de marca aplicada:** El acento de color teal (`#00ccb2`) en la palabra "gimnasio" y en el CTA primario establece la identidad cromática de SpotTrack de forma inmediata en el primer punto de contacto visual, aplicando el branding definido en el Design System.
- **Contraste de alto impacto:** La combinación de texto blanco y teal sobre fondo negro garantiza ratios de contraste elevados, cumpliendo con los estándares de accesibilidad WCAG AA para texto sobre fondo oscuro.
- **Jerarquía tipográfica completa:** El titular en tipografía primaria Bold de gran escala, el subtítulo en tipografía secundaria Regular de peso medio y las métricas en Bold de tamaño menor crean la jerarquía visual de tres niveles definida en el Design System.
- **Diseño inclusivo — selector de idioma:** En la versión mobile, los botones de cambio de idioma "EN" y "ES" son etiquetas textuales explícitas (no solo banderas), garantizando la comprensión para usuarios con dificultades de reconocimiento visual de iconos de idioma.
- **Background con textura de partículas:** En la versión mobile del mock-up, el fondo del Hero incorpora un patrón de puntos sutiles sobre negro, añadiendo profundidad visual sin comprometer la legibilidad del texto superpuesto, respetando el principio de contraste accesible del Design System.

- Features:
  <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landing-features.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El Mock-up de la sección "La Solución" aplica la paleta de color completa sobre la cuadrícula de seis tarjetas validada en el wireframe. Los íconos de línea de cada tarjeta adoptan el color teal (`#00ccb2`) del acento primario de marca, siendo los únicos elementos cromáticos de la sección junto al subtítulo "SpotTrack: Gestión inteligente todo en uno" que se presenta en dorado (`#f5bc36`). El fondo de las tarjetas mantiene el `#1a1a1a` con bordes redondeados, consistente con el componente de tarjeta definido en el Design System.
 
Los títulos de cada característica (Sensores IoT Edge, Almacenamiento en la Nube, Monitoreo en Tiempo Real, Alertas de Mantenimiento, Dashboard Analítico, Seguridad JWT) se presentan en tipografía secundaria SemiBold en blanco, y los párrafos descriptivos en Regular gris claro.
 
**Principios y elementos de diseño aplicados:**
 
- **Color teal como acento funcional:** Los íconos teal (`#00ccb2`) en cada tarjeta son el único uso del acento primario de marca en esta sección, creando un ritmo visual consistente que refuerza la identidad cromática de SpotTrack sin sobrecargar la paleta. El teal transmite la sensación de tecnología limpia y eficiencia que el Design System define para este color.
- **Dorado como acento de subtítulo:** El subtítulo en `#f5bc36` aplica el Secondary Accent del Design System para resaltar el nombre del producto y el claim de sección, diferenciándolo del texto de cuerpo sin usar el teal en dos roles simultáneos.
- **Principio de redundancia de canales:** Cada característica se comunica mediante tres canales simultáneos: ícono teal (canal visual-simbólico), título en blanco (canal textual-primario) y descripción en gris (canal textual-secundario), garantizando la comprensión para usuarios con dificultades en cualquiera de los canales individuales.
- **Diseño inclusivo:** Los íconos de línea son simples, reconocibles y semánticamente relacionados con su función (onda = señal IoT, nube = almacenamiento, escudo = seguridad), pero el texto acompañante garantiza que el usuario comprenda la función incluso si no reconoce el ícono.


- Pricing:
   <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landing-pricing.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El Mock-up de "Planes y Precios" es la sección con mayor densidad de uso del Design System en la Landing Page. La tarjeta central "Mid" adopta un borde dorado (`#f5bc36`) que la enmarca completamente, y la etiqueta "Más Popular" sobre el borde superior se presenta con fondo dorado y texto negro, siendo el elemento de mayor énfasis visual de toda la sección. Los checkmarks de las listas de características adoptan el color dorado (`#f5bc36`) en las tres tarjetas, aplicando el Secondary Accent como indicador de verificación positiva.
 
El CTA del plan Mid ("Comprar Ahora") adopta el fondo dorado sólido con texto negro, siguiendo la jerarquía de CTA primario del Design System. Los CTAs de Basic ("Comprar Ahora") y Platinum ("Comprar Ahora") mantienen el estilo de contorno blanco sobre fondo de tarjeta, siendo visualmente subordinados al CTA del plan recomendado. Los precios ($69, $109, $189) se presentan en tipografía primaria Bold de gran escala en blanco, siendo el elemento de mayor tamaño tipográfico dentro de cada tarjeta.
 
**Principios y elementos de diseño aplicados:**
 
- **Dorado como color de acento de decisión:** El `#f5bc36` aplicado al borde de la tarjeta Mid, a la etiqueta "Más Popular", a los checkmarks y al CTA principal crea un sistema visual coherente que guía la atención del usuario hacia el plan recomendado mediante énfasis cromático, sin necesitar texto adicional para comunicar la recomendación.
- **Jerarquía de CTAs por color:** El CTA dorado sólido del plan Mid vs. los CTAs de contorno blanco de Basic y Platinum establece una jerarquía de acción explícita: el sistema recomienda el Mid mediante el mayor énfasis de CTA, pero no bloquea la elección libre del usuario al mantener los otros CTAs visibles y accesibles.
- **Diseño inclusivo:** Los checkmarks dorados acompañan siempre a texto descriptivo de cada característica, no siendo el único indicador de inclusión en el plan. El ratio de contraste entre texto blanco y fondo de tarjeta oscuro, y entre texto negro y fondo dorado del CTA, cumple con los estándares de accesibilidad.
- **Arquitectura de información — comparativa de planes:** La disposición en tres columnas de igual altura permite la comparación visual directa entre planes siguiendo la misma estructura, aplicando el principio de alineación para facilitar la comparación sin necesidad de interacción adicional (hover, tabs o acordeones).

- Contact:
 <div align= "center">
  <align>
    <img src="../assets/landing-spottrack/landing-contact.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El Mock-up de la sección "Contacto" aplica el Design System sobre el formulario validado en el wireframe. El título "Contacto" se presenta en tipografía primaria Bold en blanco sobre fondo negro. El formulario se contiene en una tarjeta con fondo `#1a1a1a` y bordes redondeados en la versión wireframe web, consistente con el componente de tarjeta del Design System. Los campos de formulario (Nombre, Email, Mensaje) muestran sus etiquetas en tipografía secundaria SemiBold en blanco por encima de cada input, y los inputs tienen fondo oscuro (`#2a2a2a`) con borde sutil y placeholder en gris medio.
 
El botón "Enviar" adopta el fondo gris claro en el estado inicial (no activo, sin datos ingresados), siguiendo el patrón de CTA deshabilitado que se activa al completar los campos. El footer "© 2026 SpotTrack. Todos los derechos reservados." cierra la página en tipografía secundaria Regular en gris sutil sobre fondo ligeramente más oscuro.
 
En la versión mobile (landing-contact.png), el formulario ocupa el ancho completo de la pantalla con los campos de mayor área táctil, el textarea de Mensaje con mayor altura para facilitar la escritura en teclado virtual, y el botón "Enviar" de ancho completo respetando las directrices táctiles del Design System.
 
**Principios y elementos de diseño aplicados:**
 
- **Etiquetas permanentes sobre los campos:** A diferencia del wireframe que usa placeholders únicos, el mock-up web presenta etiquetas visibles en texto blanco SemiBold por encima de cada campo (Nombre, Email, Mensaje), garantizando que la etiqueta no desaparezca al comenzar a escribir — requisito de diseño inclusivo para usuarios con dificultades cognitivas o de memoria de trabajo.
- **CTA de ancho completo:** El botón "Enviar" ocupa el ancho total del contenedor en ambas versiones (desktop y mobile), maximizando el área de interacción y aplicando las directrices de accesibilidad táctil del Design System.
- **Footer como elemento de cierre de identidad:** El copyright en tipografía sutil cierra la landing page sin añadir ruido visual, preservando el foco del usuario en la acción de contacto. El contraste reducido (gris sobre gris oscuro) aplica el principio de jerarquía visual: el footer es información de soporte, no contenido primario.
- **Diseño inclusivo — campo Mensaje con área amplia:** El textarea con altura generosa facilita la escritura de mensajes largos sin necesidad de scroll interno del campo, reduciendo la fricción para usuarios con motricidad fina reducida o que usen teclado virtual en dispositivos móviles.
- **Arquitectura de información — posición de cierre:** La sección Contacto como último elemento antes del footer cierra el flujo narrativo descendente de la Landing Page (propuesta de valor → funciones → precios → acción de contacto), cumpliendo con la jerarquía establecida en el Organization System y el modelo de conversión progresiva definido para la Landing Page Comercial.

## 4.4. Web Applications UX/UI Design.
### 4.4.1. Web Applications Wireframes.

1. <strong>Wireframe 1:</strong> Selección de planes de suscripción SaaS

<strong>User story asociada:</strong> 
<br> US04: Como administrador, quiero visualizar la comparativa de precios (Basic, Mid, Platinum), para saber qué plan se ajusta a mi negocio.

<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe4_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Web – Desktop):**
 
El wireframe de la sección "Planes y Precios" muestra tres tarjetas de suscripción dispuestas en un layout de tres columnas sobre fondo oscuro, siguiendo el grid de 12 columnas establecido en las Web Style Guidelines. La tarjeta central ("Mid – $109/mes") se distingue de las demás mediante una etiqueta "Más Popular" en la parte superior y un borde de mayor grosor, estableciendo la jerarquía visual sin necesidad de color.
 
**Principios y elementos de diseño aplicados:**
 
- **Jerarquía visual por tamaño y posición:** El precio de cada plan se presenta en el mayor tamaño tipográfico de la tarjeta, seguido del nombre del plan y la lista de características. Esta escala tipográfica sigue la jerarquía H1/H2/Body definida en el Design System.
- **Principio de énfasis:** La tarjeta del plan "Mid" utiliza borde diferenciado y etiqueta superior para jerarquizar la opción recomendada sin depender del color, validando que la distinción sea estructural y no cromática.
- **Consistencia de componentes:** Las tres tarjetas comparten la misma estructura interna (nombre, precio, lista con íconos de check, botón CTA), aplicando el principio de consistencia del Design System atómico.
- **Diseño inclusivo:** Los íconos de verificación acompañan a cada característica listada (no solo color), asegurando la comprensión independientemente de la percepción cromática del usuario.
- **Arquitectura de información:** La sección sigue la jerarquía descendente top-down de la Landing Page: el usuario llega a esta sección tras haber procesado el Hero Section y las Features, siguiendo el flujo lógico de decisión de compra establecido en el Organization System.
- **Spacing:** El espaciado entre tarjetas y entre elementos internos respeta la escala de múltiplos de 8px definida en las Web Style Guidelines, manteniendo el ritmo visual de la página.


2. <strong>Wireframe 2:</strong> Envío de formulario de Contacto

<strong>User story asociada:</strong> 
<br> US05: Como visitante, quiero poder llenar un formulario con mis datos y mensaje, para solicitar información al equipo de ventas de Spot Track.

<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe5_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del wireframe (Web – Desktop):**
 
El wireframe presenta la página "Contacto" en tres estados: el formulario vacío (estado inicial), el formulario con datos válidos completos (usuario "Carla Gallardo") y el formulario con un error de validación en el campo Email ("Dirección de email inválida"). La estructura es centralizada con el formulario en un contenedor de ancho medio sobre el fondo oscuro de la página.
 
**Principios y elementos de diseño aplicados:**
 
- **Principio de visibilidad del estado del sistema:** El tercer estado del wireframe muestra el campo Email con un mensaje de error de validación visible debajo del input, confirmando al usuario el problema específico antes de que intente enviar el formulario. Esto aplica retroalimentación proactiva y prevención de errores.
- **Minimalismo estructural:** El formulario se compone únicamente de los campos estrictamente necesarios (Nombre, Email, Mensaje), reduciendo la carga cognitiva. La decisión de limitar los campos es visible desde la etapa de wireframe.
- **Etiquetas posicionadas sobre los inputs:** En los tres estados del wireframe se aprecia que las etiquetas ("Nombre", "Email", "Mensaje") están fijas por encima de cada campo, nunca dentro como único placeholder, garantizando su visibilidad permanente durante el llenado — requisito de diseño inclusivo para usuarios con dificultades cognitivas o de memoria de trabajo.
- **CTA de ancho completo:** El botón "Enviar" ocupa el ancho total del contenedor del formulario, maximizando el área de interacción en consonancia con las directrices de accesibilidad táctil del Design System.
- **Arquitectura de información:** El footer de la página con copyright ("© 2026 SpotTrack. Todos los derechos reservados.") es visible en el wireframe, confirmando la estructura completa de la Landing Page y su posición dentro del Navigation System como destino final del scroll.
- **Navbar persistente:** El wireframe conserva el navbar superior con los botones "Iniciar Sesión" y "Demo Gratis", manteniendo la coherencia de navegación global definida en el sistema.


3. <strong>Wireframe 3:</strong> Acceso al portal desde la navegación

<strong>User story asociada:</strong> 
<br> US06: Como visitante o cliente potencial, quiero tener botones de Login y Demo a la vista, para ingresar a la plataforma de forma rápida desde la landing page.

<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe6_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Web – Desktop):**
 
Esta historia se refleja transversalmente en los wireframes de la Landing Page a través de la barra de navegación superior fija (Sticky Top Navbar). El wireframe muestra el logo SpotTrack en el extremo izquierdo, los ítems de navegación ("Nosotros", "Funciones", "Precios") en el centro, y los controles de autenticación ("Iniciar Sesión" como enlace de texto y "Demo Gratis" como botón con fondo gris diferenciado) en el extremo derecho.
 
**Principios y elementos de diseño aplicados:**
 
- **Affordance estructural:** En el wireframe, el botón "Demo Gratis" adopta un rectángulo relleno de gris más oscuro que diferencia su naturaleza de CTA del enlace de texto "Iniciar Sesión", estableciendo la jerarquía de acciones a nivel estructural antes de aplicar color.
- **Principio de persistencia:** Al ser un componente sticky, el wireframe valida que los controles de autenticación estén presentes en todas las vistas de la Landing Page, eliminando la necesidad de regresar al inicio para acceder a la plataforma.
- **Labeling System:** Las etiquetas "Iniciar Sesión" y "Demo Gratis" corresponden al vocabulario definido en el Labeling System de la Arquitectura de Información, siendo directas, orientadas a la acción y libres de jerga técnica.
- **Diseño inclusivo:** El área del botón "Demo Gratis" tiene dimensiones suficientes para cumplir con el target mínimo de interacción táctil, validado estructuralmente desde el wireframe.
- **Arquitectura de información – Navigation Systems:** El wireframe valida el sistema de Sticky Top Navbar con Anchor Links a las secciones clave de la Landing Page, cumpliendo con la definición de One-Page Scroll Navigation del Navigation System.


4. <strong>Wireframe 4:</strong> Inicio de sesión con validación JWT

<strong>User story asociada:</strong> 
<br> US07: Como usuario, quiero iniciar sesión de forma segura generando un token, para acceder a mi panel de control o aplicación móvil correspondiente.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe7_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe7.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
Los wireframes muestran la pantalla "Iniciar Sesión" en múltiples estados y versiones: el formulario vacío en mobile (estado inicial), el formulario con credenciales de cliente ingresadas ("cliente@email.com") en mobile, y la versión web de escritorio con el panel de navegación demo abierto. En mobile, el formulario se presenta como una tarjeta centrada sobre fondo oscuro; en desktop, el mismo componente se escala manteniendo el mismo orden estructural.
 
**Principios y elementos de diseño aplicados:**
 
- **Jerarquía tipográfica:** El wireframe establece la estructura de tres niveles: logo SpotTrack (identidad de marca), título "Iniciar Sesión" en el mayor tamaño tipográfico de la pantalla, y descripción en tipografía secundaria de menor peso. Esta jerarquía es perceptible incluso en escala de grises.
- **Responsive Design:** Los wireframes de mobile y desktop del mismo formulario evidencian que la estructura se adapta al viewport manteniendo el mismo orden de elementos: logo → título → descripción → campos → CTA → enlace de registro. Esto valida el sistema de grid responsive del Design System.
- **Diseño inclusivo — Sección "Demo de prueba":** El bloque de credenciales de demostración (Admin y Cliente) es estructuralmente visible en el wireframe como una subsección diferenciada por un borde sutil, reduciendo la barrera de entrada para evaluadores y nuevos usuarios sin comprometer la seguridad del diseño.
- **Etiquetas permanentes:** Los campos "Email" y "Contraseña" muestran sus etiquetas posicionadas sobre los inputs en todos los estados del wireframe, nunca dependiendo únicamente del placeholder.
- **Enlace de registro visible:** El texto "¿No tienes cuenta? Regístrate aquí" está posicionado inmediatamente debajo del CTA principal, conectando estructuralmente los flujos de login y registro en el wireframe.
- **Arquitectura de información:** El wireframe valida la redirección por rol: el texto de la pantalla indica "acceder a la plataforma", y el flujo documentado en el Organization System establece que la redirección post-login diferirá entre Admin (Dashboard) y Cliente (Mapa), sin que esto requiera lógica visual en esta pantalla.

5. <strong>Wireframe 5:</strong> Gestión de preferencias y perfil

<strong>User story asociada:</strong> 
<br> US08: Como usuario, quiero actualizar mi información personal y cambiar el idioma del sistema, para mantener mis datos al día y usar la plataforma cómodamente.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe8_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe8.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del wireframe (Mobile y Web – Desktop):**
 
Los wireframes presentan la pantalla "Mi Perfil" en versión mobile (columna única, scroll vertical) y en versión web de escritorio (misma estructura pero en contenedor más ancho). Se muestran tres estados: la vista estándar con los datos del usuario "Juan Pérez", el estado tras pulsar "Guardar Cambios" (con un banner de confirmación "¡Cambios guardados!" en la parte inferior) y el estado con el idioma cambiado a "Inglés". El Dashboard Admin también es visible en miniatura en el primer estado del wireframe web, mostrando el contexto de acceso desde el mapa de disponibilidad.
 
**Principios y elementos de diseño aplicados:**
 
- **Agrupación por proximidad (Gestalt):** El wireframe organiza el contenido del perfil en bloques semánticos claramente delimitados mediante bordes de tarjeta y espaciado interno consistente: bloque de usuario y puntos, información del plan, historial de puntos, información personal, preferencias de idioma, notificaciones y seguridad. Esta segmentación es estructural y visible sin color.
- **Jerarquía tipográfica por sección:** Cada bloque lleva un encabezado de sección (ej. "Historial de Puntos", "Información Personal") en tipografía secundaria SemiBold con un ícono contextual, diferenciado en tamaño del contenido de la sección.
- **Feedback estructural:** El wireframe del estado de guardado exitoso muestra un banner en la parte inferior de la pantalla con el texto "¡Cambios guardados!", validando el posicionamiento del componente de retroalimentación sin aplicar color.
- **Botón CTA sticky:** El botón "Guardar Cambios" se posiciona al pie de la pantalla en todos los estados del wireframe, validando que permanezca accesible independientemente de cuánto haya scrolleado el usuario en el perfil.
- **Diseño inclusivo — Selector de idioma:** El dropdown de idioma muestra una bandera seguida del nombre del idioma en texto ("Español" / "Inglés"), combinando indicador visual e indicador textual para garantizar la comprensión sin depender de un único canal de información.
- **Diseño inclusivo — Notificaciones:** La sección de notificaciones presenta cada tipo de alerta con su nombre y una descripción explicativa del evento que la dispara, no solo el nombre de la preferencia, reduciendo la ambigüedad para usuarios con menor familiaridad con la plataforma.
- **Arquitectura de información:** La pantalla es accesible desde el ícono de perfil de la bottom navigation bar. El encabezado "Mi Perfil" con flecha de retroceso valida el sistema de navegación jerárquica de la aplicación móvil definido en el Navigation System.

 6. <strong>Wireframe 6:</strong> Visualización del mapa de calor en VIVO

<strong>User story asociada:</strong> 
<br> US09: Como cliente frecuente, quiero ver la disponibilidad de las máquinas en tiempo real (verde/rojo), para esquivar aglomeraciones y no perder tiempo en filas.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe9_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe9.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
El wireframe presenta la pantalla principal de la aplicación móvil y su equivalente web, mostrando el "Mapa de Disponibilidad en Tiempo Real". El mapa central despliega los íconos de cada máquina en una cuadrícula semiespacial dentro de un contenedor de fondo oscuro. En escala de grises, los tres estados de las máquinas se distinguen mediante diferentes tonos de gris (más claro para Libre, gris medio para Reservado con contador, gris oscuro para Ocupado). La leyenda inferior ("Libre (4), Ocupado (3), Reservado (1)") complementa la información del mapa.
 
**Principios y elementos de diseño aplicados:**
 
- **Jerarquía visual de la App Móvil:** El mapa ocupa la posición central y absoluta de la pantalla, subordinando todas las demás funciones a la barra de navegación inferior. Esto valida el Organization System de la Web App B2C que posiciona el mapa como componente de máxima prioridad.
- **Codificación por tono (sin color):** En el wireframe, los tres estados de disponibilidad se diferencian mediante variaciones tonales de gris, validando que la estructura semafórica no depende exclusivamente del color y es comprensible en escala de grises — requisito clave de diseño inclusivo.
- **Leyenda estructural:** La leyenda con puntos y etiquetas textuales debajo del mapa combina indicador icónico e indicador textual, garantizando la comprensión del sistema de estados para usuarios con daltonismo o baja visión, cumpliendo con las directrices de diseño inclusivo.
- **Contador de tiempo regresivo:** El badge "09:59" sobre el ícono de la máquina en estado Reservado es visible en el wireframe, validando el posicionamiento del componente de feedback temporal sin aplicar color.
- **Bottom Navigation Bar:** La barra inferior con cuatro destinos (Mapa, Reservas, Rutinas, Perfil) con íconos y etiquetas textuales es visible y consistente en todas las vistas del wireframe, cumpliendo con el Navigation System de la aplicación móvil.
- **Selector de sede y filtros:** El dropdown "Gimnasio Centro" y los botones de filtro ("Todos / Fuerza / Cardio") son componentes estructurales del wireframe, validando el Searching System facetado definido en la Arquitectura de Información.
- **Arquitectura de información:** El título "Mapa de Disponibilidad en Tiempo Real" con su subtítulo "Visualiza el estado de todas las máquinas del gimnasio" funciona como encabezado de contexto que orienta al usuario sin necesidad de interacción previa.

 7. <strong>Wireframe 7:</strong> Filtrado del inventario por tipo de máquina

<strong>User story asociada:</strong> 
<br> US10: Como cliente frecuente, quiero seleccionar etiquetas (ej. Fuerza o Cardio) en el mapa, para visualizar únicamente las máquinas relevantes para mi rutina.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe10_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe10.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del wireframe (Mobile y Web – Desktop):**
 
El wireframe muestra el mapa de disponibilidad con el sistema de filtros activado, presentando en paralelo el estado con el filtro "Fuerza" activo y el estado con el filtro "Cardio" activo. En ambos casos, el botón del filtro seleccionado adopta un relleno de gris más oscuro que los botones no activos, distinguiendo visualmente el estado activo sin color. Se incluye además un botón "Limpiar" junto a los filtros de categoría, cumpliendo con el escenario 2 de los criterios de aceptación.

  **Principios y elementos de diseño aplicados:**
 
- **Estado activo estructural:** La diferencia entre el botón de filtro activo (relleno gris oscuro) y los inactivos (contorno sutil) es visible en escala de grises, validando que el estado activo no depende del color para ser percibido — principio de visibilidad del estado del sistema aplicado desde el wireframe.
- **Filtrado facetado (Searching System):** Las etiquetas "Todos", "Fuerza", "Cardio" y "Limpiar" corresponden exactamente al sistema de filtros por categoría definido en el Searching System, validando su implementación estructural en la interfaz.
- **Consistencia del mapa:** El wireframe muestra que al aplicar el filtro, el layout del mapa mantiene su estructura espacial, validando que el cambio de estado no altera la organización de la pantalla ni genera desorientación en el usuario.
- **Diseño inclusivo — Etiqueta textual del filtro activo:** Las etiquetas de los botones de filtro emplean lenguaje directo del Labeling System ("Fuerza", "Cardio") en lugar de códigos o íconos únicos, asegurando la comprensión para todo el espectro de usuarios.
- **Botón "Limpiar":** Su posición consistente junto al grupo de filtros es validada en el wireframe, garantizando que el usuario pueda restablecer la vista completa del inventario con una acción predecible.


 8. <strong>Wireframe 8:</strong> Cambio de sucursal para revisión de aforo

<strong>User story asociada:</strong> 
<br> US11: Como cliente frecuente, quiero seleccionar otras sedes en la app, para revisar el croquis y aforo de sucursales alternas antes de salir de casa.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe11_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe11.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
Los wireframes muestran el flujo de cambio de sede en dos estados: la vista con "Gimnasio Centro" seleccionado y la misma pantalla tras seleccionar "Gimnasio Norte" desde el dropdown. La versión web de escritorio muestra adicionalmente el menú desplegado del selector de sede con las tres opciones disponibles (Gimnasio Centro, Gimnasio Norte, Gimnasio Sur). En todos los casos, la estructura de la pantalla permanece idéntica al cambiar de sede, variando únicamente el nombre en el selector y el contenido del mapa.
 
**Principios y elementos de diseño aplicados:**
 
- **Control del usuario:** El dropdown de selección de sede en el wireframe otorga al usuario pleno control para cambiar el contexto de visualización sin salir de la pantalla principal, validando el principio de libertad y control del usuario desde la etapa de estructura.
- **Ícono semántico de ubicación:** El ícono de pin de ubicación junto al nombre de la sede es visible en el wireframe y refuerza semánticamente la función del control selector, cumpliendo con el principio de reconocimiento sobre recuerdo.
- **Consistencia entre sedes:** Los wireframes de "Gimnasio Centro" y "Gimnasio Norte" mantienen exactamente la misma estructura de pantalla, validando que el usuario no deba reaprender la interfaz al cambiar de sede.
- **Arquitectura de información:** El selector de sede corresponde al filtro por Sede definido en el Searching System de la Arquitectura de Información, trasladado al contexto de la aplicación cliente. La versión web muestra el dropdown con las tres opciones de sede disponibles, validando el Labeling System con nombres de sede directos.
- **Diseño inclusivo:** Los nombres de las sedes en el dropdown son descriptivos y únicos (Gimnasio Centro, Norte, Sur), evitando ambigüedades o nomenclaturas de código que podrían dificultar la selección para usuarios con menor familiaridad con la plataforma.


9. <strong>Wireframe 9:</strong> Notificaciones push de resolución de disponibilidad

<strong>User story asociada:</strong> 
<br> US12: Como cliente frecuente, quiero activar una campana de aviso, para recibir una alerta en mi celular cuando la máquina que esperaba se libere.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe12_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe12.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
El wireframe presenta dos estados del flujo de notificación: el mapa de disponibilidad en estado normal (sin notificación activa) y el estado posterior a la liberación de una máquina, donde aparece un banner de notificación en la parte inferior de la pantalla con el texto "✗ Máquina ocupada nuevamente" (escenario de descarte automático) o la notificación positiva de liberación. En el wireframe web, el mismo banner aparece como un toast notification de ancho completo en la parte inferior del viewport.
 
**Principios y elementos de diseño aplicados:**
 
- **Posicionamiento del feedback:** El banner de notificación se posiciona en la parte inferior de la pantalla (toast notification), validando en el wireframe que el componente de feedback es no bloqueante: el usuario puede ver simultáneamente el mapa actualizado sin que la notificación ocupe toda la pantalla.
- **Texto descriptivo en la notificación:** El mensaje "Máquina ocupada nuevamente" emplea el Labeling System del producto con lenguaje natural y directo, evitando códigos técnicos, validado desde el wireframe antes de aplicar color o iconografía final.
- **Diseño inclusivo:** La notificación combina un ícono (✗ o ✓) con texto descriptivo, no dependiendo exclusivamente del color o el ícono para comunicar el mensaje. Esto garantiza comprensión para usuarios con daltonismo o lectores de pantalla.
- **Actualización del mapa:** El wireframe muestra que el estado del mapa se actualiza simultáneamente con la aparición del banner, validando la coherencia del estado del sistema en todos sus canales de feedback.
- **Consistencia entre mobile y web:** Ambas versiones del wireframe muestran el mismo componente de notificación, validando la coherencia del Design System a través de los dos contextos de uso.


10. <strong>Wireframe 10:</strong> Sistema de recompensas de Crowdsourcing

<strong>User story asociada:</strong> 
<br> US13: Como cliente frecuente, quiero ganar puntos canjeables en mi perfil, para motivarme a actualizar manualmente el estado de disponibilidad de los equipos.

- web 
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe13_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe13.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
El wireframe muestra dos interacciones clave del flujo: el modal emergente al tocar una máquina libre ("Polea Alta – Estado: Libre") con las opciones "Reservar 15 minutos" y "Reportar como Ocupado", y la pantalla de confirmación posterior al reporte con el mensaje "Gracias por tu apoyo +25 puntos" sobre una superposición del mapa.
 
**Principios y elementos de diseño aplicados:**
 
- **Modal contextual:** Al tocar una máquina en el mapa, el wireframe valida que se despliega un modal superpuesto con información específica del equipo seleccionado (nombre y estado) y las acciones disponibles. El fondo del mapa se oscurece parcialmente, aplicando el principio de foco sin eliminar el contexto.
- **Jerarquía de acciones en el modal:** En el wireframe, la acción primaria "Reservar 15 minutos" adopta un relleno de gris más claro (equivalente al CTA primario en color) diferenciándose de "Reportar como Ocupado", que mantiene el estilo de botón secundario. Esta jerarquía estructural valida la implementación del Design System en la etapa de wireframe.
- **Botón de cierre (×):** El wireframe incluye el botón de cierre del modal en la esquina superior derecha, garantizando que el usuario pueda descartar la acción sin consecuencias involuntarias — principio de libertad y control del usuario.
- **Pantalla de confirmación gamificada:** El wireframe del estado de confirmación "+25 puntos" muestra el mensaje centrado sobre el mapa con una superposición oscura, validando el posicionamiento del componente de retroalimentación positiva y su jerarquía visual sobre el resto de la pantalla.
- **Arquitectura de información:** El flujo del modal conecta directamente con el historial de puntos del perfil (US08), cerrando el loop de la mecánica de gamificación. El wireframe valida que la interacción contextual desde el mapa no requiere cambio de pantalla para acceder a la acción de reporte.
- **Diseño inclusivo:** Los botones del modal incluyen íconos acompañando al texto (calendario para "Reservar", bandera para "Reportar"), añadiendo un canal visual de reconocimiento para la función de cada acción.


   11. <strong>Wireframe 11:</strong> Motor de sugerencia de rutinas alternativas

<strong>User story asociada:</strong> 
<br> US14: Como cliente del gimnasio, quiero recibir recomendaciones de ejercicios alternativos cuando mi máquina esté ocupada, para no perder mi ritmo de entrenamiento.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe14_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe/wireframe14.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del wireframe (Mobile y Web – Desktop):**
 
El wireframe presenta la sección "Rutinas y Ejercicios" en tres vistas: el mapa de disponibilidad (contexto del flujo), la lista de ejercicios con su disponibilidad actual y el panel "Rutinas alternativas" desplegado como drawer lateral. Cada tarjeta de ejercicio muestra el nombre, la máquina asociada, las etiquetas de grupo muscular y nivel de dificultad, y el estado de disponibilidad. La versión web de escritorio muestra las tres vistas simultáneamente en un layout de mayor ancho.
 
**Principios y elementos de diseño aplicados:**
 
- **Arquitectura de información — Labeling System:** Las etiquetas de grupo muscular ("Pectorales", "Piernas", "Espalda", "Hombros", "Brazos") como filtros de la sección y el buscador ("Buscar ejercicio o máquina...") son visibles en el wireframe, validando el sistema de categorización por tópicos definido para la aplicación móvil.
- **Estado integrado en el catálogo:** Cada tarjeta de ejercicio incorpora un badge de estado de disponibilidad (punto gris claro = Disponible, punto gris oscuro = Ocupado/Mantenimiento) en el wireframe, validando que la disponibilidad de la máquina es un atributo visible en la lista sin necesitar regresar al mapa.
- **Alternativas contextuales:** Cuando una máquina está ocupada ("Rack Sentadilla #2 – Ocupado"), el wireframe muestra que la tarjeta expande automáticamente una subsección "Alternativas disponibles:" con la lista de alternativas y su estado, eliminando la fricción de búsqueda manual.
- **Drawer de rutinas alternativas:** El panel "Rutinas alternativas" se despliega como drawer desde el lateral de la pantalla, mostrando tarjetas compactas con la misma estructura que el listado principal. El wireframe valida la consistencia de componentes entre el listado y el drawer, aplicando el principio de consistencia del Design System.
- **CTA "Ver en el Mapa":** El wireframe muestra el botón de ancho completo "Ver en el Mapa" en dorado al pie de la sección de alternativas disponibles, conectando el flujo de rutinas con el mapa de disponibilidad sin requerir navegación manual.
- **Diseño inclusivo — Buscador:** El campo de búsqueda en la parte superior del listado y del drawer permite a usuarios con necesidades específicas encontrar ejercicios por nombre sin depender exclusivamente de los filtros de categoría.
- **Diseño inclusivo — Mantenimiento como estado explícito:** El badge "Mantenimiento" en algunas tarjetas del drawer es visible estructuralmente en el wireframe, cumpliendo con el criterio de aceptación US14 escenario 2 que requiere excluir equipos con ticket técnico abierto y comunicarlo explícitamente al usuario.
- **Bottom Navigation Bar:** La barra inferior está activa en la pestaña "Rutinas" en todos los wireframes de esta historia, manteniendo la orientación del usuario dentro de la aplicación y validando el estado activo de navegación desde la etapa de estructura.
 
13. <strong>Wireframe 13:</strong> Sistema de reserva exprés en horas pico

<strong>User story asociada:</strong> 
<br> US16: Como cliente frecuente, quiero separar virtualmente una máquina libre por 10 minutos durante horas pico, para asegurar su uso mientras me dirijo a ella.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe13_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe13.png" alt="wireflow" width="500"/>
  </div> <br>

  14. <strong>Wireframe 14:</strong> Acumulación automática de horas de uso

<strong>User story asociada:</strong> 
<br> US17: Como administrador, quiero ver gráficos con la sumatoria de minutos reales de uso de cada máquina, para comprender la demanda real sin tener que vigilar el local.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe14_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe14.png" alt="wireflow" width="500"/>
  </div> <br>

  15. <strong>Wireframe 15:</strong> Identificación de equipos subutilizados

<strong>User story asociada:</strong> 
<br> US18: Como administrador, quiero que el sistema resalte en una tabla qué máquinas tienen una tasa de uso excepcionalmente baja, para evaluar su reubicación o descarte.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe18_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe18.png" alt="wireflow" width="500"/>
  </div> <br>

  16. <strong>Wireframe 16:</strong> Visualización de picos de estrés del local

<strong>User story asociada:</strong> 
<br> US19: Como dueño del negocio, quiero ver gráficos que destaquen las horas donde el aforo de máquinas supera el 90%, para identificar cuellos de botella diarios.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe19_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe19.png" alt="wireflow" width="500"/>
  </div> <br>

  17. <strong>Wireframe 17:</strong> Exportación de analíticas de uso

<strong>User story asociada:</strong> 
<br> US20: Como gerente de operaciones, quiero generar documentos formateados en PDF de los gráficos de uso, para presentar reportes formales de rendimiento.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe20_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe20.png" alt="wireflow" width="500"/>
  </div> <br>

  18. <strong>Wireframe 18:</strong> Monitoreo de estado de hardware Edge IoT

<strong>User story asociada:</strong> 
<br> US21: Como administrador, quiero revisar la salud de la red y el estado de los nodos IoT, para detectar si un sensor se ha desconectado.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe21_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe21.png" alt="wireflow" width="500"/>
  </div> <br>

  19. <strong>Wireframe 19:</strong> Alerta predictiva de mantenimiento

<strong>User story asociada:</strong> 
<br> US22: Como gerente de operaciones, quiero recibir alertas automáticas cuando un equipo supere sus horas seguras de uso, para realizar mantenimientos preventivos antes de que fallen.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe22_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe22.png" alt="wireflow" width="500"/>
  </div> <br>

  20. <strong>Wireframe 20:</strong> Despacho automatizado de tickets técnicos

<strong>User story asociada:</strong> 
<br> US23: Como gerente de operaciones, quiero que el sistema convierta una alerta en un ticket técnico y notifique al soporte, para agilizar la reparación.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe23_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe23.png" alt="wireflow" width="500"/>
  </div> <br>

  21. <strong>Wireframe 21:</strong> Notificación de restablecimiento a los usuarios

<strong>User story asociada:</strong> 
<br> US24: Como administrador, quiero que el sistema notifique a los clientes cuando un equipo reportado es reparado, para mejorar su percepción del servicio.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe24_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe24.png" alt="wireflow" width="500"/>
  </div> <br>

  22. <strong>Wireframe 22:</strong> Calendario inteligente de bloqueos por mantenimiento

<strong>User story asociada:</strong> 
<br> US25: Como gerente de operaciones, quiero que el sistema agende los mantenimientos preventivos exclusivamente en horarios valle, para no afectar la disponibilidad en horas de alta demanda.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe25_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe25.png" alt="wireflow" width="500"/>
  </div> <br>

  23. <strong>Wireframe 23:</strong> Gestión de activos físicos y altas

<strong>User story asociada:</strong> 
<br> US26: Como administrador, quiero registrar o dar de baja equipos vinculándolos a un sensor IoT, para actualizar el inventario digital y el mapa de calor.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe26_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe26.png" alt="wireflow" width="500"/>
  </div> <br>

  24. <strong>Wireframe 24:</strong> Estadísticas de reubicación multisede

<strong>User story asociada:</strong> 
<br> US27: Como administrador, quiero registrar o dar de baja equipos vinculándolos a un sensor IoT, para actualizar el inventario digital y el mapa de calor.

- web
<div align= "center">
  <align>
    <img src="../assets/wireframe27_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe27.png" alt="wireflow" width="500"/>
  </div> <br>

  25. <strong>Wireframe 25:</strong> 	Gestión automatizada de stock de repuestos

<strong>User story asociada:</strong> 
<br> US28: Como administrador, quiero controlar el inventario de piezas clave y recibir alertas de reabastecimiento, para que los técnicos siempre tengan insumos disponibles.
- web
<div align= "center">
  <align>
    <img src="../assets/wireframe28_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe28.png" alt="wireflow" width="500"/>
  </div> <br>

  26. <strong>Wireframe 26:</strong> 	Calculadora de impacto financiero por inactividad

<strong>User story asociada:</strong> 
<br> US29: Como dueño del negocio, quiero cuantificar la pérdida monetaria estimada por cada hora de inactividad de una máquina, para entender el impacto real de las averías.
- web
<div align= "center">
  <align>
    <img src="../assets/wireframe29_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe29.png" alt="wireflow" width="500"/>
  </div> <br>

  27. <strong>Wireframe 27:</strong> 		Analítica predictiva de compras e inversión

<strong>User story asociada:</strong> 
<br> US30: Como dueño del negocio, quiero reportes basados en la tasa de uso para proyectar inversiones y simular el ROI, para tomar decisiones sobre qué equipos adquirir o descartar.
- web
<div align= "center">
  <align>
    <img src="../assets/wireframe30_web.png" alt="wireflow" width="500"/>
  </div> <br>

- mobile
  <div align= "center">
  <align>
    <img src="../assets/wireframe30.png" alt="wireflow" width="500"/>
  </div> <br>

### 4.4.2. Web Applications Wireflow Diagrams.

1. <strong>Wireflow 1:</strong> Selección de planes de suscripción SaaS

- User goal: Como administrador, quiero visualizar la comparativa de precios. 

<strong>User story asociada:</strong> 
<br> US04: Como administrador, quiero visualizar la comparativa de precios (Basic, Mid, Platinum), para saber qué plan se ajusta a mi negocio.


<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow4_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Hero Section:** El usuario visualiza la propuesta de valor principal de SpotTrack con los CTAs "Comenzar Ahora →" y "Ver Demo". Al hacer scroll o seleccionar "Precios" en el navbar, el sistema desplaza la vista hacia la sección de planes.
2. **Sección "Planes y Precios":** Se muestran las tres tarjetas (Basic $69/mes, Mid $109/mes, Platinum $189/mes) con sus características y CTAs diferenciados. Al presionar "Demo Gratis" en el plan Basic o "Comenzar Ahora →" en el plan Mid, el sistema redirige al formulario de creación de cuenta.
3. **Formulario "Crear Cuenta" (vacío → con datos):** El usuario completa los campos: Nombre Completo, Email, Teléfono, Tipo de Usuario (dropdown "Administrador de Gimnasio"), Contraseña y Confirmar Contraseña. El wireflow muestra la transición del estado vacío al estado con datos ingresados.
4. **Transición al Login:** Al presionar "Crear Cuenta", si los datos son válidos, el sistema redirige automáticamente (flecha diagonal en el wireflow) a la pantalla de "Iniciar Sesión", cerrando el flujo de onboarding.

2. <strong>Wireflow 2:</strong> Envío de formulario de Contacto

- User goal: Como visitante, quiero poder llenar un formulario con mis datos y mensaje. 

<strong>User story asociada:</strong> 
<br> US05: Como visitante, quiero poder llenar un formulario con mis datos y mensaje, para solicitar información al equipo de ventas de Spot Track.

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow5_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción de cada paso:**
 
1. **Formulario vacío:** La página muestra los campos Nombre, Email y Mensaje con sus placeholders orientativos y el botón "Enviar" inactivo estructuralmente. El footer con copyright es visible al final de la página.
2. **Formulario con datos válidos:** El wireflow muestra el estado completado con datos reales (nombre: "carla gallardo", email: "carllaaaa28@hotmail.com", mensaje descriptivo del problema con las máquinas). El campo Mensaje tiene el borde activo, indicando que es el campo en foco.
3. **Estado de error de validación:** Al introducir un email inválido, el sistema muestra el mensaje "Dirección de email inválida" debajo del campo Email, impidiendo el envío. El campo Nombre mantiene el valor ingresado ("carla gallardo") para no obligar al usuario a reingresar toda la información.
**Principio de diseño aplicado:** El wireflow evidencia el principio de **prevención de errores y retroalimentación proactiva**: el sistema valida el email antes del envío, no después, mostrando el error de forma localizada en el campo afectado, reduciendo la frustración del usuario. La persistencia de los datos válidos en el formulario (nombre conservado) aplica el principio de eficiencia de uso.
 

3. <strong>Wireflow 3:</strong> Acceso al portal desde la navegación

- User goal: Como visitante o cliente potencial, quiero tener botones de Login y Demo.

<strong>User story asociada:</strong> 
<br> US06: Como visitante o cliente potencial, quiero tener botones de Login y Demo a la vista, para ingresar a la plataforma de forma rápida desde la landing page.

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow6_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Navbar persistente:** En todos los wireflows de la Landing Page (Hero Section, Planes y Precios, Contacto), el navbar superior muestra de forma consistente los controles de acceso "Iniciar Sesión" (enlace de texto) y "Demo Gratis" (botón con fondo diferenciado). Su posición en el extremo derecho del navbar sigue la convención de navegación web establecida.
2. **Redirección a "Iniciar Sesión":** Al hacer clic en "Iniciar Sesión", el sistema redirige directamente al formulario de autenticación de la plataforma, sin pasos intermedios.
3. **Redirección a "Crear Cuenta":** Al hacer clic en "Demo Gratis", el sistema redirige al formulario de registro, iniciando el flujo de onboarding de US04.
**Principio de arquitectura de información aplicado:** El Sticky Top Navbar con los dos CTAs de acceso cumple con el Navigation System definido: navegación global superior fija con CTA persistente, eliminando la necesidad de que el usuario regrese al inicio de la página para encontrar el punto de acceso a la plataforma.

4. <strong>Wireflow 4:</strong> Inicio de sesión con validación JWT

- User goal: Como usuario, quiero iniciar sesión de forma segura generando un token.

<strong>User story asociada:</strong> 
<br> US07: Como usuario, quiero iniciar sesión de forma segura generando un token, para acceder a mi panel de control o aplicación móvil correspondiente.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow7.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow7_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Formulario vacío:** La pantalla muestra el logo SpotTrack, el título "Iniciar Sesión", los campos Email y Contraseña (con placeholder "tu@email.com" y puntos de contraseña), el CTA principal "Iniciar Sesión", el enlace "¿No tienes cuenta? Regístrate aquí" y la sección de demo con credenciales de prueba.
2. **Formulario con credenciales de cliente:** El wireflow muestra el estado del formulario con "cliente@email.com" ingresado en el campo Email y la contraseña enmascarada en el campo Contraseña. Este estado ilustra el momento previo al envío.
3. **Redirección por rol:** Al presionar "Iniciar Sesión", el sistema valida las credenciales y genera el token JWT. La flecha del wireflow bifurca el flujo: si el rol es Cliente, redirige al Mapa de Disponibilidad (pantalla central de la App); si el rol es Admin, redirige al Dashboard Gerencial. En el wireflow web se aprecia el panel de "Navegación Demo" que permite al evaluador saltar entre las secciones del prototipo.

  5. <strong>Wireflow 5:</strong> Gestión de preferencias y perfil

- User goal: Como usuario, quiero actualizar mi información personal y cambiar el idioma

<strong>User story asociada:</strong> 
<br> US08: Como usuario, quiero actualizar mi información personal y cambiar el idioma del sistema, para mantener mis datos al día y usar la plataforma cómodamente.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow8.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow8_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción de cada paso:**
 
1. **Punto de entrada desde el Dashboard/Mapa:** La flecha del wireflow parte desde el Dashboard Administrativo (con gráficos de "Horas Pico de Capacidad", "Uso de Máquinas" y "Equipos Subutilizados" visibles en la versión Admin) hacia la pantalla de perfil del cliente, conectando ambos contextos de uso.
2. **Pantalla "Mi Perfil" - estado inicial:** Muestra todos los bloques de información: datos del usuario (Juan Pérez, 245 puntos acumulados, badge "Cliente"), Plan Basic con CTA "Mejorar Plan", Historial de Puntos (+25, +15, +20 pts), Información Personal (nombre, email, teléfono), Preferencias de Idioma, Notificaciones y Seguridad.
3. **Estado con datos modificados:** El wireflow muestra el momento en que el usuario ha editado algún campo o cambiado el selector de idioma. El botón "Guardar Cambios" al pie de la pantalla permanece visible y es el CTA que dispara la acción.
4. **Confirmación de guardado:** Tras presionar "Guardar Cambios", aparece el banner de confirmación en la parte inferior de la pantalla. En el wireflow web se aprecia el banner "¡Cambios guardados!" como un toast que no ocupa la pantalla completa.
5. **Cambio de idioma:** Un estado adicional del wireflow muestra el selector de idioma con "Inglés" activo, ilustrando el escenario 2 de los criterios de aceptación.


 6. <strong>Wireflow 6:</strong> Visualización del mapa de calor en VIVO

- User goal: Como cliente frecuente, quiero ver la disponibilidad de las máquinas en tiempo real.

<strong>User story asociada:</strong> 
<br> US09: Como cliente frecuente, quiero ver la disponibilidad de las máquinas en tiempo real (verde/rojo), para esquivar aglomeraciones y no perder tiempo en filas.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow9.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow9_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Login a Mapa:** La flecha del wireflow conecta directamente el formulario de login con el estado completo del Mapa de Disponibilidad, representando la redirección automática post-autenticación para usuarios con rol Cliente.
2. **Mapa de Disponibilidad:** La pantalla central muestra el contenedor del mapa con 8 íconos de máquinas distribuidos en una cuadrícula 3×3 (con dos posiciones vacías en la tercera fila). Los íconos tienen diferentes tonos de gris en el wireflow para representar los tres estados: claro (Libre), medio con badge de tiempo (Reservado - "09:59"), oscuro (Ocupado). Todos los íconos incluyen el glifo de pesas de SpotTrack.
3. **Elementos persistentes:** El selector de sede "Gimnasio Centro" con dropdown, los filtros de categoría ("Todos" activo, "Fuerza", "Cardio") y la bottom navigation bar son visibles y accesibles desde este estado sin interacción adicional.

 7. <strong>Wireflow 7:</strong> Filtrado del inventario por tipo de máquina

- User goal: Como cliente frecuente, quiero seleccionar etiquetas en el mapa.

<strong>User story asociada:</strong> 
<br> US10: Como cliente frecuente, quiero seleccionar etiquetas (ej. Fuerza o Cardio) en el mapa, para visualizar únicamente las máquinas relevantes para mi rutina.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow10.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow10_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Estado con filtro "Fuerza":** El wireflow muestra el botón "Fuerza" con relleno de fondo gris más oscuro que los otros botones, diferenciándolo visualmente como estado activo. El botón "Limpiar" aparece a la derecha del grupo de filtros.
2. **Transición a filtro "Cardio":** La flecha horizontal del wireflow conecta el estado "Fuerza" activo con el estado "Cardio" activo, ilustrando que el usuario puede cambiar de filtro con un solo clic sin pasar por el estado "Todos" primero.
3. **Estado con filtro "Cardio":** El botón "Cardio" adopta el relleno activo y el mapa actualiza la visibilidad de los íconos de máquinas, mostrando únicamente los equipos de la categoría seleccionada. La estructura general de la pantalla (título, selector de sede, leyenda, bottom nav) permanece idéntica.
4. **Flujo de web (desktop):** El wireflow web muestra el mismo flujo pero con el mapa en layout de escritorio, donde los íconos de máquinas están más espaciados y etiquetados con el nombre de cada equipo (Cinta 1, Prensa, Polea Alta, etc.).


 8. <strong>Wireflow 8:</strong> Cambio de sucursal para revisión de aforo

- User goal: Como cliente frecuente, quiero seleccionar otras sedes en la app.

<strong>User story asociada:</strong> 
<br> US11: Como cliente frecuente, quiero seleccionar otras sedes en la app, para revisar el croquis y aforo de sucursales alternas antes de salir de casa.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow11.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow11_web.png" alt="wireflow" width="500"/>
  </div> <br>

 
**Descripción de cada paso:**
 
1. **Estado inicial — "Gimnasio Centro":** El wireflow muestra el mapa con el selector en "Gimnasio Centro" como sede predeterminada del usuario. En la versión web de escritorio, el dropdown desplegado muestra las tres opciones disponibles: Gimnasio Centro, Gimnasio Norte, Gimnasio Sur.
2. **Transición → "Gimnasio Norte":** La flecha horizontal del wireflow conecta la vista de Gimnasio Centro con la vista de Gimnasio Norte. La estructura de la pantalla permanece idéntica; únicamente cambia el nombre en el selector y la distribución de máquinas en el mapa.
3. **Transición → "Gimnasio Sur":** Una segunda flecha del wireflow conecta la vista de Gimnasio Norte con la de Gimnasio Sur, representando que el usuario puede navegar entre múltiples sedes de forma consecutiva sin volver a una pantalla de menú.
4. **Consistencia del mapa entre sedes:** Los tres estados del wireflow evidencian que la estructura de la pantalla (título, filtros, contenedor del mapa, leyenda, bottom nav) es idéntica entre sedes, validando el principio de consistencia del Design System.

   9. <strong>Wireflow 9:</strong> Notificaciones push de resolución de disponibilidad

- User goal: Como cliente frecuente, quiero activar una campana de aviso.

<strong>User story asociada:</strong> 
<br> US12: Como cliente frecuente, quiero activar una campana de aviso, para recibir una alerta en mi celular cuando la máquina que esperaba se libere.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow12.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow12_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción de cada paso:**
 
1. **Login a Mapa:** El wireflow replica los dos primeros pasos del flujo de US07/US09, partiendo del formulario vacío, pasando por el estado con credenciales ingresadas, y llegando al Mapa de Disponibilidad mediante la flecha de redirección post-autenticación.
2. **Mapa en estado normal:** El usuario visualiza el mapa con sus 8 máquinas y sus estados de disponibilidad. En este punto, activa la campana de aviso en una máquina que está en estado Ocupado (interacción no representada como pantalla separada en el wireflow al ser un estado transitorio).
3. **Notificación de estado:** La última pantalla del wireflow muestra el Mapa de Disponibilidad con el banner toast en la parte inferior. En el wireflow presentado, el banner muestra el texto "Máquina ocupada nuevamente" con el ícono de cierre, representando el escenario 2 de los criterios de aceptación: el sistema envió la notificación de disponibilidad, pero otro usuario ocupó la máquina antes de que el cliente llegara, por lo que el sistema cancela automáticamente la alerta y notifica el nuevo estado.
4. **Actualización del mapa:** Simultáneamente con el banner, el mapa refleja el cambio de estado de la máquina, manteniendo la coherencia del sistema en todos los canales de feedback.


   10. <strong>Wireflow 10:</strong> Sistema de recompensas de Crowdsourcing

- User goal: Como cliente frecuente, quiero ganar puntos canjeables en mi perfil.

<strong>User story asociada:</strong> 
<br> US13: Como cliente frecuente, quiero ganar puntos canjeables en mi perfil, para motivarme a actualizar manualmente el estado de disponibilidad de los equipos.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow13.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow13_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción de cada paso:**
 
1. **Mapa de Disponibilidad — punto de entrada:** El usuario se encuentra en la pantalla principal del mapa con todas las máquinas visibles. Al tocar cualquier ícono de máquina, el sistema despliega el modal contextual sin cambiar de pantalla, manteniendo el mapa como fondo.
2. **Modal contextual "Polea Alta":** El wireflow muestra el modal emergente superpuesto sobre el mapa. El modal presenta el nombre específico de la máquina seleccionada ("Polea Alta") y su estado actual ("Libre") como información de contexto. Las dos acciones disponibles están jerarquizadas visualmente: "Reservar 15 minutos" adopta el estilo de CTA primario (relleno claro) y "Reportar como Ocupado" el estilo secundario (contorno), comunicando la prioridad de cada acción sin ambigüedad. El botón de cierre × en la esquina superior derecha garantiza que el usuario pueda cancelar sin consecuencias.
3. **Pantalla de confirmación "+25 puntos":** Tras presionar "Reportar como Ocupado", el wireflow muestra la pantalla de confirmación gamificada: el mapa de fondo se oscurece parcialmente con una superposición, y sobre ella aparece una tarjeta centrada con el mensaje "Gracias por tu apoyo" y la recompensa "+25 puntos". Este estado es transitorio: tras unos segundos o al tocar la pantalla, el sistema regresa al mapa actualizado con el nuevo estado de la máquina.
4. **Versión web (desktop):** El wireflow de escritorio replica exactamente el mismo flujo de tres estados, adaptando el modal y la pantalla de confirmación al layout de mayor ancho, donde el mapa ocupa toda la pantalla y el modal aparece centrado con dimensiones proporcionales.

   11. <strong>Wireflow 11:</strong> Motor de sugerencia de rutinas alternativas

- User goal: Como cliente del gimnasio, quiero recibir recomendaciones de ejercicios alternativos.

<strong>User story asociada:</strong> 
<br> US14: Como cliente del gimnasio, quiero recibir recomendaciones de ejercicios alternativos cuando mi máquina esté ocupada, para no perder mi ritmo de entrenamiento.

- mobile

<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow14.png" alt="wireflow" width="500"/>
  </div> <br>

- web 
<div align= "center">
  <align>
    <img src="../assets/wireflow/wireflow14_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción de cada paso:**
 
1. **Mapa de Disponibilidad — punto de entrada:** El wireflow parte de la pantalla principal del mapa. La bottom navigation bar con "Rutinas" como destino es el punto de conexión entre el contexto de disponibilidad y la sección de ejercicios.
2. **Sección "Rutinas y Ejercicios":** Al seleccionar "Rutinas" en la barra de navegación inferior, el wireflow muestra la sección con el buscador global en la parte superior, los filtros de grupo muscular como etiquetas horizontales desplazables y el listado de ejercicios de la rutina del usuario. Cada tarjeta integra la disponibilidad en tiempo real de la máquina asociada mediante un badge de estado, sin necesidad de volver al mapa.
3. **Tarjeta con máquina ocupada — alternativas expandidas:** Cuando una máquina de la rutina está en estado "Ocupado" (ej. "Rack Sentadilla #2"), la tarjeta del ejercicio afectado expande automáticamente la subsección "Alternativas disponibles:" con el listado de equipos sustitutos en estado Libre. El wireflow muestra esta expansión en el mismo nivel de la tarjeta, sin abrir una pantalla nueva. Al final de la subsección, el CTA "Ver en el Mapa" de ancho completo conecta el flujo de rutinas de vuelta al mapa, señalando la ubicación exacta de la alternativa seleccionada.
4. **Drawer "Rutinas alternativas":** El wireflow muestra el panel lateral que se despliega desde el borde derecho de la pantalla al solicitar una búsqueda más amplia de alternativas. El drawer contiene el mismo buscador y sistema de filtros que el listado principal, pero presenta únicamente ejercicios alternativos. Las tarjetas muestran el estado de cada alternativa: "Disponible" para equipos libres y "Mantenimiento" para equipos con ticket técnico abierto, cumpliendo el criterio de aceptación del escenario 2 (exclusión de máquinas averiadas). El botón de cierre × en la esquina superior derecha permite descartar el drawer sin perder el estado del listado principal.
5. **Versión web (desktop):** El wireflow de escritorio muestra las tres vistas simultáneamente: el mapa reducido a la izquierda (para mantener el contexto de disponibilidad), el listado de rutinas en el centro y el drawer de alternativas como panel superpuesto a la derecha. Esta disposición aprovecha el mayor ancho de pantalla del desktop para mantener el contexto del mapa visible durante toda la interacción de búsqueda de alternativas.

### 4.4.2. Web Applications Mock-ups.

1. <strong>Mockup 1:</strong> Selección de planes de suscripción SaaS

<strong>User story asociada:</strong> 
<br> US04: Como administrador, quiero visualizar la comparativa de precios (Basic, Mid, Platinum), para saber qué plan se ajusta a mi negocio.


<div align= "center">
  <align>
    <img src="../assets/mockups/mockup4_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El mock-up de esta historia se ubica en la **Landing Page** (vista web de escritorio) y presenta la sección de **"Planes y Precios"** mediante tres tarjetas de suscripción dispuestas en un layout de tres columnas sobre fondo negro (`#000000`), respetando el grid de 12 columnas definido en las Web Style Guidelines.
 
**Aplicación de principios de diseño:**
 
- **Jerarquía visual:** El plan "Mid" ($109/mes) se posiciona como el más destacado mediante una tarjeta enmarcada con borde dorado (`#f5bc36`) y una etiqueta de "Más Popular" en la parte superior, guiando la atención del usuario hacia la opción recomendada. Esta distinción sigue el principio de énfasis para dirigir la toma de decisión sin abrumar.
- **Contraste y legibilidad:** Los precios se presentan en tipografía primaria Bold de gran tamaño sobre fondo oscuro, garantizando un ratio de contraste elevado y facilitando el escaneo rápido de la información.
- **Consistencia:** Los tres planes comparten la misma estructura interna (nombre del plan, precio mensual, lista de características con íconos de check en verde/teal, y un botón de CTA), aplicando el principio de consistencia del Design System para reducir la carga cognitiva.
- **Diseño inclusivo:** El uso de íconos de verificación junto al texto (no solo color) garantiza que la información sea legible para personas con deficiencias en la percepción del color. Los botones de CTA ("Demo Gratis", "Comenzar Ahora →", "Contactar") presentan etiquetas claras y áreas de toque suficientes.
- **Arquitectura de información:** La sección sigue la jerarquía descendente de la Landing Page: el usuario llega a esta sección después de haber comprendido el producto en el Hero Section y las Features, siguiendo el flujo lógico de decisión de compra.

2. <strong>Mockup 2:</strong> Envío de formulario de Contacto

<strong>User story asociada:</strong> 
<br> US05: Como visitante, quiero poder llenar un formulario con mis datos y mensaje, para solicitar información al equipo de ventas de Spot Track.

<div align= "center">
  <align>
    <img src="../assets/mockups/mockup5_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El mock-up muestra la página de **"Contacto"** en dos estados: el formulario vacío (estado inicial) y el formulario con datos completados por el usuario "Carla Gallardo" (estado de llenado en progreso). Ambos estados se presentan en desktop para ilustrar el flujo completo de interacción.
 
**Aplicación de principios de diseño:**
 
- **Principio de visibilidad del estado del sistema:** Los campos del formulario muestran claramente el estado de foco mediante un borde destacado en color dorado (`#f5bc36`) cuando el usuario está escribiendo en ellos, tal como se aprecia en el campo "Mensaje" del estado activo. Esto confirma al usuario que la interfaz está respondiendo a su interacción.
- **Minimalismo y carga cognitiva reducida:** El formulario se compone únicamente de los campos estrictamente necesarios: Nombre, Email y Mensaje. Esta decisión de diseño, alineada con el principio de simplicidad, reduce la fricción para el usuario y aumenta la probabilidad de completar el formulario.
- **Tipografía secundaria:** Los placeholders ("Tu nombre completo", "tu@email.com", "Cuéntanos sobre tu gimnasio y tus necesidades") utilizan la tipografía secundaria en color gris sutil, cumpliendo una función orientativa sin competir con el contenido ingresado.
- **CTA prominente:** El botón "Enviar" ocupa el ancho completo del contenedor del formulario, con fondo dorado (`#f5bc36`) y texto negro, siguiendo las convenciones de CTA del Design System y maximizando el área de interacción.
- **Arquitectura de información:** La página de Contacto se accede desde el menú de navegación superior fija de la Landing Page, coherente con el sistema de Navegación One-Page Scroll definido. El footer con copyright refuerza la identidad de marca.
- **Diseño inclusivo:** Los campos tienen etiquetas visibles por encima de los inputs (no solo placeholders), asegurando que la etiqueta no desaparezca al comenzar a escribir, lo que favorece la usabilidad para usuarios con dificultades cognitivas o de memoria de corto plazo.

3. <strong>Mockup 3:</strong> Acceso al portal desde la navegación

<strong>User story asociada:</strong> 
<br> US06: Como visitante o cliente potencial, quiero tener botones de Login y Demo a la vista, para ingresar a la plataforma de forma rápida desde la landing page.

<div align= "center">
  <align>
    <img src="../assets/mockups/mockup6_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
Esta historia se refleja de forma transversal en todos los mock-ups de la **Landing Page** a través de la **barra de navegación superior fija (Sticky Top Navbar)**. El mock-up muestra claramente los botones "Iniciar Sesión" (texto plano) y "Demo Gratis" (botón con fondo dorado `#f5bc36`) posicionados en el extremo derecho del navbar, tanto en la vista de escritorio como en la vista compacta.
 
**Aplicación de principios de diseño:**
 
- **Affordance y reconocimiento:** El botón "Demo Gratis" adopta el color de acento primario del Design System (`#f5bc36`) con texto negro de alto contraste, señalando inmediatamente al usuario que es la acción principal y prioritaria. El enlace "Iniciar Sesión" mantiene un estilo secundario, jerarquizando las opciones de acceso.
- **Persistencia de la navegación:** Al ser un navbar sticky, ambos botones permanecen accesibles en todo momento del scroll de la landing page, eliminando la necesidad de que el usuario regrese al inicio para encontrar el acceso. Este comportamiento aplica el principio de eficiencia de uso.
- **Labeling System:** Las etiquetas "Iniciar Sesión" y "Demo Gratis" fueron definidas explícitamente en el Labeling System de la Arquitectura de Información del producto, empleando lenguaje claro y orientado a la acción, libre de tecnicismos.
- **Diseño inclusivo:** El alto contraste del botón dorado sobre el fondo oscuro del navbar asegura visibilidad para usuarios con baja agudeza visual. El tamaño del target del botón cumple con las recomendaciones de al menos 44x44px para interacción táctil.


4. <strong>Mockup 4:</strong> Inicio de sesión con validación JWT

<strong>User story asociada:</strong> 
<br> US07: Como usuario, quiero iniciar sesión de forma segura generando un token, para acceder a mi panel de control o aplicación móvil correspondiente.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup7.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup7_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El mock-up presenta la pantalla de **"Iniciar Sesión"** en tres variantes: el formulario vacío (estado inicial), el formulario con credenciales de cliente ingresadas ("cliente@email.com") y, en la versión web, el panel de navegación demo que permite al evaluador explorar los distintos flujos. Las versiones mobile y web (desktop) del mismo formulario se muestran para evidenciar el diseño responsive.
 
**Aplicación de principios de diseño:**
 
- **Jerarquía visual clara:** El logo de SpotTrack encabeza la pantalla, seguido del título "Iniciar Sesión" en tipografía primaria Bold, la descripción en tipografía secundaria Regular y los campos de formulario. Esta jerarquía guía el ojo del usuario de forma natural desde la identidad de marca hasta la acción requerida.
- **Feedback y estado del sistema:** El campo de contraseña muestra los caracteres enmascarados con puntos, confirmando al usuario que su entrada es segura. El botón "Iniciar Sesión" con fondo dorado es el único CTA de la pantalla, evitando distracciones.
- **Diseño inclusivo y accesibilidad:** Las etiquetas "Email" y "Contraseña" están posicionadas por encima de cada campo (no como placeholders únicos), asegurando su visibilidad permanente. Los placeholders orientativos ("tu@email.com", "········") complementan la etiqueta sin reemplazarla.
- **Onboarding y orientación:** La sección "Demo de prueba" con credenciales precargadas (Admin y Cliente) es un elemento de diseño inclusivo que reduce la barrera de entrada para evaluadores y nuevos usuarios, permitiendo explorar la plataforma sin fricción.
- **Arquitectura de información:** El enlace "¿No tienes cuenta? Regístrate aquí" en color dorado conecta este flujo con el de registro, manteniendo la coherencia del sistema de navegación. Tras un login exitoso, el sistema redirige al usuario a la vista correspondiente según su rol (Dashboard Admin o Mapa de Disponibilidad para el cliente), aplicando la organización por audiencia definida en el Organization System.

  5. <strong>Mockup 5:</strong> Gestión de preferencias y perfil

<strong>User story asociada:</strong> 
<br> US08: Como usuario, quiero actualizar mi información personal y cambiar el idioma del sistema, para mantener mis datos al día y usar la plataforma cómodamente.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup8.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup8_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El mock-up presenta la pantalla **"Mi Perfil"** en la versión mobile, con múltiples estados: vista estándar, estado de guardado exitoso (con notificación en verde "¡Cambios guardados!") y estado con actualización de idioma. La pantalla está organizada en secciones claramente diferenciadas mediante agrupación visual.
 
**Aplicación de principios de diseño:**
 
- **Organización por grupos de información (Gestalt – Proximidad):** La pantalla divide la información del perfil en bloques semánticos bien delimitados: datos del usuario y puntos acumulados, información del plan activo con CTA "Mejorar Plan", Historial de Puntos, Información Personal, Preferencias de Idioma, Notificaciones y Seguridad. Esta segmentación aplica el principio de proximidad de la Gestalt para agrupar información relacionada, reduciendo la carga cognitiva.
- **Jerarquía tipográfica aplicada:** Cada sección lleva un encabezado en tipografía secundaria SemiBold con un ícono contextual (globo para idioma, campana para notificaciones, candado para seguridad), reforzando la semántica visual de cada bloque.
- **Historial de puntos y gamificación:** La sección "Historial de Puntos" muestra entradas con puntos en verde positivo (+25 pts, +15 pts, +20 pts) con descripciones y fechas relativas, aplicando el principio de feedback positivo para motivar la participación del usuario en el sistema de recompensas (relacionado con US13).
- **Feedback del sistema:** El estado de guardado exitoso muestra un banner de notificación en verde brillante con ícono de check, brindando confirmación inmediata de la acción completada. El botón "Guardar Cambios" en color dorado permanece fijo al pie de la pantalla (sticky), manteniéndose siempre accesible.
- **Diseño inclusivo:** El selector de idioma ("Español" / "Inglés") se presenta como un dropdown con bandera e indicación textual del idioma activo, no solo con código de idioma, facilitando la comprensión para usuarios con menor alfabetización digital. Las notificaciones son configurables (toggle) con descripciones explicativas del tipo de alerta que recibirá el usuario.
- **Arquitectura de información – Navigation Systems:** La pantalla "Mi Perfil" es accesible desde el ícono de perfil en la bottom navigation bar, siguiendo la convención de la aplicación móvil. El botón de retroceso (Mi Perfil) en la parte superior cumple con el estándar de navegación móvil.
- **Información del plan:** Se muestra el plan activo (Basic, $69/mes), la próxima fecha de renovación y las características incluidas, con un CTA "Mejorar Plan" que conecta al flujo de US04. Esta integración de información en el perfil reduce la necesidad de que el usuario navegue a otra sección para conocer su estado de suscripción.

 6. <strong>Mockup 6:</strong> Visualización del mapa de calor en VIVO

<strong>User story asociada:</strong> 
<br> US09: Como cliente frecuente, quiero ver la disponibilidad de las máquinas en tiempo real (verde/rojo), para esquivar aglomeraciones y no perder tiempo en filas.

<- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup9.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup9_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El mock-up muestra la pantalla principal de la **aplicación móvil** y su equivalente web (desktop), presentando el **"Mapa de Disponibilidad en Tiempo Real"**. El mapa central despliega los íconos de cada máquina en una cuadrícula semiespacial dentro de un contenedor oscuro (#1a1a1a), con tres estados visuales diferenciados: verde (Libre), rojo (Ocupado) y dorado/amarillo (Reservado), con contador de tiempo regresivo visible.
 
**Aplicación de principios de diseño:**
 
- **Principio de señalética semafórica (diseño inclusivo):** El sistema de tres colores (verde/rojo/dorado) sigue la convención universal del semáforo, permitiendo una interpretación inmediata del estado de cada máquina sin necesidad de leer texto adicional. Adicionalmente, cada ícono de máquina incluye un glifo de pesas que actúa como indicador redundante de tipo de equipo, reforzando la comprensión para usuarios daltónicos.
- **Jerarquía visual de la App Móvil:** Siguiendo el Organization System definido para la Web App B2C, el mapa de disponibilidad ocupa la posición central y absoluta de la pantalla, subordinando todas las demás funciones a la barra de navegación inferior. Esto refleja la prioridad de acceso inmediato a la disponibilidad como necesidad primaria del usuario.
- **Leyenda visual:** En la parte inferior del mapa se incluye una leyenda compacta con los tres estados y el conteo actual de máquinas en cada estado (Libre 4, Ocupado 3, Reservado 1), reforzando la comprensión del estado global del gimnasio de un vistazo.
- **Bottom Navigation Bar:** La barra inferior presenta cuatro destinos (Mapa, Reservas, Rutinas, Perfil) con íconos y etiquetas textuales, cumpliendo con las directrices de accesibilidad de navegación móvil y facilitando el uso con una sola mano.
- **Feedback en tiempo real:** El contador regresivo "09:59" sobre el ícono de la máquina en estado Reservado comunica al usuario cuánto tiempo resta para que ese equipo quede disponible, gestionando las expectativas sin necesidad de interacción adicional.
- **Selector de sede y filtros:** El dropdown "Gimnasio Centro" en la parte superior y los filtros de categoría (Todos / Fuerza / Cardio) completan la arquitectura de navegación facetada definida en el Searching System, siendo el punto de entrada a las historias US10 y US11.

 7. <strong>Mockup 7:</strong> Filtrado del inventario por tipo de máquina

<strong>User story asociada:</strong> 
<br> US10: Como cliente frecuente, quiero seleccionar etiquetas (ej. Fuerza o Cardio) en el mapa, para visualizar únicamente las máquinas relevantes para mi rutina.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup10.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup10_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El mock-up muestra el mapa de disponibilidad con el sistema de filtros activado, presentando en paralelo el estado con filtro "Fuerza" activo y el filtro "Cardio" activo. El botón del filtro seleccionado se resalta con fondo dorado (`#f5bc36`) y texto negro, mientras los demás botones mantienen el estilo de contorno.
 
**Aplicación de principios de diseño:**
 
- **Estado activo claramente comunicado:** El cambio visual del botón de filtro activo (fondo dorado sólido vs. contorno sutil) aplica el principio de visibilidad del estado del sistema de Nielsen, confirmando inmediatamente qué categoría está siendo visualizada. No se depende únicamente del color: la tipografía Bold del botón activo refuerza la distinción.
- **Filtrado facetado (Searching System):** La implementación de las etiquetas "Todos", "Fuerza" y "Cardio" corresponde exactamente al sistema de filtros por categoría definido en la Arquitectura de Información, permitiendo al usuario acotar el inventario de máquinas a los equipos relevantes para su sesión de entrenamiento.
- **Consistencia del mapa:** Al aplicar el filtro, el layout de íconos dentro del mapa mantiene su distribución espacial pero cambia la visibilidad de los equipos no correspondientes, sin modificar la estructura de la pantalla. Esto respeta el principio de consistencia y evita la desorientación del usuario.
- **Botón "Limpiar":** Se incluye un botón "Limpiar" junto a los filtros para restablecer la vista completa del inventario, tal como exige el escenario 2 de los criterios de aceptación (limpieza de filtros). Su posición es consistente con el grupo de filtros.
- **Diseño inclusivo:** Las etiquetas de los filtros emplean lenguaje directo del Labeling System ("Fuerza", "Cardio") en lugar de tecnicismos, reduciendo la carga cognitiva del usuario en contexto de uso en movimiento.

 8. <strong>Mockup 8:</strong> Cambio de sucursal para revisión de aforo

<strong>User story asociada:</strong> 
<br> US11: Como cliente frecuente, quiero seleccionar otras sedes en la app, para revisar el croquis y aforo de sucursales alternas antes de salir de casa.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup11.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup11_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El mock-up muestra el flujo de cambio de sede a través de dos estados: la vista con "Gimnasio Centro" seleccionado y la misma pantalla tras seleccionar "Gimnasio Norte" desde el dropdown. También se presenta la vista de escritorio con el menú desplegado mostrando múltiples opciones de sede (Gimnasio Centro, Gimnasio Norte, Gimnasio Sur).
 
**Aplicación de principios de diseño:**
 
- **Control del usuario (principio de Nielsen):** El selector de sede mediante dropdown en la esquina superior derecha otorga al usuario pleno control para cambiar el contexto de visualización sin salir de la pantalla principal. El ícono de pin de ubicación junto al nombre de la sede refuerza semánticamente la función del control.
- **Retroalimentación inmediata:** Al cambiar la sede, el mapa se actualiza inmediatamente con el inventario y estados de la nueva sucursal, sin necesidad de recargar la página. El nombre de la sede en el dropdown refleja la selección activa en todo momento.
- **Arquitectura de información – Organization System:** El selector de sucursal corresponde al filtro por Sede definido en el Searching System del Dashboard Administrativo, trasladado al contexto de la aplicación cliente. La organización de datos por ubicación (sede) sigue el modelo de categorización por tópicos de la Plataforma Móvil.
- **Diseño inclusivo – Plan y acceso:** El mock-up evidencia que el flujo de cambio de sede está disponible para usuarios con el plan correspondiente. El sistema contempla el escenario de sede fuera del plan, donde debe bloquearse el acceso y sugerir la mejora de membresía (visible en el criterio de aceptación US11, escenario 2).
- **Consistencia visual entre sedes:** Los mapas de "Gimnasio Centro" y "Gimnasio Norte" mantienen exactamente la misma estructura de pantalla, paleta de colores y componentes, asegurando que el usuario no deba reaprender la interfaz al cambiar de contexto.

   9. <strong>Mockup 9:</strong> Notificaciones push de resolución de disponibilidad

<strong>User story asociada:</strong> 
<br> US12: Como cliente frecuente, quiero activar una campana de aviso, para recibir una alerta en mi celular cuando la máquina que esperaba se libere.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup12.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup12_web.png" alt="wireflow" width="500"/>
  </div> <br>

  **Descripción del mock-up:**
 
El mock-up presenta dos estados clave del flujo: el mapa de disponibilidad en estado normal y el estado posterior a la liberación de una máquina, donde aparece un **banner de notificación push** en la parte inferior de la pantalla con el mensaje "✓ Un cliente se ha retirado de la Prensa" sobre fondo verde brillante.
 
**Aplicación de principios de diseño:**
 
- **Feedback del sistema (principio central de Nielsen):** El banner de notificación en verde brillante con ícono de check es el mecanismo de feedback principal de esta historia. Su posición en la parte inferior de la pantalla (toast notification) sigue las convenciones de Material Design para notificaciones no bloqueantes, permitiendo al usuario ver simultáneamente el mapa actualizado sin interrumpir su experiencia.
- **Semántica del color:** El verde del banner de notificación es consistente con el color del estado "Libre" en el mapa de disponibilidad, reforzando la asociación semántica: verde = disponible = acción positiva. Esta consistencia cromática reduce el tiempo de interpretación del mensaje.
- **Lenguaje orientado al usuario:** El mensaje "Un cliente se ha retirado de la Prensa" emplea el Labeling System del producto (nombre real de la máquina) y un lenguaje natural y directo, evitando códigos técnicos de máquina o mensajes genéricos como "Estado actualizado".
- **Diseño inclusivo:** La notificación combina texto descriptivo e ícono de check, no dependiendo exclusivamente del color para comunicar el mensaje. Esto garantiza comprensión para usuarios con daltonismo o baja visión.
- **Actualización del mapa en tiempo real:** El mock-up muestra cómo la máquina liberada actualiza su ícono a verde en el mapa simultáneamente con la aparición del banner, evidenciando la coherencia del estado del sistema en todos sus canales de feedback a la vez.


   10. <strong>Mockup 10:</strong> Sistema de recompensas de Crowdsourcing

<strong>User story asociada:</strong> 
<br> US13: Como cliente frecuente, quiero ganar puntos canjeables en mi perfil, para motivarme a actualizar manualmente el estado de disponibilidad de los equipos.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup13.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup13_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El mock-up muestra dos interacciones clave: el modal emergente al tocar una máquina libre ("Polea Alta – Estado: Libre") con las opciones "Reservar 15 minutos" y "Reportar como Ocupado", y la pantalla de confirmación posterior al reporte con el mensaje "Gracias por tu apoyo +25 puntos" sobre una superposición oscura del mapa.
 
**Aplicación de principios de diseño:**
 
- **Diseño de interacción contextual:** Al tocar cualquier máquina en el mapa, se despliega un modal con acciones relevantes para ese equipo específico (nombre, estado actual y CTAs). Este patrón de interacción contextual reduce la distancia entre el descubrimiento de la disponibilidad y la acción, siguiendo el principio de eficiencia de uso.
- **Jerarquía de acciones:** En el modal, la acción primaria "Reservar 15 minutos" se presenta con el estilo de CTA dorado, mientras que "Reportar como Ocupado" adopta un estilo secundario oscuro. La jerarquía visual de botones comunica la importancia relativa de cada acción sin ambigüedad.
- **Gamificación y motivación intrínseca:** La pantalla de confirmación "+25 puntos" es un elemento de diseño motivacional que cierra el ciclo de acción del usuario con una recompensa inmediata y visible. El diseño minimalista de esta pantalla (solo el mensaje sobre el mapa difuminado) maximiza el impacto emocional del feedback positivo.
- **Conexión con el perfil (US08):** Los puntos ganados en este flujo se reflejan en la sección "Historial de Puntos" del perfil del usuario, cerrando el loop de la mecánica de gamificación en la arquitectura de la aplicación.
- **Diseño inclusivo:** El modal incluye un botón de cierre (×) claramente posicionado, garantizando que el usuario pueda descartar la acción sin consecuencias involuntarias. Las áreas de toque de ambos botones cumplen con el tamaño mínimo recomendado para dispositivos móviles.

   11. <strong>Mockup 11:</strong> Motor de sugerencia de rutinas alternativas

<strong>User story asociada:</strong> 
<br> US14: Como cliente del gimnasio, quiero recibir recomendaciones de ejercicios alternativos cuando mi máquina esté ocupada, para no perder mi ritmo de entrenamiento.

- mobile: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup14.png" alt="wireflow" width="500"/>
  </div> <br>

- web: 
<div align= "center">
  <align>
    <img src="../assets/mockups/mockup14_web.png" alt="wireflow" width="500"/>
  </div> <br>

**Descripción del mock-up:**
 
El mock-up presenta la sección **"Rutinas y Ejercicios"** con tres vistas en progresión: el mapa de disponibilidad (contexto del flujo), la lista de ejercicios con su disponibilidad actual y el panel de "Rutinas alternativas" desplegado como drawer lateral. Cada tarjeta de ejercicio muestra el nombre, la máquina asociada, las etiquetas de grupo muscular, el nivel de dificultad y el estado de disponibilidad (verde "Disponible" / rojo "Ocupado").
 
**Aplicación de principios de diseño:**
 
- **Visibilidad del estado del sistema:** El uso de tarjetas de métricas con indicadores de tendencia (flechas verdes/rojas) permite al usuario entender el rendimiento actual respecto al mes anterior de un solo vistazo.

- **Arquitectura de información:** Los datos están agrupados de lo general a lo específico. Primero las métricas globales, luego la distribución visual (gráficos) y finalmente el detalle tabular con impacto financiero.

- **Contraste semántico:** En la tabla de inactividad, se utilizan etiquetas de color (Rojo - Alto, Amarillo - Medio, Verde - Bajo) para categorizar el impacto, facilitando la toma de decisiones basada en la urgencia económica.

![MOCKUP-US16](../assets/mockups/US16%20Sistema%20de%20reserva%20exprés%20en%20horas%20pico%20(Epic_%20EP04).png)


<strong>User story asociada:</strong> 
<br> US17: Como administrador, quiero ver gráficos con la sumatoria de minutos reales de uso de cada máquina, para comprender la demanda real sin tener que vigilar el local.

![MOCKUP-US17](../assets/MOCKUPS/US17%20Acumulación%20automática%20de%20horas%20de%20uso.png)

**Descripción del mock-up:**
Este mock-up presenta el módulo de **Reportes y Analíticas**. En la parte superior se muestran KPIs clave (Horas totales, Tasa de ocupación, Picos y Tiempo inactivo). Incluye un gráfico de barras para la comparativa semanal y una "Tabla de Inactividad e Impacto Operativo" que traduce el tiempo muerto de las máquinas en pérdida monetaria ($), permitiendo al administrador ver el costo de oportunidad. 

**Aplicación de principios de diseño:**
 
- **Visibilidad del estado del sistema:** El uso de tarjetas de métricas con indicadores de tendencia (flechas verdes/rojas) permite al usuario entender el rendimiento actual respecto al mes anterior de un solo vistazo.
- **Arquitectura de información:** Los datos están agrupados de lo general a lo específico. Primero las métricas globales, luego la distribución visual (gráficos) y finalmente el detalle tabular con impacto financiero.
- **Contraste semántico:** En la tabla de inactividad, se utilizan etiquetas de color (Rojo - Alto, Amarillo - Medio, Verde - Bajo) para categorizar el impacto, facilitando la toma de decisiones basada en la urgencia económica.

<strong>User story asociada:</strong> 
<br> US18: Como administrador, quiero que el sistema resalte en una tabla qué máquinas tienen una tasa de uso excepcionalmente baja, para evaluar su reubicación o descarte.

![MOCKUP-US18](../assets/MOCKUPS/US18%20Identificación%20de%20equipos%20subutilizados%20.png)

**Descripción del mock-up:**
La interfaz se centra en el "Reporte de Ineficiencia Operativa". Presenta una lista de equipos filtrados automáticamente por el motor de análisis que operan por debajo del 60% (parámetro base). Cada fila incluye una barra de progreso visual de la "Tasa de Uso" y una sección de "Recomendaciones del Sistema" que sugiere acciones como reubicación o promociones selectivas.

**Aplicación de principios de diseño:**
 
- **Prevención de errores y ayuda:** La sección de "Recomendaciones del Sistema" actúa como una guía proactiva, transformando datos brutos en insights accionables para el gerente.
- **Reconocimiento antes que recuerdo:** El uso de barras de progreso horizontales dentro de la tabla permite comparar visualmente el rendimiento de las máquinas sin tener que leer y procesar cada número individualmente.
- **Consistencia funcional:** El botón de "Exportar CSV" mantiene la ubicación y estilo de otros reportes, asegurando que el usuario sepa siempre cómo llevarse la data a herramientas externas como Excel.

<strong>User story asociada:</strong> 
<br> US19: Como dueño del negocio, quiero ver gráficos que destaquen las horas donde el aforo de máquinas supera el 90%, para identificar cuellos de botella diarios.

![MOCKUP-US19](../assets/MOCKUPS/US19%20Visualización%20de%20picos%20de%20estrés%20del%20local.png)

**Descripción del mock-up:**
Este mock-up destaca el gráfico de "Picos de Estrés por Hora", donde se visualiza el aforo del local a lo largo del día. El gráfico de líneas permite identificar rápidamente los intervalos de tiempo que superan el umbral crítico (> 90%). Además, cuenta con un selector de "Rango Personalizado" para el análisis de periodos específicos.

**Aplicación de principios de diseño:**
 
- **Jerarquía visual (Énfasis):** El gráfico de líneas utiliza puntos de datos destacados para marcar los momentos de máxima saturación, permitiendo que el dueño identifique "cuellos de botella" en segundos.
- **Diseño centrado en el usuario:** El tooltip interactivo en el gráfico de barras (comparando "Semana Actual" vs "Capacidad") proporciona precisión de datos "on-demand", evitando saturar la pantalla con números permanentes.
- **Minimalismo (Ley de Hick):** A pesar de manejar gran cantidad de datos de sensores IoT, la interfaz se mantiene limpia utilizando un fondo negro puro y acentos en amarillo (#f5bc36) para no distraer al usuario de la información crítica: la saturación del local.

![MOCKUP-US20](../assets/mockups/US20%20Exportación%20de%20analíticas%20de%20uso%20(Epic_%20EP05).png)
![MOCKUP-US21](../assets/mockups/US21%20Monitoreo%20de%20estado%20de%20hardware%20Edge%20IoT%20(Epic_%20EP05).png)
![MOCKUP-US22-UMBRAL](../assets/mockups/US22%20Alerta%20predictiva%20de%20mantenimiento%20(Epic_%20EP06)%20CONFIGURAR%20UMBRAL.png)
![MOCKUP-US22](../assets/mockups/US22%20Alerta%20predictiva%20de%20mantenimiento%20(Epic_%20EP06).png)
![MOCKUP-US23](../assets/mockups/US23%20Despacho%20automatizado%20de%20tickets%20técnicos%20(Epic_%20EP06).png)
![MOCKUP-US24](../assets/mockups/US24%20Notificación%20de%20restablecimiento%20a%20los%20usuarios%20(Epic_%20EP06).png)
![MOCKUP-US25](../assets/mockups/US25%20Calendario%20inteligente%20de%20bloqueos%20de%20reserva(Epic_%20EP04).png)
![MOCKUP-US26](../assets/mockups/US26%20Gestión%20de%20activos%20físicos%20y%20altas%20(Epic_%20EP07).png)
![MOCKUP-US27](../assets/mockups/US27%20Estadísticas%20de%20reubicación%20multisede%20(Epic_%20EP07).png)
![MOCKUP-US29](../assets/mockups/US29%20Calculadora%20de%20impacto%20financiero%20por%20inactividad%20(Epic_%20EP08).png)
![MOCKUP-US28](../assets/mockups/US28%20Gestión%20automatizada%20de%20stock%20de%20repuestos%20(Epic_%20EP07).png).png)
![MOCKUP-US30](../assets/mockups/US30%20Analítica%20predictiva%20de%20compras%20e%20inversión%20(Epic_%20EP08).png)

### 4.4.3. Web Applications User Flow Diagrams.

---
## US04: Selección de planes de suscripción SaaS

<div align= "center">
  <align>
    <img src="../assets/user flow/userflow4_web.png" alt="userflow" width="500"/>
  </div> <br>

  * **Happy Path:** El visitante hace clic en Pricing en la barra de navegación. El sistema despliega correctamente la grilla comparativa con los tres niveles de suscripción (Basic $69, Mid $109, Platinum $189), mostrando características y costos mensuales claramente diferenciados para cada plan.
  * **Unhappy Path:** El visitante desea acceder al pago de la pagina, pero al no rellenar los campos necesarios, el programa muestra un error de campos vacios.

---
## US05: Envío de formulario de Contacto

<div align= "center">
  <align>
    <img src="../assets/user flow/userflow5_web.png" alt="userflow" width="500"/>
  </div> <br>

  * **Happy Path:** El visitante completa todos los campos obligatorios incluyendo un email con formato válido y presiona Enviar. El sistema pasa la validación sin bloqueos y completa el flujo exitosamente.
  * **Unhappy Path:** Si el visitante intenta presionar Enviar dejando el campo Email vacío, el sistema impide el envío, resalta el campo con un indicador de error y exige completar la información requerida antes de continuar. No se realiza ninguna llamada al servidor.
---
## US06: Acceso al portal desde la navegación

<div align= "center">
  <align>
    <img src="../assets/user flow/userflow6_web.png" alt="userflow" width="500"/>
  </div> <br>

* **Happy Path:** El cliente hace clic en el enlace Iniciar Sesión ubicado en la esquina superior derecha del menú. El sistema redirige al usuario al módulo de autenticación de SpotTrack, donde puede ingresar sus credenciales para acceder al dashboard o al mapa de disponibilidad según su rol.

* **Unhappy Path:** Si el visitante intenta presionar Enviar dejando el campo Email vacío, el sistema muestra el mensaje de campos vacios, resalta el campo con un indicador de error y exige completar la información requerida antes de continuar. 
---
## US07: Inicio de sesión con validación JWT

![UF-07](../assets/USERFLOWS/US07%20Inicio%20de%20sesión%20con%20validación%20JWT%20(Epic_%20EP02).png)
![UFM-07](../assets/USERFLOW%20MOBILE/US07%20Inicio%20de%20sesión%20con%20validación%20JWT%20(Epic_%20EP02).png)

* **Happy Path:** El usuario se autentica ingresando credenciales válidas. El sistema verifica el token JWT y evalúa el rol de la cuenta. Los administradores son redirigidos directamente al dashboard analítico, mientras que los clientes acceden al mapa de disponibilidad en tiempo real.
* **Unhappy Path:** Si las credenciales son incorrectas, la interfaz despliega una alerta visual de error. Si se intenta procesar el formulario con campos vacíos, el frontend bloquea la petición y exige completar la información requerida.

---

## US08: Gestión de preferencias y perfil

![UF-08](../assets/USERFLOWS/US08%20Gestión%20de%20preferencias%20y%20perfil%20(Epic_%20EP02).png)
![UFM-08](../assets/USERFLOW%20MOBILE/US08%20Gestión%20de%20preferencias%20y%20perfil%20(Epic_%20EP02).png)

* **Happy Path:** Mediante el menú lateral, el usuario accede a "Mi Perfil" para consultar su plan actual, métricas y puntos acumulados. Puede actualizar configuraciones como el idioma de la interfaz. Al guardar, la plataforma registra y aplica los cambios instantáneamente.
* **Unhappy Path:** Ante un fallo de red o un error de validación en el backend durante el guardado, los cambios se descartan de forma segura. La UI mantiene el estado previo de la configuración y notifica al usuario sobre el fallo.

---

## US09 y US10: Mapa de calor y filtros de equipamiento

![UF-09-10](../assets/USERFLOWS/US09%20Y%20US10_%20MAPA%20DE%20CALOR%20Y%20FILTROS.png)
![UFM-09-10](../assets/USERFLOW%20MOBILE/US09%20Y%20US10_%20MAPA%20DE%20CALOR%20Y%20FILTROS.png)

* **Happy Path:** Dentro del mapa de disponibilidad, el usuario interactúa con los chips de filtrado. Al seleccionar "Fuerza", el renderizado aísla y muestra únicamente ese tipo de equipamiento. Alternar a "Cardio" refresca la vista instantáneamente con la nueva categoría.
* **Unhappy Path:** Si la combinación de filtros aplicada no arroja resultados (ej. todas las máquinas de la categoría están en mantenimiento o no existen en la sede actual), la interfaz maneja la excepción mostrando un *empty state* limpio.

---

## US11: Cambio de sucursal para revisión de aforo

![UF-11](../assets/USERFLOWS/US11%20Cambio%20de%20sucursal%20para%20revisión%20de%20aforo%20(Epic_%20EP03).png)
![UFM-11](../assets/USERFLOW%20MOBILE/US11%20Cambio%20de%20sucursal%20para%20revisión%20de%20aforo%20(Epic_%20EP03).png)

* **Happy Path:** El usuario despliega el selector de sucursales y elige una ubicación distinta (ej. "Gimnasio Norte"). El sistema valida la jerarquía de su membresía y, al confirmar acceso multisede, carga el mapa de disponibilidad de la nueva ubicación.
* **Unhappy Path:** Si un usuario con plan "Basic" intenta acceder a la telemetría de una sede no incluida en su paquete, el sistema interrumpe la navegación y levanta un modal de "Sede Premium", funcionando como un punto de upsell para mejorar la membresía.

---

## US12: Notificaciones push de resolución de disponibilidad

![UF-12](../assets/USERFLOWS/US12%20Notificaciones%20push%20de%20resolución%20de%20disponibilidad%20(Epic_%20EP03).png)

![UFM-12](../assets/USERFLOW%20MOBILE/US12%20Notificaciones%20push%20de%20resolución%20de%20disponibilidad%20(Epic_%20EP03).png)

* **Happy Path:** El usuario visualiza una máquina en estado ocupado (rojo) y suscribe una alerta de disponibilidad. Cuando el hardware IoT detecta que el equipo ha sido liberado, el sistema despacha una notificación push al dispositivo y el nodo en el mapa pasa a verde.
* **Unhappy Path:** Si la máquina continúa ocupada prolongadamente o es reclamada de inmediato por un usuario con mayor prioridad en la cola, el estado visual se mantiene en rojo y la notificación queda en espera o se informa de un cambio de estado a mantenimiento.

---

## US13: Reporte de máquina

![UF-13](../assets/USERFLOWS/US13_%20Reporte%20de%20máquina.png)
![UFM-13](../assets/USERFLOW%20MOBILE/US13_%20Reporte%20de%20máquina.png)

* **Happy Path:** El usuario levanta un ticket reportando un fallo en un equipo específico. El sistema procesa el reporte, valida su legitimidad cruzando la telemetría, confirma la recepción y recompensa al usuario sumando +25 puntos a su perfil.
* **Unhappy Path:** Si el algoritmo de seguridad detecta un comportamiento anómalo (spam de reportes o falsos positivos recurrentes), la solicitud es rechazada. El sistema aplica una penalización automática, bloqueando la capacidad del usuario para emitir nuevos reportes durante 48 horas.

---

## US14: Motor de sugerencia de rutinas alternativas

![UF-14](../assets/USERFLOWS/US14%20Motor%20de%20sugerencia%20de%20rutinas%20alternativas%20(Epic_%20EP04).png)
![UFM-14](../assets/USERFLOW%20MOBILE/US14%20Motor%20de%20sugerencia%20de%20rutinas%20alternativas%20(Epic_%20EP04).png)

* **Happy Path:** Al encontrarse con una máquina inhabilitada u ocupada dentro de su rutina programada, el usuario solicita alternativas. El motor de recomendación mapea el grupo muscular y devuelve una lista de ejercicios biomecánicamente equivalentes (ej. sustituir press de banca por flexiones) utilizando el equipo disponible.
* **Unhappy Path:** Si la base de datos no logra resolver una equivalencia factible para ese ejercicio dadas las restricciones actuales del entorno, la UI presenta un *empty state* comunicando que temporalmente no hay rutinas alternativas disponibles.

## US16: Sistema de reserva exprés en horas pico

![UF-14](../assets/USERFLOWS/us16diagram.png){ width=90%}

* **User Goal:** Como cliente frecuente, quiero separar virtualmente una máquina libre por 10 minutos durante horas pico, para asegurar su uso mientras me dirijo a ella.
* **Happy Path:** El cliente accede al Mapa de Disponibilidad y selecciona una máquina en estado verde. Al presionar Separar, el sistema bloquea el equipo, cambia su icono a amarillo y activa el cronómetro de 10 minutos en la pestaña Mis Reservas. Al llegar a la ubicación física y validar su identidad antes de que el tiempo se agote, el sistema vincula automáticamente la sesión, cambia el estado a rojo (ocupado) y finaliza la reserva virtual para dar inicio al cobro o uso regular.
* **Unhappy Path:** El cliente genera una reserva virtual, lo que provoca que la máquina pase a estado amarillo y quede restringida para otros usuarios. Sin embargo, el contador de 10 minutos llega a cero sin que el sistema detecte una activación física o inicio de sesión en el equipo. Ante esto, la plataforma ejecuta un reinicio automático de estado: la reserva desaparece del panel del cliente, se emite una notificación de "Reserva Expirada" y la máquina regresa instantáneamente al color verde en el mapa general para estar disponible nuevamente.

## US17: Acumulación automática de horas de uso (EP08)
![UF-17](../assets/USERFLOWS/US17_%20Acumulación%20automática%20de%20horas%20de%20uso%20(EP08).png){ width=90%}

* **User Goal:** Como administrador, quiero ver gráficos con la sumatoria de horas reales de uso de las máquinas, para comprender la demanda real sin tener que vigilar el local.
* **Happy Path:** El administrador ingresa a Reportes y visualiza los gráficos de uso generados por los sensores IoT. Al revisar el tiempo inactivo, el sistema calcula y detalla automáticamente la pérdida monetaria por cada máquina. Finalmente, al aplicar un filtro de fechas, la plataforma recalcula y actualiza toda la información al instante.
* **Unhappy Path:** El administrador ingresa a Reportes, pero el backend no logra comunicarse con los sensores IoT. El sistema no se cae, sino que muestra un estado de alerta ("Sin conexión con los equipos") y los gráficos aparecen en cero o con el último dato en caché.


## US18: Identificación de equipos subutilizados (EP05)

![UF-18](../assets/USERFLOWS/US18_%20Identificación%20de%20equipos%20subutilizados%20(EP05).png){ width=90% }


* **User Goal:** Como administrador, quiero que el sistema resalte en una tabla qué máquinas tienen una tasa de uso excepcionalmente baja, para evaluar su reubicación o descarte.
* **Happy Path:** El administrador ingresa a la sección de Reportes para evaluar la ineficiencia operativa de la sede. El sistema procesa las estadísticas de ocupación recopiladas por los sensores y resalta automáticamente en una tabla aquellas máquinas cuya tasa de uso es inferior al parámetro base. Finalmente, el administrador hace clic en "Exportar CSV" y la plataforma descarga exitosamente un archivo con la data detallada para su análisis externo.
* **Unhappy Path:** El administrador visualiza correctamente la tabla consolidada de equipos subutilizados y procede a hacer clic en "Exportar CSV". Debido a un error de conexión con el servidor, la generación del documento falla y el sistema despliega una notificación de error advirtiendo que no es posible descargar el archivo.


## US19: Visualización de picos de estrés del local (EP05) 

![UF-19](../assets/USERFLOWS/US19_%20Visualización%20de%20picos%20de%20estrés%20del%20local%20(EP05)%20(1).png){ width=90% }
* **User Goal:** Como administrador, quiero que el sistema resalte en una tabla qué máquinas tienen una tasa de uso excepcionalmente baja, para evaluar su reubicación o descarte.
* **Happy Path:** El administrador accede al módulo de Reportes en SpotTrack, donde el sistema genera automáticamente un gráfico de picos de estrés resaltando en rojo las horas con aforo superior al 90%. Al activar la comparativa intersemanal, la interfaz superpone dos líneas de tendencia, permitiendo al dueño del negocio identificar cuellos de botella diarios y comparar el comportamiento de la demanda entre distintos periodos de forma inmediata.
* **Unhappy Path:** Debido a un error de red, el sistema no puede procesar el porcentaje de uso. En lugar del gráfico de estrés, se muestra un estado de carga infinito o un aviso de "Error al cargar analíticas de aforo", sugiriendo reintentar la consulta.


## US20 Exportación de analíticas de uso (Epic: EP05)

![UF-20](../assets/USERFLOWS/US20%20Exportación%20de%20analíticas%20de%20uso%20(Epic_%20EP05).png){ width=90% }
![UFM-20](../assets/USERFLOW%20MOBILE/US20%20Exportación%20de%20analíticas%20de%20uso%20(Epic_%20EP05).png){ width=50% }

* **User Goal**: Como gerente de operaciones, quiero generar documentos formateados en PDF de los gráficos de uso, para presentar reportes formales de rendimiento.
  

* **Happy Path:** El usuario accede a la sección de Reportes y Analíticas, selecciona el período y las sedes deseadas, y genera el reporte en formato CSV o PDF. El sistema procesa la solicitud y muestra una confirmación de "PDF generado correctamente" junto con la opción de descarga inmediata del archivo.
* **Unhappy Path:** Si no existen datos registrados para el período o la sede seleccionada, o si ocurre un fallo durante la generación del archivo, el sistema no puede completar la exportación y muestra un mensaje de error indicando la imposibilidad de generar el reporte, sin ofrecer archivo de descarga.


## US21 Monitoreo de estado de hardware Edge IoT (Epic_ EP05)

![UF-21](../assets/USERFLOWS/US21%20Monitoreo%20de%20estado%20de%20hardware%20Edge%20IoT%20(Epic_%20EP05).png){ width=90% }
![UFM-21](../assets/USERFLOW%20MOBILE/US21%20Monitoreo%20de%20estado%20de%20hardware%20Edge%20IoT%20(Epic_%20EP05).png){ width=50% }

* **User Goal:** Como administrador, quiero revisar la salud de la red y el estado de los nodos IoT, para detectar si un sensor se ha desconectado.
* **Happy Path:** El sistema detecta automáticamente la reconexión de un sensor IoT previamente desconectado y notifica al administrador mediante un mensaje de éxito con opción de descarga de reporte.
* **Unhappy Path:** Si el sensor permanece desconectado tras el intento de sincronización, la interfaz alerta al administrador sobre la falla crítica de conexión, manteniendo el estado de "Desconectado" en el reporte de alertas.

## US22 Alerta predictiva de mantenimiento (Epic_ EP06) CONFIGURAR UMBRAL


![UF-22](../assets/USERFLOWS/US22%20Alerta%20predictiva%20de%20mantenimiento%20(Epic_%20EP06)%20CONFIGURAR%20UMBRAL.png){ width=90% }
![UFM-22](../assets/USERFLOW%20MOBILE/US22%20Alerta%20predictiva%20de%20mantenimiento%20(Epic_%20EP06)%20CONFIGURAR%20UMBRAL.png){ width=50% }

* **User Goal:**
* **Happy Path:** El administrador ajusta los parámetros de los umbrales (batería, tiempos de inactividad, horas críticas) en el panel de configuración, y el sistema guarda los cambios aplicando las nuevas reglas a los modelos predictivos.
* **Unhappy Path:** Ante valores de configuración fuera de los rangos técnicos permitidos (ej. un intervalo de ping inexistente), el sistema bloquea la acción de guardado y requiere el ajuste de los parámetros.

## US23 Despacho automatizado de tickets técnicos (Epic_ EP06)

![UF-23](../assets/USERFLOWS/US23%20Despacho%20automatizado%20de%20tickets%20técnicos%20(Epic_%20EP06).png){ width=90% }
![UFM-23](../assets/USERFLOW%20MOBILE/US23%20Despacho%20automatizado%20de%20tickets%20técnicos%20(Epic_%20EP06).png){ width=50% }

* **User Goal:**
* **Happy Path:** El usuario técnico crea un ticket completando todos los campos requeridos (ID máquina, descripción, prioridad), y el sistema lo integra en el tablero de mantenimiento en tiempo real.
* **Unhappy Path (Missing fields):** Si el formulario se envía sin descripción o prioridad, la UI invalida la creación del ticket y solicita completar la información obligatoria.
* **Unhappy Path (Incorrect data):** Al ingresar datos técnicos inconsistentes o IDs de máquinas inexistentes, el sistema muestra un error de validación impidiendo el despacho del ticket.

## US24 Notificación de restablecimiento a los usuarios (Epic_ EP06)

![UF-24](../assets/USERFLOWS/US24%20Notificación%20de%20restablecimiento%20a%20los%20usuarios%20(Epic_%20EP06).png){ width=90% }
![UFM-24](../assets/USERFLOW%20MOBILE/US24%20Notificación%20de%20restablecimiento%20a%20los%20usuarios%20(Epic_%20EP06).png){ width=50% }
* **User Goal:** Como administrador, quiero que el sistema notifique a los clientes cuando un equipo reportado es reparado, para mejorar su percepción del servicio.
* **Happy Path:** Tras la resolución de una incidencia en el centro de mantenimiento, el sistema actualiza automáticamente el mapa de disponibilidad, habilitando nuevamente la máquina para los usuarios finales.
* **Unhappy Path:** Si la resolución del ticket es parcial o el problema persiste tras la intervención técnica, la máquina permanece inhabilitada en el mapa de disponibilidad, manteniendo la alerta de estado crítico en el centro de mantenimiento.

## US25 Calendario inteligente de bloqueos de reserva(Epic_ EP04)

![UF-25](../assets/USERFLOWS/US25%20Calendario%20inteligente%20de%20bloqueos%20de%20reserva(Epic_%20EP04).png){ width=90% }
![UFM-25](../assets/USERFLOW%20MOBILE/US25%20Calendario%20inteligente%20de%20bloqueos%20de%20reserva(Epic_%20EP04).png){ width=50% } 

* **User Goal:** Como gerente de operaciones, quiero que el sistema agende los mantenimientos preventivos exclusivamente en horarios valle, para no afectar la disponibilidad en horas de alta demanda.
* **Happy Path:** El usuario selecciona un activo desde el mapa de disponibilidad, completa el formulario de reserva con datos válidos y el sistema confirma la operación exitosamente.
* **Unhappy Path:** Si el usuario intenta realizar una reserva con campos obligatorios vacíos o ingresa datos inválidos (como horarios conflictivos), la UI presenta validaciones en rojo indicando los errores específicos.

## US26 Gestión de activos físicos y altas (Epic_ EP07)

![UF-26](../assets/USERFLOWS/US26%20Gestión%20de%20activos%20físicos%20y%20altas%20(Epic_%20EP07).png){ width=90% }
![UFM-26](../assets/USERFLOW%20MOBILE/US26%20Gestión%20de%20activos%20físicos%20y%20altas%20(Epic_%20EP07).png){ width=50% }
* **User Goal:**Como administrador, quiero registrar o dar de baja equipos vinculándolos a un sensor IoT, para actualizar el inventario digital y el mapa de calor. 
* **Happy Path:** El administrador completa el formulario de registro de nueva máquina con datos correctos (nombre, tipo, sede, ID de sensor) y el sistema lo añade al inventario global.
* **Unhappy Path:** Si existen campos faltantes o datos inválidos (como un ID de sensor ya existente), el flujo se detiene y la interfaz resalta los campos que requieren corrección antes de permitir el guardado.

## US28: Gestión automatizada de stock de repuestos

![UF-14](../assets/USERFLOWS/us18diagram.png){ width=90%}

* **User Goal:** Como administrador, quiero controlar el inventario de piezas clave y recibir alertas de reabastecimiento, para que los técnicos siempre tengan insumos disponibles.
* **Happy Path:** El administrador accede al formulario de "Nuevo Ticket de Mantenimiento" y selecciona los repuestos necesarios para la reparación. Al guardar el ticket, el sistema descuenta automáticamente las unidades del inventario y, si el nivel cae por debajo del umbral mínimo, actualiza el estado del repuesto a "Stock Crítico" (color rojo/amarillo en la tabla). Finalmente, el administrador visualiza la alerta en el panel de "Almacén de Repuestos" y el sistema genera una sugerencia de pedido de compra basada en la cantidad faltante para optimizar el inventario.
* **Unhappy Path:** El administrador intenta registrar un ticket de mantenimiento seleccionando un repuesto cuyo stock actual es insuficiente para la operación. Al intentar confirmar la acción, la plataforma despliega una alerta de error indicando que no hay existencias suficientes en el almacén, impidiendo el registro del ticket para evitar inconsistencias en el inventario. El sistema resalta automáticamente el repuesto agotado en la lista y redirige al usuario a la sección de compras para gestionar el reabastecimiento antes de permitir la finalización del ticket técnico.

## US29 Calculadora de impacto financiero por inactividad (Epic: EP08)

![UF-29](../assets/USERFLOWS/US29%20Calculadora%20de%20impacto%20financiero%20por%20inactividad%20(Epic_%20EP08).png){ width=90% }
![UFM-29](../assets/USERFLOW%20MOBILE/US29%20Calculadora%20de%20impacto%20financiero%20por%20inactividad%20(Epic_%20EP08).png){ width=50% }
* **User Goal:**
* **Happy Path:** El sistema calcula y presenta automáticamente el impacto financiero de la inactividad de activos, mostrando métricas clave como la pérdida por inactividad ($1,872), el costo de mantenimiento ($5,150), el ahorro potencial con mantenimiento predictivo ($1,840) y el ROI promedio de recuperación de inversión (7.2 meses).
* **Unhappy Path:** Si los activos no cuentan con datos de operación o historial de inactividad registrado, o si los parámetros financieros ingresados son incompletos o inválidos, la calculadora no puede generar los indicadores y muestra los campos vacíos o un mensaje de error indicando la imposibilidad de calcular el impacto financiero.

## US30 Analítica predictiva de compras e inversión (Epic_ EP08)

![UF-30](../assets/USERFLOWS/US30%20Analítica%20predictiva%20de%20compras%20e%20inversión%20(Epic_%20EP08).png){ width=90% }
![UFM-30](../assets/USERFLOW%20MOBILE/US30%20Analítica%20predictiva%20de%20compras%20e%20inversión%20(Epic_%20EP08).png){ width=50% }
* **User Goal:**
* **Happy Path:** El sistema procesa los datos financieros y de uso para generar proyecciones de ROI y recomendaciones de inversión automáticas basadas en la salud de los activos.
* **Unhappy Path:** Ante la falta de datos históricos suficientes o la introducción de parámetros de cálculo inconsistentes en el simulador, el motor de análisis muestra un estado de error o campos vacíos informando la imposibilidad de generar la proyección.


## 4.5. Web Applications Prototyping.

https://upcedupe-my.sharepoint.com/:v:/g/personal/u202414928_upc_edu_pe/IQB69P8G4G2dQKd17O9Wj0ugAVQ5T99voYxAnWVz-UJhSYI?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=zbX1cQ
