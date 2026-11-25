# Auditor de Optimización para Motores Generativos (GEO)

[![Auditor GEO](https://img.shields.io/badge/TAVARDT-Busqueda%20IA%20GEO-5b3cf5.svg)](https://tools.tavardt.com/mx/auditor-busqueda-ia-geo/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Motor de auditoría técnica automatizada para Generative Engine Optimization (GEO) y Answer Engine Optimization (AEO), evaluando permisos de rastreadores de IA, entidades Schema.org y señales semánticas.

La herramienta examina la preparación de entornos web frente a arquitecturas de generación aumentada por recuperación (RAG) implementadas en SearchGPT, Perplexity AI, Claude, Gemini y Apple Intelligence. Desarrollada sin dependencias externas, se ejecuta de forma nativa en consola Python y flujos automatizados de validación.

***

## Capacidades de Auditoría GEO y Alcance Algorítmico

El posicionamiento orgánico convencional dependía de palabras clave fijas y enlaces de entrada. Los motores de búsqueda generativa actuales redactan respuestas conversacionales realizando recuperación semántica sobre grafos de conocimiento estructurados y fuentes contrastadas.

* **Inspección de Rastreadores de IA**: Verificación de directivas en `robots.txt` para los principales agentes de búsqueda: GPTBot, OAI-SearchBot, PerplexityBot, ClaudeBot, Google-Extended y Applebot-Extended.
* **Extracción de Entidades Semánticas**: Comprobación de marcado estructurado Schema.org en formato JSON-LD (`application/ld+json`), permitiendo a los LLMs contextualizar datos corporativos.
* **Jerarquía Semántica y Anclaje Contextual**: Validación de encabezados H1 y meta descriptions para facilitar la división y vectorización de contenidos.
* **Puntuación Técnica de Preparación GEO**: Diagnóstico cuantitativo de 0 a 100 puntos que califica el sitio web en Alta Visibilidad, Visibilidad Moderada o Acceso Restringido.
* **Ejecución Ligera sin Dependencias**: Código basado exclusivamente en la biblioteca estándar de Python, garantizando análisis en milisegundos en cualquier entorno de servidor.

***

## Matriz de Verificación y Puntuación GEO

<table>
  <thead>
    <tr>
      <th align="left">Dimensión Auditada</th>
      <th align="left">Asignación de Puntos</th>
      <th align="left">Regla de Validación Algorítmica</th>
      <th align="left">Impacto en Síntesis y Citación de IA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Disponibilidad de robots.txt</strong></td>
      <td>20 Puntos</td>
      <td>Código HTTP 200 válido en la ruta /robots.txt.</td>
      <td>Garantiza que los rastreadores recuperen de forma predecible las directivas de acceso.</td>
    </tr>
    <tr>
      <td><strong>Permisos para Bots de IA</strong></td>
      <td>30 Puntos</td>
      <td>Ausencia de directivas Disallow: / hacia rastreadores de IA.</td>
      <td>Evita que el dominio sea descartado de las fuentes de información de los LLMs.</td>
    </tr>
    <tr>
      <td><strong>Schema.org JSON-LD</strong></td>
      <td>30 Puntos</td>
      <td>Presencia de scripts application/ld+json válidos en el documento.</td>
      <td>Aporta referencias directas para la creación de entidades en el grafo de conocimiento.</td>
    </tr>
    <tr>
      <td><strong>Meta Description Textual</strong></td>
      <td>10 Puntos</td>
      <td>Etiqueta meta name=description con contenido definido.</td>
      <td>Proporciona un resumen temático directo para contextualizar respuestas y resúmenes de IA.</td>
    </tr>
    <tr>
      <td><strong>Encabezado Semántico H1</strong></td>
      <td>10 Puntos</td>
      <td>Elemento h1 presente definiendo el eje central de la página.</td>
      <td>Fija el ancla temática inicial para la fragmentación y cálculo vectorial del contenido.</td>
    </tr>
  </tbody>
</table>

***

## Instalación y Guía Rápida de Uso

Requiere Python 3.8 o versión superior utilizando únicamente librerías estándar (`sys`, `re`, `json`, `ssl`, `argparse`, `urllib.request`). No requiere descargas de módulos mediante pip.

Clone el repositorio y ejecute el escaneo sobre el dominio deseado:

```bash
git clone https://github.com/TAVARDT-Mexico/geo-search-readiness-mx.git
cd geo-search-readiness-mx
python geo_auditor.py ejemplo.mx
```

Para generar los resultados estructurados en formato JSON:

```bash
python geo_auditor.py ejemplo.mx -j
```

Inspeccione dominios introduciendo el protocolo web completo:

```bash
python geo_auditor.py https://ejemplo.mx -j
```

Ejemplo de respuesta en formato JSON:

```json
{
  "domain": "ejemplo.mx",
  "robots_txt_status": "Found (HTTP 200)",
  "blocked_bots": [],
  "has_schema_jsonld": true,
  "has_meta_description": true,
  "has_h1": true,
  "score": 100,
  "status": "AI-Search Ready (High Visibility)",
  "recommendations": []
}
```

Niveles de preparación técnica para búsqueda generativa:

* **Puntuación 85 a 100**: Preparado para Búsqueda IA (Alta Visibilidade). Acceso pleno y entidades estructuradas implementadas.
* **Puntuación 50 a 84**: Visibilidad Moderada (Requiere Optimización). Bloqueos parciales o carencia de marcado Schema.org.
* **Puntuación 0 a 49**: Acceso Restringido (Inconformidades Críticas Detectadas). Bloqueo activo de bots de IA o ausencia de estructura semántica.

***

## Preguntas Frecuentes (FAQ Técnico)

### ¿Por qué restringir OAI-SearchBot o PerplexityBot perjudica el posicionamiento en motores conversacionales?
OAI-SearchBot y PerplexityBot ejecutan la búsqueda y recuperación de información en vivo para ChatGPT Search y Perplexity. Si se bloquean estos rastreadores, las aplicaciones de IA no pueden consultar ni citar contenidos de su sitio al responder consultas de usuarios.

### ¿Cómo facilita el marcado Schema.org JSON-LD la comprensión de entidades por parte de los LLMs?
Los modelos de lenguaje masivo utilizan grafos semánticos para validar datos y corroborar hechos. El formato JSON-LD proporciona especificaciones directas sobre organizaciones, productos y artículos sin ruido visual, mejorando la fiabilidad de las respuestas generadas.

### ¿Qué criterio algorítmico define la puntuación de 0 a 100 de preparación GEO?
La puntuación pondera 20 puntos por la presencia del robots.txt, 30 puntos por no bloquear rastreadores de IA, 30 puntos por incluir Schema.org JSON-LD, 10 puntos por la meta description y 10 puntos por el encabezado H1, completando los 100 puntos totales.

### ¿De qué manera audita el script el robots.txt y el código HTML sin emplear navegadores complejos?
La herramienta realiza peticiones HTTP GET directas con un User-Agent específico a `/robots.txt` y a la página de inicio. El contenido se evalúa con expresiones regulares rápidas, permitiendo inspecciones instantáneas sin requerir motores de navegación en segundo plano.

### ¿Cómo pueden los equipos técnicos integrar este informe JSON en flujos de integración continua?
Al utilizar el parámetro `-j`, el script emite datos JSON directamente a la salida estándar. Las herramientas de CI/CD pueden validar el valor de `score` o el contenido de `blocked_bots` con jq, deteniendo el despliegue si algún cambio bloquea accidentalmente a los rastreadores de IA.

***

## Consultoría en Optimización Semántica y Búsqueda IA

Para diseño de datos estructurados, ingeniería de grafos de entidades y visibilidad en asistentes de IA en México, contacte con los especialistas de **TAVARDT México**.

***

## Enlaces Útiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnósticos:** https://tools.tavardt.com/mx/
* **Contacto Técnico:** https://ag.tavardt.com/mx/contacto/

***

### Licencia
Distribuido bajo la Licencia MIT.

***

© 2026 TAVARDT. Todos los derechos reservados.
