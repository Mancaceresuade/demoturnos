# demoturnos

Repositorio de demostración de SI2 · Viernes Mañana. Especifica el sistema de
**gestión de turnos de un consultorio**, el mismo ejemplo de las clases 9 a 12.
Clave del proyecto en Jira: **G00** (grupo de ejemplo).

## Relevamiento

Estos son los fragmentos que citan los archivos de `specs/`.

| ID | Quién | Fragmento |
|----|-------|-----------|
| F1 | Recepción | «El paciente pide turno por teléfono o por la web. Si hay lugar, lo confirmamos; si no, le ofrecemos otra fecha.» |
| F2 | Recepción | «Puede cancelar hasta 24 horas antes.» |
| F3 | Recepción | «El día del turno anotamos si vino. Si se atendió, la consulta pasa a facturación.» |
| F4 | Director | «Que el sistema sea rápido.» |
| F5 | Recepción | «Lo anotamos en el Google Calendar.» |
| F6 | Agenda 2026.xlsx | La columna Estado tiene, además de los estados del turno, los valores «OK» y «reprogramado». |

## Issues en Jira

| Issue | Qué es |
|-------|--------|
| G00-1 | Estructura del repositorio |
| G00-2 a G00-6 | RF-01 a RF-05 (`specs/requirements.md`) |
| G00-7 | UC-01 Solicitar turno (`specs/use-cases.md`) |
| G00-8 | Página generada para la E3 (rama `e3-pagina`) |
