# 🧭 Strategic Thinking Skill

**A Claude Code skill** that turns any business situation into a structured
analysis by applying the right strategic-consulting framework — not all of
them at once, and not before it has enough context.

Instead of answering with generic frameworks or a wall of text, the skill
first asks the minimum needed (business, objective, time horizon, scope),
identifies whether the problem is **strategic** (long-term) or **tactical**
(short-term), picks 1–3 frameworks from its decision tree, and delivers a
report with clear sections and tables, ready to use.

## ✨ Why this skill

- **Asks before analyzing.** No auto-generated SWOT without context — the
  skill collects business, objective, time horizon and scope before picking
  a framework.
- **A decision tree, not a catalog.** 20+ frameworks organized by *user
  situation*, so the right one gets applied, not just the most popular one.
- **Explicitly separates strategy from tactics** in every report — never
  mixed without saying so.
- **Consistent output.** A report template plus per-framework tables (SWOT,
  PESTEL, Porter, BMC, 7S, impact/effort matrix, stakeholder map...) instead
  of free-form prose.
- **Optional narrative close.** Only if the user asks, it offers to help
  communicate the strategy once it's already defined — never before it
  exists.

## 📦 Installation

Copy this folder into your Claude Code skills directory (`.claude/skills/`
or `.agents/skills/`, depending on your setup):

```bash
git clone https://github.com/daaniidev/strategic-thinking-skill.git
```

Claude Code will automatically detect `SKILL.md` and activate the skill
when the conversation calls for it.

## 🚀 When it triggers

Say things like:

> "I need a SWOT analysis for my business"
> "How do I structure a strategic expansion plan?"
> "I want to validate my business model with a Business Model Canvas"
> "We're stuck on a big decision, what framework can help?"
> "Analyze the competition using Porter's five forces"

## 🗂️ Framework decision tree

| Situation | Framework(s) |
|---|---|
| Fast, unpredictable environment | VUCA / BANI |
| General starting point, internal/external risks | SWOT |
| Macro environment | PESTEL |
| Competitive structure of an industry | Porter's Five Forces |
| Designing or validating the business model | Business Model Canvas |
| Expansion into new markets | Ansoff Matrix |
| Internal organizational design | McKinsey 7S |
| Internal competitive advantage | VRIO, value chain, generic strategies |
| Portfolio of businesses/products | BCG Matrix / GE-McKinsey |
| New market space needed | Blue Ocean, Jobs to be Done, Three Horizons |
| Setting goals | SMART / OKR |
| Tracking an already-defined strategy | Balanced Scorecard |
| Stuck on a decision | Cynefin, Six Thinking Hats, decision trees |
| Stakeholder mapping / prioritization | Mendelow Matrix, impact/effort |
| Organizational change under way | Kotter's 8-step change process |
| Investment decision with direct economic impact | Business case, ROI/NPV, unit economics |
| Communicating strategy to others | Strategic narrative (offered at the end, on request) |

*(Full table with file references in [`SKILL.md`](SKILL.md).)*

## 📁 Project structure

```
.
├── SKILL.md                        # Skill definition, flow, and decision tree
├── assets/templates/
│   ├── informe-estrategico.md      # Final report skeleton
│   └── tablas-frameworks.md        # Per-framework tables (SWOT, PESTEL, BMC...)
├── references/                     # One file per framework family
│   ├── marcos-entorno.md
│   ├── dafo-pestel.md
│   ├── porter-canvas.md
│   ├── mckinsey-7s.md
│   ├── estrategia-competitiva.md
│   ├── matrices-portafolio.md
│   ├── innovacion-crecimiento.md
│   ├── objetivos-smart.md
│   ├── balanced-scorecard.md
│   ├── toma-decisiones.md
│   ├── stakeholders-riesgo.md
│   ├── fundamentos-financieros.md
│   ├── fundamentos-estrategia.md
│   ├── narrativa-estrategica.md
│   └── glosario-y-checklist.md
└── LICENSE
```

## 🔗 Boundary with branding skills

If the request is purely about brand identity or positioning (naming,
manifesto, brand architecture), this skill says so explicitly and points to
`brand-strategy` or `brand-positioning` instead of forcing a SWOT/PESTEL
onto a problem that isn't one.

## 📄 License

[MIT](LICENSE) © 2026 daanidev

---

# 🧭 Pensamiento y Mentalidad Estratégica

**Skill para Claude Code** que convierte cualquier situación de negocio en un
análisis estructurado, aplicando el framework de consultoría estratégica
adecuado — no todos a la vez, y no antes de tiempo.

En vez de responder con marcos genéricos o un muro de texto, la skill primero
pregunta lo mínimo imprescindible (negocio, objetivo, horizonte, alcance),
identifica si el problema es **estratégico** (largo plazo) o **táctico**
(corto plazo), elige entre 1 y 3 frameworks del árbol de decisión y entrega un
informe con secciones y tablas, listo para usar.

## ✨ Por qué esta skill

- **Pregunta antes de analizar.** Nada de DAFO automático sin contexto: la
  skill recopila negocio, objetivo, horizonte temporal y alcance antes de
  elegir el marco.
- **Un árbol de decisión, no un catálogo.** 20+ frameworks organizados por
  *situación del usuario*, para que se aplique el correcto y no el más
  popular.
- **Distingue estrategia de táctica** de forma explícita en cada informe —
  nunca se mezclan sin avisar.
- **Salida consistente.** Plantilla de informe + tablas por framework
  (DAFO, PESTEL, Porter, BMC, 7S, matriz impacto/esfuerzo, mapa de
  stakeholders...) en vez de prosa libre.
- **Cierre con narrativa opcional.** Solo si el usuario lo pide, ofrece
  ayudar a comunicar la estrategia ya definida — nunca antes de que exista.

## 📦 Instalación

Copia esta carpeta dentro de tu directorio de skills de Claude Code
(`.claude/skills/` o `.agents/skills/`, según tu configuración):

```bash
git clone https://github.com/daaniidev/strategic-thinking-skill.git
```

Claude Code detectará automáticamente `SKILL.md` y activará la skill cuando
la conversación lo justifique.

## 🚀 Cuándo se activa

Di cosas como:

> "Necesito un DAFO para mi negocio"
> "¿Cómo estructuro un plan estratégico de expansión?"
> "Quiero validar mi modelo de negocio con un Business Model Canvas"
> "Estamos bloqueados en una decisión importante, ¿qué framework me ayuda?"
> "Analiza la competencia con las 5 fuerzas de Porter"

## 🗂️ Árbol de decisión de frameworks

| Situación | Framework(s) |
|---|---|
| Entorno rápido e impredecible | VUCA / BANI |
| Punto de partida general, riesgos internos/externos | DAFO / FODA |
| Entorno macro | PESTEL |
| Estructura competitiva de un sector | 5 fuerzas de Porter |
| Diseño o validación del modelo de negocio | Business Model Canvas |
| Expansión a nuevos mercados | Matriz de Ansoff |
| Diseño organizativo interno | McKinsey 7S |
| Ventaja competitiva interna | VRIO, cadena de valor, estrategias genéricas |
| Portafolio de negocios/productos | Matriz BCG / GE-McKinsey |
| Espacio de mercado nuevo | Blue Ocean, Jobs to be Done, Tres Horizontes |
| Definición de metas | SMART / OKR |
| Seguimiento de una estrategia ya definida | Balanced Scorecard |
| Bloqueo en una decisión | Cynefin, seis sombreros, árboles de decisión |
| Mapeo de stakeholders / priorización | Matriz de Mendelow, impacto/esfuerzo |
| Cambio organizacional en marcha | Proceso de Kotter (8 pasos) |
| Decisión de inversión con impacto económico | Business case, ROI/NPV, unit economics |
| Comunicar la estrategia a terceros | Narrativa estratégica (al final, bajo demanda) |

*(Tabla completa con referencias de archivo en [`SKILL.md`](SKILL.md).)*

## 📁 Estructura del proyecto

```
.
├── SKILL.md                        # Definición de la skill, flujo y árbol de decisión
├── assets/templates/
│   ├── informe-estrategico.md      # Esqueleto del informe final
│   └── tablas-frameworks.md        # Tablas por framework (DAFO, PESTEL, BMC...)
├── references/                     # Un archivo por familia de frameworks
│   ├── marcos-entorno.md
│   ├── dafo-pestel.md
│   ├── porter-canvas.md
│   ├── mckinsey-7s.md
│   ├── estrategia-competitiva.md
│   ├── matrices-portafolio.md
│   ├── innovacion-crecimiento.md
│   ├── objetivos-smart.md
│   ├── balanced-scorecard.md
│   ├── toma-decisiones.md
│   ├── stakeholders-riesgo.md
│   ├── fundamentos-financieros.md
│   ├── fundamentos-estrategia.md
│   ├── narrativa-estrategica.md
│   └── glosario-y-checklist.md
└── LICENSE
```

## 🔗 Límite con skills de marca

Si la petición es puramente de identidad o posicionamiento de marca (naming,
manifiesto, arquitectura de marca), esta skill lo indica explícitamente y
recomienda usar `brand-strategy` o `brand-positioning` en su lugar, en vez de
forzar un DAFO/PESTEL sobre un problema que no lo es.

## 📄 Licencia

[MIT](LICENSE) © 2026 daanidev
