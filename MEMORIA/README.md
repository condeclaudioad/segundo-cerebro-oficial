# MEMORIA — las reglas de cómo se trabaja

Acá no va **qué** pasó (eso es `OUTPUTS/` y `changelog/`). Acá va **cómo** se trabaja: tus preferencias, tus reglas de negocio, lo que aprendiste a la fuerza y no querés volver a explicar.

Ejemplos de memorias que valen oro:
- *"El ROAS se lee a nivel campaña, nunca por anuncio."*
- *"Todas las horas en hora de Buenos Aires."*
- *"Nunca prometer un resultado en dinero en un anuncio."*
- *"Los mensajes a clientes los mando yo: la IA deja el borrador."*

## Formato (uno por archivo)

`MEMORIA/nombre-corto-de-la-regla.md`:

```markdown
---
name: nombre-corto-de-la-regla
description: Una línea que diga la regla y cuándo aplica. Es lo que la IA lee para decidir si abrirla.
type: regla | preferencia | aprendizaje | referencia
fecha: 2026-11-03
---

La regla, dicha en una o dos frases.

**Por qué:** qué pasó o qué dato la sostiene. Sin esto, la regla se rompe en el primer caso raro.

**Cómo se aplica:** cuándo entra en juego y qué hacer concretamente.
```

- **`regla`**: algo que se cumple siempre (*"nada de reembolsos en efectivo, sí créditos"*).
- **`preferencia`**: cómo te gusta que se hagan las cosas (*"respuestas de 3-4 líneas"*).
- **`aprendizaje`**: algo que se descubrió con un error (*"al duplicar campañas, revisar que no se agregue un destino nuevo"*).
- **`referencia`**: dónde está algo (*"la key de X está en el llavero, nunca en el repo"*).

Las crea la IA con `/recordar`, o sola cuando la corregís en algo que vale para siempre. **Nunca guardes una key o una contraseña acá**: guardás dónde está, no el valor.

## Índice

Una línea por memoria, la más nueva arriba, con el formato `- [nombre](archivo.md) — fecha: la regla en una línea`.

_(vacío hasta tu primera memoria)_
