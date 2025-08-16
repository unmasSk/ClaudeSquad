# 📚 ClaudeSquad Commands

Professional command suite for enhanced Claude Code workflows.

## 🎯 Available Commands

| Command | Description | Parameters |
|---------|-------------|------------|
| `/agent-health` | ❤️‍🩹 Check health of dynamic agents | `[module]` `--report` |
| `/commit` | 📝 Create git commits with analysis | `--no` `--push` |
| `/docs` | 📖 Update module documentation | `[module]` `--check` |
| `/issue` | 🪲 Manage GitHub issues | `["error description"]` |
| `/pr` | 🔀 Create pull request with analysis | none |
| `/save` | 💾 Save session context to memory | `--all` |
| `/setup` | 🚀 Setup project with ClaudeSquad agents | `--update` |
| `/todo` | 📅 Manage project TODOs | `["task description"]` `--list` |
| `/tts` | 🎙️ Instant TTS with ElevenLabs | `[text to speak]` |

## 📋 Command Details

### `/agent-health`
Analyzes the health and drift of dynamic agents. Delegates to `agent-health-monitor` to preserve context.
- No params: Check all dynamic agents
- `[module]`: Check specific module agent
- `--report`: Show status table without scanning

### `/commit`
Intelligent commit system with linting, multi-agent analysis, and changelog generation.
- Default: Full process with confirmations
- `--no`: Fast mode, skip linting and analysis
- `--push`: Auto-push to remote after commit

### `/docs`
Updates module documentation using module-specific agents.
- No params: Show available modules
- `[module]`: Update specific module docs
- `--check`: Verify documentation status

### `/issue`
GitHub issue management with intelligent categorization.
- No params: List open issues
- `["description"]`: Create new issue with error analysis

### `/pr`
Creates pull requests with automated branch management and description generation.
- Analyzes changes across modules
- Generates structured PR description
- Auto-detects labels and suggests reviewers

### `/save`
Saves session context for persistence between conversations.
- Default: Save to Memory Server + SESSIONS/ folder
- `--all`: Additionally create Trello card

### `/setup`
Initializes or updates ClaudeSquad agent system for projects.
- Default: Complete setup for new projects
- `--update`: Update existing setup with new modules

### `/todo`
Manages persistent todos in `todos.md` file at project root.
- `["task"]`: Add new todo task
- `--list`: Show all pending tasks

### `/tts`
Text-to-speech using ElevenLabs API with Leonidas voice.
- Instant playback of any text
- Supports multiple languages
- Saves to `temp_tts_audio.mp3`

## 🚀 Quick Start

1. **Initial Setup**: Run `/setup` to configure agents for your project
2. **Daily Work**: Use `/todo` to manage tasks
3. **Commits**: Use `/commit` for intelligent git commits
4. **Documentation**: Keep docs updated with `/docs [module]`
5. **Save Progress**: Use `/save` before ending sessions

## 🔧 Configuration

Commands can be customized by editing their `.md` files in this directory. Each command file contains:
- Frontmatter with command name and description
- Detailed implementation instructions
- Usage examples and workflows

## 🎯 Best Practices

1. **Use `/save` regularly** to preserve context between sessions
2. **Run `/agent-health` weekly** to maintain agent accuracy
3. **Prefer `/commit` over manual commits** for better consistency
4. **Document changes with `/docs`** after major updates
5. **Track work with `/todo`** for team visibility

## 🔗 Integration

These commands integrate with:
- **Memory Server MCP**: Persistent storage across sessions
- **GitHub CLI**: Issue and PR management
- **Trello API**: Task tracking and memory cards
- **ElevenLabs API**: Text-to-speech functionality
- **Git Server MCP**: Enhanced git operations

## 📝 Creating Custom Commands

To add a new command:

1. Create `command-name.md` in this directory
2. Add frontmatter:
   ```yaml
   ---
   command: command-name
   description: 🎯 Short description. Params: [param1] --flag
   ---
   ```
3. Document the command behavior and implementation

---

*Part of the ClaudeSquad professional development ecosystem*