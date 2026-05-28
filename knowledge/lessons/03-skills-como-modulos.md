# L3 — Claude Code Skills como Módulos de No-Code

## La analogía

| No-Code | Claude Code |
|---|---|
| Módulo de Make / nodo de n8n | Skill (slash command) |
| Template reutilizable | `.claude/commands/nombre.md` |
| Trigger manual | `/nombre-del-skill` en el chat |
| Input del módulo | Argumentos del slash command |
| Lógica del módulo | Instrucciones en el `.md` |

Un Skill es un archivo Markdown en `.claude/commands/`. Claude lo ejecuta como instrucción cuando escribes `/nombre`.

## Estructura de un Skill

```markdown
# Nombre del Skill

Descripción de una línea de qué hace.

## Instrucciones

[Lo que Claude debe hacer cuando se invoca este skill.
Puede incluir templates, pasos, criterios de evaluación, etc.]

## Output esperado

[Formato y estructura del resultado.]
```

## Tus Skills prioritarios (ya creados en este repo)

- `/prompt-audit` — Revisa y mejora un prompt
- `/workflow-debug` — Debug estructurado de automatizaciones
- `/plan-builder` — Genera planes con hitos y métricas
- `/context-load` — Carga tu Digital Passport como contexto
- `/brief-content` — Brief para contenido (tono, audiencia, formato)

## Cómo usar un Skill

1. Escribe `/prompt-audit` en Claude Code
2. Claude lee el archivo `.claude/commands/prompt-audit.md`
3. Ejecuta las instrucciones definidas ahí
4. Si el skill acepta argumentos: `/prompt-audit Crea un plan de 90 días para...`

## Cómo crear un Skill nuevo en <5 minutos

```bash
# En tu terminal con Claude Code activo
# Simplemente dile: "Crea un skill llamado /X que haga Y"
# O créalo manualmente:
touch .claude/commands/mi-skill.md
```

Luego escribe las instrucciones en el archivo. La próxima vez que escribas `/mi-skill`, Claude lo ejecuta.

## Caso de uso inmediato

El skill `/workflow-debug` reemplaza directamente tus conversaciones de 100-167 turnos de debug en n8n y Make. En lugar de explicar el contexto cada vez, el skill fuerza la estructura correcta desde el primer mensaje.
