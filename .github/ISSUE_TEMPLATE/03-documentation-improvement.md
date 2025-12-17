---
name: Documentation Improvement / Mejora de Documentación
description: Suggest improvements to documentation / Sugerir mejoras a la documentación
title: "[Docs]: "
labels: ["documentation", "good-first-issue"]
body:
  - type: markdown
    attributes:
      value: |
        ## Thanks for helping improve our documentation! / ¡Gracias por ayudar a mejorar nuestra documentación!

        Clear documentation helps everyone understand and contribute to the project.

        Una documentación clara ayuda a todos a entender y contribuir al proyecto.

  - type: dropdown
    id: doc-type
    attributes:
      label: Documentation Type / Tipo de Documentación
      description: Which documentation needs improvement? / ¿Qué documentación necesita mejora?
      options:
        - README (English / Inglés)
        - README.es (Spanish / Español)
        - CONTRIBUTING
        - CODE_OF_CONDUCT
        - SECURITY
        - STYLE_GUIDE
        - Presenter Notes (Notas del Presentador)
        - Code Comments (Comentarios de Código)
        - Setup Guide (Guía de Configuración)
        - Other (Otro)
    validations:
      required: true

  - type: dropdown
    id: issue-type
    attributes:
      label: Issue Type / Tipo de Problema
      description: What kind of documentation issue is this? / ¿Qué tipo de problema de documentación es este?
      options:
        - Missing Information (Información Faltante)
        - Incorrect Information (Información Incorrecta)
        - Outdated Information (Información Desactualizada)
        - Unclear/Confusing (Poco Claro/Confuso)
        - Typo/Grammar (Error Tipográfico/Gramática)
        - Translation Issue (Problema de Traducción)
        - Needs Examples (Necesita Ejemplos)
        - Broken Link (Enlace Roto)
        - Other (Otro)
    validations:
      required: true

  - type: textarea
    id: current-issue
    attributes:
      label: Current Issue / Problema Actual
      description: Describe what's wrong or missing in the current documentation / Describe qué está mal o falta en la documentación actual
      placeholder: |
        Example: The installation section doesn't explain how to...
        Ejemplo: La sección de instalación no explica cómo...
    validations:
      required: true

  - type: textarea
    id: location
    attributes:
      label: Location / Ubicación
      description: Where exactly is this issue? (file name, section, line number) / ¿Dónde exactamente está este problema? (nombre de archivo, sección, número de línea)
      placeholder: |
        Example: README.md, line 45 in "Getting Started" section
        Ejemplo: README.md, línea 45 en la sección "Primeros Pasos"
    validations:
      required: true

  - type: textarea
    id: proposed-improvement
    attributes:
      label: Proposed Improvement / Mejora Propuesta
      description: How should the documentation be improved? / ¿Cómo debería mejorarse la documentación?
      placeholder: |
        We should add a section that explains...
        Deberíamos agregar una sección que explique...
    validations:
      required: true

  - type: textarea
    id: suggested-content
    attributes:
      label: Suggested Content / Contenido Sugerido
      description: If you have specific text to add or replace, provide it here / Si tienes texto específico para agregar o reemplazar, proporciónalo aquí
      placeholder: |
        You can write the suggested content in Markdown...
        Puedes escribir el contenido sugerido en Markdown...
      render: markdown
    validations:
      required: false

  - type: dropdown
    id: bilingual
    attributes:
      label: Bilingual Update / Actualización Bilingüe
      description: Does this affect both English and Spanish docs? / ¿Esto afecta tanto los documentos en inglés como en español?
      options:
        - English only (Solo inglés)
        - Spanish only (Solo español)
        - Both languages (Ambos idiomas)
        - Not applicable (No aplica)
    validations:
      required: false

  - type: dropdown
    id: priority
    attributes:
      label: Priority / Prioridad
      description: How important is this improvement? / ¿Qué tan importante es esta mejora?
      options:
        - Low - Nice to have (Bajo - Sería bueno tenerlo)
        - Medium - Should be fixed (Medio - Debería corregirse)
        - High - Prevents understanding (Alto - Impide la comprensión)
        - Critical - Incorrect/Misleading (Crítico - Incorrecto/Engañoso)
    validations:
      required: false

  - type: textarea
    id: additional
    attributes:
      label: Additional Context / Contexto Adicional
      description: Any other information that would help improve the documentation / Cualquier otra información que ayudaría a mejorar la documentación
      placeholder: Screenshots, links to similar good examples... / Capturas de pantalla, enlaces a buenos ejemplos similares...
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist / Lista de Verificación Pre-envío
      description: Please confirm the following / Por favor confirma lo siguiente
      options:
        - label: I have checked that this isn't already documented elsewhere / He verificado que esto no esté ya documentado en otro lugar
          required: true
        - label: I have read the current documentation / He leído la documentación actual
          required: true
        - label: I would be willing to help write this documentation / Estaría dispuesto a ayudar a escribir esta documentación
          required: false
