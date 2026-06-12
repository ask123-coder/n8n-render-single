# /ask-upsell-analyzer

Analiza los resultados de encuestas post-curso (Toque 2 empleados y Ejecutiva dueño) para identificar oportunidades de upsell concretas y generar el mensaje de seguimiento.

## Instrucciones

Solicita al usuario:
- **Cliente:** Nombre
- **Respuestas P7** (qué no lograron aplicar) — pegar respuestas
- **Respuestas P9** (qué procesos automatizar) — pegar respuestas
- **Respuesta P4 dueño** (apertura a siguiente paso) — pegar respuesta
- **Respuesta P5 dueño** (referidos mencionados) — pegar respuesta

Analiza y genera:

## Output esperado

```markdown
## Análisis de Upsell — [Cliente]

### Oportunidades detectadas (ordenadas por probabilidad)

**Alta probabilidad:**
- [Oportunidad basada en respuestas P9] → Servicio recomendado: [Implementación llave en mano / Nivel 4 / Acompañamiento 1-a-1] · Precio: $[X]
  
**Media probabilidad:**
- [Oportunidad basada en P7] → Servicio: [Sesión de seguimiento grupal $25k]

**Referidos a contactar:**
- [Nombre/empresa mencionada por dueño] → Canal: [tío/contacto directo]

### Mensaje de seguimiento recomendado (para llamada o email)
[Texto listo para usar, conectando sus respuestas específicas con la solución]

### Siguiente paso accionable
[Una acción concreta con fecha sugerida]
```

Nunca inventes oportunidades que no están respaldadas por las respuestas. Si las respuestas son débiles en señales de upsell, dilo directamente.
