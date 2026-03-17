# CLAUDE.md — Robby's Personal Website & Portfolio

> PARA-style project file. Organized into Projects, Areas, Resources, Archives.

---

## P — Projects

Active, time-bound work with a clear outcome.

### 1. Portfolio Website (robbyambler.github.io)
- **Goal:** Launch a personal portfolio site on GitHub Pages showcasing work, skills, and personality.
- **Stack:** TBD (options: Next.js static export, Astro, plain HTML/CSS)
- **Repo:** `robbyambler/robbyambler.github.io` on GitHub
- **Status:** Setup phase
- **Key tasks:**
  - [ ] Choose stack & scaffold repo
  - [ ] Define content sections (About, Work, Projects, Contact)
  - [ ] Design system / brand kit (use Canva MCP for assets)
  - [ ] Write and review copy
  - [ ] Deploy to GitHub Pages

### 2. Project Showcase Pages
- **Goal:** Publish individual project write-ups alongside the portfolio.
- **Status:** Blocked on portfolio foundation

---

## A — Areas

Ongoing responsibilities with no defined end date.

### Personal Brand
- Visual identity: colors, typography, logo (see OneDrive → MCP stuff for historical assets)
- Tone of voice: professional but approachable, concise
- Canva brand kit to be established and linked here

### Technical Presence
- GitHub: `robbyambler` — keep repos tidy, READMEs current, pinned projects relevant
- GitHub Pages: `robbyambler.github.io` — primary public-facing URL
- OneDrive: `/Users/robbyambler/Library/CloudStorage/OneDrive-Personal/` — asset storage, archives

### Content Strategy
- Decide what goes on the site vs. what lives in GitHub READMEs
- Keep portfolio projects current as work evolves

---

## R — Resources

Reference material, tools, patterns, and decisions.

### Agent System
This project uses three sub-agents coordinated by an orchestrator. See `.claude/agents/`:
- `orchestrator.md` — top-level coordination, task routing, decision-making
- `coding.md` — implementation, git, deployment, build tooling
- `ux-ui.md` — design, Canva MCP, visual decisions, layout & copy feedback

### MCP Servers
- **onedrive** — Filesystem MCP server mounted at OneDrive root.
  Config: `.claude/settings.json`
  Root: `/Users/robbyambler/Library/CloudStorage/OneDrive-Personal/`
  Use for: reading assets, logos, old site files from OneDrive
- **canva** (global) — Available via `mcp__claude_ai_Canva__*` tools for design work

### Tech Stack Decisions (TBD)
| Decision | Options | Chosen |
|---|---|---|
| Site framework | Next.js, Astro, plain HTML | **SvelteKit + static adapter** |
| Styling | Tailwind, CSS modules, vanilla CSS | **Tailwind CSS v4** |
| Deployment | GitHub Pages, Vercel | GitHub Pages |
| CMS | None (static), Contentlayer | TBD |

### Key Paths
| Name | Path |
|---|---|
| OneDrive root | `/Users/robbyambler/Library/CloudStorage/OneDrive-Personal/` |
| Old MCP site assets | `…/OneDrive-Personal/MCP stuff/` |
| Projects folder | `…/OneDrive-Personal/Projects/` |
| This project | `…/Projects/Robby website/` |

### Workflow
1. Use **orchestrator** agent to plan and coordinate tasks
2. Route design/visual work to **ux-ui** agent (with Canva MCP access)
3. Route code/build/deploy work to **coding** agent
4. Use **onedrive** MCP to pull assets from OneDrive when needed

---

## Archives

Completed or paused work.

*(Empty — project just started 2026-03-09)*
