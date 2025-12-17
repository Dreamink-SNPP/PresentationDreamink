---
name: Bug Report / Reporte de Error
description: Report a technical issue with the presentation / Reportar un problema técnico con la presentación
title: "[Bug]: "
labels: ["bug", "needs-triage"]
body:
  - type: markdown
    attributes:
      value: |
        ## Thanks for reporting! / ¡Gracias por reportar!

        Please help us understand and fix the issue by providing detailed information.

        Por favor ayúdanos a entender y corregir el problema proporcionando información detallada.

  - type: dropdown
    id: category
    attributes:
      label: Category / Categoría
      description: What type of issue is this? / ¿Qué tipo de problema es este?
      options:
        - Build/Export (Compilación/Exportación)
        - Development Server (Servidor de Desarrollo)
        - Content Display (Visualización de Contenido)
        - Styling/Layout (Estilos/Diseño)
        - Animations/Transitions (Animaciones/Transiciones)
        - Performance (Rendimiento)
        - Accessibility (Accesibilidad)
        - Other (Otro)
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: Bug Description / Descripción del Error
      description: A clear and concise description of what the bug is / Una descripción clara y concisa de cuál es el error
      placeholder: |
        Example: When I export to PDF, the images on slide 5 are missing...
        Ejemplo: Cuando exporto a PDF, las imágenes en la diapositiva 5 están faltando...
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: Steps to Reproduce / Pasos para Reproducir
      description: How can we reproduce this issue? / ¿Cómo podemos reproducir este problema?
      placeholder: |
        1. Run 'pnpm dev' / Ejecutar 'pnpm dev'
        2. Navigate to slide 5 / Navegar a diapositiva 5
        3. Click on... / Hacer clic en...
        4. See error / Ver error
    validations:
      required: true

  - type: textarea
    id: expected
    attributes:
      label: Expected Behavior / Comportamiento Esperado
      description: What should happen instead? / ¿Qué debería suceder en su lugar?
      placeholder: The slide should display correctly... / La diapositiva debería mostrarse correctamente...
    validations:
      required: true

  - type: textarea
    id: actual
    attributes:
      label: Actual Behavior / Comportamiento Actual
      description: What actually happens? / ¿Qué sucede realmente?
      placeholder: The slide is blank... / La diapositiva está en blanco...
    validations:
      required: false

  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots / Capturas de Pantalla
      description: If applicable, add screenshots to help explain your problem / Si aplica, agrega capturas de pantalla para ayudar a explicar tu problema
      placeholder: Drag and drop images here... / Arrastra y suelta imágenes aquí...
    validations:
      required: false

  - type: textarea
    id: environment
    attributes:
      label: Environment / Entorno
      description: Your system configuration / Tu configuración de sistema
      value: |
        - OS: (e.g., Ubuntu 22.04, Windows 11, macOS 13)
        - Browser: (e.g., Chrome 120, Firefox 121)
        - Node.js Version: (run `node --version`)
        - pnpm Version: (run `pnpm --version`)
        - Slidev Version: (check package.json)
      render: markdown
    validations:
      required: true

  - type: textarea
    id: additional
    attributes:
      label: Additional Context / Contexto Adicional
      description: Add any other context about the problem here / Agrega cualquier otro contexto sobre el problema aquí
      placeholder: This started happening after... / Esto empezó a suceder después de...
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist / Lista de Verificación Pre-envío
      description: Please confirm the following / Por favor confirma lo siguiente
      options:
        - label: I have searched for similar issues / He buscado issues similares
          required: true
        - label: I have read the Contributing Guide / He leído la Guía de Contribución
          required: true
        - label: I can reproduce this issue consistently / Puedo reproducir este issue consistentemente
          required: false
