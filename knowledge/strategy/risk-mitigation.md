# Mapa de Riesgos → Mitigaciones ASK

*Bridge document: conecta Plan_Maestro_ASK_v4.pdf (riesgos) con growth-plan.md (skills/lecciones)*
*Fuente primaria: Plan Maestro ASK v4.0 — Sección 7 Riesgos + Sección Skills*

---

## Por qué existe este archivo

`Plan_Maestro_ASK_v4.pdf` documenta 7 riesgos con probabilidades y contingencias.
`knowledge/growth-plan.md` documenta las habilidades técnicas de Claude y los skills de negocio.
Este archivo mapea explícitamente cada riesgo a los skills y lecciones que lo mitigan — cerrando el gap entre la estrategia y la ejecución.

---

## Mapa Riesgo → Mitigación

### R1 — Pipeline vacío en Fase 1
**Probabilidad:** 40%
**Contingencia Plan Maestro:** Precio temporal $90k o Nivel 1 $35k como entrada
**Mitigado por:**
- `/ask-proposal` — genera propuestas en <30 min, reduce fricción de ventas
- `/ask-pipeline-review` — revisión semanal previene que el pipeline se vacíe sin detectarlo
- `/ask-upsell-analyzer` — activa referidos de HIR Casa como fuente de leads calificados
- `knowledge/growth-plan.md` → Plan 60 días: pipeline de referidos HIR Casa activado en semana 6
- `real-estate-analyst` subagente — análisis rápido de prospectos inmobiliarios acelera calificación

---

### R2 — Cancelación Nivel 4 mid-delivery
**Probabilidad:** 15%
**Contingencia Plan Maestro:** Contratos 50% inicio + 50% milestone 4
**Mitigado por:**
- `/course-builder` — estructura modular con entregables claros por etapa facilita milestone tracking
- `/ask-proposal` — propuestas con términos de pago explícitos desde el inicio
- `L1: El Problema de los 100 Turnos` — debug estructurado reduce fricciones técnicas que pueden escalar a cancelación

---

### R3 — Crisis emocional / recaída operativa
**Probabilidad:** 35%
**Contingencia Plan Maestro:** Sistema 3 modos (Sprint/Normal/Mínimo) + revisión domingo con pareja
**Mitigado por:**
- `/ask-pipeline-review` — revisión semanal estructurada los domingos: termómetro de meta + modo de la semana
- `CLAUDE.md → Modos de operación` — Mínimo = 30 min/día + 1 acción. Sistema que no se cancela.
- `growth-plan.md → Baseline` — métricas visibles previenen sorpresas que disparan crisis

---

### R4 — Conflicto 9-5 vs ASK
**Probabilidad:** 25%
**Contingencia Plan Maestro:** Evaluar caso a caso — acelerar o pausar ASK
**Mitigado por:**
- Modo Mínimo documentado en `CLAUDE.md` — ASK nunca para, solo baja de velocidad
- `growth-plan.md → Plan 30 días` — estructura de 1-2 hrs/día compatible con carga laboral normal
- `/ask-pipeline-review` — visibilidad de avance evita acumulación de deuda operativa

---

### R5 — Comoditización del mercado
**Probabilidad:** 60% (riesgo más alto documentado)
**Contingencia Plan Maestro:** Profundizar Nivel 3-4, abandonar Nivel 1 si presión llega
**Mitigado por:**
- `L3: Skills como Módulos` — sistema de delivery reproducible y propietario, difícil de copiar
- `L6: Subagentes como Flows Paralelos` — capacidades de análisis paralelo que genéricos no tienen
- `/course-builder` — cursos construidos sobre casos reales del cliente (60%+ ejercicios con su contexto)
- `/ask-proposal` — posicionamiento como especialista en IA y automatización, no "experto en ChatGPT"
- `CLAUDE.md → Posicionamiento` — multi-plataforma (Claude + ChatGPT + Gemini + Make + n8n) como escudo
- Rutina de actualización de stack cada 3-4 meses (documentada en Plan Maestro)

---

### R6 — Cambio tecnológico disruptivo
**Probabilidad:** 40%
**Contingencia Plan Maestro:** Multi-plataforma protege. Actualizar stack c/3-4 meses.
**Mitigado por:**
- `L4: MCP como Integraciones` — arquitectura de conectores intercambiables: si una plataforma muere, el conector se reemplaza
- `L5: Hooks como Triggers` — automatizaciones independientes de plataforma específica
- `CLAUDE.md → Stack tecnológico` — Fase 1: Claude+ChatGPT+Gemini+Make | Fase 2: +agents+MCP | Fase 3: +Ollama local
- `growth-plan.md → 90 días semana 11` — revisión de Dynamic Workflows + Managed Agents como checkin trimestral

---

### R7 — Cliente Enterprise demanda fuera del alcance
**Probabilidad:** 50%
**Contingencia Plan Maestro:** Subcontratar freelance (costo de delivery)
**Mitigado por:**
- `L6: Subagentes como Flows Paralelos` — arquitectura que permite delegar tareas específicas a agentes especializados
- `/ask-proposal` — propuestas con scope claro y exclusiones explícitas desde el inicio
- `CLAUDE.md → Regla 12` — NO Nivel 4 nuevo después de agosto 2027: límite hard que previene sobrecompromisos

---

## Posicionamiento → Skills que lo implementan

| Principio (Plan Maestro) | Implementado por |
|---|---|
| Especialista multi-plataforma (no "experto en ChatGPT") | `L4 MCP` + `/ask-proposal` + `CLAUDE.md Stack por fase` |
| Ventana de diferenciación 18-24 meses | `L3 Skills` + `/course-builder` (Nivel 3-4 profundización) |
| "Miembro externo del board para temas de IA" | `/ask-change-mgmt` (Fase 2+) |
| Todo curso = oportunidad de upsell | `/ask-encuesta-deployer` + `/ask-upsell-analyzer` |

---

## Fases Plan Maestro → Acciones en growth-plan.md

| Fase (PDF) | Período | Meta | Acción en growth-plan.md |
|---|---|---|---|
| Fase 0 | Junio 2026 | Inversión | Plan 30 días — sistema operativo |
| Fase 1 | Jul-Dic 2026 | $200-280k | Plan 60 días — pipeline activo |
| Fase 2 | Ene-Jun 2027 | $300-450k | Plan 90 días — routines autónomas |
| Fase 3 | Jul-Nov 2027 | $200-300k | Change Management + Nivel 3-4 exclusivo |

---

## Modelo financiero → Skills de soporte

| Regla financiera (Plan Maestro) | Soportada por |
|---|---|
| 50/30/20 de cada cobranza | `/ask-pipeline-review` — registra cobranza real vs meta |
| 16-20% reserva fiscal | `/ask-pipeline-review` — termómetro incluye desglose |
| Meta $56,667 MXN/mes promedio | `/ask-pipeline-review` → métrica semanal de avance |
| Costo operativo 10-15% ingresos | Visible en `/ask-pipeline-review` mensual |
