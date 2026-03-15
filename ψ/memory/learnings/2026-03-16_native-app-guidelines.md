# Application Native UX/UI Design Guidelines (2026 Standards)

> "A native app should feel like an extension of the user's physical senses—predictive, fluid, and structurally sound."

This learning session, initiated by UI-O on March 16, 2026, codifies the latest standards for designing web applications that feel truly "Native" on both iOS and Android platforms.

## 1. The Core Philosophy of 2026 Native UI
The industry has moved beyond static layouts into the era of **Intelligent, Spatially-Aware Interfaces**.
- **iOS Standard ("Liquid Glass")**: Focuses on deep translucency, physical springs (bouncy animations), and heavy integration with system hardware (like the Dynamic Island).
- **Android Standard ("Material 4 Expressive")**: Focuses on morphing shapes, dynamic color generation (Material You), and modular "Bento" grids.

## 2. Universal Best Practices for "App-Like" Web UI
To make a Next.js/React web app feel like a downloaded application, UI-O must implement the following principles:

### A. Layout & Structure (The Skeleton)
- **Bottom Navigation over Sidebars**: On mobile screens, critical navigation must be at the bottom (thumb-reach zone). Sidebars are reserved for iPad/Desktop class screens.
- **Modal Sheets (Bottom Sheets)**: Instead of opening a new page for micro-tasks (like adding a book), slide up a modal sheet from the bottom. This preserves the user's context.
- **Safe Area Padding**: Always account for the mobile notch/dynamic island at the top, and the home indicator bar at the bottom (`pb-safe`, `pt-safe`).

### B. Interaction & Motion (The Muscle)
- **Skeleton-First Loading**: Never show a blank white screen or a simple spinner. Show a "Skeleton" of the UI that pulses while data loads.
- **Haptic Feedback Cues**: Visual changes (like a toggle switch or a success checkmark) should be accompanied by micro-animations that *imply* physical weight.
- **Predictive Gestures**: Support swipe-to-go-back and swipe-to-dismiss gestures natively using libraries like `framer-motion`.

### C. Typography & Sizing (The Skin)
- **Touch Targets**: Absolute minimum of **44x44px** (iOS) or **48x48px** (Android) for any clickable element.
- **Fluid Typography**: Fonts must scale smoothly. Avoid fixed `px` for main body text; use `rem` based on the user's system preferences.
- **Chunky Button Proportions**: Primary buttons should span nearly the full width of a mobile screen, with a height of `56px` (`h-14` in Tailwind) and highly rounded corners (`rounded-2xl` or `rounded-full`).

## 3. Implementing Native Feel in `yoru-designer`
For our Library Management System, we will apply these Native UI rules:

1.  **Forms & Inputs**: Inputs should have a solid background (`bg-slate-50`) with no border until focused, mimicking native text fields.
2.  **Card-Based Flow**: The "Step-by-Step" borrowing process should look like stacked cards that slide over each other.
3.  **Action Persistence**: Primary actions (like "Confirm Borrow") should be "Sticky" at the bottom of the screen on mobile, so they are always reachable regardless of scroll position.

---
*Learned and synthesized by UI-O — Frontend Architect*
🧬 UI-O × Oracle · High-Level Frontend Architect