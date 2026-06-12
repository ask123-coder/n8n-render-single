# L5 — Hooks como Triggers de Automatización

## La analogía

| n8n / Make | Claude Code Hooks |
|---|---|
| Trigger "antes de ejecutar módulo" | `PreToolUse` hook |
| Trigger "después de ejecutar módulo" | `PostToolUse` hook |
| Trigger "al iniciar el flow" | `UserPromptSubmit` hook |
| Trigger "al terminar el flow" | `Stop` hook |
| Condición / filtro en el trigger | `matcher` en el hook |

Hooks son comandos shell que Claude Code ejecuta automáticamente antes o después de sus acciones. Tu lógica de automatización, dentro del entorno de desarrollo.

## Casos de uso reales

| Hook | Qué hace | Cuándo se activa |
|---|---|---|
| Auto-format | `prettier --write` después de editar código | Cada vez que Claude edita un archivo |
| Auto-lint | `eslint --fix` antes de guardar | Antes de que Claude escriba a disco |
| Log de sesión | Guarda cada acción en un archivo | Al terminar cada tool use |
| Validación de workflow | Corre tests antes de que Claude continúe | Antes de ejecutar comandos |
| Notificación | Slack webhook cuando Claude termina una tarea | Al finalizar una sesión |

## Configuración básica

En `.claude/settings.json`:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write",
        "hooks": [
          {
            "type": "command",
            "command": "prettier --write $CLAUDE_TOOL_RESULT_FILE_PATH"
          }
        ]
      }
    ],
    "Stop": [
      {
        "hooks": [
          {
            "type": "command",
            "command": "echo 'Sesión completada: $(date)' >> ~/claude-log.txt"
          }
        ]
      }
    ]
  }
}
```

## Analogía práctica para ti

En Make, cuando un módulo falla, puedes redirigir el flujo a un handler de errores. En Claude Code, el hook `PreToolUse` puede validar antes de que Claude ejecute algo potencialmente destructivo, y cancelar la operación si no pasa la validación.

Esto es especialmente útil cuando Claude Code edita archivos críticos o ejecuta comandos en producción.

## Ejercicio

Configura un hook `Stop` simple que escriba en un archivo de log la fecha y hora de cada vez que termina una sesión de Claude Code. Es el "Hello World" de los hooks — te da visibilidad inmediata de cuánto usas Claude Code y cuándo.
