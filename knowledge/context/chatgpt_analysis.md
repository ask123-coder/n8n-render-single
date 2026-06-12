# Análisis — Historial ChatGPT

*Generado automáticamente. 93 conversaciones analizadas.*

## Distribución de temas

| Área | % aprox |
|---|---|
| No-Code / Automatización | 5% (explícito) |
| Marketing / Negocio | 7% (explícito) |
| Literatura / Creativo | 5% |
| Técnico / Código | 2% |
| General (mixto) | ~77% |

> El 77% "General" indica ausencia de organización temática, no falta de expertise.

## Nivel de sofisticación de prompts

| Nivel | % | Patrón |
|---|---|---|
| Básico (<100 chars) | 56% | Pregunta directa sin contexto |
| Intermedio (100–500 chars) | 33% | Contexto moderado, follow-ups esperados |
| Avanzado (>500 chars) | 10% | Persona + contexto + instrucción estructurada |

## Fortalezas detectadas

- Wins en pocos turnos cuando el ask es claro
- Refinamiento iterativo específico ("cambia X", "agrega restricción Y")
- Roleplay / "Act as" bien ejecutado cuando lo usa
- Code-switching ES/EN sin fricción

## Gaps principales

| Gap | Evidencia | Impacto |
|---|---|---|
| Prompts iniciales subespecificados | 3 conversaciones de 100–167 mensajes | Alto: loops de clarificación costosos |
| Sin formato de output definido | Raro uso de "dame el resultado en tabla / JSON / checklist" | Medio: outputs que requieren reformateo |
| Sin criterios de éxito en asks técnicos | Debugging n8n/Make sin especificar entorno | Alto: espirales de 100+ turnos |
| Sin reutilización de contexto | Mismo contexto re-explicado en múltiples sesiones | Medio: fricción innecesaria |

## Flujos repetidos sin sistematizar

1. "Crea un plan paso a paso para X" — sin granularidad, timeline ni métricas
2. Debug técnico (n8n, Make) — error log sin entorno ni expected behavior
3. Contenido / copy — sin brief estructurado (tono, audiencia, formato)
4. Evaluación estratégica — sin criterios de decisión predefinidos
