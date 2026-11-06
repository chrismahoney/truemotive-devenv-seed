# Skill Tracking Documentation

## npx Skillkit Coordination

### Current Setup
- **Tool**: npx skillkit
- **Version**: 1.7.11 (from hosts.json)
- **Local Host**: turbo (ID: f5ab55a0-7e25-44d4-aa36-eb31c0585e84)
- **Local Host Port**: 9876
- **Discovery Enabled**: true

### Agent Coordination

#### Claude Code
- **Status**: Active agent in turnkey dev environment
- **Skills**: Academy guide, algorithmic art, brand guidelines, canvas design
- **Skillkit locations**:
  - `~/.claude/skills/academy-guide/.skillkit.json`
  - `~/.claude/skills/algorithmic-art/.skillkit.json`
  - `~/.claude/skills/brand-guidelines/.skillkit.json`
  - `~/.claude/skills/canvas-design/.skillkit.json`

#### Cline (This Agent)
- **Status**: Active coordination partner
- **Skills**: Part 1-6 interview series completion
- **Current focus**: Dev environment onboarding documentation

#### Qwen Code
- **Status**: Part of the agent coordination triad
- **Skills**: Yet to be fully documented in skillkit format

### Skillkit Structure

#### Skill Discovery
- Skills stored in `~/.claude/skills/` directory
- Each skill has `.skillkit.json` metadata file
- Skills can be: academy-guide, algorithmic-art, brand-guidelines, canvas-design, etc.

#### Skill Installation
- Via npx skillkit command
- Skills versioned and tracked per-agent
- Discovery enabled for cross-agent coordination

#### Current Skill Inventory

| Skill Area | Claude Code | Cline | Qwen Code | Status |
|------------|-------------|-------|-----------|--------|
| Dev Environment Onboarding | ✅ Part 1 COMPLETED | ✅ Part 1 COMPLETED | - | Shared |
| Docker Compose Stacks | - | - | - | Part 2 pending |
| Frontend URLs & Local Dev | - | - | - | Part 3 pending |
| Essential Tools & Services | - | - | - | Part 4 pending |
| Handy Commands & Shortcuts | - | - | - | Part 5 pending |
| TODO & Onboarding | ✅ SEED_NEEDS.md complete | ✅ SEED_NEEDS.md complete | - | Repository tracking |

### v1 Checkpoint Requirements

Based on `/home/chris/.cline/truemotive-dev-setup/SKILL.md` gap analysis:

1. **npx skillkit setup for v1**
   - [ ] Installable skills for turnkey dev environment
   - [ ] Minimum skill set defined across agents
   - [ ] Skill discovery and versioning working

2. **Agent Coordination**
   - [ ] Claude Code, Cline, Qwen Code skill sets aligned
   - [ ] Cross-agent skill discovery operational
   - [ ] Skillkit configuration standardized

3. **Turnkey Dev Environment**
   - [ ] Single-command onboarding via skillkit
   - [ ] All essential services configured
   - [ ] Docker compose stacks integrable via skills

4. **Repository Tracking**
   - [ ] truemotive-desktop status verified
   - [ ] mediamesh integration documented
   - [ ] Skillkit ↔ repo synchronization working

### Gap Analysis (from SKILL.md v1 Checkpoint)

| Area | Current Status | v1 Target | Action Needed |
|------|---------------|-----------|---------------|
| skillkit.yaml config | `.skillkit/` directory exists, no yaml | Standardized config file | Create skillkit.yaml |
| Cross-agent discovery | Partially (hosts.json tracked) | Full discovery across all agents | Enable/configure discovery |
| Minimum skill set | Onboarding skills (Part 1) | Full turnkey skill set | Define v1 minimum skills |
| Skill versioning | hosts.json version 1.7.11 | Semantic versioning | Implement version tracking |
| Onboarding automation | SEED_NEEDS.md TODO complete | One-command setup | Create init scripts |

### Integration Points

#### With truemotive-desktop
- Skills can trigger PR-based deployments
- Docker compose stack integration via skill commands
- Repository status checking and sync

#### With mediamesh
- Backend control plane skills
- Docker compose stack management
- Service startup/shutdown orchestration

#### With Tailscale
- Cross-tailnet skill execution
- Remote service access via tailnet
- Danny/Rob's machines coordinatable

### Next Steps

1. **Standardize skillkit.yaml** at project root
2. **Define v1 minimum skill set** across all three agents
3. **Enable cross-agent discovery** and skill sharing
4. **Create onboarding script** that runs `npx skillkit init`
5. **Document skill inventory** per agent in this file
6. **Integrate with SEED_NEEDS.md** tracking for complete dev environment

### Reference Files

- **Skillkit config**: `/home/chris/.skillkit/hosts.json`
- **Agent skills**: `~/.claude/skills/*/.skillkit.json`
- **Interview guide**: `/home/chris/.cline/truemotive-dev-setup/SKILL.md`
- **SEED_NEEDS.md**: `/home/chris/src/mahoney-linux-devsetup-leo/docs/SEED_NEEDS.md`
- **Interview log**: `/home/chris/src/mahoney-linux-devsetup-leo/convos/interview_log_01.md`
- **Tailscale docs**: `/home/chris/src/mahoney-linux-devsetup-leo/convos/tailscale_tailnet_doc.md`