# Skills recomendadas (de terceros)

Estas Skills pertenecen a sus autores y se usan bajo su licencia. Revisa siempre el repositorio original para obtener la versión más reciente.

## Teach, de Matt Pocock (licencia MIT)
- Original: https://github.com/mattpocock/skills (carpeta `skills/productivity/teach`)
- Qué hace: convierte a Claude en tu tutor personal a lo largo de varias sesiones, con lecciones, hojas de referencia y registro de lo aprendido.
- Instalación en Claude Desktop: [teach.zip](teach.zip) (copia de la versión del 13/11/2026, incluye su LICENSE). Úsala en Cowork con una carpeta seleccionada.
- Uso: `/teach Quiero aprender [tema]. Mi nivel es [nivel]. Tengo 20 minutos al día.`
- Nota del autor: tiene un bug abierto en sus rutas (issue #377) y recomienda verificar las fuentes primarias.

## Anatomy, de wheresryan22 (licencia MIT)
- Original: https://github.com/wheresryan22/anatomy
- Qué hace: explica un concepto técnico construyéndolo como una máquina interactiva (SVG isométrico).
- Requisitos: pensada para la pestaña Code (Claude Code). Necesita Node.js 20.10 o superior y Chrome.
- Instalación: descarga el ZIP oficial (https://github.com/wheresryan22/anatomy/archive/refs/heads/main.zip), descomprime, renombra la carpeta `anatomy-main` a `anatomy` y muévela a `~/.claude/skills/`. Detalles en el README del autor.
- Uso: `/anatomy explica cómo funciona [concepto], interactivo, versión simple con máximo 3 controles.`
- Consume mucho tiempo y uso: empieza siempre con una versión simple.


## find-skills, de Vercel Labs (licencia MIT)
- Original: https://www.skills.sh/vercel-labs/skills/find-skills (código en https://github.com/vercel-labs/skills)
- Qué hace: es la Skill para encontrar Skills. Cuando preguntas "¿cómo hago X?" o "busca una Skill para X", revisa el ranking de skills.sh (Skills más instaladas y probadas), busca con el CLI `npx skills find`, te recomienda opciones priorizando instalaciones (1K+), reputación del autor (Anthropic, Vercel) y estrellas en GitHub, y puede instalarlas por ti.
- Valor: en lugar de construir todo desde cero, descubres en segundos si alguien ya resolvió tu tarea, con criterios de calidad.
- Instalación recomendada (pestaña Code, requiere Node.js): `npx skills add https://github.com/vercel-labs/skills --skill find-skills` y elige Claude Code cuando lo pregunte.
- En Claude Desktop (Cowork): sube [find-skills.zip](find-skills.zip) en Customize > Skills. Necesita poder ejecutar `npx`; si no puede, te dará las búsquedas y enlaces para instalar a mano.
- Buscar sin instalar nada: navega https://skills.sh o usa `npx skills find [tema]` en una terminal.
- Prompts de ejemplo: `Busca una Skill para crear rúbricas de evaluación`, `¿Hay una Skill para hacer revisiones sistemáticas de literatura?`, `Encuentra una Skill para generar presentaciones con mi marca`.
- Recuerda: antes de instalar lo que encuentre, lee su SKILL.md y su licencia.
