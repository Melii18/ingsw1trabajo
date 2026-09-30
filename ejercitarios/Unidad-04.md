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

_Respuesta:_


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


---

## Tema 7 · Prototipado de los requerimientos

**12. Explica la diferencia entre un prototipo desechable y un prototipo evolutivo, con un ejemplo de un proyecto donde usarías cada uno.**

_Respuesta:_ Un prototipo desechable se crea para probar una idea o comprender mejor los requerimientos y luego se descarta. Por ejemplo, realizar una maqueta de una aplicación bancaria para mostrarle al cliente cómo serían las pantallas antes de comenzar el desarrollo real.
Un prototipo evolutivo comienza como una versión básica y luego se va mejorando hasta convertirse en parte del sistema final. Por ejemplo, desarrollar una primera versión de una aplicación universitaria y agregar funcionalidades progresivamente según las necesidades de los usuarios.


---

## Tema 8 · Técnicas de construcción rápida

**13. Menciona dos técnicas de construcción rápida de prototipos vistas en clase y explica brevemente en qué consiste cada una.**

_Respuesta:_


---

## Tema 9 · Validación de requerimientos

**14. Completen el siguiente cuadro relacionando cada técnica de validación con el tipo de problema que detecta mejor.**

| Técnica de validación | Qué tipo de problema detecta mejor |
|---|---|
| Revisiones de requisitos | |
| Prototipado | |
| Generación de casos de prueba | |

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
