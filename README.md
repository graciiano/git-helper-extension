# README.md

# DevOrbit

DevOrbit is an internal developer tooling platform for Visual Studio Code designed to optimize workflows in multi-project, monorepo, and microfrontend environments.

The extension centralizes common engineering operations directly inside VSCode, reducing repetitive terminal interactions and improving developer experience across teams.

---

# Vision

DevOrbit is designed to evolve beyond Git utilities into a complete internal developer platform integrated directly into the IDE.

The long-term goal is to provide:

* Git workflow orchestration
* workspace intelligence
* environment management
* CI/CD integrations
* developer automation
* internal engineering tooling

---

# Current Scope

Initial MVP focused on Git workflow automation using the VSCode Command Palette.

Current features:

* Repository selection
* Branch listing
* Branch search
* Pull operations
* Checkout operations
* Integrated terminal execution
* Workspace detection

---

# Installation

## VSCode Marketplace

Search for:

```txt id="0o4t57"
DevOrbit
```

inside the VSCode Extensions Marketplace.

Or install directly from the extension page.

---

# Development Setup

Clone repository:

```bash id="w73h3r"
git clone <repository-url>
```

Install dependencies:

```bash id="jlwmwz"
yarn install
```

Run extension:

```bash id="jlwmx0"
F5
```

This opens a new Extension Development Host window.

---

# Architecture

DevOrbit follows a scalable modular architecture designed for long-term platform evolution.

```txt id="jlwmx1"
src/
├── commands/
├── services/
├── providers/
├── repositories/
├── storage/
├── ui/
├── config/
├── constants/
├── types/
└── utils/
```

---

# Core Principles

* Scalable internal tooling
* Separation of concerns
* Modular architecture
* Workspace-aware operations
* Cross-project orchestration
* Developer experience first

---

# Technologies

* TypeScript
* VSCode Extension API
* Node.js
* simple-git

---

# Commands

## Current Commands

| Command                     | Description                                   |
| --------------------------- | --------------------------------------------- |
| DevOrbit: Pull Repository   | Pull selected branch from selected repository |
| DevOrbit: Checkout Branch   | Checkout selected branch                      |
| DevOrbit: Fetch Branches    | Fetch remote branches                         |
| DevOrbit: Select Repository | Select active repository                      |

---

# Workflow Example

## Pull Branch

1. Open Command Palette
2. Run:

```txt id="jlwmx2"
DevOrbit: Pull Repository
```

3. Select repository
4. Select branch
5. DevOrbit executes:

   * checkout
   * pull

---

# Planned Features

## v0.2

* Favorite repositories
* Favorite branches
* Recent branches
* Persistent state

## v0.3

* Sidebar Tree View
* Repository explorer
* Branch status indicators

## v0.4

* Automatic workspace discovery
* Multi-root workspace support
* Monorepo intelligence

## v0.5

* Pull all repositories
* Batch operations
* Workspace synchronization

## v1.0

* CI/CD integrations
* Jira integration
* Git platform integrations
* Environment tooling
* Internal developer portal

---

# Development Guidelines

## Architectural Rules

### Commands

Responsible only for:

* user interaction
* workflow orchestration

### Services

Responsible for:

* Git operations
* business logic
* workflow rules

### Providers

Responsible for:

* VSCode APIs
* terminal integration
* workspace integration

### Storage

Responsible for:

* persistent state
* favorites
* workspace data

---

# Commit Convention

DevOrbit follows Conventional Commits.

## Examples

```txt id="jlwmx3"
feat(git): add branch quick pick
fix(terminal): prevent duplicated terminals
refactor(commands): extract pull workflow
docs(readme): update installation guide
```

---

# Branch Strategy

```txt id="jlwmx4"
main
develop
feature/*
fix/*
release/*
```

Examples:

```txt id="jlwmx5"
feature/branch-picker
fix/workspace-detection
release/v0.1.0
```

---

# Versioning Strategy

DevOrbit follows Semantic Versioning.

```txt id="jlwmx6"
MAJOR.MINOR.PATCH
```

Examples:

* `0.1.0` → new feature
* `0.1.1` → bug fix
* `1.0.0` → stable platform release

---

# Marketplace Publishing

## Install VSCE

```bash id="jlwmx7"
npm install -g @vscode/vsce
```

---

## Login

```bash id="jlwmx8"
vsce login <publisher-name>
```

---

## Generate VSIX

```bash id="jlwmx9"
vsce package
```

---

## Publish Extension

```bash id="jlwmxa"
vsce publish
```

Version bump options:

* patch
* minor
* major

Example:

```bash id="jlwmxb"
vsce publish minor
```

---

# Internal Usage

DevOrbit is intended for engineering teams working with:

* monorepos
* microfrontends
* submodules
* multi-repository environments
* internal tooling ecosystems

---

# Long-Term Direction

DevOrbit aims to become a centralized engineering platform embedded directly inside VSCode, enabling teams to manage development workflows, environments, repositories, and operational tooling from a unified interface.

---

# License

Public Use
