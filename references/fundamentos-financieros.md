# Fundamentos financieros para decisiones de inversión

**Advertencia de alcance**: esto NO es un curso de finanzas corporativas ni
sustituye un análisis financiero profesional para decisiones grandes (una
ronda de inversión, una adquisición, una reestructuración de deuda). Es el
mínimo de números que un desarrollador/emprendedor necesita para no decidir a
ciegas cuando una decisión estratégica tiene un componente de inversión o
escalado — justo lo suficiente para detectar si una idea es obviamente buena,
obviamente mala, o merece que alguien con más profundidad financiera la mire
antes de comprometer dinero. Deliberadamente no incluye WACC, valoración de
empresa, EBITDA ajustado ni modelos de descuento de flujos completos: eso
pertenece a un asesor financiero, no a esta skill.

## 1. Business case (caso de negocio estratégico)

Un business case es un documento breve (3-7 páginas) que justifica una
inversión conectando problema, opciones, coste, beneficio esperado, riesgo y
una recomendación explícita. No es un framework de análisis nuevo — es cómo
se **empaqueta** el resultado de un análisis (DAFO, coste/beneficio, un árbol
de decisión — ver `references/toma-decisiones.md`) para pedir aprobación o
presupuesto a quien no ha estado en el proceso.

**Cuándo usarlo**: cuando ya se ha decidido internamente qué se quiere hacer y
hace falta convencer a alguien (un socio, un inversor, un cliente, uno mismo
antes de comprometer ahorros) de que la inversión tiene sentido. Nunca es el
punto de partida de un análisis — es el envoltorio final.

### Estructura mínima

1. **Resumen ejecutivo** — una página, se escribe al final aunque va primero.
   Problema, recomendación y coste/beneficio en cuatro frases.
2. **Problema/oportunidad** — qué pasa si esto no se aborda, con datos si los
   hay.
3. **Opciones** — mínimo 3, siempre incluyendo:
   - No hacer nada (opción base, para poder comparar el coste de no actuar).
   - Solución parcial (más barata, resuelve parte del problema).
   - Solución completa (la recomendada, si aplica).
4. **Coste y beneficio esperado** — cifras, aunque sean estimaciones con
   rango ("entre 8.000€ y 15.000€", no solo "caro"). Aquí es donde encajan
   las secciones 2 y 3 de este archivo (unit economics y criterios de
   inversión) si la decisión lo requiere.
5. **Riesgos** — 3-5, cada uno con probabilidad, impacto y mitigación.
6. **Recomendación** — la opción elegida, ligada explícitamente a los números
   anteriores, con un plazo de decisión o ejecución.

Esta estructura se rellena dentro de `assets/templates/informe-estrategico.md`
ya existente (secciones "Contexto recopilado", "Análisis" y "Recomendaciones
priorizadas" cubren la mayoría del business case); no crees una plantilla
paralela.

### Preguntas guía

- ¿La opción de "no hacer nada" es realmente viable, o es solo la excusa
  cómoda para no decidir?
- ¿El beneficio esperado está sustentado en datos (ventas pasadas, tasas de
  conversión, benchmarks del sector) o es una esperanza disfrazada de
  proyección?
- ¿Qué riesgo de la lista, si se materializa, invalida toda la
  recomendación? Si la respuesta es "ninguno en concreto", probablemente
  falta identificar el riesgo real.

## 2. Unit economics (CAC, LTV, margen por unidad)

Antes de mirar la cuenta de resultados agregada de un negocio, hay que saber
si gana o pierde dinero por cada cliente o unidad individual. Es esencial
antes de escalar: un negocio puede parecer sano en el agregado (más ingresos
cada mes) mientras pierde dinero en cada cliente nuevo, compensado solo por
el volumen — una ilusión contable que revienta en cuanto se intenta crecer
más rápido.

**Fórmulas simplificadas:**

- **CAC** (coste de adquisición de cliente) = Gasto total en marketing y
  ventas / Nº de clientes nuevos adquiridos.
- **LTV** (valor de vida del cliente) ≈ (Ingreso medio por cliente × Margen
  bruto) / Tasa de abandono (churn).
- **Ratio LTV:CAC** = LTV / CAC. Regla de referencia: ≥ 3:1 se considera
  saludable; < 1:1 significa que cada cliente cuesta más de lo que genera
  (el negocio pierde dinero por cliente, no solo "a corto plazo").
- **Margen por unidad** = Precio de venta − Coste variable directo por
  unidad.

**Cuándo usarlo**: antes de decidir escalar adquisición de clientes, entrar
en un mercado nuevo, o cuando el negocio crece en ingresos pero no se tiene
claro si crece en rentabilidad real.

### Preguntas guía

- ¿Ganamos dinero por cliente antes de contar gastos generales, o solo
  "a escala" — es decir, la mejora solo aparece si se asume un volumen que
  todavía no existe?
- Si duplicamos el gasto de adquisición para entrar en un mercado nuevo,
  ¿el CAC sube más rápido de lo que sube el LTV en ese mercado?
- ¿Qué pasa con el ratio LTV:CAC si el churn empeora un 5% al entrar en un
  segmento nuevo? (Un ratio saludable en el segmento actual puede no
  sobrevivir a un churn distinto en uno nuevo.)

## 3. Criterios simples de evaluación de inversión

Tres formas rápidas de valorar si una inversión concreta compensa, ordenadas
de más simple a más completa. Ninguna sustituye un análisis financiero
riguroso — son suficientes para descartar opciones claramente malas o
comparar alternativas del business case entre sí.

- **Payback period (periodo de recuperación)** = Coste de la inversión /
  Flujo de caja anual generado. Da en cuántos meses o años se recupera lo
  invertido. Simple de calcular, pero ignora qué pasa después de recuperar
  la inversión y el valor del dinero en el tiempo (1.000€ hoy valen más que
  1.000€ dentro de tres años).
- **ROI simple** = (Beneficio − Coste) / Coste, expresado en %.
- **NPV/VAN muy simplificado** (valor actual neto): convierte dinero futuro
  a "euros de hoy" descontándolo un porcentaje, y resta la inversión
  inicial. Positivo significa que el proyecto genera más valor del que
  cuesta (incluyendo el coste de oportunidad); negativo significa que no
  compensa frente a esa alternativa. Fórmula de un solo flujo:

  ```
  NPV = Flujo futuro / (1 + i)^t − inversión inicial
  ```

  No hace falta calcularlo a mano ni con precisión de decimales — la idea a
  transmitir es: cuidado con comparar dos proyectos solo por su beneficio
  total si tardan en llegar en plazos muy distintos; el NPV corrige ese
  sesgo temporal. Cuidado también con la falsa precisión: inventarse una
  tasa de descuento concreta y presentarla como si fuera un cálculo riguroso
  es peor que no calcularlo, porque aparenta un rigor que no existe.

### Preguntas guía

- ¿En cuánto tiempo recupero la inversión, y ese plazo es aceptable dado el
  riesgo de la opción elegida?
- ¿El ROI de esta opción es claramente mejor que el de las alternativas
  descartadas en el business case, o es un empate que en realidad se decide
  por otros factores (riesgo, plazo, capacidad del equipo)?
- Si comparo dos opciones con el mismo ROI pero una tarda el doble en dar
  resultados, ¿cuál preferimos y por qué? (No hay respuesta única — depende
  de cuánto valga la rapidez en ese contexto — pero la pregunta debe
  hacerse explícita, no asumirse.)

## Cuándo cargar este archivo

Solo cuando la decisión tiene un componente explícito de inversión o
escalado (pedir presupuesto, decidir si escalar adquisición de clientes,
comparar alternativas de inversión con cifras). Nunca es el punto de entrada
por defecto de un análisis: el punto de partida sigue siendo DAFO/PESTEL para
diagnóstico y el análisis coste/beneficio cualitativo de
`references/toma-decisiones.md` para decisiones sin necesidad de este nivel
de detalle numérico.
