# Conversation Log - Dev Environment Onboarding Skill

## Interview Series: TrueMotive Ubuntu Dev Environment Setup
### Skill: Dev Environment Onboarding (SKILL.md)
### Project: TrueMotive Ubuntu Dev Environment Seed
### Project Root: /home/chris/src/mahoney-linux-devsetup-leo

### Conversation #1: Service Infrastructure & gh CLI Setup (COMPLETED)
- **Date**: Current session (2026-11-06)
- **Part**: Part 1 - Local Services & Infrastructure
- **Status**: COMPLETED - All sections A-F addressed
- **Topics covered** (per user A-F responses):

  **A) Databases**: PostgreSQL, Supabase
  - GitHub-based repo "firenook" cloned to homebase source (/home/chris/src/firenook)
  - Firenook: Faster drop-in replacement for Firebase Local Emulator Suite
  - 40× faster writes, 10× less memory, no Java, data survives restarts

  **B) Caching & Queues**: SKIPPED (per user instruction - leave for now)

  **C) Other Infrastructure**:
  - Local S3 and Cloudflare R2 via 'npx wrangler' CLI tool
  - Prometheus and Grafana running via docker compose
  - Docker and docker compose infra already exists on machine
  - GitHub CLI tool with agent permission to access repo information read-only for now
  - Permission gating to revisit when passing v1 of the repo

  **D) Docker Compose awareness** - MOST IMPORTANT REPO:
  - Query existing docker infrastructure for 'mediamesh' compose stack
  - **truemotive-desktop** is the most important repo to start with in GitHub
  - Mediamesh repo (chrismahoney/org) is original v1 interface
  - Migrating UI features out of mediamesh through design passes/migrations
  - To truemotive-desktop project (homebase source directory)
  - Mediamesh compose stacks: docker-compose.yml, docker-compose.secondary.yml, docker-compose.livekit-agents.yml

  **E) Skill tracking**: Synchro across desired agents (Claude Code, Cline, Qwen Code)
  - Taking place via npx skillkit usage
- **Pivotal feature**: First installable skills for turnkey dev environment
- **Cross-agent sync**: Skills installed in .claude.skills/ also accessible via .cline.skills/ directory
- **Sync mechanism**: `npx skillkit skillkit sync` registers skills with both Claude Code (CLAUDE.md) and Cline configs
- **Directory structure**: Same SKILL.md format in both ~/.claude/skills/ and ~/.cline/skills/ ensures compatibility
- Claude Code: ✅ Skills installed in .claude/skills/, CLAUDE.md configured via skillkit sync
- Cline: ✅ Skills populated in .cline/skills/ (remotion-dev, anthropic, vercel-lab, stripe/ai, expo/skills, glebis)
- Sync status: ✅ Both agents synchronized with 61 total skills installed
- Qwen Code: ⚠️ Skill inventory TBD, coordination via shared SKILL.md format planned
- Last sync: 2026-11-06 (this session)
- Next sync: After new developer onboarding or skill addition
    - Built and deployed via PR activity in truemotive-desktop cloned repo

### Repository Status Summary (post-research)
- **truemotive-desktop**: MODIFIED (package.json changed), most important repo
- **occc-ui**: MODIFIED (app/package-lock.json changed)
- **mediamesh**: CLEAN working tree, huge backend control plane project
- **firenook**: NEWLY CLONED, upstream + origin remotes
- **truemotive-website**: CLEAN working tree, Astro-based
- **mahoney-linux-devsetup-leo**: Clean, just pushed to GitHub
- All repos checked against remote origin - machine idle for at least a month

### Tailscale Network Status
- Machine: turbo-1 on mastodon-adder.ts.net tailnet
- TUN up, Online, Self IP: 100.124.160.30 (exit node: dfw)
- Peer developers: Danny and Rob also on tailnet
- Documentation should track tailnet device info in memory-bank/convos/

### Docker Compose Infrastructure (post-research)
- mediamesh has 3 compose stacks:
  - docker-compose.yml (primary, engine service)
  - docker-compose.secondary.yml
  - docker-compose.livekit-agents.yml
- Prometheus + Grafana running via docker compose
- Local S3 + Cloudflare R2 via npx wrangler CLI
- GitHub CLI read-only permissions (extendable case-by-case)

### Next Conversation Trigger
- Proceed to Part 2: Docker Compose Stacks details
- Focus on mediamesh compose stacks and truemotive-desktop integration
- Discuss frontend URLs for local development stacks
- Continue skill tracking across agents via npx skillkit

### Anthropic + Vercel Skills → Interview Stage Mapping (Added 2026-11-06)

| # | Skill Name | Brief Description | Useful Interview Parts | Specific Section References* |
|---|------------|-------------------|------------------------|------------------------------|
| 1 | **academy-guide** | Onboarding guide for new developers – covers environment setup, tooling, and processes. | Part 6 (TODO & Onboarding), Part 4 (Essential Tools & Services) | **E** (skill-tracking across agents via `npx skillkit`), **F** (Tailscale/placeholder notes) |
| 2 | **brand-guidelines** | Company brand & design guidelines ensuring consistent UI/UX and documentation styling. | Part 1 (D), Part 3 (Frontend URLs & Local Dev) | **D** (mediamesh compose stack / truemotive-desktop most important repo) |
| 3 | **claude-api** | Skill for interacting with Anthropic's Claude API – task automation, integration, and dynamic prompts. | Part 4 (Essential Tools & Services), Part 1 (E) | **E** (skill-tracking across agents) |
| 4 | **code-review-analysis** | Automated code-review assistant that flags style, patterns, and potential issues. | Part 1 (D), Part 3 (Frontend URLs & Local Dev) | **D** (truemotive-desktop repo quality), **C** (docker-compose code) |
| 5 | **circuit-breaker-pattern** | Implements resilient fault-tolerance for microservices and API calls. | Part 1 (C), Part 4 (Essential Tools & Services) | **C** (S3/R2, Prometheus/Grafana, docker-compose infra) |
| 6 | **cloud-cost-management** | Monitors and optimizes cloud spending, integrates with billing and usage metrics (Prometheus-compatible). | Part 1 (C), Part 4 (Essential Tools & Services) | **C** (Prometheus/Grafana cost dashboards) |
| 7 | **dependency-management** | Handles project-wide dependency updates, conflict resolution, and lockfile maintenance. | Part 1 (D), Part 2 (Docker Compose Stacks) | **D** (mediamesh compose-stack dependency mapping), **C** (docker-compose service deps) |
| 8 | **error-tracking** | Captures and reports application errors, integrates with Sentry/Prometheus-style pipelines. | Part 1 (C), Part 4 (Essential Tools & Services) | **C** (S3/R2 error logs, Grafana alerts) |
| 9 | **vercel-optimize** | Audits a Vercel project for cost, performance, reliability, caching, function usage, and billing. | Part 3 (Frontend URLs & Local Dev), Part 4 (Essential Tools & Services) | **C** (performance metrics), **3-L** (local URL optimization) |
| 10 | **react-best-practices** | 40+ rules across 8 categories (bundle size, data fetching, re-renders, etc.) for React/Next.js. | Part 3 (Frontend URLs & Local Dev), Part 5 (Handy Commands & Shortcuts) | **3-A** (React component guidelines), **5-S** (common npm/yarn shortcuts) |
| 11 | **web-design-guidelines** | Audits UI code for 100+ rules covering accessibility, performance, typography, dark-mode, touch, i18n, etc. | Part 1 (D), Part 3 (Frontend URLs & Local Dev) | **D** (truemotive-desktop UI consistency), **3-G** (accessibility & theming) |
| 12 | **writing-guidelines** | Audits documentation for 80+ rules on voice, structure, code samples, typography, AI-workflow, pricing pages. | Part 6 (TODO & Onboarding), Part 1 (E) | **E** (skill-tracking docs), **6-F** (onboarding checklists) |
| 13 | **react-native-guidelines** | 16 rules across 7 sections for React-Native/Expo performance, layout, animation, state-management, platform patterns. | Part 3 (Frontend URLs & Local Dev), Part 5 (Handy Commands & Shortcuts) | **3-H** (mobile-friendly URLs), **5-C** (expo-CLI shortcuts) |
| 14 | **react-view-transitions** | Implements smooth page transitions using React's View Transition API for Next.js App Router. | Part 3 (Frontend URLs & Local Dev), Part 5 (Handy Commands & Shortcuts) | **3-I** (transition-aware URL routing), **5-V** (keyboard-shortcut cheat-sheet) |
| 15 | **composition-patterns** | Avoids boolean-prop proliferation via compound components, state-lifting, and internal composition. | Part 3 (Frontend URLs & Local Dev), Part 2 (Docker Compose Stacks) | **3-J** (component-composition for URL-driven UI), **2-A** (service-level composition) |
| 16 | **deploy-to-vercel** | Deploys applications/websites to Vercel via git-push, CLI, or temporary (`--temporary`) deployments. | Part 3 (Frontend URLs & Local Dev), Part 2 (Docker Compose Stacks) | **3-K** (preview-deployment URLs), **2-B** (docker-compose ↔ Vercel parity) |

\* **Section references** use the Part 1 label scheme (A-F) plus the part-specific sub-labels (3-A, 5-S, etc.) that the interview uses to locate the discussion point.

**Part 1 sections:**
- **A** – Postgres, Supabase, firenook
- **B** – (skipped)
- **C** – S3/R2, Prometheus/Grafana, docker-compose, gh CLI (read-only)
- **D** – mediamesh compose stack, truemotive-desktop (most important repo)
- **E** – skill-tracking across agents via `npx skillkit`
- **F** – Tailscale turbo-1, mediamesh/TrueMotive Production Center placeholders

**Other parts reference:**
- **Part 2** = Docker Compose Stacks
- **Part 3** = Frontend URLs & Local Development
- **Part 4** = Essential Tools & Services
- **Part 5** = Handy Commands & Shortcuts
- **Part 6** = TODO & Onboarding

### Interview Format Reference
- **1-5**: Options 1-4 are suggested/Recommended choices, Option 5 is free text response
- **F**: Free text response (always available)
- **Double asterisks (**)**: Out-of-band hints tracked in AGENTS.md
- **PMA tone**: Positive mental attitude with emojis, balanced (not excessive)