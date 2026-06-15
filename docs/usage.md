# Usage

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R skill/elderly-product-accessibility ~/.codex/skills/
```

Restart Codex if needed, then invoke:

```text
使用 $elderly-product-accessibility，帮我制定适老化产品设计方案。
```

## Use Cases

### 1. 新产品立项

```text
使用 $elderly-product-accessibility，帮我为一个面向中老年用户的生活服务 App 输出 PRD。
请覆盖用户分层、核心任务、页面结构、交互逻辑、信息展示、安全信任和研发验收清单。
```

### 2. 旧产品改造

```text
使用 $elderly-product-accessibility，审查这个现有页面是否适老化。
请按 P0/P1/P2 输出问题清单和改造建议。
```

### 3. UI_SPEC

```text
使用 $elderly-product-accessibility，基于这个 PRD 输出适老化 UI_SPEC。
请包含字号、行距、触控区域、颜色对比、按钮层级、表单、弹窗、错误态、空状态和 TalkBack/VoiceOver 验收。
```

### 4. 移动端研发计划

```text
使用 $elderly-product-accessibility，基于这个设计稿输出 Android/iOS 研发落地计划。
请把适老化要求转换成组件、状态、埋点、测试和验收项。
```

### 5. QA 验收

```text
使用 $elderly-product-accessibility，帮我生成这个版本的适老化测试用例。
请覆盖系统字体放大、读屏、对比度、误触、高风险操作、错误恢复和客服入口。
```

## Recommended Workflow

1. 用 Skill 生成或审查 PRD。
2. 将页面结构和核心路径收敛到 3 到 5 个高频任务。
3. 输出 UI_SPEC，把字号、对比度、触控区域和状态反馈变成硬性验收项。
4. 研发实现时保留系统字体缩放和辅助技术语义。
5. QA 使用 checklist 做设备级验证。

## Notes

- 默认输出中文，更适合国内产品、设计和研发团队协作。
- Skill 会优先考虑中老年用户的低心力、低误触、低风险和可恢复体验。
- 对医疗、政务、金融、支付等高风险场景，应额外加强确认、凭证、客服和家人协助路径。
