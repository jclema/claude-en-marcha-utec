# 04 · Investigación profunda y scraping

Regla: **si no lo abriste, no lo cites.**

## Literatura académica con Consensus
Conector oficial: https://claude.com/connectors/consensus

Entra a tu Proyecto de Investigación, haz clic en `+` y confirma que Consensus esté activado. Luego envía:
```
Usa Consensus para buscar la literatura revisada por pares más relevante de 2020 a 2026 sobre [tu pregunta de investigación]. Dame una tabla con: autor, año, título, revista, DOI, método, hallazgo principal y relevancia para mi pregunta. Luego escribe un estado del arte de 400 palabras que cite esa tabla e identifique 3 vacíos de investigación. Marca cualquier fuente que no hayas podido verificar.
```

## Research (investigación profunda en la web)
```
/deep-research ¿Cuál es el estado actual de [tema aplicado] entre 2024 y 2026? Prioriza fuentes oficiales, académicas y de organismos sectoriales. Entrega un informe con hallazgos clave, cifras con su fuente y una lista de fuentes con enlace.
```

## Scraping: 4 caminos
| Camino | Cuándo | Cómo |
|---|---|---|
| 1. Claude lee la página | Una o pocas páginas públicas | Pega el enlace y pide la extracción |
| 2. Claude in Chrome | Sitios donde hay que navegar, filtrar o paginar | Con la extensión, pide recorrer el sitio y extraer a una tabla |
| 3. Apify o Firecrawl (conectores) | Extracción a escala con scrapers ya hechos | Customize > Connectors > Apify o Firecrawl. Firecrawl tiene conector oficial: lo conectas y le describes en lenguaje natural qué datos quieres. Ambos tienen plan gratuito con créditos limitados. Docs: https://docs.apify.com/integrations/mcp · https://docs.firecrawl.dev/developer-guides/mcp-setup-guides/claude-ai |
| 4. Claude Code | Recolección repetible | Pide un script que extraiga y guarde un CSV |

```
Entra a [URL pública]. Extrae [qué datos] en una tabla con columnas [columnas], guárdala como CSV en mi carpeta Claude/02_Investigacion/[tema] e indica la fecha de extracción y la URL de origen.
```

Si usas el camino 2 (Claude in Chrome): abre Chrome, entra a la página, haz clic en el ícono de Claude en la barra de extensiones para abrir su panel lateral y pega el prompt ahí. No cierres la pestaña mientras trabaja. Desde Chrome no puede guardar en tu carpeta: pídele la tabla en formato CSV, cópiala y pásala a una conversación de Cowork para guardarla.

Buenas prácticas: solo datos públicos, revisa términos de uso y robots.txt, no extraigas datos personales, baja frecuencia, guarda fuente y fecha.
