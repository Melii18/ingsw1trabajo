# Respuestas — Ejercitario Unidad 03

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · El significado de proceso

**1. Define en tus propias palabras qué es un proceso de software.**

_Respuesta:_ Un proceso de software es el conjunto organizado de actividades, acciones y tareas que se realizan para construir un producto de software de buena calidad, no son instrucciones estrictas,
sino un marco que el equipo adapta según el proyecto para saber qué hacer, en que orden y quién lo hace, desde que surge la necesidad hasta 
que el sistema está funcionando y se logra mantener estable.


**2. Explica la diferencia entre proceso, metodología y modelo de proceso, con un ejemplo de cada uno.**

_Respuesta:_ PROCESO: es el concepto general, el conjunto de actividades necesarias para desarrollar software (el qué se hace). EJEMPLO: el marco genérico de Pressman (comunicación, planeación, modelado, construcción y despliegue).
MODELO DE PROCESO: es una representación abstracta que define el orden y el flujo en que se organizan esas actividades. EJEMPLO: el modelo en cascada, donde cada fase se completa antes de pasar a la siguiente.
METODOLOGÍA: es la aplicación concreta y detallada de un modelo, con roles, prácticas, técnicas y entregables definidos (el cómo se hace). EJEMPLO: Scrum, que define sprints, roles (Product Owner, Scrum Master, equipo) y artefactos como el backlog.


**3. Enumera las cinco actividades genéricas del marco de trabajo de Pressman.**

_Respuesta:_ 

a- Comunicación
b- Planeación
c- Modelado
d- Construcción
e- Despliegue


**4. Menciona dos actividades "de la sombrilla" y explica por qué se dice que "cubren" todo el proceso.**

_Respuesta:_

A- Gestión de riesgos: identificar qué cosas pueden salir mal en el proyecto o afectar la calidad del producto y pensar cómo evitarlas o reducir su impacto. Por ejemplo, 
en un sistema que depende de un servicio externo, un riesgo es que ese servicio cambie o deje de funcionar.

B- Gestión de la configuración del software: controlar los cambios en el código y en los documentos a lo largo del proyecto, por ejemplo usando Git para tener versiones 
y poder volver atrás si algo se rompe.

---

## Tema 2 · Modelos de proceso

**5. Completen el siguiente cuadro indicando en qué situación conviene usar cada modelo de proceso visto en clase.**

| Modelo | ¿Cuándo conviene usarlo? |
|---|---|
| Cascada | conviene usarlo cuando los requisitos están bien claros desde el inicio y casi no van a cambiar. Por ejemplo, adaptar un sistema de facturación a un cambio puntual de normativa, donde ya se sabe exactamente qué hay que hacer. | 

| Incremental | Cuando se necesita tener algo funcionando rápido y después ir agregando funcionalidades. Por ejemplo, un sistema de ventas donde primero se entrega el registro de ventas y después los reportes. |
| Evolutivo (prototipos) | Cuando el cliente sabe más o menos lo que quiere pero no puede definir los detalles, o hay dudas sobre cómo debería verse la interfaz. Por ejemplo, armar primero la maqueta de una tienda online para que el cliente diga si le sirve. |
| Evolutivo (espiral) | conviene usarlo en proyectos grandes, caros o riesgosos, donde conviene analizar los riesgos en cada vuelta antes de seguir. Por ejemplo, un sistema bancario o uno de salud. |
| Concurrente | conviene para varias actividades o equipos trabajan al mismo tiempo y cada parte del proyecto está en un estado distinto. Por ejemplo, una app donde un equipo diseña la interfaz mientras otro ya programa el backend. |

**6. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Modelo de proceso | Característica principal |
|---|---|
| A. Cascada | 2 |
| B. Incremental | 4 |
| C. Prototipos | 5 |
| D. Espiral | 1 |
| E. Concurrente | 3 |

1. Combina iteración con análisis explícito de riesgo en cada vuelta.
2. Enfoque secuencial y lineal, actividad por actividad.
3. Representa actividades ocurriendo en paralelo, no en secuencia estricta.
4. Entrega el producto en porciones funcionales cada vez más completas.
5. Construye una versión parcial y rápida para validar requisitos poco claros.

**7. Elegí un proyecto de software (hipotético o real) y justificá qué modelo de proceso usarías para desarrollarlo y por qué.**

_Respuesta:_ 

Proyecto (real): un sistema de punto de venta (POS) web para AccountStore PY, mi emprendimiento de venta de suscripciones digitales (Netflix, Spotify, ChatGPT, etc.). El sistema tiene que registrar ventas y clientes y controlar cuándo vence cada suscripción.

Justificación: el negocio ya está funcionando, así que necesitaba empezar a usar el sistema lo antes posible y no podía esperar a que estuviera todo terminado. Con el modelo incremental primero se entrega lo básico (registrar ventas y clientes) y después 
se van sumando partes: control de vencimientos, reportes de ganancias, facturación, etc. Cada incremento ya se usa en el día a día, y eso me sirve para ver qué falta o qué hay que mejorar antes de la siguiente entrega.

Además, lo desarrollo prácticamente solo, así que hacer todo de una vez no sería realista. Cascada no me serviría porque los requisitos fueron apareciendo a medida que usaba el sistema (por ejemplo, al principio no pensé en los recordatorios de vencimiento). 
El espiral tampoco, porque es demasiado pesado para un proyecto de este tamaño y con este nivel de riesgo.
---

## Tema 3 · Iteración de procesos

**8. Explica con tus palabras por qué la mayoría de los procesos modernos son iterativos.**

_Respuesta:_ Porque en la vida real casi nunca se sabe todo desde el principio. Los requisitos cambian por el negocio, por el mercado o porque el mismo cliente se da cuenta de lo que necesita recién cuando ve algo funcionando. Si se trabaja en iteraciones, 
se repite el ciclo varias veces, se recibe feedback rápido y se corrigen errores antes de que sean grandes. Es mucho más barato ajustar el rumbo en ciclos cortos que descubrir al final que el sistema no era lo que se necesitaba.

Me pasó con mis propios proyectos: cada vez que usaba una versión nueva del sistema de ventas aparecían ideas o problemas que no había previsto. Si hubiera querido definir todo al inicio, lo más probable es que hubiera tenido que rehacer gran parte.


**9. Menciona una ventaja y una desventaja de trabajar con iteraciones cortas.**

_Respuesta:_

Ventaja: se recibe feedback seguido, entonces los errores y malentendidos se detectan temprano y es más fácil adaptarse a los cambios. Por ejemplo, si una pantalla no es cómoda para cargar ventas, se nota en la primera semana de uso y se arregla en la siguiente iteración.
Desventaja: hay más trabajo de organización (planificar, revisar y probar en cada iteración), y si no se cuida la estructura del código, los cambios constantes pueden terminar dejando el sistema desordenado y difícil de mantener.

---

## Tema 4 · Especificación, diseño, implementación, validación y evolución

**10. Describan brevemente qué implica cada una de las cuatro actividades fundamentales del proceso de software, según Sommerville.**

| Actividad | Qué implica |
|---|---|
| Especificación | 	Definir qué tiene que hacer el sistema y bajo qué restricciones. Incluye estudiar si es factible y obtener, analizar, documentar y validar los requisitos. Ej.: definir que el POS debe registrar ventas y avisar los vencimientos. |
| Diseño e implementación | Pasar de la especificación a un sistema que funcione: definir la arquitectura, las interfaces, los componentes y la base de datos, y después programarlo. Ej.: diseñar las tablas de clientes y ventas y programar las pantallas. |
| Validación | Comprobar que el sistema cumple con lo especificado y con lo que realmente necesita el cliente, con pruebas (de componentes, de sistema y de aceptación) y revisiones. Ej.: cargar ventas de prueba y verificar que los totales den bien. |
| Evolución | 	Modificar el sistema con el tiempo para adaptarlo a nuevos requisitos, cambios del negocio o corrección de errores. Ej.: agregar un módulo de facturación cuando el negocio lo necesita. |

**11. Relaciona estas cuatro actividades con las cinco fases del ciclo del software vistas en la Unidad 1 (análisis, diseño, implementación, pruebas, mantenimiento). ¿En qué se parecen y en qué se diferencian?**

_Respuesta:_ La relación es bastante directa:

a- Especificación <----> Análisis
b- Diseño e implementación <----> Diseño + Implementación
c- Validación <----> Pruebas
d- Evolución <----> Mantenimiento

En qué se parecen: las dos describen el mismo camino del software, desde entender qué se necesita hasta mantenerlo funcionando, y en el fondo cubren las mismas tareas.

En qué se diferencian: Sommerville junta diseño e implementación en una sola actividad, porque en la práctica se mezclan bastante (muchas veces se diseña mientras se programa). Además, sus actividades no tienen que seguir un orden lineal, sino que se pueden intercalar 
o repetir según el modelo que se use. Y habla de "evolución" en vez de "mantenimiento" para remarcar que el software no solo se corrige, sino que cambia y crece todo el tiempo.

---

## Tema 5 · Herramientas y técnicas para modelado de procesos

**12. Menciona dos formas de representar un proceso (no un sistema) y explica brevemente cada una.**

_Respuesta:_

a- Diagrama de actividades UML: muestra el flujo de actividades del proceso, con decisiones, caminos en paralelo y quién es responsable de cada parte (usando carriles o swimlanes). Por ejemplo, se puede representar el proceso de "tomar un pedido, desarrollar, 
probar y entregar", separado por rol.

b- BPMN (Business Process Model and Notation): es una notación estándar para modelar procesos con eventos, tareas, compuertas de decisión y flujos entre participantes. La ventaja es que la entienden tanto las personas técnicas como las de negocio.

También existe SPEM, una notación de la OMG pensada específicamente para describir procesos de desarrollo de software, con sus roles, tareas y productos de trabajo.

**13. ¿Qué es un patrón de proceso? Da un ejemplo hipotético de un problema recurrente en un proyecto y su solución.**

_Respuesta:_

Un patrón de proceso describe un problema que se repite en el desarrollo de software, el contexto en el que aparece y una solución que ya se probó que funciona. Sirve para reutilizar experiencias que salieron bien en lugar de improvisar cada vez.

Permite establecer una forma ordenada de actuar ante situaciones conocidas durante un proyecto. Por ejemplo, si constantemente se presentan errores porque los requisitos cambian, el equipo puede establecer como solución revisar y aprobar los requisitos con el cliente antes de comenzar cada etapa de desarrollo. De esta manera, se reduce la posibilidad de repetir el mismo problema.

También permite mejorar la planificación del proyecto, ya que el equipo puede anticiparse a situaciones conocidas y aplicar directamente una estrategia adecuada. Esto facilita la toma de decisiones y ayuda a mantener un desarrollo más organizado.

Un ejemplo:

Nombre: Validación temprana con prototipo.
Contexto: un desarrollador arma sistemas web a medida para pequeños negocios cuyos dueños no son técnicos (por ejemplo, una tienda online o una calculadora de costos de envío).
Problema: cada vez que entrega una parte, el cliente dice que "no era así lo que quería", y hay que rehacer pantallas y lógica varias veces.
Solución: antes de programar cada módulo, armar una maqueta rápida de las pantallas (en papel, en Figma o una página simple sin lógica), mostrarla al cliente y pedir su aprobación. Recién ahí se programa.
Resultado: los requisitos quedan validados antes de invertir tiempo en el desarrollo y se reducen mucho los retrabajos.
---

## Tema 6 · Ayuda automatizada al proceso

**14. Explica la diferencia entre herramientas Upper-CASE y Lower-CASE.**

_Respuesta:_

Upper-CASE (alto nivel): ayudan en las primeras etapas del ciclo, como la planificación, el análisis de requisitos y el diseño. Por ejemplo, las herramientas para hacer diagramas UML o el modelo de la base de datos.
Lower-CASE (bajo nivel): ayudan en las etapas finales, más cerca del código: implementación, generación de código, depuración, pruebas y mantenimiento. Por ejemplo, un editor de código con depurador o un sistema de control de versiones.

La diferencia está en qué parte del proceso cubren: las Upper-CASE trabajan sobre modelos y diagramas, y las Lower-CASE sobre el código y el producto que se ejecuta. Las I-CASE (integradas) combinan las dos y cubren todo el ciclo.

También se puede decir que las Upper-CASE se enfocan principalmente en organizar y representar el sistema antes de programarlo, mientras que las Lower-CASE se utilizan cuando el sistema ya está siendo construido o necesita ser revisado y mejorado. Por eso, las primeras ayudan a definir qué se va a desarrollar y las segundas ayudan a determinar cómo se desarrolla, prueba y mantiene.

**15. Menciona tres herramientas que consideren CASE (de su propia experiencia o investigación) y clasifíquenlas según la categoría a la que pertenecen.**

| Herramienta | Categoría (Upper / Lower / I-CASE) |
|---|---|
| draw.io / StarUML (diagramas UML y de base de datos, que uso para planificar mis sistemas) | Upper-CASE |
| Visual Studio Code con depurador y Git (programar, depurar y controlar versiones de mis proyectos) | Lower-CASE |
| Enterprise Architect (modelado, generación de código e ingeniería inversa en una sola herramienta) | I-CASE |

**16. Reflexión final:** de los modelos de proceso vistos en esta unidad, ¿cuál elegirían para un proyecto personal? Justifiquen su elección considerando el tamaño del proyecto, el tiempo disponible y el nivel de certeza sobre los requisitos.

_Respuesta:_

Para un proyecto personal elegiría el modelo incremental, por ejemplo para el sistema de facturación que estoy armando para mi emprendimiento. Es un proyecto chico que desarrollo yo solo, así que no hace falta algo pesado como el espiral. 
Como mi tiempo está repartido entre la facultad y el negocio, me conviene tener rápido una primera versión útil (facturas simples) y después ir sumando el resto. Además, los requisitos no están del todo claros desde el inicio 
y van apareciendo con el uso, por eso descartaría cascada. Con el incremental puedo usar el sistema desde temprano y adaptarlo en cada versión.
