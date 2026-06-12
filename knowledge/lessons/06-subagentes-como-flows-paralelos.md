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

Los subagentes son archivos Markdown en `.claude/agents/` — igual que los Skills, pero con su propio system prompt y permisos de herramientas.

```
.claude/
├── commands/        ← Skills (slash commands)
│   └── prompt-audit.md
└── agents/          ← Subagentes
    ├── market-analyst.md
    ├── financial-modeler.md
    └── risk-checker.md
```

Cada archivo de subagente define:
- Su rol y system prompt
- Qué herramientas puede usar
- Qué modelo usar (opcional, puede ser diferente al orquestador)

Luego le dices al orquestador:
```
"Analiza esta propiedad. Lanza los 3 subagentes en paralelo:
market-analyst, financial-modeler, risk-checker.
Sintetiza los resultados en un executive summary."
```

Claude Code maneja la orquestación internamente.

## Aplicaciones para tus proyectos actuales

| Proyecto | Cómo aplicar subagentes |
|---|---|
| Real estate prospecting | Agente mercado + Agente financiero + Agente riesgo → Ejecutivo |
| Audit de automatizaciones | Agente por cada flow → Reporte consolidado |
| Mentorship content | Agente investigación + Agente redacción + Agente revisión |
| CRM analysis | Agente por pipeline stage → Vista unificada |

## Siguiente paso

Antes de usar subagentes directamente, entiende bien Skills y Hooks (L3, L5). Los subagentes son el nivel avanzado — se aprovechan más cuando ya tienes tus Skills como bloques reutilizables que los subagentes pueden invocar.
