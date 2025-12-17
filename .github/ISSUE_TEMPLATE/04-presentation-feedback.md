---
name: Presentation Feedback / Retroalimentación de Presentación
description: Provide academic or scholarly feedback on the presentation / Proporcionar retroalimentación académica o académica sobre la presentación
title: "[Feedback]: "
labels: ["feedback", "academic"]
body:
  - type: markdown
    attributes:
      value: |
        ## Academic Feedback / Retroalimentación Académica

        We appreciate scholarly feedback on our thesis presentation!

        ¡Apreciamos la retroalimentación académica sobre nuestra presentación de tesis!

        This template is for academic and content feedback. For technical issues, please use the Bug Report template.

        Esta plantilla es para retroalimentación académica y de contenido. Para problemas técnicos, por favor usa la plantilla de Reporte de Error.

  - type: dropdown
    id: section
    attributes:
      label: Section / Sección
      description: Which section does your feedback apply to? / ¿A qué sección aplica tu retroalimentación?
      options:
        - Cover (Portada)
        - Introduction (Introducción)
        - Problem Statement (Planteamiento del Problema)
        - Objectives (Objetivos)
        - Justification (Justificación)
        - Methodological Framework (Marco Metodológico)
        - Conclusion (Conclusión)
        - Acknowledgments (Agradecimientos)
        - Overall Presentation (Presentación General)
        - All Sections (Todas las Secciones)
    validations:
      required: true

  - type: dropdown
    id: feedback-type
    attributes:
      label: Feedback Type / Tipo de Retroalimentación
      description: What type of feedback are you providing? / ¿Qué tipo de retroalimentación estás proporcionando?
      options:
        - Content Accuracy (Precisión del Contenido)
        - Methodological Suggestion (Sugerencia Metodológica)
        - Clarity Improvement (Mejora de Claridad)
        - Academic Citation (Citación Académica)
        - Theoretical Framework (Marco Teórico)
        - Data Presentation (Presentación de Datos)
        - Visual/Design (Visual/Diseño)
        - Argument Structure (Estructura de Argumentos)
        - Literature Review (Revisión de Literatura)
        - Other (Otro)
    validations:
      required: true

  - type: textarea
    id: feedback
    attributes:
      label: Feedback / Retroalimentación
      description: Your scholarly feedback and observations / Tu retroalimentación y observaciones académicas
      placeholder: |
        Please provide constructive, evidence-based feedback...
        Por favor proporciona retroalimentación constructiva basada en evidencia...
    validations:
      required: true

  - type: textarea
    id: suggestions
    attributes:
      label: Suggested Changes / Cambios Sugeridos
      description: Specific improvements or changes you recommend / Mejoras específicas o cambios que recomiendas
      placeholder: |
        I suggest adding/modifying... because...
        Sugiero agregar/modificar... porque...
    validations:
      required: false

  - type: textarea
    id: references
    attributes:
      label: Supporting References / Referencias de Apoyo
      description: Academic sources that support your feedback / Fuentes académicas que apoyan tu retroalimentación
      placeholder: |
        Smith, J. (2023). Title of work...
        García, M. (2024). Título del trabajo...
      render: markdown
    validations:
      required: false

  - type: dropdown
    id: severity
    attributes:
      label: Importance / Importancia
      description: How important is this feedback? / ¿Qué tan importante es esta retroalimentación?
      options:
        - Minor suggestion (Sugerencia menor)
        - Moderate improvement (Mejora moderada)
        - Significant issue (Problema significativo)
        - Critical concern (Preocupación crítica)
    validations:
      required: false

  - type: dropdown
    id: expertise
    attributes:
      label: Your Area of Expertise / Tu Área de Especialización
      description: What is your background in relation to this topic? / ¿Cuál es tu experiencia en relación a este tema?
      options:
        - Screenwriting/Guionismo
        - Film/Media Studies (Estudios de Cine/Medios)
        - Research Methodology (Metodología de Investigación)
        - Audiovisual Production (Producción Audiovisual)
        - Literary Theory (Teoría Literaria)
        - Education/Pedagogy (Educación/Pedagogía)
        - General Academic (Académico General)
        - Student (Estudiante)
        - Other (Otro)
    validations:
      required: false

  - type: input
    id: affiliation
    attributes:
      label: Academic Affiliation (Optional) / Afiliación Académica (Opcional)
      description: Your institution or role, if you wish to be acknowledged / Tu institución o rol, si deseas ser reconocido
      placeholder: Professor at Universidad..., PhD Student in..., etc.
    validations:
      required: false

  - type: dropdown
    id: acknowledgment
    attributes:
      label: Acknowledgment Preference / Preferencia de Reconocimiento
      description: How would you like to be acknowledged if your feedback is incorporated? / ¿Cómo te gustaría ser reconocido si tu retroalimentación es incorporada?
      options:
        - Acknowledge with name and affiliation (Reconocer con nombre y afiliación)
        - Acknowledge with name only (Reconocer solo con nombre)
        - Anonymous acknowledgment (Reconocimiento anónimo)
        - No acknowledgment needed (No necesito reconocimiento)
    validations:
      required: false

  - type: textarea
    id: strengths
    attributes:
      label: Strengths / Fortalezas
      description: What aspects of the presentation are particularly strong? / ¿Qué aspectos de la presentación son particularmente fuertes?
      placeholder: |
        The methodology section effectively...
        La sección de metodología efectivamente...
    validations:
      required: false

  - type: textarea
    id: additional
    attributes:
      label: Additional Comments / Comentarios Adicionales
      description: Any other observations or suggestions / Cualquier otra observación o sugerencia
      placeholder: Overall, this presentation... / En general, esta presentación...
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: Feedback Guidelines / Guías de Retroalimentación
      description: Please confirm the following / Por favor confirma lo siguiente
      options:
        - label: This feedback is constructive and professional / Esta retroalimentación es constructiva y profesional
          required: true
        - label: This feedback is based on evidence or scholarly standards / Esta retroalimentación está basada en evidencia o estándares académicos
          required: true
        - label: I have reviewed the relevant section(s) of the presentation / He revisado la(s) sección(es) relevante(s) de la presentación
          required: true
