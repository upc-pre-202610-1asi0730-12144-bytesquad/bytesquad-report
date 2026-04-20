# Capítulo I: Introducción
## 1.1. Startup Profile
### 1.1.1 Descripción de la Startup
**Descripción general:**
LocalSync nace para cerrar la brecha entre la gestión tradicional de recintos deportivos y la innovación tecnológica impulsada por el Internet de las Cosas (IoT). Somos una startup comprometida con la optimización de los activos físicos y la mejora de la experiencia del usuario en gimnasios, asegurando que la toma de decisiones basada en datos reemplace a la intuición, maximizando la rentabilidad y la satisfacción del cliente.

**Misión:**
La misión de LocalSync es ofrecer un servicio inteligente de monitoreo y analítica de uso de equipos deportivos, orientado a gimnasios y centros de fitness universitarios. Buscamos optimizar sus procesos operativos y de mantenimiento mediante el uso de IoT (cámaras con visión computacional y sensores en el Edge) para transformar el uso físico de las máquinas en datos accionables gestionados eficientemente en la nube.

**Visión:**
La visión de LocalSync es ser la plataforma líder en telemetría y gestión de activos deportivos en Perú, promoviendo una administración moderna y predictiva que impulse a los gimnasios hacia una transformación digital eficiente y a la vanguardia de la tecnología.

### 1.1.2 Perfiles de integrante del equipo

<img src="../assets/foto-alvaro-f.png" alt="foto-alvaro-f" width="200" height="280">

Soy Alvaro Sebastian Fernanadez Linares (Codigo: u202414928), estudiante de 5to ciclo de Ingeniería de Software. Cuento con un nivel intermedio en C++ y bases sólidas en Java, lenguajes que me han permitido especializarme en el desarrollo backend, enfocándome en la lógica de negocio y la funcionalidad del servidor.
Me defino como una persona responsable, organizada y con una fuerte orientación al trabajo en equipo y la eficiencia. Para este ciclo, mi objetivo en Desarrollo de Aplicaciones Open Source es trasladar mi experiencia en desarrollo estructurado hacia entornos colaborativos. Aspiro a integrar mis habilidades técnicas con la filosofía de código abierto para crear soluciones que no solo sean eficientes, sino también accesibles y transparentes, entendiendo que el futuro de la ingeniería de software se construye colectivamente.

<img src="../assets/foto-lui-f.png" alt="foto-lui-f" width="200" height="280">

Soy Lui Gamero, estudiante de ingeniería de Software, actualmente me encuentro cursando el cuarto ciclo de la carrera y desde el cuarto año de secundario mi interés se fijó en los problemas de la programación, ya cuento con experiencia en programación con C++ lo que considero que es una base sólida en la buena estructura de la programación, además de ello me considera analista y creativo al poder resolver problemas confusos o complejos.

<img src="../assets/foto-carla-f.png" alt="foto-lui-f" width="200" height="280">

Soy Carla Alejandra Gallardo Morales, tengo 19 años. Desde que me incorporé en la Universidad Peruana de Ciencias Aplicadas en el periodo 2024-01, es decir que ahora mismo estoy cursando el quinto ciclo de la carrera de Ing. de Software, he adquirido y desarrollado distintos conocimientos a cerca de la programación, específicamente en el lenguaje C++ y Java, además, de forma autodidacta y extracurricular, he profundizado en el lenguaje Python, lo que ha ampliado mi perspectiva sobre la lógica y resolución de problemas.
Dentro del equipo, mi contribución se basa en el apoyo continuo del desarrollo del backend y frontend de nuestro aplicativo, asimismo ayudo en la implementación del informe de nuestro proyecto.

<img src="../assets/foto-jesus-c.png" alt="foto-jesus-c" width="200" height="280">

Soy Jesús Miguel Cataño Zárate, (Codigo: u202413214). Actualmente estudio el 5to ciclo de Ingeniería de Software. Cuento con un nivel intermedio en C++,C# y experiencia usando Java, para desarrollos moviles y HTML,JS,Node.Js en cuanto a paginas web. 
Mi aporte al equipo, a nivel técnico, contribuyo en el desarrollo Fullstack utilizando Spring Boot y Angular para la creación de arquitecturas escalables y eficientes. Por otro lado, desempeño el rol de Team Leader dentro de mi grupo, asumiendo la responsabilidad de guiar y coordinar al equipo para trabajar de manera efectiva.

## 1.2. Solution Profile
### 1.2.1 Antecedentes y problemática

La gestión operativa y el mantenimiento de equipos en centros deportivos representan un desafío crítico en la actualidad. Una administración deficiente, caracterizada por el desconocimiento del estado real y la disponibilidad de las máquinas, desencadena consecuencias operativas y financieras severas para las empresas. De acuerdo con ResQ (s.f.), cuando se producen fallas repentinas en los equipos por falta de monitoreo, los costos de reparación suelen ser entre 3 y 5 veces más altos en comparación con los gastos de un mantenimiento preventivo programado.

Además del impacto económico directo, la experiencia del cliente se ve profundamente perjudicada. El 70% de los usuarios finales manifiesta una alta insatisfacción al descubrir que su máquina preferida se encuentra averiada en el momento de su entrenamiento (Athletic Business, 2024, como se citó en DINGG, 2025). Esta falta de visibilidad impide que los usuarios organicen su tiempo adecuadamente, generando desánimo e incrementando significativamente la probabilidad de que cancelen sus suscripciones. Paralelamente, para la administración del establecimiento, esta carencia de información centralizada y en tiempo real se traduce en una planificación de mantenimiento ineficiente y en una toma de decisiones imprecisa respecto a la reubicación, reparación o compra de nuevos equipos.


**What (Qué):**

El problema es la baja administración que se le dan a las máquinas, de tal manera que se ignoran el estado y disponibilidad de estas. Según ResQ (s.f), las fallas repentinas de las máquinas ocasionan que los costos de reparación sean 3 o 5 veces más caros de lo normal. Por otro lado, el 70% de usuarios finales muestran insatisfacción cuando su máquina preferida está dañada (Athletic Business, 2024, como se citó en DINGG, 2025).
Esto repercute en que los usuarios finales no tengan la capacidad de organizar su tiempo adecuadamente al no saber si una máquina está disponible o si está en mantenimiento. Incluso, es posible que se desanimen y cancelen su suscripción. Por otro lado, con respecto a la administración, la planificación del mantenimiento y la toma de decisiones fundamentadas sobre la compra o reubicación de equipos termina siendo imprecisa.
https://dingg.app/blogs/your-5-step-operational-plan-to-handle-equipment-failures

**When (Cuándo):**

El problema surge y se intensifica drásticamente durante las "horas pico" de los gimnasios (generalmente temprano por la mañana y después de las 6:00 PM). En estos momentos, los usuarios deben lidiar con instalaciones abarrotadas y disputar el uso de máquinas populares (como trotadoras o racks de sentadillas), lo que implica tiempos de espera que rompen el ritmo de sus entrenamientos.
Desde la perspectiva administrativa, el problema del mantenimiento surge de forma imprevista. Las roturas de cables o fallos de motor en máquinas cardiovasculares ocurren súbitamente en medio de la operación diaria, obligando a poner carteles de "Fuera de Servicio" que generan malestar general.

**Where (Dónde):**

El principal lugar donde se encuentran los mayores clientes potenciales sería en las cadenas de gimnasios de tamaño mediano y grande en Lima, así como en centros deportivos universitarios. Estos establecimientos poseen una gran cantidad de activos costosos distribuidos en espacios amplios y, en muchos casos, cuentan con múltiples sedes, lo que dificulta bastante el control manual de qué se usa, cuánto se usa y dónde hace falta más equipamiento.

**Who (Quién):**

El problema afecta principalmente a dos grupos bien definidos: los administradores de los gimnasios y los usuarios/clientes (feligreses del fitness).
Por un lado, los administradores y dueños lidian con presupuestos ajustados. Al no tener telemetría, deben adivinar cuándo hacer mantenimiento o qué máquinas comprar. Esto representa una gran dificultad operativa y un riesgo de pérdida económica por mala gestión de activos.
Por otro lado, los usuarios se ven directamente afectados por la falta de disponibilidad. Llegan al local y deben caminar por todo el recinto buscando una máquina libre, lo cual genera estrés y pérdida de tiempo.
La solución que proponemos está pensada para que los administradores utilicen un dashboard analítico que les alerte de mantenimientos y muestre estadísticas de uso. Asimismo, está diseñada para que los clientes, mediante una app móvil, puedan consultar la "temperatura" (disponibilidad) de las máquinas en tiempo real antes de salir de casa o mientras están en el local.

**Why (Por qué):**

En primer lugar, la principal causa del problema es la carencia de sistemas de telemetría e IoT en los gimnasios tradicionales. La gestión se basa en la observación visual de los entrenadores y en reportes manuales cuando algo ya falló. Esto puede confirmarse gracias a MantainNow (2025), un error común de las organizaciones es que el mantenimiento que se realiza es reactivo. Es decir, se efectúa una vez el daño ya está hecho.

https://www.maintainnow.app/learn/guides/mro-maintenance-repair-operations-a-practical-guide

En segundo lugar, otro factor es la incapacidad de procesar datos de flujo de personas en tiempo real. Aunque algunos gimnasios tienen torniquetes de ingreso, esto solo indica cuánta gente hay en el local, pero no indica qué están usando. En consecuencia, la gestión de la capacidad se vuelve deficiente, haciendo que los clientes pierdan tiempo y que los administradores presenten dificultades para optimizar sus locales. Esto lo confirma Rework (s.f), en donde menciona que el aforo no debería percibirse por cantidad si no por acumulación de usuarios en las máquinas. O sea, 78 personas pueden encontrarse dentro de un local con un aforo de 100 personas. No obstante, estas se agruparán en máquinas específicas, dejando el resto con un porcentaje de uso significativamente menor.

**How (Cómo):**

La plataforma funcionará mediante un sistema dual (Web App para usuarios y Dashboard para administradores) alimentado por dispositivos IoT. En las instalaciones se utilizarán cámaras simples con reconocimiento en el Edge (o sensores de uso) que solo enviarán datos de estado (Ocupado/Libre) y tiempo a nuestra base de datos, respetando la privacidad (no se graba video).
La mayoría de los clientes preferirán acceder mediante dispositivos móviles, por lo que la interfaz en Angular será responsiva. Verán un catálogo de máquinas agrupadas por tipo (Cardio, Pesas, etc.) con indicadores de colores (ej. Verde: Libre, Rojo: Ocupado) como un mapa de calor.
Los administradores ingresarán mediante un login seguro (JWT) a un panel donde visualizarán gráficos de barras de uso histórico, alertas de "Mantenimiento requerido (Límite de 500 horas superado)", y recomendaciones para reubicar equipos poco usados.

**How much (Cuánto):**

La ineficiencia en la gestión de activos dentro de los centros fitness desencadena un impacto financiero que compromete severamente la rentabilidad del negocio. En primer lugar, la dependencia de un modelo reactivo infla el Sobrecosto Operativo (OPEX), dado que la ejecución de mantenimientos correctivos de emergencia resulta entre 3 a 5 veces más costosa que una estrategia preventiva planificada (Oxmaint, 2023). Este sobrecosto se agrava con la Depreciación Acelerada de Activos (CAPEX) considerando que el equipamiento cardiovascular comercial exige inversiones iniciales de $3,000 a $8,000 USD por unidad (Top Fitness, 2024), una falla correctiva mayor (como el reemplazo de un motor AC por fricción) puede consumir hasta el 40% de su valor residual, fulminando el Retorno de Inversión (ROI) proyectado. Finalmente, esta precariedad logística golpea el indicador más crítico: la retención. Con una tasa de abandono (Churn Rate) anual de la industria que oscila entre el 30% y el 40%, la inoperatividad de los equipos y la consecuente congestión de los locales se posicionan consistentemente en el "Top 3" de motivos de cancelación (Energym, 2023). Sabiendo que el Costo de Adquisición de Clientes (CAC) es 5 veces mayor que el costo de retenerlos (IHRSA, 2023), el downtime constante de las máquinas puede convertirse en una fuga de capital insostenible.

Energym. (2023). *Why do gym members cancel their memberships?* https://energym.io/blogs/braingains/why-do-gym-members-cancel-their-memberships

Oxmaint. (2023). *Corrective vs. preventive work orders*. https://www.oxmaint.com/blog/post/corrective-vs-preventive-work-orders

Top Fitness Store. (2024). *Commercial & professional treadmills*. https://www.topfitness.com/collections/commercial-treadmills

### 1.2.2 Lean UX Process
#### 1.2.2.1. Lean UX Problem Statements.

Nuestro servicio ofrece una plataforma de telemetría y visualización en tiempo real para monitorear el uso, desgaste y disponibilidad de las máquinas de ejercicio. Hemos observado que los gimnasios enfrentan sobrecostos por mantenimientos reactivos y tiempos prolongados de equipos inoperativos, a la par que los usuarios experimentan largos tiempos de espera para entrenar durante las horas pico, reduciendo la tasa de retención. ¿De qué manera podemos visibilizar la ocupación y el estado de los activos para optimizar la planificación preventiva de la gerencia y permitir a los usuarios ejecutar sus rutinas sin tiempos muertos?
#### 1.2.2.2. Lean UX Assumptions.
**¿Quién es el usuario?**

Nuestros usuarios principales son los administradores/dueños de gimnasios y los usuarios finales (clientes). El administrador utilizará el sistema para ver reportes y alertas, mientras que el cliente lo usará para ver la disponibilidad en tiempo real.

**¿Dónde encaja nuestro producto en su trabajo o vida?**

Para el cliente, encaja en su rutina diaria de planificación de entrenamiento (antes de ir al gimnasio o mientras descansa entre series). Para el administrador, es una herramienta de gestión diaria y de planificación financiera mensual.

**¿Qué problemas tiene nuestro producto que resolver?**

La saturación de máquinas, la pérdida de tiempo de los usuarios, las averías imprevistas de equipos costosos y la mala distribución del inventario de máquinas entre diferentes locales.

**¿Cuándo y cómo es usado nuestro producto?**

Los clientes lo usarán en sus smartphones principalmente en horas pico o minutos antes de dirigirse al local. Los administradores lo usarán en computadoras de escritorio o tablets durante su jornada laboral para revisar el estado del local.

**¿Qué características son importantes?**

Mapa de calor de disponibilidad en tiempo real, registro automático de horas de uso vía IoT, notificaciones de mantenimiento predictivo, panel estadístico de máquinas más/menos usadas, e interfaz responsiva.

**¿Cómo debe verse nuestro producto y cómo debe comportarse?**

Debe tener un aspecto moderno, deportivo y ágil. Para los usuarios, debe ser extremadamente visual (uso de semaforización: verde, amarillo, rojo). Para los administradores, debe lucir como una herramienta profesional y gerencial (dashboards claros, tablas ordenadas y alertas visibles).

**Creo que mi cliente necesita** una mejora en la organización de sus tiempos de rutina y, por el lado administrativo, una reducción en costos de mantenimiento.

**Estas necesidades se pueden resolver con** la implementación de nuestra plataforma IoT de telemetría y mapas de calor.

**Nuestros clientes iniciales son** las cadenas medianas de gimnasios en Lima, regiones cercanas a Lima y centros deportivos universitarios.

**El mayor valor que prioriza** mi cliente (usuario) es no hacer filas; y para el administrador, maximizar la vida útil de sus activos y tener menos pérdidas.

**El cliente también puede obtener beneficios adicionales** como tener certeza de cómo invertir su capital de manera más precisa, enfocar la labor operativa del staff hacia los clientes en vez de perder tiempo en la inspección de máquinas. Esto es por la parte administrativa. Por otro lado, con respecto a los usuarios finales, estos podrán tomar decisiones más inteligentes a la hora de planificar sus rutinas, lo que mejora drásticamente la conveniencia y la utilidad percibida de su membresía.

**Obtendremos clientes** ofreciendo un piloto gratuito de un mes instalando hardware básico en una zona específica (ej. zona de cardio) para demostrar el valor de la data obtenida.

**Generamos ingresos mediante** un modelo B2B SaaS: cobramos a los gimnasios una suscripción mensual por el uso del panel analítico y un costo de instalación inicial del hardware IoT.

**Nuestra competencia principal** serían las aplicaciones genéricas de reservas de gimnasios, pero los venceremos mediante nuestro valor diferencial. No requerimos que el usuario reserve una máquina manualmente, sino que usamos hardware IoT (cámaras/sensores) para reportar la realidad de forma automática y pasiva.

**Los venceremos** debido a que proponemos una solución utilizando diversos dispositivos IoT que permiten una recopilación de datos eficiente, además de que estos datos luego son convertidos a mapas de calor y gráficos estadísticos. Todo esto permite mejorar la administración de las máquinas y la satisfacción del cliente, lo que significa más ingresos y menos pérdidas para la empresa.

**Nuestros mayores riesgos** son la complejidad en la instalación física del hardware y la dependencia de la red Wi-Fi del local. 

**Esto lo resolveremos** utilizando protocolos ligeros y dispositivos que puedan guardar temporalmente la data si se cae la red.

**Otras suposiciones** que tenemos es que ciertos gimnasios ya tengan este tipo de sistemas o que cierta maquinaria venga con telemetría ya incluída. En consecuencia, nuestra idea carecería de valor. Por ende, es importante tener en mente que si un gimnasio ya posee este sistema debemos proponer una mejora.

#### 1.2.2.3. Lean UX Hypothesis Statements.

Hipótesis 1:

**Creemos que proporcionar** un panel de control web de alertas preventivas de mantenimiento a los gerentes de operaciones les permitirá anticiparse a las fallas mecánicas.

**Sabremos que** hemos tenido éxito

**Cuando veamos** que el tiempo de inactividad de las máquinas se reduce en un 40%.

Hipótesis 2:

**Creemos que** ofrecer una funcionalidad en la aplicación web que sugiera horarios de menor demanda a los clientes frecuentes les ayudará a evitar largos tiempos de espera para usar sus equipos.

**Sabremos que** nuestra solución es acertada

**Cuando veamos** que la retención de usuarios del gimnasio se incrementa en un 15%.

#### 1.2.2.4. Lean UX Canvas.

## 1.3. Segmentos objetivos

**Segmento 1:**
Administradores y Gerentes de Operaciones
Profesionales encargados de la rentabilidad, el mantenimiento y la gestión diaria de las sedes del gimnasio. Suelen tomar decisiones bajo presión y manejan presupuestos operativos. Tienen un nivel de conocimiento tecnológico intermedio, por lo que requieren interfaces limpias, dashboards analíticos fáciles de interpretar y reportes financieros (como cálculos de ROI o impacto financiero por inactividad) generados de manera automatizada.

**Segmento 2:** Clientes frecuentes de gimnasio Hombres y mujeres de 18 a 45 años, estudiantes universitarios o profesionales, con una rutina activa y tiempo limitado para entrenar. Valoran la eficiencia durante su estadía en el recinto deportivo. Buscan herramientas digitales rápidas y responsivas accesibles desde sus dispositivos móviles para optimizar su tiempo de entrenamiento y evitar aglomeraciones.