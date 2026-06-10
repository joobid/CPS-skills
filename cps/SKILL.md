---
name: cps
description: >
  Metodología de Resolución de Problemas Complejos (CPS) que integra Nardone, Cynefin, Rumelt, Meadows,
  Kahneman, De Bono, Wardley Mapping y JTBD. Se invoca únicamente de forma explícita con /cps.
disable-model-invocation: true
---

# Complex Problem Solving (CPS)

Skill de Resolución de Problemas Complejos que aplica una metodología integrada con las mejores herramientas de análisis
estratégico, pensamiento sistémico y creatividad estructurada.

**Eje metodológico central:** Problem Solving Estratégico de Giorgio Nardone — entender qué mantiene el problema,
romper el ciclo de soluciones fallidas, y avanzar con experimentación controlada.

**Complementado por:** Cynefin (Snowden), Pensamiento Sistémico (Meadows), Estrategia (Rumelt), Sesgos Cognitivos
(Kahneman/Munger), Creatividad (De Bono/Damas), Wardley Mapping, Jobs to Be Done, Team of Teams (McChrystal),
y la escuela de CPS de Javier Recuenco.

---

## Cómo arrancar: Menú de 3 niveles

Cuando esta skill se active, lo PRIMERO es preguntar al usuario qué nivel de profundidad necesita. Presenta
exactamente estas tres opciones:

**Nivel 1 — Análisis Rápido** (~5-10 min de lectura)
Cubre: Clasificación del problema + Definición rigurosa + Causas raíz principales + Primeras recomendaciones.
Formato: Respuesta conversacional en el chat.
Ideal para: Consultas rápidas, primeras impresiones, validar si estamos ante un problema complejo.

**Nivel 2 — Análisis Estándar** (~15-25 min de lectura)
Cubre: Fases 0 a 5 (Clasificación → Diagnóstico → Causas → Sesgos → Soluciones → Evaluación estratégica).
Formato: Respuesta estructurada en el chat o documento breve según prefiera el usuario.
Ideal para: Análisis de situación, preparación de decisiones, arranque de proyectos.

**Nivel 3 — Análisis Completo** (~30-60 min de lectura)
Cubre: La Fase 0 (clasificación previa) + las 7 fases completas con herramientas detalladas + documento entregable.
Formato: Documento Markdown (.md) con análisis completo.
Ideal para: Proyectos estratégicos, transformaciones, problemas persistentes que resisten soluciones convencionales.

Tras elegir el nivel, confirmar el idioma (español/inglés) si no es evidente por contexto.

---

## Fase 0 (clasificación previa) + las 7 fases del CPS

La Fase 0 es una clasificación previa que determina qué metodología aplicar; sobre ella se despliegan
las 7 fases del proceso CPS (1 a 7).

### FASE 0 — Clasificación del Problema

**Propósito:** Antes de analizar nada, necesitamos saber a qué tipo de problema nos enfrentamos, porque la
metodología correcta depende del tipo de problema. Usar la herramienta equivocada es peor que no usar ninguna.

Aplicar el **framework Cynefin** (Snowden):

| Dominio | Señales | Enfoque correcto |
|---------|---------|------------------|
| **Simple/Claro** | Causa-efecto evidente, existen mejores prácticas | Percibir → Categorizar → Responder |
| **Complicado** | Requiere análisis experto, múltiples respuestas válidas | Percibir → Analizar → Responder |
| **Complejo** | Causa-efecto solo visible en retrospectiva, emergencia | Probar → Percibir → Responder |
| **Caótico** | Crisis, no hay relación causa-efecto aparente | Actuar → Percibir → Responder |
| **Desorden** | No sabemos en qué dominio estamos | Descomponer y clasificar cada parte |

**Criterio práctico (Recuenco):** Si el problema fuera sencillo, ya estaría resuelto. La mayoría de problemas
que llegan a un análisis CPS son complejos con múltiples causas raíz (*complex rooting*). Asumir complejidad
como hipótesis inicial y descartarla si el análisis lo justifica.

Para profundizar en este framework: leer `references/01_clasificacion_cynefin.md`.

---

### FASE 1 — Definición Rigurosa del Problema (Diagnóstico)

**Propósito:** Entender QUÉ está pasando realmente antes de proponer nada. Esta es la fase más importante
de todo el proceso. La inmensa mayoría de fracasos en resolución de problemas vienen de una mala definición,
no de malas soluciones.

**Principio Nardone:** "No puedes resolver un problema que no comprendes. Y comprender un problema exige
entender qué lo mantiene vivo."

**Principio Rumelt:** "La diagnosis es la esencia de la estrategia. Sin ella, solo hay ilusión."

#### Paso 1.1 — Reductor de complejidad (Nardone/Recuenco)

Responder estas preguntas con la máxima concreción:

1. **¿En QUÉ consiste el problema?** — Describir comportamientos observables, no interpretaciones.
2. **¿QUIÉN está implicado?** — Todos los actores, incluyendo los que no están en la mesa.
3. **¿DÓNDE se produce?** — Contextos geográficos, organizacionales, de mercado.
4. **¿CUÁNDO se produce?** — ¿Siempre? ¿En ciertos momentos? ¿Desde cuándo?
5. **¿CÓMO funciona?** — Mecánica del problema, secuencia de eventos.
6. **¿Cómo lo perciben los demás?** — Perspectivas de los diferentes stakeholders.

#### Paso 1.2 — Soluciones Intentadas Redundantes (Nardone)

Esta es una de las herramientas más poderosas del arsenal. La idea central es: **la mayoría de problemas
persisten no a pesar de los intentos de solución, sino A CAUSA de ellos.**

Preguntar:
- ¿Qué se ha intentado hacer hasta ahora para resolver esto?
- ¿Qué pasó? ¿Por qué no funcionó?
- ¿Se ha repetido alguna solución que no funciona ("más de lo mismo")?
- ¿Hay un patrón en los intentos fallidos?

La clave es que el patrón de soluciones fallidas REVELA la estructura del problema. Si todos los intentos
van en la misma dirección y fracasan, la solución real probablemente esté en una dirección diferente.

#### Paso 1.3 — Herramientas complementarias (según necesidad)

Si el problema lo requiere, profundizar con estas herramientas (ver `references/02_diagnostico_herramientas.md`):

- **CATWOE:** Customers, Actors, Transformation, Worldview, Owner, Environment — Para problemas organizacionales.
- **IS/IS NOT (Kepner-Tregoe):** Para aislar qué es exactamente el problema y qué no es.
- **Jobs to Be Done:** Para problemas de producto/mercado — ¿qué trabajo intenta hacer el usuario/cliente?
  (ver `references/09_jtbd_wardley.md`)
- **Pensamiento Sistémico:** Stocks, flujos, bucles de retroalimentación, arquetipos sistémicos
  (ver `references/03_analisis_causal.md`)

---

### FASE 2 — Análisis de Causas Raíz

**Propósito:** Ir más allá de los síntomas para encontrar las causas profundas. Pero con una advertencia
importante.

**Advertencia (Recuenco):** Los problemas complejos tienen múltiples causas raíz (*complex rooting*).
No buscar UNA causa raíz. Buscar la constelación de factores que mantiene vivo el problema.

**Advertencia (Nardone):** A veces la "causa raíz" es irrelevante para la solución. Lo que importa es
entender qué mantiene el problema AHORA, no necesariamente qué lo originó. Un dolor de espalda puede
haberse originado por una mala postura hace 10 años, pero lo que lo mantiene hoy es un patrón de
compensación muscular.

#### Herramientas de análisis causal

Elegir las más apropiadas según el tipo de problema (detalle en `references/03_analisis_causal.md`):

1. **5 Porqués:** Cadena causal iterativa. Simple pero poderosa para problemas con causalidad lineal.
   Ojo: en problemas complejos, cada "por qué" puede bifurcarse en múltiples ramas.

2. **Diagrama de Ishikawa (Espina de Pescado):** Mapa visual de causas organizadas por categorías.
   Categorías clásicas: Personas, Procesos, Tecnología, Entorno, Materiales, Medición.

3. **Árboles Lógicos (Watanabe):** Descomposición MECE (Mutuamente Excluyente, Colectivamente Exhaustiva).
   Particularmente útil cuando el problema es grande y necesita trocearse.

4. **Puntos de Apalancamiento (Meadows):** ¿Dónde intervenir para máximo efecto? Desde parámetros
   superficiales hasta cambios de paradigma. La tentación es intervenir donde es fácil (parámetros),
   pero el impacto real suele estar en niveles más profundos (reglas, metas, paradigmas).

5. **Wardley Mapping:** Para problemas con componente tecnológico o de posicionamiento estratégico.
   Mapear la cadena de valor, identificar la evolución de cada componente, y encontrar dónde actuar.
   (ver `references/09_jtbd_wardley.md`)

---

### FASE 3 — Auditoría de Sesgos y Pensamiento Crítico

**Propósito:** Verificar que nuestro propio análisis no está contaminado por trampas cognitivas.
Esta fase es incómoda pero esencial: consiste en cuestionar lo que creemos saber.

**Fundamento (Kahneman):** El Sistema 1 (rápido, intuitivo) domina nuestras decisiones y produce
errores sistemáticos. El CPS requiere activar deliberadamente el Sistema 2 (lento, analítico).
El problema es que el Sistema 2 es "perezoso" y se resiste a activarse.

**Fundamento (Munger):** "Invierte siempre. Piensa al revés." Si no puedes refutar tu propia
hipótesis, probablemente no la entiendes lo suficiente.

#### Checklist de sesgos (aplicar al análisis realizado en Fases 1-2)

Para cada conclusión del diagnóstico, verificar:

- **Sesgo de confirmación:** ¿Estamos buscando solo evidencia que confirma nuestra hipótesis?
- **Anclaje:** ¿La primera información recibida está distorsionando todo el análisis?
- **Disponibilidad:** ¿Estamos sobrevalorando información reciente o memorable?
- **Coste hundido:** ¿Inversiones pasadas están contaminando decisiones futuras?
- **Efecto halo:** ¿El éxito en un área nos hace asumir éxito en otra?
- **Sesgo del superviviente:** ¿Estamos mirando solo los casos de éxito?
- **Exceso de confianza:** ¿Sabemos realmente lo que creemos saber?
- **Falso consenso:** ¿Asumimos que todos piensan como nosotros?

#### Técnica de inversión (Munger/Nardone)

Invertir el problema: ¿Qué tendríamos que hacer para GARANTIZAR que este problema empeore?
Las respuestas revelan las fuerzas que mantienen el problema y los errores que debemos evitar.

Detalle completo en `references/04_sesgos_pensamiento.md`.

---

### FASE 4 — Generación de Soluciones

**Propósito:** Producir el mayor número de opciones posibles ANTES de evaluar ninguna.

**Regla de oro (Damas):** Separar ESTRICTAMENTE tres tipos de pensamiento. Nunca mezclarlos en la
misma conversación o sesión de trabajo:

1. **Pensamiento Creativo** — proponer opciones sin juzgarlas
2. **Pensamiento Crítico-Defensivo** — anticipar consecuencias negativas (DESPUÉS, no durante)
3. **Pensamiento Operativo** — decidir y planificar (AL FINAL)

La contaminación más peligrosa es cuando el pensamiento defensivo entra durante la fase creativa
("eso no va a funcionar", "eso es imposible"). Mata la creatividad antes de que nazca.

#### Técnicas de Nardone (eje central)

1. **Técnica "Cómo Empeorar":** Preguntar: "¿Qué tendríamos que hacer para empeorar voluntariamente
   esta situación?" Parece absurdo, pero es extraordinariamente revelador: la respuesta muestra la
   estructura del problema y lo que realmente lo mantiene vivo. Las soluciones suelen estar en hacer
   LO CONTRARIO de lo que empeora.

2. **Técnica "Más Allá del Problema":** Imaginar que el problema ya se resolvió. "Si mañana nos
   despertáramos y el problema hubiera desaparecido, ¿qué sería diferente? ¿Qué haríamos que hoy
   no hacemos?" Esto define el estado deseado y revela acciones que podemos empezar a tomar ya.

3. **Técnica del Escalador:** Planificar DESDE la cima hacia la base. Definir el objetivo final,
   luego el paso inmediatamente anterior, y así hacia atrás hasta el presente. Esto evita quedarse
   atrapado en la complejidad del camino.

4. **Técnica de Pequeños Pasos:** Identificar micro-acciones de bajo riesgo para testar hipótesis.
   No necesitamos resolver todo de golpe; necesitamos aprender rápido con experimentos controlados.

#### Técnicas complementarias (según necesidad)

Detalle en `references/05_generacion_soluciones.md`:

- **Seis Sombreros de De Bono:** Blanco (datos), Rojo (emociones), Negro (riesgos), Amarillo
  (beneficios), Verde (creatividad), Azul (proceso).
- **Pensamiento Lateral (De Bono):** Romper patrones establecidos.
- **Flor de Loto, Conexiones Morfológicas Forzadas, Binomio Fantástico.**
- **Jobs to Be Done:** Reformular las soluciones en términos del "trabajo" que el cliente/usuario
  necesita que se haga (ver `references/09_jtbd_wardley.md`).

#### Enfoque dual (Recuenco)

Buscar en dos direcciones simultáneas:
- **Flashes of Brilliance:** ¿Hay una solución elegante, un "golpe decisivo"?
- **Strategic Hard Nosing:** ¿Cuál es la opción pragmática que funciona aunque sea incómoda?
  ¿A qué hay que renunciar?

---

### FASE 5 — Evaluación Estratégica y Selección

**Propósito:** Filtrar las opciones y construir una estrategia coherente.

#### El Kernel de Rumelt (test de calidad estratégica)

Toda buena estrategia tiene tres componentes. Si falta alguno, no es estrategia, es wishful thinking:

1. **Diagnóstico:** ¿Cuál es el desafío crítico? (Hecho en Fases 1-2)
2. **Política Guía:** ¿Cuál es nuestro enfoque general para superar el obstáculo? No es un objetivo
   ("ser los mejores"), es una dirección ("competir en precio en segmento X priorizando eficiencia operativa").
3. **Acciones Coherentes:** ¿Qué conjunto COORDINADO de acciones implementamos? Las acciones deben
   reforzarse mutuamente, no contradecirse.

#### Filtros de evaluación

Para cada opción que sobreviva al kernel de Rumelt:

1. **Test de Nardone:** ¿Esta solución es una variante de algo que ya se intentó y fracasó?
   ¿Estamos cayendo en "más de lo mismo"?

2. **Test de apalancamiento (Meadows):** ¿Estamos interviniendo al nivel correcto del sistema?
   ¿O estamos ajustando parámetros superficiales cuando deberíamos cambiar reglas o metas?

3. **Test de renuncias (Rumelt):** Estrategia genuina implica renunciar. ¿A qué renunciamos
   al elegir esta opción? Si no renunciamos a nada, probablemente no tenemos una estrategia real.

4. **Test de Wardley:** ¿Nuestra solución está alineada con la fase evolutiva de los componentes
   involucrados? (ver `references/09_jtbd_wardley.md`)

Detalle en `references/06_evaluacion_estrategica.md`.

---

### FASE 6 — Planificación e Implementación

**Propósito:** Convertir la estrategia en un plan de acción ejecutable.

#### Estructura del plan de acción

1. **Qué hay que hacer** — Acciones concretas, no aspiraciones
2. **Quién es responsable** — Nombres, no departamentos
3. **Cuándo se hace** — Fechas, no "pronto"
4. **Cómo medimos éxito** — Indicadores observables
5. **Qué puede salir mal** — Riesgos y mitigaciones
6. **Primeros pasos inmediatos** — Las primeras 72 horas

#### Gestión de la implementación

Según el tipo de problema, aplicar:

- **Metodología 8D** para problemas técnicos estructurados en dominio Complicado — requiere
  causa raíz verificable y plan formal con trazabilidad (ver `references/08_metodologia_8d.md`).
  No usar en dominio Complejo donde se necesita experimentación.
- **Team of Teams (McChrystal) + Range (Epstein)** para implementación en entornos complejos:
  construir conciencia compartida (toda la información relevante fluye a todos los niveles),
  habilitar ejecución empoderada (las decisiones las toma quien tiene la mejor información, no quien
  tiene más rango), y crear equipos adaptativos con personas en T (profundidad en su especialidad +
  amplitud para colaborar transversalmente) y generalistas que ven lo que los especialistas no
  (ver `references/10_equipos_y_generalistas.md`)
- **Comunicación y Storytelling (Damas)** para gestión del cambio: narrativa, manejo de resistencias,
  técnicas de consenso (ver `references/07_comunicacion_consenso.md`)
- **Empatía Táctica (Voss)** para gestionar stakeholders difíciles: preguntas calibradas,
  etiquetado de emociones, auditoría de acusaciones

---

### FASE 7 — Monitorización, Ajuste y Aprendizaje

**Propósito:** Verificar que la solución funciona y corregir el rumbo. Los problemas complejos
NUNCA se resuelven en un solo movimiento.

#### Principio de la matrioshka (Nardone)

Los problemas complejos son como matrioshkas: al resolver una capa, aparece la siguiente.
Esto no es un fracaso; es la naturaleza de la complejidad. Resolver lo más accesible primero,
luego REDEFINIR el problema desde la nueva situación y repetir el ciclo.

#### Ciclos adaptativos (Cynefin)

En el dominio complejo: Probar → Percibir → Responder.
- Diseñar experimentos "safe-to-fail" (que enseñan incluso si fallan)
- Monitorizar señales débiles de cambio
- Amplificar lo que funciona, amortiguar lo que no

#### Feedback sistémico (Meadows)

- ¿La intervención está produciendo los efectos esperados?
- ¿Hay efectos secundarios no previstos?
- ¿Los bucles de retroalimentación están respondiendo como esperábamos?
- ¿Necesitamos ajustar el punto de intervención?

---

## Formato de salida según nivel

### Nivel 1 (Rápido) — en chat

```
## Clasificación: [dominio Cynefin]
## Diagnóstico: [definición del problema + soluciones intentadas]
## Causas principales: [2-3 causas clave]
## Recomendación inicial: [dirección a seguir + próximos pasos]
```

**Ejemplo aplicado (Nivel 1):**

> *Problema planteado: "Nuestro equipo de soporte está saturado y los tiempos de respuesta no dejan de subir."*
>
> **Clasificación:** Complejo. No hay una causa-efecto evidente; el sistema (clientes, agentes,
> producto) es adaptativo y los intentos previos no han funcionado de forma estable.
>
> **Diagnóstico:** Los tiempos de respuesta han pasado de 4h a 18h en 3 meses. Soluciones intentadas:
> (1) contratar a 2 agentes — alivio temporal, luego peor; (2) pedir "más esfuerzo" — sin efecto.
> El patrón "más de lo mismo" (añadir capacidad) sugiere que el problema no es de capacidad.
>
> **Causas principales:** (1) Los tickets repetidos por un bug conocido del producto generan ~40%
> del volumen; (2) no hay base de conocimiento, así que cada agente reinvestiga; (3) el incentivo
> premia cerrar rápido, no resolver de raíz → reaperturas.
>
> **Recomendación inicial:** Atacar el origen, no la capacidad. Priorizar el fix del bug que genera
> el 40% del volumen y montar una base de conocimiento mínima esta semana. Medir reaperturas, no solo
> velocidad de cierre. Próximo paso (72h): cuantificar el volumen por causa antes de tocar plantilla.

Para un ejemplo completo de Nivel 2 (las fases desarrolladas paso a paso), ver
`references/11_ejemplo_aplicado.md`.

### Nivel 2 (Estándar) — en chat o documento breve

```
## 0. Clasificación del problema
## 1. Diagnóstico
### 1.1 Definición del problema
### 1.2 Soluciones intentadas (Nardone)
## 2. Análisis de causas
## 3. Sesgos detectados
## 4. Opciones generadas
## 5. Evaluación estratégica (Kernel de Rumelt)
## Próximos pasos
```

### Nivel 3 (Completo) — documento Markdown (.md)

Documento Markdown completo con la Fase 0 y las 7 fases, herramientas detalladas, diagramas donde
aporten valor, plan de implementación con responsables y fechas, y mecanismos de monitorización.

---

## Principios transversales

Estos principios aplican durante todo el proceso:

1. **Primero entender, después actuar.** La urgencia es enemiga del buen diagnóstico.
2. **Los problemas complejos tienen múltiples causas raíz.** No simplificar prematuramente.
3. **Las soluciones intentadas son información, no fracasos.** El patrón de intentos revela la estructura.
4. **Separar creatividad de crítica.** Nunca evaluar y generar al mismo tiempo.
5. **Estrategia = renunciar.** Si no renuncias a nada, no tienes estrategia.
6. **Experimentar antes que planificar en exceso.** Pequeños pasos > grandes planes en dominios complejos.
7. **Cuestionar los propios sesgos.** El análisis más brillante es inútil si está contaminado cognitivamente.
8. **La solución perfecta no existe.** Buscar la mejor opción disponible con la información disponible.

---

## Archivos de referencia

Leer estos archivos SOLO cuando una fase específica requiera profundizar en una herramienta concreta.
No leerlos todos al inicio — eso sería ineficiente y cargaría contexto innecesariamente.

| Archivo | Cuándo leerlo |
|---------|---------------|
| `references/01_clasificacion_cynefin.md` | Fase 0, si hay dudas sobre el dominio |
| `references/02_diagnostico_herramientas.md` | Fase 1, cuando se necesite CATWOE, IS/IS NOT, etc. |
| `references/03_analisis_causal.md` | Fase 2, para herramientas de causa raíz |
| `references/04_sesgos_pensamiento.md` | Fase 3, para checklist completo de sesgos y falacias |
| `references/05_generacion_soluciones.md` | Fase 4, para técnicas creativas detalladas |
| `references/06_evaluacion_estrategica.md` | Fase 5, para filtros de evaluación avanzados |
| `references/07_comunicacion_consenso.md` | Fase 6, para gestión del cambio y stakeholders |
| `references/08_metodologia_8d.md` | Fase 6, para implementación estructurada tipo 8D |
| `references/09_jtbd_wardley.md` | Fases 1, 2, 4, 5 — cuando el problema tenga componente de producto/mercado o tecnología |
| `references/10_equipos_y_generalistas.md` | Fase 6, para diseño de equipos, ejecución en entornos complejos (Team of Teams) y el valor de los generalistas (Range) |
| `references/11_ejemplo_aplicado.md` | Cualquier fase, como ejemplo de un análisis CPS completo de Nivel 2 desarrollado paso a paso |
