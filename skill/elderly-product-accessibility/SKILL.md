---
name: elderly-product-accessibility
description: Design, implement, review, or retrofit products for middle-aged and older users. Use when Codex needs to create PRDs, UX flows, UI specs, accessibility audits, acceptance criteria, Android/iOS/Web implementation guidance, elderly mode, senior-friendly page structure, interaction logic, information display, onboarding, login, forms, payments, safety, customer support, or old-product accessibility改造 for中老年用户.
---

# Elderly Product Accessibility

Use this skill to turn "适老化" from a vague request into concrete product, design, engineering, and QA decisions.

Default to Chinese deliverables unless the user asks otherwise. Treat适老化 as reducing five burdens: visual burden, cognitive burden, operation burden, trust burden, and recovery burden.

## Load References

Read `references/elderly-accessibility-baseline.md` when any of these are true:

- Creating a PRD, UI spec, design system, implementation plan, or audit report.
- Deciding numeric UI thresholds such as font size, line height, contrast, and touch target size.
- Reviewing login, payment, form, onboarding, customer support, content, learning, medical, government, or finance flows.
- Retrofitting an existing app or page for older users.

For a tiny answer, use the Quick Workflow below first and load the reference only if details are needed.

## Quick Workflow

1. Classify user capability, not just age: light, medium, heavy, and helper users.
2. Identify the user's primary task and make the first screen support "open and do".
3. Give each core page exactly one primary action. Demote secondary actions.
4. Replace feature-channel navigation with task-result navigation.
5. Use large readable typography, high contrast, large touch targets, and stable layout.
6. Avoid complex gestures, hidden controls, time pressure, auto-jumps, and ambiguous popups.
7. Make every critical action explainable, reversible, or recoverable.
8. Add obvious help: customer service, family assistance, voice reading, accessibility mode.
9. Convert design choices into measurable acceptance criteria before implementation.
10. Verify with system font scaling, TalkBack/VoiceOver, contrast checks, and real-device interaction.

## Non-Negotiables

- Do not treat "large font" as the whole solution. Redesign structure, flow, language, feedback, and recovery paths.
- Do not put ads, random popups,誘导下载,誘导付款, or deceptive buttons in elderly mode or senior-first products.
- Do not hide core functionality behind long press, swipe-only, multi-finger gestures, hover, dense menus, or carousel banners.
- Do not rely on color alone for state, error, warning, or confirmation.
- Do not make time-limited UI changes unless the time limit is essential to the task and safely communicated.
- Do not require unnecessary registration, permissions, personal data, or app downloads.
- Do not frame learning, health, finance, welfare, or service flows as competitive, shame-based, or punishment-based.

## Output Shape

When producing product or design work, include:

- `用户分层`: capability-based segments and helper-user role.
- `核心任务`: top 3 to 5 user tasks and the lowest-effort default path.
- `页面结构`: homepage, detail, list, form, result, empty, error, and help states.
- `交互逻辑`: primary action, secondary action, cancellation, undo, confirmation, and failure handling.
- `信息展示`: typography, contrast, line height, icon+text, status, amount, deadline, and plain-language rules.
- `安全信任`: permissions, privacy, payment, legal/financial confirmation, no誘导, and support escalation.
- `研发约束`: platform-specific implementation requirements and accessibility semantics.
- `验收清单`: measurable checks that QA and Codex can verify.

For old-product改造, lead with:

1. Current risk inventory.
2. P0 critical-path改造.
3. P1 common-page改造.
4. P2 design-system and accessibility hardening.
5. Regression and accessibility test plan.

## Development Guidance

For Android, prefer Jetpack Compose or native View accessibility primitives. Preserve system font scaling, set semantics/content descriptions for non-text controls, enforce minimum touch targets, test with TalkBack, and avoid custom controls that bypass accessibility services.

For iOS, support Dynamic Type, VoiceOver labels/hints/traits, sufficient hit targets, Reduce Motion, and system contrast settings. Avoid fixed-height text containers that clip under larger accessibility sizes.

For Web, align with WCAG 2.2 AA where practical: semantic landmarks/headings, keyboard navigation, visible focus, sufficient contrast, reflow, clear labels, error prevention, and no keyboard traps.

## Product Bias

Prefer calm, practical, life-oriented interfaces. For中老年 learning products, start from低心力 and positive completion: "open and learn", small daily slices, optional continuation, no ranking, no exam pressure, and one clear main action.
