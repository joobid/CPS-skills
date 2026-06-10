# Metodología 8D para Implementación Estructurada

## Origen y propósito

La metodología 8D (8 Disciplines) fue desarrollada por Ford Motor Company. Es un enfoque
estructurado para resolver problemas técnicos y organizacionales, diseñado para ser exhaustivo
y prevenir la recurrencia.

Se usa cuando el problema requiere un plan de implementación formal con trazabilidad.

---

## Las 8 disciplinas

### D1 — Formar el equipo

- Seleccionar personas con conocimiento del proceso, producto o sistema afectado
- El equipo debe incluir representantes de las áreas clave (no solo los "sospechosos habituales")
- Asignar un líder de equipo con autoridad para tomar decisiones
- Establecer roles y responsabilidades claras
- Incluir un "outsider" que aporte perspectiva fresca (Principio de Epstein: los generalistas
  ven lo que los especialistas no)

### D2 — Describir el problema

Usar las herramientas de la Fase 1 del CPS:
- Reductor de Complejidad (Nardone/Recuenco): ¿Qué, quién, dónde, cuándo, cómo?
- IS/IS NOT (Kepner-Tregoe): Delimitar con precisión
- Soluciones Intentadas Redundantes: ¿Qué se ha intentado y por qué no ha funcionado?

La descripción debe ser:
- Observable (comportamientos, no interpretaciones)
- Cuantificable cuando sea posible
- Verificable por cualquiera

### D3 — Implementar contención temporal

Si el problema está causando daño activo, implementar medidas de contención ANTES de buscar
la causa raíz. La contención no resuelve el problema; lo contiene mientras se investiga.

- ¿Qué podemos hacer AHORA para limitar el daño?
- ¿La contención tiene efectos secundarios?
- ¿Cómo verificamos que la contención funciona?

Nota: La contención es como aplicar un torniquete. Necesaria en emergencia, pero no es la cura.

### D4 — Identificar la causa raíz

Aplicar las herramientas de la Fase 2 del CPS:
- 5 Porqués
- Diagrama de Ishikawa
- Árboles Lógicos
- Puntos de Apalancamiento

Requisito clave: la causa raíz propuesta debe ser VERIFICABLE. Si no puedes demostrar que
al eliminar la causa el problema desaparece, no has encontrado la causa raíz.

**Prueba ácida:** Si reintroduzco la causa propuesta, ¿reaparece el problema?

### D5 — Definir acciones correctivas permanentes

A partir de la causa raíz verificada:
- ¿Qué acción elimina la causa raíz (no solo el síntoma)?
- ¿La acción es implementable con los recursos disponibles?
- ¿Tiene efectos secundarios aceptables?
- ¿Puede medirse su efectividad?

Cada acción correctiva debe tener:
- Descripción clara de la acción
- Responsable (nombre, no departamento)
- Fecha de implementación
- Criterio de éxito verificable

### D6 — Implementar y validar

- Ejecutar las acciones correctivas según plan
- Retirar las medidas de contención temporal (D3) una vez que las correctivas estén operativas
- Monitorizar durante un período definido para verificar eficacia
- Recopilar datos que confirmen que el problema se ha resuelto

### D7 — Prevenir recurrencia

Esta disciplina distingue al 8D de otros métodos. No basta con resolver el problema;
hay que asegurarse de que no vuelva a ocurrir:

- ¿Qué cambios sistémicos previenen la recurrencia?
- ¿Hay otros procesos/sistemas donde pueda ocurrir el mismo problema?
- ¿Qué procedimientos, estándares o controles hay que actualizar?
- ¿Qué formación se necesita?
- ¿Cómo se transfiere este aprendizaje a la organización?

Conectar con los Puntos de Apalancamiento de Meadows: las acciones de nivel alto
(cambio de reglas, flujos de información) son más efectivas para prevenir recurrencia
que las de nivel bajo (ajustar parámetros).

### D8 — Reconocer al equipo

- Celebrar el trabajo realizado
- Documentar el aprendizaje
- Compartir los hallazgos con la organización
- Reconocer las contribuciones individuales y colectivas

Parece trivial, pero es importante: refuerza la cultura de resolución de problemas y
motiva la participación en futuros esfuerzos.

---

## Cuándo usar 8D en el proceso CPS

La metodología 8D encaja mejor cuando:
- El problema es técnico o de proceso (Dominio Complicado en Cynefin)
- Se necesita trazabilidad formal (regulación, auditoría, compliance)
- El problema ya se ha diagnosticado (Fases 1-5 completadas) y se necesita implementar
- Hay un equipo asignado con responsabilidad clara

No es ideal cuando:
- El problema está en el Dominio Complejo (requiere experimentación, no plan formal)
- El problema es fundamentalmente político o cultural
- No hay claridad sobre la causa raíz (volver a Fases 1-3)

---

## Plantilla 8D resumida

```
INFORME 8D
Fecha: ___
Líder: ___

D1 — Equipo: [nombres y roles]
D2 — Descripción del problema: [qué, quién, dónde, cuándo, magnitud]
D3 — Contención temporal: [acción inmediata] → [verificación]
D4 — Causa raíz: [causa verificada] → [evidencia]
D5 — Acciones correctivas:
  - Acción 1: [qué] → [quién] → [cuándo] → [criterio de éxito]
  - Acción 2: ...
D6 — Validación: [datos de monitorización] → [eficacia confirmada sí/no]
D7 — Prevención: [cambios sistémicos implementados]
D8 — Cierre: [lecciones aprendidas, reconocimiento]
```
