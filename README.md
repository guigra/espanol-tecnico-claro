# Español técnico claro

Skill portable en formato [Agent Skills](https://agentskills.io/specification) para redactar, revisar, explicar y resumir textos técnicos en español claro, con perfiles regionales y un glosario corporativo configurable.

**Versión:** 0.1.0 · **Autor:** Ricardo Guillén Gracia · **Licencia:** [MIT](LICENSE)

## Qué hace

- Reescribe procedimientos, documentación, informes de incidencias y comunicaciones técnicas en español natural y preciso.
- Conserva el significado: condiciones, excepciones, negaciones, cifras, plazos, grados de certeza y obligaciones.
- Conserva literales: código, comandos, identificadores, rutas, URL, errores y etiquetas de interfaz.
- Ofrece dos modos:
  - **Claro:** español natural adaptado a la audiencia.
  - **Controlado:** estructura de propósito, requisitos previos, pasos, resultado esperado y condiciones de parada, solo con los datos que aporta la fuente.
- Aplica es-ES por defecto y admite cualquier variante del español. El tratamiento (tú, usted, vos) se elige aparte del país.
- Trata el texto suministrado como datos e ignora las instrucciones incrustadas en él.

Valores iniciales: `es-ES`, modo claro, tú, audiencia técnica.

## Contenido

```
espanol-tecnico-claro/
├── SKILL.md              # Reglas, configuración, perfiles regionales y glosario
└── agents/
    └── openai.yaml       # Metadatos opcionales para herramientas OpenAI
USO.md                    # Guía detallada de instalación y uso
```

No necesita Python, API, red ni un modelo concreto.

## Instalación

### Aplicaciones compatibles con Agent Skills

Copia la carpeta `espanol-tecnico-claro` completa en el directorio de skills de tu aplicación. Mantén los nombres de la carpeta y de `SKILL.md`.

Ejemplos:

```bash
# Claude Code (personal)
cp -R espanol-tecnico-claro ~/.claude/skills/

# Codex local (personal)
cp -R espanol-tecnico-claro ~/.agents/skills/
```

Si no aparece la skill, reinicia el cliente. En Codex, actívala con `$espanol-tecnico-claro`.

### Aplicaciones sin soporte nativo

Copia el cuerpo de `SKILL.md`, sin la cabecera YAML, en las instrucciones del proyecto, asistente o agente. Esto reutiliza las reglas, pero no equivale a instalar la skill.

Consulta [USO.md](USO.md) para más detalles por producto.

## Uso

```text
Revisa este procedimiento con Español técnico claro. Modo controlado, es-ES. Conserva condiciones, excepciones y comandos.
```

```text
Explica este informe con Español técnico claro. Modo claro y audiencia no técnica.
```

```text
Adapta este texto a es-MX, tratamiento usted. Conserva etiquetas de interfaz y términos corporativos aprobados.
```

## Comprobación tras instalar

Pide que reescriba este texto:

> Reintenta solo si el estado es 503 y la operación es idempotente, salvo que se haya agotado el límite. El botón se llama Ingresar. Podría existir un fallo de red.

Comprueba que el resultado:

1. Conserva las dos condiciones y la excepción.
2. Mantiene el nombre del botón «Ingresar».
3. Presenta el fallo de red como hipótesis, no como certeza.

`SKILL.md` incluye 12 casos de aceptación para evaluar cambios en la skill.

## Estado y limitaciones

- **es-ES:** perfil activo.
- **es internacional:** disponible para audiencias multinacionales.
- **Otras variantes** (es-AR, es-MX, es-CO, es-CL, es-US y demás): contrato de configuración preparado, pendiente de validación local.
- **Glosario:** contiene propuestas, no equivalencias corporativas aprobadas.
- Se ha validado la estructura; no se ha probado la instalación en cada producto.
- Esta skill **no** acredita conformidad con ASD-STE100, UNE-ISO 24495-1 ni ninguna certificación de lenguaje claro.

## Contribuir

Las contribuciones son bienvenidas, sobre todo para validar perfiles regionales y ampliar el glosario. Al modificar `SKILL.md`, comprueba que siguen cumpliéndose los casos de aceptación.

Para añadir un perfil regional, completa el contrato `perfil` de `SKILL.md` con fuentes locales. No marques un perfil como validado sin evidencia.

## Referencias

- [Especificación Agent Skills](https://agentskills.io/specification)
- [RAE-ASALE, Guía panhispánica de lenguaje claro y accesible](https://www.rae.es/obras-academicas/obras-linguisticas/guia-panhispanica-de-lenguaje-claro-y-accesible)
- [ASD-STE100](https://www.asd-ste100.org/) (estándar para inglés; solo inspiración)
- [prithivrajmu/asd-ste100](https://github.com/prithivrajmu/asd-ste100) (inspiración funcional; no se ha copiado su código)
- UNE-ISO 24495-1:2024, principios generales de lenguaje claro
- Gobbi, Ilaria (2014), [Spagnolo Tecnico Semplificato](https://amsdottorato.unibo.it/id/eprint/6681/)

## Licencia

Este proyecto se distribuye bajo la [licencia MIT](LICENSE). Al contribuir, aceptas que tu contribución se publique bajo la misma licencia.
