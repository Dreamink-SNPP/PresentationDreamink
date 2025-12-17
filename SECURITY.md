# Security Policy

> **Languages:** [English](SECURITY.md) | [Español](SECURITY.es.md)

## Overview

This security policy covers dependency security, deployment security, and academic data protection for the PresentationDreamink project. While this is a presentation repository rather than traditional software, we maintain security best practices for dependencies, deployments, and research data.

## Supported Versions

We actively monitor security updates for all project dependencies:

| Component | Version | Status |
|-----------|---------|--------|
| Slidev CLI | ^52.11.0 | ✅ Supported |
| Vue | ^3.5.25 | ✅ Supported |
| Node.js | v20+ | ✅ Supported |
| Theme Seriph | latest | ✅ Supported |

Dependencies are regularly updated to address security vulnerabilities.

## Reporting a Vulnerability

### Dependency Vulnerabilities

If you discover a security vulnerability in project dependencies:

**1. Check Severity**
- Run `pnpm audit` to verify the vulnerability
- Review the vulnerability details and potential impact

**2. Report Privately**
- **Preferred**: Use [GitHub Security Advisory](https://github.com/Dreamink-SNPP/PresentationDreamink/security/advisories/new) (create a private security advisory)
- **Alternative**: Email the maintainers directly:
  - Fernando Cardozo: fernando.cardozo@example.com
  - Alberto Álvarez: alberto.alvarez@example.com

**3. Provide Details**
Include in your report:
- Affected package name and version
- Type of vulnerability (e.g., XSS, prototype pollution, etc.)
- Potential impact on the presentation
- Suggested fix or mitigation (if known)
- Steps to reproduce (if applicable)

**Expected Response**: Within 48 hours

### Content or Academic Data Concerns

For concerns related to academic data privacy, research integrity, or content security:

- **Email**: Contact the academic supervisor
  - Prof. Lic. Moisés Ávalos: moises.avalos@example.com
- **Include**:
  - Nature of the concern
  - Affected files or content
  - Suggested remediation
  - Privacy implications (if applicable)

**Expected Response**: Within 1 week

### Deployment Security Issues

For security issues related to Netlify or Vercel deployments:

- Create a private GitHub issue or email the maintainers
- **Include**:
  - Deployment URL where issue was observed
  - Type of security concern (e.g., exposed headers, HTTPS issues)
  - Observed behavior
  - Potential security risk

**Expected Response**: Within 72 hours

## Security Best Practices

### For Contributors

#### Dependency Management
- Keep `package.json` dependencies up to date
- Review changes to `pnpm-lock.yaml` in pull requests
- Run `pnpm audit` before submitting pull requests
- Report vulnerable dependencies immediately through proper channels
- Avoid adding unnecessary dependencies

#### Code Safety
- **Never commit** API keys, tokens, or secrets
- Avoid user input injection in slide content
- Review third-party integrations and scripts carefully
- Use only trusted npm packages from reputable maintainers
- Verify package integrity before installation

#### Data Protection
- No personal participant data should be committed to the repository
- All examples must be anonymized
- Research data should be stored separately from the presentation
- Follow institutional research ethics guidelines

### For Deployment

#### Static Site Security

**HTTPS Configuration**
- All deployments must use HTTPS
- HTTP requests should redirect to HTTPS
- Enable HSTS (HTTP Strict Transport Security)

**Security Headers**
Configure the following security headers in deployment settings:

```toml
# netlify.toml
[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
    Referrer-Policy = "strict-origin-when-cross-origin"
    Content-Security-Policy = "default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval'; style-src 'self' 'unsafe-inline';"
```

**Build Security**
- Review build logs for exposed secrets or sensitive information
- Use environment variables for any configuration
- Enable Netlify/Vercel security features (e.g., HTTPS, DDoS protection)
- Regularly review deployment access logs

### Academic Data Protection

#### Research Data Management
- **Thesis research data** is stored separately from this repository
- Only anonymized, publicly shareable examples appear in the presentation
- No participant identification information is included
- All data handling follows institutional research ethics guidelines

#### Intellectual Property
- Respect copyright in all images, fonts, and content
- Properly attribute all sources and references
- Maintain academic citation integrity
- Obtain necessary permissions for third-party content

## Security Monitoring

We actively monitor security through multiple channels:

### Automated Alerts
- **GitHub Dependabot**: Automated dependency vulnerability alerts
- **npm Audit Reports**: Regular scanning of npm packages
- **Slidev Security Announcements**: Monitoring official Slidev security updates
- **Node.js Security Releases**: Tracking Node.js CVEs and patches

### Manual Reviews
- **Quarterly Dependency Updates**: Review and update all dependencies
- **Security Headers Validation**: Regular checks of deployment security headers
- **Access Log Reviews**: Periodic review of deployment platform access logs
- **Third-Party Integration Audits**: Assessment of external scripts and resources

## Vulnerability Disclosure Timeline

When a vulnerability is reported, we follow this timeline:

1. **Report Received**: Acknowledge receipt within 48 hours
2. **Assessment**: Complete severity evaluation within 1 week
3. **Fix Development**: Timeline based on severity
   - **Critical**: Immediate action (24-48 hours)
   - **High**: Within 1 week
   - **Medium**: Within 2 weeks
   - **Low**: Next maintenance cycle
4. **Disclosure**: Public disclosure after fix is deployed and users are notified

## Security Updates

### Notification Channels

Security updates are communicated through:
- GitHub Security Advisories (for critical issues)
- Repository README updates
- Email notifications to known contributors (for critical vulnerabilities)
- Commit messages with security fix details

### Update Documentation

All security updates are documented with:
- CVE numbers (when applicable)
- Affected versions
- Mitigation steps
- References to security advisories
- Commit SHA references

## Acknowledgments

We appreciate responsible disclosure and will acknowledge security contributions. Contributors will be recognized in:

- Acknowledgments slide of the presentation (unless anonymity is preferred)
- GitHub Security Advisories
- Project documentation

**Security Contributors Hall of Thanks**:
- *List will be updated as security contributions are received*

## Resources

### Security Documentation
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [Node.js Security](https://nodejs.org/en/security/)
- [npm Security Advisories](https://docs.npmjs.com/about-security-advisories)
- [Slidev GitHub Security](https://github.com/slidevjs/slidev/security)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

### Reporting Tools
- Run `pnpm audit` to scan for known vulnerabilities
- Use `pnpm audit fix` to automatically fix patchable issues
- Check [npm advisories](https://www.npmjs.com/advisories) for known issues

## Contact

### Security Team
- **Fernando Cardozo**: fernando.cardozo@example.com
- **Alberto Álvarez**: alberto.alvarez@example.com

### Academic Supervisor
- **Prof. Lic. Moisés Ávalos**: moises.avalos@example.com

### Institution
**Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP**
- San Lorenzo, Paraguay

---

## About This Project

This repository is part of an academic thesis research project:

**Title**: Organizational Dispersion of Dramatic Structures in Screenwriters from the Central Department

**Authors**: Ing. Fernando Cardozo & Alberto Álvarez

**Academic Supervisor**: Prof. Lic. Moisés Ávalos

**Institution**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Year**: 2025

**License**: MIT License
