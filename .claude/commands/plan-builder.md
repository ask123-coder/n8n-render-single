# /plan-builder

Genera un plan estructurado con timeline, hitos y métricas de éxito. Para cualquier objetivo: proyecto, aprendizaje, lanzamiento, sistema.

## Instrucciones

Pide al usuario:
- **Objetivo:** ¿Qué quiere lograr?
- **Timeline:** ¿Cuánto tiempo tiene? (si no lo da, asume 30/60/90 días)
- **Contexto:** ¿Qué ya tiene / qué ya intentó?
- **Recursos:** ¿Qué limitaciones hay? (tiempo semanal, presupuesto, equipo)

Con esa información, genera el plan con esta estructura:

## Output esperado

```markdown
## Executive Summary
[2-3 líneas: objetivo, approach, resultado esperado]

## Baseline
[Qué existe hoy. Punto de partida medible.]

## Plan por fases

### Fase 1 — [Nombre] ([semanas/días])
| Semana | Acción | Entregable |
|---|---|---|
| 1 | ... | ... |

### Fase 2 — [Nombre]
...

## Métricas de éxito

| Métrica | Ahora | [Fase 1] | [Fase Final] |
|---|---|---|---|
| ... | ... | ... | ... |

## Riesgos principales
1. [Riesgo] → [Mitigación]

## Próximo paso inmediato
[Una acción específica para empezar hoy]
```

Sé específico. Si el usuario da objetivos vagos, presiona por métricas concretas antes de generar el plan.
