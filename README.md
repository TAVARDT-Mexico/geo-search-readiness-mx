# Auditor de Búsqueda con IA y GEO

[![Auditor GEO](https://img.shields.io/badge/TAVARDT-Busqueda%20IA%20GEO-5b3cf5.svg)](https://tools.tavardt.com/mx/auditor-busqueda-ia-geo/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditor CLI de Generative Engine Optimization (GEO) para evaluacion de permisos de bots de IA, arquitectura semantica y citacion en LLMs.

Desarrollado y mantenido por la division de ingenieria semantica y visibilidad digital de **TAVARDT**.

***

## Capacidades de Auditoria GEO

* **Acceso de Rastreadores de IA**: Inspeccion de directivas en `robots.txt` para bots como GPTBot, OAI-SearchBot, PerplexityBot, ClaudeBot y Google-Extended.
* **Extraccion de Entidades Semanticas**: Verificacion de marcado estructurado Schema.org en formato JSON-LD.
* **Jerarquia y Contexto Semantico**: Comprobacion de encabezados H1 y meta descriptions para indexacion en LLMs.
* **Puntuacion de Preparacion**: Evaluacion tecnica de 0 a 100 puntos con recomendaciones directas de optimizacion.

***

## Instalacion y Ejecucion

Requiere unicamente Python 3.8 o superior sin dependencias externas.

```bash
git clone https://github.com/TAVARDT/geo-search-readiness-mx.git
cd geo-search-readiness-mx
python geo_auditor.py empresa.mx
```

Para exportar los resultados en formato JSON:

```bash
python geo_auditor.py empresa.mx -json
```

***

## Diagnostico Completo en la Web

Para auditorias continuas con interfaz grafica, acceda a la herramienta oficial:

* **Auditor de Busqueda con IA y GEO**
* **[Portal Corporativo TAVARDT](https://ag.tavardt.com/mx/)**

***

## Consultoria en Visibilidad y Motores de IA

Para proyectos de optimizacion semantica y presencia en modelos generativos en Mexico, consulte a los especialistas de **TAVARDT**.

***

## Enlaces Útiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnósticos:** https://tools.tavardt.com/mx/
* **Contacto Técnico:** https://ag.tavardt.com/mx/contacto/

***

### Licencia
Distribuido bajo la Licencia MIT. Consulte el archivo [LICENSE](LICENSE) para obtener más detalles.

***

© 2026 TAVARDT. Todos los derechos reservados.
