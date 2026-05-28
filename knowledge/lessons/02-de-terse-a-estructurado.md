# L2 — De Terse a Estructurado (sin perder velocidad)

## El diagnóstico

56% de tus prompts son <100 caracteres. Para asks simples esto funciona. Para asks técnicos o estratégicos, genera ambigüedad que cuesta múltiples turnos de corrección.

La meta no es escribir más — es escribir mejor las veces que importa.

## El framework PCICO (en <30 segundos)

| Bloque | Pregunta que responde | ¿Siempre necesario? |
|---|---|---|
| **P**ersona | ¿Qué rol debe adoptar Claude? | No (solo si el rol cambia el output) |
| **C**ontexto | ¿Qué background necesita saber? | Sí, siempre |
| **I**nstrucción | ¿Qué exactamente debe hacer? | Sí, siempre |
| **C**onstraints | ¿Qué no puede hacer / qué límites hay? | Si aplica |
| **O**utput | ¿En qué formato quiero la respuesta? | Sí, siempre |

## Regla práctica

- **Ask simple** (facts, conversión, resumen corto): terse está bien.
- **Ask técnico o estratégico**: mínimo C + I + O.
- **Ask de sistema o plan**: PCICO completo.

## Comparación real (de tu historial)

**Terse (lo que hacías):**
> "Break down the top 5% of knowledge I need to master no-code development"

**Estructurado (lo que funciona mejor):**
> **Contexto:** Tengo 3 años de experiencia con Make, n8n y Airtable. Domino flujos básicos e intermedios.
> **Instrucción:** Dame el 5% de conocimiento de no-code que separa a los practitioners del top tier del resto.
> **Constraints:** Enfocado en automatización y AI integration, no en apps visuales tipo Bubble/Webflow.
> **Output:** Lista priorizada, máx 10 ítems, con una línea de por qué cada uno importa.

La versión estructurada elimina 2-3 turnos de "¿pero para qué nivel?" y "¿incluyo herramientas de frontend?".

## Atajo de velocidad

Guarda este snippet como template de texto expansor (Raycast, TextExpander, o atajo de teclado):

```
C: 
I: 
Constraints: 
O: [formato: ] [nivel: ]
```

Llenar esto toma <20 segundos y elimina el spiral.

## Ejercicio

Toma los últimos 5 prompts que escribiste. Identifica cuáles eran de categoría "técnico o estratégico" y tenían <100 chars. Reescríbelos con C+I+O. Nota la diferencia en especificidad.
