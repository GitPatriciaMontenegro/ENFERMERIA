# Administracion de Medicamentos

**Area:** Enfermeria general (transversal a todos los servicios)
**Fecha:** 8 abr 2026
**Documentado por:** Patricia Lorena Montenegro
**Fuente:** Conocimiento institucional de enfermeria — Clinica Foianini

---

## Que es

Proceso completo de medicacion al paciente hospitalizado: desde que el medico genera la indicacion en el sistema hasta que la enfermera administra el medicamento al paciente en su habitacion. Incluye validacion por farmacia, programacion de horarios, preparacion y administracion.

## Cuando aplica

- Cada vez que existe una indicacion medica para un paciente internado
- Aplica las 24 horas, todos los dias
- Excepcion: eventos inesperados (ej: fiebre) tienen cumplimiento inmediato, no esperan programacion estandar

## Como se hace (paso a paso)

### Etapa 1 — Indicacion medica

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 1 | Medico genera indicacion en el sistema (expediente clinico institucional) | Medico hospitalista o residente | Sistema/Software |
| 2 | Hospitalista valida la indicacion | Medico hospitalista | Sistema |

### Etapa 2 — Programacion y validacion

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 3 | Enfermera visualiza la indicacion en el sistema | Enfermera de turno | Estacion de enfermeria |
| 4 | Enfermera programa horarios segun estandares del sistema | Enfermera de turno | Sistema |
| 5 | Programacion va a Farmacia para validacion (verifican que no haya interaccion entre medicamentos) | Farmacia | Farmacia |
| 6 | Farmacia prepara medicacion para 24 horas de tratamiento del paciente | Farmacia | Farmacia |

### Etapa 3 — Recepcion y almacenamiento

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 7 | Enfermera recoge medicamentos del area de farmacia | Enfermera de turno | Farmacia |
| 8 | Sube medicamentos al area de enfermeria del piso/servicio | Enfermera de turno | Piso correspondiente |
| 9 | Si hay medicacion de uso controlado: se guarda bajo llave en area restringida | Enfermera de turno | Area restringida de enfermeria |

### Etapa 4 — Preparacion

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 10 | Toma la medicacion del taper asignado al paciente | Enfermera de turno | Estacion de enfermeria |
| 11 | Verifica en formulario fisico: dosis y via de administracion (la hora la da el sistema) | Enfermera de turno | Estacion de enfermeria |
| 12 | Prepara la medicacion | Enfermera de turno | Area de preparacion de enfermeria |

### Etapa 5 — Administracion

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 13 | Ingresa a la habitacion con el carro de medicacion preparada | Enfermera de turno | Habitacion del paciente |
| 14 | Realiza check con la manilla identificatoria del paciente (matcheo paciente-medicamento) — **el matcheo deja el registro en el sistema** | Enfermera de turno | Junto al paciente |
| 15 | Verifica: paciente correcto, medicamento correcto | Enfermera de turno | Junto al paciente |
| 16 | Administra el medicamento | Enfermera de turno | Junto al paciente |

### Registro en el sistema

- El registro de la administracion **queda automaticamente** al momento del matcheo entre el medicamento y la manilla identificatoria del paciente (paso 14).
- No hay un paso manual adicional posterior a la administracion: el matcheo ES el registro.
- Implicacion: si no se hace el matcheo de manilla, **no queda registro de la administracion** — ver Riesgo 2.

### Etapa 6 — Efectos adversos

| Paso | Que pasa | Quien | Donde |
|------|----------|-------|-------|
| 17 | Si la enfermera nota alguna reaccion adversa en el paciente | Enfermera de turno | Habitacion del paciente |
| 18 | Comunica inmediatamente al medico hospitalista o residente | Enfermera de turno | Comunicacion directa |
| 19 | Mientras espera indicacion medica: monitorea al paciente, habla con el para evaluar estado | Enfermera de turno | Junto al paciente |
| 20 | Segun necesidad: puede colocar oxigeno u otras medidas de soporte inmediato | Enfermera de turno | Junto al paciente |
| 21 | Medico indica tratamiento para los efectos adversos | Medico | Indicacion directa o sistema |

## Excepciones y casos especiales

- **Evento inesperado (fiebre, etc.):** La indicacion y cumplimiento es inmediato — no espera programacion estandar de horarios
- **Medicacion controlada:** Se almacena en area restringida bajo llave, no en el taper general del paciente

## Riesgos identificados

| # | Riesgo | Descripcion | Gravedad |
|---|--------|-------------|----------|
| 1 | **No hay verificacion de dosis al momento de administrar** | La medicacion ya fue preparada y la guia esta en formulario fisico transcrito por la enfermera. No hay doble verificacion digital al lado del paciente | ALTO |
| 2 | **Administracion sin matcheo de manilla** | Se ha detectado que algunas enfermeras preparan y administran directamente sin verificar la manilla identificatoria del paciente | ALTO |

## Quien lo sabe mejor si hay dudas

- Patricia Lorena Montenegro (Coordinadora de enfermeria)
- Enfermeras con mayor antiguedad en el servicio

---

*Documentado en sesion de arranque con Claude — 8 abr 2026*
*Primer documento del piloto de documentacion institucional de enfermeria*
