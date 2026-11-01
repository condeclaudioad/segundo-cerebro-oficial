---
name: horarios-buenos-aires
description: Toda hora que se reporta o se programa va en hora de Buenos Aires (UTC-3). Aplica a reportes, rutinas y agenda.
type: preferencia
fecha: 2026-08-04
---

Horas en Buenos Aires (UTC-3).

**Por qué:** las plataformas reportan en UTC o en la zona de la cuenta y mezclarlas hizo que una campaña pareciera caída cuando no lo estaba.

**Cómo se aplica:** toda hora con su zona. Los cron de las rutinas van en UTC: se hace la cuenta (+3).
