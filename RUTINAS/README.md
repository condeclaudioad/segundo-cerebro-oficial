# RUTINAS — lo que corre sin vos (Nivel 3)

Una rutina es una skill que se dispara sola: cada X tiempo o cuando pasa algo. Vos no apretás nada.

**No todo tiene que terminar en rutina.** Lo que necesitás ver antes de que salga (creativos, mensajes a clientes, guiones) se queda en Nivel 2. Una rutina puede dejarte el borrador listo cada mañana; lo que no hace es enviarlo por vos.

## Dónde corre cada una

| Si la rutina… | Corre en… |
|---|---|
| Es todo API y deja el resultado en el repo | **La nube de tu IA.** En Claude Code son las *routines*: clonan tu repo, corren el prompt y pushean. Se crean con `/schedule` o desde claude.ai/code. |
| Necesita un navegador logueado o mucho cómputo (render) | **Una computadora en la nube** (una Mac o VM remota con tus accesos) |
| Es una cuenta determinista cada pocos minutos | **Un script con cron** (GitHub Actions con secrets, por ejemplo) y la IA solo para el resumen |
| — | **Nunca tu compu personal como base.** Se apaga en silencio cuando la cerrás. |

## El contrato (vale para todas)

1. **El prompt vive en el repo:** `RUTINAS/<slug>.md`. La rutina programada solo dice *"Leé RUTINAS/README.md y RUTINAS/<slug>.md y ejecutalo"*. Para cambiar una rutina editás el archivo, no la programación.
2. **Cada corrida deja rastro:** `RUTINAS/log/AAAA-MM-DD/<slug>.md`. Primera línea: `OK` · `HALLAZGOS n` · `ERROR <razón>`. Si no hay nada, igual escribe `OK · nada que informar`. **El silencio no distingue "todo bien" de "se murió".**
3. **Sube sus cambios bien:** `git add RUTINAS/log … && git commit && git pull --rebase origin main && git push origin HEAD:main`. Siempre `pull --rebase` antes del push (otras sesiones y rutinas también suben cosas). En la nube la sesión suele arrancar con HEAD suelto: por eso `HEAD:main` y no `main`. Si falla 3 veces, rama aparte y lo dice en el log.
4. **Solo lectura sobre el dinero y los clientes.** Leer sí. Devolver, cobrar, responder o publicar, solo si vos lo autorizaste explícito y queda escrito en su prompt.
5. **Un conector en error nunca se reporta como OK.** Sin dato no es todo bien.
6. **Sin cambios = una línea.** Antes de escribir, la rutina lee su log anterior. Un hallazgo igual al de ayer va en `## Sin cambios` como `ID · qué · desde d/m · N días`. Se repite completo solo si cambió, cruzó un plazo o empeoró. **Un rojo que sale todos los días deja de significar urgencia.**
7. **Un dueño por frente.** Si dos rutinas ven lo mismo, una lo desarrolla y la otra lo menciona en una línea.
8. **Horas en tu zona horaria.** El cron suele ir en UTC: hacé la cuenta.
9. **Una rutina no está viva hasta que su primer aviso llegó.** Corrida a mano, log leído. Escrita, programada, ejecutada y verificada son cuatro estados distintos.
10. **Las keys van en el entorno de la rutina**, nunca en el repo. Y conectores, solo los que usa.

## Cómo programar una (5 minutos)

1. Tu cerebro tiene que estar en GitHub, **privado**, con el prompt pusheado.
2. En Claude Code: `/schedule` y decile, por ejemplo: *"Creá una rutina diaria a las 21:00 de Buenos Aires que lea RUTINAS/README.md y RUTINAS/bibliotecario-nocturno.md y lo ejecute sobre este repo."* También se puede desde claude.ai/code → Routines.
3. Pegá las keys que necesite en el entorno de la rutina.
4. Corréla a mano una vez y leé el log.
5. Sumala a la tabla de abajo y a la lista de `vigia.md`.

## Las que vienen de plantilla (ninguna está programada todavía)

| slug | qué hace | cadencia sugerida | dónde |
|---|---|---|---|
| [`bibliotecario-nocturno`](bibliotecario-nocturno.md) | RAW nuevo → WIKI + índice + changelog. Días 1 y 15: auditoría con preguntas de limpieza | diaria 21:00 | nube |
| [`resumen-diario`](resumen-diario.md) | Junta los logs del día y te manda UN aviso | diaria 08:00 | nube |
| [`vigia`](vigia.md) | Que nada se apague en silencio: rutinas sin log, errores repetidos, vencimientos | diaria 07:00 | nube |
| [`matriz-domingo`](matriz-domingo.md) | Corre `/matriz` y te deja las 3 tareas del lunes | domingo 20:30 | nube |

Empezá por **una**. La que más sentido tenga para vos. Cuando su primer aviso te llegue y lo leas tres días seguidos, sumá la siguiente.
