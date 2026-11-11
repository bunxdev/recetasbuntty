# Recetas BunTTY

Configuraciones, agentes y skills para [BunTTY](https://github.com/bunxdev/buntty) — terminal web colaborativa multi-agente.

## Agentes (Grid 3x2)

BunTTY corre 6 agentes especializados en un grid 3x2, cada uno con su propia sesión de shell:

| # | Nombre | Rol | Color | Descripción |
|---|--------|-----|-------|-------------|
| 1 | Designer | UI/UX Designer | `#e74c3c` | Diseño de interfaces, componentes y experiencia de usuario |
| 2 | Backend | Backend Developer | `#3498db` | Lógica del servidor, base de datos y arquitectura |
| 3 | API | Bun API Expert | `#2ecc71` | Diseño y construcción de APIs con Bun |
| 4 | Red Team | Offensive Security | `#ff4444` | Pruebas de penetración y búsqueda de vulnerabilidades |
| 5 | Blue Team | Defensive Security | `#4488ff` | Defensa, monitoreo y hardening del sistema |
| 6 | Purple Team | Security Analysis | `#9b59b6` | Análisis cruzado entre Red y Blue, validación de controles |

La configuración completa está en [`agents.json`](agents.json).

## Archivos

- **`agents.json`** — Configuración de los 6 agentes (sesiones, nombres, roles, colores, workspaces)
- **`Camino.md`** — Arquitectura y filosofía de BunTTY
- **`README.md`** — Este archivo

## Claude Code Skills

Skills instaladas en `.claude/skills/` del proyecto BunTTY para potenciar a los agentes:

### Superpowers

Workflow y colaboración multi-agente.

| Skill | Descripción |
|-------|-------------|
| `superpowers-brainstorming` | Sesiones de brainstorming estructuradas |
| `superpowers-dispatching-parallel-agents` | Despacho de agentes en paralelo |
| `superpowers-executing-plans` | Ejecución paso a paso de planes |
| `superpowers-subagent-driven-development` | Desarrollo dirigido por sub-agentes |

Repo: [complexthings/superpowers](https://github.com/complexthings/superpowers)

### Claude-Mem

Memoria, exploración y conocimiento del codebase.

| Skill | Descripción |
|-------|-------------|
| `claude-mem-mem-search` | Búsqueda en la memoria del proyecto |
| `claude-mem-learn-codebase` | Aprendizaje del codebase |
| `claude-mem-smart-explore` | Exploración inteligente de código |
| `claude-mem-how-it-works` | Explicación de cómo funciona el sistema |
| `claude-mem-do` | Ejecutar tareas con contexto |
| `claude-mem-knowledge-agent` | Agente de conocimiento |

Repo: [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)

### Impeccable

Diseño y UI de nivel profesional.

| Skill | Descripción |
|-------|-------------|
| `impeccable` | Diseño, rediseño, critique, audit, polish, animate para frontend y UI |

Comandos: `shape`, `audit`, `critique`, `polish`, `bolder`, `quieter`, `distill`, `animate`, `colorize`, `typeset`, `layout`, `delight`, `overdrive`, `clarify`, `adapt`, `optimize`, `live`, `generate`

Repo: [pbakaus/impeccable](https://github.com/pbakaus/impeccable)

### Ponytail

Modo "senior developer perezoso" — el cambio más pequeño que resuelve el problema completo.

| Skill | Descripción |
|-------|-------------|
| `ponytail` | Minimismo en código: lazy senior dev mode |

Niveles: `lite` (construye lo pedido), `full` (default, mínimo código), `ultra` (cuestiona el request)

Repo: [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail)

### Find Skills

| Skill | Descripción |
|-------|-------------|
| `find-skills` | Descubre y lista skills disponibles, slash commands y MCP servers |

Custom skill — incluida en este proyecto.

## Uso

```bash
# Clonar las recetas
git clone https://github.com/bunxdev/recetasbuntty.git

# Copiar agents.json a tu proyecto BunTTY
cp recetasbuntty/agents.json tu-proyecto/scripts/agents/

# Las skills se instalan en .claude/skills/ del proyecto BunTTY
# Ver el repo principal: https://github.com/bunxdev/buntty
```

## BunTTY v5.3

Features completas del stack:

- **v5.0**: Auth (BT_TOKEN), TLS, readonly, download log, WebGL, search, grid NxM
- **v5.1**: 7 themes + picker, mobile keys, Sixel images
- **v5.2**: File transfer (drag-drop + API), Files panel, CSP headers
- **v5.3**: Session recording (asciinema v2), web replay player, REC indicator, grid minimal mode
