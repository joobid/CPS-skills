# Clasificación del Problema: Framework Cynefin

## Origen y propósito

El framework Cynefin (pronunciado "ku-NE-vin", palabra galesa que significa "hábitat") fue creado por
Dave Snowden en 1999 mientras trabajaba en IBM Global Services. Es una herramienta de sensemaking que
ayuda a clasificar el tipo de problema al que nos enfrentamos para elegir el enfoque metodológico correcto.

La idea central es simple pero poderosa: **no todos los problemas son iguales, y usar la metodología
equivocada puede ser peor que no usar ninguna.**

---

## Los cinco dominios

### 1. Dominio Simple/Claro — "Known knowns"

**Señales:**
- La relación causa-efecto es evidente para todos
- Existen mejores prácticas establecidas y probadas
- La situación es estable y predecible
- Cualquier persona competente puede resolverlo

**Enfoque:** Percibir → Categorizar → Responder
- Observar la situación
- Clasificarla en una categoría conocida
- Aplicar la mejor práctica correspondiente

**Ejemplo:** Un servidor se queda sin espacio en disco. La solución es conocida: limpiar logs, ampliar disco,
configurar rotación.

**Riesgo principal:** La complacencia. Si se asume que todo es simple, se pierde la capacidad de detectar
cuando una situación migra a otro dominio.

---

### 2. Dominio Complicado — "Known unknowns"

**Señales:**
- Existe relación causa-efecto pero requiere análisis experto
- Puede haber múltiples soluciones correctas
- Se necesita conocimiento especializado
- El análisis puede llevar tiempo pero el problema es fundamentalmente analizable

**Enfoque:** Percibir → Analizar → Responder
- Observar la situación
- Aplicar análisis experto
- Implementar una buena práctica (no necesariamente "la mejor")

**Ejemplo:** Optimizar el rendimiento de una arquitectura de microservicios. Hay múltiples enfoques válidos
(caching, escalado horizontal, rediseño de queries...) y se necesita expertise para elegir el mejor.

**Riesgo principal:** La "parálisis por análisis" — analizar interminablemente sin actuar. También el sesgo
del experto (el martillo de Maslow: si eres experto en bases de datos, todo parece un problema de BD).

---

### 3. Dominio Complejo — "Unknown unknowns"

**Señales:**
- La causa-efecto solo es visible en retrospectiva
- Los resultados emergen de la interacción de múltiples factores
- Condiciones iniciales similares pueden producir resultados muy diferentes
- Los agentes del sistema son adaptativos (cambian su comportamiento)
- No hay experto que pueda predecir con certeza qué pasará

**Enfoque:** Probar → Percibir → Responder
- Diseñar experimentos "safe-to-fail"
- Observar qué emerge
- Amplificar lo que funciona, amortiguar lo que no
- Iterar

**Ejemplo:** Transformar la cultura de una organización. No hay receta. Lo que funcionó en la empresa A
puede ser desastroso en la empresa B. Hay que experimentar, observar qué pasa, y ajustar.

**Riesgo principal:** Intentar "analizar" el problema como si fuera complicado. En el dominio complejo,
los planes detallados a largo plazo son una fantasía. Lo que funciona es la experimentación rápida.

---

### 4. Dominio Caótico — "Unknowable unknowns"

**Señales:**
- No hay relación causa-efecto perceptible
- Situación de crisis aguda
- Necesidad de acción inmediata
- No hay tiempo para análisis

**Enfoque:** Actuar → Percibir → Responder
- Tomar acción decisiva para estabilizar
- Observar qué ha cambiado
- Trabajar para mover la situación a un dominio más manejable (complejo o complicado)

**Ejemplo:** Caída masiva de producción sin causa conocida. Primero restaurar el servicio (actuar),
luego entender qué pasó (percibir), luego establecer medidas preventivas (responder).

**Riesgo principal:** Quedarse en modo crisis permanente. El dominio caótico debe ser transitorio.

---

### 5. Desorden (centro del framework)

**Señales:**
- No sabemos en qué dominio estamos
- Diferentes personas clasifican la situación de formas distintas
- Confusión generalizada sobre cómo abordar el problema

**Enfoque:**
- Descomponer la situación en partes
- Clasificar cada parte en su dominio correspondiente
- Aplicar el enfoque apropiado a cada parte

Este es el estado más peligroso porque las personas tienden a clasificar la situación en el dominio
donde se sienten más cómodas, no donde realmente está.

---

## Transiciones entre dominios

Las situaciones no son estáticas. Pueden migrar entre dominios:

- **Simple → Caótico:** Cuando la complacencia permite que un problema sencillo se descontrole
  (el "precipicio de la complacencia").
- **Caótico → Complejo:** Tras estabilizar una crisis, entramos en exploración.
- **Complejo → Complicado:** Cuando los patrones se hacen visibles y podemos establecer buenas prácticas.
- **Complicado → Simple:** Cuando las buenas prácticas se consolidan en procedimientos estándar.

---

## Error más común en CPS

El error más frecuente es tratar problemas complejos como si fueran complicados. Esto se manifiesta como:

- Encargar un "estudio" o "análisis" exhaustivo esperando que revele "la respuesta"
- Contratar a un "experto" que tenga "la solución"
- Crear un plan detallado a 3 años para un entorno que cambia cada 3 meses
- Buscar benchmarks y mejores prácticas de otras empresas para copiar

En el dominio complejo, el único camino es experimentar. No hay atajo analítico.

---

## Integración con el proceso CPS

La clasificación Cynefin se usa en la Fase 0 y condiciona TODO el proceso posterior:

| Si el dominio es... | El CPS enfatiza... |
|---------------------|-------------------|
| Simple | Verificar que realmente es simple, aplicar estándar, siguiente problema |
| Complicado | Fases 1-3 (diagnóstico + causas + sesgos) con profundidad, Fase 5 analítica |
| Complejo | Todo el proceso, con énfasis en Nardone (Pequeños Pasos) y Fase 7 (iteración) |
| Caótico | Acción inmediata primero, luego aplicar CPS completo a la situación estabilizada |
