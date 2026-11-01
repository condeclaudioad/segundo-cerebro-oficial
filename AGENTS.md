# Segundo cerebro — entrada para Codex y otros agentes

Este repo es el segundo cerebro de una persona. **Las reglas completas están en [CLAUDE.md](CLAUDE.md): leelo entero antes de la primera tarea.** Valen igual para vos. Este archivo existe para que no haya dos versiones de las reglas: si cambiás una regla, cambiala en `CLAUDE.md`.

## Lo mínimo que no podés saltearte

1. Si `CLAUDE.md` tiene llaves dobles `{{ASÍ}}`, el cerebro no está instalado: leé `.claude/skills/instalar/SKILL.md` y seguilo.
2. Antes de responder, buscá en `WIKI/`, `MEMORIA/`, `OUTPUTS/` y `RAW/` (`rg` sirve). Si no está, decilo.
3. `RAW/` es solo lectura. `WIKI/` y `OUTPUTS/` las escribís vos. El changelog va por mes y **la entrada nueva va arriba**.
4. Delegá la ejecución, nunca el criterio: lo que necesita aprobación se entrega como borrador.
5. Nada de secretos en el repo.

## Skills (Nivel 2)

Las skills están en `.claude/skills/<nombre>/SKILL.md` (formato de Claude Code). Si tu herramienta no las carga sola, cuando la persona escriba `/<nombre>` o pida algo que una skill cubre, **abrí ese archivo y seguí sus pasos**. El catálogo está en [SKILLS/README.md](SKILLS/README.md).

## Rutinas (Nivel 3)

Cada rutina es un prompt en `RUTINAS/<slug>.md` con el contrato de [RUTINAS/README.md](RUTINAS/README.md). Cualquier herramienta que pueda clonar el repo y correr por horario puede ejecutarlas.
