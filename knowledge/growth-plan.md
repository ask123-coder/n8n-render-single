# Plan de Crecimiento — Alberto Saltiel × Claude

*Actualizado: junio 2026 · Integra: Digital Passport + 93 conversaciones ChatGPT + Plan Maestro ASK v4 + recursos Anthropic*

---

## Executive Summary

El objetivo no es "aprender Claude". Es **usar Claude como motor de ASK para generar $1,020k MXN antes de noviembre 2027**. Las habilidades técnicas de Claude son los instrumentos, no el fin.

Tu gap no es de conocimiento — es de protocolo y sistemas. Tienes el instinto, el stack y la visión. Lo que falta: prompts front-loaded que eviten espirales de 100 turnos, Skills que sistematicen tu delivery, y Notion+MCP como cerebro operativo vivo dentro de Claude Code.

**Alineación con fases ASK:**
- 30 días → Cierre Fase 0 (junio 2026): Claude listo para operar el negocio
- 60 días → Arranque Fase 1 (julio 2026): Claude activo en entrega a clientes
- 90 días → Fase 1 en velocidad (agosto-septiembre 2026): pipeline automatizado

---

## Baseline

| Dimensión | Estado actual | Target 90 días |
|---|---|---|
| Prompt sophistication | 10% avanzado, 56% básico (<100 chars) | >60% avanzado |
| Turns por sesión técnica | 100-167 (espiral) | <15 (front-loaded) |
| Reutilización de contexto | Manual, ad-hoc | Automática via CLAUDE.md + Skills |
| Claude Code dominio | CLI básico | Skills + Hooks + MCP activos |
| Notion via MCP | Databases creadas | Claude lee/escribe Notion en tiempo real |
| Propuestas ASK generadas con Claude | 0 sistematizadas | Template + `/ask-proposal` skill activo |
| Sistemas autónomos | 0 | 2+ Routines corriendo |

---

## Lecciones Personalizadas

| # | Lección | Archivo | Relevancia para ASK |
|---|---|---|---|
| L1 | El Problema de los 100 Turnos | `lessons/01-...` | Debug de automatizaciones para clientes |
| L2 | De Terse a Estructurado | `lessons/02-...` | Propuestas, scripts, contenido de cursos |
| L3 | Skills como Módulos | `lessons/03-...` | Sistema de delivery reproducible |
| L4 | MCP como Integraciones | `lessons/04-...` | Notion ya conectado — activar ahora |
| L5 | Hooks como Triggers | `lessons/05-...` | Automatización del workflow de desarrollo |
| L6 | Subagentes como Flows Paralelos | `lessons/06-...` | Análisis inmobiliario para clientes |

---

## Plan 30 / 60 / 90 Días

### 30 días — Cierre Fase 0 (junio 2026)

Objetivo: Claude Code operacional como herramienta de negocio antes del lanzamiento.

| Semana | Acción | Entregable para ASK |
|---|---|---|
| 1 | Leer L1 + L2. Activar `/workflow-debug` y `/prompt-audit` | 0 sesiones de debug >30 turnos |
| 2 | Leer L4. Conectar Claude Code a Notion via MCP — verificar que lee D1-D6 | Claude consulta Pipeline y Clientes en tiempo real |
| 3 | Leer L3. Crear `/ask-proposal` y `/course-builder` | Primer borrador de propuesta generada por Claude |
| 4 | Cerrar pendientes Fase 0: subir cursos anteriores a knowledge base | Base de conocimiento ASK completa en el repo |

**Métrica de éxito:** CLAUDE.md activo + Notion MCP funcionando + 3 Skills de negocio operativos.

### 60 días — Arranque Fase 1 (julio 2026)

Objetivo: Claude como copilot activo en la entrega a clientes y activación del pipeline de referidos HIR Casa.

| Semana | Acción | Entregable para ASK |
|---|---|---|
| 5 | Leer L5. Configurar Hook de log de sesiones | Visibilidad de cuánto tiempo dedicas a cada área |
| 6 | Activar pipeline de referidos HIR Casa con Claude: analizar encuestas, generar scripts de seguimiento | Script `/ask-referral-followup` + análisis de respuestas |
| 7 | Primer cliente Fase 1: usar Claude para preparar propuesta Nivel 1 o 2 | Propuesta generada con `/ask-proposal` en <30 min |
| 8 | Documentar caso HIR Casa con Claude (Anexo G) | Primer draft del caso de estudio listo |

**Métrica de éxito:** Al menos 1 propuesta enviada generada con Claude + pipeline de referidos activado.

### 90 días — Fase 1 en velocidad (agosto-septiembre 2026)

Objetivo: Sistemas autónomos que mantengan el pipeline vivo en modo Mínimo.

| Semana | Acción | Entregable para ASK |
|---|---|---|
| 9 | Leer L6. Crear subagentes para análisis de cliente: `client-researcher` + `proposal-drafter` | Flujo de propuesta paralelo: investigación + redacción simultánea |
| 10 | Configurar primera Routine: revisión semanal de pipeline en Notion | Routine activa cada lunes — resumen de D2 Pipeline sin intervención manual |
| 11 | Blog post de Claude Code: leer Dynamic Workflows + Managed Agents | Evaluar si Managed Agents aplica para automatizaciones Nivel 4 |
| 12 | Auditoría: ¿qué tareas de Fase 1 siguen siendo manuales? | Lista de candidatos para automatizar en Fase 2 |

**Métrica de éxito:** 1 Routine activa + flujo de propuesta <45 min de principio a fin.

---

## Skills ASK (Claude Code)

| Skill | Archivo | Para qué en ASK |
|---|---|---|
| `/context-load` | `.claude/commands/context-load.md` | Carga perfil + contexto ASK al inicio de sesión |
| `/prompt-audit` | `.claude/commands/prompt-audit.md` | Mejora prompts antes de enviar |
| `/workflow-debug` | `.claude/commands/workflow-debug.md` | Debug de Make/n8n para clientes |
| `/plan-builder` | `.claude/commands/plan-builder.md` | Planes con hitos y métricas |
| `/brief-content` | `.claude/commands/brief-content.md` | Brief para scripts, posts, material de cursos |
| `/ask-proposal` | `.claude/commands/ask-proposal.md` | Genera propuesta comercial (Nivel 1-4) |
| `/course-builder` | `.claude/commands/course-builder.md` | Estructura curso en cualquier nivel |

## Subagentes activos

| Agente | Archivo | Uso |
|---|---|---|
| `real-estate-analyst` | `.claude/agents/real-estate-analyst.md` | Análisis de mercado para clientes inmobiliarios |

---

## Recursos Prioritarios

| Prioridad | Recurso | Por qué |
|---|---|---|
| 1 | [How to configure hooks](https://claude.com/blog/how-to-configure-hooks) | Triggers = automatización del workflow diario |
| 2 | [Subagents in Claude Code](https://claude.com/blog/subagents-in-claude-code) | Análisis paralelo para propuestas de clientes |
| 3 | [Lessons: How we use skills](https://claude.com/blog/lessons-from-building-claude-code-how-we-use-skills) | Mejores prácticas de Skills del equipo de Anthropic |
| 4 | [Introducing routines](https://claude.com/blog/introducing-routines-in-claude-code) | Revisión de pipeline automática (semana 10) |
| 5 | [Claude Code docs](https://code.claude.com/docs/en/overview) | Referencia técnica de todo lo anterior |

---

## Métricas de Progreso

| Métrica | Ahora | 30d (Fase 0 cierre) | 60d (Fase 1 arranque) | 90d (Fase 1 velocidad) |
|---|---|---|---|---|
| Turns / sesión técnica | ~100 | <20 | <15 | <10 |
| Skills activos | 5 base | +2 ASK | +2 más | 10+ |
| Notion MCP activo | Databases creadas | Leer/escribir funcionando | En uso diario | Routine automática |
| Propuestas con Claude | 0 | Template listo | 1 enviada | 3+ en pipeline |
| Tiempo por propuesta | Manual, variable | <60 min | <45 min | <30 min |
| Routines autónomas | 0 | 0 | 0 | 1 (pipeline review) |
| % prompts avanzados | 10% | 40% | 60% | >75% |
