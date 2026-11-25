# LuthierDesk

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5-6DB33F)
![Spring Security](https://img.shields.io/badge/Spring_Security-JWT-6DB33F)
![Status](https://img.shields.io/badge/Status-In_Development-yellow)
![Sprint](https://img.shields.io/badge/Sprint-1-blue)

LuthierDesk es una aplicación desarrollada con **Java** y **Spring Boot** para organizar un taller de lutheria: desde el catálogo de tareas con sus precios hasta la factura final, pasando por clientes, instrumentos, presupuestos, hojas de taller y la planificación del trabajo (qué cliente es el siguiente y cuánto tiempo de espera hay).

Es un **proyecto de práctica**: sirve para reforzar Spring Boot repitiendo lo aprendido sobre un dominio con reglas de negocio reales. No está pensado para desplegarse ni para usarse como producto.

---

## Estado del proyecto

🚧 En desarrollo

El proyecto está en el **Sprint 1**: base del proyecto y seguridad de la API (usuarios, login y JWT).

### Implementado hasta ahora

- Esqueleto del proyecto: `pom.xml`, Maven wrapper y estructura inicial.

### Alcance de la v1

- Seguridad con Spring Security: JWT para la API y formulario con sesión para las pantallas.
- Clientes e instrumentos.
- Catálogo de tareas con precios y tiempos estimados.
- Expedientes (recepción del instrumento y estados).
- Presupuestos.
- Hoja de taller.
- Cola de trabajo y calendario de carga, con fechas estimadas.
- Facturación (numeración correlativa, facturas inmutables y rectificativas).

---

## Tecnologías

- Java 21
- Spring Boot 3.5
- Spring Security (JWT con jjwt)
- Spring Data JPA
- Bean Validation
- Thymeleaf
- H2 Database
- springdoc-openapi (Swagger)
- JUnit, Mockito y MockMvc para las pruebas

---

## Arquitectura

El proyecto sigue una arquitectura sencilla por capas:

```
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

Además utiliza DTO, Mapper manual, Entity y excepciones personalizadas.

Hay dos cadenas de seguridad: JWT sin estado para `/api/**` y formulario de login con sesión para las pantallas Thymeleaf.

---

## Ejecución

Requisitos: **Java 21**. No hace falta instalar Maven, porque el proyecto incluye el wrapper.

Compilar y verificar:

```bash
./mvnw clean verify
```

Las instrucciones para ejecutar la aplicación (perfiles y `JWT_SECRET`) se añadirán cuando existan.

---

## Roadmap

- 🔄 Sprint 1 - Base del proyecto y seguridad de la API
- ⏳ Sprint 2 - Autorización, respuestas 401/403, seguridad de las pantallas y tests de seguridad
- ⏳ Sprint 3 - Clientes e instrumentos
- ⏳ Sprint 4 - Catálogo de tareas, precios y tiempos
- ⏳ Sprint 5 - Expedientes
- ⏳ Sprint 6 - Presupuestos
- ⏳ Sprint 7 - Hoja de taller
- ⏳ Sprint 8 - Cola de trabajo
- ⏳ Sprint 9 - Capacidad, calendario y planificación
- ⏳ Sprint 10 - Facturación

---

## Después de la v1

- PDF y envío por email de presupuestos y facturas.
- Fotos del instrumento.
- Histórico de precios.
- Vista de calendario por semana y mes.
- Acceso de clientes con login propio.
- Cambio y recuperación de contraseña.