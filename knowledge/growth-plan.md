# Plan de Crecimiento — Alberto Saltiel × Claude

*Generado: Mayo 2026 · Basado en: Digital Passport + análisis de 93 conversaciones ChatGPT + recursos oficiales Anthropic*

---

## Executive Summary

Tienes el instinto de automatización, el stack técnico, y la visión estratégica. El gap no es de conocimiento — es de **protocolo**. Tus conversaciones de ChatGPT muestran un patrón claro: cuando el prompt inicial es sólido, resuelves en 2-3 turnos. Cuando no lo es, terminas con 100-167 mensajes de clarificación.

El plan tiene tres fases:
1. **30 días** — Eliminar el spiral. Prompting estructurado como hábito.
2. **60 días** — Trasladar tu instinto de automatización a Claude Code (Skills, Hooks, MCP).
3. **90 días** — Operar como elite: Subagentes, Routines, Agent SDK. Sistemas que se ejecutan solos.

---

## Baseline

| Dimensión | Estado actual | Target 90 días |
|---|---|---|
| Prompt sophistication | 10% avanzado, 56% básico | >60% avanzado |
| Turns por sesión técnica | 100-167 (espiral) | <15 (front-loaded) |
| Reutilización de contexto | Manual, ad-hoc | Automatizada via Skills |
| Claude Code dominio | CLI básico | Skills + Hooks + MCP activos |
| Sistemas autónomos con Claude | 0 | 3+ Routines corriendo |

---

## Lecciones Personalizadas

### L1 — El Problema de los 100 Turnos
**Archivo:** `lessons/01-el-problema-de-los-100-turnos.md`

Tu mayor oportunidad de eficiencia. Aprenderás a front-load contexto para convertir espirales en sesiones de <10 turnos. Template de debug técnico incluido.

### L2 — De Terse a Estructurado (sin perder velocidad)
**Archivo:** `lessons/02-de-terse-a-estructurado.md`

El 56% de tus prompts son <100 caracteres. Aprenderás el framework PCICO en <30 segundos de escritura, con atajos para no ralentizar tu flujo.

### L3 — Claude Code Skills como Módulos de No-Code
**Archivo:** `lessons/03-skills-como-modulos.md`

Analogía directa: Skills = módulos reutilizables. Aprenderás a crear `/prompt-audit`, `/workflow-debug`, y `/plan-builder` — tus propios módulos de Make dentro de Claude.

### L4 — MCP como Integraciones
**Archivo:** `lessons/04-mcp-como-integraciones.md`

MCP (Model Context Protocol) = conectores de Claude. Mapeo directo a tu experiencia con APIs y Webhooks. Conectar Claude a Google Drive, Airtable, o sistemas custom.

### L5 — Hooks como Triggers de Automatización
**Archivo:** `lessons/05-hooks-como-triggers.md`

Hooks en Claude Code = triggers en Make/n8n. Ejecuta acciones antes/después de cualquier operación de Claude. Tu lógica de automatización, dentro del entorno de desarrollo.

### L6 — Subagentes como Flows Paralelos
**Archivo:** `lessons/06-subagentes-como-flows-paralelos.md`

Subagentes = flows en paralelo con diferentes responsabilidades. Aprenderás a orquestar múltiples instancias de Claude para tareas complejas, análogo a ramas paralelas en n8n.

---

## Plan 30 / 60 / 90 Días

### 30 días — Protocolo Base

| Semana | Acción | Entregable |
|---|---|---|
| 1 | Leer L1 + L2. Instalar `/prompt-audit` skill | Prompts con PCICO consistente |
| 2 | Template de debug técnico en práctica | 0 sesiones de >30 turnos |
| 3 | Leer L3. Crear 3 Skills propios | `/plan-builder`, `/workflow-debug`, `/brief-content` |
| 4 | Auditoría de sesiones: medir turns promedio | Baseline documentado |

**Métrica de éxito:** Turns promedio por sesión técnica < 20.

### 60 días — Automatización Claude

| Semana | Acción | Entregable |
|---|---|---|
| 5 | Leer L4. Conectar MCP con 1 herramienta de tu stack | Claude + Airtable o Google Drive activo |
| 6 | Leer L5. Configurar 2 Hooks en tu workflow de desarrollo | Auto-validación o auto-formato activo |
| 7 | CLAUDE.md con Digital Passport como contexto persistente | 0 re-explicaciones de contexto |
| 8 | Auditoría: ¿qué tareas manuales puedes delegar a Claude? | Lista de candidatos para Routines |

**Métrica de éxito:** Al menos 1 integración MCP activa + contexto persistente funcionando.

### 90 días — Operación Elite

| Semana | Acción | Entregable |
|---|---|---|
| 9 | Leer L6. Primer flujo con Subagentes | Tarea compleja resuelta en paralelo |
| 10 | Configurar 1 Routine (tarea recurrente automatizada) | Routine activa en producción |
| 11 | Documentar tus 5 Skills más usados | Library personal de Skills |
| 12 | Evaluar Agent SDK para un proyecto real | Prototipo o plan técnico |

**Métrica de éxito:** 3+ sistemas autónomos con Claude corriendo sin intervención manual.

---

## Skills a Crear (Claude Code)

| Skill | Archivo | Función |
|---|---|---|
| `/prompt-audit` | `.claude/commands/prompt-audit.md` | Revisa y mejora un prompt antes de enviarlo |
| `/workflow-debug` | `.claude/commands/workflow-debug.md` | Template estructurado para debug de automatizaciones |
| `/plan-builder` | `.claude/commands/plan-builder.md` | Genera plan con timeline, hitos y métricas |
| `/context-load` | `.claude/commands/context-load.md` | Carga el Digital Passport como contexto de sesión |
| `/brief-content` | `.claude/commands/brief-content.md` | Brief estructurado para contenido (tono, audiencia, formato) |

---

## Recursos Prioritarios

| Recurso | URL | Por qué es relevante para ti |
|---|---|---|
| Claude Code Docs | code.claude.com/docs/en/overview | Hooks, Skills, MCP, Subagents — tu palanca principal |
| Claude API Docs | platform.claude.com/docs/en/home | Tool use, Prompt caching — nivel API |
| Build with Claude | anthropic.com/learn/build-with-claude | Solo módulos: Tool use + Agents (el resto ya lo sabes) |
| GitHub Anthropic | github.com/anthropics | Ejemplos reales, Agent SDK, repos de referencia |

---

## Métricas de Progreso

| Métrica | Ahora | 30d | 60d | 90d |
|---|---|---|---|---|
| Turns promedio / sesión técnica | ~100 | <20 | <15 | <10 |
| Skills activos propios | 0 | 3 | 5 | 8+ |
| Integraciones MCP | 0 | 0 | 1 | 3+ |
| Routines autónomas | 0 | 0 | 1 | 3+ |
| % prompts avanzados | 10% | 40% | 60% | >75% |
