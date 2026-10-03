---
name: apple-internal-docs
description: Consult Apple Internal Documentation bundled with Xcode 26/27 (iOS 26+, macOS 26+, visionOS 26+). Use when implementing modern frameworks (StoreKit, MapKit, WebKit, AlarmKit), adopting design systems (Liquid Glass), or using new Swift features (SwiftData inheritance, InlineArray).
allowed-tools: Read, Grep, Glob
---

# Apple Internal Documentation

## Overview
Use this skill to access and apply the latest Apple API documentation and implementation guides. These documents contain the source of truth for Xcode 26/27 (iOS 26+), Swift 6.2, and new design paradigms like Liquid Glass. Prioritize patterns found here over general web knowledge.

## Workflow Decision Tree
Choose the path that matches the request:

### 1) Research an API or Feature
- **Search**: Use `grep` or `glob` in `references/` for keywords (e.g., "PlaceDescriptor", "WebView", "AppTransaction").
- **Identify**: Select the specific markdown file covering the domain.
- **Read**: Analyze the "Overview" and "Usage" sections.

### 2) Implement a Feature
- **Design System**: If building UI, check `*-Implementing-Liquid-Glass-Design.md` for the specific framework (SwiftUI/UIKit/AppKit).
- **Data Models**: Use `SwiftData-Class-Inheritance.md` for complex models or `MapKit-GeoToolbox-PlaceDescriptors.md` for location data.
- **Commerce**: Refer to `StoreKit-Updates.md` for subscriptions and JWS signing.
- **Web**: Use the native `WebView` and `WebPage` from `SwiftUI-WebKit-Integration.md`.

### 3) Review & Refactor
- Check code against "Best Practices" in the relevant doc.
- Verify availability checks (e.g., `#available(iOS 18.4, *)` for new StoreKit features).
- Ensure accessibility compliance (e.g., `Implementing-Assistive-Access-in-iOS.md`).

## Core Guidelines
- **Liquid Glass**: Use native APIs (`glassEffect`, `UIGlassEffect`) instead of custom blurs. See specific files for SwiftUI, UIKit, AppKit, or WidgetKit.
- **SwiftData**: Prefer class inheritance for hierarchical models over flat structures when appropriate.
- **MapKit**: Use `PlaceDescriptor` and `GeoToolbox` for standardized location handling.
- **StoreKit**: Implement `SubscriptionOfferView` for merchandising and check `AppTransaction.shared` for attribution.
- **VisionOS**: Handle specific widget textures (`.glass` vs `.paper`) and mounting styles (`.recessed` vs `.elevated`).

## Implementation Checklist
- **Doc Selection**: Identified correct file in `references/`.
- **Availability**: Guarded code with correct `#available` checks (note: some features are iOS 18.4+).
- **Patterns**: Used specific snippets (e.g., `GlassEffectContainer`, `WebView(page)`).
- **Configuration**: Applied necessary Info.plist keys (e.g., for AlarmKit or Assistive Access).
- **Performance**: Verified against performance notes (e.g., `InlineArray` for hot paths).

## Resources
The following documentation is available in the `references/` directory:

### Core Frameworks & Swift
- `references/AppIntents-Updates.md`
- `references/Foundation-AttributedString-Updates.md`
- `references/FoundationModels-Using-on-device-LLM-in-your-app.md`
- `references/Swift-Concurrency-Updates.md`
- `references/Swift-InlineArray-Span.md`
- `references/SwiftData-Class-Inheritance.md`

### Liquid Glass Design System
- `references/SwiftUI-Implementing-Liquid-Glass-Design.md`
- `references/UIKit-Implementing-Liquid-Glass-Design.md`
- `references/AppKit-Implementing-Liquid-Glass-Design.md`
- `references/WidgetKit-Implementing-Liquid-Glass-Design.md`

### App Services
- `references/StoreKit-Updates.md`
- `references/MapKit-GeoToolbox-PlaceDescriptors.md`
- `references/SwiftUI-AlarmKit-Integration.md`
- `references/Implementing-Visual-Intelligence-in-iOS.md`
- `references/Implementing-Assistive-Access-in-iOS.md`

### SwiftUI Components
- `references/SwiftUI-WebKit-Integration.md`
- `references/SwiftUI-Styled-Text-Editing.md`
- `references/SwiftUI-New-Toolbar-Features.md`
- `references/Swift-Charts-3D-Visualization.md`
- `references/Widgets-for-visionOS.md`
