# ClaudeSquad Agents Catalog

## Agent Statistics

**Total Agents:** 75  
**Complete Agents:** 19 (25%)  
**Placeholder Agents:** 56 (75%)

## Complete Agents

These agents have full implementations with detailed documentation, expertise sections, protocols, and examples:

### Core System Agents (4)

**context-manager** - First agent activated in every session. Maintains complete project mental map, loads session memory, detects changes, provides relevant context to other agents, prevents code duplication and conflicts.

**agent-creator** - Module research specialist that reads all module files, understands code purpose and history, detects all patterns (obvious and hidden), generates dynamic agents with complete module knowledge.

**specialist-git** - Professional Git workflow specialist mastering conventional commits, branching strategies, conflict resolution, and release management.

**documentation-changelog** - Professional changelog and semantic versioning expert. Maintains project history, generates release notes, manages version numbers following industry standards.

### Engineer Agents (1)

**engineer-laravel** - Expert in Laravel 11+ and PHP 8.3+. Implements production-ready code following clean architecture (DDD, Hexagonal, CQRS), testing with Pest PHP (>90% coverage), optimization with Octane/Swoole/RoadRunner.

### Setup Agents (4)

**setup-context** - Analyzes project architecture and technology stack during initial setup.

**setup-codebase** - Examines existing codebase structure and patterns during setup.

**setup-environment** - Detects development environment configuration and tools.

**setup-infrastructure** - Analyzes deployment infrastructure and DevOps setup.

### Coordinator Agents (10)

**coordinator-backend** - Master Backend Orchestrator with complete visibility. Loads all backend modules (~100k tokens), analyzes cross-module dependencies, detects cascade effects, plans systemic migrations.

**coordinator-frontend** - Master Frontend Orchestrator with complete UI visibility. Orchestrates Design Tokens, Component Library, Core Web Vitals optimization, micro-frontends coordination, WCAG 2.1 AA compliance.

**coordinator-database** - Master Data Orchestrator with complete data architecture visibility. Orchestrates zero-downtime migrations, manages sharding/replication, handles distributed transactions, ensures 99.99% uptime.

**coordinator-devops** - Master DevOps Orchestrator with complete ecosystem visibility. Orchestrates CI/CD pipelines, manages Terraform/Kubernetes/Ansible, implements GitOps with ArgoCD/Flux, handles DevSecOps compliance.

**coordinator-infrastructure** - Master Infrastructure Orchestrator with complete cloud visibility. Orchestrates AWS/Azure/GCP/on-premise, manages Infrastructure as Code, implements zero-trust architecture, optimizes cloud costs.

**coordinator-security** - Master Security Orchestrator with complete threat landscape visibility. Orchestrates zero-trust/SASE/ZTNA enterprise-wide, manages multi-framework compliance, implements threat intelligence and hunting.

**coordinator-testing** - Master Testing Orchestrator with complete quality landscape visibility. Orchestrates unit/integration/E2E/API/performance tests, implements shift-left testing, manages AI-powered testing and self-healing tests.

**coordinator-data** - Master Data Ecosystem Orchestrator with complete visibility. Orchestrates data mesh/lakehouse/data fabric architectures, manages ETL/ELT/streaming, implements data governance and quality.

**coordinator-migration** - Master Migration Orchestrator managing complete transformations. Orchestrates monolith→microservices, on-premise→cloud, manages strangler fig/expand-contract patterns, handles zero-downtime migrations.

**coordinator-testing** - Master Testing Orchestrator with complete quality panorama visibility. Orchestrates comprehensive testing strategies across all layers and manages quality assurance processes.

## Placeholder Agents (56 agents)

These agents have basic YAML frontmatter but contain [TODO] placeholder content. They follow a standard template and need full implementation:

### Engineer Agents (Backend - 8)
engineer-fastapi, engineer-nodejs, engineer-graphql, engineer-database, engineer-billing, engineer-cms, engineer-email, engineer-notification

### Engineer Agents (Frontend - 6)  
engineer-react, engineer-vue, engineer-angular, engineer-nextjs, engineer-ui-ux, engineer-system

### Engineer Agents (Database - 7)
engineer-postgres, engineer-mysql, engineer-redis, engineer-sqlite, engineer-weaviate, engineer-postgis, engineer-search

### Engineer Agents (DevOps - 8)
engineer-git, engineer-memory, engineer-mapbox, engineer-licensing, engineer-message-queue, engineer-ml, engineer-prompt, engineer-ai-integration

### Operations Agents (9)
operations-docker, operations-debugging, operations-troubleshooter, operations-apm, operations-observability, operations-logging, operations-performance, operations-incident

### Auditor & Security Agents (5)
auditor-security, auditor-gdpr, auditor-compliance, auditor-accessibility, auditor-cost

### Testing Agents (3)
testing-automation, testing-e2e, testing-quality

### Analyst Agents (7)
analyst-business, analyst-requirements, analyst-risk, analyst-user-research, analyst-tech-stack, analyst-metrics, analyst-data-scientist

### Documentation Agents (2)
documentation-technical, documentation-clarification

### Planning & Architecture Agents (4)
planning-project, planning-roadmap, architect-cloud, architect-system

### Specialist Agents (1)
specialist-discovery

## Agent Development Guidelines

### Creating Complete Agents

To transform a placeholder agent into a complete agent, follow the engineer-laravel model:

1. **Detailed Frontmatter**: Include proper model, category, activation, and context usage
2. **Core Expertise**: Comprehensive list of domain knowledge areas
3. **Specialized Capabilities**: Specific technical skills and functions
4. **Activation Triggers**: Clear conditions for when to use the agent
5. **Input/Output Patterns**: Expected data formats and structures
6. **Integration Points**: How the agent works with other agents
7. **Memory Management**: For dynamic agents - memory loading/updating protocols
8. **Cross-Domain Protocols**: FLAGS creation and processing capabilities
9. **Examples and Use Cases**: Practical application scenarios
10. **Performance Considerations**: Token usage and optimization strategies

### Quality Standards

Complete agents must have:
- Minimum 200+ lines of detailed documentation
- Specific technical expertise (not generic descriptions)
- Clear activation criteria and usage patterns
- Integration protocols with other agents
- Practical examples and use cases

## Memory Systems Integration

### Local JSON Memory System
Located in `.claude/memory/` - used by dynamic agents for project-specific knowledge persistence.

### Global Memory Server (MCP)
Used by Claude orchestrator for cross-session and cross-project context persistence.

## FLAGS System

Agents create FLAGS in `.claude/memory/flags/pending.json` when they detect issues affecting other modules. Claude reads flags and delegates directly to appropriate agents.

## Contributing

To complete placeholder agents:
1. Choose an agent from the placeholder list
2. Research the domain thoroughly
3. Follow the engineer-laravel implementation pattern
4. Include all required sections with specific, actionable content
5. Test with realistic scenarios
6. Ensure proper integration with the FLAGS system

## File Structure

```
.claude/agents/
├── README.md (this file)
├── [19 complete agent files]
├── [8 dynamic ClaudeSquad-* agent files]  
└── [56 placeholder agent files]
```

Last updated: 2025-08-15
