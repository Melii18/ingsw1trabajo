---
title: "Análisis"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 2 · Análisis

> *Qué debe hacer el sistema, desde la perspectiva del negocio y del usuario.*

> 📌 **Versión inicial.** Este análisis parte de la información relevada en la [Conceptualización](conceptualizacion.md). Los valores marcados como *(a validar)* se confirmarán con el cliente antes de pasar al Diseño.

---

## 1. Requisitos funcionales

| ID | Requisito | Prioridad |
|---|---|---|
| RF-01 | El sistema debe permitir que el personal autorizado inicie sesión con usuario y contraseña. | Alta |
| RF-02 | El sistema debe permitir registrar, modificar y dar de baja libros con sus datos bibliográficos (título, autor/es, editorial, año, ISBN opcional y categoría). | Alta |
| RF-03 | El sistema debe permitir registrar los ejemplares de cada libro con un código único y su ubicación en estantería. | Alta |
| RF-04 | El sistema debe permitir cambiar el estado de un ejemplar (disponible, prestado, dañado, perdido o dado de baja), registrando el motivo del cambio. | Alta |
| RF-05 | El sistema debe mostrar, para cada libro, el stock total y el stock disponible. | Alta |
| RF-06 | El sistema debe permitir buscar libros por título, autor, categoría, ISBN o código de ejemplar. | Alta |
| RF-07 | El sistema debe permitir registrar y modificar socios con sus datos básicos (CI, nombre, apellido, teléfono y dirección). | Alta |
| RF-08 | El sistema debe permitir registrar el préstamo de un ejemplar disponible a un socio, con fecha de préstamo y fecha límite de devolución. | Alta |
| RF-09 | El sistema debe permitir registrar la devolución de un ejemplar prestado y actualizar su estado. | Alta |
| RF-10 | El sistema debe permitir gestionar autores, editoriales y categorías. | Media |
| RF-11 | El sistema debe listar los préstamos vencidos (fecha límite superada sin devolución). | Media |
| RF-12 | El sistema debe generar reportes de inventario, préstamos vencidos y libros más solicitados en un período. | Media |
| RF-13 | El sistema debe permitir al administrador crear usuarios, asignarles un rol (administrador o bibliotecario) y desactivarlos. | Media |
| RF-14 | El sistema debe permitir la carga inicial del catálogo mediante un formulario de carga rápida o la importación desde una planilla. | Media |
| RF-15 | El sistema debe guardar el historial de movimientos de cada ejemplar (altas, préstamos, devoluciones y cambios de estado). | Baja |
| RF-16 | El sistema debe permitir al administrador generar una copia de respaldo de la información. | Baja |

---

## 2. Requisitos no funcionales

| ID | Requisito | Categoría |
|---|---|---|
| RNF-01 | La búsqueda de un libro debe mostrar resultados en menos de 2 segundos, con un catálogo de hasta 20.000 libros. | Rendimiento |
| RNF-02 | Las contraseñas deben almacenarse cifradas (hash) y la sesión debe cerrarse tras 30 minutos de inactividad. | Seguridad |
| RNF-03 | Cada usuario solo debe poder acceder a las funciones permitidas por su rol. | Seguridad |
| RNF-04 | Buscar un libro, registrar un préstamo y registrar una devolución deben poder hacerse en 3 pasos o menos, y un bibliotecario sin experiencia informática debe poder operarlos tras una capacitación de 1 hora. | Usabilidad |
| RNF-05 | El sistema debe funcionar en una sola PC o en la red local de la biblioteca, sin depender de una conexión a internet. | Disponibilidad |
| RNF-06 | El sistema debe generar al menos una copia de respaldo diaria de la base de datos. | Fiabilidad |
| RNF-07 | El sistema debe funcionar en las versiones actuales de Chrome, Firefox y Edge, sobre Windows o Linux. | Portabilidad |
| RNF-08 | El sistema debe desarrollarse con Java (JSP y Servlets, patrón MVC) y MySQL, según la selección tecnológica de la Entrega 1. | Mantenibilidad |
| RNF-09 | La interfaz y los mensajes del sistema deben estar en español. | Usabilidad |

---

## 3. Modelo de casos de uso

**Actores:**

- **Bibliotecario:** persona que atiende la biblioteca y opera el sistema a diario.
- **Administrador:** puede hacer todo lo que hace el bibliotecario y, además, gestiona usuarios y respaldos.

**Diagrama de casos de uso:**

![Diagrama de casos de uso](https://www.plantuml.com/plantuml/svg/VP8zRjj048NxFSL0QID3fFu3Gx0eM4RQ2ExSZ9TZUgFbBZ6pJ20aFapA5Abo15qi81d-W43IFUXzR_HsE7SIa4EPMz0eNgOfJKlnoj9BWE21JVOQ83LCEXZlb9oDAv0nXmBr6JCwXOibg6nqcQK18A-O-g_6PV22LePEAQHH2BufW0JrEMDVklJWhMTuTtz_N1oFbUCv9VxxwpnP9lkjUbEeWsUO9ERP6Xz88ni_0HH8MckVviOP2OofvzhQgprCl-yWKQeh2fEJaK0vGZFg5Bm-J-fARRt9uN4wY-2ZCzeWWv2OwszNJpmypg8n6SC3IRKaPB3ccRsqQ3n6vmEKFbDUM6II9tS1QMeqkVaujnZai0oUITu_EKfDy6pGai05D0RAF5z_OVV_Y_6SvM2EU6twgiinkeAa55trT43LaOJh3-iptmPMuy0QFb5Mhv-XuEjF2PXtz7fCRmPqIb-yBVLmoPinluK7SbJHJ8NdG5tpxGYDPeD7bb9MXrAlcBtjKj5id8hWW9mXzoy5Kn-0RIFZ3n_5WqvIe4tRvqQnUbCgWUbqrrnC9-DUpdkvwEMobwjUhdkvwUMsar5KNNeZPxsCbQh2S7FJ38GFS7jhdBPbIhjTvMt-uyt_vTsHIylSgZy0)

**Especificación de casos de uso principales:**

### CU-01 · Iniciar sesión

- **Actor(es):** Bibliotecario, Administrador
- **Precondición:** El usuario está registrado y activo en el sistema.
- **Flujo principal:**
  1. El usuario ingresa su nombre de usuario y contraseña.
  2. El sistema valida los datos.
  3. El sistema muestra la pantalla principal con las opciones de su rol.
- **Flujos alternativos:**
  - 2a. Los datos son incorrectos: el sistema muestra un mensaje de error y permite reintentar.
  - 2b. El usuario está desactivado: el sistema informa que debe comunicarse con el administrador.
- **Postcondición:** El usuario tiene una sesión iniciada.

### CU-03 · Gestionar ejemplares y stock

- **Actor(es):** Bibliotecario
- **Precondición:** Sesión iniciada; el libro existe en el catálogo.
- **Flujo principal:**
  1. El bibliotecario busca el libro (CU-06) y abre su ficha.
  2. El sistema muestra los ejemplares del libro con su ubicación, su estado, el stock total y el stock disponible.
  3. El bibliotecario elige "Agregar ejemplar" e ingresa la ubicación.
  4. El sistema genera el código del ejemplar, lo registra como DISPONIBLE y actualiza el stock.
- **Flujos alternativos:**
  - 3a. Cambiar estado: el bibliotecario selecciona un ejemplar, elige el nuevo estado (dañado, perdido o dado de baja) y escribe el motivo; el sistema registra el movimiento y actualiza el stock disponible.
  - 3b. El ejemplar está prestado: el sistema no permite darlo de baja hasta su devolución, salvo que se declare PERDIDO.
- **Postcondición:** Los ejemplares y el stock del libro quedan actualizados, y el cambio queda en el historial.

### CU-06 · Buscar en el catálogo

- **Actor(es):** Bibliotecario
- **Precondición:** Sesión iniciada.
- **Flujo principal:**
  1. El bibliotecario elige el criterio (título, autor, categoría, ISBN o código) y escribe el texto a buscar.
  2. El sistema muestra los libros que coinciden, con su stock total y disponible.
  3. El bibliotecario selecciona un libro para ver su ficha.
- **Flujos alternativos:**
  - 2a. No hay resultados: el sistema lo informa y ofrece registrar un libro nuevo.
- **Postcondición:** No modifica datos.

### CU-07 · Registrar préstamo

- **Actor(es):** Bibliotecario
- **Precondición:** Sesión iniciada; el socio está registrado.
- **Flujo principal:**
  1. El bibliotecario busca al socio por CI o nombre.
  2. El sistema muestra los datos del socio y sus préstamos activos.
  3. El bibliotecario busca el libro (CU-06) y selecciona un ejemplar disponible.
  4. El sistema propone la fecha límite según el plazo por defecto.
  5. El bibliotecario confirma el préstamo.
  6. El sistema registra el préstamo, marca el ejemplar como PRESTADO y muestra el comprobante.
- **Flujos alternativos:**
  - 2a. El socio tiene préstamos vencidos o llegó al máximo permitido: el sistema avisa y no permite continuar.
  - 3a. No hay ejemplares disponibles: el sistema lo informa y el caso de uso termina.
  - 4a. El bibliotecario modifica la fecha límite antes de confirmar.
- **Postcondición:** El préstamo queda registrado y el stock disponible del libro baja en uno.

### CU-08 · Registrar devolución

- **Actor(es):** Bibliotecario
- **Precondición:** Sesión iniciada; existe un préstamo activo del ejemplar.
- **Flujo principal:**
  1. El bibliotecario busca el ejemplar por su código o al socio.
  2. El sistema muestra el préstamo activo.
  3. El bibliotecario confirma la devolución.
  4. El sistema registra la fecha de devolución y marca el ejemplar como DISPONIBLE.
- **Flujos alternativos:**
  - 3a. El ejemplar vuelve dañado: el bibliotecario indica el estado DAÑADO y el motivo; el sistema lo registra y el ejemplar no vuelve al stock disponible.
  - 4a. La devolución está fuera de plazo: el sistema deja constancia del atraso en el historial del socio.
- **Postcondición:** El préstamo queda cerrado y el estado del ejemplar, actualizado.

---

## 4. Modelo de dominio

**Diagrama de clases conceptual:**

![Modelo de dominio](https://www.plantuml.com/plantuml/svg/TL5DRzim3BthLn3UhK221TiEyo5eqYMd3YWmx3Ji84kCpLKI3KhEW0tzxuFy5HVrRYBVu-CJttrCMbBd7NYsw7XZsLCWLWrP18-fOHk7mf0OXoe-KsYrQ0-nqPP_KwZXebrS8iRf68_QFDV2NR0Fx5ZWtUbq_dW-lw6nM9IHyk7uwNZuh5IFm2DLml1N0IHAdMC5GB4AyEFzThlxgG1q87xgAaT66-AW02n68zJsrSieS-WIIoyJs5U2Ct2ob5X8kpNmGIUiCxew-Gjzw_IWQjXIdSrrrSq8ngHjRbxGDFhWafw7lx6XuLk6Rj80kaNdg1zAwF328Jyj2PfHzAtMa-H5Vf3huQaprO_aAU5KVS4hkoxBJLUSbBx7JileQx0qTfOMXTqyy9Mlv0b3MYpleshpYET4LrOlIWqf5hljzgw0pMPw3QcKq0UM65eMs4_aaPaT5ekOIcY7jEqwVrSiOYkXHKaOq23e6tMtD37dM48Y30XxDRScvbrnkt894Q7jAy00UpLakKuLJ2HvytJQ_z5gYgadhkrUdBc4Xk9uYbNLLrn1xUXFbht7O3llr3y0)

- **Libro:** la obra (título y autor), sin importar cuántas copias haya. Puede no tener ISBN si es antiguo.
- **Ejemplar:** cada copia física de un libro, con su código, ubicación y estado (disponible, prestado, dañado, perdido o dado de baja). El stock de un libro es la cantidad de sus ejemplares.
- **Autor, Editorial y Categoría:** datos que clasifican y describen a cada libro.
- **Socio:** persona registrada que puede retirar libros en préstamo.
- **Préstamo:** entrega temporal de un ejemplar a un socio, con fecha límite y fecha de devolución.
- **Usuario:** persona del personal que usa el sistema, con rol de administrador o bibliotecario.
- **Movimiento:** registro de cada cambio en un ejemplar (alta, cambio de estado o baja), para mantener el historial.

Los términos coinciden con el [glosario de la Conceptualización](conceptualizacion.md).

---

## 5. Diagramas de comportamiento

**Diagrama de secuencia — Registrar préstamo (CU-07):**

![Diagrama de secuencia: registrar préstamo](https://www.plantuml.com/plantuml/svg/NP4zRbj138JxFSN0bGn45r1Xs98T85KClvHk-7OfYVRkyeNSfq2vKGfNEO8k5kWdaPHwFd8umtjlP6qi6Svnv1g5feEnDoeQ_5tgG4O5lgQaFwIkiAJiVAdmz_qOFvCrYJ9GRHXhOijI-KHJR6gOIvz56qSoKP1Z7eQBePjEl76Xrte4kwRn_MRFTI7CCRr3XndceqSok4PHJ1PVeAXQUkFRq64wlSCSCpnIKqVYVEAs66ptwv39GR79HZrGRkWESjHw2MpsBIHrABY2C_BkeqZZ09mj7ZRYEaDL32CdXd4J8qCTUQEEBBsf1yxE9vCrzPAbKT80_1_dW6FITXzjpFe9DEuBKyJTxoGhlRsoVdhZCcGoTcpX8_RFkjxQSUOOHIiP-4GZYGzQfS_NGJvpNDFVYF1nnIQ9C1ao_LGCQaYyvDWEH_npM6XTYXMoSt77hKVvXLVYpIvbR5zh8OkN9qKjYkUNf-xRm-FNgwiMMWRJdchZmn_FBbnJkEUQnfB37m00)

Muestra el intercambio entre el bibliotecario y el sistema al prestar un libro: primero se verifica que el socio esté habilitado y luego se elige un ejemplar disponible. Al confirmar, el sistema registra el préstamo y cambia el estado del ejemplar.

**Diagrama de actividad — Registrar devolución (CU-08):**

![Diagrama de actividad: registrar devolución](https://www.plantuml.com/plantuml/svg/TL4nJWD13Ept5IwJWW-G0eX2WOG0AMqQPzUN67Rjqthl4Fo29r1IfCe3aBYFeRia2W7HsZFZySob5SobIH7G5suvO3WBr6fiFAiuUsAfCMC2MsFGPvOLL1YDtC1pvrDUHjP27ZChB1lp21I17YdL4VD2HhxR1bxf6BHVc7hMYJkVinLA2AaXAtdWrBdxi899TrPwrAbwffPj9sy5WqBLROozGlXnSUAuWj7Nv_LnrCExTo21PKEo9r-CeQn9O6JTPkm0Zeumd_u0NfF2x6R-S7ztCxszdZYAHZ0I7NYd7ba2UuJPLVTsDRjVo0kG-SnBwXMJxlxwSItJYWy196qvCKdHdlUVZvton944hjnVeOXGaLyZ1893azrM3hdCzzEMkorK3UK1M4Ty_J-IG8y8NiKAYcSSyiQIqNGXVQ0Hrcn5CsCSTlkIZp7zydeeFGwg5UU4UuzMj7QN9A59qNq3)

Describe los pasos de una devolución, incluyendo qué pasa si el ejemplar vuelve dañado o fuera de plazo.

---

## 6. Prototipo de interfaz (mockups)

**Pantalla — Buscar en el catálogo:**

![Mockup: buscar en el catálogo](https://www.plantuml.com/plantuml/svg/RL9DIoj14BplhoZqfXWIFouIWnf11HL9H11HwDrju-1aU-sP4TJnntZqu47UJzW_zfXTatTvSwgUwQfggcVVULBlo7hCfNWAzKOUt7FWahBtzGnuNyDfPGeZY1YJRpwjp1A-rERBUPgBGyHK2jE22TUYdjixiaRnaG5xUnamp4U7mHMau0fiKIoqaWUwfrr4h8mDLw3cHnnAXXFB9PLepmeYxg-QRn-it2FYjgFTjIwz9BIQfRvXFXetVqhJ3ZhCHx-KhZW8NhI3O_8y4ss-gQkdNegd3XuPLqjbSikkbJpRwFS7coc3_uuNSTp3CMcHjCwRJtqE_8Q82tbXczIt4B6vLDhUGSIDf1oceLQUfzaEUfW8uP2SRxDSSfDjVy4Tz0U8E37EYnf2oHQNf3GBz8g8Qz9k4Sk6YDG_oF0l9DnUi-B158zqbrAy2FmYi2PNQUi9puppIefwiUGKyKUsprMPVahs5m00)

Pantalla principal de trabajo. El bibliotecario escribe lo que busca, elige el criterio y ve al instante cuántos ejemplares hay y cuántos están disponibles.

**Pantalla — Registrar préstamo:**

![Mockup: registrar préstamo](https://www.plantuml.com/plantuml/svg/RP7DJi9058NtVOgJhb03j0KnCMAGYaaJWWIMnCLbEk9essbc1XUsF8nB5ooCZz0NCzEAmSJTpUGxF_VEI1jIHbDYa4hsiitRkUBQK2gTuim1YbD4cM12eaH8fdfFvCRESrLzr9X6YQLaeXuMF9VAyFgD4g6mSu3Xq06krjSBlX7QA5B83s87wDYGnW6jC3gvH0ctt_63NgT_FW3WeiHglDMCr4FjLs0cqxNYbhp926EULNl3t_ws8cR4gzGMyX5pz6fjapPvvccUa4ABLL-nsCWcTThsF3zeUy7_gLEnLjA2eU0PgFgKsXfhcV2OOfIOQ4DnJTn6o_dzB1fF9qUfTvmzaLNyhczHxwBhUzt02mO_CGsMLFjKc7f7r-yV4FV8RXLIndXY-vLOXJ9x52ezFgxjlND6F8ljzphV)

En una sola pantalla se identifica al socio, se elige el ejemplar y se confirma el préstamo, con la fecha límite ya sugerida.

**Pantalla — Ficha del libro:**

![Mockup: ficha del libro](https://www.plantuml.com/plantuml/svg/VLBBJXin5DtFLnp11Wgfyf2AYaB4C0nH91eGGrS8f3kscneyuzJsi6Wc7yEoYomGd-0Vg-oXYx3eNLqVdtFkmpwrZeopf1mgpPwQPU-7P3-ffsHfTB8wI83L9yngoQH6YuoSVr5w4V9hu_zOHvMsQ55e9cDo8vRQE14nKj9WdG0d9mamBYSNmHjSA7J-m0gtVkCQfO_HOYUJeWRvLst11QnMWXF7U-n4gnNInccp9-n-b4ofD58eJCamlo5yyo_cLoD-RsjoBfqsabJGF1GDfqeOoQYc1xH8_MjNV_3roz4_IKPEBBJn6ugQkNuMAh9dnTayil4XEkNdRjJyKLHBHKPOx5cdsHESTg7-w11SsgMkPQc4FSPmFvJRJOB3k9na_etBkDznEVbUIaPC-hUwE-VM4TUHUjdhzmV3Nd-05W6kdK0w2izoanUtwVdL5cluaNK-AwwlvhEpotoBD_elhrlCNRemOa46udt4UxIuowWgPG1ZYn6QDcGu6R1mfUqzriawEHKr3zyj-Gi0)

Muestra los datos del libro y la lista de sus ejemplares con su estado. Desde aquí se agregan ejemplares o se cambia su estado.

---

## 7. Reglas del negocio

| ID | Regla |
|---|---|
| RN-01 | Solo se pueden prestar ejemplares en estado DISPONIBLE. |
| RN-02 | Un socio puede tener como máximo 3 ejemplares prestados al mismo tiempo *(a validar)*. |
| RN-03 | El plazo de préstamo por defecto es de 7 días; el bibliotecario puede modificarlo al registrar el préstamo *(a validar)*. |
| RN-04 | Un socio con préstamos vencidos no puede retirar nuevos libros hasta devolverlos. |
| RN-05 | Cada ejemplar tiene un código único. Un libro puede registrarse sin ISBN. |
| RN-06 | Para registrar un libro son obligatorios el título, al menos un autor y la categoría; el resto de los datos pueden quedar pendientes. |
| RN-07 | Los libros y ejemplares no se eliminan: se dan de baja, para conservar el historial. |
| RN-08 | Toda baja o cambio de estado de un ejemplar debe registrar un motivo (pérdida, deterioro o donación). |
| RN-09 | Un ejemplar prestado no puede darse de baja hasta su devolución, salvo que se declare PERDIDO. |
| RN-10 | Solo el administrador puede gestionar usuarios y generar respaldos. |
| RN-11 | El sistema no calcula multas por atraso (fuera de alcance); solo deja constancia del atraso. |

---

## 8. Matriz de trazabilidad

| Requisito | Caso(s) de uso relacionado(s) |
|---|---|
| RF-01 | CU-01 |
| RF-02 | CU-02 |
| RF-03 | CU-03 |
| RF-04 | CU-03 |
| RF-05 | CU-03, CU-06 |
| RF-06 | CU-06 |
| RF-07 | CU-05 |
| RF-08 | CU-07 |
| RF-09 | CU-08 |
| RF-10 | CU-04 |
| RF-11 | CU-09 |
| RF-12 | CU-09 |
| RF-13 | CU-10 |
| RF-14 | CU-11 |
| RF-15 | CU-03, CU-07, CU-08 |
| RF-16 | CU-12 |

Las fuentes editables de todos los diagramas están en [`diagramas/analisis.puml`](https://github.com/Melii18/ingsw1trabajo/blob/main/diagramas/analisis.puml).

---

[← Anterior: Conceptualización](conceptualizacion.md) · [Siguiente: Diseño →](diseno.md)
