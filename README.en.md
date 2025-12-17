# Thesis Presentation - Slidev

> **Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department**

Academic thesis presentation developed with [Slidev](https://sli.dev/), a modern and powerful presentation tool for developers.

## About This Presentation

This presentation accompanies a thesis research project that explores the **systematization of the pre-writing process for audiovisual scripts**. The study examines tools and methodologies adapted to different contexts and needs of screenwriters, with emphasis on local practices in the Central Department of Paraguay.

### Research Overview

The thesis constitutes a fundamental practice to guarantee the coherence and viability of audiovisual projects before final literary composition. It covers five chapters:

- **Introductory Framework** - Problem contextualization
- **Theoretical Framework** - Conceptual foundations
- **Methodological Framework** - Research design
- **Analytical Framework** - Findings and data analysis
- **Software Requirements** - Architectural documentation

### Authors

- **Ing. Fernando Cardozo**
- **Alberto Álvarez**

**Academic Supervisor:** Prof. Lic. Moisés Ávalos

**Institution:** Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / Servicio Nacional de Promoción Profesional (SNPP)

**Location:** San Lorenzo, Paraguay

**Year:** 2025

---

## Presentation Structure

The presentation is organized into 8 sections:

1. **Cover** (`01-portada.md`) - Title, authors, institution
2. **Introduction** (`02-introduccion.md`) - General introduction and context
3. **Problem Statement** (`03-planteamiento-problema.md`) - Research problem
4. **Objectives** (`04-objetivos.md`) - General and specific objectives
5. **Justification** (`05-justificacion.md`) - Study justification
6. **Methodological Framework** (`06-marco-metodologico.md`) - Research methodology
7. **Conclusion** (`07-conclusion.md`) - Conclusions and findings
8. **Acknowledgments** (`08-agradecimientos.md`) - Thanks and closing

---

## Quick Start

### Prerequisites

- [Node.js](https://nodejs.org/) (v20 or higher)
- [pnpm](https://pnpm.io/) (package manager)

### Installation

```bash
# Install dependencies
pnpm install
```

### Development

```bash
# Start development server
pnpm dev
```

Visit [http://localhost:3030](http://localhost:3030) to view the presentation.

The presentation will automatically reload when you save changes to files.

### Build

```bash
# Build for production (generates static files)
pnpm build
```

### Export

```bash
# Export to PDF
pnpm export

# Export to PPTX (PowerPoint)
pnpm export --format pptx

# Export to PNG (images per slide)
pnpm export --format png
```

---

## Project Structure

```
PresentationDreamink/
├── slides/              # Presentation sections (edit here)
│   ├── 01-portada.md
│   ├── 02-introduccion.md
│   ├── 03-planteamiento-problema.md
│   ├── 04-objetivos.md
│   ├── 05-justificacion.md
│   ├── 06-marco-metodologico.md
│   ├── 07-conclusion.md
│   └── 08-agradecimientos.md
├── public/              # Static resources (images, logos, etc.)
├── styles/              # Custom styles
│   └── custom.css
├── slides.md            # Main file (DO NOT edit, only imports sections)
└── package.json
```

---

## Editing Content

### How to Edit

1. Open the section file you want to edit in `slides/`
2. Modify the content in Markdown format
3. Save the file
4. Changes will be automatically reflected in the browser

### Markdown Syntax

Slidev uses extended Markdown with special features:

```markdown
# Main Title (h1)
## Subtitle (h2)
### Section Title (h3)

- Bulleted list
- Second item

1. Numbered list
2. Second item

**Bold text**
*Italic text*

`inline code`

```javascript
// Code block
const example = "Hello World";
```
```

### Advanced Features

#### Click Animations
```markdown
<div v-click>
This content appears on click
</div>
```

#### Presenter Notes
```markdown
<!--
These are notes only visible in presenter mode
-->
```

#### Custom Layouts
```markdown
---
layout: center
class: text-center
---

# Centered content
```

Check the [Slidev documentation](https://sli.dev/guide/syntax.html) for more features.

---

## Resource Management (Images, Logos)

### Adding Images

1. Place your files in the `public/` folder
2. Reference from any slide with absolute path:

```markdown
![Description](/image.png)

<!-- Or with HTML -->
<img src="/university-logo.png" alt="Logo" width="200">
```

### Git LFS (Large File Storage)

This project is configured to use Git LFS for large files:

```bash
# Install Git LFS (only once)
git lfs install

# Files in public/ will be tracked automatically
# according to configuration in .gitattributes
```

File types tracked by Git LFS:
- Images: jpg, png, gif, svg, webp
- Videos: mp4, mov, avi, webm
- Documents: pdf, pptx, docx
- Fonts: ttf, otf, woff, woff2

---

## Presenter Mode

When running `pnpm dev`, you can open presenter mode:

1. Press `O` to open presenter mode in another window
2. The main window shows the presentation
3. The presenter window shows:
   - Current slide
   - Next slide
   - Presenter notes
   - Timer

---

## Keyboard Shortcuts

In presentation mode:

- `→` / `Space`: Next slide
- `←`: Previous slide
- `↑` / `↓`: First / Last slide
- `O`: Presenter mode
- `F`: Full screen
- `D`: Dark mode
- `G`: Go to specific slide

---

## Deployment

### Netlify / Vercel

This project includes configuration for automatic deployment:

- **Netlify**: Configured in `netlify.toml`
- **Vercel**: Configured in `vercel.json`

Connect your repository and deployment will be automatic on each push.

### Manual

```bash
# Build
pnpm build

# Files will be in ./dist
# Upload the contents of dist/ to your server
```

---

## Customization

### Theme

The current theme is **Seriph** (professional, academic).

To change theme, edit `slides.md`:
```yaml
---
theme: seriph  # Change to 'default' or another theme
---
```

Available themes: [Slidev Theme Gallery](https://sli.dev/resources/theme-gallery)

### Custom Styles

Edit `styles/custom.css` to adjust:
- Institutional colors
- Typography
- Spacing
- Custom components

---

## Collaboration

This project is open for collaboration under the MIT License. Feel free to:

- Fork the repository
- Submit pull requests
- Report issues
- Suggest improvements

### Recommended Workflow

For team collaboration without conflicts:

1. **Assign sections**: Each collaborator works on different files
2. **Use branches** (optional but recommended):
   ```bash
   # Create branch for your section
   git checkout -b feature/introduction

   # Make commits
   git add slides/02-introduccion.md
   git commit -m "feat(introduction): add historical context"

   # Push changes
   git push origin feature/introduction
   ```

3. **Pull Requests**: Review changes before merging to `main`

### Commit Conventions

```
feat(section): brief description
fix(section): bug fix
docs(readme): update documentation
style(css): adjust styles
```

Examples:
- `feat(objectives): add specific objectives`
- `fix(methodology): correct sample table`
- `docs(readme): update installation instructions`

---

## Resources

- [Slidev Documentation](https://sli.dev/)
- [Markdown Syntax](https://sli.dev/guide/syntax.html)
- [Animations](https://sli.dev/guide/animations.html)
- [Themes](https://sli.dev/resources/theme-gallery)
- [Slidev GitHub](https://github.com/slidevjs/slidev)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Ing. Fernando Cardozo and Alberto Álvarez

---

## Support

If you encounter issues:

1. Check the [official documentation](https://sli.dev/)
2. Search in [GitHub issues](https://github.com/slidevjs/slidev/issues)
3. Contact the authors

---

**Developed with [Slidev](https://sli.dev/)** - Presentations for developers
