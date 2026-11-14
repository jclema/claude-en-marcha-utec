# 03 · Skills

Una Skill es una carpeta con un archivo `SKILL.md` que enseña a Claude a hacer una tarea siempre de la misma forma. Guía oficial: https://support.claude.com/en/articles/12512180-use-skills-in-claude

## Dónde buscar
- En la app: Customize > Skills
- Repositorio oficial de Anthropic: https://github.com/anthropics/skills
- Este repo: [skills-utec](skills-utec) y [skills-recomendadas](skills-recomendadas)
- Directorio abierto con ranking por instalaciones: https://skills.sh
- Skill find-skills: le pides a Claude "busca una Skill para X" y la encuentra por ti (ver skills-recomendadas)

## Antes de instalar una Skill de terceros
1. Abre su `SKILL.md` y lee qué hace.
2. Revisa la licencia y el autor.
3. Verifica que no pida acceso a cosas que no necesita.

## Cómo instalar en Claude Desktop
1. Abre este repo en **Google Chrome**. En Safari los ZIP se descomprimen solos al descargarse y después no se pueden subir.
2. Descarga el ZIP: haz clic en el nombre del archivo y luego en el ícono de descarga (flecha hacia abajo, arriba a la derecha, "Download raw file"). Queda en tu carpeta Descargas.
3. En Claude: Customize > Skills > + > Upload a skill (si no ves Customize, busca Skills en Settings > Capabilities). Sube el ZIP sin descomprimir. Si el archivo aparece como carpeta y no como .zip, descárgalo de nuevo desde Chrome.
4. Verifica que aparezca en la lista con su interruptor encendido.

## Cómo usar una Skill
No necesitas comandos: Claude la usa sola cuando tu pedido coincide con su descripción, y lo verás en sus pasos. Para llamarla a propósito, escribe `/` en la caja de mensajes y elígela de la lista (por ejemplo `/teach`).

Para publicar un quiz o artefacto: se abre en un panel a la derecha de la conversación; arriba de ese panel busca Share o Publish, elige que cualquiera con el enlace pueda verlo, copia el enlace y pruébalo en una ventana de incógnito.

## Skills UTEC (creadas para este taller)
| Skill | Para qué | ZIP |
|---|---|---|
| disenador-sesiones | Sesiones, secuencias, casos y actividades | [disenador-sesiones.zip](skills-utec/disenador-sesiones.zip) |
| evaluador-rubrica | Borrador de retroalimentación con rúbrica, sin nota final | [evaluador-rubrica.zip](skills-utec/evaluador-rubrica.zip) |
| asistente-investigacion | Estado del arte con fuentes verificables | [asistente-investigacion.zip](skills-utec/asistente-investigacion.zip) |

Prompts de ejemplo en la guía del participante, bloque 3.

## Crear tu propia Skill
```
Usa skill-creator para ayudarme a crear una Skill que resuelva la tarea número [1 o 2] de mi Mapa-de-oportunidades.md. Entrevístame primero con las preguntas necesarias. La descripción debe decir qué hace y cuándo usarla. Guárdala en Claude/05_Skills y empaquétala como ZIP para subirla.
```
Buenas prácticas: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices
