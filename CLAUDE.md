# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This project deploys a Dockerized API to AWS ECR (Elastic Container Registry) via GitHub Actions. The project is initialized using the Specify framework for structured feature specification and implementation.

## Development Workflow with Specify

This repository uses [Specify](https://github.com/specifyapp/specify), a framework for systematic feature development. Specify provides slash commands accessible via `/speckit.*`:

### Key Specify Commands

- `/speckit.specify` - Create or update feature specifications from natural language descriptions
- `/speckit.plan` - Execute implementation planning workflow to generate design artifacts
- `/speckit.tasks` - Generate actionable, dependency-ordered tasks.md from design artifacts
- `/speckit.implement` - Execute implementation plan by processing tasks.md
- `/speckit.clarify` - Identify underspecified areas and ask targeted clarification questions
- `/speckit.analyze` - Perform cross-artifact consistency and quality analysis
- `/speckit.checklist` - Generate custom checklists for current feature
- `/speckit.constitution` - Create or update project constitution and principles

### Typical Feature Development Flow

1. Start with `/speckit.specify` to create a specification from a feature description
2. Use `/speckit.clarify` if requirements are unclear
3. Run `/speckit.plan` to create implementation design
4. Execute `/speckit.tasks` to generate task breakdown
5. Use `/speckit.analyze` to verify consistency across artifacts
6. Implement with `/speckit.implement`

## Project Structure

```
.specify/           # Specify framework configuration
  memory/          # Project constitution and principles
  templates/       # Templates for spec, plan, tasks, checklist
  scripts/         # Bash scripts for Specify operations
.claude/
  commands/        # Custom slash commands for Speckit integration
.github/
  workflows/       # GitHub Actions workflows (to be added for ECR deployment)
```

## Architecture

The project is being built to:
- Package an API application into a Docker container
- Deploy to AWS Elastic Container Registry (ECR)
- Automate deployment via GitHub Actions CI/CD pipeline

**Note**: The actual API application code has not been implemented yet. The repository is currently a template ready for development.

## Future Development Areas

When developing features for this project, consider:
- API framework and language selection (not yet determined)
- Dockerfile configuration for the chosen stack
- AWS ECR authentication and push workflow in GitHub Actions
- Environment-specific deployment configurations
- Health checks and monitoring for deployed containers
