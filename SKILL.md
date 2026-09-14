---
name: pensamiento-mentalidad-estrategica
description: Aplica pensamiento y mentalidad estratégica corporativa a una situación de negocio: pregunta primero el contexto que falte (negocio, objetivo, horizonte, alcance) y luego aplica el framework adecuado, distinguiendo si la petición es estratégica (largo plazo) o táctica (corto plazo). Cubre marcos de entorno (VUCA, BANI, PESTEL, escenarios), análisis competitivo y de portafolio (DAFO, 5 fuerzas de Porter, VRIO, BCG, GE-McKinsey), modelo de negocio y crecimiento (Business Model Canvas, Ansoff, Blue Ocean, Jobs to be Done), organización y objetivos (McKinsey 7S, SMART, OKR, Balanced Scorecard), decisión y cambio (Cynefin, seis sombreros, Kotter) y fundamentos financieros/narrativa estratégica. Devuelve un informe estructurado con recomendaciones priorizadas. Use when user says "estrategia", "DAFO", "FODA", "PESTEL", "plan estratégico", "análisis competitivo", "modelo de negocio", "Business Model Canvas", "McKinsey 7S", "OKR", "matriz BCG", o para expandirse, invertir o decidir algo complejo.
---

# Pensamiento y mentalidad estratégica

Skill de consultoría estratégica: convierte una situación de negocio en un
análisis estructurado usando el framework adecuado, no todos a la vez.

## Límite con skills de marca

Si la petición es puramente de identidad/posicionamiento de marca (naming,
manifiesto, arquitectura de marca), dilo explícitamente y sugiere `brand-strategy`
o `brand-positioning` en vez de forzar DAFO/PESTEL sobre un problema de marca.

## 1. Flujo híbrido: preguntar antes de analizar

Antes de aplicar cualquier framework, pregunta lo que falte de esta lista (no
repitas lo que el usuario ya dio en su mensaje; máximo 4-5 preguntas, una sola
vez):

1. **Contexto del negocio** — sector, tamaño, situación actual (¿ya opera, es una
   idea, está en crisis?).
2. **Objetivo / problema a resolver** — qué decisión hay que tomar o qué pregunta
   hay que responder.
3. **Horizonte temporal** — corto plazo (< 1 año → táctico) vs largo plazo
   (expansión, inversión, transformación → estratégico). Esta respuesta decide la
   etiqueta explícita "esto es estratégico" / "esto es táctico" que debe aparecer
   en la salida.
4. **Alcance** — interno (organización, procesos, personas), externo (mercado,
   competencia, entorno macro) o ambos.
5. *(Opcional, solo si es relevante)* restricciones — presupuesto, plazo duro,
   partes interesadas a convencer.

Nunca mezcles estratégico y táctico sin decirlo explícitamente en la respuesta.

## 2. Árbol de decisión de frameworks

No apliques más de 2-3 frameworks por análisis salvo que el usuario pida
expresamente "un análisis completo". Si la situación es ambigua, usa DAFO como
entrada por defecto y ofrece ampliar.

| Situación del usuario | Framework(s) | Referencia |
|---|---|---|
| Cambios rápidos e impredecibles del entorno | VUCA | `references/marcos-entorno.md` |
| Dinámicas internas / desafíos existenciales del nuevo mundo laboral | BANI | `references/marcos-entorno.md` |
| Factores internos/externos de riesgo, punto de partida general | DAFO/FODA | `references/dafo-pestel.md` |
| Entorno macro (político, económico, social, tecnológico, ecológico, legal) | PESTEL | `references/dafo-pestel.md` |
| Estructura competitiva de un sector/mercado | 5 fuerzas de Porter | `references/porter-canvas.md` |
| Diseño o validación del modelo de negocio | Business Model Canvas | `references/porter-canvas.md` |
| Expansión a nuevos mercados o crecimiento (producto/mercado actual vs. nuevo) | Matriz de Ansoff | `references/porter-canvas.md` |
| Diseño organizativo interno (estructura, sistemas, cultura) | McKinsey 7S | `references/mckinsey-7s.md` |
| Análisis interno de ventaja competitiva (recursos, actividades, postura competitiva) | Estrategias genéricas de Porter, cadena de valor, VRIO | `references/estrategia-competitiva.md` |
| Portafolio de varios negocios/productos: dónde invertir, mantener o desinvertir | Matriz BCG / GE-McKinsey | `references/matrices-portafolio.md` |
| Sector saturado, necesidad de espacio de mercado nuevo o repensar dónde innovar | Blue Ocean, Tres Horizontes de McKinsey, Jobs to be Done, Innovator's Dilemma | `references/innovacion-crecimiento.md` |
| Definición de metas y objetivos | SMART (+ OKR si hay que desplegarlo en el tiempo) | `references/objetivos-smart.md` |
| Traducir una estrategia ya definida en un sistema de indicadores de seguimiento | Balanced Scorecard | `references/balanced-scorecard.md` |
| Bloqueo en una decisión concreta | Modelos de decisión (racional, intuitivo, Cynefin, seis sombreros, árboles de decisión, coste/beneficio) | `references/toma-decisiones.md` |
| Necesidad de generar opciones antes de decidir | Lluvia de ideas, Delphi, equipos multifuncionales, design thinking | `references/toma-decisiones.md` |
| Mapeo de partes interesadas o priorización de iniciativas/riesgos | Matriz de Mendelow, matriz impacto/esfuerzo, matriz de riesgos | `references/stakeholders-riesgo.md` |
| Cambio organizacional en marcha | Proceso de cambio estratégico de Kotter (8 pasos: urgencia, coalición conductora, visión, comunicación, empoderamiento, victorias tempranas, consolidar, anclar en la cultura) | `references/toma-decisiones.md` |
| Entorno muy incierto, decisión grande e irreversible a varios años | Planificación de escenarios | `references/marcos-entorno.md` |
| Decisión de inversión/expansión con impacto económico directo | Business case, unit economics, payback/ROI/NPV simplificado | `references/fundamentos-financieros.md` |
| Necesidad de comunicar o vender el plan a otros | Narrativa estratégica — se ofrece al final, no se aplica de entrada | `references/narrativa-estrategica.md` |
| Fundamentos generales (6P, qué contiene una estrategia, liderazgo vs gestión) | Marco de fondo, casi siempre implícito | `references/fundamentos-estrategia.md` |
| Dudas de terminología, checklist de calidad antes de entregar | — | `references/glosario-y-checklist.md` |

Carga solo el/los archivo(s) de `references/` que correspondan a la situación —no
los cargues todos de entrada.

## 3. Plantilla de salida

Usa `assets/templates/informe-estrategico.md` como esqueleto del informe, y
`assets/templates/tablas-frameworks.md` para la tabla del framework aplicado
(DAFO 2x2, PESTEL, Porter, BMC 9 bloques, 7S, matriz impacto/esfuerzo, mapa de
stakeholders). Salida por defecto: informe estructurado con secciones/tablas, no
un muro de texto conversacional.

Antes de entregar, repasa el checklist de calidad de
`references/glosario-y-checklist.md`.

## 4. Cierre: ofrecer narrativa estratégica

Al final del informe, si el usuario no lo pidió ya, pregunta:

> "¿Quieres que te ayude también a comunicar esta estrategia — construir el
> relato para presentarla a tu equipo o a terceros?"

Solo si responde que sí, carga `references/narrativa-estrategica.md` y aplica ese
módulo. Nunca antes: la narrativa comunica una estrategia que todavía no existe.

## 5. Tono general

La mentalidad estratégica (valores, liderazgo, narrativa, visión de largo plazo)
puede impregnar el tono general de tus respuestas en esta sesión cuando el
usuario esté claramente en modo de reflexión o decisión de negocio de fondo —
pero no la fuerces en preguntas puntuales, técnicas o conversacionales dentro de
la misma sesión; vuelve a un tono neutro en cuanto el tema se aleje de la
estrategia.
