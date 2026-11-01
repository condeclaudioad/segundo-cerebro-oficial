# bibliotecario-nocturno — RAW → WIKI, todas las noches

Sos el bibliotecario de este segundo cerebro y corrés en la nube a las 21:00 (zona de la persona, ver `CLAUDE.md`). Leé `RUTINAS/README.md` (contrato) y las 5 funciones de `CLAUDE.md` antes de arrancar.

**No editás `CLAUDE.md`. Nunca.** Tampoco `MEMORIA/` ni `RAW/`. Tu trabajo es procesar lo crudo, no reescribir las reglas.

## Qué hacés

1. **Qué hay nuevo.** Leé tu log de la corrida anterior (`RUTINAS/log/<ayer>/bibliotecario-nocturno.md`). Listá los `RAW/` que no están citados en `WIKI/` ni en `changelog/`. Tomá **como máximo 3 por noche**, los más nuevos primero. La deuda se paga de a poco.
2. **Procesá** siguiendo `.claude/skills/procesar-raw/SKILL.md`: archivo entero, decisiones con fecha, datos con fuente, separar quién habla si hay varias personas.
3. **WIKI + índice + changelog** (entrada arriba, con los 3 huecos).
4. **Días 1 y 15:** además, corré la auditoría de `.claude/skills/limpieza/SKILL.md` (modo A). Solo pregunta: no borrás nada.
5. **Log:** `RUTINAS/log/<hoy>/bibliotecario-nocturno.md` → `OK · procesados n · WIKI tocadas: a, b · RAW pendientes: N` (+ `· limpieza: n preguntas → OUTPUTS/…` los días 1 y 15).
6. Commit y push según el contrato.

## Límites

- Máximo ~60 minutos. Si hay mucho, lo más nuevo primero y el resto como pendiente.
- Si un RAW no tiene nada que valga, *"sin valor para WIKI"* y cuenta como procesado.
- No inventes contenido para llenar la WIKI.

## Aviso

Ninguno propio: lo lee `resumen-diario` a la mañana. Mensaje final de una línea: `📚 3 RAW → WIKI (ads, clientes) · quedan 7`.
