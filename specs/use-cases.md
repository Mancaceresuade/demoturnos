# Casos de uso

## UC-01: Solicitar turno

**Issue:** G00-7 · Realiza RF-01 y RF-03.

**Actor:** Paciente (principal). Recepcionista, cuando la solicitud llega por teléfono.

**Precondición:** El paciente está registrado en el consultorio.

**Flujo principal:**
1. El paciente pide un turno para una fecha y hora. Si llama por teléfono, la recepcionista carga el pedido.
2. El sistema registra la solicitud con el canal por el que llegó (RF-01).
3. Se ejecuta UC-02 Consultar agenda (include).
4. Hay lugar: el sistema confirma el turno (RF-03).
5. El sistema le informa al paciente el turno confirmado.

**Flujo(s) alternativo(s):**
- 4a. No hay lugar: se ejecuta UC-03 Ofrecer otra fecha (extend). Si el paciente acepta la fecha ofrecida, el flujo sigue en el paso 4 con esa fecha.
- 4b. El paciente no acepta ninguna fecha ofrecida: [NEEDS CLARIFICATION: el relevamiento no dice si la solicitud queda registrada o se descarta. Decide la recepción.]

**Postcondición:** El turno queda Confirmado en la agenda, con el canal por el que se pidió.

**Relaciones con otros casos de uso:**

| Relación | Caso de uso relacionado | Tipo (include/extend) | Justificación |
|----------|--------------------------|------------------------|----------------|
| UC-01 → UC-02 | Consultar agenda | include | Siempre se ejecuta: sin consultar la agenda no se sabe si hay lugar (F1). |
| UC-03 → UC-01 | Ofrecer otra fecha | extend | Solo ocurre si no hay lugar (F1). Cuando hay lugar, el flujo base termina sin ella. |

## Fragmentos considerados para este caso de uso

| Fragmento | Qué aporta al caso de uso |
|-----------|------------------------------|
| F1 | El orden de los pasos, el canal (paso 2), el include de la agenda y el extend de la otra fecha. |
| F6 | Nada todavía: «reprogramado» queda pendiente y no se modela en este caso de uso. |
