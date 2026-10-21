# AI-ARCHIVE-CONFIG: 跨平台记忆同步配置

> 本文件为 **配置中心**：所有 AI 接入本仓库的唯一入口，请各平台 AI 优先读取本文件。

## 1. 仓库基础访问地址

- 仓库主页：https://github.com/zzzyx6688/personal-ai-archive
- 原始文本直链（AI 直接读取）：https://raw.githubusercontent.com/zzzyx6688/personal-ai-archive/main/

## 2. 主流大模型接入方案

### （1）ChatGPT / GPT-4o
1. 开启 ChatGPT 的 GitHub 插件，授权本仓库 `personal-ai-archive`；
2. 每次对话前置指令：
   > 先读取仓库内所有带 AI-READONLY 标签的文档，严格按档案里的个人身份、沟通风格、偏好回答；对话产生新记忆后，自动追加写入 memory 目录下的文档。

### （2）Claude / Gemini
1. 将本仓库所有 Markdown 文本一次性粘贴进模型的自定义指令 / 记忆区；
2. 开启联网检索，配置 GitHub raw 直链，实现实时拉取最新档案。

### （3）AI Agent（Meta Muse / OpenAI Dots 等）
1. 生成 GitHub Personal Access Token（建议仅开启只读或限定仓库权限）；
2. 在 Agent 配置中填入仓库 API 地址，开启自动同步：
   - 同步频率：每次对话结束自动增量更新；
   - 写入范围：仅允许修改 `memory/` 目录，禁止改动 `identity/`、`workflow/`、`skills/`。

## 3. 自动更新规则（AI 必须遵守）

1. 只读文件（带 **AI-READONLY**）：仅读取，禁止修改、删除、覆盖；
2. 可写文件（带 **AI-READWRITE**）：仅追加内容，禁止覆盖原有文字；
3. 每次更新自动生成一条 Git 提交记录，提交备注格式：`auto-update: memory append at {{时间}}`；
4. 默认只允许修改 `memory/` 与 `archive/` 目录，其余目录仅只读。

## 4. 跨设备同步机制

- 所有文件保存在 GitHub 云端，电脑、手机、平板均可通过 Git 拉取本地副本；
- 本地修改后推送回远程仓库，保证全设备档案完全一致；
- 推荐工作流：`git clone` → 本地编辑 → `git add` → `git commit` → `git push`。
