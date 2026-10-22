# Tabla de decisión

## Cancelación de un turno (RF-02)

| Condición / Acción | Regla 1 | Regla 2 | Regla por defecto |
|----------------------|---------|---------|---------------------|
| El turno está Confirmado | Sí | Sí | - |
| Faltan 24 horas o más para el turno | Sí | No | - |
| **Acción** | Cancelar el turno | No permitir la cancelación | No cancelar y avisar a la recepción |

**Regla por defecto:** cualquier caso que no sea un turno Confirmado (por
ejemplo, un turno Solicitado o Atendido) no se cancela desde el sistema y
se le avisa a la recepción. Ver la observación sobre turnos Solicitados.

**Cómo se lee esta tabla:** se evalúan las reglas de izquierda a derecha;
la primera que se cumple decide. Si ninguna se cumple, aplica la regla por
defecto.

## Observaciones

- **Conflictos detectados:** ninguno entre fragmentos.
- **Huecos del material:**
  - F2 no dice qué pasa con exactamente 24 horas de anticipación.
    [NEEDS CLARIFICATION: ¿con 24 h exactas se puede cancelar? Decide la recepción.]
  - F2 habla de cancelar un turno, pero no dice si un turno todavía
    Solicitado (sin confirmar) se puede cancelar.
- **Decisiones de negocio pendientes:** los dos huecos anteriores. Hasta
  que la recepción los decida, la regla por defecto no cancela.
