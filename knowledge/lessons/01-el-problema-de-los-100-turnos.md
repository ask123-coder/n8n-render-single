# L1 — El Problema de los 100 Turnos

## El diagnóstico

Tu historial muestra 3 conversaciones de 100–167 mensajes. No es falta de habilidad — es falta de protocolo inicial. Cuando el primer mensaje es terse, el LLM asume, tú corriges, él asume de nuevo. Loop.

El patrón: `pregunta vaga → respuesta amplia → "no, más bien X" → corrección → "ahora falta Y" → ...`

## La solución: Front-loading

Poner el 80% del contexto en el primer mensaje. No es más lento — es más eficiente en tiempo total.

## Template: Debug Técnico (reemplaza el spiral)

```
# Contexto
- Herramienta: [n8n / Make / otro]
- Versión / entorno: [cloud / self-hosted / versión]
- Nodo / módulo con problema: [nombre exacto]

# Comportamiento actual
[Qué pasa exactamente. Incluye el error completo si aplica.]

# Comportamiento esperado
[Qué debería pasar.]

# Lo que ya intenté
[Máximo 3 cosas. Si no intentaste nada, dilo.]

# Restricciones
[Lo que NO puedo cambiar: estructura del flow, herramientas disponibles, etc.]

# Output que necesito
[Solución lista para aplicar / explicación del root cause / ambas]
```

## Template: Ask Estratégico

```
# Contexto
[Situación en 2-3 líneas. Datos relevantes, no historia completa.]

# Objetivo
[Qué quiero lograr. Específico y medible si es posible.]

# Restricciones
[Presupuesto / tiempo / stack / lo que no puedo cambiar.]

# Output
[Formato: tabla / lista / plan / análisis. Nivel: ejecutivo / técnico / ambos.]
```

## Ejercicio

Toma tu próxima sesión técnica con Claude. Antes de escribir, completa el template de debug en <2 minutos. Observa cuántos turnos necesitas vs. tu promedio histórico.

## Métrica

- Antes: ~100 turnos por sesión técnica compleja
- Target: <10 turnos con front-loading consistente
