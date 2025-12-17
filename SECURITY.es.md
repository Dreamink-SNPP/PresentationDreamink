# Política de Seguridad

> **Idiomas:** [English](SECURITY.md) | [Español](SECURITY.es.md)

## Descripción General

Esta política de seguridad cubre la seguridad de dependencias, seguridad de despliegue y protección de datos académicos para el proyecto PresentationDreamink. Aunque este es un repositorio de presentación en lugar de software tradicional, mantenemos las mejores prácticas de seguridad para dependencias, despliegues y datos de investigación.

## Versiones Soportadas

Monitoreamos activamente las actualizaciones de seguridad para todas las dependencias del proyecto:

| Componente | Versión | Estado |
|-----------|---------|--------|
| Slidev CLI | ^52.11.0 | ✅ Soportado |
| Vue | ^3.5.25 | ✅ Soportado |
| Node.js | v20+ | ✅ Soportado |
| Theme Seriph | latest | ✅ Soportado |

Las dependencias se actualizan regularmente para abordar vulnerabilidades de seguridad.

## Reportar una Vulnerabilidad

### Vulnerabilidades de Dependencias

Si descubre una vulnerabilidad de seguridad en las dependencias del proyecto:

**1. Verificar Severidad**
- Ejecute `pnpm audit` para verificar la vulnerabilidad
- Revise los detalles de la vulnerabilidad y el impacto potencial

**2. Reportar Privadamente**
- **Preferido**: Use [GitHub Security Advisory](https://github.com/Dreamink-SNPP/PresentationDreamink/security/advisories/new) (crear un aviso de seguridad privado)
- **Alternativa**: Envíe un correo electrónico directamente a los mantenedores:
  - Fernando Cardozo: fernando.cardozo@example.com
  - Alberto Álvarez: alberto.alvarez@example.com

**3. Proporcionar Detalles**
Incluya en su reporte:
- Nombre del paquete afectado y versión
- Tipo de vulnerabilidad (ej., XSS, contaminación de prototipos, etc.)
- Impacto potencial en la presentación
- Corrección o mitigación sugerida (si la conoce)
- Pasos para reproducir (si aplica)

**Respuesta Esperada**: Dentro de 48 horas

### Preocupaciones sobre Contenido o Datos Académicos

Para preocupaciones relacionadas con privacidad de datos académicos, integridad de investigación o seguridad de contenido:

- **Correo Electrónico**: Contacte al supervisor académico
  - Prof. Lic. Moisés Ávalos: moises.avalos@example.com
- **Incluya**:
  - Naturaleza de la preocupación
  - Archivos o contenido afectado
  - Remediación sugerida
  - Implicaciones de privacidad (si aplica)

**Respuesta Esperada**: Dentro de 1 semana

### Problemas de Seguridad de Despliegue

Para problemas de seguridad relacionados con despliegues en Netlify o Vercel:

- Cree un issue privado en GitHub o envíe un correo a los mantenedores
- **Incluya**:
  - URL de despliegue donde se observó el problema
  - Tipo de preocupación de seguridad (ej., encabezados expuestos, problemas HTTPS)
  - Comportamiento observado
  - Riesgo de seguridad potencial

**Respuesta Esperada**: Dentro de 72 horas

## Mejores Prácticas de Seguridad

### Para Contribuyentes

#### Gestión de Dependencias
- Mantenga las dependencias de `package.json` actualizadas
- Revise los cambios a `pnpm-lock.yaml` en pull requests
- Ejecute `pnpm audit` antes de enviar pull requests
- Reporte dependencias vulnerables inmediatamente a través de los canales apropiados
- Evite agregar dependencias innecesarias

#### Seguridad del Código
- **Nunca haga commit** de claves API, tokens o secretos
- Evite la inyección de entrada de usuario en contenido de diapositivas
- Revise cuidadosamente integraciones y scripts de terceros
- Use solo paquetes npm confiables de mantenedores reputados
- Verifique la integridad del paquete antes de la instalación

#### Protección de Datos
- No se debe hacer commit de datos personales de participantes al repositorio
- Todos los ejemplos deben ser anonimizados
- Los datos de investigación deben almacenarse separadamente de la presentación
- Siga las pautas de ética de investigación institucionales

### Para Despliegue

#### Seguridad de Sitio Estático

**Configuración HTTPS**
- Todos los despliegues deben usar HTTPS
- Las solicitudes HTTP deben redirigir a HTTPS
- Habilitar HSTS (HTTP Strict Transport Security)

**Encabezados de Seguridad**
Configure los siguientes encabezados de seguridad en la configuración de despliegue:

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

**Seguridad de Construcción**
- Revise los registros de construcción para secretos expuestos o información sensible
- Use variables de entorno para cualquier configuración
- Habilite las características de seguridad de Netlify/Vercel (ej., HTTPS, protección DDoS)
- Revise regularmente los registros de acceso de despliegue

### Protección de Datos Académicos

#### Gestión de Datos de Investigación
- **Los datos de investigación de tesis** se almacenan separadamente de este repositorio
- Solo aparecen ejemplos anonimizados y compartibles públicamente en la presentación
- No se incluye información de identificación de participantes
- Todo el manejo de datos sigue las pautas de ética de investigación institucionales

#### Propiedad Intelectual
- Respete los derechos de autor en todas las imágenes, fuentes y contenido
- Atribuya apropiadamente todas las fuentes y referencias
- Mantenga la integridad de citas académicas
- Obtenga los permisos necesarios para contenido de terceros

## Monitoreo de Seguridad

Monitoreamos activamente la seguridad a través de múltiples canales:

### Alertas Automatizadas
- **GitHub Dependabot**: Alertas automatizadas de vulnerabilidades de dependencias
- **Reportes de Auditoría npm**: Escaneo regular de paquetes npm
- **Anuncios de Seguridad de Slidev**: Monitoreo de actualizaciones de seguridad oficiales de Slidev
- **Lanzamientos de Seguridad de Node.js**: Seguimiento de CVEs y parches de Node.js

### Revisiones Manuales
- **Actualizaciones Trimestrales de Dependencias**: Revisión y actualización de todas las dependencias
- **Validación de Encabezados de Seguridad**: Verificaciones regulares de encabezados de seguridad de despliegue
- **Revisiones de Registros de Acceso**: Revisión periódica de registros de acceso de la plataforma de despliegue
- **Auditorías de Integración de Terceros**: Evaluación de scripts y recursos externos

## Cronograma de Divulgación de Vulnerabilidades

Cuando se reporta una vulnerabilidad, seguimos este cronograma:

1. **Reporte Recibido**: Confirmar recepción dentro de 48 horas
2. **Evaluación**: Completar evaluación de severidad dentro de 1 semana
3. **Desarrollo de Corrección**: Cronograma basado en severidad
   - **Crítico**: Acción inmediata (24-48 horas)
   - **Alto**: Dentro de 1 semana
   - **Medio**: Dentro de 2 semanas
   - **Bajo**: Próximo ciclo de mantenimiento
4. **Divulgación**: Divulgación pública después de que se despliegue la corrección y se notifique a los usuarios

## Actualizaciones de Seguridad

### Canales de Notificación

Las actualizaciones de seguridad se comunican a través de:
- Avisos de Seguridad de GitHub (para problemas críticos)
- Actualizaciones del README del repositorio
- Notificaciones por correo electrónico a contribuyentes conocidos (para vulnerabilidades críticas)
- Mensajes de commit con detalles de correcciones de seguridad

### Documentación de Actualizaciones

Todas las actualizaciones de seguridad se documentan con:
- Números CVE (cuando aplica)
- Versiones afectadas
- Pasos de mitigación
- Referencias a avisos de seguridad
- Referencias de SHA de commits

## Reconocimientos

Apreciamos la divulgación responsable y reconoceremos las contribuciones de seguridad. Los contribuyentes serán reconocidos en:

- Diapositiva de agradecimientos de la presentación (a menos que se prefiera anonimato)
- Avisos de Seguridad de GitHub
- Documentación del proyecto

**Salón de Agradecimientos de Contribuyentes de Seguridad**:
- *La lista se actualizará a medida que se reciban contribuciones de seguridad*

## Recursos

### Documentación de Seguridad
- [Mejores Prácticas de Seguridad de GitHub](https://docs.github.com/en/code-security)
- [Seguridad de Node.js](https://nodejs.org/en/security/)
- [Avisos de Seguridad de npm](https://docs.npmjs.com/about-security-advisories)
- [Seguridad de GitHub de Slidev](https://github.com/slidevjs/slidev/security)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

### Herramientas de Reporte
- Ejecute `pnpm audit` para escanear vulnerabilidades conocidas
- Use `pnpm audit fix` para corregir automáticamente problemas parchables
- Verifique [avisos de npm](https://www.npmjs.com/advisories) para problemas conocidos

## Contacto

### Equipo de Seguridad
- **Fernando Cardozo**: fernando.cardozo@example.com
- **Alberto Álvarez**: alberto.alvarez@example.com

### Supervisor Académico
- **Prof. Lic. Moisés Ávalos**: moises.avalos@example.com

### Institución
**Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP**
- San Lorenzo, Paraguay

---

## Acerca de Este Proyecto

Este repositorio es parte de un proyecto de investigación de tesis académica:

**Título**: Dispersión Organizacional de las Estructuras Dramáticas en Guionistas del Departamento Central

**Autores**: Ing. Fernando Cardozo & Alberto Álvarez

**Supervisor Académico**: Prof. Lic. Moisés Ávalos

**Institución**: Centro Tecnológico de Formación Profesional Paraguay-Japón (CTFP-PJ) / SNPP

**Año**: 2025

**Licencia**: Licencia MIT
