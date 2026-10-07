# Respuestas — Ejercitario Unidad 04

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · El proceso de requerimientos

**1. Define en tus propias palabras qué es la ingeniería de requerimientos.**

_Respuesta:_ La ingeniería de requerimientos es el proceso de identificar, analizar, documentar y validar las necesidades que debe cumplir un sistema. Su objetivo es entender qué necesita realmente el usuario y convertir esas necesidades en requisitos claros para que el equipo pueda desarrollar correctamente el software.


**2. Explica la diferencia entre "requerimiento", "especificación de requisitos" e "ingeniería de requisitos", con un ejemplo de cada uno.**

_Respuesta:_ Un requerimiento es una necesidad o condición que el sistema debe cumplir. Por ejemplo: “El sistema debe permitir registrar nuevos estudiantes”.
La especificación de requisitos es el documento donde se detallan de manera organizada los requisitos que debe cumplir el sistema. Por ejemplo, especificar los datos que se deben ingresar para registrar a un estudiante, como nombre, apellido, documento y carrera.

La ingeniería de requisitos es todo el proceso utilizado para descubrir, analizar, documentar y validar esos requisitos. Por ejemplo, entrevistar a los funcionarios de una universidad para conocer qué necesitan del sistema de inscripción.

---

## Tema 2 · Tipos de requerimientos

**3. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Tipo de requerimiento | Descripción |
|---|---|
| A. Funcional | _2_ |
| B. No funcional | _3_ |
| C. Del dominio | _1_ |

1. Proviene de las reglas o restricciones propias del área o dominio de negocio.
2. Describe una función o servicio concreto que el sistema debe realizar.
3. Restringe cómo debe comportarse el sistema (desempeño, seguridad, usabilidad, etc.).

**4. Completen el siguiente cuadro comparando los requerimientos de usuario y los requerimientos de sistema.**

| Aspecto | Requerimientos de usuario | Requerimientos de sistema |
|---|---|---|
| Audiencia principal |Usuarios y clientes |Desarrolladores y equipo técnico |
| Nivel de detalle |General y de alto nivel |Detallado y específico |
| Lenguaje utilizado |Lenguaje natural y fácil de entender |Lenguaje más técnico y preciso |

**5. Elegí un sistema que conozcas (una app, una plataforma, un sistema de tu universidad o trabajo) y da un ejemplo propio de un requerimiento funcional y uno no funcional para ese mismo sistema.**

_Respuesta:_ Sistema elegido: el sistema académico web de la universidad, donde los alumnos consultan notas e inscripciones.

- **Requerimiento funcional:** "El sistema debe permitir que el alumno se inscriba a las materias del semestre y descargue el comprobante de inscripción en PDF."
- **Requerimiento no funcional:** "El sistema debe soportar al menos 500 alumnos conectados al mismo tiempo durante el período de inscripciones, mostrando cada página en menos de 3 segundos."

El primero describe un servicio concreto que el sistema realiza (qué hace), mientras que el segundo restringe cómo debe comportarse (rendimiento y capacidad) y se puede verificar con una prueba de carga.


---

## Tema 3 · Características de los requerimientos

**6. Completen el siguiente cuadro indicando qué pregunta permite verificar cada característica de un buen requerimiento.**

| Característica | Pregunta que permite verificarla |
|---|---|
| Correcto | ¿Este requerimiento refleja realmente lo que la biblioteca (el cliente) necesita? |
| No ambiguo | 	¿Se puede interpretar de una sola forma, o dos personas podrían entenderlo distinto? |
| Completo | 	¿Incluye toda la información necesaria (casos, datos, condiciones) o falta algo para poder implementarlo? |
| Verificable | 	¿Se puede diseñar una prueba concreta que demuestre si el sistema lo cumple o no? |

**7. Tomá el requerimiento "El sistema debe ser rápido" y reescribilo de forma que cumpla con las características de un buen requerimiento vistas en clase.**

_Respuesta:_

"El sistema debe mostrar el resultado de la búsqueda de un libro por título, autor o ISBN en menos de 2 segundos, con un catálogo de hasta 20.000 libros y hasta 10 usuarios consultando al mismo tiempo."
Así el requerimiento ya no es ambiguo ("rápido" puede significar cualquier cosa), dice exactamente qué operación se mide y en qué condiciones, y se puede verificar con una prueba cronometrando la búsqueda.

---

## Tema 4 · Obtención y análisis de requerimientos

**8. Enumera las cuatro etapas del ciclo de obtención y análisis de requerimientos vistas en clase.**

_Respuesta:_

1- Descubrimiento de requerimientos: interactuar con los interesados (bibliotecarios, director, socios) para conocer sus necesidades.
2- Clasificación y organización: agrupar los requerimientos relacionados, por ejemplo en "gestión de libros", "préstamos y devoluciones" y "reportes".
3- Priorización y negociación: ordenar los requerimientos por importancia y resolver conflictos entre los distintos interesados.
4- Especificación (documentación): documentar los requerimientos para usarlos en la siguiente vuelta del ciclo.

Es un ciclo, así que estas etapas se repiten varias veces hasta que los requerimientos quedan claros.

**9. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Técnica de obtención | Situación en que conviene usarla |
|---|---|
| A. Entrevistas | _3_ |
| B. Observación | _1_ |
| C. Talleres / workshops | _2_ |

1. Cuando el usuario no puede verbalizar fácilmente lo que necesita.
2. Cuando hay varios interesados con visiones distintas que negociar.
3. Cuando se quiere profundizar con un interesado en particular.

---

## Tema 5 · Técnicas de especificación de requerimientos

**10. Completen el siguiente cuadro indicando una ventaja y una limitación de cada técnica de especificación de requerimientos.**

| Técnica | Ventaja | Limitación |
|---|---|---|
| Lenguaje natural estructurado | Es fácil de entender para todos, incluso para los bibliotecarios, y con plantillas se mantiene cierto orden. | Sigue siendo lenguaje natural, así que puede tener ambigüedades y quedar muy extenso. |
| Casos de uso | 	Muestran claramente la interacción entre el usuario y el sistema paso a paso, por ejemplo el caso "Registrar préstamo" con sus flujos alternativos (libro sin stock, socio con deuda). | Pueden volverse muy detallados y difíciles de mantener, y no sirven bien para requerimientos no funcionales. |
| Historias de usuario | Son cortas y centradas en el usuario. Ej.: "Como bibliotecario, quiero ver qué libros están con la devolución vencida para poder reclamarlos". | Tienen poco detalle, por lo que dependen de la comunicación constante con el cliente y de los criterios de aceptación. |
| Diagramas (UML) | Representan visualmente la estructura y el comportamiento del sistema (por ejemplo, un diagrama de clases con Libro, Ejemplar, Socio y Préstamo), lo que ayuda a ver relaciones que en texto no se notan. | Requieren conocimientos técnicos para entenderlos, así que no siempre sirven para validar con el cliente. |

---

## Tema 6 · Especificaciones formales

**11. ¿Qué es una especificación formal y en qué tipo de sistemas se justifica su uso? Da un ejemplo hipotético de un sistema donde la usarías.**

_Respuesta:_

Una especificación formal describe los requerimientos usando notaciones matemáticas (por ejemplo, lógica, teoría de conjuntos o lenguajes como Z o B), en lugar de lenguaje natural. Como todo queda definido de forma precisa, se eliminan las ambigüedades y se puede demostrar matemáticamente si el sistema cumple o no con lo especificado.

El problema es que es costosa, lleva mucho tiempo y necesita gente especializada, por eso solo se justifica en sistemas críticos, donde un error puede causar pérdidas de vidas, daños graves o pérdidas económicas muy grandes: sistemas médicos, aeronáuticos, ferroviarios, nucleares o bancarios.

En el sistema de control de stock de la biblioteca no se justificaría, porque un error (por ejemplo, un stock mal calculado) se puede corregir sin consecuencias graves, y el costo de una especificación formal sería mucho mayor que el beneficio.
Ejemplo hipotético donde sí la usaría: el software que controla una bomba de insulina, que calcula y aplica la dosis al paciente. Usaría una especificación formal para definir exactamente cuándo se puede aplicar una dosis, cuál es la dosis máxima permitida y qué pasa si falla un sensor, porque un error en esa lógica podría poner en riesgo la vida del paciente.

---

## Tema 7 · Prototipado de los requerimientos

**12. Explica la diferencia entre un prototipo desechable y un prototipo evolutivo, con un ejemplo de un proyecto donde usarías cada uno.**

_Respuesta:_ Un prototipo desechable se crea para probar una idea o comprender mejor los requerimientos y luego se descarta. Por ejemplo, realizar una maqueta de una aplicación bancaria para mostrarle al cliente cómo serían las pantallas antes de comenzar el desarrollo real.
Un prototipo evolutivo comienza como una versión básica y luego se va mejorando hasta convertirse en parte del sistema final. Por ejemplo, desarrollar una primera versión de una aplicación universitaria y agregar funcionalidades progresivamente según las necesidades de los usuarios.


---

## Tema 8 · Técnicas de construcción rápida

**13. Menciona dos técnicas de construcción rápida de prototipos vistas en clase y explica brevemente en qué consiste cada una.**

_Respuesta:_

Desarrollo con lenguajes de alto nivel / dinámicos: usar lenguajes y entornos que permiten programar rápido, como Python, JavaScript o PHP, que tienen muchas funciones ya incorporadas y no requieren tanto código. Así se llega a algo funcional en poco tiempo, aunque no esté optimizado. Por ejemplo, armar en pocas horas una página que permita cargar libros y ver el stock.

Ensamblaje de componentes y aplicaciones (reutilización): armar el prototipo juntando componentes que ya existen (librerías, frameworks, plantillas, APIs), en lugar de programar todo desde cero. Por ejemplo, usar Bootstrap para la interfaz y una API pública de libros (como Open Library) para completar automáticamente el título y el autor a partir del ISBN. También se pueden usar prototipos en papel o wireframes (con herramientas como Figma), que muestran solo la interfaz sin lógica y sirven para validar pantallas muy rápido con los bibliotecarios.

---

## Tema 9 · Validación de requerimientos

**14. Completen el siguiente cuadro relacionando cada técnica de validación con el tipo de problema que detecta mejor.**

| Técnica de validación | Qué tipo de problema detecta mejor |
|---|---|
| Revisiones de requisitos | Errores en el documento: requerimientos ambiguos, incompletos, contradictorios entre sí o que no cumplen los estándares. Ej.: un requisito dice que el préstamo dura 15 días y otro dice 7. |
| Prototipado | Requerimientos que no reflejan lo que el usuario realmente necesita, o problemas de usabilidad que solo se notan al ver el sistema funcionando. Ej.: el bibliotecario ve que para prestar un libro tiene que pasar por demasiadas pantallas. |
| Generación de casos de prueba | Requerimientos que no se pueden verificar o que son demasiado vagos; si no se puede escribir una prueba para un requerimiento, significa que está mal definido. Ej.: "El sistema debe avisar cuando haya poco stock" no dice cuánto es "poco". |

---

## Tema 10 · Administración de requerimientos

**15. Explica con tus palabras qué es la trazabilidad de requerimientos y por qué es importante en un proyecto real.**

_Respuesta:_ La trazabilidad de requerimientos consiste en poder relacionar cada requerimiento con su origen, diseño, implementación y pruebas correspondientes. Es importante porque permite saber de dónde surgió cada requisito y comprobar que realmente fue desarrollado y probado. También facilita realizar cambios en el proyecto sin perder de vista qué partes del sistema pueden verse afectadas.

---

## Tema 11 · Medición de requerimientos

**16. Menciona dos métricas que se pueden aplicar a los requerimientos de un proyecto y qué información le aporta cada una al equipo.**

_Respuesta:_ 
1. Cantidad de requerimientos: permite conocer cuántos requisitos tiene el proyecto y ayuda al equipo a estimar el tamaño y alcance del trabajo.

2. Porcentaje de requerimientos validados: indica qué cantidad de los requisitos ya fueron revisados y aprobados por los interesados. Esto permite conocer el avance del proceso de definición de requisitos.


**17. Reflexión final:** pensá en un proyecto de software (hipotético o real). Describí qué técnica de obtención, qué técnica de especificación y qué técnica de validación usarías para sus requerimientos, y justificá tu elección considerando el tipo de proyecto y de usuarios.

_Respuesta:_

Para el sistema de control de stock de una biblioteca usaría:

Obtención: entrevistas y observación. Con entrevistas al director y a los bibliotecarios entendería qué necesitan, y observándolos trabajar vería cómo registran hoy los libros y los préstamos, incluso los pasos que no mencionan porque ya los hacen de memoria.

Especificación: casos de uso. El sistema tiene procesos bien definidos (alta de libros, préstamo, devolución, control de stock), y los casos de uso permiten describir cada uno paso a paso, incluyendo situaciones como un libro sin stock o un socio con devoluciones pendientes.

Validación: prototipado. Los bibliotecarios no son técnicos, así que la mejor forma de validar es mostrarles las pantallas y que prueben registrar un préstamo, para confirmar que el sistema se adapta a su forma de trabajar.
