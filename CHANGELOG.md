# Registro de cambios

Todos los cambios relevantes de este proyecto se documentan en este archivo.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y el proyecto usa [versionado semántico](https://semver.org/lang/es/).

## [Sin publicar]

## [0.1.1] - 2026-11-16

### Cambiado

- La skill se mueve a `skills/espanol-tecnico-claro/`, la ruta estándar que rastrean los directorios de skills.

### Añadido

- Instalación con `npx skills add guigra/espanol-tecnico-claro`.
- Plugin y marketplace de Claude Code en `.claude-plugin/`.

## [0.1.0] - 2026-11-16

### Añadido

- Skill `espanol-tecnico-claro` en formato Agent Skills.
- Modos claro y controlado.
- Perfil regional es-ES activo y perfil es internacional.
- Contrato de configuración para otras variantes regionales, pendientes de validación local.
- Glosario corporativo inicial con propuestas no aprobadas.
- 12 casos de aceptación para evaluar cambios.
- Metadatos opcionales para herramientas OpenAI (`agents/openai.yaml`).
- Guía de instalación y uso (`USO.md`) y `README.md`.
- Licencia MIT.
