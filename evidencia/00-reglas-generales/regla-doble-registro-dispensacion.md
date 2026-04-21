# Manejo de doble registro de paciente que bloquea dispensacion de medicacion

> **Estado: BORRADOR — pendiente de revision y validacion por Lotty Paniagua + confirmacion de SLA con areas de Gestorias y Sistemas.**

**Area:** Enfermeria general (transversal a todos los servicios) + interfaz con Farmacia, Gestorias y Sistemas
**Fecha:** 21 abr 2026
**Documentado por:** Patricia Lorena Montenegro
**Origen:** Turno tarde del lun 20 abr 2026 — 4to Piso C Internacion. Paciente con doble registro en sistema → Farmacia no podia dispensar medicacion. Escalado a Gestoria (1er nivel segun mensaje del sistema), no se resolvio; escalado luego a Sistemas, quien resolvio a las 20:30 (~1 hora despues del escalamiento). Ver `turno-2026-04-20-tarde.md`.

---

## Que es

Regla que define el flujo de deteccion, comunicacion, escalamiento, seguimiento y handoff cuando Farmacia no puede dispensar medicacion a un paciente por tener doble registro en el sistema.

## Cuando aplica

- Cualquier paciente internado con doble registro detectado en el sistema.
- En cualquier turno. La regla aplica especialmente cerca del pase de turno, donde el handoff es critico.

## Flujo (paso a paso)

### 1. Deteccion

| Quien | Que hace |
|-------|----------|
| **Farmacia** | Al intentar dispensar, detecta la duplicidad. Es el primer punto de deteccion. |
| **Farmacia** | Comunica a Enfermeria **via telefonica** al piso donde esta internado el paciente. |

### 2. Escalamiento

| Nivel | A quien | Cuando |
|-------|---------|--------|
| 1er nivel | **Gestoria** | Primer contacto, segun el mensaje que aparece en el sistema al detectar el doble registro. |
| 2do nivel | **Sistemas** | Si Gestoria no puede resolver a nivel de registro, se escala a Sistemas para correccion tecnica. |

> **Observacion real (20 abr):** el escalamiento a Gestoria no resolvio; Sistemas resolvio en ~1 hora desde que tomo el caso.

### 3. SLA propuesto (a confirmar con Gestorias y Sistemas)

| Franja | Tiempo maximo de resolucion |
|--------|------------------------------|
| Horario laboral (07:30 - 19:30) | 1 hora desde escalamiento |
| Fuera de horario laboral | A definir |

> Dato real observado: 1 hora (20 abr, caso escalado alrededor de 19:30, resuelto 20:30).

### 4. Clasificacion de urgencia clinica

**Antes de seguir el flujo estandar**, la enfermera clasifica el caso:

| Categoria | Criterio | Accion |
|-----------|----------|--------|
| **URGENTE** | Medicacion critica pendiente (antibioticos IV, analgesia programada, medicacion de soporte vital, etc.) | 1. Escalamiento reforzado: llamar directamente a Sistemas ademas de Gestoria. 2. **Mitigacion con Farmacia** — solicitar liberacion excepcional de solo la medicacion necesaria para la hora/s criticas, mientras Sistemas resuelve el doble registro completo. 3. Si no hay resolucion en la siguiente hora, avisar a supervisora. |
| **NO URGENTE** | No hay medicacion de administracion inmediata pendiente | Flujo estandar. Se puede esperar al SLA. |

> **Caso 20 abr:** clasificado NO URGENTE — no habia medicacion de administracion urgente. Por eso el handoff al turno noche no genero impacto clinico.
> **Mitigacion confirmada por Farmacia (20 abr):** si el caso hubiera sido urgente, Farmacia podia liberar solo la medicacion necesaria para esa hora mientras Sistemas corregia el doble registro. Es la valvula de escape operativa para evitar impacto clinico cuando el SLA no se cumple a tiempo.

### 5. Handoff al turno siguiente (si no se resolvio)

La enfermera saliente deja registrado en el pase de turno:

| Dato | Ejemplo |
|------|---------|
| Paciente y sector | "Paciente X, cama 4to C habitacion N" |
| Hora de deteccion | |
| Hora de escalamiento | |
| Con quien se hablo | "Gestoria (nombre) a las HH:MM; Sistemas (nombre) a las HH:MM" |
| Estado actual | "Abierto / En proceso / Resuelto" |
| Clasificacion | "Urgente / No urgente" |
| Medicacion pendiente | "Medicacion X programada para las HH:MM" |

### 6. Coordinacion con Farmacia

- Farmacia mantiene el caso abierto hasta que Sistemas confirme la resolucion.
- Una vez resuelto, Farmacia dispensa y comunica a Enfermeria (misma via telefonica).
- Enfermeria confirma recepcion y procede con la administracion segun protocolo.

## Excepciones y casos especiales

- **Fuera de horario laboral:** hasta definir SLA con Sistemas, la enfermera de turno deja el caso documentado en pase de turno y escala por segunda vez al inicio del siguiente horario laboral.
- **Paciente con medicacion critica y sin resolucion:** escalamiento a supervisora de turno + medico tratante para decidir plan alternativo (coordinar con farmacia externa, posponer indicacion medica segun criterio clinico, etc.).

## Quien lo sabe mejor si hay dudas

- **Patricia Lorena Montenegro** (Coordinadora de enfermeria)
- **Supervisora de turno**
- **Jefe de Farmacia** — para confirmar flujo del lado de farmacia
- **Jefe de Sistemas** — para confirmar SLA y canal de escalamiento

## Pendientes para cerrar esta regla

- [ ] Confirmar SLA con Sistemas (1 hora en horario laboral es viable?)
- [ ] Definir SLA fuera de horario laboral
- [ ] Validar con Jefe de Farmacia el flujo de comunicacion (telefonica) y si hay canal adicional
- [ ] **Formalizar con Farmacia el procedimiento de liberacion excepcional de medicacion por hora** cuando el caso sea urgente y el doble registro no se resuelva a tiempo (quien autoriza, como se registra, como se concilia despues)
- [ ] Incorporar al reporte de enfermeria un campo especifico para trazabilidad de doble registro

---

*Borrador 21 abr 2026. Patricia Montenegro. Pendiente de revision por Lotty Paniagua + confirmacion de SLA con Gestorias y Sistemas.*
