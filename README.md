# 🚀 ClaudeSquad - The ONLY Multi-Agent System with Dual Persistent Memory

> Transform Claude Code into an intelligent development team with **DUAL MEMORY SYSTEMS** that persist across sessions - a unique feature no other agent system offers. 85+ specialized agents with true knowledge retention.

[![Memory](https://img.shields.io/badge/Dual%20Memory-Persistent-red)](./.claude/memory)
[![Agents](https://img.shields.io/badge/Agents-85+-green)](./.claude/agents)
[![Commands](https://img.shields.io/badge/Commands-9-yellow)](./.claude/commands)
[![Status](https://img.shields.io/badge/Status-Active%20Development-brightgreen)](https://github.com/unmasSk/ClaudeSquad)
[![Setup](https://img.shields.io/badge/Setup-Automated-orange)](./.claude/commands/setup.md)

## 🧠 What Makes ClaudeSquad UNIQUE?

### 🔥 THE GAME CHANGER: Dual Persistent Memory System

**No other Claude Code agent system has this.** ClaudeSquad implements TWO complementary memory systems that make agents truly intelligent:

1. **MCP Memory Server** - Global knowledge graph that persists FOREVER across all sessions
2. **JSON Memory System** - Project-specific knowledge versioned with your code

This means:
- ✅ Agents remember EVERYTHING between conversations
- ✅ No more repeating context every session
- ✅ Cumulative learning that improves over time
- ✅ Project knowledge that travels with your repo
- ✅ Cross-project intelligence sharing

**Coming Soon:** RAG (Retrieval-Augmented Generation) integration for unlimited memory scaling.

### Additional Power Features

- **85+ Specialized Agents** - Domain experts from Laravel to React, PostgreSQL to Kubernetes
- **Dynamic Module Agents** - Automatically created for YOUR project's specific modules
- **Professional Commands** - `/commit`, `/pr`, `/issue`, `/docs` for Git workflow automation
- **FLAGS Coordination** - Automatic cross-domain issue detection and resolution
- **Voice Notifications** - Spanish TTS with personalized completion messages

## ⚡ Quick Start

```bash
# 1. Clone repository
git clone https://github.com/unmasSk/ClaudeSquad.git
cd ClaudeSquad

# 2. Install globally (Windows)
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude"
Copy-Item ".\.claude\*" "$env:USERPROFILE\.claude\" -Recurse -Force

# 2. Install globally (Mac/Linux)
mkdir -p ~/.claude
cp -r .claude/* ~/.claude/

# 3. Navigate to your project
cd /path/to/your/project

# 4. Run setup
claude /setup
```

## 🎮 Professional Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `/setup` | Initialize ClaudeSquad for your project | `claude /setup` |
| `/commit` | Intelligent commits with multi-agent analysis | `claude /commit --no --push` |
| `/pr` | Create pull requests with automated descriptions | `claude /pr` |
| `/issue` | GitHub issue management with templates | `claude /issue "bug description"` |
| `/docs` | Update module documentation | `claude /docs [module]` |
| `/save` | Save session context to memory | `claude /save --all` |
| `/todo` | Manage persistent project todos | `claude /todo "new task"` |
| `/agent-health` | Check dynamic agent accuracy | `claude /agent-health [module]` |
| `/tts` | Text-to-speech notifications | `claude /tts "Hello world"` |

[Detailed command documentation](./.claude/commands/README.md)

## 🏗️ System Architecture

```
Claude (Orchestrator)
    │
    ├── Global Specialists (~/.claude/agents/)
    │   ├── Engineers: Laravel, FastAPI, React, Vue, Node.js
    │   ├── Database: PostgreSQL, MySQL, Redis, SQLite
    │   ├── DevOps: Docker, Kubernetes, CI/CD
    │   ├── Testing: E2E, Performance, Security
    │   └── Coordinators: Backend, Frontend, Database
    │
    └── Dynamic Module Agents (project/.claude/agents/)
        ├── api-agent (knows YOUR API)
        ├── auth-agent (knows YOUR auth)
        └── [auto-created for your modules]
```

## 🧠 Dual Memory Systems

### 1. JSON Memory (Project-Local)
- Git-versioned with your project
- Module-specific knowledge
- FLAGS for cross-domain coordination

### 2. MCP Memory Server (Global)
- Persists between ALL Claude sessions
- Knowledge graph with relationships
- Project context preservation

## 🚀 Usage Examples

### Intelligent Development
```bash
"Build user authentication with OAuth2"
# Claude automatically:
# → Analyzes your project structure
# → Creates auth-agent with module knowledge
# → Implements with engineer-laravel
# → Reviews with security-auditor
```

### Git Workflow Automation
```bash
# Smart commits with analysis
claude /commit

# Create PR with auto-description
claude /pr

# Report issues with templates
claude /issue "Login fails after timeout"
```

### Cross-Domain Problem Solving
```bash
"The checkout is slow"
# → api-agent finds N+1 queries
# → Creates FLAG for database-agent
# → database-agent optimizes queries
# → Result: 500ms → 15ms (33x faster)
```

## 📦 Available Agents (Sample)

### ✅ Complete (13)
- `engineer-laravel` - Laravel 11+ with modern patterns
- `specialist-git` - Git workflow automation
- `agent-creator` - Dynamic agent generator
- `context-manager` - Project memory coordination
- All coordinator agents (backend, frontend, database, etc.)

### 🚧 In Development (72+)
- Backend: FastAPI, Node.js, GraphQL, Django
- Frontend: React, Vue, Angular, Next.js
- Database: PostgreSQL, MySQL, MongoDB
- DevOps: Docker, Kubernetes, Terraform
- Testing: E2E, Performance, Security

[Full agent catalog](./.claude/agents/README.md)

## 📊 What Gets Configured

When you run `/setup`:

1. **Environment Verification** - Checks tools and dependencies
2. **Project Analysis** - 4 agents analyze your codebase in parallel
3. **Language Preferences** - Configure interaction languages
4. **CLAUDE.md Generation** - Project-specific instructions
5. **Dynamic Agents** - Creates module-specific agents
6. **FLAGS System** - Cross-domain communication
7. **Memory Systems** - Both JSON and MCP configured

## 🎯 Benefits Over Standard Claude Code

| Feature | Claude Code | ClaudeSquad |
|---------|------------|-------------|
| Agents | Single AI | 85+ specialists |
| Memory | Session only | Persistent dual-system |
| Git Workflow | Manual | Automated commands |
| Module Knowledge | Generic | Project-specific agents |
| Coordination | Manual | Automatic FLAGS |
| Parallelism | Limited | 10 agents simultaneously |

## 📈 Project Status & Roadmap

### Current Status
```
[████████████░░░░░░░] 40% Complete

✅ Dual Memory Systems   ✅ FLAGS System
✅ Setup Command         ✅ Git Commands  
✅ MCP Integration       ✅ 13 Core Agents
🚧 72+ Agent Development
🚧 Testing Framework
```

### 🚀 Actively Under Development

This project is **continuously evolving** with regular updates:

- **Weekly**: New agent implementations
- **Monthly**: Major feature releases
- **Q1 2025**: RAG integration for unlimited memory
- **Q2 2025**: VS Code extension
- **Q3 2025**: Cloud synchronization

Watch/Star this repo to stay updated!

## 🤝 Contributing

Key areas for contribution:
- **Agent Development** - Complete placeholder agents using engineer-laravel as template
- **Testing** - Comprehensive test coverage
- **Documentation** - Improve agent documentation
- **Templates** - Language-specific agent templates

## 📚 Documentation

- [Commands Reference](./.claude/commands/README.md)
- [Agent Catalog](./.claude/agents/README.md)
- [FLAGS System](./.claude/docs/flags-system.md)
- [Memory Systems](./.claude/docs/memory-system-real.md)
- [Setup Documentation](./.claude/commands/setup.md)

## 🙏 Acknowledgments

- Anthropic team for Claude Code
- [@disler](https://github.com/disler) for TTS inspiration
- Community contributors

## 📜 License

MIT License - Free for commercial and personal use

---

⭐ **Star this repo if you find it useful!**

**Transform your Claude Code into a complete development team today!** 🚀