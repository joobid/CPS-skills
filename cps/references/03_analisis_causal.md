# Análisis de Causas Raíz

## Principios fundamentales

Antes de usar cualquier herramienta, recordar:

**Principio de Recuenco:** Los problemas complejos tienen múltiples causas raíz (*complex rooting*).
Buscar UNA causa es un error. Buscar la constelación de factores que mantiene el problema.

**Principio de Nardone:** A veces la causa original es irrelevante. Lo que importa es qué MANTIENE
el problema ahora. Las soluciones intentadas pueden ser la verdadera causa de la persistencia.

**Principio de Meadows:** Los síntomas visibles suelen estar lejos de las causas profundas. Los
puntos de mayor impacto (apalancamiento) suelen ser contraintuitivos.

---

## 5 Porqués (Toyota Production System)

### Cómo funciona
Ante un síntoma, preguntar "¿por qué?" iterativamente hasta llegar a una causa sobre la que podamos actuar.

### Ejemplo
- ¿Por qué las entregas se retrasan? → Porque las estimaciones son incorrectas.
- ¿Por qué las estimaciones son incorrectas? → Porque no consideran las dependencias externas.
- ¿Por qué no se consideran? → Porque el equipo no conoce el roadmap de otros equipos.
- ¿Por qué no lo conocen? → Porque no hay un proceso de sincronización entre equipos.
- ¿Por qué no hay proceso? → Porque cada equipo opera como silo independiente.

### Cuándo funciona bien
- Problemas con causalidad relativamente lineal
- Como punto de partida rápido antes de herramientas más sofisticadas

### Limitaciones
- En problemas complejos, cada "por qué" puede bifurcarse en múltiples ramas
- Puede llevar a causas "cósmicas" inaccionables ("porque así es la naturaleza humana")
- No captura interacciones entre causas (feedback loops)

### Regla práctica
Si al tercer "por qué" ya tienes múltiples ramas divergentes, cambia a Ishikawa o árboles lógicos.

---

## Diagrama de Ishikawa (Espina de Pescado / Causa-Efecto)

### Cómo funciona
El efecto (problema) se coloca en la "cabeza" del pez. Las espinas principales representan categorías
de causas. Las espinas secundarias representan causas específicas dentro de cada categoría.

### Categorías clásicas (6M)
- **Mano de obra / People:** Competencias, motivación, cantidad, experiencia
- **Métodos / Process:** Procedimientos, flujos de trabajo, estándares
- **Máquinas / Technology:** Herramientas, sistemas, infraestructura
- **Materiales / Materials:** Datos, inputs, recursos, información
- **Medición / Measurement:** KPIs, métricas, feedback, monitorización
- **Medio ambiente / Environment:** Cultura, mercado, regulación, contexto

### Cuándo usar Ishikawa
- Cuando el problema tiene múltiples categorías de causas potenciales
- Para sesiones de análisis grupal (facilita la conversación estructurada)
- Cuando necesitas visualizar la complejidad causal

### Cómo hacerlo bien
1. Definir el problema con precisión ANTES de empezar
2. Generar causas SIN juzgarlas (fase creativa)
3. Agrupar y priorizar DESPUÉS
4. Verificar las causas más probables con datos

---

## Árboles Lógicos (Watanabe / McKinsey)

### Cómo funciona
Descomponer el problema de forma MECE (Mutuamente Excluyente, Colectivamente Exhaustiva) hasta
llegar a componentes accionables.

### Tipos de árboles lógicos
- **Árbol de problemas:** Descompone "¿por qué?" → causas
- **Árbol de soluciones:** Descompone "¿cómo?" → opciones
- **Árbol de hipótesis:** Descompone "¿qué podría estar pasando?" → hipótesis verificables

### MECE: el estándar de calidad
- **Mutuamente Excluyente:** Las ramas no se solapan. Cada causa está en un solo lugar.
- **Colectivamente Exhaustiva:** Las ramas cubren todo el espacio de posibilidades. No falta nada.

### Ejemplo: Árbol de problemas
"Las ventas han bajado un 20%"
├── Menos clientes nuevos
│   ├── Menor alcance de marketing
│   ├── Peor conversión
│   └── Mercado contraído
├── Más clientes perdidos (churn)
│   ├── Problemas de producto/servicio
│   ├── Competencia más atractiva
│   └── Cambio en necesidades del cliente
└── Menor ticket medio
    ├── Mix de productos desfavorable
    ├── Más descuentos
    └── Productos premium descatalogados

### Cuándo usar árboles lógicos
- Problemas cuantitativos que se pueden descomponer
- Cuando necesitas ser exhaustivo y no dejarte nada
- Para comunicar la estructura del análisis a otros

---

## Puntos de Apalancamiento (Donella Meadows)

### Los 12 niveles de intervención (de menor a mayor impacto)

**Nivel bajo — Parámetros del sistema:**
12. Constantes, parámetros, números (subir precio, bajar coste...)
11. Tamaño de los buffers (inventario, cash reserve...)

**Nivel medio — Estructura del sistema:**
10. Estructura de stocks y flujos materiales
9. Longitud de los retrasos en feedback
8. Fuerza de los bucles de retroalimentación negativa
7. Impulso de los bucles de retroalimentación positiva

**Nivel alto — Información y reglas:**
6. Estructura de flujos de información (quién sabe qué)
5. Reglas del sistema (incentivos, penalizaciones, normas)
4. Poder de añadir, cambiar o auto-organizar la estructura

**Nivel máximo — Paradigma:**
3. Metas del sistema
2. Paradigma / mentalidad del sistema
1. Poder de trascender paradigmas

### Principio clave
La tentación es intervenir donde es fácil y visible (parámetros: nivel 12). Pero el impacto real
suele estar en niveles más profundos (reglas, metas, paradigma). Cuanto más profundo, más difícil
pero más transformador.

### Ejemplo aplicado
Problema: "El equipo entrega con baja calidad."
- Nivel 12 (parámetro): Aumentar las horas de testing → bajo impacto
- Nivel 8 (feedback): Implementar code review con feedback inmediato → impacto medio
- Nivel 6 (información): Hacer visible el coste real de los bugs a todo el equipo → impacto alto
- Nivel 5 (reglas): Cambiar incentivos de "entregar rápido" a "entregar bien" → impacto alto
- Nivel 3 (meta): Redefinir la meta del equipo de "cumplir plazos" a "satisfacer al cliente" → impacto máximo

---

## Arquetipos Sistémicos (Meadows/Senge)

Patrones recurrentes en sistemas complejos. Reconocerlos permite anticipar dinámicas:

### Límites al crecimiento
Un proceso se refuerza produciendo crecimiento, hasta que choca con un límite.
**Señal:** Crecimiento que se estanca o se invierte.
**Error típico:** Empujar más fuerte en el motor de crecimiento. **Solución:** Identificar y relajar el límite.

### Desplazamiento de la carga
Un problema se "resuelve" con una solución sintomática que debilita la capacidad de resolver la causa.
**Señal:** Dependencia creciente de la solución temporal. **Ejemplo:** Usar consultores externos en vez de
desarrollar talento interno.

### Escalada
Dos partes compiten, cada una respondiendo al movimiento del otro con más esfuerzo.
**Señal:** Costes crecientes sin mejora relativa. **Ejemplo:** Guerra de precios entre competidores.

### Éxito genera éxito
Los que tienen éxito acumulan recursos que generan más éxito, a costa de los demás.
**Señal:** Concentración creciente de recursos. **Ejemplo:** Los equipos que mejor funcionan atraen el mejor talento.

### Soluciones que fallan
Una solución produce efectos secundarios que empeoran el problema original.
**Señal:** El problema vuelve peor tras cada "solución". **Ejemplo:** Recortar personal para ahorrar costes
→ sobrecarga → más errores → más costes.

### Tragedia de los comunes
Cada actor optimiza su beneficio individual agotando un recurso compartido.
**Señal:** Recurso compartido en declive mientras todos dicen "mi parte es pequeña".
