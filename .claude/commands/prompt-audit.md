# /prompt-audit

Audita y mejora un prompt antes de enviarlo. Úsalo cuando tengas un ask técnico o estratégico y quieras asegurarte de que está bien especificado antes de iniciar la conversación.

## Instrucciones

El usuario te dará un prompt (o lo describirá). Evalúalo contra el framework PCICO:

| Bloque | ¿Presente? | ¿Suficiente? |
|---|---|---|
| Persona | ✓/✗ | Comentario |
| Contexto | ✓/✗ | Comentario |
| Instrucción | ✓/✗ | Comentario |
| Constraints | ✓/✗ | Comentario |
| Output format | ✓/✗ | Comentario |

Luego:
1. Da un score del 1-10 con justificación en una línea
2. Identifica los 1-2 gaps más críticos
3. Devuelve una versión mejorada del prompt, lista para usar

## Output esperado

```
## Score: X/10
[Una línea de por qué]

## Gaps críticos
- [Gap 1]
- [Gap 2]

## Prompt mejorado
[Prompt listo para copiar/pegar]
```

Sé directo. No expliques teoría — solo aplica la auditoría y entrega el resultado.
