# BiblioStock — Trabajo Práctico Integrador


Este repositorio contiene el análisis y diseño del sistema **BiblioStock**, desarrollado como Trabajo Práctico Integrador de la asignatura **Ingeniería de Software**.

El sitio publicado en GitHub Pages es la entrega oficial del trabajo. **No se envían archivos impresos ni copias por otros medios.**

🔗 **Sitio publicado:** `https://[usuario-o-organizacion].github.io/[nombre-del-repositorio]/`

---

## Integrantes del grupo

| Nombre completo | Rol / Responsabilidad principal | Usuario de GitHub |
|---|---|---|
| Melisa Tillner | 	Coordinación y contacto con el cliente | [@melii18] |
| Marcelo Benitez | Análisis de requisitos y modelado | [@themarce001] |
| Cesar Pereira | 	Responsable técnico (repositorio y sitio) | [@by-rafael] |

## Usuario / cliente real

**Biblioteca Municipal de Piribebuy** — Institución pública que resguarda y ofrece libros a la comunidad. Actualmente no cuenta con ningún sistema informático y gestiona su acervo con registros en pequeñas tarjetas.

## Metodología de diseño y desarrollo elegida


**Design Thinking + UML, con iteraciones cortas y validación con el cliente.**

El grupo eligió combinar estas dos herramientas porque se complementan bien en un proyecto pequeño con un cliente real:

- **Design Thinking** guía la etapa inicial. Antes de definir qué construir, entendemos cómo trabaja hoy la Biblioteca Municipal de Piribebuy con sus tarjetas, qué dificultades tiene el personal y qué necesita realmente. Esto se hace con entrevistas y observación, y evita diseñar un sistema que no responda a su realidad.
- **UML** aporta un lenguaje estándar para modelar el sistema en las entregas de Análisis y Diseño (casos de uso, modelo de dominio, diagramas de clases y de secuencia). Así los requisitos y las decisiones técnicas quedan documentados de forma clara, trazable y entendible para cualquier lector.
- **Iteraciones cortas con validación:** cada entrega se revisa con el cliente antes de avanzar a la siguiente, lo que reduce el riesgo de malentendidos y permite corregir a tiempo.

Elegimos esta combinación porque el sistema tiene un alcance acotado, el equipo es de tres integrantes y el cliente es accesible. Una metodología más pesada, como RUP completo, exigiría más documentación y roles de los que el proyecto necesita. Además, el enfoque centrado en el usuario es clave en este caso: quienes usarán el sistema no tienen experiencia informática previa y hoy trabajan de forma totalmente manual.

---

## Entregas

| Entrega | Estado | Enlace |
|---|---|---|
| 1. Conceptualización | 🔲 Pendiente / ✅ Entregado | [Ver documento](docs/conceptualizacion.md) |
| 2. Análisis | 🔲 Pendiente / ✅ Entregado | [Ver documento](docs/analisis.md) |
| 3. Diseño | 🔲 Pendiente / ✅ Entregado | [Ver documento](docs/diseno.md) |

## Estructura del repositorio

```
/docs           → contenido publicado en GitHub Pages (este es el sitio oficial de entrega)
  ├─ index.md          → página principal del sitio
  ├─ conceptualizacion.md
  ├─ analisis.md
  └─ diseno.md
/diagramas      → imágenes o archivos fuente de los diagramas (UML, mockups, etc.)
/src            → código fuente, si el grupo decide avanzar con una implementación
```

## Cómo publicar este sitio en GitHub Pages

1. Suban este repositorio a GitHub (público, o privado con acceso otorgado a la cátedra).
2. Vayan a **Settings → Pages**.
3. En **Source**, seleccionen la rama `main` (o `master`) y la carpeta **/docs**.
4. Guarden. GitHub publicará el sitio en `https://[usuario].github.io/[repositorio]/` en unos minutos.
5. Verifiquen que `docs/index.md` se muestre correctamente como página principal.
6. Actualicen el enlace del sitio arriba en este README y entréguenlo a la cátedra antes de la fecha límite de cada entrega.

> 💡 Tip: cada vez que hagan `push` a la rama publicada, el sitio se actualiza automáticamente. No es necesario volver a configurar nada en las siguientes entregas.
