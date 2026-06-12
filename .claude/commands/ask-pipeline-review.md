# /ask-pipeline-review

Revisión semanal de pipeline ASK. Diseñado para el domingo por la noche con pareja. Genera el resumen ejecutivo de avance + decide el modo de la semana siguiente.

## Instrucciones

Consulta (vía MCP Notion si está disponible, o solicita al usuario) el estado actual de:
- D2 Pipeline: leads activos por etapa
- D5 Cobranza: ingresos cobrados en el mes
- D4 Tareas: tareas pendientes bloqueantes

Si MCP Notion no está disponible, solicita al usuario que pegue el estado actual.

Genera este output:

## Output esperado

```markdown
## Revisión ASK — Semana del [fecha]

### Termómetro de meta
$[X cobrado] / $1,020,000 MXN · [X]% acumulado
Fase [X] — [X]% de meta de fase completado

### Pipeline activo
| Lead | Nivel | Estado | Próxima acción | Fecha límite |
|---|---|---|---|---|
| [empresa] | N3 | Cotización enviada | Follow-up call | [fecha] |

### Ingresos del mes
- Cobrado: $[X]
- Meta del mes: $56,667
- Diferencia: [+/-$X]

### Modo de la semana siguiente
☐ Sprint (hay cliente en delivery)
☐ Normal (entre clientes — 1-2 hrs/día)
☐ Mínimo (semana de baja energía — 30 min + 1 acción)

**Modo seleccionado:** [X]
**Razón:** [una línea]

### 3 acciones concretas para esta semana
1. [Acción específica con responsable y fecha]
2. [Acción específica]
3. [Acción específica]

### Bloqueadores
- [Qué está deteniendo avance]

### Lección de esta semana
[Una cosa que funcionó + una cosa a mejorar]
```

Sé directo con el avance. Si hay riesgo de no alcanzar la meta de la fase, señálalo explícitamente.
