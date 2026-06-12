# /ask-encuesta-deployer

Crea el contenido listo para desplegar las 3 encuestas post-curso en Tally. Se activa al terminar un curso o como paso 6 del proceso estándar de delivery.

## Instrucciones

Solicita al usuario:
- **Nombre del cliente:** (para personalizar)
- **Nivel del curso:** 2 / 3 / 4
- **Fecha del curso:** (para calcular envío de Toque 2 = día+7)
- **Nombre del facilitador:** Alberto (default)
- **¿Tiene permiso para caso de estudio?** Sí / No / Por confirmar

Genera las 3 encuestas completas con preguntas numeradas, listas para copiar a Tally:

## Output esperado

```markdown
## Encuesta Toque 1 — Mismo día (90 seg)
*Para: [empleados/participantes de nombre_cliente]*
*Enviar: Al finalizar el curso*

P1. En general, ¿cómo calificarías el taller de hoy? (1-10)
P2. ¿Qué fue lo más útil para tu trabajo diario?
P3. ¿Hay algo que quedó poco claro o que te gustaría explorar más?
P4. ¿Qué probabilidad hay de que recomiendes este taller a un colega? (0-10)
P5. ¿Ya tienes en mente algún proceso donde podrías usar lo aprendido? (Sí/No + cuál)

---

## Encuesta Toque 2 — Empleados Día 7
*Para: [empleados de nombre_cliente]*
*Enviar: [fecha_curso + 7 días]*

P1-P9: [estructura completa según plantilla estándar ASK]
- P7: ¿Qué herramienta o técnica intentaste usar pero no lograste aplicar? ← CLAVE UPSELL
- P9: ¿Qué proceso de tu trabajo diario crees que podría automatizarse? ← CLAVE UPSELL

---

## Encuesta Ejecutiva — Dueño/Director Día 10-12
*Para: [dueño/director de nombre_cliente]*
*Enviar: [fecha_curso + 10 días]*

P1-P5 incluyendo:
- P3: ¿Percibes cambios en cómo tu equipo usa las herramientas? ← ROI percibido
- P4: ¿Estarías dispuesto a explorar un siguiente paso con ASK? ← apertura upsell
- P5: ¿Conoces otras empresas que pudieran beneficiarse de este tipo de capacitación? ← referidos

---

## Checklist de seguimiento
- [ ] Toque 1 enviado el día del curso
- [ ] Toque 2 programado para [fecha+7]
- [ ] Ejecutiva programada para [fecha+10]
- [ ] Resultados cargados en Notion D1 Clientes
- [ ] Análisis de upsell con /ask-upsell-analyzer
```
