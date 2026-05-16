# 🚀 AzoDesk: The Autonomous Terminal Engineering Agent

<div align="center">

[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg?style=for-the-badge)](https://azodesk.com)
[![Node](https://img.shields.io/badge/Node-%3E=20.0.0-green.svg?style=for-the-badge)](https://nodejs.org)
[![License](https://img.shields.io/badge/License-MIT-purple.svg?style=for-the-badge)](https://github.com/chaudaryglobal/azodesk/blob/main/LICENSE)
[![Website](https://img.shields.io/badge/Official-azodesk.com-orange.svg?style=for-the-badge)](https://azodesk.com)

**Experience the future of development where the terminal isn't just a tool—it's your senior engineer partner.**

[Overview](#-overview) • [The Autonomous Engine](#-the-autonomous-engine) • [Installation](#-installation) • [Configuration](#-configuration) • [Command Reference](#-command-reference) • [Internal Architecture](#-architecture) • [Support](#-support-the-developer)

</div>

---

## 🌟 Overview

**AzoDesk** is the world's most advanced autonomous workspace for the terminal. It transforms standard shell environments into high-performance engineering cockpits. Unlike traditional AI assistants that merely "suggest" code, AzoDesk acts as an **Agentic Engine** that plans, executes, verifies, and self-heals your codebase in real-time.

Built for developers who demand speed, security, and absolute reliability, AzoDesk leverages multiple high-reasoning models (DeepSeek-R1, GPT-4o, Llama 3.1) to navigate complex codebases, refactor architectures, and eliminate the friction of modern software development.

---

## 🔥 The Autonomous Engine (Deep Dive)

AzoDesk is powered by a proprietary **Four-Pillar Autonomy Engine** that ensures every AI interaction is safe and successful.

### 1. 🔧 Self-Healing Execution Loop
When a command fails—be it a missing dependency, a syntax error, or a permission issue—AzoDesk doesn't stop.
- **Diagnostic Phase**: The `AutoFixService` immediately consumes the `stderr` and `stdout`.
- **Reasoning Phase**: High-reasoning models (like DeepSeek-R1) analyze the failure context.
- **Remediation Phase**: The system proposes a precise "Self-Heal" command (e.g., `npm install @types/node`).
- **Confirmation**: With your approval (or in auto-mode), it applies the fix and re-runs the original task.

### 2. ⚡ Speculative Context Retrieval
Traditional RAG is slow. AzoDesk implements a **Warm Context Buffer** that works ahead of you.
- **Predictive Indexing**: As you type or while the AI is streaming, the system speculatively loads related files into memory.
- **Latency Reduction**: This reduces the "Time-to-First-Token" by up to **40%**, making interaction feel instantaneous even on massive repositories.

### 3. 🛡️ Atomic Snapshots & Zero-Risk Rollbacks
Never fear a large refactor again.
- **Micro-Snapshots**: Before every AI-suggested modification, AzoDesk creates a lightweight snapshot of the affected files.
- **Instant Recovery**: If a command fails or you simply don't like the result, the `/rb` command triggers a **Zero-Latency Rollback**, restoring your codebase to its exact previous state.

### 4. 🔍 High-Integrity Verification Loop
Code that "looks" right isn't enough. AzoDesk enforces **Structural Integrity**.
- **Post-Change Verification**: After every modification, the system automatically runs `npx tsc --noEmit` or `npm run build`.
- **Autonomous Repair**: If the verification fails (e.g., a type mismatch), the Self-Healing Loop is triggered automatically to fix the discrepancy.

---

## 🛠️ Core Features

- **Multi-Model Orchestration**: Seamlessly switch between OpenRouter, NVIDIA AI, and local providers.
- **Skill Orchestration**: Semantic search and execution of specialized engineering skills (Docker, AWS, Performance Tuning).
- **Intelligent Task Engine**: Automatically decomposes high-level prompts into actionable execution steps.
- **Multi-Workspace Isolation**: Maintain separate AI contexts and histories for every project you work on.
- **Secure Sandbox**: Advanced command analysis blocks dangerous operations (e.g., `rm -rf /`) before they happen.
- **TUI Cockpit**: A premium, responsive Text User Interface with real-time status bars and streaming displays.

---

## 📦 Installation

AzoDesk-CLI is designed to be universal.

### 📦 npm / Bun / pnpm
```bash
# Global installation via npm
npm i -g azodesk-cli

# Fast installation via bun
bun add -g azodesk-cli
```

### 🚀 Curl (The One-Liner)
Ideal for CI/CD or fresh Linux installs:
```bash
curl -fsSL https://azodesk.com/install.sh | sh
```

### 🍺 Homebrew (macOS)
```bash
brew install azodesk/tap/azodesk-cli
```

### 🐧 Arch Linux (paru/yay)
```bash
paru -S azodesk-cli
```

---

## 🔑 API Key Setup Guide

AzoDesk is a multi-provider orchestrator. To begin, you will need an API key from at least one of the supported providers.

### 1️⃣ OpenRouter (Highly Recommended)
OpenRouter provides a single interface for over 100+ models including GPT-4o, Claude 3.5, and DeepSeek.

*   **Step 1**: Visit [openrouter.ai](https://openrouter.ai/keys).
*   **Step 2**: Sign in or create an account.
*   **Step 3**: Click on **"Create Key"** and give it a name (e.g., `AzoDesk-CLI`).
*   **Step 4**: Copy the key and run:
    ```bash
    azodesk config set openrouter_key YOUR_KEY_HERE
    ```

### 2️⃣ NVIDIA AI Foundation (Best for Speed)
NVIDIA offers high-speed access to open-weights models like Llama 3 and Mistral.

*   **Step 1**: Go to the [NVIDIA API Catalog](https://build.nvidia.com/).
*   **Step 2**: Select a model (e.g., `Meta Llama 3.1 70B`).
*   **Step 3**: Click on **"Get API Key"**.
*   **Step 4**: Copy the generated key and run:
    ```bash
    azodesk config set nvidia_key YOUR_KEY_HERE
    ```

### 3️⃣ Verifying Your Setup
Once configured, you can verify your connection to the models:
```bash
# List available models and check status
azodesk models list

# Test a specific model
azodesk models test openrouter/deepseek/deepseek-r1
```

---

## ⌨️ Command Reference

### 🚀 Global Commands
| Command | Usage |
| :--- | :--- |
| `azodesk` | Launch the Interactive TUI Cockpit |
| `azodesk ai "<prompt>"` | Execute a specific task autonomously |
| `azodesk chat` | Open a persistent chat session with the AI |
| `azodesk workspace create <name>` | Initialize a new isolated workspace |
| `azodesk models list` | See all available and tested models |
| `azodesk config show` | View current settings and API status |

### 🧭 AI Modes (`/mode`)
Fine-tune the AI's persona for your specific task:
- **`architect`**: Focuses on high-level system design and patterns.
- **`debugger`**: Specialized in stack trace analysis and error fixing.
- **`optimizer`**: Identifies bottlenecks and refactors for performance.
- **`reviewer`**: Performs security audits and code quality checks.
- **`generator`**: Rapid scaffolding and boilerplate generation.

### ⌨️ Interactive Shortcuts
- **`Ctrl + P`**: Quick Model Selection & Config
- **`Ctrl + S`**: Create a manual Snapshot
- **`Ctrl + K`**: Clear context and history
- **`Esc`**: Cancel the current AI generation or command

---

## 🏗️ Internal Architecture

AzoDesk is built on a modular, event-driven architecture designed for extreme reliability.

```
src/
├── ai/            # AI Orchestration, Prompt Engineering & Auto-Fix
├── cli/           # REPL, Handler Logic & TUI Entry Point
├── executor/      # Command Execution, Sandbox & Safety Checks
├── workspace/     # Persistence, Snapshots & Context Isolation
├── knowledge/     # Vector Service, Skills & Warm Context Buffer
├── task-engine/   # Task Decomposition & State Machines
├── ui/            # Responsive TUI Components & Renderers
└── security/      # Blocklists, Sanitization & Audit Logs
```

- **Persistence**: Workspaces are stored as atomic JSON stores at `~/.azodesk/workspaces/`.
- **Networking**: All AI communication is handled via the Provider Layer with automatic fallback and retry logic.
- **Performance**: Heavy tasks like vector indexing are offloaded to Worker Threads to keep the UI at 60fps.

---

## 🛡️ Security & Privacy

Your security is our top priority.
- **Sandbox Execution**: Commands are analyzed for high-risk patterns before execution.
- **Privacy-First**: No code is ever stored or shared by AzoDesk. Your API keys are stored locally in an encrypted-at-rest configuration.
- **Full Transparency**: Every autonomous action requires confirmation (unless you explicitly enable `autoConfirm`).

---

## 🤝 Support the Developer

> **"Development is a relentless pursuit of the impossible. AzoDesk was born from a vision to make that pursuit effortless. If this tool has saved you hours of debugging or empowered your creativity, your support is the fuel that keeps this engine running."**

Every donation helps me maintain the infrastructure, integrate new cutting-edge models, and keep AzoDesk open and accessible to developers worldwide.

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
**Collaborations & Business**: [ahmadabdullahchaudary@gmail.com](mailto:ahmadabdullahchaudary@gmail.com)

---

<div align="center">
Built with ❤️ by Ahmad Abdullah Chaudary.
</div>
