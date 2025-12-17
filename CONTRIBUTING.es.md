# Contribuir a PresentationDreamink

> **Idiomas:** [English](CONTRIBUTING.md) | [Español](CONTRIBUTING.es.md)

¡Gracias por tu interés en contribuir a nuestro proyecto de presentación de tesis académica! Esta guía te ayudará a entender cómo contribuir efectivamente y mantener la calidad e integridad de este trabajo académico.

## Tabla de Contenidos

1. [Acerca de Este Proyecto](#acerca-de-este-proyecto)
2. [Formas de Contribuir](#formas-de-contribuir)
3. [Primeros Pasos](#primeros-pasos)
4. [Flujo de Trabajo de Desarrollo](#flujo-de-trabajo-de-desarrollo)
5. [Convenciones de Commits](#convenciones-de-commits)
6. [Proceso de Pull Request](#proceso-de-pull-request)
7. [Guías de Pruebas](#guías-de-pruebas)
8. [Colaboración Académica](#colaboración-académica)
9. [Guías Bilingües](#guías-bilingües)
10. [Revisión de Código](#revisión-de-código)
11. [Reconocimiento](#reconocimiento)

## Acerca de Este Proyecto

Este repositorio aloja una presentación de tesis académica desarrollada con [Slidev](https://sli.dev/), enfocada en la **sistematización del proceso de pre-escritura para guiones audiovisuales** en el Departamento Central de Paraguay.

**Título**: Dispersión Organizacional de las Estructuras Dramáticas en Guionistas del Departamento Central

**Autores**: Ing. Fernando Cardozo & Alberto Álvarez

**Supervisor Académico**: Prof. Lic. Moisés Ávalos

**Institución**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Año**: 2025

Antes de contribuir, por favor lee nuestro [Código de Conducta](CODE_OF_CONDUCT.es.md) para entender nuestros estándares comunitarios.

## Formas de Contribuir

Damos la bienvenida a varios tipos de contribuciones:

### Contribuciones Técnicas
- Corregir errores en la construcción o exportación de la presentación
- Mejorar estilos y diseños visuales
- Mejorar animaciones y transiciones
- Optimizar rendimiento y tiempos de carga
- Mejorar características de accesibilidad

### Contribuciones de Contenido
- Mejorar claridad y legibilidad de las diapositivas
- Sugerir mejores visualizaciones para datos
- Mejorar notas del presentador
- Corregir errores tipográficos o de formato
- Refinar lenguaje académico

### Contribuciones de Documentación
- Mejorar claridad y completitud del README
- Traducir documentación a otros idiomas
- Agregar ejemplos y tutoriales útiles
- Actualizar guías de configuración y despliegue
- Crear tutoriales en video o guías paso a paso

### Contribuciones Académicas
- Proporcionar retroalimentación académica sobre metodología
- Sugerir referencias académicas relevantes
- Revisar precisión y rigor del contenido
- Ofrecer revisión por pares de expertos en la materia
- Contribuir a discusiones del marco teórico

## Primeros Pasos

### Prerrequisitos

Antes de comenzar, asegúrate de tener:

- **Node.js** v20 o superior ([descargar](https://nodejs.org/))
- **pnpm** gestor de paquetes ([instrucciones de instalación](https://pnpm.io/installation))
- **Git** para control de versiones
- Una **cuenta de GitHub**
- Conocimiento básico de Markdown y Slidev (opcional pero útil)

### Configuración Inicial

1. **Hacer Fork del Repositorio**
   ```bash
   # Haz clic en el botón "Fork" en GitHub, luego clona tu fork:
   git clone https://github.com/TU-USUARIO/PresentationDreamink.git
   cd PresentationDreamink
   ```

2. **Instalar Dependencias**
   ```bash
   pnpm install
   ```

3. **Iniciar Servidor de Desarrollo**
   ```bash
   pnpm dev
   ```
   Visita [http://localhost:3030](http://localhost:3030) para ver la presentación.

4. **Verificar que Todo Funciona**
   ```bash
   # Probar construcción de producción
   pnpm build

   # Probar exportación a PDF
   pnpm export
   ```

### Tu Primera Contribución

¿Buscas una buena primera contribución? Busca issues etiquetados como:
- `good-first-issue` - Tareas amigables para principiantes
- `help-wanted` - Tareas donde necesitamos asistencia
- `documentation` - Mejoras de documentación

**Pasos para tu primera contribución**:
1. Navega por los [issues existentes](https://github.com/Dreamink-SNPP/PresentationDreamink/issues)
2. Comenta en un issue para expresar interés
3. Espera confirmación del mantenedor
4. Haz fork del repositorio y crea una rama
5. Realiza tus cambios
6. Envía un pull request

## Flujo de Trabajo de Desarrollo

### Convenciones de Nombres de Ramas

Crea nombres de ramas descriptivos usando estos prefijos:

- `feature/descripcion` - Nuevas características o mejoras
  - Ejemplo: `feature/agregar-diagrama-metodologia`
- `fix/descripcion` - Correcciones de errores
  - Ejemplo: `fix/error-formato-titulo`
- `docs/descripcion` - Actualizaciones de documentación
  - Ejemplo: `docs/actualizar-guia-instalacion`
- `style/descripcion` - Cambios de estilo y visuales
  - Ejemplo: `style/mejorar-transiciones-diapositivas`

```bash
# Crear una nueva rama desde main
git checkout main
git pull origin main
git checkout -b feature/nombre-de-tu-caracteristica
```

### Realizando Cambios

1. **Hacer cambios enfocados y lógicos**
   - Mantén los cambios pequeños y enfocados en un solo propósito
   - Evita mezclar múltiples cambios no relacionados en un PR

2. **Probar exhaustivamente**
   - Ejecuta `pnpm dev` y verifica tus cambios visualmente
   - Prueba `pnpm build` para asegurar que la construcción de producción funciona
   - Prueba `pnpm export` si cambiaste el contenido de las diapositivas
   - Verifica el modo presentador (presiona `O` en modo dev)

3. **Actualizar documentación**
   - Actualiza el README si agregaste nuevas características
   - Agrega notas del presentador para diapositivas complejas
   - Actualiza STYLE_GUIDE.md si introdujiste nuevos patrones

4. **Asegurar consistencia bilingüe**
   - Si editas archivos de documentación, actualiza tanto las versiones en inglés como en español
   - Si solo hablas un idioma, marca tu PR con la etiqueta `needs-translation`

## Convenciones de Commits

Seguimos [Conventional Commits](https://www.conventionalcommits.org/) para un historial de commits claro y semántico.

### Formato

```
tipo(alcance): descripción breve

[cuerpo opcional]

[pie opcional]
```

### Tipos

- `feat` - Nueva característica o mejora
- `fix` - Corrección de error
- `docs` - Cambios en documentación
- `style` - Estilos, formato, cambios de CSS
- `refactor` - Refactorización de código sin cambio de comportamiento
- `test` - Agregar o actualizar pruebas
- `chore` - Tareas de mantenimiento, dependencias

### Alcances

Usa el nombre de la sección de diapositiva o componente:

- `introduccion`, `objetivos`, `metodologia`, `conclusion`
- `readme`, `contributing`, `security`
- `deps` - Dependencias
- `build` - Configuración de construcción

### Ejemplos

```bash
# Nuevo contenido
git commit -m "feat(metodologia): agregar diagrama de metodología de investigación"

# Corrección de error
git commit -m "fix(introduccion): corregir formato del título de tesis"

# Documentación
git commit -m "docs(readme): actualizar instrucciones de instalación"

# Estilo
git commit -m "style(objetivos): mejorar espaciado de viñetas"

# Múltiples archivos
git commit -m "feat(slides): agregar animaciones click a todas las secciones"
```

## Proceso de Pull Request

### Antes de Enviar

Asegúrate de que tu pull request:
- [ ] Sigue la convención de nombres de ramas
- [ ] Usa mensajes de commit convencionales
- [ ] Incluye pruebas o pasos de verificación
- [ ] Actualiza documentación si es necesario
- [ ] Mantiene consistencia bilingüe (si aplica)
- [ ] No tiene errores o advertencias en consola
- [ ] Pasa todas las construcciones (`pnpm build`, `pnpm export`)

### Enviando un Pull Request

1. **Enviar tus cambios**
   ```bash
   git push origin nombre-de-tu-rama
   ```

2. **Crear Pull Request en GitHub**
   - Haz clic en "New Pull Request"
   - Completa la plantilla de PR completamente
   - Vincula issues relacionados (ej., "Closes #123")
   - Agrega etiquetas apropiadas

3. **Responder a retroalimentación**
   - Atiende los comentarios de revisores prontamente
   - Realiza los cambios solicitados
   - Re-solicita revisión después de actualizaciones

4. **Esperar aprobación**
   - Los PRs requieren al menos 1 aprobación de mantenedor
   - Cambios mayores pueden requerir revisión del supervisor académico
   - Una vez aprobado, los mantenedores fusionarán tu PR

### Lista de Verificación de PR

Tu pull request debe incluir:

- **Descripción Clara**: Qué cambios se hicieron y por qué
- **Evidencia de Pruebas**: Capturas de pantalla o descripción de cómo probaste
- **Issues Relacionados**: Enlace a cualquier issue relacionado
- **Cambios Disruptivos**: Nota si esto introduce cambios disruptivos
- **Actualizaciones Bilingües**: Confirma que ambas versiones de idioma se actualizaron (si aplica)

## Guías de Pruebas

### Pruebas Manuales

Siempre realiza estas pruebas antes de enviar:

1. **Servidor de Desarrollo**
   ```bash
   pnpm dev
   ```
   - Verifica que las diapositivas se muestren correctamente
   - Verifica que las animaciones funcionen como se espera
   - Prueba navegación entre diapositivas
   - Revisa en modos claro y oscuro (presiona `D`)

2. **Construcción de Producción**
   ```bash
   pnpm build
   ```
   - Asegura que la construcción se complete sin errores
   - Verifica la salida de construcción en el directorio `dist/`

3. **Funcionalidad de Exportación**
   ```bash
   # Exportación a PDF
   pnpm export

   # Exportación a PowerPoint
   pnpm export --format pptx

   # Exportación a imágenes PNG
   pnpm export --format png
   ```
   - Verifica que las exportaciones se completen exitosamente
   - Verifica la calidad de los archivos exportados

4. **Modo Presentador**
   - Ejecuta `pnpm dev`
   - Presiona `O` para abrir modo presentador
   - Verifica que las notas del presentador aparezcan correctamente
   - Prueba funcionalidad del temporizador

5. **Pruebas Multi-navegador**
   - Prueba en Chrome, Firefox y Safari (si está disponible)
   - Verifica comportamiento responsivo en diferentes tamaños de pantalla

### Pruebas de Accesibilidad

Asegura que tus cambios mantengan accesibilidad:

- **Contraste de Color**: Usa colores de `STYLE_GUIDE.md` (cumple WCAG 2.1 AA)
- **Legibilidad de Texto**: Tamaño mínimo de fuente 16px, altura de línea adecuada
- **Navegación por Teclado**: Prueba usando solo teclado (flechas, espacio, tab)
- **Lector de Pantalla**: Prueba con lector de pantalla si es posible
- **Texto Alternativo**: Proporciona atributos `alt` para imágenes

### Verificaciones de Calidad

Antes de enviar, verifica:

- No hay errores JavaScript en la consola del navegador
- No hay enlaces rotos en documentación
- Las imágenes cargan correctamente
- Las animaciones no causan problemas de rendimiento
- El código sigue patrones existentes en `STYLE_GUIDE.md`

## Colaboración Académica

### Proporcionando Retroalimentación Académica

Usa la plantilla de issue "Presentation Feedback" para proporcionar aportes académicos:

**Áreas de enfoque**:
- Rigor metodológico y diseño de investigación
- Precisión de contenido y alineación teórica
- Claridad de argumentos y conclusiones
- Efectividad visual de presentación de datos
- Completitud y precisión de citas
- Alineación con estándares institucionales

**Guías de Retroalimentación**:
- Sé constructivo y específico
- Proporciona evidencia o referencias cuando sea posible
- Sugiere mejoras, no solo críticas
- Respeta el contexto y limitaciones académicas
- Mantén discurso académico profesional

### Requisitos de Citas

Si usas este trabajo en contextos académicos, por favor cita como:

```
Cardozo, F. & Álvarez, A. (2025). Dispersión Organizacional de
las Estructuras Dramáticas en Guionistas del Departamento Central.
[Presentación de Tesis]. Centro Tecnológico de Formación Profesional
Paraguay-Japón.
```

Para BibTeX:
```bibtex
@misc{cardozo2025dreamink,
  title={Dispersi\'on Organizacional de las Estructuras Dram\'aticas en Guionistas del Departamento Central},
  author={Cardozo, Fernando and Álvarez, Alberto},
  year={2025},
  type={Presentación de Tesis},
  institution={Centro Tecnol\'ogico de Formaci\'on Profesional Paraguay-Jap\'on},
  note={Disponible en: https://github.com/Dreamink-SNPP/PresentationDreamink}
}
```

### Oportunidades de Colaboración

Para contribuciones académicas significativas o colaboraciones de investigación:

- **Contacto**: fernanditocardozo@protonmail.com, alberto.alvarez@example.com
- **Temas**: Metodologías de guionismo, estructuras dramáticas, herramientas de pre-escritura
- **Co-autoría**: Discutido caso por caso para contribuciones sustanciales
- **Reconocimiento**: Contribuyentes reconocidos en diapositivas de presentación

## Guías Bilingües

Este proyecto mantiene documentación en inglés y español por igual.

### Actualizando Documentación

Al editar archivos con contrapartes `.es.md`:

1. **Actualizar primero versión en inglés**
   - Realiza tus cambios al archivo en inglés
   - Haz commit con mensaje descriptivo

2. **Actualizar versión en español**
   - Traduce cambios al archivo en español
   - Mantén terminología consistente
   - Mantén términos técnicos precisos

3. **Verificar enlaces entre idiomas**
   - Asegura que los enlaces de cambio de idioma funcionen
   - Verifica todas las referencias internas

4. **Nota en descripción de PR**
   - Menciona que ambas versiones fueron actualizadas
   - Solicita revisión bilingüe si es posible

### Ayuda con Traducción

Si solo puedes contribuir en un idioma:

1. Realiza tus cambios en tu idioma preferido
2. Agrega etiqueta `needs-translation` a tu PR
3. En la descripción del PR, nota qué archivo necesita traducción
4. Los mantenedores o contribuyentes bilingües asistirán

### Consistencia de Terminología

**Inglés → Español referencia**:
- Contributing → Contribución
- Pull Request → Solicitud de Cambios / Pull Request
- Issue → Problema / Issue
- Commit → Commit
- Deployment → Despliegue
- Build → Construcción

## Revisión de Código

### Qué Buscan los Revisores

Los revisores verificarán:

1. **Cumplimiento del Código de Conducta**
   - Comunicación respetuosa
   - Colaboración profesional

2. **Adherencia a Guía de Estilo**
   - Sigue paleta de colores Dreamink
   - Usa clases CSS apropiadas
   - Mantiene tono académico

3. **Formato de Mensaje de Commit**
   - Estructura de commit convencional
   - Mensajes claros y descriptivos

4. **Consistencia Bilingüe**
   - Ambas versiones de idioma actualizadas
   - Traducciones precisas
   - Referencias cruzadas funcionando

5. **Cobertura de Pruebas**
   - Pruebas manuales realizadas
   - Construcción y exportación verificadas
   - No se introdujeron regresiones

6. **Completitud de Documentación**
   - README actualizado si es necesario
   - Notas del presentador agregadas
   - Comentarios de código (donde sea necesario)

7. **Precisión Académica** (para cambios de contenido)
   - Citas formateadas apropiadamente
   - Metodología sólida
   - Contenido alineado con tesis

### Cronograma de Revisión

- **Revisión inicial**: 2-3 días hábiles
- **Respuesta a retroalimentación**: Por favor responde dentro de 1 semana
- **Aprobación final**: 1-2 días después de toda retroalimentación atendida

**Nota**: Los plazos de tesis pueden afectar cronogramas de revisión. Comunicaremos cualquier cronograma urgente.

### Requisitos de Aprobación

- **Cambios menores** (errores tipográficos, correcciones pequeñas): 1 aprobación de mantenedor
- **Cambios mayores** (contenido, estructura): 2 aprobaciones de mantenedores
- **Cambios de metodología**: Se requiere aprobación del supervisor académico

## Reconocimiento

¡Valoramos y reconocemos todas las contribuciones!

### Cómo se Reconoce a los Contribuyentes

1. **Historial de Git**: Tus contribuciones están registradas permanentemente
2. **Diapositiva de Agradecimientos**: Contribuyentes significativos son reconocidos en la presentación
3. **Archivo CONTRIBUTORS**: Mantenemos una lista de contribuyentes (si se crea)
4. **Citas Académicas**: Contribuciones académicas pueden ser citadas en el trabajo de tesis
5. **Perfil de GitHub**: Las contribuciones aparecen en tu perfil de GitHub

### Criterios de Reconocimiento

- **Mencionado en diapositiva**: Contribuciones que mejoran significativamente contenido o metodología
- **Listado en CONTRIBUTORS**: Todos los pull requests fusionados
- **Cita académica**: Contribuciones intelectuales sustanciales a la investigación

**Optar por no participar**: Si prefieres no ser reconocido públicamente, por favor nótalo en tu PR.

## ¿Preguntas o Necesitas Ayuda?

- **Preguntas Generales**: Abre una [GitHub Discussion](https://github.com/Dreamink-SNPP/PresentationDreamink/discussions)
- **Reportes de Errores**: Usa la plantilla de issue Bug Report
- **Ideas de Características**: Usa la plantilla de issue Feature Request
- **Retroalimentación Académica**: Usa la plantilla de issue Presentation Feedback
- **Problemas de Seguridad**: Ve nuestra [Política de Seguridad](SECURITY.es.md)
- **Consultas Privadas**: Envía un correo directamente a los mantenedores

## Recursos Adicionales

- [Documentación de Slidev](https://sli.dev/)
- [Guía de Markdown](https://sli.dev/guide/syntax.html)
- [Animaciones de Slidev](https://sli.dev/guide/animations.html)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)

---

## Acerca de Este Proyecto

Este repositorio es parte de un proyecto de investigación de tesis académica:

**Título**: Dispersión Organizacional de las Estructuras Dramáticas en Guionistas del Departamento Central

**Autores**: Ing. Fernando Cardozo & Alberto Álvarez

**Supervisor Académico**: Prof. Lic. Moisés Ávalos

**Institución**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Año**: 2025

**Licencia**: Licencia MIT

---

**¡Gracias por contribuir al avance de la investigación y metodología de guionismo!**
