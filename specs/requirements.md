# Requerimientos

Sistema de gestión de turnos del consultorio. Fragmentos de origen: ver la
tabla de relevamiento del `README.md`. Convención: `skill/SKILL.md`
(atómico, verificable, sin tecnología mezclada).

## Requerimientos funcionales

| ID | Issue | Requerimiento | Nivel / Tipo | Fragmento(s) de origen | Criterio de verificación |
|----|-------|---------------|--------------|------------------------|--------------------------|
| RF-01 | G00-2 | El sistema debe registrar la solicitud de turno con el canal por el que llegó: teléfono o web. | Usuario / Funcional | F1 | Una solicitud sin canal no se puede guardar. |
| RF-02 | G00-3 | El sistema no debe permitir cancelar un turno con menos de 24 horas de anticipación. | Negocio / Funcional | F2 | Un turno al que le faltan menos de 24 horas no se puede cancelar. |
| RF-03 | G00-4 | El sistema debe confirmar el turno solo si hay lugar en la fecha y hora pedidas. | Usuario / Funcional | F1 | Un turno en un horario ya ocupado no queda Confirmado. |
| RF-04 | G00-5 | El sistema debe registrar si el paciente asistió al turno. | Usuario / Funcional | F3 | Para cualquier turno del día se puede ver si el paciente vino o no. |
| RF-05 | G00-6 | El sistema debe enviar a facturación los datos de cada consulta atendida. | Sistema / Funcional | F3 | Un turno marcado como atendido aparece en lo enviado a facturación; uno ausente, no. |

## Fragmentos que NO son requerimientos funcionales

| Fragmento | Texto | Categoría | Justificación |
|-----------|-------|-----------|----------------|
| F4 | «Que el sistema sea rápido.» | RNF | No tiene métrica: no se responde con sí o no. |
| F5 | «Lo anotamos en el Google Calendar.» | Restricción técnica | Nombra una herramienta; describe cómo se hace hoy, no qué debe hacer el sistema. |

## Conflictos u observaciones detectadas

- [NEEDS CLARIFICATION: en Agenda 2026.xlsx, «OK» puede significar
  Confirmado o Atendido (F6). Afecta a RF-04 y RF-05. Decide la recepción.]
- [NEEDS CLARIFICATION: «reprogramado» (F6): ¿el turno vuelve a Solicitado
  o se cancela y se crea otro? Decide la recepción.]
