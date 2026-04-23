# Decisiones Pendientes

> Decisiones que necesitan aprobacion de Pedro via commit o issue.

## Preguntas pendientes para Patricia — revisadas con Lotty (15 abr 2026)

Estas preguntas surgieron de la revision de calidad del 15 abr. Patricia debe responderlas e incorporar las respuestas en los documentos correspondientes.

| # | Pregunta | Documento | Quien responde | Estado |
|---|----------|-----------|----------------|--------|
| P1 | Despues de administrar el medicamento, la enfermera lo registra en el sistema de la clinica? Si es asi, como se hace y en que momento exactamente? | `administracion-medicamentos.md` | Patricia (Lorena) | CERRADA — 17 abr 2026 |
| P2 | Existe un rol semanal o diario escrito (papel, excel, pizarron, sistema) que dice quien trabaja en que piso cada dia? Como se comunica a las enfermeras? Con cuanta anticipacion lo saben? | `dotacion-turnos-cobertura.md` | Patricia (Lorena) | CERRADA — 17 abr 2026 |

### Respuestas (17 abr 2026 — Patricia)

- **P1:** El registro queda al realizar el matcheo entre el medicamento y la manilla identificatoria del paciente (paso 14 de Etapa 5). No hay paso manual adicional posterior. Incorporado en `evidencia/00-reglas-generales/administracion-medicamentos.md`.
- **P2:** No existe rol escrito. El conocimiento vive en las lideres de equipo y supervisoras; no se comunica al equipo con anticipacion formal. Incorporado en `evidencia/00-reglas-generales/dotacion-turnos-cobertura.md` (nueva seccion + Riesgo 5).

---

## Decisiones Abiertas

| # | Que | Quien | Cuando | Que pasa si no | Estado |
|---|-----|-------|--------|----------------|--------|
| A1 | Trabajar con Lotty el diseno operativo de los Espacios de Contencion (Categoria 3) | Patricia + Lotty | Por agendar | Categoria 3 queda resuelta en papel pero sin mecanismo operativo | ABIERTA — 17 abr 2026 |
| A2 | Cerrar las 2 personas faltantes del Grupo 1 (documentadas 6 de ~8) | Patricia + Lorena | Lun 20 abr si hay oportunidad | Queda incompleto el lote y se acumula para Grupo 2 | ABIERTA — 17 abr 2026 |
| A3 | Arrancar documentacion del Grupo 2 Internacion (~8 personas) | Patricia + Lorena | Lun 20 abr 2026 | Se rompe el ritmo y se compromete la meta de 50 al 1 may | ✅ COMPLETADO 20 abr — 6 personas documentadas (4to Piso C), acumulado 12/50 |
| A4 | Formalizar reglas faltantes: (a) "que hacer cuando el paciente posterga la toma de medicacion" [17 abr]; (b) "que hacer con doble registro de paciente que bloquea dispensacion de medicacion" [20 abr — resuelto ~1h despues del escalamiento, a las 20:30] | Patricia (propone) + Lotty (revisa) | Proponer en la proxima sesion con Lotty | Se repiten los hallazgos y queda sin trazabilidad al handoff entre turnos | ABIERTA — ampliada 20 abr 2026 |
| A5 | Agregar a Pedro Escobar como colaborador del repo ENFERMERIA (GitHub) | Patricia | Cuando Pedro pase su usuario de GitHub | Pedro no tiene visibilidad directa del repo de evidencia | ABIERTA — 17 abr 2026 |
| A6 | Incluir en el manual de procedimientos de enfermeria (actualmente en actualizacion) la seccion de baño del paciente: horarios, justificacion del turno mañana, criterios ante rechazo | Patricia + equipo que actualiza el manual | En el marco de la actualizacion en curso | Se mantiene como cultura no escrita y genera vacios como el del 21 abr | ABIERTA — 21 abr 2026 |
| A7 | Seguimiento al refuerzo aplicado con personal 3er B sobre registro en expediente de todas las actividades (regla existente) | Patricia + Lorena | Proximos turnos | Si el refuerzo no tiene efecto, escalar con Maria Elena para accion mas firme | ABIERTA — 21 abr 2026 — **señal preliminar 22 abr:** grupo tarde del 3er B cumple la regla (Actividad 2 registrada). Problema parece del grupo mañana, no transversal al piso. Pendiente medir al grupo reforzado en proxima oportunidad. |

### Observaciones abiertas para la proxima sesion con Lotty

- **Riesgo 2 de medicamentos confirmado en vivo** (turno 17 abr): medicacion dejada en habitacion sin supervisar toma. Ya no es hipotesis. No se repitio el 20 abr.
- **Pase de turno con 2 desvios chicos** el 17 abr: (a) personal incompleto al iniciar, (b) auxiliar sin registro fisico a la mano. **El 20 abr el pase se hizo conforme — sirve como caso ejemplar.**
- **Nuevo hallazgo bioseguridad (20 abr):** auxiliar realiza control de glucemia sin guantes + descarte fuera de habitacion, en 2 oportunidades. Observacion aplicada al cierre. Requiere refuerzo de protocolo y verificar disponibilidad de guantes en el piso.
- **Patron rol auxiliar:** 17 abr (sin registro) y 20 abr (bioseguridad glucemia) — 2 desvios consecutivos del mismo rol. Validar con Maria Elena si hay brecha de capacitacion/supervision.
- **Incidencia abierta al 20 abr:** doble registro de paciente bloqueando dispensacion. ✅ **RESUELTO el 20 abr a las 20:30** por Sistemas (~1 hora desde el escalamiento). Medicacion dispensada OK.
- **Hallazgo 21 abr — incumplimiento de regla existente:** registro en expediente clinico NO se realizo en 2 instancias del 3er B (rechazo de baño + actividades del pase). Se reforzo con el personal del 3er B en el turno. Verificar efecto en proximos turnos (A7).
- **Oportunidad 21 abr — actualizacion del manual de procedimientos:** incluir baño del paciente (horarios + justificacion turno mañana + criterios ante rechazo) en el manual que el equipo esta actualizando (A6).

## Decisiones Cerradas

| # | Decision | Quien | Fecha | Resultado |
|---|----------|-------|-------|-----------|
| C1 | Enfermeria es area piloto, Lorena es referente | Lotty | 2 abr 2026 | APROBADO |
| C2 | Crear repo ENFERMERIA en GitHub + acceso Patricia | Pedro | 3 abr 2026 | COMPLETADO |
| C3 | Enfermeria confirmada como caso piloto para reglas | Lotty | 2 abr 2026 | APROBADO |
| C4 | Que documenta Lorena: TODO (procesos, reglas, excepciones) | Lotty + Lorena | 6 abr 2026 | DEFINIDO |
| C5 | Formato: PLANTILLA-TURNO.md, frecuencia: al final de cada turno | Patricia + Lotty | 6 abr 2026 | DEFINIDO |
| C6 | Categoria 3 (problemas personales/emocionales): derivar a Espacios de Contencion, psicologas emiten informe a RRHH + Lorena/Maria Elena | Lotty | 15 abr 2026 | RESUELTO |
