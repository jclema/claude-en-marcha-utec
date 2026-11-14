# Loops: recetas para docentes

Un loop es un ciclo en el que Claude repite trabajo hasta que se cumple una condición de parada. Marco oficial del equipo de Claude Code: [Loop engineering: Getting started with loops](https://claude.com/blog/getting-started-with-loops).

| Loop | Le delegas | Úsalo cuando | Herramienta |
|---|---|---|---|
| Turn-based | La verificación | Exploras o decides | Skills de verificación |
| Goal-based | La condición de parada | Sabes cómo se ve "terminado" | `/goal` (Code) |
| Time-based | El disparador | El trabajo se repite en el tiempo | `/loop` (Code), Scheduled, `/schedule` |
| Proactive | El prompt completo | El trabajo es recurrente y bien definido | Todo lo anterior + agentes |

Reglas: empieza por el loop más simple, pon siempre un límite de intentos y detén los loops que ya no necesites. Cada ejecución consume tu límite del plan.

Datos clave: `/goal` usa un segundo modelo que revisa la meta cada vez que Claude intenta terminar (escribe el límite de intentos en la misma frase). `/loop` corre en tu sesión (mínimo 1 minuto entre ejecuciones, necesita la computadora encendida, se detiene a los 7 días). `/schedule` corre en la nube con la laptop cerrada, como máximo cada hora. Para detener un loop de tiempo, pídele a Claude que lo cancele.

---

## 1. Turn-based · Retroalimentación que se autoverifica
Dónde: Chat o Cowork, con la Skill evaluador-rubrica.
```
Usa la rúbrica del curso para revisar este trabajo. Antes de responderme, verifica que cada criterio tenga evidencia textual citada y una sugerencia accionable; si alguno no la tiene, corrígelo y vuelve a verificar. No asignes la nota final.
```

## 2. Goal-based · Herramienta que cumple su spec (SDD)
Dónde: pestaña Code, en la carpeta de tu spec.
```
/goal la herramienta cumple todos los criterios de aceptación de spec.md y funciona abriendo un solo archivo HTML. Detente después de 5 intentos.
```

## 3. Goal-based · Estado del arte verificado
Dónde: pestaña Code, en tu carpeta de investigación.
```
/goal investigacion.md tiene una tabla con 10 artículos revisados por pares (2020-2026) sobre [tema], cada uno con DOI que abre y un hallazgo que coincide con el resumen del artículo. Detente después de 4 intentos.
```

## 4. Time-based · Vigilar entregas mientras trabajas
Dónde: pestaña Code, con la carpeta de entregas sincronizada en tu computadora.
```
/loop 30m revisa la carpeta entregas/ y dime qué trabajos nuevos llegaron, si cumplen el formato pedido y cuáles están incompletos.
```

## 5. Time-based · Resumen diario del docente
Dónde: Scheduled (cadencia diaria, 07:00), con Gmail y Calendar conectados.
```
Revisa mi agenda de hoy y los correos de las últimas 24 horas. Dame: 1) mis clases y reuniones del día, 2) correos de estudiantes o colegas que requieren respuesta, ordenados por urgencia, con un borrador corto para cada uno, 3) plazos de esta semana. No envíes nada.
```

## 6. Proactive · Monitoreo semanal de investigación con subagentes
Dónde: Scheduled (semanal, lunes 07:00), con Consensus y Drive conectados. En Code puedes usar los subagentes de [../agents](../agents).
```
Actúa como coordinador de 3 especialistas. 1) Buscador: encuentra papers (con Consensus) y noticias de los últimos 7 días sobre [tema]. 2) Verificador: comprueba cada fuente y descarta lo que no se pueda abrir. 3) Redactor: escribe un informe de una página con los 5 hallazgos más relevantes, con enlace y por qué me importa. Guarda el informe en Google Drive en Claude-UTEC/Monitoreo con la fecha en el nombre. Yo decido qué comparto con mis tesistas.
```
Variante: monitoreo mensual de convocatorias de fondos de investigación (CONCYTEC u otras) con fecha límite y requisitos.
