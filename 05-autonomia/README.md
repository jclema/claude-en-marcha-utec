# 05 · Autonomía: tareas programadas, agentes y subagentes

- **Flujo:** pasos definidos que Claude sigue en orden.
- **Agente:** Claude recibe un objetivo, decide pasos y herramientas, verifica y repite.
- **Subagentes:** un coordinador reparte trabajo entre especialistas con contexto propio.

## Agente coordinador (carril base, en el chat)
```
Actúa como coordinador de un equipo de 3 especialistas para este objetivo: [objetivo]. Trabaja en etapas separadas y muéstrame el resultado de cada una: 1) Buscador: encuentra papers (con Consensus) y noticias relevantes de los últimos 7 días. 2) Verificador: comprueba cada fuente, descarta lo que no se pueda abrir y marca la confianza. 3) Redactor: escribe un informe de una página con los 5 hallazgos más relevantes, cada uno con enlace y por qué me importa. Guarda el informe en Google Drive en la carpeta Claude-UTEC/Monitoreo con la fecha en el nombre.
```

## Programarlo
Scheduled > Create with Claude. Pega el prompt anterior, cadencia semanal (lunes 07:00), guarda y prueba con Run now. Para que corra en la nube debe usar conectores, no archivos locales. Guía: https://support.claude.com/en/articles/13854387-schedule-recurring-tasks-in-claude-cowork

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
