# Español técnico claro · 0.1.1

## Contenido y compatibilidad

La carpeta skills/espanol-tecnico-claro es una skill de instrucciones en formato Agent Skills. SKILL.md contiene todas las reglas, la configuración inicial, los perfiles regionales y el glosario. agents/openai.yaml contiene metadatos opcionales para herramientas OpenAI; los demás clientes pueden ignorarlo.

No necesita Python, API, red ni un modelo concreto para redactar. La búsqueda de fuentes solo es necesaria cuando el encargo pide verificación externa. La compatibilidad depende de la aplicación que ejecuta el modelo, no del modelo por sí solo. Validación estructural realizada; no se ha probado la instalación en cada producto.

## Aplicaciones compatibles con Agent Skills

Extrae el archivo y usa la carpeta skills/espanol-tecnico-claro completa. Instálala en el directorio de skills o mediante el importador documentado por tu aplicación. Mantén el nombre SKILL.md y el nombre de la carpeta. No adjuntes el archivo .zip esperando que todas las aplicaciones lo importen: el archivo es de distribución y cada importador puede exigir otro formato.

En Codex local, la documentación consultada indica ~/.agents/skills como ubicación personal. Copia allí la carpeta completa. Actívala con $espanol-tecnico-claro; si no aparece, reinicia el cliente.

En ChatGPT, la creación y selección dependen de la superficie y las funciones habilitadas. En una superficie que ofrezca el creador de skills, solicita registrar esta skill a partir de SKILL.md. Comprueba que aparece en el selector antes de considerarla instalada. Las skills locales del entorno de ejecución no garantizan registro permanente en la cuenta. Para distribución mediante plugins, sigue el empaquetado y registro del producto; este archivo no constituye un plugin publicado.

Para otros agentes, consulta su documentación de Agent Skills. No se garantiza importación directa en productos sin soporte de ese formato.

## Aplicaciones sin soporte nativo

Copia el cuerpo de SKILL.md, sin su cabecera YAML, en las instrucciones del proyecto, asistente o agente cuando el producto lo permita. También puedes adjuntar SKILL.md y pedir que se aplique en una conversación. Esto reutiliza las instrucciones, pero no equivale a instalación ni activación automática de una skill. Respeta los límites de longitud y prioridad del producto.

## Uso

- Revisa este procedimiento con Español técnico claro. Modo controlado, es-ES. Conserva condiciones, excepciones y comandos.
- Explica este informe con Español técnico claro. Modo claro y audiencia no técnica.
- Adapta este texto a es-MX, tratamiento usted. Conserva etiquetas de interfaz y términos corporativos aprobados.

Valores iniciales: es-ES, modo claro, tú, audiencia técnica. Los perfiles de otros países tienen un contrato de configuración y están pendientes de validación local. El glosario contiene propuestas, no equivalencias corporativas ya aprobadas.

## Comprobación tras instalar

Prueba: «Reintenta solo si el estado es 503 y la operación es idempotente, salvo que se haya agotado el límite. El botón se llama Ingresar. Podría existir un fallo de red.»

Comprueba que conserva ambas condiciones y la excepción, mantiene Ingresar y no convierte la hipótesis del fallo de red en una certeza. Repite con la variante y el tratamiento seleccionados. Esta comprobación no acredita conformidad normativa.

## Fuentes de formato e instalación

- https://agentskills.io/specification
- https://learn.chatgpt.com/docs/build-skills
