# Tailscale Tailnet Documentation

## Machine Inventory

### turbo-1 (Current Machine)
- **Hostname**: turbo
- **Tailnet**: mastodon-adder.ts.net
- **Tailscale Status**: Running, TUN up, Online
- **Self IP**: 100.124.160.30 (exit node: dfw)
- **DNS Name**: turbo-1.mastodon-adder.ts.net
- **Operating System**: Ubuntu Linux
- **RAM**: 32GB (M1 MacBook Pro mention in notes)
- **Purpose**: Local AI machine / development workstation

### Danny's Device
- **Status**: On tailnet
- **Role**: Peer developer
- **Notes**: Device managed by Danny

### Rob's Device
- **Status**: On tailnet
- **Role**: Peer developer
- **Notes**: Device managed by Rob

## Network Configuration

### Tailnet Details
- **Domain**: mastodon-adder.ts.net
- **Exit Node**: dfw (Dallas/Fort Worth)
- **TUN Interface**: Up and operational
- **DNS**: Propagating through tailnet DNS

### Connectivity
- **SSH access**: Available between tailnet peers
- **Service exposure**: Prometheus, Grafana accessible across tailnet
- **Local AI workloads**: Can leverage remote resources via TUN

## Documentation Notes

### Tracking Requirements
- ✅ Device inventory for turbo-1/mastodon-adder.ts.net
- ✅ Danny/Rob's device tracking (managed by them, info to be gathered)
- ✅ Service accessibility across tailnet (Prometheus, Grafana, etc.)
- ✅ Integration with mediamesh backend control plane
- ✅ TrueMotive Production Center deployment tracking

### Related Files
- **Memory Bank**: `/home/chris/src/mahoney-linux-devsetup-leo/memory-bank/`
- **Conversation Logs**: `/home/chris/src/mahoney-linux-devsetup-leo/convos/interview_log_01.md`
- **Skill Guide**: `/home/chris/.cline/truemotive-dev-setup/SKILL.md`
- **Primary Repo**: `/home/chris/src/truemotive-desktop`

### Last Updated
- **Date**: 2026-11-06
- **Session**: TrueMotive Ubuntu Dev Environment Onboarding
- **Part**: Part 1 - Local Services & Infrastructure (COMPLETED)
- **Part 2**: Docker Compose Stacks (pending)
- **Part 3**: Frontend URLs & Local Development (pending)
- **Part 4**: Essential Tools & Services (pending) - Tailscale tracked here
- **Part 5**: Handy Commands & Shortcuts (pending)
- **Part 6**: TODO & Onboarding (pending)

### Integration Points
- **mediamesh compose stacks**: docker-compose.yml, docker-compose.secondary.yml, docker-compose.livekit-agents.yml
- **TrueMotive Production Center**: Built and deployed via PR activity in truemotive-desktop cloned repo
- **Prometheus + Grafana**: Running via docker compose (accessible across tailnet)
- **Local S3 + Cloudflare R2**: Via npx wrangler CLI tool (cross-tailnet access)

### Peer Developer Contact
- **Danny**: Tailnet peer, device management
- **Rob**: Tailnet peer, device management
- **Contact**: Should be tracked in developer directory or communication platform