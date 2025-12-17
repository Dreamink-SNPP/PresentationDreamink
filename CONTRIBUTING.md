# Contributing to PresentationDreamink

> **Languages:** [English](CONTRIBUTING.md) | [Español](CONTRIBUTING.es.md)

Thank you for your interest in contributing to our academic thesis presentation project! This guide will help you understand how to contribute effectively and maintain the quality and integrity of this scholarly work.

## Table of Contents

1. [About This Project](#about-this-project)
2. [Ways to Contribute](#ways-to-contribute)
3. [Getting Started](#getting-started)
4. [Development Workflow](#development-workflow)
5. [Commit Conventions](#commit-conventions)
6. [Pull Request Process](#pull-request-process)
7. [Testing Guidelines](#testing-guidelines)
8. [Academic Collaboration](#academic-collaboration)
9. [Bilingual Guidelines](#bilingual-guidelines)
10. [Code Review](#code-review)
11. [Recognition](#recognition)

## About This Project

This repository hosts an academic thesis presentation developed with [Slidev](https://sli.dev/), focusing on the **systematization of the pre-writing process for audiovisual scripts** in the Central Department of Paraguay.

**Title**: Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department

**Authors**: Ing. Fernando Cardozo & Alberto Álvarez

**Academic Supervisor**: Prof. Lic. Moisés Ávalos

**Institution**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Year**: 2025

Before contributing, please read our [Code of Conduct](CODE_OF_CONDUCT.md) to understand our community standards.

## Ways to Contribute

We welcome various types of contributions:

### Technical Contributions
- Fix bugs in presentation build or export processes
- Improve styling and visual layouts
- Enhance animations and transitions
- Optimize performance and loading times
- Improve accessibility features

### Content Contributions
- Improve clarity and readability of slides
- Suggest better visualizations for data
- Enhance presenter notes
- Correct typos or formatting issues
- Refine academic language

### Documentation Contributions
- Improve README clarity and completeness
- Translate documentation to other languages
- Add helpful examples and tutorials
- Update setup and deployment guides
- Create video tutorials or walkthroughs

### Academic Contributions
- Provide scholarly feedback on methodology
- Suggest relevant academic references
- Review content accuracy and rigor
- Offer peer review from subject matter experts
- Contribute to theoretical framework discussions

## Getting Started

### Prerequisites

Before you begin, ensure you have:

- **Node.js** v20 or higher ([download](https://nodejs.org/))
- **pnpm** package manager ([install instructions](https://pnpm.io/installation))
- **Git** for version control
- A **GitHub account**
- Basic knowledge of Markdown and Slidev (optional but helpful)

### Initial Setup

1. **Fork the Repository**
   ```bash
   # Click the "Fork" button on GitHub, then clone your fork:
   git clone https://github.com/YOUR-USERNAME/PresentationDreamink.git
   cd PresentationDreamink
   ```

2. **Install Dependencies**
   ```bash
   pnpm install
   ```

3. **Start Development Server**
   ```bash
   pnpm dev
   ```
   Visit [http://localhost:3030](http://localhost:3030) to view the presentation.

4. **Verify Everything Works**
   ```bash
   # Test production build
   pnpm build

   # Test PDF export
   pnpm export
   ```

### Your First Contribution

Looking for a good first contribution? Check for issues labeled:
- `good-first-issue` - Beginner-friendly tasks
- `help-wanted` - Tasks where we need assistance
- `documentation` - Documentation improvements

**Steps for your first contribution**:
1. Browse [existing issues](https://github.com/Dreamink-SNPP/PresentationDreamink/issues)
2. Comment on an issue to express interest
3. Wait for maintainer confirmation
4. Fork the repository and create a branch
5. Make your changes
6. Submit a pull request

## Development Workflow

### Branch Naming Conventions

Create descriptive branch names using these prefixes:

- `feature/description` - New features or enhancements
  - Example: `feature/add-methodology-diagram`
- `fix/description` - Bug fixes
  - Example: `fix/title-formatting-error`
- `docs/description` - Documentation updates
  - Example: `docs/update-installation-guide`
- `style/description` - Styling and visual changes
  - Example: `style/improve-slide-transitions`

```bash
# Create a new branch from main
git checkout main
git pull origin main
git checkout -b feature/your-feature-name
```

### Making Changes

1. **Make focused, logical changes**
   - Keep changes small and focused on a single purpose
   - Avoid mixing multiple unrelated changes in one PR

2. **Test thoroughly**
   - Run `pnpm dev` and verify your changes visually
   - Test `pnpm build` to ensure production build works
   - Test `pnpm export` if you changed slide content
   - Check presenter mode (press `O` in dev mode)

3. **Update documentation**
   - Update README if you added new features
   - Add presenter notes for complex slides
   - Update STYLE_GUIDE.md if you introduced new patterns

4. **Ensure bilingual consistency**
   - If you edit documentation files, update both English and Spanish versions
   - If you only speak one language, mark your PR with `needs-translation` label

## Commit Conventions

We follow [Conventional Commits](https://www.conventionalcommits.org/) for clear and semantic commit history.

### Format

```
type(scope): brief description

[optional body]

[optional footer]
```

### Types

- `feat` - New feature or enhancement
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Styling, formatting, CSS changes
- `refactor` - Code refactoring without behavior change
- `test` - Adding or updating tests
- `chore` - Maintenance tasks, dependencies

### Scopes

Use the slide section name or component:

- `introduction`, `objectives`, `methodology`, `conclusion`
- `readme`, `contributing`, `security`
- `deps` - Dependencies
- `build` - Build configuration

### Examples

```bash
# New content
git commit -m "feat(methodology): add research methodology diagram"

# Bug fix
git commit -m "fix(introduction): correct thesis title formatting"

# Documentation
git commit -m "docs(readme): update installation instructions"

# Styling
git commit -m "style(objectives): improve bullet point spacing"

# Multiple files
git commit -m "feat(slides): add click animations to all sections"
```

## Pull Request Process

### Before Submitting

Ensure your pull request:
- [ ] Follows the branch naming convention
- [ ] Uses conventional commit messages
- [ ] Includes tests or verification steps
- [ ] Updates documentation if needed
- [ ] Maintains bilingual consistency (if applicable)
- [ ] Has no console errors or warnings
- [ ] Passes all builds (`pnpm build`, `pnpm export`)

### Submitting a Pull Request

1. **Push your changes**
   ```bash
   git push origin your-branch-name
   ```

2. **Create Pull Request on GitHub**
   - Click "New Pull Request"
   - Fill out the PR template completely
   - Link related issues (e.g., "Closes #123")
   - Add appropriate labels

3. **Respond to feedback**
   - Address reviewer comments promptly
   - Make requested changes
   - Re-request review after updates

4. **Await approval**
   - PRs require at least 1 maintainer approval
   - Major changes may require academic supervisor review
   - Once approved, maintainers will merge your PR

### PR Checklist

Your pull request should include:

- **Clear Description**: What changes were made and why
- **Testing Evidence**: Screenshots or description of how you tested
- **Related Issues**: Link to any related issues
- **Breaking Changes**: Note if this introduces breaking changes
- **Bilingual Updates**: Confirm both language versions updated (if applicable)

## Testing Guidelines

### Manual Testing

Always perform these tests before submitting:

1. **Development Server**
   ```bash
   pnpm dev
   ```
   - Verify slides display correctly
   - Check animations work as expected
   - Test navigation between slides
   - Review in both light and dark modes (press `D`)

2. **Production Build**
   ```bash
   pnpm build
   ```
   - Ensure build completes without errors
   - Check build output in `dist/` directory

3. **Export Functionality**
   ```bash
   # PDF export
   pnpm export

   # PowerPoint export
   pnpm export --format pptx

   # PNG images export
   pnpm export --format png
   ```
   - Verify exports complete successfully
   - Check quality of exported files

4. **Presenter Mode**
   - Run `pnpm dev`
   - Press `O` to open presenter mode
   - Verify presenter notes appear correctly
   - Test timer functionality

5. **Cross-browser Testing**
   - Test in Chrome, Firefox, and Safari (if available)
   - Verify responsive behavior at different screen sizes

### Accessibility Testing

Ensure your changes maintain accessibility:

- **Color Contrast**: Use colors from `STYLE_GUIDE.md` (WCAG 2.1 AA compliant)
- **Text Readability**: Minimum font size 16px, adequate line height
- **Keyboard Navigation**: Test using only keyboard (arrows, space, tab)
- **Screen Reader**: Test with a screen reader if possible
- **Alternative Text**: Provide `alt` attributes for images

### Quality Checks

Before submitting, verify:

- No JavaScript errors in browser console
- No broken links in documentation
- Images load correctly
- Animations don't cause performance issues
- Code follows existing patterns in `STYLE_GUIDE.md`

## Academic Collaboration

### Providing Academic Feedback

Use the "Presentation Feedback" issue template to provide scholarly input:

**Focus areas**:
- Methodological rigor and research design
- Content accuracy and theoretical alignment
- Clarity of arguments and conclusions
- Visual effectiveness of data presentation
- Citation completeness and accuracy
- Alignment with institutional standards

**Feedback Guidelines**:
- Be constructive and specific
- Provide evidence or references when possible
- Suggest improvements, not just criticisms
- Respect the academic context and constraints
- Maintain professional scholarly discourse

### Citation Requirements

If you use this work in academic contexts, please cite as:

```
Cardozo, F. & Álvarez, A. (2025). Organizational Dispersion of
Dramatic Structures in Screenwriters from the Central Department.
[Thesis Presentation]. Centro Tecnológico de Formación Profesional
Paraguay-Japón.
```

For BibTeX:
```bibtex
@misc{cardozo2025dreamink,
  title={Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department},
  author={Cardozo, Fernando and Álvarez, Alberto},
  year={2025},
  type={Thesis Presentation},
  institution={Centro Tecnol\'ogico de Formaci\'on Profesional Paraguay-Jap\'on},
  note={Available at: https://github.com/Dreamink-SNPP/PresentationDreamink}
}
```

### Collaboration Opportunities

For significant academic contributions or research collaborations:

- **Contact**: fernando.cardozo@example.com, alberto.alvarez@example.com
- **Topics**: Screenwriting methodologies, dramatic structures, pre-writing tools
- **Co-authorship**: Discussed on a case-by-case basis for substantial contributions
- **Acknowledgment**: Contributors acknowledged in presentation slides

## Bilingual Guidelines

This project maintains equal English and Spanish documentation.

### Updating Documentation

When editing files with `.es.md` counterparts:

1. **Update English version first**
   - Make your changes to the English file
   - Commit with descriptive message

2. **Update Spanish version**
   - Translate changes to Spanish file
   - Maintain consistent terminology
   - Keep technical terms accurate

3. **Verify cross-language links**
   - Ensure language switcher links work
   - Check all internal references

4. **Note in PR description**
   - Mention that both versions were updated
   - Request bilingual review if possible

### Translation Help

If you can only contribute in one language:

1. Make your changes in your preferred language
2. Add `needs-translation` label to your PR
3. In PR description, note which file needs translation
4. Maintainers or bilingual contributors will assist

### Terminology Consistency

**English → Spanish reference**:
- Contributing → Contribución
- Pull Request → Solicitud de Cambios / Pull Request
- Issue → Problema / Issue
- Commit → Commit
- Deployment → Despliegue
- Build → Construcción

## Code Review

### What Reviewers Look For

Reviewers will check:

1. **Code of Conduct Compliance**
   - Respectful communication
   - Professional collaboration

2. **Style Guide Adherence**
   - Follows Dreamink color palette
   - Uses proper CSS classes
   - Maintains academic tone

3. **Commit Message Format**
   - Conventional commit structure
   - Clear, descriptive messages

4. **Bilingual Consistency**
   - Both language versions updated
   - Accurate translations
   - Working cross-references

5. **Test Coverage**
   - Manual testing performed
   - Build and export verified
   - No regressions introduced

6. **Documentation Completeness**
   - README updated if needed
   - Presenter notes added
   - Code comments (where necessary)

7. **Academic Accuracy** (for content changes)
   - Citations properly formatted
   - Methodology sound
   - Content aligns with thesis

### Review Timeline

- **Initial review**: 2-3 business days
- **Feedback response**: Please respond within 1 week
- **Final approval**: 1-2 days after all feedback addressed

**Note**: Thesis deadlines may affect review timelines. We'll communicate any urgent timelines.

### Approval Requirements

- **Minor changes** (typos, small fixes): 1 maintainer approval
- **Major changes** (content, structure): 2 maintainer approvals
- **Methodology changes**: Academic supervisor approval required

## Recognition

We value and acknowledge all contributions!

### How Contributors are Recognized

1. **Git History**: Your contributions are permanently recorded
2. **Acknowledgments Slide**: Significant contributors are acknowledged in the presentation
3. **CONTRIBUTORS File**: We maintain a list of contributors (if created)
4. **Academic Citations**: Scholarly contributions may be cited in thesis work
5. **GitHub Profile**: Contributions appear on your GitHub profile

### Acknowledgment Criteria

- **Mentioned in slide**: Contributions that significantly improve content or methodology
- **Listed in CONTRIBUTORS**: All merged pull requests
- **Academic citation**: Substantial intellectual contributions to research

**Opt-out**: If you prefer not to be acknowledged publicly, please note this in your PR.

## Questions or Need Help?

- **General Questions**: Open a [GitHub Discussion](https://github.com/Dreamink-SNPP/PresentationDreamink/discussions)
- **Bug Reports**: Use the Bug Report issue template
- **Feature Ideas**: Use the Feature Request issue template
- **Academic Feedback**: Use the Presentation Feedback issue template
- **Security Issues**: See our [Security Policy](SECURITY.md)
- **Private Inquiries**: Email the maintainers directly

## Additional Resources

- [Slidev Documentation](https://sli.dev/)
- [Markdown Guide](https://sli.dev/guide/syntax.html)
- [Slidev Animations](https://sli.dev/guide/animations.html)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)

---

## About This Project

This repository is part of an academic thesis research project:

**Title**: Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department

**Authors**: Ing. Fernando Cardozo & Alberto Álvarez

**Academic Supervisor**: Prof. Lic. Moisés Ávalos

**Institution**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Year**: 2025

**License**: MIT License

---

**Thank you for contributing to advancing screenwriting research and methodology!**
