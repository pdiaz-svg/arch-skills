Fuentes oficiales (consultar / citar antes de diseñar)1. Salesforce Brand Central — brand.salesforce.comFuente de verdad de marca. Secciones relevantes para diagramas de arquitectura:
Color: https://brand.salesforce.com/in/core-brand/color
Typography: https://brand.salesforce.com/in/core-brand/typography
Iconography: https://brand.salesforce.com/in/core-brand/iconography
Layouts: https://brand.salesforce.com/in/core-brand/layout
Data visualization: https://brand.salesforce.com/in/core-brand/data-visualization
Graphics: https://brand.salesforce.com/in/core-brand/graphics
UI, displays & devices: https://brand.salesforce.com/in/core-brand/ui-displays-devices
Logo: https://brand.salesforce.com/in/core-brand/logo
Presentations (recursos vigentes): https://brand.salesforce.com/in/resources/presentations#top
AI tools for brand creative: https://brand.salesforce.com/in/resources/ai-tools-for-brand-creative
Asset Library / Gallery: https://brand.salesforce.com/in/gallery
Todas las guidelines: https://brand.salesforce.com/in/guidelines/core-brand



2. Salesforce Corporate Template Hub (Google Slides, 2026) — usar esto, no el deck viejoEl antiguo "Salesforce Presentation Slide Library" está en retiro y desaparecerá pronto — no usarlo como referencia.

Recursos vigentes (listados en brand.salesforce.com/in/resources/presentations):
Salesforce Corporate Template 2026 (Google Slides) — base para presentaciones generales / decks internos, incluye Covers, Agendas, Content layouts, Image layouts, Quotes & statements, Segues, Product features, Data visualization, Thank you (Template slides) y Characters, Iconography, Devices, Photography, Maps & flags (Assets): https://docs.google.com/presentation/d/15bBgTADtCxDmXeh4PJX3fZBz2yloMkzRepVU2KJoe6M/edit
Salesforce Corporate Presentation — "Now Everyone's an Einstein" (Official, Google Slides): https://docs.google.com/presentation/d/1B-9H1bNuCcGcQfQ5NQqONcwsRTsX-nbPOa6bpAmYDms/edit
FY26 Industries Design Templates — Datasheet & Kit Of Parts (Google Slides, hacer copia antes de editar) — usar este para todo lo que sea .doc / datasheet / documento de arquitectura tipo one-pager: https://docs.google.com/presentation/d/12-OISW9Uxs5b4GGuvHS5eCN7nuP3POS25FtHFCxr7Lw/edit



Regla de uso de las fuentes
Priorizar assets e iconografía reales de Brand Central / Corporate Template Hub por sobre shapes genéricos, siempre que la herramienta usada pueda acceder a esos assets.
Si la herramienta de IA no puede "ver" esos assets, aplicar las reglas de estilo de abajo como aproximación — y decirlo explícitamente.
Nunca inventar un ícono de producto Salesforce: si no está disponible, usar una forma neutra y aclararlo.



Reglas de estilo (fallback cuando no hay acceso directo a los assets oficiales)Paleta de colores
Fondo: blanco (#FFFFFF) o gris muy claro (#F3F3F3).
Primario (capas core): Salesforce Blue (#0176D3).
Secundario (servicios externos/terceros): Slate Gray (#706E6B).
Acento (alertas/puntos críticos): Salesforce Orange (#FE9339) — uso moderado.
Éxito: Green (#04844B). Error/riesgo: Red (#C23934).
Texto: Charcoal (#181818) sobre fondo claro.



Tipografía
Títulos: Salesforce Sans (o Arial/Helvetica), Bold, 20-24pt.
Subtítulos/capas: Semibold, 14-16pt. Etiquetas: Regular, 10-12pt, horizontal.
Máximo 2 tipografías por documento.



Formas y capas
Rectángulos de esquinas redondeadas (radius 4-8px) para componentes.
Contenedores (borde punteado, fondo gris claro) para agrupar capas: Presentation / Integration / Data / Security.
Flechas: sólida = flujo síncrono; punteada = asíncrono/eventual.
Iconografía: preferir íconos oficiales de producto; si no existen, usar ícono genérico neutro (nunca emoji ni clip art).



Layout
Lectura izquierda→derecha o arriba→abajo. Máximo 3 niveles de anidamiento.
Un diagrama = una idea (dividir en contexto + detalle si hay +8-10 componentes, estilo C4).
Leyenda obligatoria si hay más de 2 colores con significado distinto.



Documentos .doc (Word/Google Docs)
Fuente obligatoria de estilo: FY26 Industries Design Templates — Datasheet & Kit Of Parts (hacer copia primero, link arriba). Extraer layout de datasheet, jerarquía tipográfica y kit de componentes antes de aplicar las reglas genéricas como fallback.
Título Heading 1, secciones Heading 2/3. Diagramas centrados, caption debajo en cursiva, 10pt. Un diagrama por página cuando sea posible.
Tablas de componentes: Componente | Responsabilidad | Owner | Notas.



Google Slides
Usar como base el Corporate Template 2026 en vez de un theme genérico.
Un diagrama por slide, título arriba, diagrama centrado. Sin transiciones ni animaciones en slides de arquitectura.



Salida esperadaAl aplicar este estilo, cualquier diagrama/documento generado debe:
Decir si usó assets oficiales o una aproximación por reglas.
Ofrecer variante en Slides Y en .doc con el mismo estilo, cuando aplique.
Señalar qué ícono oficial no estaba disponible y qué genérico se usó, si aplica.



Instructivo de implementación por herramientaClaude (Claude.ai / Claude Code)
Proyecto con instrucciones: pegar este documento completo en las "Custom Instructions" de un Proyecto de Claude.
Claude Code: guardar como salesforce-architecture-diagram-style.md en .claude/skills/ y pedir "Leé este archivo y aplicá el estilo a partir de ahora para diagramas y documentos de arquitectura."
Límite: Claude no navega los links de Brand Central por sí solo salvo que tenga research/web habilitado.



AI Expert Suite (Claude Code / Cursor / DevBar)
Copiar este documento como spec de la skill.
Usar /discover-plugins para chequear que no exista ya una equivalente.
Publicar vía el flujo de PR al Expert Registry (plugins/<id>/registry.yaml).


Gemini (edición de Slides/Docs)
Pegar el bloque de reglas en el prompt antes de cada edición grande, o guardarlo en una diapositiva oculta al final del archivo y referenciarla.
