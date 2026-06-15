# Elderly Product Accessibility Skill

一个用于中老年产品新建、旧产品改造、UI 审查和研发验收的 Codex Skill。

适老化不是把字体放大，而是系统性降低用户的视觉负担、认知负担、操作负担、信任负担和恢复负担。本仓库把这套方法沉淀成可复用的 Codex Skill，方便在后续产品开发中快速生成 PRD、UI_SPEC、改造方案和验收清单。

## What It Helps With

- 生成中老年产品 PRD
- 审查旧 App / Web 页面是否适老化
- 输出适老化 UI_SPEC
- 生成 Android / iOS / Web 研发落地要求
- 生成 QA 可执行的适老化验收清单
- 将工信部适老化规范、WCAG、Android/iOS 可访问性建议转成产品和研发语言

## Repository Structure

```text
.
├── skill/
│   └── elderly-product-accessibility/
│       ├── SKILL.md
│       ├── agents/
│       │   └── openai.yaml
│       └── references/
│           └── elderly-accessibility-baseline.md
├── docs/
│   ├── 适老化产品设计基线.md
│   ├── usage.md
│   └── checklist.md
├── examples/
│   ├── prd-example.md
│   ├── ui-spec-example.md
│   └── audit-report-example.md
├── CHANGELOG.md
└── LICENSE
```

## Quick Start

Copy the skill folder into your Codex skills directory:

```bash
cp -R skill/elderly-product-accessibility ~/.codex/skills/
```

Then use it in Codex:

```text
使用 $elderly-product-accessibility，帮我为一个面向中老年用户的学习 App 输出 PRD、页面结构、交互逻辑和研发验收清单。
```

For more usage patterns, see [docs/usage.md](docs/usage.md).

## Example Prompts

New product PRD:

```text
使用 $elderly-product-accessibility，帮我为一个面向中老年用户的健康管理 App 输出 PRD。
请覆盖用户分层、核心任务、首页结构、核心流程、信息展示、交互反馈、安全信任、研发验收标准。
```

Old product retrofit:

```text
使用 $elderly-product-accessibility，审查这个现有 App 页面是否适老化。
请按 P0/P1/P2 输出改造优先级，并给出页面结构、交互、信息展示、可访问性和安全信任问题。
```

UI spec:

```text
使用 $elderly-product-accessibility，为这个产品制定适老化 UI_SPEC。
请包含字体、行距、触控区域、颜色对比、按钮层级、表单、弹窗、错误态、空状态和辅助技术验收。
```

## Design Baseline

核心判断:

- 首页按任务组织，不按业务频道组织。
- 每个核心页面只保留一个主动作。
- 默认路径要短，进阶路径可隐藏。
- 错误要解释原因和解决办法。
- 高风险操作必须可确认、可取消、可修改或可联系客服。
- 适老版不应出现广告插件、诱导下载、诱导付款或欺骗性按钮。

详细规范见 [docs/适老化产品设计基线.md](docs/适老化产品设计基线.md)。

## References

- 工信部《移动互联网应用(APP)适老化通用设计规范》
- WCAG 2.2
- Android Accessibility
- Apple Human Interface Guidelines

## License

This repository is released under [CC BY 4.0](LICENSE). You may share and adapt the contents with attribution.
