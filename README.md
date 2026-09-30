<div align="center">

# 🧰 pearkSoar Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/Skills-2-20c997.svg)](#-技能目录)

这里的每个 Skill 都是 Agent 能直接加载的结构化指令集，遵循 [Agent Skills](https://agentskills.io/) 开放标准。Claude Code、Codex、Qoder、ZCode、CodeBuddy、Cursor 等支持该标准的 Agent 都能装。

## 📋 目录

| **技能名** | **用途** | **介绍** |
| --- | --- | --- |
| **[storage-analyzer](storage-analyzer/)** | **分析 macOS / Windows 磁盘占用，生成可折叠的 HTML 报告** | **[查看 SKILL.md](storage-analyzer/SKILL.md)** |
| **[evidence-driven](evidence-driven/)** | **管理长期 AI 协作中的阶段、证据、验证和跨会话接力** | **[查看 README](evidence-driven/README.md)** |

## 📦 安装方式

**手动：**

把需要的技能目录复制到用户级或仓库级 `.agents/skills/` 目录：

```text
<target>/.agents/skills/storage-analyzer/
<target>/.agents/skills/evidence-driven/
```

**Agent安装：**

在 Claude Code、Codex 等支持 Agent Skills 的工具里，直接说：

```
帮我安装这个 skill：https://github.com/peakSoar/pearkSoar-skills/tree/main/<skill-name>
```

把 `<skill-name>` 换成项目中的技能名字。

## ✨ Skills

### storage-analyzer（清理垃圾）

随口跟 Agent 说一句"帮我看看存储"或"C 盘满了"，它会扫一遍整机磁盘，在浏览器里打开一份**交互式 HTML 报告**：磁盘总览、占用 Top 5、清理优先级、🟢🟡🔴 三色分级清单。命令一键复制，也可以直接点按钮移到废纸篓 / 删除（每次都有二次确认弹窗）

**三色分级是核心**

- 🟢 **绿灯** — 纯缓存、临时文件，删了自动再生。可以让 Agent 一键清
- 🟡 **黄灯** — 含用户数据（离线视频、下载、项目代码）。只给"在访达打开"和"移废纸篓"，让你自己决定，不给直接删
- 🔴 **红灯** — 运行中应用核心数据、系统文件。解释为什么不能动，最多给"打开文件夹"，永远不给删除按钮

**铁律**

全程只读扫描，绝不擅自动手。删除操作必须你在浏览器上点按钮 + 浏览器弹框二次确认才执行。本地服务跑在 127.0.0.1 + 随机端口 + token，安全模型上三套白名单分级（绿灯能删、橙灯只能移废纸篓、红灯只能打开）

**怎么触发**

```
帮我看看存储
C 盘满了
清理一下磁盘
看下电脑空间
storage analysis
```

→  [SKILL.md](https://github.com/peakSoar/pearkSoar-skills/blob/master/storage-analyzer/SKILL.md) 

### evidence-driven（证据驱动开发）

给长期 AI 协作开发使用的工程 Harness。它会把任务拆成可恢复的阶段，记录每个阶段的状态、owner、验证证据和验收结果，方便跨会话继续工作，也方便审计 AI 是否真正完成了要求。

**它能做什么**

- 初始化或转换仓库级 AI Harness；
- 管理阶段目标、当前状态和 owner；
- 记录测试、验证命令和验收证据；
- 生成 `AGENTS.md`、阶段、验证和验收模板；
- 支持跨会话接力，避免长期任务丢失上下文。

**怎么触发**

```text
$evidence-driven
帮我把这个项目转换成证据驱动的开发流程
检查这个项目的阶段状态和验证证据
```

→  [README.md](https://github.com/peakSoar/pearkSoar-skills/blob/master/evidence-driven/README.md)

[MIT License](https://github.com/KKKKhazix/khazix-skills/blob/main/LICENSE) · 自由使用 / 修改 / 再分发

Made by [@pearSoar](https://github.com/peakSoar)
