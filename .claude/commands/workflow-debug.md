# /workflow-debug

Debug estructurado de automatizaciones (n8n, Make, Zapier, APIs). Reemplaza las sesiones de 100+ turnos con un protocolo de diagnóstico front-loaded.

## Instrucciones

Solicita al usuario que complete esta estructura antes de diagnosticar. Si ya la proporcionó, úsala directamente.

```
HERRAMIENTA: [n8n / Make / Zapier / API / otro]
ENTORNO: [cloud / self-hosted / versión si aplica]
NODO/MÓDULO: [nombre exacto del paso con problema]

ERROR: [mensaje de error completo, o "ninguno pero el comportamiento es incorrecto"]
COMPORTAMIENTO ACTUAL: [qué pasa]
COMPORTAMIENTO ESPERADO: [qué debería pasar]

YA INTENTÉ: [máx 3 cosas, o "nada aún"]
NO PUEDO CAMBIAR: [restricciones de estructura, herramientas, permisos]
OUTPUT NECESARIO: [solución aplicable / explicación del root cause / ambas]
```

Con esa información:
1. Diagnóstica el root cause en máximo 3 líneas
2. Da la solución paso a paso, lista para aplicar
3. Si hay múltiples causas posibles, ordénalas por probabilidad
4. Si necesitas más información, pide solo lo que es bloqueante — no hagas 5 preguntas a la vez

## Output esperado

```
## Root cause
[1-3 líneas]

## Solución
1. [Paso concreto]
2. [Paso concreto]
...

## Verificación
[Cómo confirmar que funcionó]

## Prevención
[Una línea de cómo evitar que vuelva a pasar]
```
