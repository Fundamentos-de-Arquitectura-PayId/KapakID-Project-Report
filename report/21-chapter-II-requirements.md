# Capítulo II: Requirements & Analysis

Este capítulo documenta el proceso de **elicitación y análisis de requisitos** de KapakID para el curso de **Fundamentos de Arquitectura de Software**. Incluye análisis competitivo, entrevistas a los segmentos del Cap. I y needfinding (Personas, Task Matrix, Empathy Maps y As-Is Scenario Mapping), alineado a los objetivos O-01…O-05 y procesos P-01…P-06 (identidad digital, pagos, trazabilidad e integraciones).

---

## 2.1 Competidores

### ¿Por qué llevar a cabo este análisis?

El análisis de competidores es esencial para KapakID porque permite:

- Identificar el panorama de billeteras digitales, identidad electrónica y servicios parciales (transporte, pagos, documentos).
- Detectar fortalezas y debilidades de la competencia.
- Definir la propuesta diferencial: **identidad + documentos + pagos + auditoría + integraciones**.
- Orientar producto/marketing hacia gaps no cubiertos.
- Anticipar amenazas (bancos consolidados, desconfianza en datos sensibles, regulación SBS/SUNAT).

### 2.1.1 Análisis competitivo (Competitive Analysis Landscape)

**Pregunta / objetivo:** ¿Cómo se posiciona KapakID frente a soluciones parciales de pagos e identidad en Perú, y qué gap ocupamos al integrar identidad verificable, documentos, pagos cotidianos y trazabilidad?

| Aspecto | **KapakID (F1nTrack)** | **Yape** | **Plin** | **ID Perú (RENIEC)** |
| :--- | :--- | :--- | :--- | :--- |
| **Overview** | Identidad digital + documentos + pagos + trazabilidad, con visión de integraciones (RENIEC, transporte, banca, SBS). | Billetera digital bancaria masiva en Perú. | Billetera interoperable entre bancos. | Identidad digital / autenticación oficial del Estado. |
| **Ventaja / valor** | Centraliza identidad, documentos, pagos, alertas y auditoría. | Confianza y adopción masiva en pagos P2P. | Interoperabilidad bancaria y simplicidad. | Respaldo oficial en trámites. |
| **Mercado objetivo** | Estudiantes y familias (Lima) que necesitan identidad + pagos cotidianos. | Jóvenes y adultos bancarizados. | Usuarios de banca digital. | Ciudadanos en trámites oficiales. |
| **Marketing** | Diferenciación por seguridad, centralización local y freemium familiar. | Marketing masivo + respaldo bancario. | Interoperabilidad. | Difusión estatal. |
| **Productos** | Verificación, documentos QR, pagos/recargas, notificaciones, multi-perfil, historial auditado. | Pagos y transferencias. | Pagos entre bancos. | Autenticación y certificados. |
| **Precios** | Freemium (básico gratis; premium: multi-perfil / alertas avanzadas). | Gratis. | Gratis. | Gratis (Estado). |
| **Canales** | App móvil / web + API Gateway (M-01…M-06). | App móvil. | App móvil. | Canales de gobierno. |

#### SWOT (síntesis)

| | **KapakID** | **Yape** | **Plin** | **ID Perú** |
| :--- | :--- | :--- | :--- | :--- |
| **Fortalezas** | Integración identidad+pagos+trazabilidad; listo para arquitectura (microservicios, auditoría). | Marca y adopción. | Interoperabilidad. | Oficialidad. |
| **Debilidades** | Debe ganar confianza inicial; madurez de producto. | No gestiona documentos ni transporte unificado. | Sin documentos/alertas/auditoría ciudadana. | No cubre pagos ni transporte. |
| **Oportunidades** | Trámites digitales + pagos cotidianos + NFC/QR. | Ampliar servicios. | Ampliar experiencia. | Ampliar servicios digitales. |
| **Amenazas** | Bancos/fintech; regulación; desconfianza. | Apps más completas. | Nuevos fintech. | Baja adopción vs. privados. |

### 2.1.2 Estrategias y tácticas frente a competidores

**Estrategias:** diferenciación por centralización + seguridad + trazabilidad (O-01, O-03, O-04); enfoque local (RENIEC, Metropolitano/Lima Pass, banca); cumplimiento Ley 29733.

**Tácticas:** alianzas universidades/transporte; campaña “Identidad y pagos en un solo lugar”; freemium familiar; roadmap evolutivo de integraciones (M-06) con resiliencia ante fallos de APIs externas.

---

## 2.2 Entrevistas

### 2.2.1 Diseño de entrevistas

**Segmentos:** Estudiantes universitarios (18–29) y padres/madres o tutores (25–45).

**Objetivo:** Validar fricciones de identidad/documentos/pagos, confianza (biometría, cifrado), alertas, multi-perfil, trazabilidad e interés en integraciones (RENIEC, transporte, banca).

#### Preguntas principales

1. ¿Qué documentos y tarjetas llevas a diario? ¿Cuáles preferirías en el celular?
2. ¿Has perdido u olvidado un documento importante? ¿Cómo ayudaría un respaldo digital seguro?
3. ¿Cómo recargas Metropolitano/Lima Pass hoy? ¿Usarías QR/NFC desde la app?
4. ¿Qué te estresa al renovar DNI/carné? ¿Te ayudaría escanear requisitos desde el celular?
5. Si la app avisara vencimientos o saldo bajo, ¿cómo y con cuánta anticipación?
6. ¿Confiarías en guardar documentos sensibles? ¿Qué seguridad te tranquiliza?
7. ¿Administrarías documentos de hijos/familiares? ¿Qué es imprescindible?
8. ¿Qué tan útil sería un checklist de trámites con calendario?
9. En móvil, ¿qué priorizas? (biometría, widget, push, recargas, offline, historial)
10. ¿Pagarías suscripción premium? ¿Por qué funciones?

#### Preguntas complementarias

11. ¿Te importaría un historial auditado de pagos/documentos?
12. ¿Usarías validación con RENIEC al registrarte si entiendes el beneficio?

### 2.2.2 Registro de entrevistas

> Meta: **3 a 5 entrevistas por segmento**.

#### Segmento A — Estudiantes universitarios

| Campo | Entrevista 1 | Entrevista 2 | Entrevista 3 |
| :--- | :--- | :--- | :--- |
| Nombres | Sebastian Delgado | Jose Rodrigo Rodriguez | Daniel Paolo Ita Rojas |
| Edad | 21 | 21 | 22 |
| Distrito | San Borja | Villa María del Triunfo | Villa María del Triunfo |
| Evidencia | ![Sebastian](../assets/cap-2/Interviews/InterviewSebastianDelgado.png) | ![Jose](../assets/cap-2/Interviews/InterviewJoseRodrigo.png) | ![Paolo](../assets/cap-2/Interviews/InterviewPaoloIta.png) |
| Video | [Grabación](https://drive.google.com/file/d/1L56VeFgJNXZNlBG1SJi8R2q2ly_IwkGr/view?usp=sharing) | [Grabación](https://drive.google.com/file/d/1NJMvMY5To5xtlis-if2pwjwBhdjVMOpi/view?usp=sharing) | [Grabación](https://drive.google.com/file/d/16iohQr01hyAhS6zoUO3Td08Vxon0hDhe/view?usp=sharing) |

**Resúmenes**

- **Sebastian:** Fricción en recarga física; dispuesto a premium si elimina colas; alertas de saldo (~S/5) y vencimientos (~1 mes).
- **Jose Rodrigo:** Biometría/PIN y **offline** decisivos; reposición de carné es lenta; necesita bóveda digital confiable.
- **Daniel Paolo:** Valora organización, **multi-perfil**, historial y dashboard de alertas.

#### Segmento B — Padres/madres o tutores

| Campo | Entrevista 1 |
| :--- | :--- |
| Nombres | Freddy Jesús Torre Valverde |
| Edad | 35 |
| Distrito | Surco |
| Video | [YouTube](https://youtu.be/LSnkTj_Xj1Q) |

**Resumen:** Control familiar, documentos de dependientes y alertas/previsión (P-06 / premium multi-perfil).

> **Pendiente:** completar ≥2 entrevistas adicionales del segmento B (meta 3–5).

### 2.2.3 Análisis de entrevistas

#### Segmento A — Estudiantes

| Hallazgo | Evidencia | Implicancia KapakID |
| :--- | :--- | :--- |
| Recarga física = mayor dolor operativo | 3/3 | P-03 / F-07 (M-03+M-06) |
| Biometría + cifrado condicionan adopción | Jose + consenso | F-01, F-17, M-01 |
| Offline imprescindible | Jose | Caché local de documentos verificados |
| Alertas de alto valor | Sebastian + Daniel | P-05 / M-05 |
| Multi-perfil e historial interesan | Daniel | P-06, P-04 / M-02, M-04 |
| Disposición a premium | Sebastian ≈ S/10–15 | Freemium (O-02/O-05) |

**Objetivo común:** 18–22 años, Lima, DNI + carné + transporte + débito a diario.  
**Subjetivo común:** rapidez, odio a colas, desconfianza sin biometría, “todo en una pantalla”.

#### Segmento B — Padres/tutores (preliminar)

| Hallazgo | Implicancia |
| :--- | :--- |
| Documentos de hijos/dependientes | Multi-perfil (F-15) |
| Alertas y previsión | Notificaciones (F-13/F-14) |
| Control y trazabilidad | Historial/auditoría (F-10/F-11, M-04) |

---

## 2.3 Needfinding

### 2.3.1 User Personas

#### Persona 1 — Estudiante universitario (“Luis”, ~21)

![User Persona Estudiante](../assets/cap-2/Needfinding/User%20Personas.png)

Relacionado a: eficiencia en transporte, alertas de saldo, biometría, centralización de DNI/carné.

#### Persona 2 — Madre/padre o tutor (“Patricia”, ~35–40)

![User Persona Madre](../assets/cap-2/Needfinding/User%20Personas2.png)

Relacionado a: multi-perfil, vencimientos, compartir documentos, historial y control familiar.

### 2.3.2 User Task Matrix

Tareas de la vida real (independientes de KapakID):

| Task | Estudiante Frec. | Estudiante Imp. | Tutor Frec. | Tutor Imp. |
| :--- | :---: | :---: | :---: | :---: |
| Centralizar / tener a mano documentos | Often | High | Always | High |
| Recargar / pagar transporte | Always | High | Often | Medium |
| Alertas de saldo / vencimiento | Always | High | Always | High |
| Gestionar perfiles familiares | Rarely | Medium | Often | High |
| Acceso offline a documentos | Sometimes | Medium | Often | High |
| Checklist de trámites | Sometimes | Medium | Often | High |
| Historial de pagos/trámites | Sometimes | Medium | Often | Medium |
| Autenticación biométrica / PIN | Often | High | Always | High |
| Usar billeteras / transferencias | Often | High | Sometimes | Medium |
| Compartir documento verificado | Sometimes | Medium | Often | High |
| Renovar documentos | Rarely | High | Sometimes | High |
| Pagar servicios del hogar | Rarely | Medium | Often | High |
| Monitorear gastos / reportes | Rarely | Medium | Often | Medium |
| Validar identidad en control/trámite | Often | High | Sometimes | High |

**Lectura:** ambos valoran centralización, alertas y seguridad. Estudiante → transporte + rapidez; tutor → multi-perfil + previsión. Confirma O-01/O-02/O-05 y P-02/P-03/P-05/P-06.

### 2.3.3 Empathy Maps

#### Empathy Map — Estudiante universitario

![Empathy Map Estudiante](../assets/cap-2/Needfinding/Empathy%20Map%20Estudiante%20Universitario.png)

#### Empathy Map — Madre de familia / tutor

![Empathy Map Madre](../assets/cap-2/Needfinding/Empathy%20Map%20Madre%20de%20Familia.png)

**Pains:** colas de recarga, miedo a perder documentos, desconfianza sin biometría, requisitos poco claros, falta de vista única de estado.  
**Gains:** tiempo recuperado, alertas, documentos disponibles, organización familiar, historial claro.

### 2.3.4 As-is Scenario Mapping

#### As-Is — Estudiante universitario

![As-Is Estudiante](../assets/cap-2/Needfinding/User%20Journey%20Mapping%20Estudiante%20Universitario.png)

**Síntesis:** varias tarjetas → transporte → cola/saldo bajo → DNI/carné en controles → pagos en otra app → olvido de vencimientos. Emociones: prisa, frustración, alivio breve.

#### As-Is — Madre de familia / tutor

![As-Is Madre](../assets/cap-2/Needfinding/User%20Journey%20Mapping%20Madre%20de%20Familia.png)

**Síntesis:** documentos de varios miembros → búsqueda de papeles → vencimientos escolares/salud → pagos del hogar → reacción tardía a olvidos. Emociones: carga mental, ansiedad, necesidad de control.

**Blank areas:** adopción real de RENIEC en onboarding; WTP premium en segmento B; fricción NFC en estaciones (validar en campo).

---

*Fin del Capítulo II. El Capítulo III (To-Be, User Stories, Impact Map, Product Backlog) continúa en `feature/chapter-3`.*
