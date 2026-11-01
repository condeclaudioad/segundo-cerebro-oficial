# SKILLS — tus métodos guardados (Nivel 2)

Una skill es un método probado que llamás por su nombre: `/procesar-raw`, `/matriz`, `/crear-skill`. La IA va sola, sin que le expliques el contexto de nuevo.

**Dónde viven:** en `.claude/skills/<nombre>/SKILL.md` (es la carpeta que Claude Code carga sola; empieza con punto, por eso no la ves en el explorador de archivos). Esta carpeta es el **catálogo**: qué hay y para qué sirve. Si usás Codex, decile *"usá la skill X"* y lee el archivo.

## Las que vienen instaladas

| Comando | Qué hace | Nivel que te ayuda a subir |
|---|---|---|
| [`/instalar`](../.claude/skills/instalar/SKILL.md) | Te hace preguntas con opciones y arma tu cerebro | — |
| [`/procesar-raw`](../.claude/skills/procesar-raw/SKILL.md) | Lee lo nuevo de `RAW/` y lo ordena en `WIKI/` | Base |
| [`/mapear-negocio`](../.claude/skills/mapear-negocio/SKILL.md) | Marketing, ventas y producto, proceso por proceso, en N1/N2/N3 | Te dice qué subir primero |
| [`/crear-skill`](../.claude/skills/crear-skill/SKILL.md) | Convierte una tarea repetida en skill | N1 → N2 |
| [`/crear-rutina`](../.claude/skills/crear-rutina/SKILL.md) | Convierte una skill con reglas fijas en rutina | N2 → N3 |
| [`/recordar`](../.claude/skills/recordar/SKILL.md) | Guarda una regla en `MEMORIA/` | Base |
| [`/preparar-manana`](../.claude/skills/preparar-manana/SKILL.md) | Le contás mañana a la noche y la IA adelanta lo que puede | Hábito |
| [`/matriz`](../.claude/skills/matriz/SKILL.md) | Ordena tus pendientes en costo × impacto: las 3 tareas de hoy | Hábito |
| [`/cerrar`](../.claude/skills/cerrar/SKILL.md) | Guarda todo y deja la nota de traspaso | Hábito |
| [`/retomar`](../.claude/skills/retomar/SKILL.md) | Te pone en contexto en 15 segundos | Hábito |
| [`/limpieza`](../.claude/skills/limpieza/SKILL.md) | Auditoría quincenal con preguntas: qué borrar, mantener o actualizar | Mantenimiento |

## Las tuyas

Las que crees con `/crear-skill` se suman acá.

| Comando | Qué hace | Cada cuánto la usás | Creada |
|---|---|---|---|

## Candidatas

Tareas que todavía son Nivel 1 pero se están repitiendo. Cuando las hiciste 3 veces igual, pasan a skill.

- _(vacío)_
