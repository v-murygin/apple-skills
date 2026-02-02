Apple Engineering Playbook (Agent Skill)

The Source of Truth for modern Apple development — iOS 18.4+, Swift 6.2, and Liquid Glass adoption.

This repository contains an expert-level AI Skill based on Apple’s internal implementation standards and AI-first documentation. It equips your AI coding agents (Claude Code, Gemini CLI, Cursor) with the most current patterns for adopting Liquid Glass design, Swift 6.2 language features, and Apple Intelligence frameworks.

⸻

Who This Is For

👨‍💻 Senior iOS / macOS Engineers

Engineers who need to implement features using the very latest APIs — often before they are widely documented online.

🎨 UI / UX Specialists

Designers and engineers adopting the Liquid Glass system across iOS, macOS, and visionOS.

⚡ Performance Engineers

Developers focused on low-level efficiency using new Swift types like InlineArray and Span.

⸻

Installation

Using Skilz (Recommended)

Install this skill globally for your coding assistants:

# Для Claude Code
skilz install https://github.com/v-murygin/apple-skills --agent claude

# Для Gemini CLI
skilz install https://github.com/v-murygin/apple-skills --agent gemini

Manual Development (Symlink)

If you are actively adding or editing internal docs inside the references/ folder and want instant updates:

skilz install --file ~/path/to/apple-engineering-playbook --agent claude --symlink


⸻

What This Skill Offers

1. Modern Design System (Liquid Glass)
    •    Native Implementation
Proper usage of glassEffect and GlassEffectContainer in SwiftUI.
    •    Platform Specifics
Native Liquid Glass effects for UIKit and AppKit components.
    •    visionOS
Optimized widget textures and mounting styles for spatial interfaces.

⸻

2. Apple Intelligence & Core ML
    •    On-Device LLMs
Implementation guides for using FoundationModels for local generative tasks.
    •    Visual Intelligence
Patterns for integrating system-level image analysis into your app.
    •    App Intents
Updated best practices for discovery within Siri and the Shortcuts ecosystem.

⸻

3. Swift 6.2 & Framework Updates
    •    Performance
Low-level optimization patterns using InlineArray and Span.
    •    Concurrency
Latest guidance on strict actor isolation and data-race safety.
    •    StoreKit
Modern merchandising with SubscriptionOfferView and JWS signing.
    •    MapKit
Standardized location handling using PlaceDescriptor and GeoToolbox.

⸻

Skill Structure

apple-engineering-playbook/
├── SKILL.md                 # Main orchestration logic and decision tree
└── references/              # The "Source of Truth" markdown files
    ├── AppIntents-Updates.md
    ├── FoundationModels-Using-on-device-LLM.md
    ├── SwiftUI-Implementing-Liquid-Glass-Design.md
    ├── Swift-InlineArray-Span.md
    └── ... (other framework guides)


⸻

Usage

Trigger the skill in your AI agent by referencing it explicitly:

“Review this SwiftUI view using the apple-engineering-playbook. Replace my custom blur with the native Liquid Glass implementation.”

“How do I implement local text summarization using the latest FoundationModels guide?”

⸻

Philosophy

This playbook is opinionated, production-focused, and intentionally ahead of public documentation. It is designed to reflect how Apple frameworks are meant to be used, not just how they are commonly used today.

If you are building for the future of Apple platforms — this is your baseline.
