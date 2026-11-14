# 05 · Loops: tareas programadas, agentes y subagentes

Primero lee los 4 tipos de loops y sus recetas: [loops/README.md](loops/README.md)

- **Flujo:** pasos definidos que Claude sigue en orden.
- **Agente:** Claude recibe un objetivo, decide pasos y herramientas, verifica y repite.
- **Subagentes:** un coordinador reparte trabajo entre especialistas con contexto propio.

## Agente coordinador (carril base, en el chat)
Abre una conversación nueva de Cowork, haz clic en `+`, activa Consensus y Google Drive, pega el prompt y envíalo. Si la carpeta `Claude-UTEC/Monitoreo` no existe en tu Drive, Claude intentará crearla; si no puede, créala tú en drive.google.com y vuelve a pedirle que guarde el informe.
```
Actúa como coordinador de un equipo de 3 especialistas para este objetivo: [objetivo]. Trabaja en etapas separadas y muéstrame el resultado de cada una: 1) Buscador: encuentra papers (con Consensus) y noticias relevantes de los últimos 7 días. 2) Verificador: comprueba cada fuente, descarta lo que no se pueda abrir y marca la confianza. 3) Redactor: escribe un informe de una página con los 5 hallazgos más relevantes, cada uno con enlace y por qué me importa. Guarda el informe en Google Drive en la carpeta Claude-UTEC/Monitoreo con la fecha en el nombre.
```

## Programarlo
1. En la barra lateral ve a **Scheduled** y elige **Create with Claude** (o pide en una conversación: "programa esta tarea").
2. Pega el prompt anterior como instrucción de la tarea.
3. Cadencia semanal, lunes a las 07:00.
4. Guarda y prueba con **Run now**. Al terminar, verifica en Google Drive que el informe esté en `Claude-UTEC/Monitoreo`.

La tarea debe usar solo conectores (Drive, Gmail, Consensus), no archivos de tu computadora. Si a la hora programada tu laptop o la app están cerradas, según tu versión la tarea corre en la nube o se ejecuta cuando vuelvas a abrir Claude: revisa su historial en Scheduled. Guía: https://support.claude.com/en/articles/13854387-schedule-recurring-tasks-in-claude-cowork

Más ideas:
- Resumen diario de agenda y correos pendientes a las 07:00.
- Recordatorio semanal de evaluaciones según el sílabo.
- Monitoreo mensual de convocatorias de fondos de investigación.

## Subagentes en Claude Code (carril avanzado)
La carpeta [agents](agents) tiene 3 subagentes listos. Cópialos a `.claude/agents/` dentro de tu carpeta de trabajo (o créalos con `/agents`) y luego pide:
```
Usa los subagentes buscador, verificador y redactor para producir un informe de estado del arte sobre [tema]. Que el buscador y el verificador trabajen en paralelo cuando sea posible. Guarda el informe final en informe-[fecha].md.
```
Docs: https://code.claude.com/docs/en/sub-agents


## Subagentes: créalos en lenguaje natural
Un subagente es Claude con una sola tarea e instrucciones propias: trabaja en su propio contexto y te reporta el resultado. No necesitas comandos: en la pestaña Code pide "Crea un subagente que haga X" o "Crea tres subagentes, uno para X, otro para Y y otro para Z". Para guardarlo y reutilizarlo, usa `/agents`.

**Regla de oro:** el agente prepara, tú apruebas. Ningún agente envía, publica o paga sin ti.

### Formaciones más útiles para docentes
| Formación | Cómo funciona | Ejemplo docente |
|---|---|---|
| Pipeline (en cadena) | Investigar, luego redactar, luego pulir | Buscador, verificador y redactor para tu estado del arte |
| En paralelo (fan-out y fan-in) | Varios agentes trabajan a la vez y se unen sus resultados | Tres agentes revisan literatura en inglés, español y portugués |
| Coordinador y trabajadores | Un agente planifica y delega | "Prepara el estado del arte de mi capítulo 2" |
| Evaluador y optimizador | Uno redacta, otro califica contra la rúbrica y repiten hasta que pasa | Mejorar un caso de estudio hasta que cumpla tus criterios (loop goal-based) |
| Consejo | Varios agentes proponen, se revisan entre sí y uno decide | Jurado simulado del plan de tesis: metodología, estadística y redacción |

Ruta recomendada: primero un agente de investigación, luego evaluador y optimizador, luego consejo. Usa la formación en paralelo solo si el trabajo de verdad se puede dividir. Cada agente consume tokens de tu plan: empieza con pocos.

Prompt de ejemplo (consejo):
```
Crea tres subagentes para revisar este plan de tesis [adjunto]: uno experto en metodología, otro en estadística y otro en redacción académica. Cada uno entrega sus observaciones por separado; luego revisen las observaciones de los otros y un cuarto agente integra un informe final priorizado. No modifiques el documento: solo propone.
```

Fuente: guía de Cindy Zhu, https://cindyzhu.com.au/guides/how-to-make-your-first-claude-subagent · Docs oficiales: https://code.claude.com/docs/en/sub-agents
