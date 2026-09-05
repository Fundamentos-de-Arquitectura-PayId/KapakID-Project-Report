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
- [Capítulo II: Requirements & Analysis](report/21-chapter-II-requirements.md) *(pendiente — feature/chapter-2)*
- [Capítulo III: Requirements Specification](report/31-chapter-III-specifications.md) *(pendiente — feature/chapter-3)*
- [Bibliografía](report/99-bibliography.md)

---

## Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción |
| :--- | :--- | :--- | :--- |
| 1.0 | 05/09/2026 | Equipo F1nTrack | Cap. I adaptado a FAS (curso 15987, ciclo 2620): Startup/Solution Profile, Lean UX y segmentos con visión de identidad + pagos + integraciones. |

---

## Estado Cap. I (esta rama)

| Sección | Estado |
| :--- | :---: |
| 1.1 Startup Profile | Listo |
| 1.1.1 Descripción startup | Listo |
| 1.1.2 Perfiles (fotos/códigos pendientes de 3 integrantes) | Parcial |
| 1.2.1 Nombre del producto | Listo |
| 1.2.2 Antecedentes y problemática (5W+2H + objetivos) | Listo |
| 1.2.3 Lean UX (Problem / Assumptions / Hypothesis / Canvas) | Listo |
| 1.3 Segmentos objetivo | Listo |
| Cap. II y III | No (siguientes ramas) |
