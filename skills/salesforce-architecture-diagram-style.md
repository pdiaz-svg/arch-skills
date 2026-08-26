# Skill: Salesforce Architecture Diagram Style (SAD-Style)

## Nombre del skill
`salesforce-architecture-diagram-style`

## Propósito
Aplicar un lenguaje visual consistente y "clean" a todo diagrama de arquitectura
que se genere o edite con IA (Claude, AI Expert Suite, Gemini), tanto en
Google Slides como en documentos .doc, para que no varíe el estilo según la
herramienta usada — y que ese estilo esté anclado a las fuentes oficiales de
marca de Salesforce, no inventado.

## Fuentes oficiales (consultar / citar antes de diseñar)

### 1. Salesforce Brand Central — brand.salesforce.com
Fuente de verdad de marca. Secciones relevantes para diagramas de arquitectura:
- Color: https://brand.salesforce.com/in/core-brand/color
- Typography: https://brand.salesforce.com/in/core-brand/typography
- Iconography: https://brand.salesforce.com/in/core-brand/iconography
- Layouts: https://brand.salesforce.com/in/core-brand/layout
- Data visualization: https://brand.salesforce.com/in/core-brand/data-visualization
- Graphics: https://brand.salesforce.com/in/core-brand/graphics
- UI, displays & devices: https://brand.salesforce.com/in/core-brand/ui-displays-devices
- Logo: https://brand.salesforce.com/in/core-brand/logo
- Presentations (resources): https://brand.salesforce.com/in/resources/presentations
- AI tools for brand creative: https://brand.salesforce.com/in/resources/ai-tools-for-brand-creative
- Asset Library / Gallery: https://brand.salesforce.com/in/gallery
- Todas las guidelines: https://brand.salesforce.com/in/guidelines/core-brand

### 2. Salesforce Corporate Template Hub (Google Slides, 2026)
Reemplaza al antiguo "Salesforce Presentation Slide Library" (en retiro).
Estructura del Hub:
- Template slides (Core = viven en el deck madre / Expanded = librerías separadas
  con más variantes): Covers, Agendas, Content layouts, Image layouts,
  Quotes & statements, Segues, Product features, Data visualization, Thank you.
- Assets (Core / Expanded): Characters, Iconography, Devices, Photography,
  Maps & flags.
- Secciones de proceso: Quick start, Presentation fundamentals, Brand guidelines,
  Accessibility, GSlides guidance.
- Nota operativa: la librería vieja está siendo retirada — si algún link roto
  aparece, redirigir siempre al Corporate Template Hub, no al deck legacy.

### Link base (fijo)
Deck madre: https://docs.google.com/presentation/d/15bBgTADtCxDmXeh4PJX3fZBz2yloMkzRepVU2KJoe6M/edit

Secciones ancladas dentro del mismo deck (Table of Contents del Hub, cada una
es un slide distinto dentro del mismo archivo — navegá con Ctrl/Cmd+F o el
panel de miniaturas):
- Covers / Agendas / Content layouts / Image layouts / Quotes & statements /
  Segues / Product features / Data visualization / Thank you (Template slides)
- Characters / Iconography / Devices / Photography / Maps & flags (Assets)
- Quick start / Presentation fundamentals / Brand guidelines / Accessibility /
  GSlides guidance (proceso)

Nota: el ID de slide en la URL (después de `id.g...`) cambia por sección, pero
todas viven en el mismo deck madre de arriba. Al pedirle a una IA que use
"el Hub", referenciar ese link base y decir a qué sección apunta.

## Regla de uso de las fuentes
Antes de generar o ajustar cualquier diagrama/documento, este skill debe:
1. Priorizar assets e iconografía reales de Brand Central / Corporate Template
   Hub por sobre shapes genéricos, siempre que la herramienta usada pueda
   acceder a esos assets (ej. pegándolos manualmente en Slides).
2. Si la herramienta de IA no puede "ver" esos assets (caso típico: Claude o
   Gemini generando desde cero sin adjuntos), aplicar las reglas de estilo
   de la sección siguiente como aproximación fiel a esas guías — y decirlo
   explícitamente ("estilo aproximado a Brand Central, sin acceso a assets
   oficiales en este entorno").
3. Nunca inventar un ícono de producto Salesforce: si no está disponible,
   usar una forma neutra y aclararlo.

## Reglas de estilo (aplicar cuando no hay acceso directo a los assets oficiales)

### 1. Paleta de colores
- Fondo: blanco (#FFFFFF) o gris muy claro (#F3F3F3).
- Color primario (marca / capas core): Salesforce Blue (#0176D3).
- Color secundario (servicios externos / terceros): Slate Gray (#706E6B).
- Acento (alertas / puntos críticos): Salesforce Orange (#FE9339) — uso moderado.
- Éxito / flujo válido: Green (#04844B). Error / riesgo: Red (#C23934).
- Texto: Charcoal (#181818) sobre fondo claro.
- Verificar siempre contra https://brand.salesforce.com/in/core-brand/color
  por si la paleta oficial cambió.

### 2. Tipografía
- Títulos: Salesforce Sans (o Arial/Helvetica de reemplazo), Bold, 20-24pt.
- Subtítulos / nombres de capa: Semibold, 14-16pt.
- Etiquetas dentro de shapes: Regular, 10-12pt, horizontal.
- Máximo 2 tipografías por documento.
- Referencia oficial: https://brand.salesforce.com/in/core-brand/typography

### 3. Formas y capas
- Rectángulos de esquinas redondeadas (radius 4-8px) para componentes.
- Contenedores (rectángulo grande, borde punteado, fondo gris claro) para
  agrupar por capa: Presentation / Integration / Data / Security.
- Flechas: línea sólida = flujo síncrono; punteada = asíncrono/eventual.
- Iconografía: preferir íconos oficiales de producto (ver
  https://brand.salesforce.com/in/core-brand/iconography); si no existen,
  usar ícono genérico neutro (nunca emoji ni clip art).

### 4. Layout
- Lectura izquierda→derecha o arriba→abajo.
- Máximo 3 niveles de anidamiento visual.
- Espaciado mínimo equivalente a 24px.
- Un diagrama = una idea (dividir en contexto + detalle si hay +8-10 componentes,
  estilo C4).
- Leyenda obligatoria si hay más de 2 colores con significado distinto.
- Referencia oficial de layouts: https://brand.salesforce.com/in/core-brand/layout

### 5. Documentos .doc (Word/Google Docs)
- Título Heading 1, secciones Heading 2/3.
- Diagramas centrados, caption debajo en cursiva, 10pt.
- Un diagrama por página cuando sea posible.
- Tablas de componentes: Componente | Responsabilidad | Owner | Notas.

### 6. Google Slides
- Usar como base el Corporate Template Hub / Corporate Template 2026 cuando
  esté disponible, en vez de un theme genérico.
- Un diagrama por slide, título arriba, diagrama centrado.
- Sin transiciones ni animaciones en slides de arquitectura.
- Consultar "Data visualization" y "GSlides guidance" dentro del Hub para
  layouts de diagramas técnicos específicos.

## Salida esperada del skill
Al aplicarlo, cualquier diagrama generado debe:
1. Decir si usó assets oficiales (Brand Central / Corporate Template Hub) o
   una aproximación por reglas.
2. Ofrecer variante en .pptx/Slides Y en .doc con el mismo estilo.
3. Señalar qué ícono oficial no estaba disponible y qué genérico se usó, si aplica.

---

## Instructivo de implementación por herramienta

### 1. Claude (Claude.ai / Claude Code)
- Opción A — Proyecto con instrucciones: crear un Proyecto en Claude y pegar
  el contenido de este archivo (desde "## Fuentes oficiales" en adelante) en
  las "Custom Instructions" del proyecto.
- Opción B — Skill de Claude Code: guardar como
  `salesforce-architecture-diagram-style.md` en `.claude/skills/` y pedir:
  > "Lee `salesforce-architecture-diagram-style.md`, priorizá las fuentes
  > oficiales de Brand Central listadas ahí, y aplicá el resto de las reglas
  > como fallback."
- Uso puntual: pegar el archivo completo al inicio del chat.
- Tip: si tenés acceso a los assets reales (Corporate Template Hub, Brand
  Central Asset Library), adjuntalos en el chat — Claude no puede "navegar"
  esos links por sí solo salvo que estén habilitadas herramientas de research/web.

### 2. AI Expert Suite (Claude Code / Cursor / DevBar)
- Copiar este archivo como spec de la skill.
- Usar `/discover-plugins` para chequear que no exista ya una skill
  equivalente de estilo de diagramas o de "Brand Central" en el marketplace.
- Publicar siguiendo el flujo estándar (Expert Candidate → evaluación →
  Expert Marketplace), documentado en el canvas interno "Using the AI Expert
  Suite and Contributing Skills".
- Una vez publicada, se invoca por nombre: `salesforce-architecture-diagram-style`.
- Como esta skill referencia URLs externas (brand.salesforce.com), confirmá
  en el proceso de evaluación que el Expert Suite pueda resolver/fetch esos
  links, o que al menos los cite como referencia para el usuario.

### 3. Gemini (edición de Slides/Docs)
- Gemini no sostiene skills persistentes; funciona mejor con instrucciones
  repetidas en el prompt.
- Pegar el bloque "## Fuentes oficiales" + "## Reglas de estilo" antes de
  cada pedido de edición.
- Como Gemini vive dentro de Google Workspace, para diagramas es más efectivo
  decirle directamente: "Usá los assets del Corporate Template Hub / Brand
  Central para íconos y colores" y adjuntar/pegar el asset relevante en el
  mismo archivo (Slides permite copiar shapes/íconos directo del Hub).
- Alternativa: guardar este texto en una diapositiva oculta al final del
  archivo y referenciarla en cada prompt de edición.

---
_Generado para Pablo Díaz — Principal, Enterprise Architect, Salesforce._
_v2: incorpora fuentes oficiales de Brand Central y Corporate Template Hub._
