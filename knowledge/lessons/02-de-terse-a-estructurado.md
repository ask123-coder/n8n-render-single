# L2 — De Terse a Estructurado (sin perder velocidad)

## El diagnóstico

56% de tus prompts son <100 caracteres. Para asks simples esto funciona. Para asks técnicos o estratégicos, genera ambigüedad que cuesta múltiples turnos de corrección.

La meta no es escribir más — es escribir **better-loaded** las veces que importa. Ningún acrónimo te va a salvar si no tienes claro el principio: **Claude no puede adivinar lo que no le diste.**

## El principio (no el acrónimo)

Antes de enviar un prompt complejo, respóndete 3 preguntas:

1. **¿Qué sabe Claude que necesita saber?** → Contexto relevante, no todo
2. **¿Qué quiero que haga exactamente?** → Verbo claro + scope definido
3. **¿Cómo quiero recibir la respuesta?** → Formato + extensión + nivel

Si las 3 tienen respuesta, el prompt está listo. Si no, está incompleto.

## 3 patrones según el tipo de ask

### Patrón RTF — Para asks rápidos (80% de los casos)
**R**ol · **T**area · **F**ormato

```
Eres [rol específico]. [Tarea concreta con contexto mínimo]. Output: [formato y extensión].
```

Ejemplo:
> Eres un copy director B2B. Reescribe este asunto de email para directores de empresas inmobiliarias medianas en México — sin jerga técnica, orientado a beneficio. Max 60 caracteres.

### Patrón Deep — Para asks estratégicos o complejos
**C**ontexto · **T**area · **C**onstraints · **F**ormato · **E**jemplo (opcional)

```
Contexto: [background necesario — stack, situación, restricciones del entorno]
Tarea: [qué exactamente debe producir Claude]
Constraints: [qué no puede hacer, qué límites hay]
Output: [formato, extensión, nivel de detalle]
Ejemplo de lo que quiero: [si aplica]
```

Ejemplo:
> **Contexto:** Tengo un curso de IA para empresa inmobiliaria (50 empleados, perfil no técnico). Ya existe material base de HIR Casa.  
> **Tarea:** Genera el módulo de apertura: gancho + objetivos + ejercicio de activación.  
> **Constraints:** No mencionar ChatGPT por nombre. Lenguaje accesible nivel secundaria.  
> **Output:** Estructura en markdown, máx 400 palabras, listo para copiar a presentación.

### Patrón Few-Shot — Para formatos que Claude debe replicar
Cuando el output debe seguir un estilo específico, muestra primero:

```
Ejemplos del formato que quiero:
[ejemplo 1]
[ejemplo 2]

Ahora genera [N] más con estas variaciones: [especificación]
```

Ejemplo:
> Estos son 2 subject lines que funcionaron para mi audiencia de directores mexicanos:
> - "Tu equipo lleva 6 meses sin usar IA. Aquí está por qué."
> - "El problema con los cursos de IA que ya tomaste"
>
> Genera 5 más con el mismo tono. Tema: automatización de procesos.

## Regla práctica

| Tipo de ask | Patrón | Tiempo de escritura |
|---|---|---|
| Fact, resumen, conversión simple | Terse está bien | <10 seg |
| Reescritura, copy, análisis rápido | RTF | 20-30 seg |
| Estrategia, propuesta, plan | Deep | 45-90 seg |
| Replicar un estilo o formato | Few-Shot | 60 seg + ejemplos |
| Debug técnico (Make/n8n) | Template L1 | Usar `/workflow-debug` |

## El atajo real

El tiempo que "pierdes" escribiendo un prompt estructurado (45 seg) lo recuperas en el primer turno. Un prompt terse que genera 3 rondas de corrección cuesta 5-10 minutos. **La inversión es negativa.**

Guarda estos 3 snippets como text expanders (Raycast / TextExpander):

```
# RTF
Eres []. [tarea + contexto mínimo]. Output: [formato, extensión]

# Deep  
Contexto: 
Tarea: 
Constraints: 
Output: [formato] [extensión] [nivel]

# Debug (ver L1)
/workflow-debug
```

## Ejercicio

Toma los últimos 3 prompts que te generaron >5 turnos de corrección. Identifica cuál de las 3 preguntas no tenía respuesta en el prompt original. Reescríbelos con el patrón correcto. La diferencia suele ser 1 prompt vs 1 thread.
