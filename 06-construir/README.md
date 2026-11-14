# 06 · Construir con SDD y Claude Code

SDD (Spec-Driven Development): primero se especifica qué construir, después se construye y se verifica contra la spec. Buenas prácticas: https://code.claude.com/docs/en/best-practices

1. **Spec:** abre una conversación nueva de Cowork con la carpeta `Claude` seleccionada, elige Opus en el selector de modelo y envía el prompt de abajo. Al terminar la entrevista pide: `Guarda la spec en 06_Specs/[herramienta]/spec.md`. Debe quedar en `Claude/06_Specs/[herramienta]/spec.md`.
2. **Plan:** abre la pestaña **Code** en la barra lateral y, con el botón de carpeta, selecciona `Documentos > Claude > 06_Specs/[herramienta]`. Con el cursor en la caja de mensajes presiona Shift+Tab una o más veces hasta ver "plan mode" y envía: `Lee spec.md. Propón un plan de implementación como una sola página HTML autocontenida (sin servidor ni base de datos). No escribas código hasta que yo apruebe el plan.`
3. **Construir:** revisa el plan; si algo no coincide con tu spec, díselo antes de aprobar. Apruébalo (botón de aprobar o escribe `Aprobado, construye`). Claude pedirá permiso para algunas acciones: lee qué va a hacer y acepta.
4. **Verificar** con un loop goal-based: `/goal la herramienta cumple todos los criterios de aceptación de spec.md. Detente después de 5 intentos.` (sin /goal: `Revisa cada criterio de aceptación de spec.md y corrige los que fallen.`)
5. **Publicar:** prueba el HTML con doble clic desde tu carpeta. Pide `publica esta herramienta como artefacto para compartir`; si Code no puede, abre una conversación nueva, adjunta el HTML y pide `Publica este archivo como artefacto`, luego usa Share.
6. **Compartir:** sube tu spec y tu HTML a `aportes/<tu-usuario>/` (ver [aportes/README.md](../aportes/README.md)).

Carril base alternativo: si Code da problemas, pega tu spec.md en una conversación normal y pide `Construye esta herramienta como un artefacto interactivo según la spec`.

## Prompt de entrevista para la spec
```
Quiero construir [idea de herramienta] para [quién la va a usar]. Entrevístame, una pregunta a la vez y máximo 8 preguntas, para escribir una especificación. Luego genera spec.md con estas secciones: 1) Objetivo y problema que resuelve, 2) Usuarios, 3) Funcionalidades (máximo 5, priorizadas), 4) Fuera de alcance, 5) Datos de entrada y salida, 6) Diseño de la interfaz (descripción simple), 7) Criterios de aceptación verificables (lista de "dado / cuando / entonces"). Mantén el alcance pequeño: debe poder construirse en 20 minutos.
```

Plantilla: [plantilla-spec.md](plantilla-spec.md) · Ejemplo: [ejemplo-spec-simulador-inventario.md](ejemplo-spec-simulador-inventario.md)
