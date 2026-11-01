# vigia-campanas — las reglas de escala, cumplidas cada 30 minutos

> Ficticio, como ejemplo de una rutina con reglas fijas (Nivel 3).

Corre cada 30 minutos como script determinista (no necesita una IA por corrida). Una vez por día, la IA lee los logs y arma el resumen.

## Reglas (escritas por Valentina el 9/10)

- si ROAS de la campaña de escala ≥ 1,8 durante 3 días seguidos → subir presupuesto 20%, máximo una vez por día.
- si ROAS < 1,2 durante 2 días → bajar presupuesto 20%.
- si gasto del día > 2× el promedio de la semana sin compras → pausar y avisar ya.
- todo a nivel campaña ([memoria](../MEMORIA/roas-a-nivel-campana.md)).

## Nunca

- Crear campañas, tocar creativos o abrir cuentas.
- Subir más de una vez por día.

## Qué escribe

`RUTINAS/log/AAAA-MM-DD/vigia-campanas.md`: primera línea `OK` / `HALLAZGOS n` / `ERROR`, cada acción con hora y el número que la disparó.
