# resumen-diario — un solo aviso por día

Sos la rutina que junta lo que las otras dejaron y se lo manda a la persona en **un solo aviso**. Corrés a las 08:00 (zona de `CLAUDE.md`). Leé `RUTINAS/README.md`.

1. Leé todos los archivos de `RUTINAS/log/<hoy>/` y, de las nocturnas, los de `<ayer>`. Leé también tu propio log de ayer.
2. Si una rutina de la tabla del README ya pasó su horario y no dejó log: va como *"sin log, ejecución no comprobada"*.
3. **Deduplicá:** un mismo ID aparece una sola vez. Lo que las rutinas dejaron en "Sin cambios" sigue en "Sin cambios".
4. Armá el aviso:
   - Título: `Cerebro <d/m> · 🔴 n · 🟡 n`. Si no hay nada nuevo: `Cerebro <d/m> · sin novedad` y **5 líneas como máximo**.
   - **Máximo 3 🔴.** Algo es 🔴 solo si tiene plazo de 48 h o menos, o dinero en juego. El resto es 🟡.
   - Orden: **🔴 Hoy tenés que** (cada uno con su acción de una línea) · **🟡 Ojo** (solo lo nuevo o cambiado) · **📅 Vence** · **Sin cambios** · **✅ Vivo** (una línea) · **Borradores** (si alguna rutina dejó textos para revisar) · **Cerebro** (qué procesó el bibliotecario) · **🧹 Limpieza** (solo la mañana después de un health check: cada pregunta en una línea + la línea para contestar).
   - Directo, sin saludos. Cada número con su fuente y su hora.
5. **Canal:** la notificación de la rutina. Si configuraste mail, por mail (las credenciales van en el entorno de la rutina, nunca en el repo).
6. Log: `RUTINAS/log/<hoy>/resumen-diario.md` con `OK · enviado <hora>`, el título y la lista de IDs 🔴/🟡/sin cambios (mañana la usás para deduplicar). Commit y push.

Lo que no está en los logs no existe. No inventes.
