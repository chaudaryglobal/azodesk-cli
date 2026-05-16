# 🚀 AzoDesk: The Elite Autonomous AI Engineering Workspace

<div align="center">

```
 █████╗ ███████╗ ██████╗ ██████╗ ███████╗███████╗██╗  ██╗
██╔══██╗╚══███╔╝██╔═══██╗██╔══██╗██╔════╝██╔════╝██║ ██╔╝
███████║  ███╔╝ ██║   ██║██║  ██║█████╗  ███████║█████╔╝ 
██╔══██║ ███╔╝  ██║   ██║██║  ██║██╔══╝  ╚════██║██╔═██╗ 
██║  ██║███████╗╚██████╔╝██████╔╝███████╗███████║██║  ██╗
╚═╝  ╚═╝╚══════╝ ╚═════╝ ╚═════╝ ╚══════╝╚══════╝╚═╝  ╚═╝
```

**"The most powerful, autonomous, and totally free AI workspace ever built for the terminal."**

[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg?style=for-the-badge)](https://azodesk.com)
[![Node](https://img.shields.io/badge/Node-%3E=20.0.0-green.svg?style=for-the-badge)](https://nodejs.org)
[![Open Source](https://img.shields.io/badge/Open%20Source-Totally%20Free-brightgreen.svg?style=for-the-badge)](https://azodesk.com)
[![License](https://img.shields.io/badge/License-MIT-purple.svg?style=for-the-badge)](https://github.com/chaudaryglobal/azodesk/blob/main/LICENSE)
[![Website](https://img.shields.io/badge/Official-azodesk.com-orange.svg?style=for-the-badge)](https://azodesk.com)

</div>

---

## 🌟 Introduction

**AzoDesk** is a production-grade, **Open Source**, and **Totally Free** autonomous terminal workspace. It is the result of a vision to bridge the gap between static code editors and the intelligence of modern AI. AzoDesk transforms your terminal into a high-performance engineering cockpit where the AI doesn't just suggest—it **acts**.

By integrating over **100+ state-of-the-art AI models** from providers like **OpenRouter** and **NVIDIA**, AzoDesk provides a unified, high-speed interface for planning, coding, testing, and self-healing. It is built by developers, for developers who live in the terminal.

---

## 🧠 The Four Pillars of Autonomy

AzoDesk is powered by a proprietary autonomous engine that handles the lifecycle of software engineering.

### 1. 🔧 Self-Healing Execution Loop
The "Plan-Code-Test" loop is fully automated. When a terminal command or a build fails:
- **Autonomous Diagnosis**: AzoDesk captures the `stderr` and uses high-reasoning models (like DeepSeek-R1) to diagnose the root cause.
- **Remediation**: It analyzes missing packages, syntax errors, or environmental issues.
- **Healing**: The system proposes a fix and, upon your confirmation, executes it immediately. It repeats this process recursively until the task is successfully completed.

### 2. ⚡ Speculative Context Retrieval (Ultra-Fast RAG)
Traditional Retrieval-Augmented Generation (RAG) often waits for the user to finish typing. AzoDesk's **Warm Context Buffer** works ahead:
- **Predictive Prefetching**: While you type your prompt or while the AI streams, the system speculatively indexes and loads related files into a memory buffer.
- **Reduced Latency**: This eliminates the wait time for context loading, reducing Time-to-First-Token by up to **40%**.

### 3. 🛡️ Atomic Snapshots & Zero-Risk Rollbacks
Autonomy should never come at the cost of stability.
- **Pre-Change Snapshots**: AzoDesk creates a micro-snapshot of your codebase before every AI-suggested modification.
- **Zero-Latency Rollback**: If an AI-driven refactor fails or introduces regressions, the `/rb` command restores your files to their exact previous state in milliseconds.

### 🔍 4. High-Integrity Verification
AzoDesk ensures that the code it generates is not only logical but also valid and buildable.
- **Structural Checks**: After every change, the system automatically runs `tsc --noEmit` and `npm run build`.
- **Auto-Fix Integration**: If verification fails, the Self-Healing Loop is triggered to fix the type errors or build issues before you even see them.

---

## 🚀 Key Features

- **100+ Models in One CLI**: Unified access to every major AI model via OpenRouter and NVIDIA.
- **Command Palette (`Ctrl + P`)**: A professional visual interface for model switching, key configuration, and skill management.
- **Autonomous Skill Orchestration**: Semantic search and execution of specialized skills (Docker, Performance, Security).
- **Secure Sandbox**: Advanced command analysis blocks dangerous operations (e.g., `rm -rf /`) before they reach your shell.
- **Smart File Tagging**: Use `@` to instantly attach specific files or directories to your AI context.
- **Multi-Workspace Isolation**: Maintain separate context, history, and models for each of your projects.
- **Premium TUI**: A responsive, 60fps terminal interface with real-time status bars and streaming displays.

---

## 📦 Installation

AzoDesk-CLI is designed to be universal and lightweight.

### 📦 npm (Recommended)
```bash
npm i -g azodesk-cli
```

### 🚀 Curl (The One-Liner)
```bash
curl -fsSL https://azodesk.com/install.sh | sh
```

### 🍺 Homebrew (macOS)
```bash
brew install azodesk/tap/azodesk-cli
```

### 🍞 Bun
```bash
bun add -g azodesk-cli
```

### 🐧 Arch Linux (paru/yay)
```bash
paru -S azodesk-cli
```

---

## 🔑 API Key Setup Guide

To unlock the power of **100+ Free and Premium Models**, follow this guide.

### 1️⃣ OpenRouter (Access 60+ Models)
OpenRouter is the recommended provider for high-reasoning tasks.
*   **Get Key**: [openrouter.ai/keys](https://openrouter.ai/keys)
*   **Configure**: Open AzoDesk → Press `Ctrl + P` → `Configure API Keys` → `OpenRouter`.
*   **Free Models**: Includes many free options like Llama 3, Mistral, and more.

### 2️⃣ NVIDIA AI Foundation (Ultra-Fast)
Perfect for rapid code generation and low-latency responses.
*   **Get Key**: [build.nvidia.com](https://build.nvidia.com/)
*   **Configure**: Open AzoDesk → Press `Ctrl + P` → `Configure API Keys` → `NVIDIA`.
*   **Direct Access**: Use high-speed NIM endpoints for Llama 3.1 and Mistral Large.

---

## ⌨️ Command Reference

### Interactive TUI Shortcuts
| Shortcut | Action |
| :--- | :--- |
| **`Ctrl + P`** | Open the Command Palette (Everything in one place) |
| **`Ctrl + K`** | Clear current chat context and history |
| **`Ctrl + S`** | Create a manual Snapshot of the current directory |
| **`Ctrl + Q`** | Show command help overlay |
| **`Ctrl + C`** | Cancel current AI stream or clear input line |
| **`Tab`** | Trigger command and file completion |
| **`Esc`** | Close palette or clear input |

### CLI Commands
| Command | Usage |
| :--- | :--- |
| `azodesk` | Launch the interactive workspace (TUI) |
| `azodesk ai "..."` | Run an autonomous goal directly from your shell |
| `azodesk chat` | Open a persistent AI chat session |
| `azodesk workspace create <name>` | Create a new isolated project context |
| `azodesk workspace list` | View all saved workspaces |
| `azodesk models list` | See all available models and provider status |
| `azodesk config show` | View current settings (keys are redacted) |

### AI Personas (`/mode`)
Switch the AI's specialty on the fly:
- **`architect`**: High-level system design and software patterns.
- **`debugger`**: Root-cause analysis and automated fixing.
- **`optimizer`**: Performance tuning and code refactoring.
- **`reviewer`**: Security audits and code quality reviews.
- **`generator`**: Rapid scaffolding and boilerplate generation.
- **`teacher`**: Deep explanations and learning-oriented guidance.

---

## 🏗️ Architecture & Internals

AzoDesk is built with a modular, scalable architecture using **Node.js 20+** and **TypeScript**.

```
src/
├── ai/            # Orchestrator, Auto-Fix Service & Prompts
├── cli/           # Handler Logic, REPL & TUI Core
├── executor/      # Command Execution, Sandbox & Safety
├── workspace/     # Persistence, Snapshots & Isolation
├── knowledge/     # Vector Service, Skills & Warm Buffer
├── task-engine/   # Plan Decomposition & Execution Logic
├── ui/            # Ink/React Components & Renderers
├── security/      # Blocklists & Privacy Scrubbing
└── router/        # Model Selection & Fallback Logic
```

- **Persistence Layer**: Data is stored atomically at `~/.azodesk/`.
- **Vector Engine**: Uses local embeddings for semantic skill discovery.
- **Isolation**: Each workspace has its own SQLite/JSON store for history and context.

---

## 🛡️ Security & Privacy

AzoDesk is designed for professional environments where security is non-negotiable.
- **Safety Sandbox**: Every command is analyzed for dangerous patterns (e.g., recursive deletes, system modifications) before execution.
- **Privacy Scrubbing**: AI prompts are optionally scrubbed for sensitive data like tokens and secrets before being sent to providers.
- **Full Transparency**: AzoDesk never performs a destructive action without your explicit confirmation (unless you choose to enable `autoConfirm`).

---

## 🤝 Support the Developer

> **"Development is a journey that thrives on community and passion. AzoDesk is my contribution to the global developer community—a tool that I built to be totally free and open for everyone. If AzoDesk has empowered your workflow, please consider supporting the project to help me keep it at the cutting edge."**

Your support helps me maintain the infrastructure, integrate new models, and continue building the future of autonomous engineering.

### 💰 Crypto Donations
- **Bitcoin (BTC)**: `bc1qr5tdgwpp0lfsug3fddjmqlsyp3jgmurcsu4lmk`
- **Ethereum (ETH)**: `0xFaC4283cBbb72B1c7bab5aea03868e8b7f506c07`
- **BNB (BEP20)**: `0xFaC4283cBbb72B1c7bab5aea03868e8b7f506c07`

### 💳 Digital Payments
- **PayPal**: [paypal.me/ahmad4572](https://paypal.me/ahmad4572)
- **Payoneer**: `ahmadabdullahchaudary@gmail.com`
- **Binance ID**: `573493421`

---

## 📩 Contact & Collaboration

**Lead Developer**: Ahmad Abdullah Chaudary  
**Official Website**: [azodesk.com](https://azodesk.com)  
**Support Email**: [chaudaryglobal@gmail.com](mailto:chaudaryglobal@gmail.com)  
**Collaborations**: [ahmadabdullahchaudary@gmail.com](mailto:ahmadabdullahchaudary@gmail.com)

---

<div align="center">
Built with ❤️ by Ahmad Abdullah Chaudary for the future of engineering.
</div>
