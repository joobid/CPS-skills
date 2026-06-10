# Complex Problem Solving (CPS) — Claude Skill

Skill de Resolución de Problemas Complejos para [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) y [Cowork](https://claude.ai).

Integra las mejores herramientas de análisis estratégico, pensamiento sistémico y creatividad estructurada en una metodología cohesiva de 7 fases.

## Qué hace

Cuando se activa, guía a Claude a través de un proceso riguroso de resolución de problemas complejos, con tres niveles de profundidad a elegir:

| Nivel | Fases | Formato | Ideal para |
|-------|-------|---------|------------|
| **Rápido** | 0-2 | Chat | Diagnósticos rápidos, primeras impresiones |
| **Estándar** | 0-5 | Chat o documento breve | Análisis de situación, preparación de decisiones |
| **Completo** | 0-7 | Documento Markdown | Proyectos estratégicos, transformaciones |

## Fase 0 + las 7 fases

La Fase 0 es una clasificación previa que determina qué metodología aplicar; sobre ella se despliegan
las 7 fases del proceso CPS (1 a 7).

| Fase | Nombre | Herramientas principales |
|------|--------|------------------------|
| 0 | Clasificación del problema | Cynefin (Snowden) |
| 1 | Definición rigurosa | Nardone (Reductor, SIR), CATWOE, IS/IS NOT, JTBD |
| 2 | Análisis de causas raíz | 5 Whys, Ishikawa, Árboles lógicos, Leverage Points, Wardley |
| 3 | Auditoría de sesgos | Kahneman (S1/S2), Munger (modelos mentales), Falacias |
| 4 | Generación de soluciones | Nardone (Cómo Empeorar, Escalador), De Bono, Creatividad |
| 5 | Evaluación estratégica | Rumelt (Kernel), Tests de evaluación, Pre-mortem |
| 6 | Implementación | 8D, Team of Teams, Storytelling, Empatía Táctica |
| 7 | Monitorización y ajuste | Matrioshka (Nardone), Ciclos adaptativos, Feedback sistémico |

## Eje metodológico

**Problem Solving Estratégico de Giorgio Nardone** como columna vertebral, complementado por:

- **Dave Snowden** — Cynefin Framework
- **Richard Rumelt** — Good Strategy Bad Strategy
- **Donella Meadows** — Thinking in Systems
- **Daniel Kahneman** — Thinking, Fast and Slow
- **Charlie Munger** — Mental Models
- **Edward de Bono** — Lateral Thinking, Six Thinking Hats
- **Stanley McChrystal** — Team of Teams
- **Chris Voss** — Never Split the Difference
- **Ken Watanabe** — Problem Solving 101
- **David Epstein** — Range
- **Simon Wardley** — Wardley Mapping
- **Clayton Christensen** — Jobs to Be Done
- **Javier Recuenco** — CPS / Singular Solving
- **Diana Damas** — Pensamiento Crítico, Creatividad, Comunicación

## Estructura

```
cps/
├── SKILL.md                              # Instrucciones principales
└── references/
    ├── 01_clasificacion_cynefin.md       # Framework Cynefin
    ├── 02_diagnostico_herramientas.md    # CATWOE, IS/IS NOT, Kipling, Stakeholders
    ├── 03_analisis_causal.md             # 5 Whys, Ishikawa, Árboles, Leverage Points
    ├── 04_sesgos_pensamiento.md          # S1/S2, Sesgos, Falacias, Munger
    ├── 05_generacion_soluciones.md       # Nardone, De Bono, Técnicas creativas
    ├── 06_evaluacion_estrategica.md      # Rumelt Kernel, Tests de evaluación
    ├── 07_comunicacion_consenso.md       # Storytelling, Resistencias, Consenso
    ├── 08_metodologia_8d.md              # Metodología 8D completa
    ├── 09_jtbd_wardley.md                # Jobs to Be Done + Wardley Mapping
    ├── 10_equipos_y_generalistas.md      # Team of Teams (McChrystal) + Range (Epstein)
    └── 11_ejemplo_aplicado.md            # Ejemplo completo de análisis CPS (Nivel 2)
```

## Instalación

### Claude Code

Copia la carpeta `cps/` a tu directorio de skills:

```bash
cp -r cps/ ~/.claude/skills/
```

La skill se invoca **únicamente** de forma explícita escribiendo `/cps` (no se activa
automáticamente).

### Empaquetar la skill (`.skill`) para Cowork

El paquete `.skill` no se versiona en el repositorio; se genera bajo demanda a partir de la carpeta
`cps/`. Es simplemente un zip de esa carpeta con la extensión `.skill`:

**macOS / Linux (bash):**

```bash
zip -r complex-problem-solving.skill cps/
```

**Windows (PowerShell):**

> Nota: `Compress-Archive` en Windows PowerShell 5.1 guarda las rutas internas con `\`, lo que algunos
> importadores (incluido Cowork) pueden rechazar. Este script genera el zip con rutas `/` correctas:

```powershell
Add-Type -AssemblyName System.IO.Compression.FileSystem
$src = (Resolve-Path .\cps).Path
$out = (Join-Path (Get-Location) 'complex-problem-solving.skill')
if (Test-Path $out) { Remove-Item $out -Force }
$zip = [System.IO.Compression.ZipFile]::Open($out, 'Create')
foreach ($f in Get-ChildItem $src -Recurse -File) {
    $entry = 'cps/' + $f.FullName.Substring($src.Length + 1).Replace('\','/')
    [void][System.IO.Compression.ZipFileExtensions]::CreateEntryFromFile($zip, $f.FullName, $entry)
}
$zip.Dispose()
```

El zip debe contener la carpeta `cps/` en su raíz con rutas tipo `cps/SKILL.md`, `cps/references/*.md`
(separador `/`, no `\`).

### Cowork (Claude Desktop)

1. Genera el archivo `complex-problem-solving.skill` con los comandos de la sección anterior
2. Arrastra el archivo a una conversación de Cowork, o bien ábrelo desde el Finder
3. Aparecerá un botón **"Copy to your skills"** — púlsalo para instalar
4. La skill estará disponible en todas tus sesiones futuras de Cowork

## Idiomas

La skill funciona en **español** e **inglés**. Claude adapta el idioma según el contexto de la conversación.

## Casos de uso

- Análisis estratégico de negocio
- Transformación organizacional
- Diagnóstico de problemas tecnológicos complejos
- Análisis de situaciones ambiguas con información incompleta
- Arranque y framing de proyectos complejos
- Evaluación de alternativas estratégicas
- Resolución de problemas persistentes que resisten soluciones convencionales

## Por qué esta skill

He escrito un artículo en LinkedIn explicando la motivación detrás de este proyecto, qué es una skill de Claude y cómo se ha diseñado la metodología CPS:

👉 [¿Y si hubiera enseñado a Claude cómo resolver problemas complejos?](https://www.linkedin.com/posts/jorgeordovas_cpslive2026-activity-7441915633513971712-E0jF)

## Licencia

MIT — ver [LICENSE](LICENSE).
