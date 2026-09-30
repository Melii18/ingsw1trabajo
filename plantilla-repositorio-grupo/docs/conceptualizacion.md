---
title: "Conceptualización"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 1 · Conceptualización

> *Punto de partida: entender el problema y encuadrar el proyecto.*

---

## 1. Presentación del proyecto

**Nombre del sistema:** [Bibliostock]

**Integrantes del grupo:**

| Nombre | Rol |
|---|---|
| [Melisa Tillner] | [Coordinación y contacto con el cliente / documentación] |
| [Cesar Pereira] | [Analista: requisitos y modelado] |
| [Marcelo Benitez] | [Responsable técnico: repositorio, sitio y tecnología] |

**Usuario / cliente real:** [Biblioteca Municipal de la ciudad de Piribebuy (Departamento de Cordillera, Paraguay), institución pública que resguarda y ofrece libros a la comunidad. Actualmente no cuenta con ningún sistema informático y gestiona su acervo con registros en pequeñas tarjetas. Referente: Jaime Valenzuela]

---

## 2. Definición del problema

[La Biblioteca Municipal de Piribebuy registra la información de cada libro en pequeñas tarjetas físicas, que se consultan y actualizan a mano. No existe ningún sistema de control de stock.

Para saber si tienen un libro, el personal debe revisar las tarjetas una por una. Las dificultades que enfrenta son:

Búsqueda lenta: encontrar un libro por título, autor o tema lleva tiempo.
Stock desconocido: no se sabe con rapidez cuántos ejemplares existen, cuántos están disponibles y cuántos prestados.
Riesgo de pérdida: las tarjetas pueden extraviarse o deteriorarse, y no hay copia de respaldo.
Errores e inconsistencias: la escritura manual favorece duplicados y datos desactualizados o incompletos.
Sin trazabilidad ni estadísticas: es difícil saber quién tiene un libro, qué préstamos están vencidos o qué libros son los más pedidos.]

---

## 3. Propósito y objetivos

**Objetivo general:**

Desarrollar un sistema web de control de stock que permita registrar, consultar y mantener actualizado el inventario de libros de la Biblioteca Municipal de Piribebuy, reemplazando el registro manual en tarjetas.

**Objetivos específicos:**

1- Registrar el catálogo de libros (alta, modificación y baja) con sus datos bibliográficos, de modo que cada tarjeta actual pueda cargarse en el sistema.
2- Controlar la cantidad de ejemplares de cada libro y su estado (disponible, prestado, dañado o perdido), mostrando el stock total y el disponible.
3- Permitir búsquedas por título, autor, categoría o código, con resultados en pocos segundos.
4- Registrar préstamos y devoluciones con fecha límite, guardando fecha, socio y ejemplar de cada movimiento.
5- Generar reportes básicos: inventario, préstamos vencidos y libros más solicitados.
6- Migrar al sistema la información existente en las tarjetas.
7- Restringir el acceso mediante usuarios y roles, de modo que solo personal autorizado modifique datos.

---

## 4. Alcance del proyecto

**Incluye (dentro del alcance):**

- [Funcionalidad / módulo 1]
- [Funcionalidad / módulo 2]

**No incluye (fuera de alcance):**

- [Aspecto explícitamente excluido 1]
- [Aspecto explícitamente excluido 2]

---

## 5. Interesados (stakeholders)

| Interesado | Descripción | Interés en el proyecto |
|---|---|---|
| [Usuario final] | [quién es] | [qué espera del sistema] |
| [Cliente] | [quién es] | [qué espera del sistema] |
| [Administrador del sistema] | [quién es] | [qué espera del sistema] |

---

## 6. Justificación / viabilidad

**Viabilidad técnica:** [¿el grupo cuenta con el conocimiento o puede adquirirlo?]

**Viabilidad operativa:** [¿el usuario/cliente podrá usar y mantener el sistema?]

**Viabilidad económica (alto nivel):** [¿es razonable en términos de costo/esfuerzo para el contexto del proyecto?]

---

## 7. Visión general de la solución

[Descripción breve, en lenguaje llano y sin detalle técnico, de cómo el grupo imagina que el sistema resolverá el problema planteado.]

---

## 8. Glosario de términos

| Término | Definición |
|---|---|
| [Término 1] | [definición en el contexto del negocio] |
| [Término 2] | [definición en el contexto del negocio] |
| [Término 3] | [definición en el contexto del negocio] |

---

## 9. Riesgos iniciales

| Riesgo | Impacto | Estrategia de mitigación |
|---|---|---|
| [ej. Baja disponibilidad del cliente para validaciones] | [Alto/Medio/Bajo] | [cómo se planea mitigar] |
| [Riesgo 2] | [Alto/Medio/Bajo] | [cómo se planea mitigar] |

---

## 10. Selección tecnológica preliminar

| Componente | Elección | Justificación breve |
|---|---|---|
| Lenguaje de programación | [ej. Python / Java / TypeScript] | [por qué] |
| Framework | [ej. Django / Spring Boot / React] | [por qué] |
| Base de datos | [ej. PostgreSQL / MongoDB] | [por qué] |

---

[← Volver al inicio](index.md) · [Siguiente: Análisis →](analisis.md)
