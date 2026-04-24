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
| A2 | Cerrar las 2 personas faltantes del Grupo 1 (documentadas 6 de ~8) | Patricia + Lorena | Lun 20 abr si hay oportunidad | Queda incompleto el lote y se acumula para Grupo 2 | ✅ CUMPLIDA Y SUPERADA — 24 abr. Pase noche→mañana 5to C sumo 4 personas nuevas (Vargas, Ruiz, Hurtado, Villarrubia). Acumulado 28/50. |
| A3 | Arrancar documentacion del Grupo 2 Internacion (~8 personas) | Patricia + Lorena | Lun 20 abr 2026 | Se rompe el ritmo y se compromete la meta de 50 al 1 may | ✅ COMPLETADO 20 abr — 6 personas documentadas (4to Piso C), acumulado 12/50 |
| A4 | Formalizar reglas faltantes: (a) postergacion toma medicacion; (b) doble registro bloquea dispensacion | Patricia (propone) + Lotty (revisa) | 23 abr | ✅ APROBADAS 23 abr — Lotty (RRHH + vision clinica). Ver pendientes institucionales P1–P5 en regla-doble-registro-dispensacion.md |
| A5 | Agregar a Pedro Escobar (`VITALIASALUD`) como colaborador del repo ENFERMERIA | Patricia | Lo antes posible | Pedro no tiene visibilidad directa del repo de evidencia | ⏳ Instrucciones recibidas 23 abr — Patricia debe agregar a `VITALIASALUD` en Settings → Collaborators |
| A6 | Incluir en el manual de procedimientos de enfermeria (actualmente en actualizacion) la seccion de baño del paciente: horarios, justificacion del turno mañana, criterios ante rechazo | Patricia + equipo que actualiza el manual | En el marco de la actualizacion en curso | Se mantiene como cultura no escrita y genera vacios como el del 21 abr | ABIERTA — 21 abr 2026 |
| A7 | Seguimiento al refuerzo aplicado con personal 3er B sobre registro en expediente de todas las actividades (regla existente) | Patricia + Lorena | Proximos turnos | Si el refuerzo no tiene efecto, escalar con Maria Elena para accion mas firme | ABIERTA — 21 abr 2026 — **señal preliminar 22 abr:** grupo tarde del 3er B cumple la regla (Actividad 2 registrada). Problema parece del grupo mañana, no transversal al piso. Pendiente medir al grupo reforzado en proxima oportunidad. |
| A8 | Agendar reunion con Calidad — avances de acreditacion. **Participantes:** Maria Elena del Granado (Gerencia Enfermeria), Patricia Montenegro (Coordinacion), Zuleidy [apellido por confirmar], Julia [apellido por confirmar] (Calidad). | Patricia (agenda) + Julia/Calidad (confirma) | **Lun 27 abr 2026 — 14:00 hrs.** Invitacion enviada hoy vie 24 abr en el bloque de seguimiento con Julia. | Sin avance agendado se acumulan temas de acreditacion sin revision (ITAES + malla de reportes + otros). Riesgo de perder hitos cercanos. | ABIERTA — 24 abr 2026 |
| A9 | Seguimiento a Calidad (Julia) — respuesta a observaciones sobre malla de reportes de eventos de enfermeria. **Correo original:** vie 17 abr. **Reenviado hoy:** vie 24 abr. | Patricia (enviado) + Julia (debe responder) | Si no hay respuesta al lun 27 abr 14:00 (reunion A8), retomar el tema en esa reunion con los 4 participantes presentes. | Sin respuesta formal el tema queda ambiguo y se acumulan observaciones sin cierre (pain point de seguimiento externo). | ⏳ ESPERA LUN 27 — 24 abr 2026: Julia confirmo recepcion del correo. Respuesta formal se dara durante la reunion A8 del lun 27 abr 14:00. |

### Observaciones abiertas para la proxima sesion con Lotty

- **Riesgo 2 de medicamentos confirmado en vivo** (turno 17 abr): medicacion dejada en habitacion sin supervisar toma. Ya no es hipotesis. No se repitio el 20 abr.
- **Pase de turno con 2 desvios chicos** el 17 abr: (a) personal incompleto al iniciar, (b) auxiliar sin registro fisico a la mano. **El 20 abr el pase se hizo conforme — sirve como caso ejemplar.**
- **Nuevo hallazgo bioseguridad (20 abr):** auxiliar realiza control de glucemia sin guantes + descarte fuera de habitacion, en 2 oportunidades. Observacion aplicada al cierre. Requiere refuerzo de protocolo y verificar disponibilidad de guantes en el piso.
- **Patron rol auxiliar:** 17 abr (sin registro) y 20 abr (bioseguridad glucemia) — 2 desvios consecutivos del mismo rol. Validar con Maria Elena si hay brecha de capacitacion/supervision.
- **Incidencia abierta al 20 abr:** doble registro de paciente bloqueando dispensacion. ✅ **RESUELTO el 20 abr a las 20:30** por Sistemas (~1 hora desde el escalamiento). Medicacion dispensada OK.
- **Hallazgo 21 abr — incumplimiento de regla existente:** registro en expediente clinico NO se realizo en 2 instancias del 3er B (rechazo de baño + actividades del pase). Se reforzo con el personal del 3er B en el turno. Verificar efecto en proximos turnos (A7).
- **Oportunidad 21 abr — actualizacion del manual de procedimientos:** incluir baño del paciente (horarios + justificacion turno mañana + criterios ante rechazo) en el manual que el equipo esta actualizando (A6).
- **Input de Calidad (24 abr):** el procedimiento de pase de turno asistencial ya existe en el manual desde 2016 — debe ACTUALIZARSE (no crearse uno nuevo). Es transversal, debe incluir rol supervisora/coordinadora + personal de apoyo + instrumentos actualizados. Borrador renombrado como insumo para actualizacion.
- **Buenas practicas documentadas 24 abr (5to C):** filtro ejemplar de medicacion (enfermera detecta medicacion no indicada antes de administrar) + comunicacion eficaz al residente/hospitalista (segundo caso del patron, confirma que funciona sostenido). Evidencia positiva para reportar al equipo y al manual.
- **Discrepancia detectada 24 abr:** dotacion 4to C y 5to C tarde/noche — Patricia reporta 2 enf vs doc `dotacion-turnos-cobertura.md` que dice 3 enf. Confirmar y actualizar el documento si corresponde.
- **Modalidad de observacion apoyada (24 abr):** relevamiento noche→mañana 5to C realizado por Maria Elena + Zuleidy con orientacion previa de Patricia. Modelo extensible para turnos no cubiertos presencialmente.

## Decisiones Cerradas

| # | Decision | Quien | Fecha | Resultado |
|---|----------|-------|-------|-----------|
| C1 | Enfermeria es area piloto, Lorena es referente | Lotty | 2 abr 2026 | APROBADO |
| C2 | Crear repo ENFERMERIA en GitHub + acceso Patricia | Pedro | 3 abr 2026 | COMPLETADO |
| C3 | Enfermeria confirmada como caso piloto para reglas | Lotty | 2 abr 2026 | APROBADO |
| C4 | Que documenta Lorena: TODO (procesos, reglas, excepciones) | Lotty + Lorena | 6 abr 2026 | DEFINIDO |
| C5 | Formato: PLANTILLA-TURNO.md, frecuencia: al final de cada turno | Patricia + Lotty | 6 abr 2026 | DEFINIDO |
| C6 | Categoria 3 (problemas personales/emocionales): derivar a Espacios de Contencion, psicologas emiten informe a RRHH + Lorena/Maria Elena | Lotty | 15 abr 2026 | RESUELTO |
