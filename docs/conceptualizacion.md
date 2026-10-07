---
title: "Conceptualización"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 1 · Conceptualización

> *Punto de partida: entender el problema y encuadrar el proyecto.*

---

## 1. Presentación del proyecto

**Nombre del sistema:** BiblioStock

**Integrantes del grupo:**

| Nombre | Rol |
|---|---|
| Melisa Tillner | Coordinación y contacto con el cliente / documentación |
| Cesar Pereira | Analista: requisitos y modelado |
| Marcelo Benitez | Responsable técnico: repositorio, sitio y tecnología |

**Usuario / cliente real:** Biblioteca Municipal de la ciudad de Piribebuy (Departamento de Cordillera, Paraguay), institución pública que resguarda y ofrece libros a la comunidad. Actualmente no cuenta con ningún sistema informático y gestiona su acervo con registros en pequeñas tarjetas. Referente: Jaime Valenzuela.

---

## 2. Definición del problema

La Biblioteca Municipal de Piribebuy registra la información de cada libro en pequeñas tarjetas físicas, que se consultan y actualizan a mano. No existe ningún sistema de control de stock.

Para saber si tienen un libro, el personal debe revisar las tarjetas una por una. Las dificultades que enfrenta son:

- **Búsqueda lenta:** encontrar un libro por título, autor o tema lleva tiempo.
- **Stock desconocido:** no se sabe con rapidez cuántos ejemplares existen, cuántos están disponibles y cuántos prestados.
- **Riesgo de pérdida:** las tarjetas pueden extraviarse o deteriorarse, y no hay copia de respaldo.
- **Errores e inconsistencias:** la escritura manual favorece duplicados y datos desactualizados o incompletos.
- **Sin trazabilidad ni estadísticas:** es difícil saber quién tiene un libro, qué préstamos están vencidos o qué libros son los más pedidos.

---

## 3. Propósito y objetivos

**Objetivo general:**

Desarrollar un sistema web de control de stock que permita registrar, consultar y mantener actualizado el inventario de libros de la Biblioteca Municipal de Piribebuy, reemplazando el registro manual en tarjetas.

**Objetivos específicos:**

1. Registrar el catálogo de libros (alta, modificación y baja) con sus datos bibliográficos, de modo que cada tarjeta actual pueda cargarse en el sistema.
2. Controlar la cantidad de ejemplares de cada libro y su estado (disponible, prestado, dañado o perdido), mostrando el stock total y el disponible.
3. Permitir búsquedas por título, autor, categoría o código, con resultados en pocos segundos.
4. Registrar préstamos y devoluciones con fecha límite, guardando fecha, socio y ejemplar de cada movimiento.
5. Generar reportes básicos: inventario, préstamos vencidos y libros más solicitados.
6. Migrar al sistema la información existente en las tarjetas.
7. Restringir el acceso mediante usuarios y roles, de modo que solo personal autorizado modifique datos.

---

## 4. Alcance del proyecto

**Incluye (dentro del alcance):**

1. Gestión de libros (título, autor, editorial, año, ISBN, categoría, ubicación en estantería).
2. Gestión de ejemplares y control de stock (cantidad, estado y disponibilidad).
3. Gestión de autores, editoriales y categorías.
4. Gestión de socios/lectores con datos básicos.
5. Registro de préstamos y devoluciones.
6. Búsqueda y consulta del catálogo.
7. Reportes básicos.
8. Usuarios y roles (administrador y bibliotecario).
9. Carga inicial del catálogo (formulario ágil o importación desde planilla).

**No incluye (fuera de alcance):**

- Cobro de multas y gestión contable.
- Préstamo interbibliotecario.
- Catálogo en línea público para lectores externos.
- Lector de código de barras o etiquetas RFID.
- Aplicación móvil nativa.
- Digitalización automática (OCR) de las tarjetas existentes.

---

## 5. Interesados (stakeholders)

| Interesado | Descripción | Interés en el proyecto |
|---|---|---|
| Usuario final: bibliotecario/a | Persona que atiende la biblioteca y opera el sistema a diario. | Registrar y buscar libros con rapidez, sin errores ni trabajo repetitivo. |
| Cliente: director/a o responsable de la biblioteca | Autoridad a cargo de la institución. | Conocer el estado real del acervo y decidir compras y bajas con datos. |
| Administrador del sistema | Persona designada para gestionar usuarios, configuración y respaldos. | Sistema estable, seguro y fácil de mantener. |
| Municipalidad de Piribebuy | Entidad titular de la biblioteca. | Mejorar el servicio público y cuidar los bienes municipales. |
| Lectores / socios | Comunidad que usa la biblioteca. | Encontrar libros más rápido y saber si están disponibles. |
| Docente de la cátedra | Evaluador del trabajo. | Que se cumplan los criterios académicos. |

---

## 6. Justificación / viabilidad

**Viabilidad técnica:** El sistema es una aplicación web de gestión (altas, bajas, modificaciones, búsqueda y reportes) con tecnologías maduras y gratuitas. El grupo cuenta con formación en desarrollo web y bases de datos y puede adquirir lo que falte durante el cuatrimestre.

**Viabilidad operativa:** El sistema replica la lógica actual de las tarjetas con pasos más cortos y una interfaz simple. Con una capacitación breve y un manual de uso, el personal podrá operarlo y mantenerlo. Se requiere que la biblioteca disponga de una computadora.

**Viabilidad económica (alto nivel):** El desarrollo es académico y sin costo para el cliente. Se usan herramientas de software libre y el costo de operación es bajo (una PC existente o un hosting básico). El beneficio esperado es el ahorro de horas de trabajo y la reducción de pérdidas de información y de material.

---

## 7. Visión general de la solución

El grupo propone una aplicación web a la que el personal ingresa desde el navegador con usuario y contraseña. Cada tarjeta en papel pasa a ser un registro digital de un libro, con sus ejemplares asociados.

Desde una pantalla principal, el bibliotecario podrá buscar un libro y ver al instante cuántos ejemplares hay y cuántos están disponibles, registrar nuevos libros o cambios de estado, anotar un préstamo o devolución y consultar reportes. Toda la información se guarda en un solo lugar, con copias de respaldo periódicas, y las tarjetas físicas quedan como archivo histórico.

---

## 8. Glosario de términos

| Término | Definición |
|---|---|
| Acervo | Conjunto total de libros y materiales de la biblioteca. |
| Tarjeta / ficha | Tarjeta de papel con los datos de un libro; es el sistema actual de registro. |
| Libro (título) | Obra identificada por título y autor, sin importar cuántas copias haya. |
| Ejemplar | Copia física individual de un libro, con su propio código y estado. |
| Stock | Cantidad de ejemplares que posee la biblioteca de cada libro. |
| Stock disponible | Ejemplares que están en la biblioteca y pueden prestarse. |
| Estado del ejemplar | Situación de un ejemplar: disponible, prestado, dañado, perdido o dado de baja. |
| ISBN | Código internacional que identifica un libro (puede no existir en libros antiguos). |
| Categoría | Clasificación temática del libro (novela, historia, ciencias, infantil, etc.). |
| Ubicación | Lugar de estantería donde se guarda un ejemplar. |
| Socio / lector | Persona registrada que puede retirar libros en préstamo. |
| Préstamo | Entrega temporal de un ejemplar a un socio con fecha de devolución. |
| Devolución | Regreso del ejemplar a la biblioteca, que lo deja nuevamente disponible. |
| Préstamo vencido | Préstamo cuya fecha de devolución ya pasó sin que se devolviera el ejemplar. |
| Baja | Retiro de un ejemplar del inventario (pérdida, deterioro o donación). |
| Bibliotecario | Usuario del sistema que realiza la operación diaria. |
| Administrador | Usuario con control total del sistema: usuarios, configuración y respaldos. |

---

## 9. Riesgos iniciales

| Riesgo | Impacto | Estrategia de mitigación |
|---|---|---|
| Baja disponibilidad del cliente para reuniones y validaciones | Alto | Agendar reuniones con anticipación, consultar dudas por mensajería y dejar los acuerdos por escrito. |
| Requisitos poco claros o cambiantes | Alto | Validar cada entrega con el cliente y documentar el alcance con claridad. |
| Querer abarcar demasiado (multas, catálogo público, etc.) | Alto | Respetar la lista de "fuera de alcance" y priorizar requisitos. |
| Poca experiencia informática del personal | Alto | Interfaz simple, manual breve y capacitación práctica. |
| Falta de computadora o de conexión a internet en la biblioteca | Alto | Diseñar para funcionar en una sola PC o en red local. |
| Tarjetas con datos incompletos o ilegibles | Medio | Definir campos mínimos obligatorios y permitir marcar datos pendientes. |
| Gran volumen de tarjetas para migrar | Medio | Formulario de carga rápida o importación por planilla, en etapas. |
| Tiempo limitado del equipo por otras materias | Medio | Dividir tareas por rol y trabajar con hitos y seguimiento en GitHub. |
| Desequilibrio de participación en el grupo | Medio | Roles definidos y seguimiento mediante commits. |
| Pérdida de datos del sistema | Alto | Respaldos periódicos y control de versiones del código.|

---

## 10. Selección tecnológica preliminar

| Componente | Elección | Justificación breve |
|---|---|---|
| Lenguaje de programación | Java | Lenguaje robusto, conocido por el grupo y con abundante documentación. |
| Framework | JSP y Servlets con patrón MVC (sobre Apache Tomcat) | Permite aplicar MVC con herramientas ya trabajadas en la carrera; es gratuito. |
| Base de datos | MySQL (o MariaDB) | Gratuita, relacional y adecuada para catálogo, ejemplares y préstamos. |

---

[← Volver al inicio](index.md) · [Siguiente: Análisis →](analisis.md)
