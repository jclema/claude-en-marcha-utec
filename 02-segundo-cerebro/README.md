# 02 · Segundo cerebro y Proyectos

## Estructura de la carpeta maestra
```
Claude/
  00_Sobre-mi/        Sobre-mi-docente.md, Mapa-de-oportunidades.md
  01_Docencia/        una subcarpeta por curso (sílabo, rúbricas, lecturas)
  02_Investigacion/   una subcarpeta por línea (papers, notas, datasets)
  03_Trabajo-Gestion/ comités, informes, acreditación, consultoría
  04_Personal/        finanzas, viajes, aprendizaje
  05_Skills/          tus Skills
  06_Specs/           specs de herramientas a construir
```

Prompt para crearla:
```
Dentro de mi carpeta Claude crea esta estructura de carpetas y, en cada una, un archivo LEEME.md de 3 líneas que explique qué va ahí: 00_Sobre-mi, 01_Docencia (con una subcarpeta para el curso [nombre del curso]), 02_Investigacion (con una subcarpeta para mi línea [tema]), 03_Trabajo-Gestion, 04_Personal, 05_Skills, 06_Specs.
```

Envía este prompt en una conversación de Cowork con la carpeta `Claude` seleccionada (puedes seguir en la del bloque 1). Luego, en Finder o el Explorador, arrastra tu sílabo, rúbrica y lectura a `01_Docencia/[curso]` y uno o dos papers a `02_Investigacion/[tema]`.

## Proyectos
Crea 4: Docencia · [curso], Investigación · [tema], Gestión y Personal. En cada uno sube Sobre-mi-docente.md y los archivos del área.

Paso a paso:
1. En la barra lateral haz clic en **Proyectos** y luego en **Nuevo proyecto**.
2. Escribe el nombre (por ejemplo, `Docencia · Gestión de Operaciones`) y una descripción de una línea, y crea el proyecto.
3. Dentro del proyecto, en el panel de la derecha, busca **Instrucciones** (Instructions), haz clic para editar, pega las instrucciones de abajo, cambia los corchetes y guarda.
4. En el mismo panel, en **Archivos** (Files), haz clic en `+` y sube `Sobre-mi-docente.md` (está en `Documentos > Claude > 00_Sobre-mi`) y los archivos del área.
5. Para trabajar dentro del proyecto, escribe en la caja de mensajes de la página del proyecto: todo chat que abras ahí hereda su contexto.

Prueba rápida en el Proyecto de Docencia: `¿Qué sabes de mí y de este curso? Resúmelo en 5 líneas`. Si responde algo genérico, revisa que estés dentro del proyecto (su nombre aparece arriba de la conversación) y que los archivos se hayan subido.

### Instrucciones: Docencia
```
Eres mi asistente para el curso [nombre], de [pregrado/posgrado], en UTEC. Lee siempre Sobre-mi-docente.md y el sílabo antes de responder. Alinea todo a los resultados de aprendizaje del sílabo y a la rúbrica del curso. Usa ejemplos del contexto peruano y latinoamericano (empresas, industrias y datos locales). Cuando diseñes actividades, indica duración, objetivo, pasos y cómo se evalúa. No inventes datos ni fuentes: si algo no está en los archivos o no lo pudiste verificar, dilo.
```

### Instrucciones: Investigación
```
Eres mi asistente de investigación sobre [tema]. Lee Sobre-mi-docente.md y los papers del proyecto. Prioriza fuentes revisadas por pares y usa el conector Consensus para buscar literatura. Toda afirmación debe ir con autor, año y DOI o enlace. Distingue entre lo que dice la evidencia y tu interpretación. Si una cita no la pudiste abrir o verificar, márcala como "no verificada".
```

### Instrucciones: Gestión
```
Eres mi asistente para tareas de gestión académica en UTEC (informes, actas, comités, acreditación, coordinación). Lee Sobre-mi-docente.md. Redacta en tono institucional, claro y breve. Usa los formatos de este proyecto cuando existan. Antes de enviar o modificar cualquier cosa, pídeme confirmación.
```

### Instrucciones: Personal
```
Eres mi asistente personal. Lee Sobre-mi-docente.md. Ayúdame a organizar mi tiempo, aprendizaje, finanzas y proyectos personales. Sé práctico y termina con próximos pasos concretos.
```
