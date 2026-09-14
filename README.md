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
