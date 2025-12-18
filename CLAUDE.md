# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev-based academic thesis presentation for "Dispersión organizativa de estructuras dramáticas en los guionistas del Departamento Central" (Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department). The presentation is built using Slidev, a modern presentation framework for developers that uses Markdown files.

## Key Commands

### Development

```bash
# Start development server (opens automatically in browser)
pnpm dev
```

The development server runs at http://localhost:3030 and automatically reloads on file changes.

### Build and Export

```bash
# Build static site for production
pnpm build

# Export to PDF (default format)
pnpm export

# Export to PowerPoint
pnpm export --format pptx

# Export to PNG images (one per slide)
pnpm export --format png
```

### Package Management

This project uses `pnpm` as the package manager. Always use `pnpm install` to install dependencies, not `npm` or `yarn`.

## Architecture and Structure

### Modular Slide System

The presentation uses a **modular architecture** where content is split into separate markdown files rather than having all slides in one file. This is critical to understand:

- **Main file:** `slides.md` - Acts as the orchestrator that imports all sections. **DO NOT edit content directly in this file.**
- **Content files:** `slides/` directory contains 8 numbered markdown files where all actual content lives.
- Each section file (`01-portada.md`, `02-introduccion.md`, etc.) is imported via the `src:` directive in `slides.md`.

### Why This Matters

When editing content:
1. **Always edit files in `slides/` directory**, never `slides.md`
2. The `slides.md` file should only be modified to add/remove/reorder sections or change global configuration
3. Each section file is self-contained and can be developed independently
4. This structure enables parallel collaboration where different people can work on different sections without conflicts

### Configuration System

Slidev configuration lives in the YAML frontmatter of `slides.md`:
- Theme: Uses the `seriph` theme (professional/academic style)
- Language: Set to `es-ES` (Spanish)
- Duration: 45 minutes
- Transitions: `slide-left`
- MDC syntax: Enabled for advanced markdown features

### Styling Architecture

The project has two separate styling systems that serve different purposes:

1. **Academic styles** (`styles/custom.css`): Generic academic presentation styles with navy/gold color palette
2. **Dreamink brand styles** (`STYLE_GUIDE.md`): Brand-specific colors (`#1B3C53` primary, `#234C6A` secondary dark, `#D2C1B6` secondary light, etc.)

**Important:** The `custom.css` currently uses academic colors, but `STYLE_GUIDE.md` defines the official Dreamink brand colors. When implementing brand-specific styling, reference the color values from `STYLE_GUIDE.md`, not `custom.css`.

### Git LFS Integration

The project uses Git Large File Storage (LFS) for binary assets. All files in `public/` matching image, video, font, and document patterns (see `.gitattributes`) are tracked via LFS. When adding media assets:
- Place them in `public/` directory
- They'll automatically be tracked by Git LFS (if you have Git LFS installed: `git lfs install`)
- Reference them in slides with absolute paths (e.g., `/logo.png`)

**LFS-tracked file types**: Images (jpg, png, gif, svg, webp), videos (mp4, mov, avi, webm), documents (pdf, pptx, docx), fonts (ttf, otf, woff, woff2), and archives (zip, tar, gz)

## Content Editing Patterns

### Slide File Structure

Each slide file contains:
- Markdown content with headings, lists, text
- YAML frontmatter for slide-specific layouts (e.g., `layout: cover`, `layout: section`)
- HTML comments with presenter notes at the bottom
- Support for Vue components via `<div>` tags with classes

### Common Layouts

- `layout: cover` - Title/cover slides with centered content
- `layout: section` - Section divider slides
- `layout: default` - Standard content slides (default if not specified)
- `layout: center` - Centered content slides

### Presenter Notes

Add notes visible only in presenter mode using HTML comments:

```markdown
<!--
Presenter notes here
- Bullet points for talking points
- Duration estimates
-->
```

Access presenter mode by pressing `O` during presentation.

### Keyboard Shortcuts (Development Mode)

When testing with `pnpm dev`, these shortcuts are essential:
- `→` / `Space` - Next slide
- `←` - Previous slide
- `↑` / `↓` - First / Last slide
- `O` - Open presenter mode
- `F` - Full screen
- `D` - Toggle dark mode
- `G` - Go to specific slide

## Testing and Verification

Before committing changes, always verify:

1. **Development mode**: `pnpm dev` - Check slides display correctly, animations work
2. **Production build**: `pnpm build` - Ensure build completes without errors
3. **Export functionality**: `pnpm export` (PDF), `pnpm export --format pptx` (PowerPoint), `pnpm export --format png` (images)
4. **Presenter mode**: Press `O` during development to verify presenter notes
5. **Cross-browser**: Test in Chrome, Firefox, Safari when possible
6. **Console**: Check browser console for errors or warnings

## Deployment

The project includes pre-configured deployment settings for:
- **Netlify:** `netlify.toml` - Build command: `npm run build`, publish: `dist/`
- **Vercel:** `vercel.json` - Same build settings with SPA routing

Both platforms will automatically deploy on push to the repository.

## Important Constraints

1. **Never use npm or yarn** - This project requires pnpm for dependency resolution
2. **Don't edit slides.md content** - Only edit section files in `slides/`
3. **Use Git LFS** - Large files must go through LFS (configured in `.gitattributes`)
4. **Language is Spanish** - All presentation content is in Spanish (`es-ES`)
5. **Theme compatibility** - When adding custom components, ensure they work with the Seriph theme
6. **Bilingual documentation** - Files with `.es.md` counterparts must be updated in both languages. If you can only edit one language version, note this in your commit message or PR.

## Commit Conventions

This project uses simple, descriptive commit messages starting with action verbs:

**Format**: `Action verb + description of what was done`

**Common patterns**:
- `Add [feature/file/content]` - For new additions
- `Change [what was changed]` - For modifications
- `Remove [what was removed]` - For deletions
- `Fix [what was fixed]` - For bug fixes

**Examples from this project**:
```bash
Add README in English version
Change original README ES for EN version
Add real content for every slide
Fix title formatting error
Remove demo content directories from Slidev
```

Keep messages clear, concise, and in imperative mood (e.g., "Add feature" not "Added feature").

## Slidev-Specific Features

### Click Animations

```markdown
<div v-click>
Content appears on click
</div>
```

### Two-Click Animations

```markdown
<div v-click="1">First click</div>
<div v-click="2">Second click</div>
```

### Code Highlighting

Slidev supports syntax highlighting for code blocks. Specify the language after the triple backticks:

```markdown
```javascript
const example = "code";
\```
```

### MDC Syntax

MDC (Markdown Components) is enabled. This allows for advanced component usage within markdown.

## Accessibility Requirements

When making changes, maintain accessibility standards defined in `STYLE_GUIDE.md`:
- All color combinations meet WCAG 2.1 AA standards
- Primary (`#1B3C53`) on white: AAA (11.2:1 contrast)
- Minimum font size: 16px with adequate line height (1.6-1.8)
- Provide `alt` attributes for all images
- Ensure keyboard navigation works (arrows, space, tab)

## Project Context

- **Authors:** Ing. Fernando Cardozo (fernanditocardozo@protonmail.com), Alberto Álvarez
- **Supervisor:** Prof. Lic. Moisés Ávalos
- **Institution:** Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP
- **Location:** San Lorenzo, Paraguay
- **Year:** 2025
- **License:** MIT License
- **Research focus:** Systematization of pre-writing process for audiovisual scripts, examining tools and methodologies adapted to screenwriters in the Central Department of Paraguay

The presentation covers 5 chapters: Introductory Framework, Theoretical Framework, Methodological Framework, Analytical Framework, and Software Requirements.

## Additional Resources

- Full contributing guidelines: See `CONTRIBUTING.md` / `CONTRIBUTING.es.md`
- Code of Conduct: See `CODE_OF_CONDUCT.md` / `CODE_OF_CONDUCT.es.md`
- Security Policy: See `SECURITY.md` / `SECURITY.es.md`
- Style Guide: See `STYLE_GUIDE.md` for complete Dreamink brand colors and design patterns
- Slidev Documentation: https://sli.dev/
