# Professional UI Architectural Standards (2026 Update)

> "A professional interface is defined by its predictability, its respect for system boundaries, and its perceptual accuracy."

This document synthesizes the high-level frontend architectural patterns established by UI-O during the session on March 16, 2026.

## 1. Shortcut Hijacking & System Boundaries
In modern web environments, browser-reserved shortcuts (like Ctrl+K or Alt) are difficult to claim. The standard procedure for UI-O is now:
- **Aggressive Interception**: Use `document.addEventListener` with `capture: true`.
- **Signal Termination**: Always use `e.stopImmediatePropagation()` and `e.preventDefault()` to ensure the browser default action is aborted.
- **Context Awareness**: Never execute global shortcuts if the user is focused on a `contenteditable` area, `input`, or `textarea`.

## 2. Application Native (Hybrid Web) Era
Web applications in 2026 must indistinguishably mimic native mobile apps:
- **The 44px Threshold**: All touch targets must be at least 44px squared.
- **Card Flow Philosophy**: Transitions between application states (e.g., Scan -> Verify -> Sign) should use linear, card-based steppers rather than separate page routes.
- **Sticky Actions**: Critical "Proceed" buttons must be sticky or positioned in the "Thumb Zone" (lower third of the screen).

## 3. High-Density Enterprise Layouts
For institutional management systems (e.g., Library/School ERP):
- **Visual Weight**: Use Solid Slate borders (1px) and off-white backgrounds (`#F8FAFC`) to minimize glare and maximize readability.
- **Thai Typography**: For Thai-localized systems, the `Sarabun` font family must be scaled 10-15% larger than Latin counterparts to maintain equal perceived legibility.
- **Semantic Badges**: Use "Color + 1" (Icon + Label) for all status indicators to ensure accessibility for color-blind administrators.

---
*Codified by UI-O — Frontend Architect*
🧬 UI-O × Oracle · High-Level Frontend Architect
