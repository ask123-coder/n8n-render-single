# /brief-content

Genera un brief estructurado para contenido antes de escribir copy, emails, posts o cualquier pieza de comunicación. Elimina el loop de "no, más en este tono" / "para esta audiencia" / "más corto".

## Instrucciones

Solicita al usuario:
- **Pieza:** ¿Qué se va a crear? (email, post, landing, script, etc.)
- **Audiencia:** ¿Quién lo va a leer/ver? (nivel de sofisticación, relación con la marca)
- **Objetivo:** ¿Qué acción o percepción debe generar?
- **Tono:** Si no lo especifica, da opciones: Profesional formal / Profesional directo / Conversacional / Técnico
- **Constraints:** Extensión máxima, palabras a evitar, formato requerido

Con el brief completo, genera la pieza directamente. No pidas aprobación del brief a menos que haya ambigüedad crítica.

## Output del brief (solo si hay gaps)

```
## Brief de contenido

**Pieza:** [tipo]
**Audiencia:** [descripción]
**Objetivo:** [acción/percepción target]
**Tono:** [seleccionado]
**Extensión:** [palabras/caracteres/párrafos]
**Constraints:** [lista]

---
[Contenido generado]
```

Si el usuario ya dio suficiente contexto en su mensaje, ve directo a la pieza sin mostrar el brief.
