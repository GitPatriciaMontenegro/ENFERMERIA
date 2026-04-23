# Manejo de doble registro de paciente que bloquea dispensacion de medicacion

> **Estado: ✅ APROBADO — 23 abr 2026. Vigente para horario laboral. Pendientes institucionales documentados abajo.**

**Area:** Enfermeria general (transversal a todos los servicios) + interfaz con Farmacia, Gestorias y Sistemas
**Fecha de origen:** 21 abr 2026
**Documentado por:** Patricia Lorena Montenegro
**Aprobado por:** Lotty Paniagua (RRHH + vision clinica) — 23 abr 2026
**Origen:** Turno tarde del lun 20 abr 2026 — 4to Piso C Internacion. Paciente con doble registro en sistema → Farmacia no podia dispensar medicacion. Escalado a Gestoria (1er nivel segun mensaje del sistema), no se resolvio; escalado luego a Sistemas, quien resolvio a las 20:30 (~1 hora despues del escalamiento). Ver `turno-2026-04-20-tarde.md`.

---

## Que es

Regla que define el flujo de deteccion, comunicacion, escalamiento, seguimiento y handoff cuando Farmacia no puede dispensar medicacion a un paciente por tener doble registro en el sistema.

## Cuando aplica

- Cualquier paciente internado con doble registro detectado en el sistema.
- En cualquier turno. La regla aplica especialmente cerca del pase de turno, donde el handoff es critico.

---

## Flujo (paso a paso)

### 1. Deteccion

| Quien | Que hace |
|-------|----------|
| **Farmacia** | Al intentar dispensar, detecta la duplicidad. Es el primer punto de deteccion. |
| **Farmacia** | Comunica a Enfermeria **via telefonica** al piso donde esta internado el paciente. |

### 2. Clasificacion de urgencia clinica

**Antes de seguir el flujo de escalamiento**, la enfermera clasifica el caso:

| Categoria | Criterio | Accion |
|-----------|----------|--------|
| **URGENTE** | Medicacion critica pendiente (antibioticos IV, analgesia programada, medicacion de soporte vital, etc.) | 1. Llamar simultaneamente a Gestoria Y a Sistemas — no esperar a que Gestoria falle primero. 2. Solicitar a Farmacia liberacion excepcional de solo la medicacion necesaria para las horas criticas mientras Sistemas resuelve. 3. Si no hay resolucion en 1 hora, avisar a supervisora de turno + medico tratante. |
| **NO URGENTE** | No hay medicacion de administracion inmediata pendiente | Flujo estandar: escalar segun paso 3. Se puede esperar al SLA. |

> **Caso 20 abr:** clasificado NO URGENTE — no habia medicacion de administracion urgente. Por eso el handoff al turno noche no genero impacto clinico.

### 3. Escalamiento (flujo estandar — casos NO URGENTES)

| Nivel | A quien | Cuando |
|-------|---------|--------|
| 1er nivel | **Gestoria** | Primer contacto, segun el mensaje que aparece en el sistema al detectar el doble registro. |
| 2do nivel | **Sistemas** | Si Gestoria no resuelve en 30 minutos, escalar directamente a Sistemas sin esperar mas. No insistir con Gestoria. |

> **Nota documentada del caso real (20 abr):** Gestoria no pudo resolver el doble registro — es un problema tecnico, no administrativo. Sistemas es el resolvedor efectivo. Si Gestoria no resuelve rapido, ir a Sistemas sin demora.

### 4. SLA vigente

| Franja | Tiempo maximo de resolucion | Estado |
|--------|-----------------------------|--------|
| Horario laboral (07:30–19:30) | 1 hora desde escalamiento a Sistemas | ✅ Confirmado por caso real 20 abr |
| Fuera de horario laboral | **A definir con Sistemas** — ver pendientes | ⚠️ PENDIENTE INSTITUCIONAL |

### 5. Mitigacion con Farmacia (casos URGENTES)

Farmacia puede liberar solo la medicacion necesaria para la hora/s criticas mientras Sistemas resuelve el doble registro completo.

> **Validado verbalmente el 20 abr por Farmacia.** Pendiente de formalizar el procedimiento — ver pendientes institucionales.

- La enfermera solicita la liberacion explicando que el caso es URGENTE y que Sistemas esta trabajando en la resolucion.
- Farmacia libera y registra internamente.
- Una vez resuelto el doble registro, Farmacia concilia.

### 6. Handoff al turno siguiente (si no se resolvio antes del pase)

La enfermera saliente deja registrado en el pase de turno:

| Dato | Que incluir |
|------|-------------|
| Paciente y sector | Nombre, cama, piso |
| Hora de deteccion | HH:MM |
| Hora de escalamiento | A Gestoria HH:MM / A Sistemas HH:MM |
| Con quien se hablo | Nombre de la persona contactada en cada area |
| Estado al cierre del turno | Abierto / En proceso / Resuelto |
| Clasificacion | Urgente / No urgente |
| Medicacion pendiente | Medicacion, dosis, horario programado |

> **Este registro es obligatorio.** Protege a la enfermera saliente y al paciente. Sin el, el turno entrante no tiene informacion para continuar la gestion.

### 7. Coordinacion con Farmacia al cierre

- Farmacia mantiene el caso abierto hasta confirmacion de resolucion por Sistemas.
- Una vez resuelto: Farmacia dispensa y avisa a Enfermeria por telefono.
- Enfermeria confirma recepcion y administra segun protocolo estandar.

---

## Excepciones y casos especiales

| Situacion | Accion |
|-----------|--------|
| Fuera de horario laboral, caso NO URGENTE | Documentar en pase de turno. Escalar al inicio del horario laboral del dia siguiente. |
| Fuera de horario laboral, caso URGENTE | Escalar directo a Sistemas (guardia). Si no hay resolucion: supervisora de turno + medico tratante para plan alternativo (farmacia externa, posponer segun criterio clinico). |
| Sistemas no responde en tiempo | Supervisora de turno + medico tratante. No dejar la decision en la enfermera sola. |

---

## Quien lo sabe mejor si hay dudas

- **Patricia Lorena Montenegro** (Coordinadora de enfermeria)
- **Supervisora de turno**
- **Jefe de Farmacia** — flujo del lado de farmacia y liberacion excepcional
- **Jefe de Sistemas** — SLA y canal de escalamiento fuera de horario

---

## Pendientes institucionales — no bloquean el uso de esta regla, pero deben resolverse

| # | Pendiente | Quien resuelve | Urgencia |
|---|-----------|---------------|---------|
| P1 | Confirmar SLA de 1 hora con Sistemas (horario laboral) | Jefe de Sistemas + Lotty | Alta |
| P2 | Definir SLA fuera de horario laboral + canal de contacto a Sistemas en guardia | Jefe de Sistemas + Lotty | Alta — hay turnos noche todos los dias |
| P3 | **Formalizar con Farmacia el procedimiento de liberacion excepcional:** quien autoriza, como se registra, como se concilia despues | Jefe de Farmacia + Lotty | Alta — es la valvula de seguridad para casos urgentes |
| P4 | Aclarar en el flujo que Gestoria generalmente NO resuelve doble registros tecnicos — Sistemas es el resolvedor efectivo. Verificar si el 1er nivel debe cambiarse directamente a Sistemas. | Patricia + Lotty + Gestoria | Media |
| P5 | Incorporar campo especifico en el reporte de enfermeria para trazabilidad de doble registro | Sistemas + Patricia | Media |

---

## Revision de calidad — 23 abr 2026

**Revisado por:** Lotty Paniagua (RRHH + vision clinica)
**Veredicto:** ✅ APROBADO para uso inmediato en horario laboral

| Aspecto | Resultado |
|---------|-----------|
| Seguridad del paciente | ✅ Cubierta — clasificacion URGENTE/NO URGENTE + mitigacion Farmacia |
| Trazabilidad y proteccion de la enfermera | ✅ Cubierta — plantilla de handoff obligatoria |
| Claridad del flujo de escalamiento | ✅ Mejorado — se aclara que Sistemas es el resolvedor efectivo, no Gestoria |
| SLA horario laboral | ✅ Confirmado por caso real — 1 hora |
| SLA fuera de horario laboral | ⚠️ Pendiente institucional — no bloquea uso |
| Liberacion excepcional Farmacia | ⚠️ Pendiente de formalizar — mecanismo existe pero no tiene procedimiento escrito |

---

*Aprobado: 23 abr 2026. Lotty Paniagua + Patricia Montenegro + Claude.*
*Pendientes institucionales (P1–P5) a resolver con Sistemas y Farmacia.*
