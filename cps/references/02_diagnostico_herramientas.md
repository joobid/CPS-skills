# Herramientas de Diagnóstico

## CATWOE (Peter Checkland — Soft Systems Methodology)

Herramienta para mapear todos los elementos relevantes de un problema organizacional. Cada letra
representa una perspectiva que debe analizarse:

**C — Customers (Clientes/Beneficiarios):**
¿Quiénes se benefician o se ven afectados por el sistema o proceso en cuestión?
¿Quiénes son los usuarios finales? ¿Quiénes sufren las consecuencias del problema?

**A — Actors (Actores):**
¿Quiénes realizan las actividades dentro del sistema?
¿Quiénes ejecutan, operan, implementan? No solo la dirección, también los operarios.

**T — Transformation (Transformación):**
¿Cuál es el proceso de transformación central?
¿Qué entrada se convierte en qué salida? ¿Cuál es el cambio que el sistema debería producir?

**W — Worldview / Weltanschauung (Visión del mundo):**
¿Qué visión del mundo o paradigma sustenta este sistema?
¿Por qué existe? ¿Qué creencias o supuestos lo hacen parecer razonable?

**O — Owner (Propietario):**
¿Quién tiene poder para cambiar o eliminar el sistema?
¿Quién puede detener la transformación? ¿Quién asigna recursos?

**E — Environmental constraints (Restricciones del entorno):**
¿Qué limitaciones externas existen? Regulación, presupuesto, tecnología, cultura, tiempo.

### Cuándo usar CATWOE
- Problemas organizacionales donde hay múltiples perspectivas
- Cuando necesitas mapear quién tiene poder, quién ejecuta, quién se beneficia
- Para asegurarte de que no estás ignorando a un stakeholder clave

### Ejemplo de aplicación
Problema: "La transformación digital del banco no avanza."
- C: Clientes del banco, empleados que usan los nuevos sistemas
- A: Equipo de IT, consultores, mandos intermedios que deben adoptar
- T: De procesos manuales/legacy → procesos digitales integrados
- W: "La digitalización es el camino hacia la eficiencia y supervivencia"
- O: CEO, Consejo de Administración
- E: Regulación bancaria, presupuesto limitado, sindicatos, legacy tecnológico

---

## IS / IS NOT (Kepner-Tregoe)

Herramienta para delimitar con precisión qué ES el problema y qué NO ES. Esto evita dos errores
comunes: definir el problema demasiado amplio (inabarcable) o demasiado estrecho (se pierden causas).

### La matriz IS/IS NOT

| Dimensión | ES (el problema) | NO ES (no es el problema) |
|-----------|-------------------|---------------------------|
| **QUÉ** | ¿Qué objeto/proceso/sistema tiene el problema? | ¿Qué objetos/procesos similares NO tienen el problema? |
| **DÓNDE** | ¿Dónde se observa geográfica u organizacionalmente? | ¿Dónde NO se observa aunque podría? |
| **CUÁNDO** | ¿Cuándo se observó por primera vez? ¿Cuándo ocurre? | ¿Cuándo NO ocurre? ¿Hay patrones temporales? |
| **CUÁNTO** | ¿Cuál es la magnitud? ¿Cuántos casos? ¿Qué tendencia? | ¿Qué magnitud esperaríamos si fuera peor? |
| **QUIÉN** | ¿A quién afecta? ¿Quién está involucrado? | ¿A quién NO afecta aunque podría? |

### Cuándo usar IS/IS NOT
- Cuando el problema es difuso y necesita acotarse
- Cuando hay confusión sobre el alcance del problema
- Para encontrar pistas: la diferencia entre "dónde SÍ ocurre" y "dónde NO ocurre" suele apuntar a la causa

### El poder de las diferencias
La clave de IS/IS NOT está en analizar las DIFERENCIAS entre las columnas. Si el problema ocurre en
la planta de Madrid pero no en la de Barcelona, ¿qué es diferente? Esa diferencia es una pista hacia
la causa raíz.

---

## Preguntas de Kipling (6W)

Marco simple y universal para explorar un problema desde todas las perspectivas:

- **WHAT / QUÉ:** ¿Qué está pasando exactamente? ¿Qué se observa?
- **WHY / POR QUÉ:** ¿Por qué es un problema? ¿Por qué importa? ¿Para qué queremos resolverlo?
- **WHEN / CUÁNDO:** ¿Cuándo empezó? ¿Cuándo ocurre? ¿Hay patrón temporal?
- **HOW / CÓMO:** ¿Cómo se manifiesta? ¿Cómo afecta? ¿Cómo hemos llegado aquí?
- **WHERE / DÓNDE:** ¿Dónde ocurre? ¿En qué contexto? ¿En qué parte de la organización?
- **WHO / QUIÉN:** ¿Quién está afectado? ¿Quién tiene influencia? ¿Quién decide?

### Cuándo usar las 6W
- Como primer barrido rápido antes de elegir herramientas más específicas
- Cuando el problema es nuevo y no tenemos ningún marco previo
- Para verificar que no nos estamos dejando ninguna perspectiva

---

## Mapeo de Stakeholders

Para problemas con múltiples actores, mapear su posición:

### Matriz Poder/Interés

| | Bajo interés | Alto interés |
|---|---|---|
| **Alto poder** | Mantener satisfechos | Gestionar de cerca |
| **Bajo poder** | Monitorizar | Mantener informados |

### Preguntas clave por stakeholder
- ¿Qué quieren que pase?
- ¿Qué temen que pase?
- ¿Qué poder real tienen?
- ¿Quién influye sobre ellos?
- ¿Cuál es su posición actual respecto al problema?

---

## Técnica del Reductor de Complejidad (Recuenco/Nardone)

Esta es la herramienta de diagnóstico central del proceso CPS. Combina la rigurosidad de Kepner-Tregoe
con la perspectiva sistémica de Nardone. Se aplica en dos pasos: primero las 6 preguntas de
caracterización (Paso 1.1) y, a continuación y por separado, las Soluciones Intentadas Redundantes
(Paso 1.2). Esta es la misma estructura del Paso 1.1 / 1.2 de la Fase 1 en `SKILL.md`.

### Paso 1.1 — Las 6 preguntas de caracterización

1. **¿En QUÉ consiste el problema?** — Solo comportamientos observables, no interpretaciones.
   MAL: "El equipo no está motivado." BIEN: "3 de 5 entregas se han retrasado más de 2 semanas."

2. **¿QUIÉN está implicado?** — TODOS los actores. Incluir los que no están en la mesa pero deberían.

3. **¿DÓNDE se produce?** — Localización física, organizacional, de mercado. ¿En qué contextos aparece?

4. **¿CUÁNDO se produce?** — Inicio, frecuencia, patrones. ¿Siempre? ¿Solo en ciertos momentos?

5. **¿CÓMO funciona el problema?** — La mecánica. ¿Cuál es la secuencia de eventos que lo reproduce?

6. **¿Cómo lo ven los demás?** — Perspectivas divergentes. Lo que para unos es un problema, para otros
   puede ser una solución (o algo invisible).

### Paso 1.2 — Soluciones Intentadas Redundantes (Nardone)

Paso separado y CRUCIAL: **¿Qué se ha intentado hacer hasta ahora para resolver el problema?**
El patrón de intentos fallidos revela la estructura del problema. Si todos los intentos van en la
misma dirección y fracasan ("más de lo mismo"), la solución real probablemente esté en otra dirección.
