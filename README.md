<div align="center">

# 🧰 pearkSoar Skills

### 我自己每天在用的一些 AI Skill，都开源在这里

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/Skills-2-20c997.svg)](#-技能目录)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Standard-7c3aed.svg)](https://agentskills.io/)
[![Codex](https://img.shields.io/badge/Codex-Compatible-1769c2.svg)](#-技能目录)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-d97706.svg)](#-技能目录)

</div>

这里的每个 Skill 都是可以单独安装的结构化指令集，适合用于 Codex、Claude Code 以及其他支持 Agent Skills 标准的工具。

## 📋 技能目录

| 技能 | 用途 | 入口 |
| --- | --- | --- |
| 💽 [storage-analyzer](storage-analyzer/) | 分析 macOS / Windows 磁盘占用，生成可折叠的 HTML 报告 | [查看 SKILL.md](storage-analyzer/SKILL.md) |
| 🔭 [evidence-driven](evidence-driven/) | 管理长期 AI 协作中的阶段、证据、验证和跨会话接力 | [查看 README](evidence-driven/README.md) |

## 📦 安装

把需要的技能目录复制到用户级或仓库级 `.agents/skills/` 目录：

```text
<target>/.agents/skills/storage-analyzer/
<target>/.agents/skills/evidence-driven/
```

安装后，在 Codex 中使用对应的技能名称调用。

## 🔗 快速跳转

- [storage-analyzer 技能目录](storage-analyzer/)
- [storage-analyzer 使用说明](storage-analyzer/SKILL.md)
- [evidence-driven 项目目录](evidence-driven/)
- [evidence-driven 项目说明](evidence-driven/README.md)
- [根目录 MIT License](LICENSE)

## 🛠️ 开发说明

本仓库脚本使用 Python 3 标准库，不需要第三方依赖。运行脚本前，先检查可用解释器：

```text
python -c "import sys; print(sys.executable)"
python3 -c "import sys; print(sys.executable)"
```

使用第一条成功返回的解释器路径运行后续脚本。

## 📄 许可证

本仓库统一采用根目录的 [MIT License](LICENSE)。
