# Capítulo III: Requirements Specification

Este capítulo traduce el análisis del Cap. II en **especificación de requisitos** de KapakID (Avance 1): escenarios To-Be, User Stories, Impact Map y Product Backlog. Se alinea a O-01…O-05, procesos P-01…P-06 y módulos M-01…M-06 de la visión FAS (identidad + pagos + trazabilidad + integraciones).

> **Pendientes globales (completar en iteraciones de campo / herramientas)**  
> - Completar **≥2 entrevistas** adicionales del segmento padres/tutores (meta 3–5). Ver Cap. II §2.2.2.  
> - Capturas formales To-Be en herramienta indicada por el docente (hoy hay mapeo textual + contraste As-Is).  
> - Actualizar imagen de Product Backlog en Jira cuando el board oficial esté creado.

---

## 3.1 To-Be Scenario Mapping

Se parte de los **As-Is** del Cap. II y se diseña el escenario deseado con KapakID (fases *Doing / Thinking / Feeling*), resaltando cambios que aporta la solución.

### 3.1.1 To-Be — Estudiante universitario (“Luis”)

| Fase | Doing (con KapakID) | Thinking | Feeling | Cambio vs As-Is |
| :--- | :--- | :--- | :--- | :--- |
| Salida de casa | Abre KapakID; DNI/carné digital y saldo transporte visibles | “Todo está en una sola app” | Tranquilo | Menos tarjetas físicas |
| Transporte | Paga/recarga con QR/NFC o saldo en app | “No haré cola en el módulo” | Aliviado | Elimina fricción de recarga física |
| Control / acceso | Muestra documento verificado (incluso offline si ya se cacheó) | “Tengo respaldo si olvidé el físico” | Seguro | Reduce riesgo de pérdida |
| Pagos cotidianos | Usa historial y métodos vinculados | “Queda registrado” | En control | Trazabilidad (M-04) |
| Cierre del día | Recibe alerta de saldo bajo / vencimiento | “Me avisan a tiempo” | Prevenido | Notificaciones (M-05) |

**Blank area a validar en campo:** adopción real de NFC en estaciones y latencia percibida (&lt; 2 s como atributo de calidad).

### 3.1.2 To-Be — Madre/padre o tutor (“Patricia”)

| Fase | Doing (con KapakID) | Thinking | Feeling | Cambio vs As-Is |
| :--- | :--- | :--- | :--- | :--- |
| Organización familiar | Cambia entre perfiles (hijos / dependientes) | “Veo documentos de todos” | Ordenada | Multi-perfil (P-06) |
| Vencimientos | Configura alertas por perfil/documento | “No se me pasan fechas” | Tranquila | Alertas proactivas |
| Trámites | Sigue checklist y adjunta evidencias desde el celular | “Sé qué me falta” | Capaz | Menos burocracia percibida |
| Pagos del hogar / transporte | Paga/recarga y consulta historial | “Tengo el rastro de todo” | En control | Auditoría (O-03) |
| Compartir | Envía documento verificado cuando lo piden | “No busco fotos sueltas” | Eficiente | Identidad digital usable |

> **[PENDIENTE — captura visual]** Subir captura del To-Be Scenario Mapping elaborado en la herramienta del curso (una por persona) cuando esté lista; reemplazar esta tabla o anexarla debajo.

---

## 3.2 User Stories

### Epics (alineados a módulos FAS)

| Epic | Título | Módulos / procesos | Descripción |
| :--- | :--- | :--- | :--- |
| **E1** | Identidad y acceso | M-01 · P-01 | Registro, login, biometría, validación RENIEC (evolutiva). |
| **E2** | Documentos y perfiles | M-02 · P-02, P-06 | Alta de documentos, QR, multi-perfil familiar. |
| **E3** | Pagos y recargas | M-03 · P-03 | Transporte, transferencias/billeteras, pagos cotidianos. |
| **E4** | Trazabilidad y auditoría | M-04 · P-04 | Historial de transacciones/documentos y reportes. |
| **E5** | Notificaciones | M-05 · P-05 | Vencimientos, saldo bajo, confirmaciones. |
| **E6** | Integraciones externas | M-06 | RENIEC, transporte, banca, SBS/SUNAT (evolutivo). |
| **E7** | Acceso offline | M-02 (+ caché) | Consulta de documentos verificados sin red. |
| **E8** | Landing / adquisición | — | Propuesta de valor y acceso a la app. |
| **E9** | Plataforma API | API Gateway | Endpoints que sostienen E1–E7. |

### Historias de usuario (Avance 1)

| US | Título | Historia | Criterios de aceptación (resumen Gherkin) | Epic |
| :--- | :--- | :--- | :--- | :--- |
| **US01** | Registro de usuario | Como ciudadano, quiero registrarme para crear mi identidad digital en KapakID. | *Given* visitante · *When* datos válidos · *Then* cuenta creada. *When* datos inválidos · *Then* rechazo con motivo. | E1 |
| **US02** | Login biométrico / PIN | Como usuario, quiero autenticarme con biometría o PIN para proteger mis documentos. | *Given* cuenta activa · *When* biometría/PIN correcto · *Then* acceso. *When* fallo · *Then* bloqueo/reintento. | E1 |
| **US03** | Validación RENIEC (evolutiva) | Como usuario, quiero validar mi DNI con RENIEC para tener identidad verificada. | *Given* DNI válido · *When* validación OK · *Then* perfil verificado. *When* API caída · *Then* mensaje y reintento (Circuit Breaker). | E1/E6 |
| **US04** | Registrar documento | Como usuario, quiero cargar/escanear DNI, carné u otros para centralizarlos. | *Given* autenticado · *When* documento válido · *Then* almacenado + metadatos. *When* inválido · *Then* rechazo. | E2 |
| **US05** | QR por documento/usuario | Como usuario, quiero un QR para identificar/documento digitalmente. | *Given* documento registrado · *When* genero QR · *Then* se muestra y es consultable. | E2 |
| **US06** | Perfiles familiares | Como tutor, quiero perfiles de hijos/dependientes para gestionar sus documentos. | *Given* plan que lo permita · *When* creo perfil · *Then* queda vinculado. *When* excedo límite · *Then* rechazo. | E2 |
| **US07** | Recarga transporte | Como estudiante, quiero recargar Metropolitano/Lima Pass desde la app. | *Given* tarjeta vinculada · *When* monto válido · *Then* saldo actualizado + registro. *When* error pago · *Then* no se altera saldo. | E3/E6 |
| **US08** | Pago / transferencia cotidiana | Como usuario, quiero pagar o transferir (banca/billeteras) sin salir de KapakID. | *Given* método vinculado · *When* confirmo pago · *Then* comprobante + historial. | E3/E6 |
| **US09** | Historial auditado | Como usuario, quiero ver el historial de pagos y gestiones documentales. | *Given* operaciones previas · *When* abro historial · *Then* lista ordenada e inmutable percibida. | E4 |
| **US10** | Alerta de vencimiento | Como usuario, quiero aviso antes del vencimiento de un documento. | *Given* doc con fecha · *When* umbral (p.ej. 30 días) · *Then* push/inbox. | E5 |
| **US11** | Alerta de saldo bajo | Como usuario, quiero aviso si el saldo de transporte es bajo. | *Given* umbral configurado · *When* saldo &lt; umbral · *Then* notificación. | E5 |
| **US12** | Documentos offline | Como usuario, quiero ver documentos ya verificados sin internet. | *Given* caché local · *When* sin red · *Then* visualizo docs. *When* intento pagar offline · *Then* no disponible. | E7 |
| **US13** | Landing — valor | Como visitante, quiero entender qué resuelve KapakID en la landing. | *Given* landing · *When* navego beneficios · *Then* veo identidad+pagos+trazabilidad. | E8 |
| **US14** | Landing — acceso | Como visitante, quiero enlaces a registro/login/app. | *Given* CTA · *When* click · *Then* redirige correctamente. | E8 |
| **US15** | API auth | Como developer, quiero `/auth` con JWT para los clientes. | *Given* credenciales OK · *Then* 200+token. *When* inválidas · *Then* 401. | E9 |
| **US16** | API documentos | Como developer, quiero CRUD/consulta de documentos por usuario. | *Given* token válido · *When* POST/GET · *Then* persistencia/consulta OK. | E9 |
| **US17** | API pagos (evolutiva) | Como developer, quiero endpoints de recarga/pago con idempotencia. | *Given* request idempotente · *When* reintento · *Then* no duplica cobro. | E9/E3 |

> Se retiró del alcance Avance 1 el epic de “voto digital” del informe móvil previo: no forma parte de la visión FAS reestructurada (identidad + pagos + auditoría + integraciones).

---

## 3.3 Impact Map

**Goal:** Centralizar identidad digital y pagos cotidianos con trazabilidad, aumentando documentos verificados y transacciones mensuales por usuario (O-01, O-02, O-03).

| Actor | Impacto buscado | Deliverables (ejemplos) |
| :--- | :--- | :--- |
| Estudiante | Menos colas/recargas físicas; documentos a mano | US07, US04, US10, US11, US12 |
| Tutor / padre-madre | Control familiar y menos olvidos | US06, US10, US09, US04 |
| Ciudadano / visitante | Entender y confiar en KapakID | US13, US14 |
| Sistema / developer | APIs seguras e integrables | US15–US17, US03 |

![Impact Mapping](../assets/cap-3/Impact_Mapping/Impact_Mapping.png)

---

## 3.4 Product Backlog

Priorización sugerida para Avance 1 / primeros sprints (ajustable en planning):

| Orden | US | Título | SP (est.) | Prioridad |
| :---: | :--- | :--- | :---: | :--- |
| 1 | US13 | Landing — valor | 3 | Must |
| 2 | US14 | Landing — acceso | 2 | Must |
| 3 | US01 | Registro de usuario | 5 | Must |
| 4 | US02 | Login biométrico / PIN | 5 | Must |
| 5 | US15 | API auth | 5 | Must |
| 6 | US04 | Registrar documento | 5 | Must |
| 7 | US16 | API documentos | 5 | Must |
| 8 | US05 | QR por documento | 3 | Should |
| 9 | US10 | Alerta de vencimiento | 3 | Must |
| 10 | US11 | Alerta de saldo bajo | 2 | Should |
| 11 | US07 | Recarga transporte | 8 | Must |
| 12 | US09 | Historial auditado | 5 | Must |
| 13 | US06 | Perfiles familiares | 5 | Should |
| 14 | US12 | Documentos offline | 5 | Should |
| 15 | US08 | Pago / transferencia | 8 | Could |
| 16 | US03 | Validación RENIEC | 8 | Could (evolutivo) |
| 17 | US17 | API pagos | 8 | Could |

![Product Backlog (referencia visual)](../assets/cap-3/Impact_Mapping/Product_Backlog.png)

> **[PENDIENTE]** Reemplazar/actualizar la captura cuando el backlog oficial viva en Jira (o herramienta del curso) con IDs US01–US17 de esta especificación.

---

*Fin del Capítulo III (Avance 1). Con Cap. I–III cerrados en contenido base; pendientes de campo/herramienta quedan etiquetados para no bloquear el avance.*
