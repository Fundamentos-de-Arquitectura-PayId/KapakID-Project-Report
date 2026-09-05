# KapakID — Project Report

<div align="center">

<img src="./assets/cap-1/Banner-UPC.png" alt="Banner UPC" width="420">

**Universidad Peruana de Ciencias Aplicadas**  
Carrera de Ingeniería de Software

| | |
| :--- | :--- |
| **Curso** | Fundamentos de Arquitectura de Software |
| **Código** | 15987 |
| **Ciclo** | 2620 |
| **Docente** | Wilder Aurelio Vega Calero |
| **Startup** | F1nTrack |
| **Producto** | KapakID |

**Integrantes**

| Apellidos y Nombres |
| :--- |
| Taquiri, Giussepe |
| Mora Blas, Diego |
| Mallqui Vilca, Dhilsen |
| Tasayco Osorio, Raul Hiroshi |

</div>

---

## ¿De qué trata este proyecto?

### El problema

En el Perú, el ciudadano vive con **identidad y pagos fragmentados**: DNI y carnés en físico, tarjetas de Metropolitano/Lima Pass, apps de banco (Yape, Plin, etc.) y documentos sueltos en el celular. No hay una sola plataforma segura que una todo eso.

### La problemática

KapakID ataca la falta de una solución **integrada** que permita:

1. **Identidad digital verificable** (p. ej. con RENIEC / biometría)
2. **Documentos digitalizados** con trazabilidad
3. **Pagos cotidianos** (transporte, bancos, comercios)
4. **Auditoría** de operaciones y cumplimiento (SUNAT, SBS, protección de datos)

No es un CRUD simple: es un producto de **arquitectura de software** (API Gateway, módulos/microservicios, integraciones externas, atributos de calidad).

### Qué vamos a hacer

Construir y documentar **KapakID** (startup **F1nTrack**): plataforma de identidad digital + documentos + pagos integrados para el ciudadano, empezando por Lima Metropolitana (estudiantes y familias).

En este repositorio entregamos el **informe académico** por capítulos.

---

## Flujo de ramas (cómo trabajamos)

Sí: **una feature por capítulo**, luego merge hacia arriba.

```text
main
 └── develop
      ├── feature/chapter-1   ← AHORA (solo Capítulo I)
      ├── feature/chapter-2   ← después (solo Capítulo II)
      └── feature/chapter-3   ← después (solo Capítulo III)
```

1. Trabajar en `feature/chapter-N` **solo** el contenido de ese capítulo.
2. Merge `feature/chapter-N` → `develop`.
3. Merge `develop` → `main` cuando el avance del capítulo esté listo.
4. Repetir para el siguiente capítulo.

Commits: Conventional Commits (`feat`, `fix`, `docs`, `chore`) · **sin co-autor**.

---

## Estructura del repositorio

```text
KapakID-Project-Report/
├── README.md
├── assets/cap-1/          ← imágenes Cap. I
└── report/
    ├── 01-student-outcome.md
    ├── 11-chapter-I-introduction.md      ← contenido actual
    ├── 21-chapter-II-requirements.md     ← stub (próxima feature)
    ├── 31-chapter-III-specifications.md  ← stub (próxima feature)
    └── 99-bibliography.md
```

Base de contenido adaptada del informe KapakID ([AppsM0viles/report](https://github.com/AppsM0viles/report)), reorientada al curso de **Fundamentos de Arquitectura de Software** (identidad + pagos + integraciones + trazabilidad).

---

## Contenido

- [Student Outcome](report/01-student-outcome.md)
- [Capítulo I: Introducción](report/11-chapter-I-introduction.md)
  - 1.1 Startup Profile
  - 1.2 Solution Profile (problema, 5W+2H, Lean UX)
  - 1.3 Segmentos objetivo
- [Capítulo II: Requirements & Analysis](report/21-chapter-II-requirements.md)
  - 2.1 Competidores
  - 2.2 Entrevistas
  - 2.3 Needfinding (Personas, Task Matrix, Empathy Maps, As-Is)
- [Capítulo III: Requirements Specification](report/31-chapter-III-specifications.md)
  - 3.1 To-Be Scenario Mapping
  - 3.2 User Stories
  - 3.3 Impact Map
  - 3.4 Product Backlog
- [Bibliografía](report/99-bibliography.md)

---

## Pendientes (no bloquean el Avance 1 base)

| Ítem | Dónde | Estado |
| :--- | :--- | :--- |
| ≥2 entrevistas nuevas segmento padres/tutores | Cap. II §2.2.2 | **Por completar** |
| Capturas To-Be en herramienta del curso | Cap. III §3.1 | **Por completar** |
| Backlog oficial en Jira (captura actualizada) | Cap. III §3.4 | **Por completar** |
| Fotos/códigos de Giussepe, Diego, Dhilsen | Cap. I §1.1.2 | **Por completar** |

---

## Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción |
| :--- | :--- | :--- | :--- |
| 1.0 | 05/09/2026 | Equipo F1nTrack | Cap. I adaptado a FAS (curso 15987, ciclo 2620): Startup/Solution Profile, Lean UX y segmentos. |
| 1.1 | 05/09/2026 | Equipo F1nTrack | Cap. II: competidores, entrevistas, needfinding. |
| 1.2 | 05/09/2026 | Equipo F1nTrack | Cap. III: To-Be, User Stories, Impact Map y Product Backlog (Avance 1). |

---

## Estado del avance (por capítulo)

| Capítulo | Estado |
| :--- | :---: |
| Cap. I — Introducción | Listo |
| Cap. II — Requirements & Analysis | Listo (con pendientes de campo) |
| Cap. III — Requirements Specification | Listo (con pendientes de capturas/Jira) |
