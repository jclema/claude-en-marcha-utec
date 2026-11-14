# 06 · Construir con SDD y Claude Code

SDD (Spec-Driven Development): primero se especifica qué construir, después se construye y se verifica contra la spec. Buenas prácticas: https://code.claude.com/docs/en/best-practices

1. Escribe la spec con Claude (modelo Opus) usando el prompt de abajo. Guarda `spec.md` en `Claude/06_Specs/[herramienta]/`.
2. En la pestaña Code, abre esa carpeta, activa el modo plan (Shift+Tab) y pide: `Lee spec.md. Propón un plan de implementación como una sola página HTML autocontenida (sin servidor ni base de datos). No escribas código hasta que yo apruebe el plan.`
3. Aprueba el plan, deja que construya y verifica: `Revisa la herramienta contra cada criterio de aceptación de spec.md. Dime cuáles se cumplen y cuáles no, y corrige los que fallen.`
4. Publica y sube tu spec y tu HTML a `aportes/<tu-usuario>/`.

## Prompt de entrevista para la spec
```
Quiero construir [idea de herramienta] para [quién la va a usar]. Entrevístame, una pregunta a la vez y máximo 8 preguntas, para escribir una especificación. Luego genera spec.md con estas secciones: 1) Objetivo y problema que resuelve, 2) Usuarios, 3) Funcionalidades (máximo 5, priorizadas), 4) Fuera de alcance, 5) Datos de entrada y salida, 6) Diseño de la interfaz (descripción simple), 7) Criterios de aceptación verificables (lista de "dado / cuando / entonces"). Mantén el alcance pequeño: debe poder construirse en 20 minutos.
```

Plantilla: [plantilla-spec.md](plantilla-spec.md) · Ejemplo: [ejemplo-spec-simulador-inventario.md](ejemplo-spec-simulador-inventario.md)
