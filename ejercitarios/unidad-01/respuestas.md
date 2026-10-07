# Respuestas — Ejercitario Unidad 01

---

## Tema 1 · Ingeniería de software: una visión previa

**1. En tus propias palabras, define qué es la Ingeniería de Software.**

_Respuesta:_ Es el area que se encarga de aplicar mètodos y tecnicas para desarrollar, utilizar y mantener programas de manera ordenada. 
Su objetivo es crear software de buena calidad, que cumpla con lo que necesitan los usuarios y que pueda realizarse dentro del tiempo y presupuesto disponible.


**2. Explica con un ejemplo la diferencia entre "programar" y "hacer ingeniería de software".**

_Respuesta:_ Programar consiste principalmente en escribir codigo para solucionar un problema. En cambio, la Ingeniería de Software abarca mucho más: 
entender qué necesita el cliente, planificar, diseñar el sistema, programar, hacer pruebas, documentar, mantener el software y trabajar con otras personas.


**3. Menciona dos razones por las cuales la ingeniería de software es necesaria en el desarrollo de sistemas actuales.**

_Respuesta:_ La complejidad y el tamaño de los sistemas: los programas actuales pueden ser muy grandes y complicados, por lo que es necesario seguir un proceso 
organizado para poder desarrollarlos correctamente.
La calidad, los costos y el tiempo: ayuda a reducir errores, trabajos repetidos y gastos innecesarios, además de lograr sistemas más confiables, fáciles de mantener y seguros.

---

## Tema 2 · El rol de la IS en el diseño de sistemas (+ impacto de la IA)

**4. Enumera los elementos que conforman un sistema basado en computadora, además del software.**

_Respuesta:_ Además del software, un sistema está formado por el hardware, las personas que lo utilizan o administran,
los datos e información, la documentación y los procedimientos o reglas que indican cómo debe utilizarse.


**5. Describe brevemente la diferencia entre una visión sistémica y una visión aislada del software en el diseño de sistemas.**

_Respuesta:_ La visión aislada considera al software como algo independiente y se concentra principalmente en el código. En cambio, 
la visión sistémica entiende que el software forma parte de un conjunto donde también están las personas, el hardware, los procesos y la organización.

Esto permite crear soluciones que no solo funcionen técnicamente, sino que también sean útiles y se adapten al entorno donde van a utilizarse.


**6. Elige una herramienta de inteligencia artificial aplicada al desarrollo de software (por ejemplo, un asistente de código o de testing) e indica:**
- Qué tarea del ingeniero de software apoya o transforma.
- Un beneficio concreto que ofrece.
- Un riesgo o desafío que introduce su uso.

_Respuesta:_ GitHub Copilot.

Tarea que apoya: ayuda principalmente en la programación, ya que puede sugerir código, completar funciones y generar pruebas o documentación.
Beneficio: permite ahorrar tiempo y hacer más rápido algunas tareas repetitivas.
Riesgo: puede generar código que tenga errores o problemas de seguridad. Por eso, no conviene aceptar todo lo que propone sin revisarlo. 
También puede generar dependencia de la herramienta y hacer que el programador entienda menos el código si simplemente copia y pega lo que genera


---

## Tema 3 · Historia de la ingeniería de software

**7. En tu opinión, ¿por qué la "crisis del software" de 1968 marcó un punto de inflexión para la disciplina?**

_Respuesta:_ Creo que fue un momento importante porque ayudó a darse cuenta de que desarrollar software no era simplemente sentarse a programar. Muchos proyectos 
estaban teniendo problemas, como retrasos, gastos mayores a los previstos y programas que no funcionaban como se esperaba.

En la conferencia de la OTAN de 1968 comenzó a utilizarse formalmente el término “Ingeniería de Software”, justamente porque se vio la necesidad de tener una forma 
más organizada y profesional de desarrollar software. A partir de ahí fueron apareciendo diferentes métodos, procesos y modelos para mejorar la forma de trabajar.

**Ejercicio de relación** (completá con la letra que corresponda a cada número):

| Evento / Período | Descripción |
|---|---|
| A. Programación artesanal (1950s–60s) | _3_ |
| B. Crisis del software (1968) | _1_ |
| C. Modelo en cascada (1970s–80s) | _5_ |
| D. Métodos iterativos (1990s) | _4_ |
| E. Metodologías ágiles (2001–hoy) | _2_ |

1. Se acuña el término "ingeniería de software" en una conferencia de la OTAN ante fallas y sobrecostos de proyectos.
2. Surge el Manifiesto Ágil; se popularizan Scrum, Kanban y XP.
3. El software se escribía de forma individual, sin procesos formales.
4. Ganan terreno la iteración, el prototipado y los modelos incrementales.
5. Se establecen los primeros procesos formales y estructurados de desarrollo.

---

## Tema 4 · El rol del ingeniero de software

**8. Menciona tres competencias que debe tener un ingeniero de software, además del conocimiento técnico.**

_Respuesta:_ 1- Comunicación efectiva, tanto con los clientes como con el equipo.
2- Capacidad para trabajar en equipo y asumir responsabilidades de liderazgo.
3- Pensamiento crítico y capacidad para resolver problemas.


**9. Describe brevemente qué hace cada uno de los siguientes roles dentro de un equipo de desarrollo:**

| Rol | Descripción |
|---|---|
| Analista | Se encarga de conocer las necesidades del cliente y convertirlas en requisitos claros para el sistema. |
| Arquitecto | Define cómo estará organizado el sistema, qué tecnologías se utilizarán y cómo se relacionarán sus diferentes partes. |
| Desarrollador | Se encarga de programar, integrar y corregir el código del sistema. |
| Tester / QA | Realiza pruebas para encontrar errores y comprobar que el software funcione de acuerdo con los requisitos. |

**10. Caso breve:** Un ingeniero de software descubre, cerca de la fecha de entrega, una falla de seguridad que podría exponer datos de usuarios, pero corregirla retrasaría el proyecto una semana. ¿Qué debería hacer y por qué, considerando la ética profesional?

_Respuesta:_ Lo correcto sería informar inmediatamente sobre la falla al responsable y al equipo, y buscar una solución antes de entregar el sistema, aunque esto signifique retrasar la entrega una semana.

La seguridad y la privacidad de los usuarios son más importantes que cumplir exactamente con una fecha. Entregar un sistema sabiendo que tiene una vulnerabilidad podría causar problemas mucho mayores después, como pérdida de información, problemas legales o daños para la empresa.

Si no es posible solucionar el problema de inmediato, también se podría buscar una solución temporal, dejando todo documentado para poder corregirlo completamente después.


---

## Tema 5 · El ciclo del software

**11. Ordena y nombra las cinco fases genéricas del ciclo de vida del software vistas en clase.**

_Respuesta:_ 
1- Análisis de requisitos.
2- Diseño.
3- Implementación o programación.
4- Pruebas.
5- Mantenimiento.


**12. ¿Por qué se afirma que el mantenimiento suele ser la fase más costosa del ciclo de vida del software? Da un ejemplo hipotético.**

_Respuesta:_ Porque el mantenimiento puede durar muchos años, mientras que el software sigue siendo utilizado y necesita cambios constantemente. 
Durante ese tiempo pueden aparecer errores, cambiar las necesidades de los usuarios, aparecer nuevas tecnologías o modificarse las normas que debe cumplir el sistema.

Por ejemplo, un sistema de facturación puede tardar unos meses en desarrollarse, pero después puede utilizarse durante muchos años. En ese tiempo pueden cambiar las leyes de facturación, 
actualizarse los servidores o solicitarse nuevas funciones. Todos esos cambios hacen que el mantenimiento termine costando más que el desarrollo inicial.

Además, el mantenimiento no consiste solamente en corregir errores, sino también en adaptar y mejorar el software para que continúe siendo útil y seguro. A medida que pasa el tiempo, pueden aumentar la cantidad de usuarios y los datos que maneja el sistema, lo que requiere optimizaciones y actualizaciones. Por esta razón, mantener un software funcionando correctamente durante muchos años puede representar un costo mayor que su desarrollo inicial.

---

## Tema 6 · Relación con otras áreas de la ciencia de la computación

**Completen el siguiente cuadro indicando cómo cada área apoya a la ingeniería de software.**

| Área | ¿Cómo apoya a la Ingeniería de Software? |
|---|---|
| Estructuras de datos y algoritmos | Ayudan a organizar y procesar la información de manera eficiente, mejorando el funcionamiento del software. |
| Bases de datos | Permiten guardar y organizar los datos del sistema de forma segura y ordenada. |
| Sistemas operativos | Se encargan de administrar recursos como la memoria, los procesos y los archivos que utiliza el software. |
| Redes | Permiten que diferentes sistemas y componentes puedan comunicarse entre sí, por ejemplo, mediante internet, APIs o servicios en la nube. |

---

## Tema 7 · Relación con otras disciplinas

**13. Elige dos de las siguientes disciplinas — Administración, Psicología, Economía, Derecho, Comunicación — y explica con un ejemplo concreto cómo se relacionan con el trabajo diario de un ingeniero de software.**

_Respuesta:_ Administración: ayuda al ingeniero a organizar los proyectos, calcular tiempos y costos, distribuir tareas y controlar los recursos. Por ejemplo, al trabajar con Scrum, se necesita organizar las tareas del equipo y decidir cuánto trabajo se puede realizar durante un sprint.
Psicología: ayuda a comprender mejor a las personas. Por ejemplo, al hablar con un cliente es importante saber escuchar y entender lo que realmente necesita. También es útil al diseñar interfaces, ya que permite pensar en cómo los usuarios van a utilizar y entender el sistema. Además, puede ayudar a manejar mejor los problemas o conflictos dentro de un equipo.


**14. Reflexión final:** de todo lo visto en clase (definición, historia, rol del ingeniero, ciclo del software, relación con otras áreas y disciplinas, e impacto de la IA), ¿qué idea te resultó más relevante y por qué?

_Respuesta:_ Lo que más me llamó la atención de este tema fue entender que la Ingeniería de Software no consiste solamente en programar. Antes pensaba que lo principal era escribir un código que funcionara, pero ahora entiendo que también es importante saber qué necesita el usuario, planificar bien el proyecto, hacer pruebas, trabajar en equipo y mantener el sistema después de terminarlo.

También me pareció interesante el uso de la inteligencia artificial, porque herramientas como GitHub Copilot pueden ayudarnos a programar más rápido. Pero al mismo tiempo, no significa que podamos dejar que la IA haga todo por nosotros. Sigue siendo necesario que el ingeniero revise lo que genera, sepa si realmente sirve y tome las decisiones correctas. Al final, la herramienta puede ayudar bastante, pero el criterio de la persona sigue siendo muy importante.

