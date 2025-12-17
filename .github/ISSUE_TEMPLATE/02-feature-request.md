---
name: Feature Request / Solicitud de Funcionalidad
description: Suggest an enhancement for the presentation / Sugerir una mejora para la presentación
title: "[Feature]: "
labels: ["enhancement", "needs-discussion"]
body:
  - type: markdown
    attributes:
      value: |
        ## Thanks for your suggestion! / ¡Gracias por tu sugerencia!

        Please help us understand your feature request by providing detailed information.

        Por favor ayúdanos a entender tu solicitud de funcionalidad proporcionando información detallada.

  - type: dropdown
    id: feature-type
    attributes:
      label: Feature Type / Tipo de Funcionalidad
      description: What type of feature is this? / ¿Qué tipo de funcionalidad es esta?
      options:
        - New Content (Nuevo Contenido)
        - Visual Enhancement (Mejora Visual)
        - Animation/Transition (Animación/Transición)
        - Interactivity (Interactividad)
        - Export Feature (Función de Exportación)
        - Accessibility (Accesibilidad)
        - Documentation (Documentación)
        - Development Tool (Herramienta de Desarrollo)
        - Other (Otro)
    validations:
      required: true

  - type: textarea
    id: problem
    attributes:
      label: Problem Statement / Planteamiento del Problema
      description: Is your feature request related to a problem? Describe it. / ¿Tu solicitud está relacionada con un problema? Descríbelo.
      placeholder: |
        Example: I find it difficult to... / I'd like to be able to...
        Ejemplo: Encuentro difícil... / Me gustaría poder...
    validations:
      required: true

  - type: textarea
    id: solution
    attributes:
      label: Proposed Solution / Solución Propuesta
      description: Describe the solution you'd like / Describe la solución que te gustaría
      placeholder: |
        I think we could add... / This could work by...
        Creo que podríamos agregar... / Esto podría funcionar mediante...
    validations:
      required: true

  - type: textarea
    id: alternatives
    attributes:
      label: Alternatives Considered / Alternativas Consideradas
      description: Have you thought of alternative solutions? / ¿Has pensado en soluciones alternativas?
      placeholder: |
        Another approach could be... / We could also...
        Otro enfoque podría ser... / También podríamos...
    validations:
      required: false

  - type: textarea
    id: use-case
    attributes:
      label: Use Case / Caso de Uso
      description: How would this feature be used? Who benefits? / ¿Cómo se usaría esta funcionalidad? ¿Quién se beneficia?
      placeholder: |
        This would help presenters by...
        Esto ayudaría a los presentadores mediante...
    validations:
      required: false

  - type: textarea
    id: mockup
    attributes:
      label: Mockups/Examples / Maquetas/Ejemplos
      description: If applicable, add mockups, screenshots, or examples / Si aplica, agrega maquetas, capturas o ejemplos
      placeholder: Drag and drop images or provide links... / Arrastra y suelta imágenes o proporciona enlaces...
    validations:
      required: false

  - type: dropdown
    id: priority
    attributes:
      label: Priority / Prioridad
      description: How important is this to you? / ¿Qué tan importante es esto para ti?
      options:
        - Nice to have (Sería bueno tenerlo)
        - Important (Importante)
        - Critical (Crítico)
    validations:
      required: false

  - type: dropdown
    id: complexity
    attributes:
      label: Estimated Complexity / Complejidad Estimada
      description: How complex do you think this would be to implement? / ¿Qué tan complejo crees que sería implementar esto?
      options:
        - Small change (Cambio pequeño)
        - Medium effort (Esfuerzo medio)
        - Large project (Proyecto grande)
        - Not sure (No estoy seguro)
    validations:
      required: false

  - type: textarea
    id: additional
    attributes:
      label: Additional Context / Contexto Adicional
      description: Add any other context or references about the feature request / Agrega cualquier otro contexto o referencias sobre la solicitud
      placeholder: Similar features in other presentations... / Funcionalidades similares en otras presentaciones...
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist / Lista de Verificación Pre-envío
      description: Please confirm the following / Por favor confirma lo siguiente
      options:
        - label: I have searched for similar feature requests / He buscado solicitudes de funcionalidad similares
          required: true
        - label: This feature aligns with the academic nature of the project / Esta funcionalidad se alinea con la naturaleza académica del proyecto
          required: true
        - label: I would be willing to help implement this feature / Estaría dispuesto a ayudar a implementar esta funcionalidad
          required: false
