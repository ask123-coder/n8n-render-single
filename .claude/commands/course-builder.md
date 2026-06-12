# /course-builder

Estructura un curso ASK en cualquier nivel (1–4). Genera el esqueleto completo: bloques, contenidos por bloque, entregables y duración estimada.

## Instrucciones

Solicita al usuario:
- **Nivel:** 1 / 2 / 3 / 4
- **Industria / cliente:** (para Nivel 2-3-4, crítico)
- **Duración target:** horas totales o días
- **Audiencia:** perfil de los participantes (técnicos, directivos, mixto)
- **Contexto del cliente:** ¿qué herramientas usan ya? ¿qué procesos quieren mejorar?
- **Caso base:** ¿hay un proyecto real del cliente para usar como hilo conductor? (como Residencial Chapultepec en HIR Casa)

Con esa información genera:

## Output esperado

```markdown
# Estructura de Curso — [Nombre Cliente/Industria]
*Nivel [X] · [Duración total] · [Audiencia]*

## Lógica del diseño
[1-2 líneas explicando el hilo conductor del curso]

## Bloques

### Bloque 1 — [Nombre] ([duración])
**Objetivo:** [Qué debe saber/poder hacer el participante al terminar]
**Contenido:**
- [Tema 1]
- [Tema 2]
**Actividad práctica:** [Ejercicio concreto]
**Entregable:** [Qué se lleva el participante]

### Bloque 2 — [Nombre] ([duración])
[...]

## Entregables del curso completo
- [ ] Material de participante (.docx)
- [ ] Guión de facilitador (.docx)
- [ ] [Entregables específicos: prompts, blueprints, GPTs, etc.]

## Sistema de encuestas post-curso
- Encuesta Mismo Día Toque 1 (captura inmediata)
- Encuesta 7 Días (seguimiento de adopción)
- Encuesta Dueño/Decisor con referidos (si aplica)

## Notas de personalización
[Lo que hay que customizar con materiales del cliente antes de entregar]
```

Para Nivel 3-4, el caso base del cliente DEBE integrarse en al menos 60% de los ejercicios prácticos. Si no hay caso base todavía, marca esos bloques con `[PENDIENTE: caso base cliente]`.
