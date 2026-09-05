# Capítulo I: Introducción

## 1.1 Startup Profile

### 1.1.1 Descripción de la Startup

**F1nTrack** es una startup de Ingeniería de Software (UPC) orientada a diseñar y construir plataformas digitales de **alta complejidad arquitectónica** para el ciudadano peruano. Su producto principal, **KapakID**, no es un simple CRUD de documentos: es una plataforma de **identidad digital + pagos integrados + trazabilidad**, pensada para interoperar con entidades reales del ecosistema nacional.

#### ¿Por qué nace F1nTrack / KapakID?

En el Perú, las personas manejan identidades y medios de pago **dispersos**:

- Documentos físicos: DNI, carné universitario, licencia, certificados.
- Tarjetas físicas: Metropolitano, Lima Pass, bancos, fidelización.
- Apps fragmentadas: Yape, Plin, banca móvil, sistemas por servicio.

No existe una plataforma única, segura e interoperable que permita **centralizar identidad digital**, **pagar lo cotidiano** y **auditar cada operación** bajo marcos normativos (SUNAT, SBS, Ley N° 29733).

#### Qué propone la startup

KapakID propone un ecosistema digital que:

| Capacidad | Qué resuelve |
| :--- | :--- |
| **Identidad digital verificable** | Registro y validación con RENIEC / biometría |
| **Documentos digitalizados** | Carga, QR por documento, reducción de físicos |
| **Pagos cotidianos** | Transporte, bancos, comercios (QR / NFC) |
| **Trazabilidad y auditoría** | Historial completo de transacciones y documentos |
| **Cumplimiento normativo** | Alineación con SUNAT, SBS y protección de datos |
| **Perfiles familiares** | Padres/tutores gestionan documentos de dependientes |

#### Misión, visión y valores

| Misión | Visión | Valores |
| :--- | :--- | :--- |
| Ofrecer una plataforma confiable que centralice la identidad digital y los pagos cotidianos del ciudadano, con trazabilidad y cumplimiento normativo. | Ser la referencia en Latinoamérica en identidad digital interoperable y pagos integrados, con arquitectura robusta (microservicios, DDD, ADD). | Seguridad, interoperabilidad, transparencia, innovación y compromiso con el usuario. |

#### Objetivos estratégicos (visión de producto)

| ID | Objetivo | KPI orientativo |
| :--- | :--- | :--- |
| **O-01** | Centralizar la identidad digital en una sola plataforma | % usuarios con documentos verificados (meta: 80%) |
| **O-02** | Facilitar pagos cotidianos (transporte, bancos, comercios) | Transacciones mensuales por usuario |
| **O-03** | Garantizar trazabilidad y auditoría de operaciones | % transacciones con registro completo (meta: 100%) |
| **O-04** | Cumplir normativas de seguridad y regulación | Observaciones regulatorias (meta: 0) |
| **O-05** | Reducir uso de documentos/tarjetas físicas | % reducción de soporte físico |

> **Nota (alcance del informe):** en el Capítulo I se define el *por qué* y el *para quién*. El detalle de módulos (M-01…M-06), patrones y despliegue se profundizará en entregas posteriores de arquitectura; aquí se introduce solo la visión necesaria para el Solution Profile y Lean UX.

### 1.1.2 Perfiles de integrantes del equipo

| Integrante | Perfil |
| :--- | :--- |
| **Giussepe Taquiri** | Estudiante de Ingeniería de Software (UPC). Interés en arquitectura de software, diseño de sistemas y buenas prácticas. Aporta análisis estructurado y alineación del Startup Profile con los objetivos del curso de **Fundamentos de Arquitectura de Software**. |
| **Diego Mora Blas** | Estudiante de Ingeniería de Software (UPC). Enfoque en requisitos, modelado de problemas y soluciones centradas en el usuario. Aporta investigación, 5W+2H y articulación de objetivos/restricciones del Solution Profile. |
| **Dhilsen Mallqui Vilca** | Estudiante de Ingeniería de Software (UPC). Gestión de entregables, control de versiones y organización del informe. Aporta flujo Git (`feature` → `develop` → `main`), Conventional Commits y trazabilidad del repositorio. |
| **Raul Hiroshi Tasayco Osorio** (U202319415) <br><img src="../assets/cap-1/Members/Image_raul_tasayco.jpeg" alt="Raul Hiroshi Tasayco Osorio" width="100"> | Estudiante de Ingeniería de Software (UPC). Experiencia en C++, Python, SQL, Angular/Vue, HTML/CSS/TS. Aporta Lean UX Process, segmentos objetivo e interfaces de usuario para KapakID. |

---

## 1.2 Solution Profile

### 1.2.1 Nombre del producto

**KapakID** — plataforma de **identidad digital verificable, gestión de documentos y pagos integrados** para el ciudadano peruano, con trazabilidad de operaciones e interoperabilidad hacia entidades externas (RENIEC, SUNAT, Metropolitano/Lima Pass, bancos, SBS, comercios/POS).

### 1.2.2 Antecedentes y problemática

#### Contexto

Hoy el ciudadano combina billetera física, apps bancarias, tarjetas de transporte y documentos en papel o fotos sueltas. Esa fragmentación genera fricción diaria, riesgo de pérdida, falta de historial unificado y dificultad para cumplir o demostrar identidad/pagos cuando se requiere.

#### Problema central

**No existe una plataforma única, integrada y segura** que permita:

1. Centralizar identidad digital (documentos verificables).
2. Pagar servicios cotidianos (transporte, bancos, comercios).
3. Tener trazabilidad de transacciones y documentos.
4. Cumplir normativas (SUNAT, SBS, protección de datos).

#### Objetivos del producto (alcance inicial)

- Verificar identidad (RENIEC / biometría) y digitalizar documentos con QR.
- Habilitar pagos y recargas (transporte, banca, comercios) desde un solo lugar.
- Registrar auditoría de operaciones y notificar vencimientos.
- Soportar perfiles familiares (padres/tutores).

#### Restricciones

- Foco inicial: Lima Metropolitana (estudiantes y familias).
- Integraciones externas se introducen de forma evolutiva (no todas en el primer sprint de producto).
- Cumplimiento de Ley N° 29733 (protección de datos personales) como restricción de diseño.
- El informe Avance 1 cubre **Capítulos I–III** (introducción, análisis y especificación); la arquitectura detallada (C4, ADD, despliegue) se documentará en fases posteriores del curso.

#### 5 “W”s + 2 “H”

- **WHAT:** Fragmentación de identidad digital y medios de pago; documentos/tarjetas físicos sin trazabilidad unificada.
- **WHEN:** De forma cotidiana (transporte, pagos, trámites) y en picos críticos (vencimientos, emergencias, renovaciones).
- **WHERE:** Perú, con foco en Lima Metropolitana (transporte masivo, banca retail, trámites ciudadanos).
- **WHO:** Ciudadanos, especialmente estudiantes universitarios (18–29) y padres/madres o tutores (25–45); también comercios afiliados como actores del ecosistema de pagos.
- **WHY:** No hay una solución local accesible que combine identidad + pagos + auditoría + cumplimiento normativo.
- **HOW:** Plataforma digital (móvil/web) con API Gateway y módulos de Identidad, Documentos, Pagos, Auditoría, Notificaciones e Integraciones Externas.
- **HOW MUCH:** El costo de oportunidad del tiempo perdido, riesgo de pérdida y herramientas empresariales inaccesibles supera el valor de una solución ciudadana integrada.

#### Visión de módulos (contexto para el Solution Profile)

KapakID se concibe con seis módulos lógicos (microservicios) detrás de un API Gateway:

| Módulo | Nombre | Rol |
| :--- | :--- | :--- |
| **M-01** | Identidad Digital | Usuarios, RENIEC, biometría |
| **M-02** | Documentos y Perfiles | Digitalización, QR, perfiles familiares |
| **M-03** | Pagos | Recargas, transporte, P2P, comercios |
| **M-04** | Auditoría | Eventos, historial, reportes |
| **M-05** | Notificaciones | Vencimientos, confirmaciones |
| **M-06** | Integraciones Externas | RENIEC, SUNAT, Metropolitano/Lima Pass, Bancos, SBS, POS |

```text
                 API GATEWAY
                      |
     +--------+-------+-------+--------+
     |        |       |       |        |
   M-01     M-02    M-03    M-04     ...
 Identidad Documentos Pagos Auditoría
     |        |       |
   M-05     M-06 <----+
 Notif.   Integraciones → RENIEC · SUNAT · Transporte · Bancos · SBS · POS
```

#### Integraciones externas previstas

| Entidad | Para qué |
| :--- | :--- |
| **RENIEC** | Validación de DNI, identidad digital, biometría |
| **SUNAT** | Validación RUC / cumplimiento tributario |
| **Metropolitano / Lima Pass** | Recargas, validación, historial de viajes (NFC/QR) |
| **Bancos** | Transferencias, depósitos, Yape/Plin |
| **SBS** | Cumplimiento y reportes financieros |
| **Comercios / POS** | Pagos QR/NFC |
| **IoT (NFC / biometría)** | Lectura de tarjetas y autenticación en dispositivo |

### 1.2.3 Lean UX Process

#### 1.2.3.1 Lean UX Problem Statement

**Domain:** Identidad digital ciudadana, documentos personales y pagos cotidianos en Perú.

**Customer segments (iniciales):** Estudiantes universitarios (18–29) y padres/madres o tutores (25–45) en Lima Metropolitana.

**Pain points:** Documentos y tarjetas físicas dispersas; apps fragmentadas; riesgo de pérdida; sin historial unificado; vencimientos sin aviso; fricción en transporte y pagos.

**Gap:** No hay una plataforma local que integre identidad verificable + documentos + pagos + auditoría + notificaciones con interoperabilidad hacia RENIEC, transporte y banca.

**Visión / strategy:** Posicionar KapakID como la capa digital que unifica identidad y pagos del ciudadano, con arquitectura preparada para crecer (microservicios, trazabilidad, cumplimiento).

**Initial segment:** Estudiantes universitarios en Lima Metropolitana.

---

Actualmente, las personas enfrentan dificultades para gestionar documentos personales y medios de pago (DNI, carnés, licencias, Metropolitano/Lima Pass, tarjetas bancarias) porque todo está fragmentado entre físico y múltiples apps. Eso genera pérdida de tiempo, riesgo de extravío, falta de trazabilidad y estrés en trámites o pagos cotidianos.

Consideramos que estos usuarios necesitan una solución integral y segura que centralice identidad digital, documentos y pagos desde el celular. KapakID resuelve esto con registro/verificación de identidad, digitalización de documentos, pagos/recargas, notificaciones de vencimiento, perfiles familiares y base para integraciones con entidades externas. Sabremos que tenemos éxito cuando en los primeros tres meses aumente la proporción de documentos verificados digitalmente, crezca el uso de pagos/recargas en la app y mejore la satisfacción reportada en la gestión diaria.

#### 1.2.3.2 Lean UX Assumptions

##### Business Outcomes

- Crecimiento de usuarios con **identidad verificada** (O-01).
- Aumento de **transacciones mensuales** por usuario (transporte, recargas, pagos) (O-02).
- **Retención** por valor diario (dashboard + alertas + historial).
- Ingresos por **plan premium** (perfiles múltiples / familia).
- Reducción de churn mediante notificaciones útiles y modo de acceso confiable a documentos.
- Cumplimiento percibido: menos fricción normativa y mayor confianza (O-04).
- Adopción de funciones de digitalización y QR (O-05).

##### User Outcomes

- Control de identidad y documentos en un solo lugar.
- Menos dependencia de billetera/tarjetas físicas.
- Pagos de transporte y servicios más rápidos.
- Menos estrés por vencimientos (alertas).
- Organización familiar con perfiles múltiples.
- Confianza por trazabilidad (historial de operaciones).
- Experiencia simple pese a la complejidad del ecosistema (RENIEC, banca, transporte).

#### 1.2.3.3 Lean UX Hypothesis

Creemos que **centralizar identidad digital verificada + documentos en KapakID** reducirá la dependencia de documentos físicos.

Sabremos que es cierto cuando los usuarios reporten menor uso de billetera física para trámites cotidianos en el primer mes.

---

Creemos que **integrar pagos/recargas de transporte y servicios** aumentará la frecuencia de uso diario.

Sabremos que es cierto cuando al menos el 40% de usuarios activos realice ≥1 pago o recarga en 30 días.

---

Creemos que las **notificaciones de vencimiento** reducirán olvidos y estrés documental.

Sabremos que es cierto cuando ≥90% de quienes reciban alerta de vencimiento inicien la gestión desde la app.

---

Creemos que el **plan premium de perfiles familiares** motivará la conversión de prueba a pago.

Sabremos que es cierto cuando ≥10% de usuarios en trial premium conviertan en el primer mes.

---

Creemos que la **trazabilidad (historial de transacciones/documentos)** aumentará la confianza y retención.

Sabremos que es cierto cuando ≥60% de usuarios activos consulte el historial al menos una vez por semana.

---

Creemos que una **UX simple** permitirá adoptar KapakID sin soporte intensivo, pese a las integraciones complejas.

Sabremos que es cierto cuando el 85% de usuarios nuevos complete perfil y registre ≥3 documentos en la primera semana sin ticket de soporte.

#### 1.2.3.4 Lean UX Canvas

![Lean UX Canvas](../assets/cap-1/LeanUX/Lean%20UX%20Canvas.png)

> El canvas se irá actualizando si el docente pide alinear hipótesis a los objetivos O-01…O-05 y a las integraciones (RENIEC, transporte, banca).

---

## 1.3 Segmentos objetivo

KapakID prioriza dos segmentos iniciales alineados al dominio (identidad + pagos cotidianos + familia):

### Estudiantes Universitarios (18–29)

Buscan conveniencia: menos tarjetas físicas (universidad, transporte, débito) y pagos rápidos. KapakID les ofrece identidad/documentos centralizados, recargas de transporte y alertas de vencimiento.

| Variable | Descripción |
| :--- | :--- |
| Edad | 18–29 |
| Ocupación | Estudiantes universitarios |
| Ubicación | Lima Metropolitana (foco inicial) |
| Dispositivo | Smartphone como canal principal |
| Motivadores | Rapidez, movilidad, menos fricción en transporte y trámites |

### Padres/Madres o Tutores (25–45)

Buscan organización y control familiar: documentos de hijos (carnés, vacunas, permisos) y pagos del hogar. KapakID les ofrece perfiles múltiples, trazabilidad y notificaciones.

| Variable | Descripción |
| :--- | :--- |
| Edad | 25–45 |
| Rol | Padres, madres o tutores |
| Ubicación | Lima Metropolitana (foco inicial) |
| Necesidad clave | Múltiples perfiles / documentos familiares |
| Motivadores | Organización, seguridad, recordatorios, historial |

---

*Fin del Capítulo I. El Capítulo II (Requirements & Analysis) y el Capítulo III (Requirements Specification) se trabajarán en `feature/chapter-2` y `feature/chapter-3`.*
