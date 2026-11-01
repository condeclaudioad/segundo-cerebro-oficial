# Segundo Cerebro Oficial

**Todos usamos los mismos modelos. Lo único que te diferencia del de al lado es el contexto que le das a la IA.**

Este repo es ese contexto, armado. Lo clonás, lo abrís con Claude Code (o Codex), escribís `/instalar` y en 5 minutos tenés tu segundo cerebro andando: una carpeta con tu negocio adentro, que tu IA lee antes de cada respuesta y que crece sola con el uso.

Y trae instalada la lógica que uso para automatizar: **los 3 niveles**. Qué se habla con la IA, qué se guarda como método y qué corre solo.

---

## El problema: la amnesia

Abrís la IA en una pestaña en blanco. Le explicás quién sos, qué vendés, cómo te gusta que te hablen. Te da algo decente. Cerrás.

Al otro día, de nuevo. Y al otro.

No es que la IA sea mala. Es que **arranca de cero cada vez**. Le explicás lo mismo por tercera vez y te devuelve algo genérico, porque no sabe nada de vos.

La solución no es un modelo mejor. Es que la IA **siempre arranque parada en tu contexto**.

## Qué es un segundo cerebro

- **Una carpeta con tu negocio adentro.** Quién sos, qué vendés, tus números, tus reglas, tus decisiones.
- **Abrís la IA siempre parada ahí.** Nunca suelta en una pestaña en blanco: ahí arranca la amnesia.
- **Crece con el uso.** Cada conversación deja algo guardado. A los meses, la IA conoce tu negocio mejor que un empleado nuevo.
- **Vive en GitHub, en un repo privado.** Lo ven tu compu, la nube y el celular. Lo que no está subido, no existe.

---

## Los 3 niveles

```
   NIVEL 3 · RUTINA  ············  la skill corre sola, cada X tiempo o cuando pasa algo
        ▲
   NIVEL 2 · SKILL  ·············  tu método probado, guardado: lo llamás por su nombre
        ▲
   NIVEL 1 · HABLAR CON LA IA  ··  le contás el problema y lo resuelven juntos

   ═══════════════ todo corre adentro de tu segundo cerebro ═══════════════
```

Casi todo el mundo se queda en el primero. No porque sea difícil subir. Porque nadie les dijo que había más.

**¿A qué nivel va una tarea? Tres preguntas, en orden:**

1. **¿La hacés 2-3 veces por semana o más?** No → **Nivel 1**. Hablalo con la IA y listo.
2. **¿Necesitás ver el resultado antes de que salga?** Sí → **Nivel 2**. Creativos, mensajes a clientes, guiones: la IA produce, vos aprobás.
3. **¿Se puede escribir como "si pasa X, hacé Y"?** Sí → **Nivel 3**, rutina. No → se queda en Nivel 2.

Un ejemplo de cada lado:

| ❌ Rutina que no sirve | ✅ Rutina que sí |
|---|---|
| *"Haceme 10 creativos por día y subilos."* Querés verlos: si el audio quedó, si los cortes están bien. Es automatizable, pero es Nivel 2. | *"Si el ROAS de la campaña supera mi vara, subí el presupuesto."* La regla la escribiste vos. La rutina solo la cumple, a cualquier hora, sin cansarse. |

### Delegá la ejecución. Nunca el criterio.

Las decisiones, los cambios de dirección y lo que necesita revisión quedan en tus manos. Si le pedís a la IA *"haceme un negocio que facture"* y te vas, te devuelve algo mediocre. Las rutinas que escalan campañas solas funcionan porque alguien escribió las reglas, y ese alguien sigue mirando que se cumplan.

---

## Instalación en 3 pasos

**1. Creá tu copia, privada.**
Arriba a la derecha: **Use this template → Create a new repository → Private**.
O por terminal, si tenés la CLI de GitHub:
<!-- PENDIENTE DE CONFIRMAR: cuenta de GitHub desde la que se publica (condeclaudioad por defecto). -->
```bash
gh repo create mi-cerebro --private --template condeclaudioad/segundo-cerebro-oficial --clone
```
> ⚠️ **Siempre privado.** Esta plantilla es pública; tu cerebro no.

**2. Abrí la carpeta con tu IA.**
- **Claude Code** (app de escritorio): entrá a Code y elegí la carpeta. Por terminal: `cd mi-cerebro && claude`.
- **Codex**: abrí la carpeta como proyecto.

**3. Escribí `/instalar`.**
Te hace preguntas cortas, casi todas con opciones: quién sos, qué vendés, cómo te gusta trabajar, qué decisiones no delegás nunca. Con eso completa tu perfil, tu negocio y tus primeras reglas. En Codex, decile: *"Leé AGENTS.md e instalá mi cerebro"*.

Y listo. Lo primero que te va a ofrecer es mapear tu negocio en los 3 niveles para saber qué automatizar primero.

---

## Qué trae

```
segundo-cerebro-oficial/
├── CLAUDE.md          ← las reglas del bibliotecario + los 3 niveles (Claude Code)
├── AGENTS.md          ← la entrada para Codex y otros agentes
├── RAW/               ← lo que entra crudo: notas, audios, transcripciones
├── WIKI/              ← tu conocimiento ordenado, un archivo por tema
├── OUTPUTS/           ← entregables con fecha
├── MEMORIA/           ← las reglas de cómo se trabaja, cada una con su porqué
├── SKILLS/            ← el catálogo de tus métodos guardados (Nivel 2)
├── RUTINAS/           ← lo que corre solo (Nivel 3) + sus logs
├── changelog/         ← qué cambió, un archivo por mes, lo nuevo arriba
├── SESIONES/          ← notas de traspaso para retomar sin reexplicar
├── .claude/skills/    ← las 11 skills, listas para usar
└── ejemplo/           ← un cerebro ficticio con 3 meses de uso
```

### Las skills que vienen instaladas

| Comando | Qué hace |
|---|---|
| `/instalar` | Te hace preguntas con opciones y arma tu cerebro |
| `/mapear-negocio` | Marketing, ventas y producto, proceso por proceso: en qué nivel va la IA y qué queda en tus manos |
| `/procesar-raw` | Lee lo nuevo de `RAW/`, lo ordena en `WIKI/` y te dice qué le falta saber |
| `/crear-skill` | Convierte una tarea que repetís en skill (**Nivel 1 → 2**) |
| `/crear-rutina` | Convierte una skill con reglas fijas en rutina, y te dice dónde tiene que correr (**Nivel 2 → 3**) |
| `/recordar` | Guarda una regla para no explicarla nunca más |
| `/preparar-manana` | A la noche le contás tus tareas de mañana y la IA adelanta todo lo que puede |
| `/matriz` | Tus pendientes en costo × impacto: las 3 tareas de hoy |
| `/cerrar` · `/retomar` | Cerrás guardando todo; mañana volvés al contexto en 15 segundos |
| `/limpieza` | Cada 15 días: qué borrar, qué mantener, qué actualizar. Pregunta antes de tocar |

### Las rutinas de plantilla

Cuatro prompts listos para programar en la nube: **bibliotecario nocturno** (procesa lo nuevo cada noche), **resumen diario** (un solo aviso a la mañana), **vigía** (que nada se apague en silencio) y **matriz del domingo** (las 3 tareas del lunes). Cómo programarlas, en [RUTINAS/README.md](RUTINAS/README.md).

Empezá por una. Cuando su primer aviso te llegue y lo leas tres días seguidos, sumá la siguiente.

---

## Cómo se ve a los 3 meses

En [`ejemplo/`](ejemplo/README.md) hay un cerebro ficticio con 3 meses de uso: una persona que vende plantillas digitales, con su WIKI, su changelog, sus memorias, dos skills propias, una rutina que escala campañas con sus reglas y los logs de lo que corrió anoche.

| | Semana 1 | Semana 13 |
|---|---|---|
| Cómo arranca el día | Chat en blanco, explicar el negocio otra vez | `/retomar` y a trabajar |
| Lo repetido | Se pide de cero cada vez | Skills con su método y sus correcciones adentro |
| Lo que tiene reglas fijas | Lo mira ella, varias veces por día | Una rutina lo cumple; ella lee el aviso |
| Lo que decide ella | Todo, incluido lo repetitivo | Solo lo que necesita criterio |

No es un modelo distinto. Es el mismo modelo, con 3 meses de contexto adentro.

---

## El día a día

1. **Abrí la IA siempre desde tu cerebro.** Es el hábito. Todo lo demás depende de esto.
2. **Mañana empieza la noche anterior.** Anotá las tareas de mañana y contáselas a tu IA con lujo de detalle, como a tu mano derecha (`/preparar-manana`). Ella adelanta lo que se puede: borradores, investigación, presentaciones, guiones. A la mañana revisás en vez de arrancar de cero.
3. **Tirá todo a `RAW/`.** Notas, transcripciones de llamadas, audios. Después `/procesar-raw`, o que lo haga el bibliotecario nocturno.
4. **Cuando explicás algo por tercera vez, es una skill.** `/crear-skill`.
5. **Cerrá con `/cerrar`.** Abrí con `/retomar`.
6. **Cada 15 días, `/limpieza`.** Más contexto no es mejor contexto: lo viejo y lo duplicado ensucia las respuestas.

## Dónde corre cada cosa

| Situación | Dónde | Por qué |
|---|---|---|
| Estás trabajando | Tu compu, con tu IA abierta en el cerebro | Es tu herramienta de trabajo |
| Rutina que es todo API | La nube de tu IA (las *routines* de Claude Code) | No depende de que nada esté prendido |
| Rutina que necesita navegador logueado o mucho cómputo | Una computadora en la nube | Tiene tus accesos y potencia, y tu compu queda libre |
| Cuenta determinista cada pocos minutos | Un script con cron (GitHub Actions, por ejemplo) | No hace falta una IA por cada latido |

**Por qué no todo en tu compu:** lo que corre solo en tu compu se apaga en silencio cuando la cerrás. Y no podés trabajar mientras la IA la usa.

¿Qué herramienta? A la mayoría le alcanza con Claude Code. Codex funciona igual con este repo: las reglas están en `AGENTS.md`.

---

## Preguntas

**¿Necesito saber programar?**
No. Necesitás abrir una carpeta y escribir. La IA hace el resto y te pregunta con opciones cuando le falta algo.

**¿Mis datos quedan públicos?**
No, si tu repo es privado (el paso 1 lo crea así). Tené en cuenta que lo que le mandás a la IA lo procesa el proveedor del modelo. Y nunca guardes contraseñas ni keys en el cerebro: las reglas ya lo prohíben.

**¿Sirve con Windows?**
Sí. Son archivos de texto y git.

**¿Y si ya tengo notas en otro lado?**
Tiralas a `RAW/` y corré `/procesar-raw`. Si ya tenés un cerebro armado, no lo pises: pedile a tu IA que compare tus reglas con las de este repo y te proponga solo lo que te falta.

**¿Esto me va a hacer facturar más?**
Esto ordena tu contexto y te saca lo repetitivo de encima. Lo que hagas con el tiempo que te devuelve depende de vos. Nadie que te prometa una cifra te está diciendo la verdad.

---

## Quién lo armó

Soy **Claudio Conde**. Opero mis negocios con este sistema todos los días, y esta es la plantilla de mi propio cerebro, sin mis datos adentro.

Si querés ver cómo lo uso por dentro y aprender a montar tu negocio con IA, con criterio y no con humo:

- **ND1 Club** → [nd1.ai](https://nd1.ai/)
- **Instagram** → [@condeclaudioad](https://www.instagram.com/condeclaudioad/)

Si te sirvió, dejale una ⭐ al repo y pasáselo a alguien que todavía le explica su negocio a la IA cada mañana.

---

Licencia [MIT](LICENSE). Usalo, cambialo, compartilo.
