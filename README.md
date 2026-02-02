# Apple Engineering Playbook (Agent Skill)

The Source of Truth for modern Apple development — iOS 18.4+, Swift 6.2, and Liquid Glass adoption.
This skill is based on "secret" Apple markdown documentation found within Xcode's AI assistant resources (e.g., `/Xcode.app/Contents/PlugIns/IDEIntelligenceChat.framework/Versions/A/Resources/AdditionalDocumentation`), which details new features and is used by Xcode Intelligence.

This repository contains an expert-level AI Skill based on Apple’s internal implementation standards and AI-first documentation. It equips your AI coding agents (Claude Code, Gemini CLI, Cursor) with the most current patterns for adopting Liquid Glass design, Swift 6.2 language features, and Apple Intelligence frameworks.

⸻

## 🎯 Who This Is For

👨‍💻 **Senior iOS / macOS Engineers**
Engineers who need to implement features using the very latest APIs — often before they are widely documented online.

🎨 **UI / UX Specialists**
Designers and engineers adopting the Liquid Glass system across iOS, macOS, and visionOS.

⚡ **Performance Engineers**
Developers focused on low-level efficiency using new Swift types like InlineArray and Span.

⸻

## 🚀 Installation

### Manual Installation

1.  Clone this repository:
    ```bash
    git clone https://github.com/v-murygin/apple-skills.git
    ```
2.  Follow your AI agent's specific instructions for installing local skills. Typically, this involves copying the relevant skill folder (e.g., `apple-core-skill` from this repository) into a designated skills directory for your agent (e.g., `~/.gemini/skills`, `~/.claude/skills`, or similar).

### Installation with Skilz (Recommended for Multiple Agents)

Skilz is a universal skill manager that simplifies installation and synchronization across various AI agents (Claude Code, Gemini CLI, Cursor, etc.).

#### Global Installation

Install this skill globally for all your coding assistants:

```bash
skilz install https://github.com/v-murygin/apple-skills --agent claude # For Claude Code
skilz install https://github.com/v-murygin/apple-skills --agent gemini  # For Gemini CLI
# Add commands for other agents as needed
```

#### Development Mode (Symlink)

If you are actively adding or editing internal docs inside the `references/` folder and want instant updates (e.g., for local development of the skill):

```bash
skilz install --file ~/path/to/apple-engineering-playbook --agent claude --symlink
# This creates a symlink, so changes in your local repo are immediately reflected.
```

⸻

## ✨ What This Skill Offers

### 1. Modern Design System (Liquid Glass)
•    Native Implementation
•    Platform Specifics
•    visionOS

### 2. Apple Intelligence & Core ML
•    On-Device LLMs
•    Visual Intelligence
•    App Intents

### 3. Swift 6.2 & Framework Updates
•    Performance
•    Concurrency
•    StoreKit
•    MapKit

⸻

## 🧩 Skill Structure

```
apple-engineering-playbook/
├── SKILL.md                 # Main orchestration logic and decision tree
└── references/              # The "Source of Truth" markdown files
    ├── AppIntents-Updates.md
    ├── FoundationModels-Using-on-device-LLM.md
    ├── SwiftUI-Implementing-Liquid-Glass-Design.md
    ├── Swift-InlineArray-Span.md
    └── ... (other framework guides)
```

⸻

## 💡 Usage

Trigger the skill in your AI agent by referencing it explicitly:

“Review this SwiftUI view using the apple-engineering-playbook. Replace my custom blur with the native Liquid Glass implementation.”

“How do I implement local text summarization using the latest FoundationModels guide?”

⸻

## 🌟 Philosophy

This playbook is opinionated, production-focused, and intentionally ahead of public documentation. It is designed to reflect how Apple frameworks are meant to be used, not just how they are commonly used today.

If you are building for the future of Apple platforms — this is your baseline.
