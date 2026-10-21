# personal-ai-archive（个人 AI 档案库）

跨 AI、跨设备通用的**个人记忆系统**，一次搭建、全平台复用。

## 仓库结构

| 目录 | 用途 | 读写权限 |
| --- | --- | --- |
| `identity/` | 个人身份、职业、核心标签、人生目标 | AI 只读 |
| `workflow/` | 工作习惯、常用工具、沟通风格、任务优先级 | AI 只读 |
| `memory/` | 历史经验、重要决策、AI 对话偏好沉淀 | AI 可追加 |
| `skills/` | 已掌握技能、学习计划、待提升能力清单 | AI 只读 |
| `archive/` | 历史项目、旧文档、已完成任务归档 | AI 可追加 |
| `ai-integration.md` | 跨 AI 平台接入配置（唯一入口） | 本人维护 |

## 快速开始

1. 把 `ai-integration.md` 中的接入方案复制给任意 AI（ChatGPT / Claude / Gemini / 各类 Agent）；
2. 让 AI 先读取所有 `AI-READONLY` 文档，再开始对话；
3. 对话结束后，AI 自动把新偏好写入 `memory/`。

## 使用规则

- `AI-READONLY`：只读，AI 不得修改；
- `AI-READWRITE`：只追加，不覆盖；
- 所有修改自动生成 Git 提交记录，支持一键回退。

## 维护人

@zzzyx6688
