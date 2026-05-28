# L6 — Subagentes como Flows Paralelos

## La analogía

| n8n / Make | Claude Code Subagentes |
|---|---|
| Flow paralelo (branches) | Múltiples agentes corriendo en paralelo |
| Subflow / llamada a otro escenario | Agent tool invocation |
| Router que distribuye trabajo | Agente orquestador |
| Módulo especializado | Agente con rol específico |
| Merge de branches | Síntesis del orquestador |

Un subagente es una instancia de Claude con un contexto y objetivo específico, invocada por otro Claude (el orquestador). El orquestador coordina, los subagentes ejecutan.

## Cuándo usar subagentes

- Tarea que tiene partes independientes que pueden correr en paralelo
- Necesitas perspectivas diferentes sobre el mismo problema (como tener dos analistas)
- Tarea demasiado larga para un solo contexto
- Quieres aislar responsabilidades (investigación vs. redacción vs. validación)

## Ejemplo práctico — Análisis de propiedad inmobiliaria

**Sin subagentes (secuencial):**
1. Claude busca datos del mercado → 2. Analiza financieramente → 3. Evalúa riesgos → 4. Redacta resumen

**Con subagentes (paralelo):**
- Agente A: Análisis de mercado comparativo
- Agente B: Modelado financiero y proyecciones
- Agente C: Detección de riesgos regulatorios
- Orquestador: Recibe los 3 outputs y genera el ejecutivo

Resultado: 3x más rápido, cada agente enfocado en su especialidad.

## Cómo funciona en Claude Code

```
# Le dices al orquestador:
"Analiza esta propiedad. Lanza 3 subagentes en paralelo:
1. Análisis de mercado y comparables
2. Proyección financiera a 5 años
3. Checklist de riesgos regulatorios
Sintetiza los resultados en un executive summary."
```

Claude Code maneja la orquestación internamente usando el Agent SDK.

## Aplicaciones para tus proyectos actuales

| Proyecto | Cómo aplicar subagentes |
|---|---|
| Real estate prospecting | Agente mercado + Agente financiero + Agente riesgo → Ejecutivo |
| Audit de automatizaciones | Agente por cada flow → Reporte consolidado |
| Mentorship content | Agente investigación + Agente redacción + Agente revisión |
| CRM analysis | Agente por pipeline stage → Vista unificada |

## Siguiente paso

Antes de usar subagentes directamente, entiende bien Skills y Hooks (L3, L5). Los subagentes son el nivel avanzado — se aprovechan más cuando ya tienes tus Skills como bloques reutilizables que los subagentes pueden invocar.
