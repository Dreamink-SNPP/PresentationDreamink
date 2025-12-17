# Presentación de Tesis - Slidev

Presentación académica de tesis desarrollada con [Slidev](https://sli.dev/), una herramienta de presentaciones moderna y potente para desarrolladores.

## Estructura del Proyecto

```
PresentationDreamink/
├── slides/              # Secciones de la presentación (editar aquí)
│   ├── 01-portada.md
│   ├── 02-introduccion.md
│   ├── 03-planteamiento-problema.md
│   ├── 04-objetivos.md
│   ├── 05-justificacion.md
│   ├── 06-marco-metodologico.md
│   ├── 07-conclusion.md
│   └── 08-agradecimientos.md
├── public/              # Recursos estáticos (imágenes, logos, etc.)
├── styles/              # Estilos personalizados
│   └── custom.css
├── slides.md            # Archivo principal (NO editar, solo importa secciones)
└── package.json
```

## Inicio Rápido

### Prerrequisitos

- [Node.js](https://nodejs.org/) (v20 o superior)
- [pnpm](https://pnpm.io/) (gestor de paquetes)

### Instalación

```bash
# Instalar dependencias
pnpm install
```

### Desarrollo

```bash
# Iniciar servidor de desarrollo
pnpm dev
```

Visita [http://localhost:3030](http://localhost:3030) para ver la presentación.

La presentación se recargará automáticamente al guardar cambios en los archivos.

### Construcción

```bash
# Construir para producción (genera archivos estáticos)
pnpm build
```

### Exportación

```bash
# Exportar a PDF
pnpm export

# Exportar a PPTX (PowerPoint)
pnpm export --format pptx

# Exportar a PNG (imágenes por diapositiva)
pnpm export --format png
```

## Edición de Contenido

### Estructura de Secciones

La presentación está organizada en 8 secciones independientes dentro de `slides/`:

1. **01-portada.md** - Portada con título, autor, institución
2. **02-introduccion.md** - Introducción y contexto general
3. **03-planteamiento-problema.md** - Problema de investigación
4. **04-objetivos.md** - Objetivos general y específicos
5. **05-justificacion.md** - Justificación del estudio
6. **06-marco-metodologico.md** - Metodología de investigación
7. **07-conclusion.md** - Conclusiones y hallazgos
8. **08-agradecimientos.md** - Agradecimientos y cierre

### Cómo Editar

1. Abre el archivo de la sección que deseas editar en `slides/`
2. Modifica el contenido en formato Markdown
3. Guarda el archivo
4. Los cambios se reflejarán automáticamente en el navegador

### Sintaxis de Markdown

Slidev utiliza Markdown extendido con características especiales:

```markdown
# Título Principal (h1)
## Subtítulo (h2)
### Título de Sección (h3)

- Lista con viñetas
- Segundo elemento

1. Lista numerada
2. Segundo elemento

**Texto en negrita**
*Texto en cursiva*

`código en línea`

\```javascript
// Bloque de código
const ejemplo = "Hola Mundo";
\```
```

### Características Avanzadas

#### Animaciones Click
```markdown
<div v-click>
Este contenido aparece al hacer click
</div>
```

#### Notas del Presentador
```markdown
<!--
Estas son notas solo visibles en modo presentador
-->
```

#### Layouts Personalizados
```markdown
---
layout: center
class: text-center
---

# Contenido centrado
```

Consulta la [documentación de Slidev](https://sli.dev/guide/syntax.html) para más características.

## Gestión de Recursos (Imágenes, Logos)

### Agregar Imágenes

1. Coloca tus archivos en la carpeta `public/`
2. Referencia desde cualquier slide con ruta absoluta:

```markdown
![Descripción](/imagen.png)

<!-- O con HTML -->
<img src="/logo-universidad.png" alt="Logo" width="200">
```

### Git LFS (Large File Storage)

Este proyecto está configurado para usar Git LFS para archivos grandes:

```bash
# Instalar Git LFS (solo una vez)
git lfs install

# Los archivos en public/ se rastearán automáticamente
# según la configuración en .gitattributes
```

Tipos de archivo rastreados por Git LFS:
- Imágenes: jpg, png, gif, svg, webp
- Videos: mp4, mov, avi, webm
- Documentos: pdf, pptx, docx
- Fuentes: ttf, otf, woff, woff2

## Colaboración

### Flujo de Trabajo Recomendado

Para trabajar en equipo sin conflictos:

1. **Asignar secciones**: Cada colaborador trabaja en archivos diferentes
   - Persona A: `01-portada.md`, `02-introduccion.md`, `03-planteamiento-problema.md`
   - Persona B: `04-objetivos.md`, `05-justificacion.md`, `06-marco-metodologico.md`
   - Ambos: `07-conclusion.md`, `08-agradecimientos.md`

2. **Usar ramas** (opcional pero recomendado):
   ```bash
   # Crear rama para tu sección
   git checkout -b feature/introduccion

   # Hacer commits
   git add slides/02-introduccion.md
   git commit -m "feat(introduccion): agregar contexto histórico"

   # Subir cambios
   git push origin feature/introduccion
   ```

3. **Pull Requests**: Revisar cambios antes de fusionar a `main`

### Convenciones de Commits

```
feat(sección): descripción breve
fix(sección): corrección de error
docs(readme): actualizar documentación
style(css): ajustar estilos
```

Ejemplos:
- `feat(objetivos): agregar objetivos específicos`
- `fix(metodologia): corregir tabla de muestra`
- `docs(readme): actualizar instrucciones de instalación`

## Personalización

### Tema

El tema actual es **Seriph** (profesional, académico).

Para cambiar de tema, edita `slides.md`:
```yaml
---
theme: seriph  # Cambia a 'default' u otro tema
---
```

Temas disponibles: [Slidev Theme Gallery](https://sli.dev/resources/theme-gallery)

### Estilos Personalizados

Edita `styles/custom.css` para ajustar:
- Colores institucionales
- Tipografía
- Espaciado
- Componentes personalizados

### Configuración

Edita el frontmatter en `slides.md` para ajustar:
```yaml
---
title: Tu Título         # Título de la presentación
duration: 45min          # Duración estimada
transition: slide-left   # Tipo de transición
background: url          # Imagen de fondo
---
```

## Modo Presentador

Al ejecutar `pnpm dev`, puedes abrir el modo presentador:

1. Presiona `O` para abrir el modo presentador en otra ventana
2. La ventana principal muestra la presentación
3. La ventana del presentador muestra:
   - Diapositiva actual
   - Próxima diapositiva
   - Notas del presentador
   - Temporizador

## Atajos de Teclado

En modo presentación:

- `→` / `Espacio`: Siguiente diapositiva
- `←`: Diapositiva anterior
- `↑` / `↓`: Primera / Última diapositiva
- `O`: Modo presentador
- `F`: Pantalla completa
- `D`: Modo oscuro
- `G`: Ir a diapositiva específica

## Despliegue

### Netlify / Vercel

Este proyecto incluye configuración para despliegue automático:

- **Netlify**: Configurado en `netlify.toml`
- **Vercel**: Configurado en `vercel.json`

Conecta tu repositorio y el despliegue será automático en cada push.

### Manual

```bash
# Construir
pnpm build

# Los archivos estarán en ./dist
# Sube el contenido de dist/ a tu servidor
```

## Recursos

- [Documentación de Slidev](https://sli.dev/)
- [Sintaxis de Markdown](https://sli.dev/guide/syntax.html)
- [Animaciones](https://sli.dev/guide/animations.html)
- [Temas](https://sli.dev/resources/theme-gallery)
- [GitHub de Slidev](https://github.com/slidevjs/slidev)

## Comunidad

¡Damos la bienvenida a contribuciones! Por favor revisa nuestras guías comunitarias:

- [Code of Conduct](CODE_OF_CONDUCT.md) | [Código de Conducta](CODE_OF_CONDUCT.es.md)
- [Contributing Guide](CONTRIBUTING.md) | [Guía de Contribución](CONTRIBUTING.es.md)
- [Security Policy](SECURITY.md) | [Política de Seguridad](SECURITY.es.md)

Para reportar problemas o solicitudes, utiliza nuestras [plantillas de issues](.github/ISSUE_TEMPLATE/).

## Soporte

Si encuentras problemas:

1. Revisa la [documentación oficial](https://sli.dev/)
2. Busca en los [issues de GitHub](https://github.com/slidevjs/slidev/issues)
3. Consulta con tu co-investigador

---

**Desarrollado con [Slidev](https://sli.dev/)** - Presentaciones para desarrolladores
