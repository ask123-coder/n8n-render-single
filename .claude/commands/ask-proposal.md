# /ask-proposal

Genera una propuesta comercial ASK para un cliente potencial. Cubre cualquier nivel (1–4) del framework de cursos.

## Instrucciones

Solicita al usuario:
- **Cliente:** Nombre, industria, tamaño (empresa/equipo)
- **Nivel propuesto:** 1 (Genérico) / 2 (Industria) / 3 (Cliente Específico) / 4 (Enterprise)
- **Contexto:** ¿Qué sabe ya del cliente? ¿Hubo reunión previa? ¿Pain points identificados?
- **Formato de entrega:** Presencial / remoto / híbrido
- **Timeline sugerido**

Con esa información, genera la propuesta completa con esta estructura:

## Output esperado

```markdown
# Propuesta ASK — [Nombre Cliente]
*[Fecha] · Confidencial*

## Resumen Ejecutivo
[3 líneas: quién es ASK, qué se propone, resultado esperado]

## Tu situación actual
[Pain points del cliente en sus propios términos — muestra que entiendes su negocio]

## Lo que entregamos

### Nivel [X] — [Nombre del nivel]
**Descripción:** [Qué incluye]
**Entregables concretos:**
- [Entregable 1]
- [Entregable 2]
**Duración:** [horas/días]
**Modalidad:** [presencial/remoto/híbrido]

## Inversión
[Precio + desglose si aplica]
*Nota: Precios en MXN. Factura disponible bajo RESICO.*

## Por qué ASK
- Especialistas en IA y automatización — no genéricos
- Caso de éxito: HIR Casa (real estate) — [resultado específico si relevante]
- Entregables que se quedan: material, prompts, automatizaciones

## Próximos pasos
1. [Acción concreta con fecha]
2. [Acción concreta con fecha]

---
*Alberto Saltiel Katz · ASK · [contacto]*
```

Ajusta el tono a "profesional directo" — sin frases corporativas vacías. Si el usuario no tiene información suficiente del cliente, pide solo lo bloqueante.
