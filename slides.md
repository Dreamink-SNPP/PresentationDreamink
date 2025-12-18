---
# Slidev Configuration for Thesis Presentation
# Documentation: https://sli.dev/

# Theme Configuration
theme: seriph
background: https://cover.sli.dev

# Presentation Information
title: Presentación de Proyecto
info: |
  ## Proyecto Técnico
  Dispersión organizativa de estructuras dramáticas
  en los guionistas del Departamento Central

  Presentado por: Ing. Fernando Cardozo y Alberto Álvarez
  Tutor: Prof. Lic. Moisés Ávalos

  Centro Tecnológico de Formación Profesional - Paraguay Japón
  2025

# MDC Syntax Support
mdc: true

# Slide Transitions
transition: slide-left

# Drawing Persistence
drawings:
  persist: false

# Presentation Duration
duration: 45min

# Custom Styling
css: unocss

# Language
lang: es-ES
---

<!--
═══════════════════════════════════════════════════════════════════
  ESTRUCTURA DE LA PRESENTACIÓN DE TESIS
═══════════════════════════════════════════════════════════════════

Este archivo es el punto de entrada principal de la presentación.
Importa todas las secciones desde la carpeta slides/

Para editar el contenido, modifica los archivos individuales en slides/:
  - 00-fondo.md                (Fondo de la presentación)
  - 01-portada.md              (Página de título)
  - 02-introduccion.md         (Introducción y contexto)
  - 03-planteamiento-problema.md (Problema de investigación)
  - 04-objetivos.md            (Objetivos general y específicos)
  - 05-justificacion.md        (Justificación del estudio)
  - 06-marco-metodologico.md   (Metodología de investigación)
  - 07-conclusion.md           (Conclusiones y hallazgos)
  - 09-agradecimientos.md      (Agradecimientos y cierre)

═══════════════════════════════════════════════════════════════════
-->

---
src: ./slides/00-fondo.md
---

---
src: ./slides/01-portada.md
---

---
src: ./slides/02-introduccion.md
---

---
src: ./slides/03-planteamiento-problema.md
---

---
src: ./slides/04-objetivos.md
---

---
src: ./slides/05-justificacion.md
---

---
src: ./slides/06-marco-metodologico.md
---

---
src: ./slides/07-conclusion.md
---

---
src: ./slides/09-agradecimientos.md
---
