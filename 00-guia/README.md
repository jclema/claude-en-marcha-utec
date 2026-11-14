# 00 · Guía y checklist

- Guía del participante: [Google Docs](https://docs.google.com/document/d/1DRpriWOaWGNzSqTLSSxME55HejNPiJ_S_DEVI4o58CE/edit)
- Descargar Claude Desktop: https://claude.com/download
- Prompt para generar la presentación de conceptos con Claude Design (36 diapositivas: Skills, Plugins, conectores, agentes, subagentes, loops, SDD y más): [Google Docs](https://docs.google.com/document/d/1Oj_SHhjhO4JI4JxYztE3qQyRQ0XyV3fAOlAubZshSr0/edit)

## Checklist antes de empezar
- [ ] Claude Desktop actualizado y con tu cuenta Pro iniciada
- [ ] Cuenta de GitHub activa y con la invitación a este repo aceptada
- [ ] Google Chrome actualizado
- [ ] Sílabo, rúbrica, una lectura o paper y 2 o 3 trabajos de ejemplo de un curso tuyo

## Agenda
| Hora | Bloque |
|---|---|
| 09:00 - 09:10 | Apertura |
| 09:10 - 09:40 | 0. Conoce Claude Desktop y configuración óptima |
| 09:40 - 10:05 | 1. Contexto con reverse prompting |
| 10:05 - 10:25 | 2. Segundo cerebro y Proyectos |
| 10:25 - 10:55 | 3. Skills |
| 10:55 - 11:10 | Pausa |
| 11:10 - 11:35 | 4. Investigación profunda y scraping |
| 11:35 - 12:05 | 5. Autonomía: tareas programadas, agentes y subagentes |
| 12:05 - 12:50 | 6. Construir con SDD y Claude Code, compartir en GitHub |
| 12:50 - 13:00 | Cierre y plan de 30 días |

## Cómo usar los prompts de este repo
1. Selecciona todo el texto del bloque de código y cópialo (Cmd+C en Mac, Ctrl+C en Windows). En GitHub también puedes usar el botón de copiar que aparece arriba a la derecha del bloque.
2. Pégalo en la caja de mensajes de Claude (Cmd+V o Ctrl+V).
3. Reemplaza cada texto entre `[corchetes]` por tu dato y borra los corchetes.
4. Presiona Enter para enviar. Shift+Enter hace un salto de línea sin enviar.

Puedes dictar: clic en el micrófono de la caja de mensajes, habla y clic de nuevo para terminar.

## Primeros 3 minutos en Claude Desktop
1. Abre Claude Desktop e inicia sesión. Para confirmar que tu plan es Pro, haz clic en tu nombre o iniciales (esquina inferior izquierda).
2. Ubica la barra lateral izquierda: nueva conversación, Proyectos, Code, Scheduled, Customize y tus conversaciones recientes.
3. Ubica la caja de mensajes (abajo al centro) y a su alrededor: el botón `+` (adjuntar archivos, activar conectores y Research), el selector de modelo (Opus, Sonnet o Haiku), el botón de carpeta (trabajar con archivos de tu computadora) y el micrófono.
4. Escribe: `Hola, en 3 líneas dime qué puedes hacer por un docente universitario` y presiona Enter.
5. Arrastra tu sílabo a la caja de mensajes y escribe: `Resume este sílabo en 5 viñetas y sugiere una mejora concreta`.

## Configuración óptima, paso a paso
1. **Privacidad:** clic en tu nombre (esquina inferior izquierda) > Settings > Privacy y apaga "Help improve Claude".
2. **Preferencias:** Settings > Profile. Completa tu nombre, pega en el campo de preferencias personales el texto de la guía del participante, ajusta los corchetes y guarda.
3. **Memoria:** en Settings, sección de memoria (Capabilities o Memory según la versión), activa generar memoria a partir de tus chats y buscar y referenciar chats anteriores.
4. **Permisos:** en la caja de mensajes, modo de permisos en Manual para acciones con consecuencias. Si no ves el selector, Claude te pedirá aprobación antes de actuar: lee siempre qué va a hacer.
5. **Skills del sistema:** Customize > Skills (o Settings > Capabilities): Skills de documentos activadas.
6. **Conectores:** Customize > Connectors > Browse. Conecta Google Drive, Calendar, Gmail, Consensus y Canva: clic en el conector > Connect > elige tu cuenta en el navegador > acepta permisos > vuelve a la app. En cada conversación revisa con `+` que estén encendidos. Si tu cuenta UTEC bloquea la conexión, usa tu cuenta personal de Google.
7. **Claude in Chrome:** instala la extensión oficial de Anthropic desde la Chrome Web Store, inicia sesión y fíjala con el alfiler en el ícono de Extensiones (pieza de rompecabezas). Para usarla desde Claude Desktop: Settings > Customize > Connectors > **Claude in Chrome** > Configure y actívalo. Viene apagado en cada conversación: enciéndelo con `+` cuando lo necesites. En la pestaña Code se conecta con `/chrome`. Solo Google Chrome y plan pago. Guía oficial: https://support.claude.com/en/articles/12012173-get-started-with-claude-in-chrome

## Carril avanzado: Composio (opcional)
Son herramientas de terceros: instálalas con tu cuenta personal y revisa qué permisos das.

### Composio: más de 1000 apps
Conecta Claude con apps que no están en el directorio de conectores (Notion, Slack, Trello, HubSpot y muchas más).
1. Crea una cuenta gratuita en https://composio.dev
2. En Claude Desktop: Settings > Customize > Connectors > `+` > **Add custom connector**.
3. Nombre `Composio`, URL `https://connect.composio.dev/mcp`. Clic en Add, luego Connect, y autoriza en el navegador.
4. En una conversación activa Composio con `+` y pide, por ejemplo, `Conecta mi Notion`. La primera vez Claude te da un enlace para autorizar cada app.
5. En la pestaña Code, alternativa con la Skill connect-apps de Composio:
   ```
   npx skills add ComposioHQ/awesome-claude-skills --skill connect-apps
   ```
Docs: https://docs.composio.dev/docs/composio-connect

## Plan de 30 días
| Semana | Reto |
|---|---|
| 1 | Revisa el primer informe de tu tarea programada y ajústala. Completa 3 lecciones de /teach. |
| 2 | Automatiza la tarea número 2 de tu Mapa de oportunidades. Usa en clase un material creado con Claude. |
| 3 | Crea una Skill propia y súbela a `aportes/`. Busca con find-skills una Skill de la comunidad para tu curso y pruébala. |
| 4 | Instala una Skill directamente desde el repo de su autor y haz un fork + pull request a este repo. Comparte cuánto tiempo ahorraste. |
