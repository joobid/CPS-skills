# Ejemplo Aplicado: un análisis CPS de Nivel 2 paso a paso

Este es un ejemplo completo de un **Análisis Estándar (Nivel 2)** desarrollado de principio a fin.
Sirve como calibración: muestra cómo se encadenan las herramientas y qué nivel de concreción se espera.
Es el mismo caso que el ejemplo breve de Nivel 1 de `SKILL.md`, ahora desarrollado en profundidad.

> **Caso:** *"Nuestro equipo de soporte está saturado y los tiempos de respuesta no dejan de subir.
> Ya hemos contratado gente y pedido más esfuerzo, y sigue empeorando."*

---

## 0. Clasificación del problema (Cynefin)

**Dominio: Complejo.** Hay múltiples factores que interactúan (producto, agentes, clientes,
incentivos), las relaciones causa-efecto no son evidentes a priori, y los intentos previos
("contratar más", "esforzarse más") no han producido una mejora estable. No es Simple (no hay una
mejor práctica que aplicar mecánicamente) ni puramente Complicado (no basta con análisis experto:
el sistema reacciona). → Enfoque: **Probar → Percibir → Responder**, con énfasis en diagnóstico
riguroso antes de actuar.

---

## 1. Diagnóstico

### 1.1 Definición del problema (Reductor de Complejidad)

- **QUÉ:** El tiempo medio de primera respuesta pasó de 4h a 18h en 3 meses. El backlog de tickets
  abiertos creció de ~120 a ~480.
- **QUIÉN:** 8 agentes de soporte, el lead de soporte, clientes de pago, y —ausente de la mesa— el
  equipo de producto (dueño del bug que veremos en causas).
- **DÓNDE:** Canal de tickets (no en chat en vivo, que mantiene tiempos normales).
- **CUÁNDO:** El deterioro empieza tras el lanzamiento de la versión 3.0, hace 3 meses.
- **CÓMO:** Llega un pico de tickets repetidos → los agentes los tratan uno a uno → el backlog crece →
  la presión por cerrar rápido sube → suben las reaperturas → más volumen.
- **CÓMO LO VEN OTROS:** Dirección lo lee como "falta de capacidad/productividad del equipo";
  los agentes lo viven como "nos llueven los mismos problemas y no podemos con todo".

### 1.2 Soluciones intentadas (Nardone)

| Intento | Qué pasó | Lógica subyacente |
|---------|----------|-------------------|
| Contratar 2 agentes | Alivio 2 semanas, luego igual o peor | "Es un problema de capacidad" |
| Pedir "más esfuerzo"/horas | Sin efecto, más fatiga | "Es un problema de actitud/productividad" |

**Patrón:** ambos intentos asumen que el cuello de botella es la *capacidad de atención*. Van en la
misma dirección y fracasan → señal Nardone de que la solución real está en **otra** dirección
(reducir el volumen entrante, no aumentar la capacidad de procesarlo).

---

## 2. Análisis de causas (5 Porqués + Apalancamiento)

**5 Porqués sobre el síntoma "el backlog crece":**
1. ¿Por qué crece el backlog? → Entran más tickets de los que se cierran de forma estable.
2. ¿Por qué entran tantos? → ~40% son por un mismo bug de la v3.0 (un error de sincronización).
3. ¿Por qué no se cierran de forma estable? → Muchos se reabren.
4. ¿Por qué se reabren? → Se cierran con workarounds rápidos, no se resuelve la causa del cliente.
5. ¿Por qué se prioriza cerrar rápido? → El único KPI del equipo es "tiempo de cierre".

**Causas raíz (constelación, no una sola — Recuenco):**
1. Un bug de producto genera ~40% del volumen (causa estructural externa al equipo de soporte).
2. No existe base de conocimiento → cada agente reinvestiga lo ya resuelto.
3. El incentivo premia velocidad de cierre, no resolución → reaperturas (causa que *mantiene* el
   problema, en términos de Nardone).

**Puntos de apalancamiento (Meadows):** contratar es nivel 12 (parámetro, bajo impacto). El fix del
bug y, sobre todo, **cambiar el KPI** (nivel 5, reglas/incentivos) son intervenciones de mucho mayor
apalancamiento.

---

## 3. Sesgos detectados (auditoría)

- **Anclaje + sesgo de confirmación:** el primer diagnóstico ("falta capacidad") ancló todas las
  acciones; se buscó evidencia que lo confirmara (colas largas) y se ignoró el dato del bug.
- **Coste hundido:** "ya hemos contratado, no podemos admitir que era el enfoque equivocado".
- **Métrica que engaña (sesgo de disponibilidad):** el "tiempo de cierre" es visible y fácil de medir,
  así que domina la conversación, mientras las reaperturas —menos visibles— se ignoran.

---

## 4. Opciones generadas

Aplicando **"Cómo empeorar" (Nardone)** — *¿qué haríamos para empeorarlo a propósito?*: no arreglar el
bug, premiar solo el cierre rápido, no documentar nada, añadir gente sin contexto. **Invertir** cada
punto da la lista de soluciones:

- **A.** Priorizar con producto el fix del bug que genera el 40% del volumen.
- **B.** Cambiar el KPI: medir reaperturas / resolución a la primera, no solo velocidad de cierre.
- **C.** Crear una base de conocimiento mínima con las 10 incidencias más frecuentes.
- **D.** Plantillas de respuesta + autoservicio para el bug mientras se arregla (contención).
- **E.** (Statu quo) seguir añadiendo capacidad. — incluida solo para contraste.

---

## 5. Evaluación estratégica (Kernel de Rumelt)

- **Diagnóstico:** el problema no es de capacidad sino de *volumen entrante evitable* (bug) sostenido
  por un *incentivo* que premia cerrar rápido sin resolver.
- **Política guía:** atacar el origen y la regla, no la cola. Reducir el volumen evitable y realinear
  el incentivo antes de tocar la plantilla.
- **Acciones coherentes:** A (fix del bug, con producto) + D (contención mientras tanto) + C (base de
  conocimiento) + B (nuevo KPI). Se refuerzan entre sí.

**Filtros:**
- *Test Nardone:* A/B/C van en dirección **distinta** a lo ya intentado (no es "más de lo mismo"). ✔
- *Test Meadows:* B interviene en reglas (alto apalancamiento), no en parámetros. ✔
- *Test de renuncia (Rumelt):* renunciamos explícitamente a contratar más por ahora. ✔
- *Pre-mortem (Klein):* "a 3 meses ha fracasado, ¿por qué?" → porque producto no priorizó el bug.
  Mitigación: conseguir el compromiso de producto como condición de inicio.

---

## Próximos pasos (primeras 72h)

1. Cuantificar el volumen de tickets **por causa** (confirmar el ~40% del bug) — dato antes que acción.
2. Reunión con producto para comprometer el fix del bug (responsable y fecha).
3. Publicar plantilla + artículo de autoservicio para el bug (contención inmediata).
4. Acordar el nuevo KPI (reaperturas) y empezar a medirlo en paralelo al actual durante 2 semanas.

> Nota: este caso es Complejo, así que el plan es un **experimento monitorizado**, no una solución
> definitiva. Tras 2-3 semanas se revisa (Fase 7) y se redefine el problema desde la nueva situación.
