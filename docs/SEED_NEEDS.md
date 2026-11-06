# Ubuntu Dev Setup Notes

## System
- Distro / version: Ubuntu
- Install date: 

## Shell & Terminal
- Shell (bash/zsh/fish): 
- Terminal emulator: 
- Dotfiles repo: 

## Core Tools
- Git config (name/email/editor): Chris Mahoney / chris.p.mahoney@gmail.com / code
- Editor / IDE: 
- Node / Python / Rust versions: 
- Package managers: 

## Ubuntu Packages
- build-essential - Essential build tools
- curl - Transfer data from/to server
- wget - Download files from web
- git - Version control system
- zsh - Shell
- tmux - Terminal multiplexer
- htop - Process viewer
- vim - Text editor
- nano - Simple text editor
- sqlite3 - Database command line tool
- redis-server - In-memory data structure store
- postgresql - Object-relational database system
- docker.io - Docker engine
- docker-compose - Docker compose tool
- npm - Node.js package manager
- pnpm - Performant npm package manager
- nodejs - Node.js runtime
- python3 - Python programming language
- pip - Python package installer
- rustc - Rust compiler
- cargo - Rust package manager
- golang-go - Go programming language
- openjdk-21-jdk - Java development kit
- android-studio - Android development IDE
- postman - API testing tool
- insomnia - API client
- visual-studio-code - Code editor
- net-tools - Network tools (ifconfig, netstat, etc.)
- avahi-daemon - mDNS/DNS-SD daemon
- avahi-discover - Service discovery
- libnss-mdns - mDNS name resolution
- rsync - Fast file transfer tool
- unzip - Decompress zip files
- tar - Archive tool
- gzip - Compression tool
- zip - Compress files
- sudo - Execute as superuser
- libssl-dev - SSL development libraries
- pkg-config - Compile flags and library paths
- libffi-dev - Foreign function interface library
- python3-dev - Python development headers
- virtualenv - Python virtual environment tool
- pipenv - Python dependencies manager
- yarn - JavaScript package manager
- pnpm-setup
- pnpm-bootstrap
- pnpm-sync
- pnpm-filter
- pnpm-duplicate
- pnpm-import
- pnpm-export
- pnpm-build
- pnpm-test
- pnpm-docs
- pnpm-website
- pnpm-design
- pnpm-i18n
- pnpm-accessibility
- pnpm-security
- pnpm-performance
- pnpm-monitor
- pnpm-debug
- pnpm-profile
- pnpm-trace
- pnpm-inspect
- pnpm-playground
- pnpm-workspace
- pnpm-set
- pnpm-store
- pnpm-bin
- pnpm-clean
- pnpm-reset
- pnpm-upgrade-interactive
- pnpm-dedupe
- pnpm-uninstall
- pnpm-replace
- pnpm-edit
- pnpm-view
- pnpm-add
- pnpm-create
- pnpm-init
- pnpm-import

## Productivity
- Window manager / DE tweaks: 
- Keyboard shortcuts: 
- Browser + extensions: 

## Development Tooling
- Node.js version management: nvm, fnm, or volta
- Python version management: pyenv
- Go version management: goenv or goro
- Rust toolchain: rustup
- Docker and Docker Compose
- Kubernetes tools: kubectl, helm
- Infrastructure as Code: terraform, ansible
- Git tools: gitui, delta, fzf-git
- Code quality: eslint, prettier, black, ruff, hadolint
- Testing: jest, pytest, playwright
- Container registry: docker, crane, regctl
- Package managers: npm, pnpm, pip, pipenv, cargo, go
- IDE/Editor setup: vscode settings, vimrc, spacemacs config
- Dotfiles management: stow, rcm, chezmoi

## Environment Scripts and Automation
- Shell initialization: .bashrc, .zshrc, .profile aliases and functions
- Path management: PATH configuration, local bin scripts
- Environment loading: direnv, contact, or similar tools
- Project scaffolding: init scripts for new TrueMotive projects
- Docker compose startup: scripts for mediamesh and other stacks
- Service management: start/stop/restart scripts for databases, caches, services
- Backup automation: scheduled backups for postgres, redis, configurations
- Update scripts: pnpm upgrade, npm audit fix, security patches
- Cleanup scripts: log rotation, temp file cleanup, package cache cleanup
- Deployment scripts: CI/CD pipeline triggers, release automation
- Monitoring scripts: health checks, status reporting, alerting scripts

## Handy Commands
- 

## TODO
- [x] Initialize GitHub remote connection
- [x] Add repository tracking for truemotive-desktop and truemotive-web
- [x] Document Ubuntu package requirements
- [x] Configure development tooling
- [x] Set up environment scripts and automation

---
# TrueMotive Ubuntu Dev Environment Seed

## Author
- **Chris Mahoney** - Customer Zero / Founder, TrueMotive

## SCM Configuration
- **Platform**: GitHub
- **Organization**: chrismahoney
- **Authentication**: OAuth preferred, or GitHub Classic Token with proper scope
- **Access**: All repos accessible via configured credentials

## Repositories (Currently in Development)
### chrismahoney / truemotive-desktop
- Target: TrueMotive desktop application environment setup
- Status: In development

### chrismahoney / truemotive-web
- Target: TrueMotive web application environment setup
- Status: In development

## Local Setup Tracking
This repository tracks Ubuntu development environment setup for TrueMotive turnkey development. Content is managed in `docs/SEED_NEEDS.md` for easy reference and version control.

### Repository Tracking (Added for Version Control)
- **chrismahoney / truemotive-desktop**
  - Target: TrueMotive desktop application environment setup
  - Status: In development - most important repo (package.json modified)
  - Last activity: Oct 12, 2025
  - Modified: package.json changed, not yet committed

- **chrismahoney / truemotive-web**
  - Target: TrueMotive web application environment setup
  - Status: In development
  - Last activity: Checked against remote origin