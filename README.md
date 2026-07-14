# AI PRD Workflow

一个面向 AI 产品的 Codex Skill：把模糊想法、已有方案或旧 PRD，转成可评审、可交付、可上线治理的产品需求文档。

它把需求澄清、概念确认、PRD 撰写、AI 专项设计、上线评审和增量更新串成一条完整工作流。

## 能做什么

- 从零梳理 AI 产品想法，先确认用户、问题、价值与边界
- 产出概念文档，再在方向确认后生成完整 PRD
- 审阅已有 PRD，定位阻塞上线的问题并给出可替换的修改内容
- 为新增功能补齐影响范围、Eval、灰度、回滚与版本记录
- 覆盖 AI 产品常见的模型、知识库、Prompt、工具调用、权限、数据治理、成本、兜底和监控问题

## 核心原则

- 先说明为什么需要 AI，并写清楚非 AI 的基线方案
- 将证据、假设和待验证项分开，不把示例数字当成事实或通用标准
- 让每个 P0 功能具备主流程、异常路径、兜底、权限、埋点和验收条件
- 在上线前明确 Eval/NoGo、灰度门槛、回滚方案、预算预警和责任归属

## 文件结构

```text
ai-prd-workflow/
├── SKILL.md                         # Skill 工作流与使用规则
├── agents/
│   └── openai.yaml                  # Codex 展示信息
└── references/
    ├── ai-prd-playbook.md           # AI 产品 PRD 全流程方法论
    └── output-templates.md          # 概念文档、PRD、评审与变更模板
```

## 使用方式

把本仓库文件夹复制到 Codex 的 skills 目录后，重启 Codex：

```text
~/.codex/skills/ai-prd-workflow/
```

在 Windows 上，通常对应：

```text
C:\\Users\\你的用户名\\.codex\\skills\\ai-prd-workflow\\
```

然后可以直接这样提需求：

```text
用 ai-prd-workflow 帮我把这个 AI 产品想法写成 PRD。
```

或：

```text
用 ai-prd-workflow 审阅这份 PRD，按阻塞上线、重要缺口、可优化项给出修改建议。
```

## 适用场景

- AI 助手、智能体、RAG、LLM 功能
- AI 功能的需求拆解与 MVP 定义
- 模型效果评估、人工兜底与风险治理
- 上线评审、灰度发布、成本和监控设计
- 既有 AI PRD 的诊断与增量更新

## 来源与边界

本 Skill 整合了 AI 产品 PRD 写作方法论、`prd-writer` 的文档结构化能力和 `brainstorming` 的需求澄清方式。它会将未验证的数据、案例和阈值标为待验证，而不会把它们写成已证实事实。
